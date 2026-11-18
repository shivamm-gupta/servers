---
"@modelcontextprotocol/server-filesystem": patch
---

`move_file` now rejects an attempt to move a directory into itself or a subdirectory of itself with `EINVAL` up front, instead of renaming the source directory first and reporting `Parent directory does not exist` for a destination parent that does exist (#5555).
