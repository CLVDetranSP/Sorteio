🎲 Sorteador de Fila Única (Leiloeiros/Avaliadores)
Arquivo Principal: index.html (Contém todo o código HTML, CSS e JavaScript)

Este repositório hospeda o código-fonte completo e aberto do utilitário de Sorteio Randômico para Formação de Fila Única, destinado à Coordenadoria de Leilões do DETRAN/SP.

O objetivo desta ferramenta é garantir a impessoalidade, a rotatividade justa e a transparência integral na escalação de Leiloeiros e Avaliadores credenciados para os serviços relacionados aos leilões.

🛡️ Transparência e Auditabilidade
O código utiliza um algoritmo de geração de números pseudoaleatórios que é reproduzível. Isso significa que, fornecendo a mesma Semente (Seed) e a mesma lista de entrada, o resultado do sorteio será sempre idêntico.

1. Semente (Seed)
A semente é o principal fator de transparência:

Semente Informada: Se a semente for preenchida pelo usuário (ex: a data do leilão), o sorteio é determinístico e pode ser repetido por qualquer pessoa.

Semente Aleatória: Se o campo for deixado vazio, o sistema gera uma semente verdadeiramente randômica (crypto.getRandomValues) e a exibe no resultado. Esta semente deve ser registrada em ata para que o sorteio possa ser auditado e validado a qualquer momento.

2. Relatório de Auditoria
Após cada sorteio, o sistema gera um Relatório de Auditoria detalhado, contendo:

Semente Utilizada: O valor numérico da semente que gerou o sorteio.

Hashes (SHA-256): Hashes criptográficos da lista de entrada, da lista processada e da lista final. A comparação desses hashes garante que a lista não foi alterada após o sorteio.

Detalhes de Processamento: Informação sobre se as opções de "remover duplicados" e "ordenar antes de embaralhar" foram aplicadas.

🚀 Como Utilizar (Validação e Execução)
O sistema é um único arquivo HTML/JavaScript e não requer instalação.

Abertura: Baixe ou clone o repositório. Simplesmente abra o arquivo index.html em qualquer navegador moderno.

Lista de Entrada: Cole a lista completa e atualizada dos Leiloeiros/Avaliadores credenciados e aptos na caixa de texto, um nome por linha.

Execução: Clique em "Sortear".

Ata/Registro: Registre a Semente exibida no resultado e anexe o Relatório de Auditoria (Baixar TXT) na ata ou processo administrativo referente ao sorteio.

Algoritmo de Randomização
O código utiliza a função Mulberry32 para a geração de números pseudoaleatórios, um algoritmo de domínio público conhecido por ser rápido e produzir bons resultados para este tipo de aplicação, desde que a semente inicial seja segura. A semente inicial, quando não fornecida, é gerada pela API criptográfica nativa do navegador (crypto.getRandomValues).

💻 Desenvolvimento e Manutenção
O código está contido integralmente no arquivo index.html.

Linguagem: JavaScript (cliente-side)

Estilização: Tailwind CSS (via CDN)

Randomização: Funções mulberry32 e shuffle implementadas em JavaScript.
