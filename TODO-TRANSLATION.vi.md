# TODO Dịch Toàn Bộ Tài Liệu sang Tiếng Việt (BMAD-METHOD)

Quy ước dịch và lưu file:
- Tài liệu trong `docs/*`: tạo bản dịch tại `docs/vi/*` (giữ nguyên tên file, thêm thư mục `vi`).
- Tài liệu ở thư mục root hoặc trong `src/modules/*` và `tools/*`: tạo file `.vi.md` cạnh file gốc (ví dụ: `README.vi.md`).
- Sau mỗi bản dịch, cập nhật liên kết trong `README.vi.md` để trỏ tới bản tiếng Việt.

Tình trạng: cập nhật tự động thông qua Copilot TODOs.

## Danh sách công việc

1. [ ] Tạo cấu trúc thư mục `docs/vi` và các subfolder cần thiết (`docs/vi/ide-info`, `docs/vi/installers-bundlers`)
2. [ ] Dịch `docs/v4-to-v6-upgrade.md` → `docs/vi/v4-to-v6-upgrade.md`
3. [ ] Dịch `docs/agent-customization-guide.md` → `docs/vi/agent-customization-guide.md`
4. [ ] Dịch `docs/USING_WEB_BUNDLES.md` → `docs/vi/USING_WEB_BUNDLES.md`
5. [ ] Dịch `docs/document-sharding-guide.md` → `docs/vi/document-sharding-guide.md`
6. [ ] Dịch `docs/BUNDLE_DISTRIBUTION_SETUP.md` → `docs/vi/BUNDLE_DISTRIBUTION_SETUP.md`
7. [ ] Dịch `docs/web-bundles-gemini-gpt-guide.md` → `docs/vi/web-bundles-gemini-gpt-guide.md`
8. [ ] Dịch `docs/index.md` → `docs/vi/index.md`
9. [ ] Dịch `docs/ide-info/github-copilot.md` → `docs/vi/ide-info/github-copilot.md`
10. [ ] Dịch `docs/installers-bundlers/ide-injections.md` → `docs/vi/installers-bundlers/ide-injections.md`
11. [ ] Dịch `docs/installers-bundlers/installers-modules-platforms-reference.md` → `docs/vi/installers-bundlers/installers-modules-platforms-reference.md`
12. [ ] Dịch `docs/installers-bundlers/web-bundler-usage.md` → `docs/vi/installers-bundlers/web-bundler-usage.md`
13. [ ] Dịch `src/modules/bmm/docs/README.md` → `src/modules/bmm/docs/README.vi.md`
14. [ ] Dịch `src/modules/bmb/README.md` → `src/modules/bmb/README.vi.md`
15. [ ] Dịch `src/modules/cis/readme.md` → `src/modules/cis/readme.vi.md`
16. [ ] Dịch `tools/cli/README.md` → `tools/cli/README.vi.md`
17. [ ] Dịch `CONTRIBUTING.md` → `CONTRIBUTING.vi.md`
18. [ ] Dịch `CHANGELOG.md` → `CHANGELOG.vi.md`
19. [ ] Dịch `v6-open-items.md` → `v6-open-items.vi.md`
20. [ ] Cập nhật liên kết trong `README.vi.md` để trỏ tới bản dịch mới
21. [ ] Kiểm tra các liên kết trong `docs/vi/**` và `*.vi.md` hoạt động đúng

## Ghi chú
- Giữ nguyên code block, đường dẫn, và cú pháp CLI. Dịch văn bản mô tả, tiêu đề, chú thích.
- Khi có hình ảnh hoặc biểu đồ, giữ nguyên đường dẫn; dịch alt text nếu có.
- Ưu tiên thuật ngữ thống nhất (ví dụ: "bundler", "installer", "workflow", "agent").
