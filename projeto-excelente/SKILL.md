---
name: projeto-excelente
description: Use quando o usuário pedir para criar um projeto novo, revisar um projeto existente ou melhorar um projeto (código, site, app, automação, documento ou produto). Planeja, constrói, audita e refina até o melhor resultado possível, sempre que for solicitado.
---

# Projeto Excelente

Skill para criar, revisar e melhorar projetos com o mais alto nível de qualidade. Ela funciona em três modos. Escolha o modo pelo que o usuário pediu e, se o pedido misturar modos, execute na ordem: criar, revisar, melhorar.

## Princípios

- **Qualidade acima de velocidade.** Entregue algo que o usuário possa usar de verdade, não um esqueleto.
- **Entenda antes de construir.** Descubra objetivo, público, restrições e o que é "sucesso" para o usuário.
- **Simples primeiro.** Prefira a solução mais simples que resolve o problema. Complexidade só entra quando se paga.
- **Tudo verificável.** Rode, teste e confira o que você produziu antes de dizer que está pronto.
- **Fale a língua do usuário.** Responda em português do Brasil, a menos que ele escreva em outro idioma. Nomes de código e arquivos seguem a convenção do ecossistema.
- **Honestidade.** Diga claramente o que não foi feito, o que é suposição e o que ainda tem risco.

## Modo 1: Criar um projeto

1. **Alinhar o escopo.** Se o pedido for vago, faça no máximo 3 perguntas objetivas (objetivo, público, tecnologia preferida). Se o usuário já deu contexto suficiente, não pergunte: assuma o caminho mais razoável e diga qual foi.
2. **Planejar.** Defina em poucas linhas: o que será entregue, a stack escolhida (e por quê), a estrutura de pastas e os marcos principais.
3. **Construir em etapas.** Comece pelo núcleo que entrega valor, depois acrescente o resto. Mantenha o projeto funcionando a cada etapa.
4. **Incluir o essencial de um bom projeto:**
   - `README.md` com: o que é, como instalar, como usar, exemplos e como contribuir.
   - Estrutura de pastas clara e nomes consistentes.
   - Tratamento de erros e validação de entradas nos pontos de risco.
   - Configuração fora do código (variáveis de ambiente, `.env.example`), nunca segredos versionados.
   - `.gitignore` adequado à stack.
   - Testes para a lógica importante.
   - Licença quando o projeto for público.
5. **Verificar.** Execute o projeto e os testes. Corrija o que quebrar antes de entregar.
6. **Entregar.** Resuma em poucas linhas o que foi criado, como rodar e qual é o próximo passo natural.

## Modo 2: Revisar um projeto

Leia o projeto inteiro antes de opinar: estrutura, arquivos principais, dependências, README e testes. Avalie cada dimensão abaixo e dê nota de 0 a 10 com uma justificativa curta:

| Dimensão | O que olhar |
|---|---|
| Funcionalidade | Faz o que promete? Casos de borda tratados? |
| Código/Conteúdo | Clareza, duplicação, nomes, organização, complexidade desnecessária |
| Arquitetura | Separação de responsabilidades, acoplamento, facilidade de evoluir |
| Segurança | Segredos expostos, entradas não validadas, dependências vulneráveis |
| Desempenho | Gargalos óbvios, consultas ou laços ineficientes |
| Testes | Cobertura do que importa, testes confiáveis |
| Documentação | README, comentários úteis, exemplos, instruções de instalação |
| Experiência de uso | Interface, mensagens de erro, acessibilidade, facilidade de começar |
| Manutenção | Dependências atualizadas, padronização, automações (lint, CI) |

Formato da revisão:

1. **Resumo em 2 a 3 frases:** o estado geral e o maior ponto forte.
2. **Notas por dimensão.**
3. **Problemas encontrados**, ordenados por prioridade:
   - **Crítico:** quebra, perde dados ou expõe segurança.
   - **Importante:** prejudica qualidade ou manutenção.
   - **Melhoria:** polimento e boas práticas.
4. **Plano de ação:** os 3 a 5 passos que mais elevam a qualidade.

Cite arquivo e linha quando possível. Não invente problemas: se algo está bom, diga que está bom.

## Modo 3: Melhorar um projeto

1. **Partir de uma revisão.** Se ainda não houve revisão nesta conversa, faça uma rápida (Modo 2) para saber onde agir.
2. **Priorizar por impacto.** Corrija primeiro o que é crítico, depois o importante e por fim o polimento.
3. **Mudar com cuidado.** Faça alterações pequenas e coerentes. Não reescreva o que funciona sem motivo. Preserve o comportamento existente, a menos que o usuário peça mudança.
4. **Verificar a cada rodada.** Rode testes e o projeto depois de mudar. Se algo regredir, desfaça ou corrija.
5. **Relatar o antes e o depois.** Liste o que mudou e por quê, em poucas linhas.
6. **Repetir.** Se o usuário pedir "melhore mais", faça nova rodada de revisão e melhoria sobre o resultado atual, buscando ganhos reais. Pare e avise quando os ganhos adicionais forem marginais.

## Checklist final antes de entregar

- [ ] O projeto roda do zero seguindo o README.
- [ ] Testes passam e cobrem o essencial.
- [ ] Sem segredos, credenciais ou arquivos temporários no repositório.
- [ ] README completo e atualizado.
- [ ] Nomes, estrutura e estilo consistentes.
- [ ] Limitações conhecidas e próximos passos anotados.

## Quando o projeto vai para o GitHub

- Confira o `.gitignore` e remova qualquer segredo antes do commit.
- Escreva mensagens de commit claras, em português do Brasil, explicando o que mudou e por quê.
- Faça commits pequenos e com um propósito cada.
- Confirme com o usuário o repositório de destino antes de enviar.
