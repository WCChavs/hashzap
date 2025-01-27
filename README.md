# hashzap

# Hashzap

O **Hashzap** é uma aplicação simples de chat, onde os usuários podem entrar em uma sala de chat, enviar mensagens e ver a lista de participantes. Quando um usuário entra no chat, todos os outros usuários são notificados e podem começar a interagir. Este projeto utiliza o framework **Flet** para criação da interface e lógica de interação.

## Funcionalidades

- **Iniciar Chat:** Um botão que permite ao usuário iniciar um chat, onde ele deve inserir seu nome.
- **Popup de Entrada:** Ao entrar no chat, o usuário vê um popup para inserir seu nome.
- **Mensagens no Chat:** Após entrar, o usuário pode enviar mensagens que aparecem para todos os participantes do chat. As mensagens são acompanhadas do nome do usuário.
- **Notificação de Entrada:** Quando um usuário entra no chat, todos são notificados de sua entrada.

## Estrutura do Código

1. **Importação do Flet**  
   A aplicação utiliza o Flet para criar a interface gráfica e gerenciar a interação do usuário.
   
2. **Funções Principais**
   - **`main(pagina)`**: Função principal que inicializa a interface da aplicação.
   - **`enviar_mensagem_tunel(mensagem)`**: Responsável por receber as mensagens enviadas e exibí-las para todos os usuários.
   - **`enviar_mensagem(evento)`**: Envia uma mensagem do usuário para todos os participantes.
   - **`entrar_popup(evento)`**: Abre o popup para que o usuário insira seu nome e entre no chat.
   - **`entrar_chat(evento)`**: Exibe o popup para o usuário entrar no chat.
   
3. **Componentes da Interface**
   - **`texto`**: Um texto que exibe "Hashzap" na tela.
   - **`botao_iniciar`**: Botão para iniciar o chat.
   - **`campo_mensagem`**: Campo de texto onde o usuário digita suas mensagens.
   - **`botao_enviar_mensagem`**: Botão para enviar as mensagens digitadas.
   - **`popup`**: Um popup onde o usuário insere seu nome antes de entrar no chat.
   - **`chat`**: A área onde as mensagens do chat são exibidas.

4. **Interatividade e Atualizações**
   - O **`pagina.pubsub.send_all`** é usado para enviar eventos de mensagens e entradas para todos os usuários conectados.
   - **`pagina.update()`** é chamado sempre que há uma atualização na interface, garantindo que os elementos da página sejam atualizados de acordo com as interações.

## Como Rodar

1. **Pré-requisitos**  
   Certifique-se de que você tem o **Flet** instalado. Se não tiver, instale via pip:
   ```bash
   pip install flet
   ```

2. **Rodar a aplicação**  
   Para rodar o aplicativo, basta executar o script Python:
   ```bash
   python hashzap.py
   ```

3. **Acessar no Navegador**  
   Após executar o código, abra o navegador e acesse `http://localhost:8000` para iniciar a interação com o chat.

## Melhorias Futuras

- **Persistência de Mensagens**: Adicionar a capacidade de salvar as mensagens trocadas em um banco de dados para que, quando o usuário voltar, ele possa visualizar o histórico do chat.
- **Identificação de Usuário**: Permitir que o nome do usuário seja único para evitar que dois usuários usem o mesmo nome.
- **Interface Melhorada**: Adicionar elementos de design para tornar a interface mais amigável, como emojis ou temas.

## Tecnologias Usadas

- **Flet**: Framework para construção da interface gráfica.
- **Python**: Linguagem de programação utilizada para o backend e lógica do chat.

## Contribuições

Sinta-se à vontade para contribuir com melhorias ou novos recursos para o Hashzap! Se tiver alguma ideia ou correção, basta criar um pull request.

## Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
