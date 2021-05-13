---
title: Limpeza do ambiente
date: 2019-10-14T12:20:58+01:00
weight: 8
pre: <b>6. </b>
---

Este último módulo ajuda a limpar o ambiente de laboratório. Isso só se aplica se você estiver executando isso em sua própria conta. Caso você esteja utilizando uma conta gerada pela AWS, essa conta e os recursos serão automaticamente deletados.

## Limpeza

Para evitar cobranças na sua conta, recomendamos limpar a infraestrutura criada. Se você planeja manter as coisas funcionando para que você possa examinar o workshop um pouco mais, por favor, lembre-se de fazer a limpeza quando terminar. É muito fácil deixar as coisas em execução em uma conta da AWS, esquecê-lo e, em seguida, ser cobrado por isso.

Se você estiver usando isso em uma sessão conduzida por instrutor, com o AWS Event Engine você não precisará executar as etapas de limpeza

Se você estiver executando isso em sua própria conta. Você precisará excluir manualmente alguns recursos antes de excluir as pilhas do CloudFormation, portanto, faça as seguintes etapas em ordem.

### Excluir buckets s3.

* Acesse o console do Amazon S3;
* Vá para o bucket s3 que você criou no módulo 1 e exclua todo o conteúdo.
* Depois que o bucket estiver vazio, exclua o bucket.
* Procure por artifactstorebucket e exclua todo o conteúdo. Você terá que clicar no botão “Mostrar” para mostrar todas as versões de arquivos. 
* As versões dos arquivos também precisam ser excluídas antes que o bucket possa ser excluído.

### Exclua a stack do Cloudformation.
* Acesse o console do AWS Cloudformation.
* Procure a pilha distribuída no módulo 1 e delete a pilha.

#### Excluir Lambdas.
* Acesse o console do AWS Lambda.
* Exclua as funções lambda que você criou.

**Parabéns!**

Parabéns por concluir este workshop! Esse workshop ficará ativo, então sinta-se livre para revisitar quantas vezes quiser.