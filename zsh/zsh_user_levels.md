# Đánh Giá Cấp Độ Người Dùng Zsh

## Cấp 1: Người mới làm quen
- Mới cài zsh, thường để có prompt đẹp (oh-my-zsh, powerlevel10k).
- Dùng zsh gần giống bash: cd, ls, mkdir, rm.
- Chưa tận dụng globbing, history hay completion nâng cao.
- **Đặc điểm:** Có theme, nhưng workflow chưa khác mấy so với bash.

## Cấp 2: Người dùng quen tay
- Cài plugin phổ biến: autosuggestions, syntax highlighting, zsh-completions.
- Dùng history search (Ctrl+R) thành thạo.
- Biết alias và function cơ bản (mkcd).
- Bật setopt cơ bản (autocd, noclobber, extended_glob).
- **Đặc điểm:** Workflow CLI dần mượt, thay thế GUI trong nhiều việc.

## Cấp 3: Power-user
- Khai thác globbing nâng cao: **/*.dart, *(.om[1,5]).
- Dùng array và parameter expansion.
- Tích hợp zoxide, fzf, direnv vào workflow.
- Tùy biến prompt với powerlevel10k hoặc PROMPT thủ công.
- Sử dụng plugin manager (zinit, antibody) để tối ưu.
- **Đặc điểm:** Làm việc thuần terminal thoải mái, CLI > GUI.

## Cấp 4: Automation & scripting
- Viết script zsh khai thác tính năng riêng (zmv, array mạnh).
- Tích hợp script vào CI/CD, git hook, build system.
- Tự viết completion bằng compdef.
- Config nhẹ, khởi động nhanh.
- **Đặc điểm:** Zsh thành “automation language”, không chỉ shell.

## Cấp 5: Người dùng lão luyện
- Tùy biến sâu .zshrc, không cần framework nặng.
- Hiểu autoload, compinit, zcompile để tăng tốc.
- Viết plugin hoặc widget zle cho zsh.
- Quản lý dotfiles với git, sync nhiều máy.
- Kết hợp tmux + zsh + neovim thành IDE full terminal.
- Debug script bằng set -x, whence, which -a.
- **Đặc điểm:** Làm chủ hoàn toàn môi trường, workflow cực nhanh và tự động hóa cao.
