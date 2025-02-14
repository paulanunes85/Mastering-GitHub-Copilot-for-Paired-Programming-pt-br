<header>

# Introdução ao GitHub Codespaces

Bem-vindo ao empolgante mundo do GitHub Codespaces, seu recurso de codificação baseado em nuvem. Neste módulo, vamos mergulhar no reino dos ambientes de desenvolvimento instantâneos e baseados em nuvem, revolucionando a maneira como você aborda a codificação. O GitHub Codespaces oferece uma experiência integrada, fornecendo um contêiner equipado com as linguagens, ferramentas e utilitários essenciais para o desenvolvimento.

Ao longo desta jornada de aprendizado, embarcaremos na descoberta do ciclo de vida e dos processos do Codespaces. Descubra o poder de personalizar a configuração do seu Codespace para atender às suas preferências e requisitos exclusivos. Para solidificar seu entendimento, encerraremos o módulo com um exercício prático, permitindo que você flexione seus músculos de codificação dentro do ambiente do GitHub Codespaces.

Imagine um ambiente de desenvolvimento totalmente configurado ao seu alcance, acessível de qualquer computador com conexão à internet. O GitHub Codespaces abre a porta para uma nova era de codificação colaborativa e flexível. Vamos mergulhar e desbloquear todo o potencial do desenvolvimento baseado em nuvem com o GitHub Codespaces!

</header>

- **Para quem é isso:** Desenvolvedores, Engenheiros DevOps, Gerentes de Engenharia, Gerentes de Produto.
- **O que você aprenderá:** Como criar um codespace, enviar código de um codespace, selecionar uma imagem personalizada e personalizar um codespace.
- **O que você construirá:** Um codespace com arquivos devcontainer.json, personalizações e customizações.
- **Pré-requisitos:** Você precisará saber o seguinte:
  - Uso do Visual Studio Code, [Visual Studio Code Docs](https://code.visualstudio.com/docs).
  - Compreensão do uso do GitHub ou conclusão do módulo anterior [Introdução ao GitHub](https://github.com/paulanunes85/Mastering-GitHub-Copilot-for-Paired-Programming/tree/main/01-Introduction-to-GitHub).
- **Tempo:** Este curso pode ser concluído em menos de uma hora.

Ao final deste módulo, você será capaz de:

1. Descrever o GitHub Codespaces.
2. Explicar o ciclo de vida do GitHub Codespaces e como realizar cada etapa.
3. Definir as diferentes personalizações que você pode fazer no GitHub Codespaces.


## Leitura pré-requisito: 

- [Code with GitHub Codespaces](https://learn.microsoft.com/training/modules/code-with-github-codespaces/?WT.mc_id=academic-113596-abartolo)
- O que é GitHub Codespaces? (Playlist de vídeos abaixo)
- [![O que é Codespaces?](https://img.youtube.com/vi/ozuDPmcC1io/0.jpg)](https://www.youtube.com/watch?v=ozuDPmcC1io&list=PLmsFUfdnGr3wTl-NCblzcrEv2lFSX975-)



### Como iniciar este curso

<!-- For start course, run in JavaScript:
'https://github.com/new?' + new URLSearchParams({
  template_owner: 'skills',
  template_name: 'code-with-codespaces',
  owner: '@me',
  name: 'skills-code-with-codespaces',
  description: 'My clone repository',
  visibility: 'public',
}).toString()
-->

[![Iniciar Curso](https://user-images.githubusercontent.com/1221423/235727646-4a590299-ffe5-480d-8cd5-8194ea184546.svg)](https://github.com/new?template_owner=skills&template_name=code-with-codespaces&owner=%40me&name=skills-code-with-codespaces&description=My+clone+repository&visibility=public)

1. Clique com o botão direito em **Iniciar curso** e abra o link em uma nova aba.
2. Na nova aba, a maioria dos prompts será preenchida automaticamente para você.
   - Para o proprietário, escolha sua conta pessoal ou uma organização para hospedar o repositório.
   - Recomendamos criar um repositório público, pois repositórios privados [use Actions minutes](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions?WT.mc_id=academic-113596-abartolo).
   - Role para baixo e clique no botão **Criar repositório** na parte inferior do formulário.
3. Após a criação do seu novo repositório, espere cerca de 20 segundos e atualize a página. Siga as instruções passo a passo no README do novo repositório.

## Avisos Legais
 
A Microsoft e quaisquer colaboradores concedem a você uma licença para a documentação da Microsoft e outros conteúdos neste repositório sob a [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode),
veja [LICENSE](LICENSE) e concedem a você uma licença para qualquer código no repositório sob a  [MIT License](https://opensource.org/licenses/MIT), consulte
[LICENSE-CODE](LICENSE-CODE)
 
Microsoft, Windows, Microsoft Azure e/ou outros produtos e serviços da Microsoft referenciados na documentação podem ser marcas registradas ou marcas registradas da Microsoft nos Estados Unidos e/ou em outros países. As licenças para este projeto não concedem a você direitos de uso de quaisquer nomes, logotipos ou marcas registradas da Microsoft. As diretrizes gerais de marcas registradas da Microsoft podem ser encontradas em http://go.microsoft.com/fwlink/?LinkID=254653.
 
As informações de privacidade podem ser encontradas em https://privacy.microsoft.com/en-us/
 
A Microsoft e quaisquer colaboradores reservam todos os outros direitos, sejam sob seus respectivos direitos autorais, patentes, ou marcas registradas, seja por implicação, estoppel ou de outra forma.
<!--
<footer>

  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---


Obtenha ajuda: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/introduction-to-github) &bull; [Review the GitHub status page](https://www.githubstatus.com/)
