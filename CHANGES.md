# Changes from upstream (markdownextra plugin, 2013-01-14)

- `markdown.php`: replaced curly brace string/array offset access (`$str{0}`, `$tag{1}`,
  `$matches[2]{0}`, ...) with square brackets. Curly brace offsets were removed in PHP 8
  and caused: "Array and string offset access syntax with curly braces is no longer supported".
  18 occurrences changed; behaviour is identical.
- Nothing else was modified. Original copyright and license notices are unchanged.
