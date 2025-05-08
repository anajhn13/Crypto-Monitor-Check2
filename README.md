# Crypto-Monitor-Check2

Sobre o projeto: 
App Android que consulta o preço da Bitcoin no Mercado Bitcoin e exibe formatado em reais quando o usuário clica em "atualizar".

Imagens do projeto: 

Zerado: 

![zerado](https://github.com/user-attachments/assets/aa07e7b4-754b-4236-847c-1cadd7c86405)

Atualizado: 

![atualizado](https://github.com/user-attachments/assets/2d4eb4a7-107f-45c4-9250-ca7fba75d9cc)

Fluxo do projeto: 

-Inicialização (onCreate)
Define o listener do botão "Refresh" para chamar a API quando pressionado.

-Requisição à API (makeRestCall)
Usa Retrofit (via MercadoBitcoinServiceFactory) para fazer uma chamada HTTP à API.

-Exibição dos Dados
Se a chamada for bem-sucedida (response.isSuccessful):
Formata o preço em Real (R$) usando NumberFormat.
Converte o timestamp da API em uma data legível (dd/MM/yyyy HH:mm:ss).
Atualiza os TextViews (lbl_value e lbl_date) na tela.
Se falhar, mostra uma mensagem de erro via Toast.

Tecnologias usadas: 

Retrofit + Gson: Para chamadas HTTP e conversão de JSON em objetos Kotlin.
Coroutins: Para chamadas assíncronas (evitar bloqueio da UI).
SimpleDateFormat & NumberFormat: Para formatação de data e valor monetário.
Android Jetpack (AppCompatActivity, ViewBinding via findViewById): Para a estrutura básica do app.
