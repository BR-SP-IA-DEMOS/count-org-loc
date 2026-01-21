# Count total lines of code across a GitHub organization

## Usage

1. `git clone https://github.com/benbalter/count-org-loc && cd count-org-loc`
2. `gem install bundler`
3. `script/bootstrap`
4. `script/count [ORG_NAME | USER_NAME]`

## Usage via GitHub Actions

Don't want to set up a local development environment? You can run this script via GitHub Actions:

1. Fork this repository into your account
2. Navigate to the "Actions" tab of your fork
3. Click the "run" workflow on the left side
4. Click "Run workflow" on the right side
5. Enter your org. or user name that you'd like to count lines of code for
6. Click "Run Workflow"

You'll see the progress and count(s) in the job output (also available from the Actions tab).

Note: If you'd like to count private repositories, as described below, you'll need to set an `ORG_GITHUB_TOKEN` GitHub Actions secret with your PAT.

## How it works

It uses [Octokit.rb](https://github.com/octokit/octokit.rb) to fetch a list of your organization's (or user's) repositories (public or public and private), clone each, and [Cloc](https://github.com/AlDanial/cloc) to count the lines of code, number of files, comments, etc.

## Example output - 24/07/2025

```
-----------------------------------------------------------------------------------
Language                         files          blank        comment           code
-----------------------------------------------------------------------------------
Python                           21874        1362380        2048282        5205392
CSV                                256           2450              0        1172384
HTML                               152          36391            630         173096
Text                               696           8029              0         148509
JSON                               131            145              0         147312
C/C++ Header                       739          59956         138729         137987
Cython                             424          30540          29085         133412
C                                  171           7429          31220         102352
Jupyter Notebook                   131              0         662390          43013
C++                                 48           3049           3401          17783
Markdown                           198           5285             56          14270
JavaScript                         154           1829            745          14058
XML                               1308             11           1347          12345
YAML                               182           1146            596           9966
HCL                                 74            579            322           5624
CUDA                                 2            427           1629           5167
XSLT                                17           1236           2288           4766
CSS                                 58            775            261           4559
SQL                                 13              2              4           4202
TypeScript                         111            524             69           3800
Protocol Buffers                   124           1784          11568           3224
Fortran 90                         173            384            278           2890
TOML                                20            159            388           2231
Meson                               56            281            319           2123
JSX                                  8            226             36           1869
reStructuredText                    45            729            809           1868
Bourne Shell                        37            264            150           1251
Fortran 77                          70             78            150           1167
PowerShell                          12            312           1223            810
Dockerfile                          41            327            224            537
Windows Resource File                3            105            135            405
SVG                                 57              1              1            319
DOS Batch                           15             88             12            263
Assembly                             4             60             28            240
ASP                                 15             66              0            204
Fish Shell                           4             58             56            196
IDL                                  3             12              0            186
INI                                 14             22              1            150
Visual Basic Script                  9             21             12             93
C Shell                              4             43             22             71
Nushell                              1             14             13             69
PO File                              1              5             10             32
Fortran 95                           3              0              3             12
Unity-Prefab                         2              0              0              4
make                                 1              0              0              4
-----------------------------------------------------------------------------------
SUM:                             27461        1527222        2936492        7380215
-----------------------------------------------------------------------------------


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
File                                                                                                                             files          blank        comment           code
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Ignite_IA_2024_AN-LISE_JURIDICA                                                                                                  12660         785781        1214030        3090087
document_intelligence-app                                                                                                         6014         334271         453425        1454560
document_intelligence-function                                                                                                    4959         340434         577314        1296221
analise-banrisul                                                                                                                    83           2791         151532        1003475
RPA_RH_Senior                                                                                                                        7          32764           1166         148246
signature-detection-yolo                                                                                                          1496             32           1791          39932
document-intelligence-app                                                                                                           66            537             95          24419
febraban-2025-juridico-frontend                                                                                                     63            449             84          23450
oec_react_frontend                                                                                                                  27            328             95          21895
Analise_ITSM                                                                                                                        18              0         286215          20178
febraban-2025-ask-docs-frontend                                                                                                     19            105             30          19771
febraban-2025-bot-maker-frontend                                                                                                    22            132             45          19054
curriculo-avaliacao-front                                                                                                           21            116             32          18945
signature-detection-bb                                                                                                             135           3237           4862          18521
yoga-game                                                                                                                           77           2780           3541          14595
mysupport                                                                                                                           31            353            722          13297
febraban-jornada-3                                                                                                                  14             89             81           9958
classificacaomm                                                                                                                     28            621           1274           8906
demoapp-pdf-gpt-NAO-USAR                                                                                                           107            731            329           8329
febraban-2025-validacao-docs                                                                                                       142           1614           2180           7773
demoapp--openai                                                                                                                    109            772            270           7425
nova_demo_caixa_ago23                                                                                                              104            672            496           7170
ia-for-cys                                                                                                                          26            102              2           6837
Google-RAG-Demo                                                                                                                     53            976          44714           6052
ESG-Relatorios-e-Anotacoes                                                                                                          67            286              0           5559
PeD_GoogleGenAI                                                                                                                     64            926           2859           4866
Ignite_IA_2024_VC_DWP                                                                                                                7            120             72           4612
curadoria-rag                                                                                                                       63            936          10276           4522
document-Intelligence-backend                                                                                                       33           1171           1240           3670
AutoPrompt                                                                                                                          31            373           5080           3621
poc-atvos                                                                                                                           22             17          58027           3291
Evaluating_Embeddings_Models                                                                                                        13            213           8443           3065
bot-maker-backend                                                                                                                   39            601          27624           2870
febraban-2025-juridico-backend                                                                                                      31            993           1115           2844
CVP                                                                                                                                 33            365            339           2774
https-github.com-Rafael-CostaF-document_intelligence-terraform                                                                      34            284            135           2611
document_preprocessing_indexing                                                                                                     20            343          24515           2566
banrisul-genai-poc                                                                                                                  23            561            506           2531
febraban-2025-ask-docs-backend                                                                                                      33            702            836           2408
edp-gestao-compartilhantes                                                                                                          21            408           8496           2284
image-manipulation-demo                                                                                                             16            467            951           2096
demo-image-manipulation-mantranet                                                                                                   25            333           1193           2076
Visual-Inspector                                                                                                                    19            580            552           1979
linkedin-rh-ranking                                                                                                                 34            277           1370           1911
cef_estudo_previo                                                                                                                    4              7           8722           1664
analisejuridicobackend                                                                                                              23            479            524           1383
CVP-IAC                                                                                                                             34            249            114           1375
oec_react_backend                                                                                                                   25            335            324           1313
RAG-Padrao-Ouro                                                                                                                     17            399            467           1282
repo-whl                                                                                                                            15            405             41           1196
analise_documentos                                                                                                                   8            188            282           1146
podnewsgenai                                                                                                                        27            282            281            981
multi-agents-call                                                                                                                   34            266            201            965
febraban-2025-analise-audio                                                                                                         17            131            135            955
CPV-APP                                                                                                                             16            251            202            928
ABI-Refactor                                                                                                                        12            221            400            922
oec_streamlit_rag                                                                                                                   16            259            395            918
signature_recognition                                                                                                               14            252            225            855
hallucinationshield                                                                                                                 16            300           4811            838
newssynth                                                                                                                           16            218            166            802
Pandas_Dataframe-Text-to-SQL                                                                                                         8            232            356            739
promptinjectiontshield                                                                                                              14            239            201            729
time_series_nixtla                                                                                                                   2              6          10677            727
Copel_treinamento_h2o                                                                                                                3              5           6457            702
LLMOPS-GCP-Finetuning-Flow                                                                                                          18            107             57            621
Ignite_IA_2024_ANALISE_LIGACOES                                                                                                      2            238             73            591
RAG_neo4j                                                                                                                           12            199             85            576
febraban-analise-contrato                                                                                                            7            186            508            548
Ignite_IA_2024_Chatbot_Inteligente_text_to_SQL                                                                                      13            203            230            510
genaisecutiry                                                                                                                       18            165             54            476
video-transcript                                                                                                                    10            175             49            435
simple-rag                                                                                                                          17            178             32            429
secgenaiappdemo                                                                                                                      9             83             36            428
ai-workflows                                                                                                                         6             93              0            403
curriculo-avaliacao-back                                                                                                             7             69            504            357
Ticket_Quality                                                                                                                       9            151            210            332
pandasagent                                                                                                                         14            104             70            286
classificacao-inteligente-imagens                                                                                                    5             54            953            269
LLM_Integrator                                                                                                                       3            133            192            265
Ignite_IA_2024_DocMentor_RAG_COMMAND_CENTER                                                                                          4            104             62            247
code_tester                                                                                                                          4             50             27            217
cemig-video-analytics                                                                                                                5             62             41            209
ESG-WebService                                                                                                                      12             49             15            196
full-project-oec                                                                                                                     4             83             10            175
extracao-de-indicadores-esg                                                                                                          3             73            206            174
apishieldai                                                                                                                         11             72             37            170
shieldgenai                                                                                                                          5             59             50            146
help-desk-neo4j                                                                                                                      7             62             23            127
ai-workflows-tester                                                                                                                  6             26              0             92
pipeline-pre-processamento-ocr                                                                                                       1             17              0             72
ollama-hub                                                                                                                           4             32             19             71
cvx-application-demo                                                                                                                 5             13             14             58
sonarqube-container                                                                                                                  2              2              0             35
analise-contrato-juridico                                                                                                            1             12              0             14
Dados_energia_POA                                                                                                                    2              0              0              5
aws-genai-workshop                                                                                                                   1              0              0              2
hub-ai-blue-force                                                                                                                    1              0              0              2
segmentacao-e-medicao-de-tamanhos-de-objetos                                                                                         1              1              0              2
signature-detection                                                                                                                  1              0              0              2
cvx-framework                                                                                                                        1              0              0              1
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
SUM:                                                                                                                             27461        1527222        2936492        7380215
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
```

## Counting private repositories

To look at private repositories, you'll need to pass a [personal access token](https://github.com/settings/tokens/new) with `repo` scope as `GITHUB_TOKEN`. You can do this by adding `GITHUB_TOKEN=[TOKEN]` to a `.env` file in the repository's root.

If you are working with GitHub Enterprise and want to change your URL, simply add `GITHUB_ENTERPRISE_URL=https://<ghe-url>/api/v3` to the `.env` file


Sample `.env` File :

```bash
GITHUB_TOKEN="<token>"
GITHUB_ENTERPRISE_URL="https://my-ghe.local/api/v3"
```
