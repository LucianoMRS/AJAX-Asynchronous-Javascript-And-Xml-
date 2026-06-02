# AJAX-Asynchronous-Javascript-And-Xml-
Aluno: Luciano Morais Rodrigues Dos Santos
Matrícula: 2025.15.735
Turma: 40.15.2025 - Curso Superior de Tecnologia em Análise e Desenvolvimento de Sistemas

===================================================================================================================================================================

1. XMLHttpRequest (XHR)
Vantagens: 
-Permite acompanhar o progresso de uploads nativamente.

Desvantagens:
-Sintaxe excessivamente detalhada e verbosa.
-Propensa ao "Callback Hell" (aninhamento excessivo de funções quando uma requisição depende do resultado de outra), tornando o código ilegível e difícil de manter.

2. Promises (Promessas)
Vantagens:
-Resolve o Callback Hell permitindo o encadeamento linear de operações.
-Centraliza o tratamento de erros em um único bloco .catch() ao fim da cadeia.

Desvantagens:
-Se a cadeia de .then() for muito longa, o código ainda pode se tornar visualmente complexo (conhecido como Promise Land).

3. Fetch API
Vantagens:
-Sintaxe limpa, focada em requisições modernas (fácil de ler e configurar cabeçalhos, métodos, corpo, etc.).
-Integra-se perfeitamente com os conceitos modernos da web (como Service Workers e Streams).

Desvantagens:
-Diferente do XHR, o fetch() não falha (não entra no .catch()) em caso de erros HTTP como 404 ou 500. Ele só rejeita a Promise se houver uma falha de rede (ex: falta de internet). É necessário validar manualmente a propriedade response.ok.
-Não possui suporte nativo simples para ler o progresso de uploads.

4. Async / Await
Vantagens:
-Permite escrever código assíncrono que se parece visualmente e estruturalmente com um código síncrono.
-O tratamento de erros é feito com os blocos tradicionais try / catch, comuns na maioria das linguagens de programação.
-Altíssima legibilidade e facilidade de manutenção.

Desvantagens:
-Requer atenção, pois esquecer de digitar a palavra await fará com que o código continue executando antes de receber os dados, gerando bugs difíceis de rastrear para iniciantes.   
