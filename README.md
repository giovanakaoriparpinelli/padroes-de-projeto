Descrição do Problema:
Criamos uma simulação de um sistema de notificações de um pedido de e-commerce. Sempre que o status do pedido muda, diversos canais de notificação precisam ser acionados, como popup para o usuário, log na tela e console para desenvolvedores.

Este problema reflete a necessidade de:
- Desacoplamento entre quem gera os eventos (pedido) e quem recebe as notificações (canais).
- Flexibilidade para adicionar, remover ou alterar os canais sem alterar a lógica principal.
- Estratégias diferentes de exibição das notificações.

Justificativa dos Padrões Escolhidos:
- **Observer:** Permite que o pedido notifique dinamicamente qualquer número de canais (popup, console, log na tela) sem acoplamento direto.
- **Strategy:** Cada canal de notificação implementa uma estratégia diferente de como a mensagem será exibida (popup, console, UI).
- **Command:** As notificações são encapsuladas como comandos, permitindo que elas sejam executadas de forma uniforme, desacoplando a emissão da execução.

Esses padrões juntos tornam o sistema escalável, organizado e de fácil manutenção.
