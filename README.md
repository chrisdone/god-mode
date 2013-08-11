# God Mode

This is a global minor mode for entering Emacs commands without
modifier keys. It's similar to Vim's separation of commands and
insertion mode. Activate by running `M-x god-mode`.

Toggle between God mode and non-God mode using `ESC`:

    (global-set-key (kbd "<escape>") 'god-local-mode)

## Mapping

This library defines the following mapping:

* All commands are assumed to be `C-<something>` unless otherwise
   indicated. Examples:

   * `a`    → `C-a`
   * `s`    → `C-s`
   * `akny` → `C-a C-k C-n C-y`
   * `xs`   → `C-x C-s`
   * `x s`  → `C-x s`

   Note the use of space to produce `C-x s`.

* `g` is a special key to indicate `M-<something>`. This means that
   there is no way to write `C-g` in this mode, you must therefore
   type `C-g` directly. Examples:

   * `gf` → `M-f`
   * `gx` → `M-x`

* `G` is a special key to indicate `C-M-<something>`. Example:

   * `Gx` → `C-M-x`

* Digit arguments:

  * `12f` → `M-12 C-f`

* Repetition:

  * `gfzz` → `M-f M-f M-f`

* Universal boolean argument:

  * `uco` → `C-u C-c C-o`

* There is a key (default `i` - think *insert*) to disable God mode,
  similar to Vim's i.

## Not implemented yet

* C- with backspace and arrow keys don't quite work, not looked into
  it yet.
