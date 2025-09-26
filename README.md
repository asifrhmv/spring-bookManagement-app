# Spring Boot Book Management App

Bu layihə **Spring Boot** istifadə edilərək yazılmış sadə Book Management API-dir.  

## Features
- CRUD əməliyyatları (`GET`, `POST`, `PUT`, `DELETE`)  
- Book modeli: `id`, `title`, `author`, `price`, `publishDate`  
- `@RestController`, `@Service`, `@Repository` qatları ilə təmiz arxitektura  
- Lombok ilə model yazma  
- Hibernate və JPA ilə MySQL inteqrasiyası  

## Tech Stack
- Java 17  
- Spring Boot 3.x  
- Lombok  
- MySQL  
- Maven  

## Usage
1. MySQL-də `bookdb` adlı database yaradın  
2. `application.properties` faylında DB konfiqurasiyanı özünüzə uyğun dəyişin  
3. Layihəni IntelliJ-də açın və `BookApiApplication`-ı run edin  
4. Postman ilə aşağıdakı endpoint-ləri test edin:  
   - `GET /api/books` → Bütün kitablar  
   - `GET /api/books/{id}` → ID-yə görə kitab  
   - `POST /api/books` → Yeni kitab əlavə et  
   - `PUT /api/books/{id}` → Kitabı yenilə  
   - `DELETE /api/books/{id}` → Kitabı sil  
