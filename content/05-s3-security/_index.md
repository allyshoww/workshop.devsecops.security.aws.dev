---
title: Segurança no S3
date: 2021-04-27T12:20:58+01:00
weight: 7
pre: <b>5. </b>
---

## Introdução

Muitas organizações utilizam o s3. É importante que os buckets s3 estejam configurados de acordo com os requisitos da organização para garantir que os dados armazenados com segurança.

Agora que você adicionou uma função lambda para impor a habilitação da Configuração de Versionamento do S3. Solte a alteração para iniciar o pipeline.

{{% notice tip %}}
O que é o Versionamento do S3? Como isso pode ajudá-lo a proteger os dados?
{{% /notice %}}

* Adicione a configuração apropriada.
* Edite resource.json e adicione as linhas apropriadas.
* Rezip o “codepipe-AWS-devsecops.zip” (o nome exato é importante)
* Carregue o zip para s3.
* Volte para o pipeline DevSecops e observe-o através dos estágios novamente.

Quer saber mais sobre as propriedades de um bucket s3? [Dá uma olhada nesse link!](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)

{{% notice tip %}}
Existem outras configurações s3 que você gostaria de impor? Existem outras maneiras nativas da AWS de impor alguns desses controles?
{{% /notice %}}