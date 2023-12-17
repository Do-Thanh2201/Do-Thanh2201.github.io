# Hướng dẫn build
Tài liệu này sử dụng [mkdocs](https://www.mkdocs.org/) để tự động generate static HTML page
## Cài đặt môi trường
- Cài đặt Python
- Install mkdocs ở local: pip install mkdocs
- Create new docs source project: tại thư mục muốn tạo, chạy cmd: mkdocs new GITHUB_PROJECT
## Hướng dẫn chạy local
- mkdocs build --config-file mkdocs.yml --site-dir build/state
- mkdocs serve --config-file mkdocs.yml
## Hướng dẫn chạy trên git repo
- echo build/ > .gitignore
- git status
- git add <files>
- git commit -m "Message"
- git push
- Build file ở local
- mkdocs gh-deploy --remote-branch buildPage --config-file mkdocs.yml --site-dir build/state
(Tạo ra 1 branch buildPage từ nhánh main, copy file trong thư mục build/state ở local push lên branch buildPage đồng thời ở github page, setting deploy từ nhánh buildPage)
## Tham khảo tài liệu
[Command Line Interface](https://www.mkdocs.org/user-guide/cli/)