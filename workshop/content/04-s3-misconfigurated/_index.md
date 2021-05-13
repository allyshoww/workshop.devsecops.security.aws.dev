---
title: Será que falta configuração no S3?
date: 2021-04-27T12:20:58+01:00
weight: 6
pre: <b>4. </b>
---

## Introdução
Neste módulo, como parte da governança de segurança, todos os buckets s3 devem ter a configuração de versionamento s3 ativada. Essa política ajuda as organizações a se recuperarem da exclusão ou alterações de dados, mantendo cópias de versões anteriores. Como engenheiro de segurança, você deseja habilitar o pipeline para impor a habilitação da configuração de versionamento do bucket s3.

{{% notice tip %}}
S3 é um dos principais serviços da AWS e é muito utilizado pelos clientes. Ele é responsável por armazenamento de objetos. 
{{% /notice %}}

### Configurando o Lambda para verificar modelos do AWS Cloudformation quanto às configurações do s3;


* Navegue até o console do Lambda e crie uma nova função a partir do zero;
* Certifique-se de selecionar o runtime do Python 3.8 e selecionar a role “{ * }-PipelineRole-{ * }“;
* Nomeie a função à sua escolha e crie a função;
* Defina o tempo do Lambda para 1 minuto;
* cfn_s3_versioning.py é fornecido no workshop. Abra isso no seu editor favorito;
* Cole o conteúdo do editor de código-fonte cfn_s3_versioning.py (aquele no console do Lambda), substituindo a função de espaço reservado inicial;
* Navegue de volta ao Console do CodePipeline e abra seu pipeline DevSecops novamente;
* Edite o pipeline usando o botão no canto superior direito
![Edit-Pipeline](../images/03-Edit-Pipeline.png)
* Use o botão Editar estágio para o estágio StaticCodeAnalysis;
* Selecione o ícone Editar para a função CFNParsing;
* Copie o conteúdo de “Parâmetros do usuário (opcional)” para o buffer de pasta. Feche o pop-up Editar ação.
![Edit-Pipeline](../images/03-Edit-Pipeline.png)

### Crie um nome para sua ação verificação de versionamento de bucket S3, escolha o AWS Lambda no menu suspenso(dropdown) Provedor de ações.”;
* Selecione “Adicionar grupo de ações”;
* Crie um nome para sua ação de varredura de chaves, escolha o AWS Lambda no menu suspenso(dropdown) Provedor de ações.
* Em “Nome da função”, selecione o nome que você deu à sua função Lambda na Etapa 2 acima.
* TemplateSource no menu suspenso “Artefatos de entrada”.
* Cole o conteúdo do buffer de pasta de cima em “Parâmetros do usuário (opcional)”
* Selecione Salvar o pipeline recém-editado. Você deve marcar a opção “Nenhuma atualização de recursos necessária para esta alteração de ação de origem” na janela pop-up salvar pipeline.
* Sua nova função do Lambda agora está integrada ao seu pipeline.
* Prossiga para o próximo módulo para testar sua função do Lambda.

{{% notice tip %}}
Que outras coisas você pode procurar em um modelo do AWS Cloudformation que você pode criar uma automação de segurança?
{{% /notice %}}