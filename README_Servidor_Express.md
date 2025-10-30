# 🧠 Servidor Básico com Express.js

## 📋 Descrição do Projeto
Este projeto tem como objetivo criar um **servidor básico** utilizando o **framework Express.js** no Node.js.  
O servidor responde a requisições do tipo **GET** na rota raiz (`/`) e exibe uma mensagem simples no navegador.

---

## 🚀 Passo a Passo para Configuração

### **1️⃣ Criar o Projeto**
Crie uma pasta para o projeto e entre nela pelo terminal:
```bash
mkdir servidor-express
cd servidor-express
```

Crie um arquivo principal chamado `app.js`:
```bash
touch app.js
```

---

### **2️⃣ Inicializar o NPM**
No terminal, execute o comando:
```bash
npm init -y
```

Esse comando cria o arquivo **`package.json`** que serve para:
- Identificar o projeto (nome, versão, autor, etc.);
- Registrar dependências (como o Express);
- Definir scripts de execução;
- Padronizar a instalação do projeto em outros computadores.

---

### **3️⃣ Instalar o Express**
Execute o comando:
```bash
npm install express
```
Isso instalará o framework Express e o adicionará às dependências do projeto no `package.json`.

---

### **4️⃣ Código do Servidor (`app.js`)**
Cole o seguinte código no arquivo `app.js`:

```js
const express = require('express'); // Importa o módulo Express
const app = express(); // Inicializa o aplicativo Express
const PORT = 3000; // Define a porta do servidor

// Rota principal do servidor
app.get('/', (req, res) => {
    res.send('Servidor Express funcionando! observe que a rota é definida como o endpoint raiz.');
});

// Inicializa o servidor
app.listen(PORT, () => {
    console.log(`Servidor rodando em http://localhost:${PORT}`);
});
```

---

### **5️⃣ Executar o Servidor**
No terminal, digite:
```bash
node app.js
```

Se tudo estiver correto, você verá a mensagem:
```
Servidor rodando em http://localhost:3000
```

---

### **6️⃣ Testar no Navegador**
Abra o navegador e acesse:
```
http://localhost:3000
```

Aparecerá a mensagem:
```
Servidor Express funcionando! observe que a rota é definida como o endpoint raiz.
```

---

### **7️⃣ Encerrar o Servidor**
Para encerrar o servidor, pressione:
```
Ctrl + C
```

---

### **8️⃣ Enviar o Projeto para o GitHub**
Crie um repositório no GitHub e execute os seguintes comandos no terminal:

```bash
git init
git add .
git commit -m "Servidor básico com Express.js"
git branch -M main
git remote add origin https://github.com/seu-usuario/nome-do-repositorio.git
git push -u origin main
```

> 📝 Substitua o link acima pelo seu repositório do GitHub.

---

## 📦 Estrutura Final do Projeto
```
servidor-express/
│
├── node_modules/
├── package.json
├── package-lock.json
├── app.js
└── README.md
```

---

## 🧾 Exemplo de `package.json`
```json
{
  "name": "servidor-express",
  "version": "1.0.0",
  "description": "Servidor básico utilizando o framework Express.js",
  "main": "app.js",
  "scripts": {
    "start": "node app.js"
  },
  "author": "Seu Nome",
  "license": "ISC",
  "dependencies": {
    "express": "^4.18.2"
  }
}
```

---

## 🧑‍💻 Autor
**Seu Nome Aqui**  
Disciplina: *Desenvolvimento Web com Node.js*  
Professor: *[Nome do professor]*  
Data: *Outubro / 2025*
