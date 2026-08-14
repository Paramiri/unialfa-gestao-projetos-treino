# UNIALFA — Sistema de Gestão de Projetos (Ambiente de Treinamento)

Este repositório é um **espelho de treinamento/demonstração** do sistema de produção
(`Paramiri/unialfa-gestao-projetos`), publicado via GitHub Pages neste próprio endereço
(`https://paramiri.github.io/unialfa-gestao-projetos-treino/`).

Repositório público (exigência do GitHub Pages no plano gratuito) — por isso as
credenciais das contas de treinamento **não** ficam neste README. Peça-as a quem
administra o ambiente.

## O que é diferente da produção

- Aponta para um **projeto Supabase separado** (`unialfa-treinamento`), com schema e
  políticas de RLS idênticos à produção, mas **dados 100% fictícios**.
- Tem uma **terceira opção de login** na tela de entrada, além do link mágico e do
  SSO Microsoft: um menu suspenso com os 6 papéis (Solicitante, Gerente de Projetos,
  Gestor Responsável, Dono do Negócio, Alta Gestão, PMO/Admin) — a pessoa só escolhe
  o papel e clica em Entrar, sem digitar e-mail nem senha. Por trás, cada papel está
  ligado a uma das 6 contas fixas (`solicitante@treino.unialfa.local`,
  `gp@treino.unialfa.local`, `gestor@treino.unialfa.local`, `dono@treino.unialfa.local`,
  `altagestao@treino.unialfa.local`, `admin@treino.unialfa.local`), com a senha
  compartilhada preenchida automaticamente pelo front-end.
- Notificação por e-mail e importação por IA (transcrição/áudio) ficam **desligadas**
  por padrão nesse ambiente.

## Como sincronizar com a produção

Este repositório é atualizado manualmente (não há workflow automático replicando
commits de `unialfa-gestao-projetos` para cá) — mas, por regra do projeto, deve ser
mantido em dia: sempre que um arquivo do site de produção muda, o mesmo arquivo é
copiado para cá no mesmo commit (ou logo em seguida), para o ambiente de treino
continuar refletindo a mesma versão do sistema. Basta copiar os arquivos alterados
do repositório principal (`unialfa-gestao-projetos`) para cá, mantendo o mecanismo
de troca de backend por hostname (`IS_TREINO = location.href.indexOf('treino')>-1`)
intacto — ele já está em cada um dos arquivos HTML e não precisa de nenhuma edição
manual para continuar funcionando aqui.

Não copie o arquivo `CNAME` do repositório principal — este repositório usa o
endereço padrão do GitHub Pages, sem domínio próprio.
