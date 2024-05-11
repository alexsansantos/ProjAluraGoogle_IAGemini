# ProjAluraGoogle_IAGemini
Repositório do projeto de Imersão Alura e Google Gemini AI

Echoes - Seu chat além do tempo
Echoes é um chatbot experimental que utiliza o poder da IA do Google (Gemini) para simular conversas com figuras históricas, personalidades famosas e até mesmo entes queridos que já partiram.
Imagine:
Ter um diálogo inspirador com Steve Jobs sobre inovação e tecnologia.
Discutir os desafios da exploração espacial com Elon Musk.
Relembrar momentos especiais com alguém que você ama, através de suas palavras e pensamentos.
Como funciona?
Echoes utiliza informações disponíveis publicamente para construir um perfil da pessoa com quem você deseja conversar. A IA do Gemini então utiliza esse perfil para gerar respostas coerentes e personalizadas, simulando um diálogo autêntico.
Disclaimer:
A qualidade da conversa depende da quantidade e da qualidade das informações disponíveis sobre a pessoa com quem você deseja interagir.
Primeiros passos:
1. Instalação:
pip install -q -U google-generativeai
from google.colab import userdata
Use code with caution.
Bash
2. Configuração da API:
import google.generativeai as genai

GOOGLE_API_KEY = userdata.get('SECRET_KEY') 
genai.configure(api_key=GOOGLE_API_KEY)
Use code with caution.
Python
3. Parâmetros do Modelo:
generation_config = {
    "candidate_count": 1,
    "temperature": 0.5,
    #"top_p": 
}

safety_settings = {
    "HARASSMENT": "BLOCK_NONE",
    "HATE": "BLOCK_NONE",
    "SEXUAL": "BLOCK_NONE",
    "DANGEROUS": "BLOCK_NONE",
}

model = genai.GenerativeModel(model_name="gemini-1.0-pro",
                             generation_config=generation_config,
                             safety_settings=safety_settings)
Use code with caution.
Python
4. Iniciando a conversa:
chat = model.start_chat(history=[])
Use code with caution.
Python
5. Exemplo de interação:
response = chat.send_message("Seja Steve Jobs e me dê seu melhor conselho.")
print(response.text)
Use code with caution.
Python
Observações:
Este README fornece uma estrutura básica. Adapte o código e as instruções de acordo com as funcionalidades e interface do seu chatbot.
Certifique-se de ter uma conta no Google Cloud Platform e configurar a API Key corretamente.
Contribuições:
Contribuições são bem-vindas! Sinta-se à vontade para reportar bugs, sugerir melhorias ou enviar pull requests.
Explore o passado, inspire o futuro. Converse com Echoes!
