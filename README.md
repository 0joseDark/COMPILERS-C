## 🔧 COMPILADORES C/C++ PARA WINDOWS 10

### 1. **MinGW (Minimalist GNU for Windows)**

#### ✅ Suporta: C e C++ (gcc, g++)

#### 📌 Baseado no compilador GNU usado no Linux.

#### 📥 Instalação:

* Site: [https://osdn.net/projects/mingw/releases/](https://osdn.net/projects/mingw/releases/)
* Ou use o `MSYS2`, que inclui o MinGW moderno.

#### 📦 Instalar com MSYS2 (recomendado):

```bash
pacman -S mingw-w64-x86_64-gcc
```

#### ⚙️ Compilar:

```bash
# Compilar C:
gcc programa.c -o programa.exe

# Compilar C++:
g++ programa.cpp -o programa.exe
```

#### 📋 Observações:

* Leve e muito usado para aplicações simples e multiplataforma.
* Pode ser usado com editores como Notepad++, VS Code, etc.

---

### 2. **TDM-GCC**

#### ✅ Suporta: C e C++ (gcc, g++)

#### 📌 Uma versão do MinGW com configurações próprias e mais fácil de instalar.

#### 📥 Instalação:

* Site: [https://jmeubank.github.io/tdm-gcc/](https://jmeubank.github.io/tdm-gcc/)

#### ⚙️ Compilar:

```bash
gcc programa.c -o programa.exe
g++ programa.cpp -o programa.exe
```

#### 📋 Observações:

* Pronto a usar depois da instalação.
* Já vem com ambiente de compilação completo.

---

### 3. **Clang (LLVM)**

#### ✅ Suporta: C e C++

#### 📌 Compilador moderno, rápido, com mensagens de erro mais claras.

#### 📥 Instalação:

* A forma mais simples é usar o **MSYS2** ou instalar o **LLVM** via pacote oficial.
* Site: [https://releases.llvm.org/](https://releases.llvm.org/)

#### ⚙️ Compilar:

```bash
clang programa.c -o programa.exe
clang++ programa.cpp -o programa.exe
```

#### 📋 Observações:

* Muito usado em sistemas modernos e para análise de código.
* Compatível com GCC e bibliotecas C/C++ padrão.

---

### 4. **Cygwin**

#### ✅ Suporta: C e C++

#### 📌 Ambiente POSIX (Linux-like) em Windows. Inclui ferramentas GNU.

#### 📥 Instalação:

* Site: [https://www.cygwin.com/](https://www.cygwin.com/)
* Escolher durante a instalação os pacotes `gcc-core` e `gcc-g++`.

#### ⚙️ Compilar:

```bash
gcc programa.c -o programa.exe
g++ programa.cpp -o programa.exe
```

#### 📋 Observações:

* Programas compilados podem depender da `cygwin1.dll`.
* Ideal para portar programas do Linux para Windows.

---

### 5. **Intel C++ Compiler (ICC ou ICX)**

#### ✅ Suporta: C e C++

#### 📌 Otimizado para desempenho em processadores Intel.

#### 📥 Instalação:

* Parte do **Intel oneAPI Toolkit**.
* Site: [https://www.intel.com/content/www/us/en/developer/tools/oneapi/toolkits.html](https://www.intel.com/content/www/us/en/developer/tools/oneapi/toolkits.html)

#### ⚙️ Compilar:

```bash
icx programa.c -o programa.exe
icx programa.cpp -o programa.exe
```

#### 📋 Observações:

* Excelente para computação científica e aplicações de alto desempenho.
* Requer registo e instalação mais complexa.

---

## 🧰 COMO CONFIGURAR O CAMINHO (PATH) DO COMPILADOR

Depois de instalar qualquer compilador, adiciona-o ao **PATH do sistema**:

### Exemplo (MinGW):

1. Vai a **Painel de Controlo > Sistema > Definições Avançadas > Variáveis de Ambiente**.
2. Em **Path**, adiciona:

   ```
   C:\MinGW\bin
   ```

---

## ✅ RESUMO COMPARATIVO

| Compilador  | Linguagens | Vantagem Principal          | Tipo de Ficheiro Final |
| ----------- | ---------- | --------------------------- | ---------------------- |
| MinGW       | C/C++      | Leve e compatível com Linux | `.exe` (nativo)        |
| TDM-GCC     | C/C++      | Fácil instalação e uso      | `.exe` (nativo)        |
| Clang/LLVM  | C/C++      | Erros mais claros e análise | `.exe` (nativo)        |
| Cygwin      | C/C++      | Ambiente Linux em Windows   | `.exe` + `cygwin1.dll` |
| Intel (ICX) | C/C++      | Otimização para CPUs Intel  | `.exe` (otimizado)     |


---

## 🛠️ COMPILADORES C# PARA WINDOWS 10

---

### 1. **.NET SDK / .NET CLI (Microsoft Oficial)**

#### ✅ Suporta: C\#

#### 📌 Ferramenta oficial da Microsoft, moderna, leve e usada em produção.

---

#### 📥 Instalação:

* Vai a: [https://dotnet.microsoft.com/download](https://dotnet.microsoft.com/download)
* Escolhe a versão mais recente do **.NET SDK (não só o runtime)**.
* Verifica no terminal:

```bash
dotnet --version
```

---

#### ⚙️ Compilar (modo simples):

```bash
# Cria um novo projeto (opcional):
dotnet new console -n MeuApp
cd MeuApp

# Compila:
dotnet build

# Corre:
dotnet run
```

#### ⚙️ Compilar diretamente um ficheiro .cs (sem projeto):

```bash
dotnet new console -n Compilador
cd Compilador
# Copia o ficheiro .cs para esta pasta
dotnet run
```

---

#### 📋 Observações:

* Leve, multiplataforma (Windows, Linux, Mac).
* Não precisa de Visual Studio.
* Usa o novo compilador **Roslyn**.

---

### 2. **Mono (Antigo e ainda útil)**

#### ✅ Suporta: C\#

#### 📌 Compilador C# multiplataforma antes do .NET Core.

---

#### 📥 Instalação:

* Site: [https://www.mono-project.com/download/stable/](https://www.mono-project.com/download/stable/)
* Depois de instalar, abre o terminal (CMD ou PowerShell).

#### ⚙️ Compilar:

```bash
mcs programa.cs -out:programa.exe
```

#### ⚙️ Executar:

```bash
mono programa.exe
```

---

#### 📋 Observações:

* Ainda usado em jogos com Unity ou em projetos antigos.
* Pode correr binários do .NET Framework.

---

### 3. **CS-Script**

#### ✅ Suporta: C\#

#### 📌 Ferramenta leve para correr scripts C# como se fossem Python.

---

#### 📥 Instalação:

* Site: [https://github.com/oleg-shilo/cs-script.core](https://github.com/oleg-shilo/cs-script.core)
* Ou instala com o .NET:

```bash
dotnet tool install -g dotnet-script
```

#### ⚙️ Executar um script C#:

```bash
dotnet script programa.csx
```

---

#### 📋 Observações:

* Útil para scripts rápidos em C#.
* Pode usar bibliotecas .NET no script.

---

### 4. **Compilação via Roslyn (C# Compiler Platform)**

#### ✅ Suporta: C\#

#### 📌 Roslyn é o compilador usado pelo próprio .NET CLI.

#### ⚙️ Também pode ser usado como biblioteca para criar compiladores, IDEs, etc.

---

## ✅ RESUMO COMPARATIVO

| Compilador/Ferramenta | Requisitos    | Tipo de Projeto       | Execução        | Observações            |
| --------------------- | ------------- | --------------------- | --------------- | ---------------------- |
| .NET CLI (`dotnet`)   | Instalar SDK  | App, biblioteca, etc. | `dotnet run`    | Moderno e oficial      |
| Mono (`mcs`)          | Instalar Mono | Simples e leve        | `mono prog.exe` | Antigo, mas compatível |
| dotnet-script         | .NET SDK      | Scripts `.csx`        | `dotnet script` | Executa C# como Python |

---

## 🧪 Exemplo: Programa "Olá Mundo" em C\#

### 🔹 `ola.cs`

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

### 🔹 Compilar com `.NET CLI`:

```bash
dotnet new console -n OlaMundo
cd OlaMundo
# Substitui o ficheiro `Program.cs` pelo `ola.cs`
dotnet run
```

### 🔹 Compilar com `Mono`:

```bash
mcs ola.cs -out:ola.exe
ola.exe
```

---

