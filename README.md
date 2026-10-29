<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=header&text=Ian%20M.&fontSize=60&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Desenvolvedor%20de%20Software%20%7C%20ADVPL%20%2F%20TOTVS%20Protheus&descAlignY=60&descSize=18" alt="Header" width="100%"/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=2C9CDB&center=true&vCenter=true&width=600&lines=Ol%C3%A1%2C+eu+sou+o+Ian+%F0%9F%91%8B;Desenvolvedor+ADVPL+%2F+TL%2B;Apaixonado+por+c%C3%B3digo+limpo+e+boas+pr%C3%A1ticas;Sempre+aprendendo+algo+novo+%F0%9F%9A%80" alt="Typing SVG" />

<br/>

<img src="https://komarev.com/ghpvc/?username=Ianm-SP&label=Visitas&color=2c5364&style=for-the-badge" alt="Visitas no perfil"/>
<img src="https://img.shields.io/github/followers/Ianm-SP?label=Seguidores&style=for-the-badge&logo=github&color=203a43" alt="Seguidores"/>

</div>

---

## 👨‍💻 Sobre mim

- 🔭 Trabalho com desenvolvimento e customização no ecossistema **TOTVS Protheus** usando **ADVPL / TL++**
- 🌱 Estudando **boas práticas em ADVPL**, qualidade de código e arquitetura de integrações
- 🔗 Interesse em **APIs REST**, **integrações** e **banco de dados (SQL)**
- 🧹 Defensor de código limpo, legível e fácil de manter
- 📍 São Paulo, Brasil 🇧🇷

---

## 🛠️ Tecnologias e Ferramentas

<div align="center">

<img src="https://img.shields.io/badge/ADVPL-0C9AD6?style=for-the-badge&logo=data:image/svg+xml;base64,&logoColor=white" alt="ADVPL"/>
<img src="https://img.shields.io/badge/TL++-1B5E8C?style=for-the-badge" alt="TL++"/>
<img src="https://img.shields.io/badge/TOTVS%20Protheus-0C9AD6?style=for-the-badge" alt="TOTVS Protheus"/>
<img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white" alt="SQL"/>
<img src="https://img.shields.io/badge/REST%20API-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="REST"/>

<br/><br/>

<img src="https://skillicons.dev/icons?i=git,github,vscode,postgres,mysql,js,html,css,md&theme=dark" alt="Skills"/>

</div>

---

## 📚 Estudos: Boas Práticas em ADVPL (Udemy)

Estou me aprofundando em **boas práticas de desenvolvimento em ADVPL** através de cursos na Udemy.

<div align="center">

<a href="https://www.udemy.com/courses/search/?q=advpl%20boas%20pr%C3%A1ticas">
  <img src="https://img.shields.io/badge/Udemy-Boas%20Pr%C3%A1ticas%20em%20ADVPL-A435F0?style=for-the-badge&logo=udemy&logoColor=white" alt="Udemy - Boas práticas em ADVPL"/>
</a>

</div>

### ✅ O que venho aplicando no dia a dia

| Prática | Por quê |
|---|---|
| **Declarar variáveis com `Local`** | Evita conflitos de escopo e vazamento de memória; evite `Private`/`Public` |
| **Notação húngara** (`cNome`, `nValor`, `dData`, `lOk`, `aLista`, `oObj`) | Deixa o tipo da variável claro na leitura |
| **Prefixar funções de usuário** (`U_`) e padronizar nomes | Evita colisão com funções padrão do Protheus |
| **Usar `#Include` e `#Define`** em vez de valores fixos ("números mágicos") | Facilita manutenção e leitura |
| **Salvar e restaurar áreas** (`GetArea()` / `RestArea()`) | Não "quebra" o posicionamento de tabelas de outras rotinas |
| **Tratamento de erros** (`Begin Sequence`, `TRY/CATCH` em TL++) | Evita falhas silenciosas e facilita o diagnóstico |
| **Evitar `RecLock` desnecessário e sempre `MsUnlock()`** | Previne travamento de registros |
| **Preferir queries com `BeginSQL`/`EndSQL` e `%table:%`** | SQL mais seguro e portável entre bancos |
| **Logar com `FWLogMsg` / `ConOut`** de forma controlada | Rastreabilidade sem poluir o console |
| **Comentar com Protheus.doc** | Documentação padronizada e gerada automaticamente |
| **Fechar áreas de trabalho temporárias** (`dbCloseArea`) | Libera recursos e evita vazamento |

### 💡 Exemplo de código seguindo as boas práticas

```advpl
#Include "TOTVS.CH"

/*/{Protheus.doc} U_BuscaCli
Retorna o nome do cliente a partir do código e da loja.
@type  User Function
@author Ian
@since 28/10/2026
@param cCodigo, character, Código do cliente
@param cLoja, character, Loja do cliente
@return character, Nome do cliente ou vazio se não encontrado
/*/
User Function BuscaCli(cCodigo, cLoja)
    Local aArea   := GetArea()
    Local aAreaA1 := SA1->(GetArea())
    Local cNome   := ""

    Default cCodigo := ""
    Default cLoja   := ""

    DbSelectArea("SA1")
    SA1->(DbSetOrder(1)) // A1_FILIAL + A1_COD + A1_LOJA

    If SA1->(DbSeek(FWxFilial("SA1") + cCodigo + cLoja))
        cNome := AllTrim(SA1->A1_NOME)
    EndIf

    RestArea(aAreaA1)
    RestArea(aArea)
Return cNome
```

---

## 📊 Estatísticas do GitHub

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Ianm-SP&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="Estatísticas do GitHub" height="170"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ianm-SP&layout=compact&theme=tokyonight&hide_border=true" alt="Linguagens mais usadas" height="170"/>

<br/>

<img src="https://streak-stats.demolab.com/?user=Ianm-SP&theme=tokyonight&hide_border=true" alt="Streak do GitHub"/>

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Ianm-SP&theme=tokyo-night&hide_border=true&area=true" alt="Gráfico de atividade" width="100%"/>

</div>

---

## 🏆 Troféus

<div align="center">

<img src="https://github-profile-trophy.vercel.app/?username=Ianm-SP&theme=tokyonight&no-frame=true&no-bg=true&margin-w=10&column=7" alt="Troféus do GitHub"/>

</div>

---

## 🎯 Metas

- [x] Aprender os fundamentos de ADVPL
- [x] Estudar boas práticas de ADVPL (Udemy)
- [ ] Migrar rotinas para **TL++** com orientação a objetos
- [ ] Criar e consumir APIs REST no Protheus (`FWRest` / `WsRestFul`)
- [ ] Contribuir com projetos open source da comunidade TOTVS

---

## 📫 Contato

<div align="center">

<a href="https://github.com/Ianm-SP">
  <img src="https://img.shields.io/badge/GitHub-Ianm--SP-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
</a>
<a href="https://www.linkedin.com/in/SEU-USUARIO">
  <img src="https://img.shields.io/badge/LinkedIn-Conectar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
</a>
<a href="mailto:seu-email@exemplo.com">
  <img src="https://img.shields.io/badge/Email-Enviar-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
</a>

<br/><br/>

> *"Código limpo não é escrito seguindo um conjunto de regras. Você não se torna um artesão de software aprendendo uma lista do que fazer e não fazer."* 

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,50:203a43,100:0f2027&height=120&section=footer" alt="Footer" width="100%"/>

</div>
