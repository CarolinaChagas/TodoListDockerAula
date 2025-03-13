# TodoListDockerAula

Aula de monolito com docker, docker-compos e nginx.

## Como rodar o Projeto 

Após realizar todas as configurações necessárias e instalar as dependências, é necessário executar alguns comandos para que o projeto rode, segue abaixo os comandos necessários:

1. docker compose up -d --build  #Serve para criar uma imagem e iniciar o contâiner em segundo plano.

2. docker compose logs -f app1 # Serve para verificar os logs na rota app1.

3. docker compose logs -f app2 #Também serve para verificar os logs na rota app2.

4. Após executar os comandos acima, abra o navegador em https://localhost/, clique em avançado e após clique em aceitar o risco e continuar, pronto, irá aparecer a lista de tarefas.

Além disso, teste se o sistema ainda continuará executando sem dar erro, para isso execute. 

5. docker compose stop app1 #Este comando irá excluir a rota app1 e após isso terá que ser feito um balanceamento de carga, poderá demorar um pouco, no entanto o sistema ainda terá que mostrar a lista de tarefas, já que possui a rota app2.

6. docker compose stop app2 #Este comando irá excluir a rota app2 e o sistema terá que utilizar a rota de backup (app3) que retornará na tela "Você agora está rodando o backup!!!" 

Agora que o sistema já está rodando e já foi feito o que precisava ser feito, temos que executar o seguinte comando: 

7. docker compose down # Serve para parar e remover o container associado que foi criado a partir do comando docker-compose up.

Caso queira remover o container, siga os passos abaixo:

8. docker stop nome_do_container #Serve para parar o container.

9. docker rm nome_do_container #Por fim, irá remover o container do seu projeto. 