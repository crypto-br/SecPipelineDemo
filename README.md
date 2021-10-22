# SecPipelineDemo

DevWeek Datum TI : Aplicando segurança em DevOps <br>
Demonstrando como aplicar ferramentas de segurança Open Source em um pipeline <br>

* GitHub Actions (para montar o workflow de demonstração)
* [Trivy](https://github.com/aquasecurity/trivy) (Para realizar analise da imgem Docker)
  * Para quebra automatica do pipeline, utilizar a opção "exit-code: '1'" no arquivo [main.yml](https://github.com/crypto-br/SecPipelineDemo/blob/main/.github/workflows/main.yml) do actions
  * ```sh
    exit-code: '1'
    ```
* [HoruSec](https://horusec.io/site/) (para análise SAST)
  * Para quebra automatica do pipeline, utilizar a opção  -e="true" na linha de comando do horusec no arquivo [main.yml](https://github.com/crypto-br/SecPipelineDemo/blob/main/.github/workflows/main.yml) do actions:
  * ```sh
    $ horusec start -p="./" -e="true"
    ```
* [OWASP ZAP](https://github.com/zaproxy/zaproxy/) (para análise DAST)

## Resultado da pipeline de demonstração

![Resultado da pipeline do LAB](https://github.com/crypto-br/SecPipelineDemo/blob/main/resultpipeline.jpg)

* [Apresentação em PDF](https://github.com/crypto-br/SecPipelineDemo/blob/main/Apresenta%C3%A7%C3%A3o%20DEV%20WEEK%20PPT.pdf)
