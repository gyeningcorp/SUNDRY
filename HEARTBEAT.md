# Heartbeat Tasks

## nmap — Go-Gig public surface scan
Run a light TCP scan on Go-Gig public endpoints and flag any unexpected open ports.

- Targets: `api.go-gig.org`, `go-gig.org`
- Command: `nmap -Pn -T4 --top-ports 100 api.go-gig.org go-gig.org`
- Expected open: 80, 443 only
- Alert if: any other port shows open/filtered-as-open, or 443 stops responding
