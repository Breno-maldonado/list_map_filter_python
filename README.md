# 🐠 Gerenciamento de Aquário em Python

Este projeto demonstra como manipular dados em **Python** utilizando arquivos **JSON**, aplicando funções como `filter`, `map` e funções personalizadas para gerenciar informações de animais em um aquário.

O sistema realiza:
- Leitura de dados a partir de um arquivo JSON
- Filtragem de animais do tipo **peixe**
- Extração dos nomes desses peixes
- Atualização do número do tanque de animais selecionados

---

## 📁 Estrutura do Projeto

📦 projeto-aquario
┣ 📜 aquario.json
┣ 📜 gerencia_aquario.py
┗ 📜 README.md


---

## 📄 aquario.json

Arquivo responsável por armazenar os dados do aquário.

### Campos utilizados:
- **name**: nome do animal  
- **species**: espécie  
- **tank number**: número do tanque  
- **type**: tipo do animal (fish, shellfish, turtle, etc.)

### Exemplo de estrutura:
```json
{
  "data": [
    {
      "name": "sammy",
      "species": "shark",
      "tank number": 11,
      "type": "fish"
    }

    🐍 gerencia_aquario.py

Script principal responsável por processar e manipular os dados do aquário.

🔹 Leitura do arquivo JSON

O arquivo aquario.json é carregado usando a biblioteca padrão json.

🔹 Filtragem dos peixes

A função abaixo verifica se o animal é do tipo "fish":
def verificar_peixe(animal):
    if animal["type"] == "fish":
        return True
    return False

Ela é usada com filter() para criar uma lista contendo apenas peixes.

🔹 Extração dos nomes dos peixes

Utiliza map() para criar uma lista apenas com os nomes dos peixes:
def animal_name(animal):
    return animal["name"]
Saída no terminal:

['sammy', 'jo', 'charlie']

🔹 Atualização do número do tanque

A função assistencia_do_tank() altera o número do tanque apenas dos animais selecionados:

def assistencia_do_tank(animals, names_selected, new_tank_number):


Exemplo de uso:

new_aquario = assistencia_do_tank(animals, animals_fish_name, 42)

▶️ Como Executar o Projeto

Certifique-se de ter o Python 3 instalado

Coloque os arquivos aquario.json e gerencia_aquario.py na mesma pasta

Execute o comando no terminal:

python gerencia_aquario.py
  ]
}
