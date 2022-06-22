Attempt to offset and pad a file with leading or trailing zeroes to match a crc32 and size.
The matching is fairly fast, so it can be quickly used on e.g. full disc images.

Usage: `crcoffset infile target_size target_crc [outfile]`

`target_size` is decimal, `target_crc` is hexadecimal.
If `outfile` is provided the first match found will be written there.

If a match is found the output will be `drop X` or `pad X`, where X
is a number of bytes in decimal.
