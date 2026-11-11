
# DIAGRAM CI/CD DEVOPS

## Alur Kolaborasi Developer

Diagram berikut menjelaskan proses CI/CD menggunakan GitHub Actions.

```mermaid
flowchart TD
    A["Developer"] --> B["GitHub Repository"]
    B --> C["Commit dan Push"]
    C --> D["GitHub Actions"]
    D --> E["Continuous Integration (CI)"]
    E --> F["Testing Aplikasi"]
    F --> G{"Testing Berhasil?"}

    G -->|Tidak| H["Perbaikan Kode"]
    H --> C

    G -->|Ya| I["Upload Artifact"]
    I --> J["Continuous Deployment (CD)"]
    J --> K["GitHub Pages"]
    K --> L["Website Berhasil Dipublikasikan"]
    L --> M["Monitoring"]
```

## Penjelasan

1. Developer membuat dan mengubah kode program.
2. Kode dikirim ke GitHub melalui Commit dan Push.
3. GitHub Actions menjalankan proses CI.
4. Sistem melakukan pengujian kode.
5. Jika pengujian berhasil, proses CD dijalankan.
6. Website dipublikasikan menggunakan GitHub Pages.
7. Developer melakukan monitoring terhadap website.
