# Changes from upstream (markdownextra plugin, 2013-01-14)

- `markdown.php`: replaced curly brace string/array offset access (`$str{0}`, `$tag{1}`,
  `$matches[2]{0}`, ...) with square brackets. Curly brace offsets were removed in PHP 8
  and caused: "Array and string offset access syntax with curly braces is no longer supported".
  18 occurrences changed; behaviour is identical.
- Nothing else was modified. Original copyright and license notices are unchanged.
- `markdown.php`: renamed the PHP 4 style constructors `Markdown_Parser()` and
  `MarkdownExtra_Parser()` to `__construct()` (and the `parent::` call accordingly).
  PHP 8 no longer treats a method named like its class as a constructor, so the parser was
  never initialised, which caused "preg_split(): Empty regular expression" warnings and
  broken emphasis (`*em*`, `**strong**`).
