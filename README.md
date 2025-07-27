# calculadora-1.0

[ Visite Linkedin ](https://www.linkedin.com/in/eliasdosreislima/)

Projeto criação de uma calculadora em Html CSS e JavaScript

### 📋 Tarefas Pendentes
- [x] Criaçao index.html
- [x] Criando conteudo HTML para calculadora
- [x] Criaçao style.css
- [x] Criando estilização css para calculadora
- [x] Criação script.js
- [x] Criando logica da calculadora javascript
### Calculadora 1.0
<img width="643" height="692" alt="image" src="https://github.com/user-attachments/assets/a5b4b7d1-4cda-4ca5-a4d0-1857e5669b41" />

## HTML
```HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Calculadora | EL</title>
</head>
<body>
    <h1>Elias Dos R. Lima</h1>
    <div class="calculator">
        <input type="text" disabled id="display" >
        <div class="box-button">
            <button onclick="clean()" >C</button>
            <button  onclick="back()" >&lt;</button>
            <button onclick="insertToDisplay('/')">/</button>
            <button onclick="insertToDisplay('*')">*</button>
            <button onclick="insertToDisplay('7')">7</button>
            <button onclick="insertToDisplay('8')">8</button>
            <button onclick="insertToDisplay('9')">9</button>
            <button onclick="insertToDisplay('-')">-</button>
            <button onclick="insertToDisplay('4')">4</button>
            <button onclick="insertToDisplay('5')">5</button>
            <button onclick="insertToDisplay('6')">6</button>
            <button onclick="insertToDisplay('+')">+</button>
            <button onclick="insertToDisplay('1')">1</button>
            <button onclick="insertToDisplay('2')">2</button>
            <button onclick="insertToDisplay('3')">3</button>
            <button onclick="insertToDisplay('0')" class="btn-zero">0</button>
            <button onclick="insertToDisplay('.')" >.</button>
            <button onclick="result()" class="btn-result">=</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>

```
## CSS
```CSS

body{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    padding: 0;
    font-family: Arial, Helvetica, sans-serif;
    background-color: #1c1b1b;
    
}

h1{
    color: #fff;   
}

.calculator{
    background-color: #fff;
    width: 300px;
    border-radius: 15px;
    padding: 20px;
}

#display{
    width: 100%;
    box-sizing: border-box;
    height: 60px;
    border: none;
    border-radius: 6px;
    background-color: #f0f0f0;
    text-align: right;
    font-weight: 900;
    font-size: 2em;
    margin-bottom: 16px;
}   
.box-button{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
    gap: 10px;
}

button{
    border: none;
    height: 60px;
    border-radius: 6px;
    font-size: 2em;
    font-weight: 900;
    transition: .4s;
}
button:hover{
    background-color: #e1e1e1;
    cursor: pointer;
    transition: .4s; 
}

.btn-zero{
    grid-column: 1 / 3;
}
.btn-result{
    grid-row: 4 / 6 ;
    height: 100%;
    grid-column: 4;
}

```
## Javascript
```Javascript

function insertToDisplay(data){
    document.querySelector('#display').value += data
}

function clean(){
    document.querySelector('#display').value = ""
}

function back(){
    const display = document.querySelector('#display')
    display.value = display.value.slice(0, -1)
}

function result(){
    const display = document.querySelector('#display')
    try{
        display.value = eval(display.value).toFixed(2)
    }catch(erro){
        display.value = 'Error'
    }
}
```

| Status     | Descrição                       | Projeto   |
|------------|----------------------------------|----------|
| ✅ Sucesso | Tudo ocorreu como esperado      | ✅       |

