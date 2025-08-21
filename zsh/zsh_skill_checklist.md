# Zsh Skill Checklist

## Cấp 1 — Làm quen
- [ ] Đặt zsh làm shell mặc định (chsh -s /bin/zsh)
- [ ] Hiểu cấu trúc lệnh cơ bản
- [ ] Điều hướng file/thư mục: pwd, cd, ls, mkdir, rm
- [ ] Biết alias cơ bản
- [ ] Sử dụng history (↑, ↓)

## Cấp 2 — Người dùng quen tay
- [ ] Cài plugin cơ bản: autosuggestions, syntax-highlighting, completions
- [ ] Tìm lệnh bằng Ctrl+R
- [ ] Tạo function đơn giản (mkcd)
- [ ] Dùng setopt cơ bản (autocd, noclobber, extended_glob)
- [ ] Dùng globbing đơn giản
- [ ] Quản lý biến môi trường trong ~/.zshrc

## Cấp 3 — Power-user
- [ ] Hiểu globbing nâng cao (**/*.md, *(.om[1,5]))
- [ ] Quản lý array & parameter expansion
- [ ] Dùng fzf, zoxide
- [ ] Tùy biến prompt (powerlevel10k hoặc PROMPT thủ công)
- [ ] Thành thạo git CLI
- [ ] Script nhỏ build/test project Flutter

## Cấp 4 — Automation & scripting
- [ ] Viết script với if, for, while
- [ ] Sử dụng expansion nâng cao (${(s: :)var})
- [ ] Dùng zmv để rename file hàng loạt
- [ ] Tích hợp script vào CI/CD hoặc git hook
- [ ] Hiểu & chỉnh compdef để viết completion riêng
- [ ] Dùng cron để chạy script định kỳ

## Cấp 5 — Lão luyện
- [ ] Hiểu autoload, compinit, zcompile để tối ưu tốc độ
- [ ] Viết plugin zsh cho riêng mình
- [ ] Viết widget zsh (zle)
- [ ] Quản lý dotfiles với git
- [ ] Kết hợp tmux + zsh + neovim thành IDE
- [ ] Debug script bằng set -x, whence, which -a
