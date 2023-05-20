# Sistem Peminjaman Buku di Perpustakaan

Program ini adalah sebuah program sederhana untuk sistem peminjaman buku di perpustakaan. Program ini menggunakan konsep Association antara dua kelas utama yaitu `Book` (Buku) dan `LibraryMember` (Anggota Perpustakaan). Setiap objek `LibraryMember` terkait dengan beberapa objek `Book` yang merupakan daftar buku yang dipinjam oleh anggota tersebut.

## Spesifikasi

Kelas `Book` memiliki atribut berikut:
- `title` (string): judul buku.
- `author` (string): penulis buku.
- `is_available` (bool): status ketersediaan buku (True jika tersedia, False jika sedang dipinjam).

Kelas `LibraryMember` memiliki atribut berikut:
- `name` (string): nama anggota perpustakaan.
- `borrowed_books` (list): daftar objek `Book` yang dipinjam oleh anggota.

Selain itu, kelas `LibraryMember` memiliki metode berikut:
- `borrow_book(book)`: untuk meminjam buku dengan menambahkannya ke dalam daftar buku yang dipinjam oleh anggota.
- `return_book(book)`: untuk mengembalikan buku dengan menghapusnya dari daftar buku yang dipinjam oleh anggota.
- `display_borrowed_books()`: untuk menampilkan daftar buku yang dipinjam oleh anggota beserta informasi detailnya, seperti judul, penulis, dan status ketersediaan.

## Penggunaan

Berikut adalah contoh penggunaan program:

```python
# Import kelas Book dan LibraryMember

class Book:
    # ...

class LibraryMember:
    # ...

# Membuat objek LibraryMember
member = LibraryMember("John Doe")

# Membuat beberapa objek Book
book1 = Book("Harry Potter and the Philosopher's Stone", "J.K. Rowling")
book2 = Book("To Kill a Mockingbird", "Harper Lee")
book3 = Book("1984", "George Orwell")

# Meminjam buku
member.borrow_book(book1)
member.borrow_book(book2)
member.borrow_book(book3)

# Menampilkan daftar buku yang dipinjam
member.display_borrowed_books()

# Mengembalikan buku
member.return_book(book2)

# Menampilkan daftar buku yang dipinjam setelah pengembalian
member.display_borrowed_books()
