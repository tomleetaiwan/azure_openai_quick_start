# 關於本 Python Notebook 

內容是修改自 https://github.com/Azure/azure-openai-samples/tree/main/quick_start ，旨在協助開發人員快速了解 Azure OpenAI Service 基本開發概念

## 環境準備

- 備妥 Microsoft Azure 訂閱帳號
- 已經申請核准建立妥 Azure OpenAI Service 資源
- 已經於 Azure AI Studio 內建立好以下模型之部署 (deployment)
    + gpt-35-turbo
    + text-embedding-ada-002
    + text-davinci-003

- 備妥 Python 3.11 與 Jupyter Notebook 相容之編輯執行環境

## 設定作業系統之環境變數
當建妥 Azure OPENAI Service，透過 Azure Portal 取得呼叫所需的 API 鍵值與呼叫端點，設定以下三個環境變數
- **OPENAI_API_BASE**  API 呼叫端點，例如 'https://<您的 Azure OpenAI 資源名稱>.openai.azure.com/'
- **OPENAI_API_KEY** 所需之 API 鍵值，例如 '1234567890abcdef1234567890abcdef'
- **DEPLOYMENT_NAME**  所建立的模型部署名稱。例如 'gpt-35-turbo' 

若不想透過環境變數設定，則可直接修改本 Notebook 中的程式碼，例如:

 ```python
API_KEY = os.getenv('OPENAI_API_KEY','1234567890abcdef1234567890abcdef').strip()
....
RESOURCE_ENDPOINT = os.getenv('OPENAI_API_BASE','https://<您的 Azure OpenAI 資源名稱>.openai.azure.com/').strip()
...
MODEL = os.getenv('DEPLOYMENT_NAME','gpt-35-turbo').strip()
 ```

## 逐一執行本 Notebook 中的程式碼