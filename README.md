# POC Docker-compose

Esta poc tem por objetivo colocar em pratica conhecimentos adquiridos no uso de Docker. Dinamica que serve de inspiração para aplicação do docker em ambiente profissional e outras soluçoes, Cada parte da aplicação esta contida em um container. Que são montados apartir de uma composição feita pelo Docker-compose
Trata-se de uma solução assincrona para envio de e-mail de forma esclavél.

- Contando com um frontend onde se encontra um formulário para envio de mensagens, neste formulario foi configurado um proxi reverso.

- O backend da aplicação desenvolvida em Python, que recebe o request, persiste em banco postgres e  envia para uma fila baseada em Redis

-A aplicação worker "SIMULA" o envio de email pegando as mensagens da fila,podendo ser escalado.

'
## Instalação e execução da aplicação

## Executando local

- Realize o clone da aplicação

```
git clone https://github.comferpioli/email-worker-compose.git
```
- Para executar o docker-compose em modo daemon

```
docker-compose up -d 
```
- Acesse a aplicação em localhost

- Para verificar os logs

```
docker-compose logs -f -t
```
