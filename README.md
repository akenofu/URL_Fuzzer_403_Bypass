# URL Fuzzer 401/403 Bypass

Fuzzes the URL with all available unicode characters to identify parser inconsistencies. Based on the research of Rafael da Costa Santos (https://rafa.hashnode.dev/exploiting-http-parsers-inconsistencies).

## Demo



## How it works 
Inserts all ASCII characters (0-255) at pre-defined insertion points in the URL.
For the path `/admin/dashboard`, the following transformations are done:
- `0x85/admin/dashboard`
- `/0x85/admin0x85/dashboard`
- `/admin0x85/dashboard`
- `/admin/dashboard0x85`
- `/admin/dashboard/0x85/`

And, more...