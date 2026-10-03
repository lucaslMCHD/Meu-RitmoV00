# Meu Ritmo

Aplicativo web de acompanhamento fitness em português, feito em HTML, CSS e
JavaScript puros, em um único arquivo, sem dependências nem etapa de build.
Funciona no navegador, pode ser instalado como PWA e convertido em APK.

## Funcionalidades

**Início**
- Saudação com o dia da semana, a data e o treino do dia
- Frase diária de atletas e bodybuilders
- Peso e progressão, com classificação lenta, média ou rápida (peso e carga)
- Nota de desempenho da semana
- Gráficos de calorias, proteína, carboidratos e passos dos últimos 7 dias
- Métrica de descanso entre séries

**Treino**
- Divisão configurável: ABC, ABCD, ABCDE, Push/Pull/Legs, Upper/Lower e Full body
- Planejamento semanal com exercícios, séries, repetições e cargas
- Timer de descanso recomendado por tipo de exercício (composto ou isolado) e por objetivo, com início automático ao concluir uma série
- Botão "Não consegui fazer", que sugere um exercício alternativo do mesmo grupo muscular

**Dieta**
- Metas de calorias, proteína, carboidratos, gorduras e água calculadas pelo perfil
- Cadastro de refeições por quantidade (g, kg ou unidade), com cálculo automático de calorias e macros a partir de uma base de alimentos comuns
- Contador de scoops de whey e creatina, com o quanto falta para a meta de proteína

**Corpo**
- Peso e medidas
- Desempenho: passos, calorias queimadas, volume, tempo e intensidade
- Metas: cálculo do gasto diário (TDEE) e do superávit ou déficit para hipertrofia, perda de peso ou manutenção, com meta de calorias editável
- Progresso: calendário mensal selecionável, comparação entre meta prescrita e realizado, e classificação do nível de avanço (alto, médio ou baixo)

## Como o nível de avanço é classificado

| Nível | Critério |
|-------|----------|
| Alto  | Acima de 105% da meta |
| Médio | De 90% a 105% (na meta) |
| Baixo | Abaixo de 90% da meta |

## Como usar

Abra o `index.html` em qualquer navegador. Na primeira vez, informe nome,
sexo, idade, peso, altura, nível de atividade, objetivo e divisão de treino.

## Dados

Os dados ficam salvos no próprio aparelho (`localStorage`), com cópia
automática diária. Há também backup e restauração em arquivo JSON, na aba
Corpo, em Metas. Se limpar os dados do navegador ou desinstalar o app, os
dados locais são perdidos, então faça backups.

## Instalar como app (PWA e APK)

O projeto inclui `manifest.json`, `sw.js` (funcionamento offline) e ícones.
Hospede a pasta em um site com HTTPS (GitHub Pages, por exemplo) e, para gerar
o APK, use o [PWABuilder](https://www.pwabuilder.com).

## Estrutura

    index.html      aplicativo completo (HTML, CSS e JS)
    manifest.json   configuração do PWA
    sw.js           service worker (cache offline)
    icons/          ícones do app

## Observações

- Os valores nutricionais da base de alimentos são aproximados (por 100 g).
- Calorias, macros e metas são estimativas gerais de nutrição esportiva e não
  substituem orientação de nutricionista, médico ou educador físico.
- As fontes (Barlow Condensed e Outfit) vêm do Google Fonts.
