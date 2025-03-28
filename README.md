#  FIAP - Checkpoint 1



## 📁 Estrutura de Pastas

```
src/main/java/br/com/fiap/checkpoint1
├── controller     # Endpoints da API
├── model          # Entidade Pedido
├── repository     # Interface JPA
├── service        # Regras de negócio
```

---

## 🔧 Configuração do Banco (H2)

No arquivo `application.properties`:

```properties
spring.datasource.url=jdbc:h2:mem:pedidosdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.h2.console.enabled=true
spring.jpa.show-sql=true
spring.jpa.hibernate.ddl-auto=update
```

Acesse o console do H2 em:  
📍 `http://localhost:8080/h2-console`  
JDBC URL: `jdbc:h2:mem:pedidosdb`

---

## 📫 Endpoints da API

| Método | Endpoint            | Descrição                    |
|--------|---------------------|------------------------------|
| GET    | /pedidos            | Lista todos os pedidos       |
| GET    | /pedidos/{id}       | Busca pedido por ID          |
| POST   | /pedidos            | Cria um novo pedido          |
| PUT    | /pedidos/{id}       | Atualiza um pedido existente |
| DELETE | /pedidos/{id}       | Remove um pedido             |

---

## 🧪 Exemplos de Requisições (JSON)

### Retornar Pedidos (GET /pedidos)
![alt text](image-1.png)

### Retornar Pedidos Especificados com ID (GET /pedidos/{id})
![alt text](image-2.png)

### Criar Pedido (POST /pedidos)
```json
{
  "clienteNome": "Pedro Henrique Pontes Farath",
  "valorTotal": 150.0
}
```
![alt text](image.png)

### Atualizar Pedido (PUT /pedidos/1)
```json
{
  "clienteNome": "Alice Freitas",
  "valorTotal": 250.00
}
```
![alt text](image-3.png)

---

### Deletar Pedidos (DELETE /pedidos/1)
![alt text](image-4.png)

## 🧑‍💻 Como rodar o projeto

### Via terminal:
```bash
mvn spring-boot:run
```

### Ou rode diretamente na sua IDE (IntelliJ / Eclipse / VSCode).

---
