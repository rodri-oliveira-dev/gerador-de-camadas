# Gerador de Camadas / DataDrain

> **Projeto histórico — não mantido**
>
> Este repositório preserva um projeto desenvolvido em uma fase importante da minha trajetória profissional. O código e as decisões arquiteturais aqui presentes refletem o contexto, as ferramentas e os padrões da época e **não devem ser interpretados como recomendações para projetos .NET atuais**.

## Sobre o projeto

O Gerador de Camadas, também identificado no código como **DataDrain**, nasceu da necessidade de reduzir o trabalho repetitivo envolvido na criação da estrutura inicial de aplicações .NET orientadas a banco de dados.

A proposta era inspecionar os objetos do banco e, a partir desse modelo, gerar automaticamente parte da solução e do código necessário para uma arquitetura em camadas.

Entre os artefatos gerados estavam projetos e classes para:

- interfaces de persistência;
- objetos de transferência de dados (TO);
- camada de acesso a dados (DAL);
- camada de regras de negócio (BLL);
- solução do Visual Studio;
- suporte opcional a WCF em uma das evoluções do projeto.

O gerador também trabalhava com metadados de tabelas, views e procedures e passou por diferentes implementações de providers de banco de dados ao longo de sua evolução.

## Contexto histórico

Embora este repositório tenha sido criado no GitHub em 2016, parte do código é anterior. O changelog original preservado no projeto registra versões publicadas em **2013**.

Naquele contexto, gerar automaticamente DALs, interfaces, objetos de transferência, projetos e arquivos de solução resolvia um problema bastante concreto: havia muito código estrutural e repetitivo sendo produzido manualmente em aplicações corporativas .NET.

O projeto evoluiu ao longo do tempo, incluindo funcionalidades como:

- geração de projetos em múltiplas camadas;
- mapeamento de tabelas, views e stored procedures;
- suporte a diferentes providers de banco de dados;
- geração de operações de persistência;
- paginação;
- validações baseadas em expressões regulares;
- geração opcional de projetos WCF;
- suporte a diferentes versões do .NET Framework;
- logging com log4net;
- geração e uso de strong names, prática que fazia parte da distribuição original dos assemblies.

O histórico completo recuperado do projeto pode ser consultado em [CHANGELOG-LEGACY.md](CHANGELOG-LEGACY.md).

## Estrutura preservada

O repositório mantém três snapshots principais:

```text
1.0/
2.0/
3.0/
```

Eles foram mantidos propositalmente como parte do registro histórico do desenvolvimento.

Alguns dos principais componentes encontrados nas diferentes versões são:

```text
DataDrain.ORM.Generator
DataDrain.MicroORM
DataDrain.ORM.DAL
DataDrain.ORM.DAL.SqlServer
DataDrain.ORM.DAL.MySQL
DataDrain.ORM.Interfaces
```

A versão `2.0` contém uma reorganização da solução em componentes como:

```text
DataDrain.BusinessLayer
DataDrain.Databases.MySql
DataDrain.Databases.SqlServer
DataDrain.Interfaces
DataDrain.IO
DataDrain.Library
DataDrain.UI.WinForm
```

## Uma nota pessoal

Tenho um carinho especial por este projeto.

Ele representa uma época em que eu estava tentando transformar problemas recorrentes do desenvolvimento em ferramentas reutilizáveis. Muito antes de algumas das facilidades que hoje fazem parte do ecossistema .NET, a ideia aqui já era automatizar trabalho repetitivo, criar convenções e permitir que o desenvolvedor se concentrasse mais na aplicação do que na criação manual de infraestrutura.

Revisitar este código muitos anos depois também é uma forma interessante de observar minha própria evolução como desenvolvedor e arquiteto de software.

Há decisões que eu certamente não repetiria hoje. Há abstrações que hoje faria de outra maneira. Há tecnologias que deixaram de fazer sentido.

E isso é justamente parte do valor deste repositório.

Ele não está aqui para demonstrar como eu escreveria uma aplicação em 2026. Está aqui para preservar **como eu pensava, quais problemas eu estava tentando resolver e o que eu construí naquele momento da minha carreira**.

## O que eu faria diferente hoje

Se estivesse resolvendo um problema semelhante atualmente, a abordagem seria bastante diferente.

Eu provavelmente evitaria um gerador rígido de arquitetura em camadas e privilegiaria soluções menores e mais composáveis. Dependendo do cenário, usaria recursos atuais do ecossistema .NET, templates, source generators ou ferramentas especializadas, mantendo regras de domínio separadas das decisões de persistência.

Também trataria configuração, dependências, observabilidade, segurança, testes e automação de build de acordo com práticas modernas.

Essa diferença não invalida a solução original. Ela mostra como o contexto tecnológico e minha própria visão de arquitetura mudaram ao longo do tempo.

## Limpeza e preservação

Em 2026 o repositório passou por uma pequena restauração para ser preservado com mais segurança e clareza.

Foram removidos apenas artefatos que não agregavam valor histórico ou que não deveriam permanecer versionados, como:

- arquivos locais do Visual Studio;
- caches e pacotes NuGet restauráveis;
- símbolos de debug;
- chaves e certificados privados usados originalmente para assinatura;
- binários órfãos sem referência no projeto.

O código-fonte, a estrutura das versões e os elementos que ajudam a compreender o funcionamento e a evolução do projeto foram mantidos.

## Contribuindo

Este projeto não está mais em desenvolvimento ativo. Contribuições são limitadas principalmente à preservação e à documentação do projeto.

Consulte [CONTRIBUTING.md](CONTRIBUTING.md) antes de abrir uma issue ou Pull Request.

## Status

Este projeto está **arquivado conceitualmente** e não recebe desenvolvimento de novas funcionalidades.

Ele é mantido como:

- registro histórico;
- material de referência;
- parte da minha trajetória profissional.

Para projetos atuais, consulte meus outros repositórios no GitHub.
