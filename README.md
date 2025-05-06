# Phần 1: Github cơ bản


## Github Sơ cấp

### 📌Kiểm tra cài đặt

```bash
git --version
```


### 🔹Cấu hình Git

Thiết lập tên và email (dùng để xác định tác giả commit):

```bash
git config --global user.name "Tên Của Bạn"
git config --global user.email "email@example.com"
git config --global init.defaultBranch main  # Đặt nhánh mặc định là main
```

Kiểm tra cấu hình:

```bash
git config --list
```



Clone về máy

```jsx
git clone https://github.com/username/repository.git
```

Tạo local trước rồi push lên GitHub

```bash
# mkdir my-project
# cd my-project
git init
git remote add origin <https://github.com/username/repository.git>
```

Các lệnh cơ bản

```bash
git status                      # Xem trạng thái các file
git add .                       # Thêm tất cả thay đổi vào staging area
git add <filename>              # Thêm file cụ thể
git commit -m "Message"         # Tạo commit với thông điệp
git push origin <branch-name>   # Đẩy code lên GitHub
git pull <origin branch-name>   # Lấy code mới nhất từ remote
git log
```

## Github Trung cấp

**1. Làm việc với branches (nhánh)**

```bash
git branch                  # Liệt kê các nhánh
git branch new-branch       # Tạo nhánh mới
git checkout branch-name    # Chuyển sang nhánh
git checkout -b new-branch  # Tạo và chuyển sang nhánh mới
git merge branch-name       # Gộp nhánh vào nhánh hiện tại
git branch -d branch-name   # Xóa nhánh local
```
Sau khi merge xong chưa hiển thị liền trên github, chúng ta cần push lên với tư cách branch hiện tại.
---
# Phần 2: Ngôn ngữ Markdown

Ngôn ngữ này khá đơn giản, bạn có thể đọc tại [đây](http://daringfireball.net/projects/markdown/syntax) để biết cách sử dụng.

Nhưng với tôi, tôi không dùng hết từng ấy thứ cho nên tôi chỉ nhớ một số cái tôi hay dùng, cách tôi dùng như sau:

Tạo một file có tên bất kỳ với đuôi .md. Có thể dùng `notepad`, `notepad++`, `vi`, `nano`,... hay bất cứ thứ gì mà bạn muốn.

Một số phương pháp tôi hay sử dụng để viết:

<a name="thetieude"></a>
### 1. Thẻ tiêu đề

Markdown sử dụng kí tự # để bắt đầu cho các thẻ tiêu đề, có thể dùng từ 1 đến 6 ký tự # liên tiếp. Mức độ riêu đề giảm dần từ 1 đến 6

Tùy mục đích và ý thích bạn có thể sử dụng cách này để thể hiện các chỉ mục khác nhau.

Ví dụ:

```
# 1.Tiêu đề cấp 1
```

# 1.Tiêu đề cấp 1

```
## 2.Tiêu đề cấp 2
```

## 2.Tiêu đề cấp 2

```
###### 6.Tiêu đề cấp 6
```

###### 6.Tiêu đề cấp 6

<a name="chenlinkchenanh"></a>
### 2. Chèn link, chèn ảnh

Để chèn hyperlink bạn chỉ cần paste luôn linh đó vào file .md

```
https://github.com
```

https://github.com

Hoặc bạn cũng có thể sử dụng cú pháp sau để thu ngắn đường dẫn của link

```
[Github](https://github.com)
```

Kết quả là:

[Github](https://github.com)

Để chèn ảnh thì bạn hãy sử dụng cú pháp sau:

```
<img src="link_anh_cua_ban">
```

Tôi thường sử dụng công cụ [Lightshot](https://app.prntscr.com/en/index.html) để chụp ảnh màn hình và up hình đó lên trang http://i.imgur.com/ để lấy đường dẫn ảnh đưa vào Github

Hai công cụ này khá dễ sử dụng, bạn chỉ cần chụp màn hình bằng Lightshot ấn Ctrl + C để copy và Ctrl + V để paste vào trình duyệt tại trang web http://i.imgur.com/

<a name=kytuindaminnghieng></a>
### 3. Ký tự in đậm, in nghiêng

- Để in đậm một đoạn text  bạn chỉ cần làm như sau:

```
**từ cần in đậm**
```

**từ cần in đậm**

- Để in nghiên một đoạn text  bạn chỉ cần làm như sau:

```
*từ cần in nghiêng*
```

*từ cần in nghiêng*

<a name="trichdanbochu"></a>
### 4. Trích dẫn, bo chữ

Để bo một đoạn text thì bạn chỉ cần sử dụng cú pháp sau:

```
`đoạn cần bo`
```

Kết quả là: `đoạn cần bo`

Để làm nổi bật một đoạn, chẳng hạn như một đoạn shell hay file cấu hình bạn có thể sử dụng cú pháp như ví dụ sau:

    ```sh
    auto eth0
    iface eth0 inet static
    ipaddress 10.10.10.10
	netmask 255.255.255.0
	gateway 10.10.10.1
	dns-nameservers 8.8.8.8
    ```

Kết quả như sau:

```sh
auto eth0
iface eth0 inet static
ipaddress 10.10.10.10
netmask 255.255.255.0
gateway 10.10.10.1
dns-nameservers 8.8.8.8
```

<a name="gachdaudong"></a>
### 5. Gạch đầu dòng

Để sử dụng gạch đầu dòng bạn chỉ cần sử dụng cú pháp sau:

```
- Gạch đầu dòng thứ nhất
  
  - Thụt với đầu dòng 1
  
  - Thụt với đầu dòng 1
 
- Gạch đầu dòng thứ hai
  
  - Thụt với đầu dòng 2
  
  - Thụt với đầu dòng 2
  
```

- Gạch đầu dòng thứ nhất
  
  - Thụt với đầu dòng 1
  
  - Thụt với đầu dòng 1
  
- Gạch đầu dòng thứ hai
  
  - Thụt với đầu dòng 2
  
  - Thụt với đầu dòng 2
  

<a name="taobang"></a>
### 6. Tạo bảng

Bạn có thể sử dụng cú pháp sau để tạo bảng:

```
| Cột 1 Hàng 1 | Cột 2 | Cột 3| Cột 4 |
|--------------|-------|------|-------|
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 | 2 x 4 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 | 3 x 4 |
| Hàng 4 | 4 x 1 | 4 x 2 | 4 x 3 | 4 x 4 |
```

Kết quả:

| Cột 1 Hàng 1 | Cột 2 | Cột 3| Cột 4 |
|--------------|-------|------|-------|
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 | 2 x 4 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 | 3 x 4 |
| Hàng 4 | 4 x 1 | 4 x 2 | 4 x 3 | 4 x 4 |

<a name="meo"></a>
###*Mẹo:*

- Sử dụng trang http://markdownlivepreview.com/ paste vào đó đoạn markdown bạn viết và xem trước để chỉnh sửa cho phù hợp.

- Bạn cũng có thể sử dụng những đoạn markdown của người khác đã viết trước để tham khảo.

Như vậy bạn đã có thể trình bày github của mình một cách sáng sủa bằng markdown.

<a name="cacthaotacvoigitvagithub"></a>
