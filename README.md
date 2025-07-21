# Projeto Wiremock - QAZANDO 🚗

Este projeto simula uma API de veículos utilizando o **WireMock** para fins de teste e aprendizado.

---

## 🔧 Tecnologias utilizadas

- [WireMock](https://wiremock.org/) (Standalone)
- Java 11 ou superior
- Postman ou ferramenta de requisições
- Git e GitHub

---

## 📦 Estrutura do Projeto

.
├── __files/
│ └── cars.json # Resposta mockada
├── mappings/
│ └── post-cars.json # Mapping com body contendo "model": "fusca"
│ └── post-cars-500.json # Mapping com body contendo "model": "up tsi"
│ └── api-cars.json # Mapping para GET de consulta
├── tests/
│ └── teste-sucesso.js
│ └── teste-consulta.js
│ └── teste-500.js
└── wiremock-standalone-3.9.1.jar

yaml
Copiar
Editar

---

## 🚀 Como rodar o WireMock localmente

1. Certifique-se que o **Java 11+** está instalado:
   ```bash
   java -version
Faça o download do repositório:

bash
Copiar
Editar
git clone https://github.com/leoschmitt98/wiremock-qazando.git
cd wiremock-qazando
Inicie o WireMock apontando para a pasta do projeto:

bash
Copiar
Editar
java -jar wiremock-standalone-3.9.1.jar --port 8080 --root-dir .
O mock estará acessível em: http://localhost:8080

📌 Casos de teste disponíveis
Tipo	Requisição	Body (model)	Resposta esperada
POST	/api/cars	"fusca"	201 Created
POST	/api/cars	"up tsi"	500 Internal
GET	/api/cars	-	200 OK

Use o Postman ou outra ferramenta para testar os endpoints.

✅ Exemplo de body para sucesso:
json
Copiar
Editar
{
  "brand": "Volkswagen",
  "model": "fusca",
  "year": "1972"
}
📄 Licença
Projeto de estudo com base no curso da QAzando.

👨‍💻 Autor
Leonardo Wilenbring Schmitt
