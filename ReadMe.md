# Git Komutları Rehberi

## Anlık Görüntü (Snapshot) Oluşturma

### Repository Başlatma
```bash
git init
# EN: Initializes a new Git repository
# TR: Yeni bir Git deposu (repository) başlatır
```

### Dosyaları Staging Area'ya Alma
```bash
git add file1.js 
# EN: Stages a single file
# TR: Tek bir dosyayı staging area'ya alır

git add file1.js file2.js 
# EN: Stages multiple files
# TR: Birden fazla dosyayı staging area'ya alır

git add *.js 
# EN: Stages with a pattern
# TR: Belirli bir pattern'e uyan dosyaları staging area'ya alır

git add . 
# EN: Stages the current directory and all its content
# TR: Mevcut dizin ve içindeki tüm dosyaları staging area'ya alır
```

### Durum Kontrolü
```bash
git status 
# EN: Shows full status
# TR: Tam durumu gösterir

git status -s 
# EN: Shows short status
# TR: Kısa durum özeti gösterir
```

### Commit İşlemleri
```bash
git commit -m "Message" 
# EN: Commits with a one-line message
# TR: Tek satırlık mesaj ile commit oluşturur

git commit 
# EN: Opens the default editor for commit message
# TR: Varsayılan editörü açarak commit mesajı yazmayı sağlar

git commit -am "Message"
# EN: Stages tracked files and commits in one step
# TR: İzlenen dosyaları staging'e alır ve commit eder
```

### Dosya İşlemleri
```bash
git rm file1.js 
# EN: Removes file from working directory and staging area
# TR: Dosyayı çalışma dizini ve staging area'dan siler

git rm --cached file1.js 
# EN: Removes file from staging area only
# TR: Dosyayı sadece staging area'dan siler

git mv file1.js file1.txt
# EN: Renames or moves a file
# TR: Dosyayı yeniden adlandırır veya taşır
```

### Değişiklikleri Görüntüleme
```bash
git diff 
# EN: Shows unstaged changes
# TR: Staging area'ya alınmamış değişiklikleri gösterir

git diff --staged 
# EN: Shows staged changes
# TR: Staging area'daki değişiklikleri gösterir
```

### Geçmiş İşlemler
```bash
git log 
# EN: Shows commit history
# TR: Commit geçmişini gösterir

git log --oneline 
# EN: Shows commit history in one line format
# TR: Commit geçmişini tek satır formatında gösterir

git log --reverse 
# EN: Shows commits from oldest to newest
# TR: Commitleri eskiden yeniye doğru sıralar
```

### Commit İnceleme
```bash
git show 921a2ff 
# EN: Shows details of specified commit
# TR: Belirtilen commit'in detaylarını gösterir

git show HEAD 
# EN: Shows details of last commit
# TR: Son commit'in detaylarını gösterir

git show HEAD~2 
# EN: Shows details of commit two steps before HEAD
# TR: HEAD'den iki commit öncesini gösterir
```

### Değişiklikleri Geri Alma
```bash
git restore --staged file.js 
# EN: Unstages file
# TR: Dosyayı staging area'dan çıkarır

git restore file.js 
# EN: Discards changes in working directory
# TR: Çalışma dizinindeki değişiklikleri geri alır

git clean -fd 
# EN: Removes untracked files
# TR: İzlenmeyen dosyaları siler
```

## Geçmiş İnceleme (History)

### Detaylı Geçmiş Görüntüleme
```bash
git log --stat 
# EN: Shows modified files statistics
# TR: Değiştirilen dosyaların istatistiklerini gösterir

git log --patch 
# EN: Shows actual changes in detail
# TR: Yapılan değişiklikleri detaylı gösterir
```

### Geçmiş Filtreleme
```bash
git log -3 
# EN: Shows last 3 commits
# TR: Son 3 commit'i gösterir

git log --author="Name"
# EN: Shows commits by author
# TR: Belirli bir yazara ait commit'leri gösterir

git log --before="2020-08-17"
# EN: Shows commits before date
# TR: Belirli bir tarihten önceki commit'leri gösterir
```

### Etiketleme (Tags)
```bash
git tag v1.0 
# EN: Creates a tag for the last commit
# TR: Son commit için etiket oluşturur

git tag 
# EN: Lists all tags
# TR: Tüm etiketleri listeler

git tag -d v1.0 
# EN: Deletes specified tag
# TR: Belirtilen etiketi siler
```

### Hata Ayıklama
```bash
git bisect start
# EN: Starts bisect session
# TR: Bisect oturumunu başlatır

git bisect bad 
# EN: Marks current commit as bad
# TR: Mevcut commit'i hatalı olarak işaretler

git bisect good ca49180 
# EN: Marks specified commit as good
# TR: Belirtilen commit'i iyi olarak işaretler

git bisect reset 
# EN: Ends bisect session
# TR: Bisect oturumunu sonlandırır
```

### Katkıda Bulunanları Görüntüleme
```bash
git blame file.txt 
# EN: Shows who changed what in file
# TR: Dosyadaki her satırın kim tarafından değiştirildiğini gösterir

git shortlog 
# EN: Shows commit history grouped by author
# TR: Commit geçmişini yazarlara göre gruplandırarak gösterir
```
