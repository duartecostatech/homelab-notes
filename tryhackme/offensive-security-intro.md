## O que aprendi
- Offensive Security = pensar como atacante para encontrar 
  vulnerabilidades antes dos hackers reais
- Um site pode ter páginas escondidas não linkadas mas acessíveis
- Com acesso a uma página admin não protegida, 
  qualquer pessoa pode manipular dados

## Ferramentas usadas
- dirb → directory enumeration (alternativa: gobuster)

## Comandos
dirb http://fakebank.thm

## O que aconteceu passo a passo
1. Descobri o nº de conta via a aplicação FakeBank (8881)
2. Corri dirb → encontrou /images e /bank-transfer
3. Acedi a /bank-transfer → painel admin sem autenticação
4. Flag obtida: BANK-HACKED

## Como o dirb funciona realmente
- Não descobre pastas "ocultas" — testa uma lista de nomes comuns
- Para cada palavra da lista tenta: http://site.com/palavra
- O servidor responde com código HTTP
  - 200 = existe
  - 404 = não existe
  - 403 = existe mas acesso negado
- A vulnerabilidade não é a pasta existir
  É a pasta existir SEM autenticação

## Conceito chave
Exposição de painel admin sem autenticação = vulnerabilidade crítica
Isto acontece em produção em empresas reais

## Para rever
- Diferença entre dirb e gobuster
- Códigos HTTP: 200, 301, 403, 404
