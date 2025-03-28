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


### Retornar Pedidos Especificados com ID (GET /pedidos/{id})
![image](https://github.com/user-attachments/assets/dcbc2a99-08ee-4c6e-adb1-0f59929eeabb)


### Criar Pedido (POST /pedidos)
{
  "clienteNome": "Lucca Vilaça Okubo",
  "valorTotal": 150.0
}
```


### Atualizar Pedido (PUT /pedidos/1)
```json
{
  "clienteNome": "Alice Freitas",
  "valorTotal": 250.00
}

### Deletar Pedidos (DELETE /pedidos/1)


## 🧑‍💻 Como rodar o projeto

### Via terminal:
```bash
mvn spring-boot:run
```
### Ou rode diretamente na sua IDE 

---
