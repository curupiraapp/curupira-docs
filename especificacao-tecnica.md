# Curupira - Especificação técnica

## Plataforma

Projeto Curupira é composto por dois Apps mobile (Curupira e Curupira - Fiscal) e um Web App.

1. **Curupira (v1.0.2)**: enviar as denúncias e acompanhar seu andamento e averiguação.
2. **Curupira - Fiscal (v1.0.1)**: gerenciar as denúncias recebidas, usuários, visualizar estatísticas e etc.
3. **Curupira - Web (v1.0)**: visualizar denúncias recebidas, gerar documentos, visualizar estatísticas e usuários ativos.

## Tecnologias:

Os Apps mobile são desenvolvidos para dispositivos Android (5.0+) utilizando a linguagem de programação Java e o Android SDK 21.
Já a versão Web é desenvolvida utilizando apenas a linguagem JavaScript e hospedada no GitHub Pages. O Curupira ainda não possui uma versão para iOS.

Todos os apps usam o Firebase como back-end através de seus serviços: Realtime Database, Cloud Storage, Cloud Functions e Auth.
Estes, por sua vez, fornecem toda a infraestrutura necessária para envio de denúncias em tempo real, armazenamento de mídias, notificações e autenticação de usuários.

Outro serviço utilizado é o Google Maps para fornecer os dados de geolocalização.

## Segurança

Todas as denúncias são anônimas, ou seja, nenhum dado pessoal é solicitado ao denunciante para utilização do app. Um ID de identificação é gerado automaticamente, 
apenas para viabilizar o recebimento de notificações e acompanhar o andamento de suas denúncias. Esse identificador é associado a cada instância do app instalado,
ou seja, em caso de desinstalação ou perda do dispositivo, não será possível continuar recebendo as atualizações das denúncias.

Quanto ao envio dos dados ao Firebase, seus serviços utilizam certificados SSL e fornecem mecanismos de autenticação e permissão no acesso aos dados.
Todos estes estão configurados para requisitar autenticação, seja para leitura ou escrita de dados.

## Links:

- Curupira: https://play.google.com/store/apps/details?id=com.ufpi.curupira
- Curupira - Fiscal: https://play.google.com/store/apps/details?id=com.ufpi.curupirafiscal
- Curupira Web: https://curupiraapp.github.io
- Política de privacidade: https://github.com/curupiraapp/curupira-docs/blob/master/politica_privacidade_curupira.pdf
- Firebase: https://firebase.google.com
- Google Maps: https://cloud.google.com/maps-platform

## Contatos:

- Email: curupiraaplicativo@gmail.com
- Instagram: @curupira18

<br>
<p align="center"><i>Desenvolvedores - Projeto Curupira - Janeiro de 2020</i></p>
