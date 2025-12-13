# Thornton Pickard Full-Stack Deployment

This repository contains the necessary configuration files (`docker-compose.yml` and `.env.example`) to run the full Thornton Pickard application suite, which comprises three separate repositories:

1.  **Go Gin API:** `thornton-pickard-api`
2.  **React UI:** `my-modern-react-setup`
3.  **PostgreSQL Database**

# ⚙️ Quick Start Setup

To run the entire stack, follow these steps. **The key is to maintain a specific directory structure for Docker Compose to find the build contexts.**

1.  **Create a central workspace directory** (e.g., `Projects`). Navigate into it.

2.  **Clone all three repositories into this central workspace:**

    ```bash
    # Ensure you are in the central workspace directory (e.g., /path/to/Projects)
    git clone [https://github.com/Candoo/Pickard-Index.git](https://github.com/Candoo/Pickard-Index.git)
    git clone <URL for thornton-pickard-api>
    git clone <URL for my-modern-react-setup>
    ```

    **Your resulting directory structure MUST look like this:**
    ```
    /Projects/
    ├── thornton-pickard-api/
    ├── my-modern-react-setup/
    └── Pickard-Index/   <-- YOU ARE HERE
    ```
    

3.  **Navigate into the deployment directory:**

    ```bash
    cd Pickard-Index
    ```

4.  **Configure environment:**

    ```bash
    cp .env.example .env
    # NOTE: Review and edit the .env file to change credentials.
    ```

5.  **Launch the stack:**

    ```bash
    docker compose up -d --build
    ```

The application should be available at `http://localhost:3000`.