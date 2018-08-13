## Compression Tech Test

You are given this text in `bible.txt`, in which is a copy of The Bishops' Bible, an old English bible, processed by optical character recognition software.

Your task is to create two programs, a `compressor` which produces a compressed file, and a `decompressor` which, given the compressed file, produces the original file again.

Your challenge is to make the sum of the size of `bible_compressed.txt` and `decompress` as small as possible.

```bash
$ ./compress bible.txt > bible_compressed.txt
$ ./decompress bible_compressed.txt > bible_original.txt

$ md5 bible.txt
MD5 (bible.txt) = 833640dfb9cb25e2ac0ae3f4496331f7

$ md5 bible_original.txt
MD5 (bible_original.txt) = 833640dfb9cb25e2ac0ae3f4496331f7

# The two hashes are the same

$ ls -l bible_compressed.txt decompress
-rw-r--r--@ 1 kay  staff  181266 13 Aug 15:55 bible_compressed.txt
-rwxr-xr-x  1 kay  staff      71 13 Aug 15:55 decompress

# The smaller the sum is  ^^^^^^ the better.
# In this case it is 181,266 + 71 = 181,337
# (The original is 181,486, so this is a saving of 149 bytes)
```

I have included a simple version of `compress` and `decompress` to get you started.

No external compression libraries allowed, of course.

## Bonus

Runtimes (e.g. the Ruby interpreter) are quite large. Write `decompress` to have no external dependencies. You may wish to consider using a compiled language like C.

Then you can sum the size of `bible_compressed.txt` and `decompress` and have genuine compression going on! What a lovely feeling!
