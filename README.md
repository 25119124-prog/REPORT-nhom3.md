# REPORT-nhom3.md
Content is user-generated and unverified.
2
BÁO CÁO BÀI TẬP THỰC HÀNH GIT - TUẦN 4
Thông tin nhóm
Tên nhóm: [nhóm 3]
Môn học: nhập môn kỹ thuật máy tính
Giảng viên: [Huỳnh Thế Thiện]
1. Link Repository
Link repo nhóm (Public): https://github.com/25119124-prog/ktmt-nhapmon1
2. Link Pull Requests đã merge
PR #1: Khởi tạo cấu trúc dự án
Link: https://github.com/username/ktmt-nhapmon/pull/1
Mô tả: Tạo cấu trúc thư mục cơ bản, thêm README.md và .gitignore
Người tạo: Trần Trọng Nghĩa,Nguyễn Hữu Thông
Trạng thái: ✅ Merged
PR #2: Thêm thông tin thành viên nhóm
Link: https://github.com/25119124-prog/ktmt-nhapmon1/pull/2
Mô tả: Cập nhật README.md với thông tin đầy đủ của các thành viên
Thành viên và nhiệm vụ:
STT  Họ và tên           MSSV      Nhiệm vụ                         Đóng góp    Link thông tin
1    Trần Trọng Nghĩa    2012345   Team Leader, Setup repo...        30%
2    Trần Phúc Bảo       2012346   Cập nhật README, Quản lý issues   15%        https://github.com/25119056-baobao/nhapmon-ktmt.git
3    Huỳnh Lê Anh Kha    2012347   Viết tài liệu, Tạo branch         15%
4    Nguyễn Minh Quang   2012348   Test và merge PR, Báo cáo         15%
5    Nguyễn Hữu Thông    25119159  Cập nhật README.md (PR #2)        15%        https://github.com/thongngury/NHT-KTMT-NHAPMON.git
6    Huỳnh Gia Bảo       25119055  Tạo file Guide.md (PR #3)         10%
Người tạo: Trần Phúc Bảo, Huỳnh Gia Bảo
Trạng thái: ✅ Merged
PR #3: Hoàn thiện tài liệu hướng dẫn
Link: https://github.com/username/ktmt-nhapmon/pull/3
Mô tả: Thêm file GUIDE.md hướng dẫn sử dụng Git cơ bản
Người tạo: Nguyễn Minh Quang, Huỳnh Lê Anh Kha
Trạng thái: ✅ Merged
3. Thành viên và nhiệm vụ
STT	Họ và tên	MSSV	Nhiệm vụ	Đóng góp
1  Trần Trọng Nghĩa, Nguyễn Hữu Thông	2012345	Team Leader, Setup repo, Review PR	30%
2	Trần Phúc Bảo, Huỳnh Gia Bảo	2012346	Cập nhật README, Quản lý issues	25%
3 Huỳnh Lê Anh Kha	2012347	Viết tài liệu, Tạo branch	25%
4 Nguyễn Minh Quang	2012348	Test và merge PR, Báo cáo	20%
Chi tiết công việc:
Nguyễn Hữu Thông

Khởi tạo repository trên GitHub
Cấu hình branch protection rules
Trần Trọng Nghĩa:
Review và merge các PR
Giải quyết conflicts
Trần Phúc Bảo:

Cập nhật thông tin nhóm trong README.md
Tạo và quản lý issues
Huỳnh Gia Bảo:
Viết commit messages theo chuẩn
Huỳnh Lê Anh Kha:

Tạo các branch feature
Viết tài liệu hướng dẫn Git
Thực hiện rebase và squash commits
Nguyễn Minh Quang:

Kiểm tra code trước khi merge
Tổng hợp báo cáo
Hỗ trợ giải quyết conflicts
4. Lệnh Git đã dùng nhiều nhất
Top 5 lệnh sử dụng thường xuyên:
git status - Kiểm tra trạng thái working directory và staging area
bash
   # Sử dụng liên tục để theo dõi thay đổi
   git status
git add - Thêm file vào staging area
bash
   git add README.md
   git add .  # Thêm tất cả file đã thay đổi
git commit - Tạo commit với message mô tả
bash
   git commit -m "docs: Update README with team info"
   git commit -m "feat: Add new feature"
   git commit -m "fix: Resolve merge conflict"
git push - Đẩy commits lên remote repository
bash
   git push origin main
   git push origin feature-branch
git pull - Cập nhật code mới nhất từ remote
bash
   git pull origin main
   # Hoặc
   git pull --rebase origin main
Các lệnh khác thường dùng:
bash
# Tạo và chuyển sang branch mới
git checkout -b feature/new-feature

# Xem lịch sử commit
git log --oneline --graph

# Xem diff trước khi commit
git diff

# Clone repository
git clone https://github.com/username/repo.git

# Xem danh sách branch
git branch -a

# Merge branch
git merge feature-branch

# Xóa branch đã merge
git branch -d feature-branch
5. Khó khăn gặp phải và cách giải quyết
Khó khăn 1: Merge Conflicts
Vấn đề: Khi nhiều người cùng chỉnh sửa một file, xảy ra xung đột khi merge.

Cách giải quyết:

bash
# 1. Pull code mới nhất
git pull origin main

# 2. Git sẽ báo conflict, mở file để xem
# 3. Sửa các phần conflict (giữa <<<< và >>>>)
# 4. Sau khi sửa xong:
git add conflicted-file.md
git commit -m "fix: Resolve merge conflict in README"
git push
Bài học: Luôn pull code mới nhất trước khi bắt đầu làm việc và chia nhỏ công việc để tránh conflict.

Khó khăn 2: Quên commit message hoặc viết sai
Vấn đề: Đã commit nhưng message không rõ ràng hoặc sai format.

Cách giải quyết:

bash
# Sửa commit message của commit cuối cùng
git commit --amend -m "docs: Update README with correct information"

# Nếu đã push, cần force push (cẩn thận!)
git push --force-with-lease
Khó khăn 3: Push nhầm code lên main branch
Vấn đề: Quên tạo branch mới và commit trực tiếp vào main.

Cách giải quyết:

bash
# 1. Tạo branch mới từ commit hiện tại
git branch feature/my-work

# 2. Reset main về commit trước đó
git reset --hard HEAD~1

# 3. Chuyển sang branch mới
git checkout feature/my-work

# 4. Tạo PR từ branch này
Khó khăn 4: Không biết cách tạo và review PR
Vấn đề: Lần đầu sử dụng GitHub, chưa quen với quy trình PR.

Cách giải quyết:

Đọc tài liệu GitHub về Pull Requests
Thực hành tạo PR từ branch sang main
Học cách comment và review code
Sử dụng GitHub Desktop hoặc VS Code để dễ hình dung hơn
Khó khăn 5: Quên pull trước khi push
Vấn đề: Lỗi "rejected" khi push vì remote có commits mới hơn.

Cách giải quyết:

bash
# 1. Pull và rebase
git pull --rebase origin main

# 2. Nếu có conflict, giải quyết rồi:
git rebase --continue

# 3. Push lại
git push origin main
6. Điều mới học được ngoài slide bài giảng
1. Conventional Commits
Học được cách viết commit message theo chuẩn:

feat: - Thêm tính năng mới
fix: - Sửa bug
docs: - Cập nhật tài liệu
style: - Format code
refactor: - Tái cấu trúc code
test: - Thêm test
chore: - Công việc maintenance
Ví dụ:

bash
git commit -m "feat: Add user authentication feature"
git commit -m "fix: Resolve login redirect bug"
git commit -m "docs: Update installation guide"
2. Git Aliases - Tạo shortcut cho lệnh dài
bash
# Tạo alias để gõ lệnh nhanh hơn
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.lg "log --oneline --graph --decorate"

# Sử dụng:
git st  # thay vì git status
git lg  # xem log đẹp hơn
3. Git Stash - Lưu tạm thay đổi
bash
# Khi cần chuyển branch nhưng chưa muốn commit
git stash

# Xem danh sách stash
git stash list

# Lấy lại thay đổi
git stash pop
4. GitHub Actions cơ bản
Hiểu về CI/CD workflow tự động
Tự động check lỗi khi có PR mới
Auto merge khi test pass
5. Branch Protection Rules
Cấu hình bảo vệ branch main:

Yêu cầu PR review trước khi merge
Bắt buộc phải pass CI/CD
Không cho force push vào main
6. Git Rebase vs Merge
Merge: Tạo merge commit, giữ nguyên lịch sử

bash
git merge feature-branch
Rebase: Viết lại lịch sử, làm cho commit history gọn gàng hơn

bash
git rebase main
7. Git Cherry-pick
Lấy một commit cụ thể từ branch khác:

bash
git cherry-pick abc123
8. .gitignore patterns
Học cách ignore file hiệu quả:

gitignore
# Ignore tất cả file .log
*.log

# Ignore thư mục node_modules
node_modules/

# Ignore file config local
config.local.js

# Nhưng vẫn track file này
!important.log
9. GitHub CLI (gh)
Thao tác với GitHub từ terminal:

bash
# Tạo PR từ command line
gh pr create --title "Add new feature" --body "Description"

# Xem danh sách PR
gh pr list

# Merge PR
gh pr merge 123
10. Semantic Versioning
Hiểu về cách đánh version: MAJOR.MINOR.PATCH

MAJOR: Thay đổi breaking changes
MINOR: Thêm feature mới (backward compatible)
PATCH: Bug fixes
7. Kết luận
Qua bài tập thực hành Git tuần 4, nhóm đã:

✅ Nắm vững quy trình làm việc với Git và GitHub
✅ Biết cách tạo và quản lý Pull Requests
✅ Hiểu rõ về branch, merge, và conflict resolution
✅ Làm việc nhóm hiệu quả với version control
✅ Áp dụng được các best practices trong thực tế
Đánh giá chung: Bài tập giúp nhóm hiểu sâu hơn về Git workflow trong môi trường làm việc thực tế, đặc biệt là kỹ năng collaboration và code review.

Ngày hoàn thành: [ ngày 30 tháng 9 năm 2025 ]

Chữ ký nhóm trưởng: __Thông__

