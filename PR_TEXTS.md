# PR Texts for Lab 5

Use these texts when opening PRs in sequence.

## PR 1

Base branch: `master`
Head branch: `pr/01-cli`

Title:
`feat: add go2web CLI skeleton`

Description:
```
## Summary
- add executable `go2web` entry point
- add CLI parser with options: `-h`, `-u`, `-s`, `-v`
- add minimal main flow and placeholders for modes

## Why
This PR creates the base command-line interface required by Lab 5.

## Validation
- run `./go2web -h`
- verify help includes `-u` and `-s`
```

## PR 2

Base branch: `pr/01-cli`
Head branch: `pr/02-http`

Title:
`feat: implement raw HTTP over TCP with URL mode`

Description:
```
## Summary
- add TCP socket connection logic for HTTP and HTTPS (TLS)
- implement manual HTTP GET request builder
- implement HTTP response parser (status line, headers, body)
- add chunked transfer decoding
- implement redirects handling (301/302/303/307/308)
- implement `-u <URL>` mode output

## Why
This PR implements core lab requirement: HTTP over sockets without HTTP client libraries.

## Validation
- run `./go2web -u 'https://utm.md/en/'`
- verify status line and readable body output
```

## PR 3

Base branch: `pr/02-http`
Head branch: `pr/03-search`

Title:
`feat: add duckduckgo lite search with top 10 results`

Description:
```
## Summary
- add HTML parser for DuckDuckGo Lite result links
- implement `-s <search-term>` mode
- normalize links and print top 10 unique results

## Why
This PR closes second mandatory CLI mode from lab: search term and print top 10 results.

## Validation
- run `./go2web -s 'technical university moldova'`
- verify top 10 results are shown with titles and links
```

## PR 4

Base branch: `pr/03-search`
Head branch: `pr/04-docs`

Title:
`docs: add lab5 usage and submission notes`

Description:
```
## Summary
- update README to Lab 5 scope
- add run instructions and feature list
- document constraints compliance
- add demo GIF placeholder section

## Why
This PR prepares repository documentation for submission and class presentation.

## Validation
- open README and verify all lab requirements are documented
```

## Suggested labels
- `lab5`
- `feature` for PR 1-3
- `documentation` for PR 4

## Push commands

```bash
git push -u origin pr/01-cli
git push -u origin pr/02-http
git push -u origin pr/03-search
git push -u origin pr/04-docs
```
