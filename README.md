# Bài 3 — CI/CD với GitHub Actions

## Ý tưởng

- Dự án Maven giống Bài 1 (MathUtils + Logback + Hibernate + JUnit 5).
- Workflow `.github/workflows/ci.yml`: trigger **`push`** và **`pull_request`**, chạy `mvn clean verify` (gồm `test` và `package`).
- **`upload-artifact`**: lưu `target/*.jar` sau build để kiểm chứng artifact trên GitHub.

## Thử nghiệm lỗi build & debug (yêu cầu đề)

1. Cố tình sửa test sai (`assertEquals(999, MathUtils.max(1,2))`) rồi push — workflow đỏ.
2. Mở tab **Actions** → chọn run → xem log bước **Build with Maven** (Surefire báo test failure).
3. Sửa lại test, push — pipeline xanh.

*(Thực hiện trên repository GitHub của bạn; trong mã nguồn nộp là bản đã pass.)*

## Chạy local

```bash
chmod +x run.sh
./run.sh
```

I wanna test
hihihi