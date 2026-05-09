# Command-line `diff` and `patch` examples

## Example A: Use `diff` to compare two files

Two people have been working on a project, Anna and Fred.  Anna starts the project, and sends a copy to Fred to add his section.  Fred now wants to check his changes, so he creates a `diff` of the two files.

```bash
# No colour.
diff -u  anna/sample.md fred/sample.md
# Colour output.  Note the different parameters.  Both work!
$ diff --color=auto -u anna fred
```

```diff
--- anna/sample.md      2026-05-09 15:41:48.459090115 +0100
+++ fred/sample.md      2026-05-09 15:42:54.083991014 +0100
@@ -1,3 +1,7 @@
 # Sample

 This is Anna's version.  She had the original idea.
+
+## Heading 2
+
+Fred added some more text here about something else.
```

You can see the lines that have been changed, `-` indicates line removed, `+` indicates line added.  The `-u` stands for "unified" which shows a small amount of context around the change (default 3 lines before and 3 lines after).  Unified diffs are the standard format for `patch`.

## Example B: Create and apply a patch

Fred wants to send his changes to Anna, but does't want to send a complete copy of all of the whole project.  Instead, he creates a `patch` file and sends that instead.

```bash
# Create patch file from original -> updated
$ diff -u anna fred > update.patch
```

Fred sends the patch file to Anna and she applies it to her work.

Anna copies her work into a new directory, `anna2`.

```bash
cd ..  # diff-patch-demo
cp -r anna anna2
```

Applies the patch.

```bash
$ patch anna2/sample.md < update.patch

# Print contents of the modified file.
$ cat anna2/sample.md
```

```md
# Sample

This is Anna's version.  She had the original idea.

## Heading 2

Fred added some more text here about something else.
```
