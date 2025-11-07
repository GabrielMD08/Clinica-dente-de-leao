# Site/Sistema Web: Clínica Dente de Leão 🦷

**Status do Projeto:** MVP (Produto Mínimo Viável) Entregue - Projeto de Conclusão (TCC).

**Descrição:** Aplicação web desenvolvida em ambiente acadêmico (SENAI) que simula um Sistema de Gestão para Clínicas Odontológicas. O foco foi na estrutura Back-end de cadastro, autenticação e gerenciamento de agendamentos.

---

## 💻 Tecnologias e Funcionalidades Chave

Este projeto demonstra familiaridade com o ecossistema Django e a aplicação de lógica de negócio específica, utilizando as seguintes bibliotecas:

* **Django 5.0.6:** Framework Back-end principal.
* **django-cpf-cnpj:** Implementação de validação de dados para **CPF e CNPJ** nos formulários, garantindo a integridade dos cadastros de pacientes e parceiros.
* **holidays & tzdata:** Utilizadas para gerenciar fusos horários e **bloquear agendamentos** em feriados nacionais, aplicando lógica de negócio específica para a área da saúde.
* **django-widget-tweaks:** Usado para customizar a aparência dos formulários (UX/Design) diretamente nos templates, focando na melhoria da **usabilidade** da interface.
* **Back-end/Front-end:** Python, HTML, CSS e JavaScript.

---

## 🛠️ Configuração Local (Passo a Passo)

Siga os passos abaixo para preparar o ambiente e rodar o projeto.

### 1. Clonar e Acessar o Repositório

```bash
git clone https://github.com/GabrielMD08/Clinica-dente-de-leao.git
cd Clinica-dente-de-leao
```

### 2. Configurar e Ativar o Ambiente Virtual (venv)

```bash
python -m venv venv
# No Linux/macOS:
source venv/bin/activate
# No Windows:
.\venv\Scripts\activate
```
### 3. Instalar Dependências

Instale todas as bibliotecas necessárias listadas no `requirements.txt.`

```Bash
pip install -r requirements.txt
```

### 4. Configurar Variáveis de Ambiente (Segurança)

Este projeto segue o padrão de segurança Twelve-Factor App e utiliza o `python-decouple` para gerenciar a `SECRET_KEY`. O arquivo `.env` está oculto no GitHub.

1. Crie um novo arquivo chamado .env na raiz do projeto.

2. Gere uma nova e segura SECRET_KEY usando o comando:
    ```bash
    python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"    
    ```
3. Cole a chave gerada no arquivo .env no seguinte formato:
    ```
    SECRET_KEY= {cole_a_chave_gerada_aqui}
    DEBUG=True
    ```
### 5. Executar Migrações e Iniciar Servidor

```bash
python manage.py migrate
python manage.py runserver
```
O sistema estará acessível em http://127.0.0.1:8000/ 