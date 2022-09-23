# PemogramanClientServer-Praktek-Latihan2
## Langkah - Langkah Membuat Latihan 2
### Langkah 1 : 
####  Buat proyek web menggunakan link berikut [start.spring.io](https://start.spring.io/) kemudian download dan extrack dari zip menjadi file kemudian import ke dalam apache netbean
### Langkah 2 :
#### Kemudian cari proyek yang bernama Latihan2ServiceApplication dibawah package com.fadhel.latihan.service kemudian pada proyek itu masukkan code berikut :
```java
package com.fadhel.latihan2service;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

@SpringBootApplication
@RestController
public class Latihan2ServiceApplication {

	public static void main(String[] args) {
		SpringApplication.run(Latihan2ServiceApplication.class, args);
	}
@GetMapping("/hello")
public String hello(@RequestParam(value = "name", defaultValue = "Latihan 2") String name) {
return String.format("Hello %s!", name);
}
}
```
##### Kemudian cari proyek aplication.properties yang berada di Other Source >> src/main/resources >> <default package> >> aplication.properties kemudian masukkan code berikut :
```java
server.port=8011
```
##### setelah itu coba di buka link berikut [http://localhost:8011/hello](http://localhost:8011/hello)
