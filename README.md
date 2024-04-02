# APS-8-SEMESTRE

COMO RODAR O PROJETO BAIXADO

Instalar todas as dependencias indicada pelo package.json
##### npm install

Rodar o projeto React - Front-end
##### npm start

Rodar o projeto React - Back-end
##### nodemon app.js


REQUESTER COM MySQL PARA O PROJETO BD

Selecionando usuarios
##### select * from robotdelivery.usuarios;

Selecionando locais
##### select * from robotdelivery.locais;

Selecionando pacotes
##### select * from robotdelivery.pacotes;

Selecionando robo_entregador
##### select * from robotdelivery.robo_entregador;

Inserindo valor padrão no robo, por conta do FOREIGN KEY dos Pacotes 
##### INSERT INTO `robotdelivery`.`robo_entregador` (`ID_Robo`,`Nome`,`Localizacao_Atual`,`Status_Disponibilidade`)VALUES(1,"robo","sala 1","disponivel");

FOREIGN KEY dos Pacotes
##### ALTER TABLE robotdelivery.Pacotes ADD FOREIGN KEY(ID_Robo) REFERENCES robotdelivery.Robo_Entregador (ID_Robo);
##### ALTER TABLE robotdelivery.Pacotes ADD FOREIGN KEY(ID_User) REFERENCES robotdelivery.Usuarios (ID_User);
