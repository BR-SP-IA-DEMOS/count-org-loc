# count-org-loc

## Descrição
Count total lines of code across a GitHub organization

## Stack Tecnológica
- Linguagem: Ruby

## Pré-requisitos
- Ruby 3.0+
- Cloc (ferramenta de contagem de linhas de código)

## Como Rodar
```bash
['git clone https://github.com/benbalter/count-org-loc && cd count-org-loc', 'gem install bundler', 'script/bootstrap', 'script/count [ORG_NAME | USER_NAME]']
```

## Estrutura do Projeto
```
{'script': {'bootstrap': 'Script de inicialização', 'count': 'Script principal de contagem de linhas de código'}, 'Brewfile': 'Arquivo de dependências do Homebrew', 'Gemfile': 'Arquivo de dependências do Ruby', 'LICENSE.md': 'Arquivo de licença', 'README.md': 'Documentação do projeto', 'loc.rb': 'Arquivo principal do script de contagem de linhas de código'}
```

## Variáveis de Ambiente
- `GITHUB_TOKEN - Token de acesso pessoal do GitHub para acessar repositórios privados`
- `GITHUB_ENTERPRISE_URL - URL da API do GitHub Enterprise, se aplicável`

## Endpoints/Funcionalidades Principais
- script/count [ORG_NAME | USER_NAME] - Conta o total de linhas de código da organização ou usuário especificado

## Testes
```bash
Não identificado
```

## Status do Projeto
✅ Em produção

_O projeto parece estar ativo e sendo utilizado pela comunidade_

## Problemas Conhecidos
- Não é possível contar linhas de código de repositórios privados sem fornecer um token de acesso pessoal do GitHub

## Autores/Contato
Não identificado

---
*Documentação gerada automaticamente com Claude AI em 2026-01-21 16:28*
