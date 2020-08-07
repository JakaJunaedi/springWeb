# springWeb
Membuat Spring menggunakan Depedencies SpringWeb

Penggunaan Depedencies SpringWeb
1. https://start.spring.io/ add dependencies spring web
2. add code dan buat file DemoApplication.java dengan class DemoApplication

              package com.example.demo;
              import org.springframework.boot.SpringApplication;
              import org.springframework.boot.autoconfigure.SpringBootApplication;
              import org.springframework.web.bind.annotation.GetMapping;
              import org.springframework.web.bind.annotation.RequestParam;
              import org.springframework.web.bind.annotation.RestController;
              
              @SpringBootApplication
              @RestController
              public class DemoApplication {
                
                  
                  public static void main(String[] args) {
                  SpringApplication.run(DemoApplication.class, args);
                  }
                  
                  @GetMapping("/hello")
                  public String hello(@RequestParam(value = "name", defaultValue = "World") String name) {
                  return String.format("Hello %s!", name);
                  }
                
              }
 
 3. Lalu jalankan spring dengan mengetik "./mvnw spring-boot:run"
 4. Buka Browser masukan url localhost:8080
