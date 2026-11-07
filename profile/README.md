# Masscollabs Cloud Platform

[Türkçe](README.tr.md) | English

Organization-wide community health and profile repository for the
Masscollabs Cloud Platform, maintained by
[Masscollabs Services Masscollabs](https://masscollabs.xyz).

## About

Masscollabs Cloud Platform is a family of cloud computing services written in
the [Go programming language](https://go.dev) and released under the
**GNU Affero General Public License, version 3 or (at your option) any later
version (AGPL-3.0-or-later)**. Every service is built for cloud computing
scenarios and is held to a military-grade standard of code quality and
resilience.

## Engineering Principles

The following principles are the quality bar for code in this organization.
They are goals that every repository is expected to meet and be reviewed
against.

- **Resilience first:** Services must tolerate partial failure. Use timeouts,
  context cancellation, bounded retries with backoff, circuit breakers, and
  graceful shutdown on every network boundary.
- **Secure by default:** Validate all input, apply least privilege, keep
  secrets out of source control, and keep dependencies minimal, pinned, and
  scanned for known vulnerabilities (for example with `govulncheck`).
- **Deterministic quality gates:** Code must pass `gofmt`, `go vet`, static
  analysis (for example `staticcheck` or `golangci-lint`), and the race
  detector (`go test -race`) before it is merged.
- **Test rigor:** Unit, integration, fuzz, and benchmark tests accompany
  changes, with failure paths covered as thoroughly as success paths.
- **Observability:** Structured logging, metrics, and distributed tracing
  (for example OpenTelemetry) are part of the design, not an afterthought.
- **Reproducible builds:** Builds are versioned through Go modules and must
  be reproducible and auditable.
- **Operational clarity:** Health and readiness endpoints, explicit
  configuration, and documented failure modes are required.

## Licensing

All code in this organization is licensed under AGPL-3.0-or-later. Because the
AGPL extends copyleft to network use, anyone who runs a modified version of
these services for remote users must offer those users the corresponding
source code. See [LICENSE](LICENSE) for the full license text.

## Contributing

1. Fork the relevant repository and create a topic branch.
2. Make focused changes and add or update tests.
3. Run the quality gates listed above locally.
4. Record user-visible changes in [ChangeLog](ChangeLog).
5. Open a pull request. By contributing, you agree that your work is
   licensed under AGPL-3.0-or-later.

## Links

- Website: <https://masscollabs.xyz>

## License

Copyright (C) 2017-2027 Masscollabs Services

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
