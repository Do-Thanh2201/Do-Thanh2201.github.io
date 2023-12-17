# Hướng dẫn build
Tài liệu này sử dụng mkdocs để tự động generate static HTML page
## Cài đặt môi trường
- Cài đặt Python
- Install mkdocs ở local: pip install mkdocs
- Create new docs source project: tại thư mục muốn tạo, chạy cmd: mkdocs new GITHUB_PROJECT
## Hướng dẫn chạy local
- mkdocs build --config-file mkdocs.yml --site-dir build
- mkdocs serve --config-file mkdocs.yml
## Hướng dẫn chạy trên git repo
- echo build/ > .gitignore
- git status
- git add <files>
- git commit -m "Message"
- git push
- mkdocs gh-deploy --remote-branch build
(Tạo ra 1 branch build từ nhánh main, đồng thời ở github page, setting deploy từ nhánh build)
## Tham khảo tài liệu
[Trang chủ của mkdocs](https://www.mkdocs.org/user-guide/configuration/#configuration)