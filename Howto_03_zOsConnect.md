# z/OS Connect
---
>O z/OS Connect é, tecnicamente, a camada de software que transforma o mainframe de uma "caixa preta" em um provedor de serviços de nuvem padrão de mercado.

**Como funciona:** No passado, para um sistema externo (como o aplicativo do banco no Google Cloud) falar com o mainframe, era necessário usar protocolos complexos e proprietários. O z/OS Connect elimina isso. Ele atua como um "tradutor" em tempo real.

**Transformação em APIs REST/JSON:** Ele pega os programas COBOL e os dados no banco de dados Db2 e os expõe como APIs RESTful (o padrão usado por toda a internet). Quando você faz uma consulta no app (mobile ou web), o app faz uma chamada HTTPS simples; o z/OS Connect recebe isso, traduz para o mainframe, busca a informação e devolve um arquivo JSON para o app.

**Desenvolvimento Ágil:** Ele permite que os desenvolvedores criem novas funcionalidades usando ferramentas modernas (como o Swagger/OpenAPI) sem precisarem ser especialistas em linguagens de mainframe.

**Performance:** Por rodar dentro do próprio ecossistema do z17, essa tradução ocorre com latência quase zero, garantindo que a experiência do usuário no celular seja instantânea.