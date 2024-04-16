## PUC-Tools

PUC-Tools simplifies the way you interact with your PUC-Rio Atividades Complementares data, providing both a user-friendly command-line interface and a powerful API for seamless integration. 

### Features ✨

* **Effortless Data Retrieval:** 
    * Access your activities data, including activity number, location, dates (start, end, status), and current status.
    * No more manual navigation and data extraction from the PUC-Rio website.
* **Flexible Access Options:**
    * **Command-Line Interface (CLI):** Ideal for quick data retrieval and on-the-go access.
    * **RESTful API:** Integrate your activities data with other applications or build custom dashboards.
* **Seamless Automation:**
    * Playwright handles data extraction behind the scenes, ensuring a smooth and efficient experience.
* **Docker Ready:**
    * The provided Dockerfile simplifies deployment and ensures consistent execution across environments. 

### Getting Started 🚀

**1. Setup**

* **Prerequisites:** Ensure you have Python 3.10+ installed.
* **Install Dependencies:** 
    * Open your terminal and navigate to the project directory.
    * Run: `pip install -r requirements.txt`

**2. Using the Command-Line Interface (CLI):**

* **Retrieve Your Data:**
    * In your terminal, run: 
    ```bash
    python CLI.py <your_matricula> <your_senha>
    ```
    * Replace `<your_matricula>` and `<your_senha>` with your actual PUC-Rio credentials.
    * Add the `--headless` flag if you prefer to run the browser in the background:
    ```bash
    python CLI.py <your_matricula> <your_senha> --headless 
    ``` 

**3. Using the API:**

* **Run the API Server:**
    * In your terminal, run:
    ```bash
    python main.py
    ``` 
    * This will start the API server, typically on `http://127.0.0.1:5000/`.
* **Retrieve Data via API Endpoint:**
    * Send a GET request to the `/api/atividades` endpoint, including your credentials in the headers:
    ```bash
    curl -X GET http://127.0.0.1:5000/api/atividades \
        -H "Matricula: <your_matricula>" \
        -H "Senha: <your_senha>"
    ```

**4. Docker Deployment (Optional):**

* **Build the Docker Image:**
    * In your terminal, run:
    ```bash
    docker build -t puc-tools .
    ```
* **Run the Docker Container:**
    * You can then run the container with:
    ```bash
    docker run -p 5000:5000 puc-tools
    ```
    * Access the API at `http://localhost:5000/api/atividades` with your credentials in the headers as shown above.

### Contributing and Support 🤝

* Feel free to fork the repository and contribute to its development.
* For any questions or support, please open an issue on the GitHub repository.
