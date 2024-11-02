# 21.01.55.0019_uts-web-service
nama: Siti Choiriyah
nim: 21.01.55.0019
PROJECT KULINER KHAS PURWODADI
Tabel: menu makanan khas Purwodadi
- id (PK)
- name
- category
- price
- portion

# LANGKAH-LANGKAH
1. Persiapan Lingkungan
   1. Buka XAMPP lalu klik start pada Apache dan mySQL
   2. Buat folder baru bernama rest_menus di dalam direktori htdocs XAMPP

3. Membuat Database
   1. Buka php My Admin
   2. Buat database baru bernama culinary
   3. Pilih database culinary, lalu buka tab SQL
   4. Jalankan query SQL berikut untuk membuat tabel dan menambahkan data sampel:
      CREATE TABLE menus (
      id INT AUTO_INCREMENT PRIMARY KEY,
      name VARCHAR(100) NOT NULL UNIQUE,
      category VARCHAR(50) NOT NULL,
      price DECIMAL(10,2) NOT NULL,
      porsi INT NOT NULL CHECK,
      INDEX idx_category (category) 
      );

      INSERT INTO menus(name, category, price, porsi) VALUES
      ('Garang Asem', 'makanan', '15000', '1'),
      ('Es potong', 'minuman', '5000', '1'),
      ('Sale Pisang', 'cemilan', '5000', '200');

5. Membuat file PHP untuk Web Service
   1. Buka vs code
   2. Buat file baru dan simpan sebagai menus_api.php di dalam folder rest_menus.
   3. Salin dan tempel kode berikut dalam menus_api.php:
      
      

7. Pengujian dengan Postman
   1. GET /api/[objek]
   2. GET /api/[objek]/{id}
   3. POST /api/[objek]
   4. PUT /api/[objek]/{id}
   5. DELETE /api/[objek]/{id}
