# Transparent VIM background with true color patch
## Decription
Patch allows you to use transparent VIM background and 24-bit true color same time.
Example *.vimrc*:
```
set termguicolors
highlight Normal guibg=NONE
highlight NonText guibg=NONE
highlight Folded guibg=NONE cterm=NONE term=NONE
```

## Installation
Just use this patch by `patch` command and make vim.

Or with homebrew:
1. `brew edit vim`
1. Add after `depends_on ...`
```
  patch do
    url "https://raw.githubusercontent.com/istarukhin/vim-guibg-truecolor-fix/master/fix_guibg_truecolor.patch"
    sha256 "56100a3cc51242aff6334549b56cfcfc3987f6ef299741c18c7245828b53129b"
  end if build.with? "fix-guibg"
```
1. Add `option "with-fix-guibg", "Fixes guibg with truecolor"` to options
1. Save file
1. `brew uninstall vim`
1. `brew install vim --with-fix-guibg`
