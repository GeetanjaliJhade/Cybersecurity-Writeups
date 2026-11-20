# Server-Side Request Forgery (SSRF)

## Overview

Server-Side Request Forgery (SSRF) is a web security vulnerability that occurs when an application fetches resources from a URL or another external source without properly validating or restricting the user's input.v

An attacker may exploit this vulnerability to make the server send unauthorized requests to internal systems, external services, or other restricted resources.

## Potential Impact

- **Internal Network Access:** Access internal services that are not publicly exposed.
- **Sensitive Information Disclosure:** Retrieve information from internal resources or services.
- **Cloud Metadata Exposure:** Potentially access sensitive cloud instance metadata.
- **Unauthorized Requests:** Make requests to systems using the server's network privileges.

## Common Types

- Basic SSRF
- SSRF with blacklist-based input filters
- SSRF with whitelist-based input filters
- SSRF with filter bypass techniques

## Prevention

- Validate and sanitize user-supplied URLs.
- Use allowlists to restrict permitted domains and destinations.
- Block requests to private, loopback, and link-local IP addresses.
- Disable unnecessary URL schemes and redirects.
- Implement network-level restrictions and monitor outgoing requests.

## Writeups

This folder contains my practical research and writeups on Server-Side Request Forgery (SSRF). It covers different SSRF scenarios, including basic exploitation, input-filter restrictions, and filter bypass techniques, with documented testing steps and findings.
