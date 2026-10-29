<h1 align="center">Ian M. <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="28" alt="👋"/></h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&pause=1200&color=0C9AD6&center=true&vCenter=true&width=520&lines=Desenvolvedor+ADVPL+%2F+TOTVS+Protheus;C%C3%B3digo+limpo+e+boas+pr%C3%A1ticas;APIs+REST+%2B+SQL" alt="Typing SVG"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ADVPL-0C9AD6?style=flat-square" alt="ADVPL"/>
  <img src="https://img.shields.io/badge/TL++-1B5E8C?style=flat-square" alt="TL++"/>
  <img src="https://img.shields.io/badge/Protheus-0C9AD6?style=flat-square" alt="Protheus"/>
  <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" alt="SQL"/>
  <img src="https://img.shields.io/badge/REST-009688?style=flat-square" alt="REST"/>
  <img src="https://komarev.com/ghpvc/?username=Ianm-SP&label=Visitas&color=0C9AD6&style=flat-square" alt="Visitas"/>
</p>

---

### 🧑‍💻 Sobre

- Desenvolvo e customizo no **TOTVS Protheus** com **ADVPL / TL++**
- Estudando **boas práticas em ADVPL** na Udemy
- Foco em integrações, APIs REST e SQL
- São Paulo, Brasil 🇧🇷

### 🛠️ Stack

<p>
  <img src="https://skillicons.dev/icons?i=git,github,vscode,postgres,mysql,js,html,css&theme=dark" alt="Stack"/>
</p>

### ✅ Boas práticas em ADVPL que uso

<a href="https://www.udemy.com/courses/search/?q=advpl%20boas%20pr%C3%A1ticas">
  <img src="https://img.shields.io/badge/Udemy-Boas%20Pr%C3%A1ticas%20ADVPL-A435F0?style=flat-square&logo=udemy&logoColor=white" alt="Udemy"/>
</a>

- `Local` sempre; evitar `Private` e `Public`
- Notação húngara: `cNome`, `nValor`, `dData`, `lOk`, `aLista`
- `GetArea()` / `RestArea()` em toda rotina que mexe em tabela
- `#Define` no lugar de números mágicos
- `BeginSQL` / `EndSQL` e `%table:%` nas queries
- Tratamento de erro com `Begin Sequence` e logs com `FWLogMsg`
- Documentar com `Protheus.doc`

```advpl
User Function BuscaCli(cCod, cLoja)
    Local aArea := GetArea()
    Local cNome := ""

    DbSelectArea("SA1")
    SA1->(DbSetOrder(1))

    If SA1->(DbSeek(FWxFilial("SA1") + cCod + cLoja))
        cNome := AllTrim(SA1->A1_NOME)
    EndIf

    RestArea(aArea)
Return cNome
```

### 📊 GitHub

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Ianm-SP&show_icons=true&theme=tokyonight&hide_border=true" height="150" alt="Stats"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ianm-SP&layout=compact&theme=tokyonight&hide_border=true" height="150" alt="Linguagens"/>
</p>

### 📫 Contato

<p>
  <a href="https://www.linkedin.com/in/SEU-USUARIO"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:seu-email@exemplo.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
</p>
