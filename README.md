# Demo
Home Page
![Screenshot 2024-06-21 185717](https://github.com/Vijeth-Rai/QA-chatbot-OpenAI/assets/57294003/914ece58-97ff-4773-9105-fc78c0c8d032)


Response for input
![Screenshot 2024-06-21 185948](https://github.com/Vijeth-Rai/QA-chatbot-OpenAI/assets/57294003/19903cea-53c3-4136-a883-6e95d9d7f527)


# Conversational Q&A Chatbot

Welcome to the Q&A Chatbot! This project features a chatbot built with Streamlit and Langchain with OpenAI and HuggingFace APIs, designed to interact with users in a conversational manner. The chatbot is pre-configured to behave like a comedian AI assistant, providing both informative and entertaining responses.

## Features

- **Conversational AI**: Engages users with dynamic and interactive dialogue.
- **Streamlit Interface**: A user-friendly web interface for seamless interactions.
- **Langchain Integration**: Utilizes advanced language models to generate responses.
- **Dockerized Deployment**: Easy to deploy and run in a containerized environment.

## Prerequisites

Before you begin, ensure you have the following installed:

- Docker
- Python 3.9+
- Git (optional, for cloning the repository)

## Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Installation

1. **Clone the repository (if applicable)**

   ```sh
   git clone https://github.com/Vijeth-Rai/QA-chatbot-OpenAI.git
   cd QA-chatbot-OpenAI
   ```

2. **Create a `.env` file**

   Create a `.env` file in the root directory of your project and add your OpenAI API key.

   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   ```

3. **Install dependencies**

   Create a `requirements.txt` file with the following content:

   ```text
   streamlit
   python-dotenv
   langchain
   openai
   ```

4. **Build the Docker image**

   ```sh
   docker build -t qa-chatbot .
   ```

5. **Run the Docker container**

   ```sh
   docker run -p 8501:8501 qa-chatbot
   ```

6. **Access the application**

   Open your web browser and navigate to `http://localhost:8501` to start interacting with the chatbot.

### Application Structure

- **`app.py`**: The main application file containing the Streamlit app code.
- **`requirements.txt`**: Lists the Python dependencies required for the project.
- **`Dockerfile`**: Docker configuration file to build the container.
- **`.env`**: Environment file to store sensitive information like API keys.

### Usage

1. **Start the Application**

   After running the Docker container, open your browser and go to `http://localhost:8501`. You will see the chatbot interface.

2. **Interact with the Chatbot**

   - Enter your questions in the input box.
   - Click the "Ask the question" button to submit your question.
   - The chatbot will respond, and you will see the conversation displayed on the screen.

### Customization

You can customize the chatbot's behavior by modifying the initial system message in the `app.py` file:

```python
if 'flowmessages' not in st.session_state:
    st.session_state['flowmessages']=[
        SystemMessage(content="You are a comedian AI assistant")
    ]
```

Change the content to fit your desired chatbot persona.

### Contact

For any inquiries or support, please contact:

- **Name**: Vijeth Rai
- **Email**: vijethrai98@gmail.com
- **LinkedIn**: https://www.linkedin.com/in/rai-vijeth/

Thank you for checking out the Conversational Q&A Chatbot! Hope you find it useful and enjoyable. Happy chatting!
