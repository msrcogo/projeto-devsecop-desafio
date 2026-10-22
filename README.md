# Desafio DevSecOps — Gerenciador de Tarefas

## Sobre o Projeto
Este repositório faz parte do desafio prático do módulo de DevSecOps da ADA Tech.
Você receberá este projeto com vulnerabilidades propositais e uma pipeline incompleta.
Seu objetivo é **implementar a pipeline de segurança** e **corrigir as vulnerabilidades**.

## Estado atual
A pipeline está **incompleta**. Os steps de segurança precisam ser implementados por você.

## Sua missão
1. Implementar os steps de segurança no `pipeline.yml`
2. Fazer a pipeline **quebrar** ao detectar os problemas
3. Corrigir as vulnerabilidades encontradas
4. Fazer a pipeline **passar** com tudo verde ✅
5. Documentar o funcionamento da pipeline neste README

## O que implementar
- [ ] Secrets Scanning com **Gitleaks**
- [ ] SAST com **Semgrep**
- [ ] SCA com **Grype**
- [ ] Assinatura do artefato com cosign
- [ ] Deploy com **GitHub Pages**

## Como a pipeline funciona
Em DevSecOps, a segurança é incorporada ao processo de desenvolvimento desde a etapa de planejamento até a produção. Ela ocorre de maneira integrada e automatizada em cada etapa, exprimindo uma cultura de responsabilidade compartilhada, com processos automatizados no CI/CD, priorizando a Shif-Left Security. 
Desse modo, sempre que uma nova versão do código é enviada para o repositório principal, uma série de verificações é executada automaticamente. Essas verificações analisam o código, as bibliotecas utilizadas e a aplicação em funcionamento, com o objetivo de identificar problemas antes da publicação. Caso alguma verificação encontre uma falha, o processo é interrompido e a nova versão não é disponibilizada. Logo, apenas versões que atendem aos critérios definidos de qualidade e segurança podem chegar ao ambiente de produção.
As atividades realizadas, na configuração inicial, foram:
Criação de uma cópia do repositório proposto no enuciado do Projeto no GitHub;  
Configuração do ambiente de desenvolvimento com o usuário da aluna; 
Utilização da branch principal para execução da pipeline, após tentativa inicial de utilização de outro branch;
Configuração de etapas automatizadas na implementação da pipeline, com identificação e correção dos problemas a seguir identificados.
1. Remoção da linha 50 da pipeline.yml;
2. Implementação das ferramentas Gitleak, Semgrep e Grype Steps;
3. Corrigida a falha env;
4. Corrigida yaml syntax no Grype e Cosign;
5. Removido eval ( ) para prevenir SQL injection no script.js;
6. Atualização de vulnerable dependencies (lodash, axios, express);
7. Update download - artifact action (versão corrigida);
8. Habilitação de Cosign Signature antes do Deploy;
9. Remoção de hardcoded API key e senha de banco de dados;
10. Prevenção de ataque XSS com a substituição de innerHTML por textContent;
11. Prevenção de exposição do usuário a err stack trace e
O projeto demonstrou a importância da automação de verificações de segurança durante o desenvolvimento. Ao incorporar essas validações ao fluxo de entrega, é possível identificar problemas mais cedo, reduzir riscos e aumentar a confiabilidade das aplicações disponibilizadas aos usuários.

## URL de Produção
>https://msrcogo.github.io/projeto-devsecop-desafio/