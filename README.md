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
- Tem uma **terceira opção de login** (e-mail/senha) na tela de entrada, além do link
  mágico e do SSO Microsoft — usa uma das 6 contas fixas, uma por papel
  (`solicitante@treino.unialfa.local`, `gp@treino.unialfa.local`,
  `gestor@treino.unialfa.local`, `dono@treino.unialfa.local`,
  `altagestao@treino.unialfa.local`, `admin@treino.unialfa.local`).
- Notificação por e-mail e importação por IA (transcrição/áudio) ficam **desligadas**
  por padrão nesse ambiente.

## Como sincronizar com a produção

Este repositório **não é atualizado automaticamente** a cada mudança em produção —
de propósito, para o ambiente de treino não mudar no meio de uma turma. Para atualizar
manualmente, copie os arquivos do repositório principal (`unialfa-gestao-projetos`)
para cá, mantendo o mecanismo de troca de backend por hostname (`IS_TREINO =
location.href.indexOf('treino')>-1`) intacto — ele já está em cada um dos arquivos
HTML e não precisa de nenhuma edição manual para continuar funcionando aqui.

Não copie o arquivo `CNAME` do repositório principal — este repositório usa o
endereço padrão do GitHub Pages, sem domínio próprio.
