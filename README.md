# sobel-edge-feature-extraction
Extração de bordas e construção de vetores de características utilizando o Filtro Sobel.

Este repositório contém a implementação da **Atividade 1 da disciplina Tópicos para Computação 1 (2026.1)**, ministrada pela **Profa. Dra. Elloá B. Guedes** na **Escola Superior de Tecnologia (EST/UEA)**.

O projeto demonstra, de forma prática, como algoritmos clássicos de **Visão Computacional** funcionam internamente, explorando operações matemáticas como convolução, cálculo de gradientes e geração de mapas de características a partir de imagens.

---

# 📁 Estrutura do Projeto
├── Topicos1-2026.1-Tarefa1.ipynb
├── cano.webp
└── README.md


- **Topicos1-2026.1-Tarefa1.ipynb** → Notebook com toda a implementação da atividade  
- **badbunny.jpeg & deepfake.png** → Imagens utilizada para demonstração da extração de bordas

---

# ⚙️ Descrição da Atividade

A atividade consiste em aplicar o **Filtro Sobel** para identificar bordas em uma imagem e gerar representações derivadas que podem ser utilizadas como **vetores de características** em tarefas de visão computacional.

O processo implementado envolve:

1. **Leitura da imagem**
2. **Conversão para escala de cinza**
3. **Aplicação das máscaras Sobel**
4. **Cálculo dos gradientes horizontal e vertical**
5. **Cálculo da magnitude do gradiente**
6. **Cálculo da orientação das bordas**
7. **Construção de um vetor de características**

---

# 🔎 Etapas do Processamento

### 🔸 Convolução com Filtro Sobel
Aplicação das máscaras Sobel nas direções **X** e **Y** para capturar variações de intensidade.

- Entrada: imagem em escala de cinza  
- Saída: gradientes **Gx** e **Gy**

---

### 🔸 Magnitude do Gradiente
A intensidade da borda é calculada a partir dos gradientes:

\[
G = \sqrt{G_x^2 + G_y^2}
\]

Essa etapa destaca regiões onde há mudanças bruscas de intensidade.

---

### 🔸 Orientação das Bordas
A direção das bordas é obtida por:

\[
\theta = \arctan \left(\frac{G_y}{G_x}\right)
\]

Essa informação é importante para algoritmos que analisam **direção e estrutura das bordas**.

---

### 🔸 Vetor de Características
Após o processamento, as matrizes resultantes podem ser **planificadas (flatten)** para formar um vetor que representa a imagem.

Esse vetor pode ser utilizado em tarefas como:

- classificação de imagens  
- detecção de objetos  
- reconhecimento de padrões  

---

# 🧰 Tecnologias Utilizadas

- **Python**
- **OpenCV (`cv2`)** – manipulação de imagens  
- **NumPy** – operações matriciais  
- **Matplotlib** – visualização de resultados  
- **PyTorch** – operações de convolução (`torch.nn.functional`)

---

# 👥 Autores

| [<img src="https://github.com/thiagocordeirum.png?size=100" width=100><br><sub>Thiago Cordeiro</sub>](https://https://github.com/thiagocordeirum) | [<img src="https://github.com/cpc231341.png?size=100" width=100><br><sub>Yago Feitoza</sub>](https://github.com/cpc231341) |
|:---:|:---:|

---

# 👩‍🏫 Orientação

**Profa. Dra. Elloá B. Guedes**  
Escola Superior de Tecnologia – Universidade do Estado do Amazonas (EST/UEA)

📅 Data da atividade: **03 de março de 2026**