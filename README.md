# Citas médicas – Taller de pruebas con Spring Boot

Java 25 · Spring Boot 4.0.0 · Maven · H2 · JUnit 5 · Mockito · MockMvc · Selenium · JaCoCo

## Ejecutar la aplicación
```
mvn spring-boot:run
```
Abrir http://localhost:8080/citas.html

## Pruebas
- `mvn test` : pruebas unitarias, REST, JPA e integración (excluye las de UI).
- `mvn verify` : lo anterior + reporte JaCoCo en `target/site/jacoco/index.html` (umbral 70 % de líneas).
- Pruebas Selenium (requieren Chrome): `mvn test -Dtest=ReservaUITest -DexcludedGroups=none`
  o ejecutar la clase desde IntelliJ.

## Reglas de negocio
- Un profesional no puede tener dos citas en el mismo horario.
- Máximo 20 citas diarias por profesional.
- POST /api/citas -> 201 (creada), 409 (conflicto de horario o cupo), 400 (entrada inválida).

## Integrantes
(completar)
