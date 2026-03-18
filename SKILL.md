---
name: assessment-conversa
description: cria json de transcrição e monta html via base.html
disable-model-invocation: true
---



1. Transcrever
1.1 Leia todos os arquivos dessa pasta que iniciem com 'TRANSC'. Esses arquivos são a transcrição de uma reunião
1.2 Use essa transcrição para gerar um arquivo chamado `resumo.json` na pasta em que está rodando o projeto
1.3 Salve o arquivo `resumo.json` nessa pasta
1.4 Ele deve ter o formato abaixo:

{
    "resumo": "",
    "problema_central": "",
    "necessidades": [
        {
            "necessidade": "",
            "desc_necessidade": ""
        },
        {
            "necessidade": "",
            "desc_necessidade": ""
        }
    ],
    "requisitos_tecnicos": [
        {
            "requisito": "",
            "desc_requisito": ""
        },
        {
            "requisito": "",
            "desc_requisito": ""
        }
    ],
    "insights": [
        "",
        "",
        ""
    ],
    "sentimentos": {
        "confiança": ,
        "entusiasmo": ,
        "colaboração": ,
        "satisfação": 
    },
    "bibliografia": [
        "",
        "",
        ""
    ],
    "markdown": "",
    "quando": "",
    "timeline": {
        "parte1": "",
        "parte2": "",
        "parte3": "",
        "parte4": "",
        "parte5": ""
    },
    "reuniao_em_numeros": [
        "",
        "",
        ""
    ],
    "perguntas_sem_respostas": [
        "",
        "",
        ""
    ],
    "contradicoes": [
        {
            "trechos": [
                "",
                ""
            ],
            "explicacao": ""
        },
        {
            "trechos": [
                "",
                ""
            ],
            "explicacao": ""
        },
        {
            "trechos": [
                "",
                ""
            ],
            "explicacao": ""
        }
    ],
	"fluxo-processo":[
		{
			"simbolo":"",
			"nome-etapa":"",
			"descricao-etapa":""
		},
	],
}




2. Esse arquivo chamado `resumo.json`, deve conter os seguintes campos:
   2.1 "resumo":
   	2.1.1 Um texto simples que organize os assuntos tratados na conversa, destacando o **tema central** da reunião com 350 palavras
	2.1.2 Não precisa destacar que foi uma reunião, conversa, debate ou relatório, apenas escreva o resumo de forma impessoal, como se estivesse contando uma história
	2.1.3 Separe os paragrafos com a tag <p> de acordo com o assunto, não quebre os parágrafos no meio das frases
	2.1.4 O texto precisa trazer riquesa de detalhes e tratar todos os temas discutidos, mas de forma resumida cada um deles
	2.1.5 As vezes você retorna texto repetido no final do resumo. Nunca faça isso!

   2.2 "problema_central":
	2.2.1 Em uma frase, descreva o problema central que o texto trata

   2.3 "necessidades":
	2.3.1 Retorne um lista com no mínimo 7 dos problemas discutidos ao longo da conversa, uma frase curta no campo "necessidade"
	2.3.2 Podem ser problemas intermediários que resultam no problema_central
	2.3.3 Podem ser, também, requisitos do cliente (fazendo analogia com análise QFD)
	2.3.4 identifique SOMENTE as causas raízes dos problemas discutidos
	2.4.4.1 Para cada frase curta de necessidade, traga outro campo chamado "desc_necessidade" com um texto claro e detalhado explicando a necessidade. Se for o caso, traga citações para contextualizar
	2.3.5 CRITÉRIOS PARA IDENTIFICAÇÃO:
	2.3.5.1 Problemas são situações que impedem, bloqueiam ou geram impacto negativo
	2.3.5.2 Causas raízes são os fatores fundamentais que originam esses problemas
	2.3.5.3 Ignore: requisitos, pedidos, sugestões, melhorias ou funcionalidades desejadas
	2.3.5.4 foque em: Não está funcionando..., O sistema falha quando..., Os usuários não conseguem..., Está causando...
	2.3.5.5 problema não começa com um verbo de ação, ignore qualquer frase que contenha ações a serem executadas


   2.4 "requisitos_tecnicos":
	2.4.1 Quero que você identifique apenas os pedidos, requisitos, solicitações ou desejos mencionados pelas pessoas, no mínimo 7
	2.4.2 Normalmente se confundem com as necessidades, busque separar bem o que é um requisito de uma necessidade
	2.4.3 Podem ser, também, requisitos técnicos (fazendo analogia com análise QFD)
	2.4.4 Não inclua necessidades, dificuldades ou problemas relatados — apenas as ações, recursos ou soluções pedidas
	2.4.5 Liste cada pedido de forma clara, em frases curtas, separadas por tópicos no campo "requisito"
	2.4.5.1 Para cada frase curta de requisito, traga outro campo chamado "desc_requisito" com um texto claro e detalhado explicando o requisito

   2.5 "insights":
	2.5.1 Retorne um lista com insights que não foram discutidos na conversa
	2.5.2 Você é um analista de estratégia.
	2.5.3 Gerar ideias acionáveis sobre o problema_central
	2.5.4 Sem elogios, sem coaching motivacional, sem enfeite. Diga na lata
	2.5.5 Não saia do tema: se algo estiver fora de problema_central, ignore.
	2.5.6 Entregue valor rápido: ideias curtas, claras, com porquês mínimos.
	2.5.7 Profundidade leve: rascunhos de linhas de raciocínio, não tratados completos.
	2.5.8 Aponte riscos/armadilhas quando aplicável.
	2.5.9 Nada de generalidades vazias (ex.: “inovar”, “melhorar comunicação”) sem um como. 

   2.6 "sentimentos":
	2.6.1 Retorne uma pontuação na escala de -1 a 1 (sendo 0 neutro), irei exemplificar a escala ao lado dos 4 sentimentos identificados nos textos:
		2.6.1.1 Confiança: (-1 se total desconfiança e 1 se muita confiança)
		2.6.1.2 Entusiasmo: (-1 se total tristeza e 1 se muito entusiasmo)
		2.6.1.3 Colaboração: (-1 se total rivalidade e 1 se extrema colaboração) 
		2.6.1.4 Satisfação: (-1 se total insatisfação e 1 se total satisfação)

   2.7 "bibliografia":
	2.7.1  Liste algumas bibliografias (livros/artigos/autores) relevante ao tema central do problema a ser tratado, sem resumos longos.
	2.7.2 Use o contexto apresentado para ser mais assertivo na recomendação

   2.8 "markdown":
	2.8.1 Você é um analista responsável por organizar uma reunião em um mapa mental detalhado, no formato **Markdown**. Gere um **mapa mental no formato Markdown**, identificando:
   	2.8.1.1 Inicie destacando o Macro tema da Conversa
   	2.8.1.1.1 No próximo nível liste todos o problemas identificados relacionados ao tema
   	2.8.1.1.1.1 Para cada problema, liste as possíveis causas raiz discutidas (pode ser mais de uma por problema)
   	2.8.1.1.1.2 Para cada problema, liste também possíveis soluções discutidas (pode ser mais de uma por problema)
   	2.8.1.1.1.2.1 Para cada soluções indique (se houver) um responsável que irá tratar
   	2.8.1.1.1.2.1 Para cada soluções indique também (se houver) a data da tratativa
	2.8.1.1.1.3 Para cada problema, liste um nível abaixo com **insights, sugestões ou ideias mencionadas para solução**
	2.8.1.1.1.4 Para cada problema, mostre os números falados e relacionados a ele
	2.8.1.3 Organize hierarquicamente, com **máxima riqueza de detalhes**
	2.8.1.4 Utlize vários níveis para abrir com clareza o raciocínio
	2.8.1.5 Quero usar essa estrutura para identificar causa raíz dos problemas discutidos
	2.8.1.6 **Não resuma**, apenas reorganize com clareza
	2.8.1.7 **Não inclua introdução, conclusão ou explicações**
	2.8.1.8 Não invente nada, não insira nenhuma palavra ou termo que não tenha sido falado
	2.8.2 Não insira "```" no inicio e no final do Markdown
	2.8.3 Detalhe o markdown vários nós
	
	
   
   2.9 "quando":
	2.9.1 Data e hora da criação do arquivo
	2.9.2 Use fuso horário do Brasil São Paulo

   
   2.10 "timeline":
	2.10.1 Divida o texto em 5 partes e retorne o assunto principal tratado em cada parte
	2.10.2 Retorne neste campo do json 5 campos dentro dele:
	2.10.2.1 Parte 1: Frase com principal tema tratado na primeira parte da conversa
	2.10.2.1 Parte 2: Frase com principal tema tratado na segunda parte da conversa
	2.10.2.1 Parte 3: Frase com principal tema tratado na terceira parte da conversa
	2.10.2.1 Parte 4: Frase com principal tema tratado na quarta parte da conversa
	2.10.2.1 Parte 5: Frase com principal tema tratado na quinta parte da conversa


   2.11 "reuniao_em_numeros":
	2.11.1 Identifique qualquer valor numérico contido na transcrição ou na anotação
	2.11.2 Liste nesse campo todos esses valores com uma frase explicando eles

   2.12 "perguntas_sem_respostas":
	2.12.1 Identifique toda questão levantada que não teve uma definição clara
	2.12.2 Liste nesse campo essas questões, pode ser mais do que uma frase, pode ser um pequeno texto para contextualizar cada uma delas
	
   2.13 "contradicoes":
	2.13.1 Encontre contradições em todos os textos e apresente como uma lista
	2.13.2 crie um campo "trechos" com uma lista, informando os trechos que se contradizem
	2.13.3 crie um campo "explicacao" explicando as contradições
	
   2.14 "fluxo-processo":
	2.14.1 Identifique na conversa etapas de um fluxo para que se possa organizar em um fluxograma descritivo
	2.14.2 Para cada etapa desse fluxo, preencha os campos:
	2.14.2.1 "simbolo": identifique o tipo de etapa e encaixe nos padrões:
	2.14.2.1.1 "Ovais": Se for o inicio ou o final do fluxo, geralmente a primeira e a última etapa
	2.14.2.1.2 "Retangulo": Se for uma ação ou tarefa específica no fluxo
	2.14.2.1.3 "Losango": Se for uma pergunta ou uma decisão, irá determinar qual caminho o fluxo irá seguir. Deve ser uma pergunta que seja possível responder com sim ou não
	2.14.2.1.4 "Paralelogramo": Se for uma entrada de dados ou saída de resultados
	2.14.2 Logo após um [Retangulo] deve existir duas novas etapas, um no caso ser resposta positiva ou negativa. Elas podem começar com os caracteres: "Se sim..." ou "Se não..."

 
3. Se as informações estiverem em ingles traduzir todas as saídas para portugues
4. Gere o arquivo resumo.json COMPLETO, sem interrupções ou parar na metade
5. Não é para gerar apenas a estrutura, deve preencher conforme as orientações passadas acima

6. Criar o arquivo html
6.1 Depois disso leia o arquivo [base.html]
6.2 Faça uma cópia e chame ele de [Assessment.html] salvando na mesma pasta do projeto
6.3 Dentro de 'Assessment.html' busque o texto '##INSIRA_CONTEUDO_JSON##' e substitua pelo conteúdo de texto do [resumo.json].
6.3.1 Observe que [Assessment.html] já possui {} do jason, cuide isso para não dar erro.
6.4 Salve [Assessment.html]
7. Não gere nenhum arquivo adicional além do [resumo.json] e do [Assessment.html]

