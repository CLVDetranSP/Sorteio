📘 Sorteio de Fila Única — Leiloeiros e Avaliadores
Coordenadoria de Leilões de Veículos — DETRAN-SP

Sistema público para geração de ordem aleatória de profissionais, com auditoria completa.

📌 Finalidade do Sistema

Este repositório disponibiliza o código-fonte completo do Sistema de Sorteio de Fila Única da Coordenadoria de Leilões de Veículos do DETRAN-SP.

O sistema é utilizado para:

Sortear de forma transparente e auditável a ordem de Leiloeiros e Profissionais terceirizados habilitados para avaliação veicular;

Garantir isonomia entre os participantes;

Registrar rastreabilidade e integridade dos resultados produzidos;

Disponibilizar o código publicamente para evitar dúvidas sobre manipulação, vieses ou alterações indevidas durante o processo de sorteio.

O objetivo é reforçar o compromisso institucional com a transparência, segurança jurídica, controle social e boa governança pública.

⚙️ Como o Sistema Funciona

O sistema é executado diretamente no navegador e não depende de servidor.
Todo o processamento (incluindo o sorteio e geração de auditoria) ocorre de forma local, reforçando a integridade do processo.

Fluxo operacional

O usuário (servidor responsável) insere a lista de nomes em uma caixa de texto.

O sistema:

limpa a lista,

remove duplicados,

ordena, se o usuário desejar,

aplica o sorteio utilizando um gerador de números pseudoaleatórios com semente controlável.

Após o sorteio:

o botão “Realizar Sorteio” é desabilitado, impedindo múltiplos sorteios inadvertidos;

o relatório de auditoria é gerado automaticamente;

o usuário pode baixar o relatório em TXT ou PDF.

🔐 Integridade e Auditoria

O sistema possui mecanismos formais de auditoria para garantir que o sorteio não seja adulterado.

✔️ Registro de auditoria

O relatório inclui:

Data e hora completa do sorteio;

Informações do navegador e ambiente;

Lista original de participantes;

Lista processada (sem duplicados e aplicada a limpeza);

Lista final sorteada;

Hashes independentes:

HASH da semente do sorteio

HASH das entradas brutas

HASH das entradas processadas

HASH da saída (resultado final)

HASH do relatório final completo (ID único auditável)

O último hash funciona como identificador único do sorteio, permitindo verificar posteriormente a integridade, garantindo que:

o relatório não foi alterado;

o sorteio pode ser reproduzido (quando a mesma semente for utilizada);

o processo pode ser auditado por qualquer pessoa.

✔️ Transparência do código

Todo o código é aberto neste repositório, possibilitando:

Verificação de integridade;

Auditoria externa;

Replicação independente do sorteio;

Eliminação de dúvidas sobre manipulação.

🛠️ Tecnologias Utilizadas

HTML + TailwindCSS — interface leve e responsiva

JavaScript — lógica do sorteio e auditoria

jsPDF — geração de PDF diretamente no navegador

GitHub Pages — hospedagem pública e imutável

Nenhum backend, servidor ou banco de dados é usado.

🚀 Como Executar

Acesse o GitHub Pages configurado neste repositório
(ou abra o arquivo index.html localmente em qualquer navegador moderno).

Cole a lista de participantes no campo indicado.

Clique em Realizar Sorteio.

Baixe os arquivos de auditoria (TXT ou PDF) conforme necessidade.

Clique em Limpar para habilitar um novo sorteio.

🧩 Estrutura do Repositório
/
├── index.html    # Interface completa do sistema
├── README.md     # Este documento
└── /assets       # (opcional) Pastas para logos ou arquivos adicionais

🧾 Conformidade e Princípios

Este projeto atende aos princípios constitucionais aplicáveis à Administração Pública:

Legalidade

Impessoalidade

Moralidade

Publicidade

Eficiência

E reforça diretrizes de:

Transparência ativa

Controle social

Rastreabilidade

Isonomia no atendimento

🛡️ Aviso Institucional

Este sistema é disponibilizado pela Coordenadoria de Leilões de Veículos do DETRAN-SP exclusivamente para:

sorteios oficiais relacionados às atividades da Coordenadoria;

processos de gestão dos leilões veiculares;

reforço da transparência pública.

Não deve ser utilizado para fins pessoais, comerciais ou não autorizados.
