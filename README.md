Spring Book Management App
Sadə bir Book Management API layihəsi. Java Spring Boot və MySQL istifadə edərək kitabları əlavə etmək, siyahıya baxmaq, yeniləmək və silmək imkanı verir.


Texnologiyalar
Java 24
Spring Boot 3.5.6
Spring Data JPA
MySQL
Lombok
Maven
Quraşdırma və İstifadə


MySQL database yarat:
CREATE DATABASE bookdb;
application.properties faylını konfiqurasiya et:
spring.application.name=bookapi
spring.datasource.url=jdbc:mysql://localhost:3306/bookdb?useSSL=false&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=YeniSabitParol123!
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
Layihəni run et:
mvn spring-boot:run
API default olaraq:
http://localhost:8080/api/books


API Endpoints
Method	Endpoint	Təsviri
GET	/api/books	Bütün kitabları göstərir
GET	/api/books/{id}	ID-yə görə kitabı gətirir
POST	/api/books	Yeni kitab əlavə edir
PUT	/api/books/{id}	Mövcud kitabı yeniləyir
DELETE	/api/books/{id}	Kitabı silir


POST və PUT Body Nümunəsi:
{
  "title": "Java Programming",
  "author": "Asif Rehimov",
  "price": 29.99,
  "publishDate": "2025-09-26"
}


Qeydlər
Hibernate ddl-auto=update sayəsində cədvəllər avtomatik yaranır.
LocalDate sahəsi publishDate üçün istifadə olunur.
Lombok kitabxanası @Data, @Builder, @NoArgsConstructor, @AllArgsConstructor annotation-ları ilə kodu sadələşdirir.


Müəllif
Asif Rehimov
