## O que aprendi
- Defensive security = monitorizar e proteger sistemas
  (ao contrário de offensive, não atacas — detectas e respondes)
- Fluxo de um analista SOC: detectar → investigar → conter

## Passo a passo do cenário
1. Dashboard de monitorização mostrou actividade suspeita
2. Identifiquei o IP de origem suspeito: 32.122.195.63
3. Investiguei "URL Discovery Attempts" — o atacante tentava
   aceder a https://fakebank.com/admin
4. Containment: bloqueei o IP através de uma regra de firewall
   (dropdown → BLOCK → Apply)
5. Flag: THM{FAKEBANK-SECURED}

## Conceitos chave
- SOC (Security Operations Center) = equipa que monitoriza sistemas
- Containment = ação imediata para parar um ataque em curso,
  antes de investigar a fundo
- O mesmo IP que tentou aceder a /admin (offensive room) 
  é o que é detectado e bloqueado aqui — perspectivas
  complementares do mesmo ataque

## Para rever
- Diferença entre detection, investigation e containment
- Regras de firewall — sintaxe básica
