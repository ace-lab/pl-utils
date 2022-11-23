# pl-utils: *nix command-line utilities for working with PrairieLearn content

These require Ruby 2 or 3 to be installed.

`pl-tag {add|remove|set} tag1,tag2,tag3 file1.json file2.json`

Add, remove, or set `tags` field in each JSON file (usually the
`info.json` associated with a question), which is overwritten in
place.  Files with errors are skipped.  If a tag to be added already
exists in the file, it is not duplicated.  If a tag to be removed
doesn't already exist, it's fine.

To do it to lots of files, try `find . `_(conditions for find)_`|xargs pl-tag add foobar`

**Warning:** Files are overwritten in place!  Be careful/do a git commit first!

