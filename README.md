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
