## PUC-Tools 📚

O PUC-Tools muda a maneira como você interage com seus dados de Atividades Complementares da PUC-Rio, oferecendo uma interface de linha de comando amigável e uma API poderosa para integração perfeita. 

### Recursos ✨

* **Recuperação de Dados Sem Esforço:** 
    * Acesse os dados de suas atividades, incluindo número da atividade, local, datas (início, fim, status) e status atual.
    * Chega de navegação manual e extração de dados do site da PUC-Rio.
* **Opções Flexíveis de Acesso:**
    * **Interface de Linha de Comando (CLI):** Ideal para recuperação rápida de dados e acesso em movimento.
    * **API RESTful:** Integre seus dados de atividades com outros aplicativos ou crie painéis personalizados.
* **Automação Perfeita:**
    * O Playwright lida com a extração de dados nos bastidores, garantindo uma experiência tranquila e eficiente.
* **Pronto para Docker:**
    * O Dockerfile fornecido simplifica a implantação e garante uma execução consistente em diferentes ambientes. 

### Como Começar 🚀

**1. Configuração**

* **Pré-requisitos:** Certifique-se de ter o Python 3.10+ instalado.
* **Instale as Dependências:** 
    * Abra seu terminal e navegue até o diretório do projeto.
    * Execute: `pip install -r requirements.txt`

**2. Usando a Interface de Linha de Comando (CLI):**

* **Recupere Seus Dados:**
    * No seu terminal, execute: 
    ```bash
    python CLI.py <sua_matricula> <sua_senha>
    ```
    * Substitua `<sua_matricula>` e `<sua_senha>` por suas credenciais PUC-Rio.
    * Seus dados de atividades serão exibidos no terminal. 

**3. Usando a API (Opcional):**

* **Execute o Servidor API:**
    * No seu terminal, execute: 
    ```bash
    python main.py
    ```
* **Acesse a API:**
    * A API estará disponível em `http://localhost:5000/api/atividades`.
    * Você precisará fornecer sua matrícula e senha nos cabeçalhos da solicitação.
    * Consulte o código `main.py` para obter mais detalhes sobre o uso da API. 

**4. Opções Adicionais:**

* **Modo Headless:** 
    * Para executar o Playwright sem uma janela do navegador visível, adicione a flag `--headless` ao comando CLI:
    ```bash
    python CLI.py <sua_matricula> <sua_senha> --headless 
    ``` 

### Docker 🐳

* **Construa a Imagem Docker:**
    ```bash
    docker build -t puc-tools .
    ```
* **Execute o Container:**
    ```bash
    docker run -it puc-tools python CLI.py <sua_matricula> <sua_senha>
    ```
