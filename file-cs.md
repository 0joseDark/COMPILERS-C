## 📄 O que é um ficheiro `.cs`?

* Um ficheiro com extensão **`.cs`** é um **ficheiro de código-fonte escrito em C#** (C Sharp), uma linguagem de programação criada pela Microsoft.
* O `.cs` significa **"C Sharp Source"**.
* Contém **classes, métodos, variáveis e lógica** que compõem um programa.

---

## 📌 Estrutura básica de um ficheiro `.cs`

```csharp
// Comentário: este programa imprime uma mensagem no ecrã

using System; // Importa a biblioteca System (entrada/saída, etc.)

// Define uma classe chamada Programa
class Programa
{
    // Método principal que o sistema executa primeiro
    static void Main()
    {
        Console.WriteLine("Olá, Mundo!");
    }
}
```

---

## 🧱 Explicação linha a linha

| Linha                    | Descrição                                                                      |
| ------------------------ | ------------------------------------------------------------------------------ |
| `using System;`          | Usa a biblioteca `System`, que contém `Console`, entre outras.                 |
| `class Programa`         | Cria uma **classe** chamada `Programa`. Todo código C# está dentro de classes. |
| `static void Main()`     | É o **ponto de entrada** do programa (onde tudo começa).                       |
| `Console.WriteLine(...)` | Imprime texto no ecrã.                                                         |

---

## 🔧 Como usar um ficheiro `.cs` na prática

### 1. Criar o ficheiro:

Abre um editor de texto (como Notepad, Notepad++, ou VS Code) e grava o seguinte conteúdo como `ola.cs`:

```csharp
using System;

class Programa
{
    static void Main()
    {
        Console.WriteLine("Olá Mundo!");
    }
}
```

---

### 2. Compilar com `dotnet`:

```bash
# Passo 1: Cria um projeto
dotnet new console -n MeuPrograma
cd MeuPrograma

# Passo 2: Substitui o ficheiro Program.cs pelo teu ola.cs
# Ou copia/cola o conteúdo

# Passo 3: Corre
dotnet run
```

---

### 3. Compilar com `Mono`:

```bash
# Supondo que tens mono instalado
mcs ola.cs -out:ola.exe
ola.exe
```

---

## 🧠 Dicas

* Um projeto grande pode ter **vários ficheiros `.cs`**, cada um com classes diferentes.
* Usa-se o `namespace` para organizar melhor o código (como pacotes).

---

## 🎯 Resumo

| Termo                 | Significado                                    |
| --------------------- | ---------------------------------------------- |
| `.cs`                 | Ficheiro de código-fonte C#                    |
| `class`               | Estrutura base que define objetos e funções    |
| `Main()`              | Função principal, ponto de entrada do programa |
| `Console.WriteLine()` | Escreve texto no terminal                      |

---
