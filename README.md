# 🏊 SafePoolEx

### Sistema Inteligente de Prevenção de Afogamentos em Piscinas

> **Projeto Acadêmico (TCC) | FATEC Botucatu — Análise e Desenvolvimento de Sistemas**

---

## 📌 Sobre o Projeto

O **SafePoolEx** é uma proposta de solução tecnológica voltada à **prevenção de acidentes em piscinas**, utilizando conceitos de **Inteligência Artificial, Visão Computacional e Internet das Coisas (IoT)**.

A ideia central do projeto é desenvolver uma camada adicional de segurança capaz de **monitorar continuamente uma área de piscina**, identificar situações potencialmente perigosas e emitir alertas para reduzir o tempo de resposta diante de um possível incidente.

O projeto foi concebido especialmente considerando situações envolvendo **crianças e animais**, nas quais a identificação rápida de uma aproximação da área da piscina poderia contribuir para uma intervenção preventiva.

O desenvolvimento surgiu no contexto de um **Trabalho de Conclusão de Curso (TCC)** e evoluiu ao longo da pesquisa para uma proposta de desenvolvimento de software, contemplando levantamento tecnológico, definição de arquitetura, estudo de modelos de Visão Computacional, análise de datasets e identificação dos desafios necessários para uma futura implementação.

> **Importante:** o SafePoolEx não deve ser apresentado como um sistema comercial ou como uma solução de prevenção de afogamentos já validada em ambiente real. O projeto representa uma **proposta tecnológica acadêmica**, acompanhada de pesquisa, definição de arquitetura, experimentação inicial e documentação dos desafios técnicos para sua evolução.

---

## 🎯 Objetivos do Projeto

### Objetivo Geral

Propor uma solução de baixo custo baseada em **Inteligência Artificial, Visão Computacional e IoT** para monitoramento de áreas de piscina e identificação de situações potencialmente perigosas, permitindo o acionamento de alertas preventivos.

### Objetivos Específicos

* Estudar a aplicação de **Visão Computacional** no monitoramento de piscinas.
* Pesquisar modelos de detecção de objetos baseados em **YOLO**.
* Investigar a possibilidade de diferenciação entre **adultos, crianças e animais**.
* Pesquisar datasets adequados para treinamento e ajuste de modelos.
* Avaliar os desafios relacionados à identificação de pessoas em diferentes posições e distâncias da câmera.
* Definir uma arquitetura de software e hardware para uma futura implementação.
* Estudar mecanismos de emissão de **alertas sonoros e visuais**.
* Avaliar a utilização de dispositivos embarcados, como Raspberry Pi e Arduino.
* Pesquisar soluções existentes e possibilidades de aplicação da tecnologia.
* Documentar as limitações encontradas durante o desenvolvimento e as possibilidades de evolução do projeto.

---

## 🧐 Problema Abordado

Piscinas residenciais e comerciais apresentam riscos de acidentes, principalmente quando não existe supervisão constante.

Uma pessoa pode se aproximar da piscina sem que os responsáveis percebam imediatamente. Em determinadas situações, segundos podem ser importantes para que uma intervenção preventiva aconteça.

A proposta do SafePoolEx surgiu justamente da possibilidade de utilizar tecnologia para criar uma **camada adicional de monitoramento**, capaz de observar continuamente o ambiente e identificar comportamentos ou situações que mereçam atenção.

A solução proposta combina:

**Câmera → Visão Computacional → Inteligência Artificial → Análise da situação → Alerta**

A intenção não é substituir a supervisão humana, mas criar um mecanismo tecnológico complementar.

---

## 🧠 Conceito da Solução

A arquitetura conceitual do SafePoolEx pode ser representada da seguinte forma:

```text
              ┌──────────────────┐
              │      Câmera      │
              │   Monitoramento  │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Visão            │
              │ Computacional    │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Modelo de IA     │
              │      YOLO        │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Identificação    │
              │ dos objetos      │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Análise de       │
              │ situação de risco│
              └────────┬─────────┘
                       │
             ┌─────────┴─────────┐
             ▼                   ▼
      ┌─────────────┐     ┌─────────────┐
      │ Alerta      │     │ Registro    │
      │ Sonoro/     │     │ do evento   │
      │ Visual      │     │             │
      └─────────────┘     └─────────────┘
```

---

## 🤖 Inteligência Artificial e Visão Computacional

Um dos principais componentes estudados no projeto foi a utilização de modelos de **detecção de objetos**, especialmente a família **YOLO (You Only Look Once)**.

A escolha desse tipo de arquitetura está relacionada à possibilidade de realizar detecção de objetos em imagens e vídeos com velocidade adequada para aplicações próximas do tempo real.

No contexto do SafePoolEx, a pesquisa considerou a possibilidade de utilizar a Visão Computacional para identificar diferentes classes de objetos e pessoas presentes no ambiente.

Entre os elementos considerados estão:

* Adultos;
* Crianças;
* Animais;
* Área da piscina;
* Possíveis situações de aproximação.

---

## 🔎 Um dos Principais Desafios Técnicos

Durante a pesquisa e o desenvolvimento da proposta, um dos maiores desafios identificados foi a **diferenciação entre adultos e crianças**.

Esse problema é mais complexo do que simplesmente identificar a presença de uma pessoa.

O sistema precisaria ser capaz de reconhecer corretamente a diferença entre essas categorias considerando diferentes condições de captura, como:

* Pessoa de frente para a câmera;
* Pessoa de costas;
* Pessoa próxima à câmera;
* Pessoa distante da câmera;
* Diferentes ângulos de visão;
* Diferentes condições de iluminação;
* Diferentes ambientes;
* Ocultação parcial do corpo;
* Diferentes posições próximas à piscina.

Por exemplo, uma pessoa distante da câmera pode apresentar poucos elementos visuais suficientes para que o modelo faça uma classificação confiável.

Da mesma forma, uma criança vista de costas ou parcialmente ocluída pode ser significativamente mais difícil de diferenciar de um adulto.

Esse desafio levou à necessidade de investigar **datasets existentes e estratégias de treinamento e fine-tuning** capazes de melhorar a capacidade de classificação do modelo.

---

## 📚 Dataset e Estratégia de Treinamento

Uma das etapas pesquisadas foi a utilização de **datasets públicos** para complementar os dados necessários ao treinamento do modelo.

A estratégia considerada consistia em aproveitar bases de dados existentes e, posteriormente, realizar um processo de adaptação do modelo para o contexto específico do projeto.

A intenção era utilizar dados que apresentassem diferentes características de pessoas, principalmente crianças e adultos, e posteriormente combinar esse conhecimento com imagens relacionadas ao ambiente de piscinas.

A estratégia conceitual seria:

```text
Dataset público
      │
      ▼
Preparação dos dados
      │
      ▼
Anotação / organização
      │
      ▼
Treinamento do modelo
      │
      ▼
Fine-tuning
      │
      ▼
Testes em diferentes cenários
      │
      ▼
Avaliação dos resultados
```

Entretanto, essa etapa possui uma dependência importante de **recursos computacionais**, especialmente GPU.

---

## ⚙️ Limitação de Recursos Computacionais

Durante o desenvolvimento, foi identificada uma limitação prática importante.

O treinamento e o fine-tuning de modelos de Inteligência Artificial, principalmente quando associados a datasets maiores e múltiplas épocas de treinamento, podem exigir uma capacidade computacional significativa.

A infraestrutura disponível não era suficiente para realizar todo o treinamento necessário de maneira adequada.

Foi estudada a utilização do **Google Colab** como alternativa para disponibilizar processamento por GPU.

Entretanto, os recursos gratuitos disponíveis foram insuficientes para concluir o treinamento necessário para a validação completa da diferenciação entre adultos e crianças.

Dessa forma, **a etapa de validação final do modelo não foi concluída**.

Essa informação é importante para manter a transparência técnica do projeto.

O SafePoolEx, portanto, **não deve afirmar que o modelo foi plenamente validado para reconhecer adultos e crianças em todos os cenários propostos**.

---

## 🧪 O Que Foi Desenvolvido

Apesar da limitação relacionada ao treinamento, o projeto não foi simplesmente interrompido.

O trabalho foi redirecionado para uma abordagem de **proposta de desenvolvimento de software**, mantendo a pesquisa e a estruturação da solução.

Entre os elementos desenvolvidos e estudados estão:

* Definição do problema;
* Levantamento de requisitos;
* Pesquisa de tecnologias;
* Pesquisa sobre Visão Computacional;
* Estudo da arquitetura YOLO;
* Investigação de datasets;
* Definição da estratégia de treinamento;
* Estudo de alternativas de infraestrutura;
* Definição conceitual da arquitetura;
* Estudo da integração entre software e hardware;
* Definição de mecanismos de alerta;
* Análise dos desafios técnicos;
* Definição de possibilidades de evolução.

---

## 🔬 O Que Foi Pesquisado

A pesquisa do projeto envolveu diferentes áreas relacionadas ao desenvolvimento da solução.

### Inteligência Artificial

* Machine Learning;
* Deep Learning;
* Redes neurais;
* Detecção de objetos;
* Classificação de objetos;
* Fine-tuning.

### Visão Computacional

* Processamento de imagens;
* Processamento de vídeo;
* Detecção de pessoas;
* Detecção de objetos;
* Análise de diferentes ângulos de captura;
* Condições de iluminação;
* Distância do objeto em relação à câmera.

### Modelos YOLO

Foram estudadas versões da arquitetura YOLO e sua utilização em aplicações de detecção de objetos.

### Datasets

Foi analisada a possibilidade de utilizar datasets públicos para complementar os dados necessários ao treinamento do modelo.

### IoT e Hardware

Também foi estudada uma arquitetura envolvendo dispositivos como:

* Raspberry Pi;
* Arduino;
* Câmeras;
* Sensores;
* Dispositivos de alerta.

---

## 🛠️ Tecnologias e Ferramentas Estudadas

| Tecnologia / Ferramenta | Utilização no projeto                        |
| ----------------------- | -------------------------------------------- |
| **Python**              | Desenvolvimento e experimentação             |
| **YOLO**                | Estudo de detecção de objetos                |
| **Ultralytics**         | Framework para modelos YOLO                  |
| **OpenCV**              | Processamento de imagens e vídeo             |
| **Google Colab**        | Ambiente para experimentação e treinamento   |
| **Git**                 | Controle de versão                           |
| **GitHub**              | Versionamento e documentação                 |
| **MySQL**               | Banco de dados considerado para persistência |
| **Raspberry Pi**        | Hardware embarcado considerado               |
| **Arduino**             | Controle de componentes e alertas            |
| **Câmeras**             | Captura das imagens para análise             |

---

## 🏗️ Arquitetura Conceitual

A arquitetura proposta considera a separação entre captura, processamento, análise e resposta.

```text
┌─────────────────────┐
│       CÂMERA        │
│ Captura do ambiente │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ PROCESSAMENTO       │
│ OpenCV / Python     │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ INTELIGÊNCIA        │
│ ARTIFICIAL          │
│ YOLO                │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ ANÁLISE DA SITUAÇÃO │
│                     │
│ Pessoa / Criança /  │
│ Adulto / Animal     │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ MOTOR DE DECISÃO    │
│                     │
│ Situação de risco?  │
└──────────┬──────────┘
           │
       ┌───┴───┐
       ▼       ▼
      SIM     NÃO
       │       │
       ▼       ▼
   ┌───────┐  Monitoramento
   │ALERTA │  contínuo
   └───────┘
```

---

## 🚨 Sistema de Alertas

A proposta prevê a utilização de mecanismos de alerta capazes de chamar a atenção dos responsáveis quando uma situação considerada de risco fosse identificada.

Entre as possibilidades estudadas:

* Sirene;
* Alerta sonoro;
* Sinalização visual;
* Comunicação com dispositivos externos;
* Registro do evento;
* Integração futura com sistemas de automação residencial.

---

## 🗄️ Persistência e Histórico

Como parte da arquitetura proposta, foi considerada a utilização de um banco de dados para armazenar informações relacionadas aos eventos detectados.

Entre os possíveis registros:

* Data e horário;
* Tipo de evento;
* Categoria identificada;
* Status do alerta;
* Histórico de ocorrências;
* Informações relacionadas ao monitoramento.

A utilização de banco de dados permanece como parte da **arquitetura proposta**, não sendo apresentada como uma funcionalidade de um sistema comercial já implementado.

---

## 🔐 Segurança e Responsabilidade

Por se tratar de uma solução relacionada à segurança de pessoas, especialmente crianças, qualquer implementação real exigiria um nível elevado de confiabilidade.

Um sistema dessa natureza não poderia depender exclusivamente da Inteligência Artificial para garantir a segurança.

Por isso, uma futura implementação deveria considerar:

* Falsos positivos;
* Falsos negativos;
* Falhas de câmera;
* Falhas de energia;
* Falhas de conexão;
* Falhas de processamento;
* Condições climáticas;
* Iluminação inadequada;
* Oclusão de pessoas;
* Manutenção dos equipamentos;
* Mecanismos redundantes de segurança.

O SafePoolEx deve ser entendido como **uma camada tecnológica complementar**, e não como substituto da supervisão humana ou de dispositivos de segurança adequados.

---

## 📊 Resultados e Validação

### O que foi efetivamente alcançado

O projeto permitiu estruturar uma proposta tecnológica envolvendo:

* Inteligência Artificial;
* Visão Computacional;
* IoT;
* Detecção de objetos;
* Monitoramento por vídeo;
* Automação de alertas;
* Hardware embarcado;
* Banco de dados;
* Arquitetura de software.

Também foram identificados os principais desafios necessários para transformar a proposta em uma solução funcional.

### O que não foi validado

A diferenciação robusta entre **adultos e crianças em diferentes condições de captura** não foi validada de forma conclusiva.

A principal razão foi a impossibilidade de realizar o treinamento e fine-tuning necessários devido à **limitação de recursos computacionais disponíveis para processamento por GPU**.

Portanto, este README não apresenta métricas de precisão, recall, mAP ou outros indicadores como resultados finais do sistema, pois não seria tecnicamente correto apresentar números que não foram obtidos por uma validação experimental concluída.

---

## 💡 Decisão de Escopo

Ao longo do desenvolvimento do TCC, o projeto passou por uma mudança de direcionamento.

Inicialmente, havia a intenção de transformar a proposta em um protótipo funcional com treinamento e validação do modelo.

Entretanto, diante dos desafios técnicos e da necessidade de infraestrutura computacional específica para realizar o treinamento adequado, o projeto foi redirecionado.

Após a mudança de orientação do TCC, a proposta passou a ser tratada como uma **sugestão estruturada de desenvolvimento de software**, preservando a pesquisa realizada e documentando os caminhos necessários para uma futura implementação.

Essa mudança permitiu manter o trabalho tecnicamente consistente sem apresentar como concluídas etapas que, de fato, ainda necessitam de experimentação e validação.

---

## 📈 Roadmap de Evolução

O desenvolvimento futuro do SafePoolEx pode seguir diferentes etapas.

### Fase 1 — Dataset

* [ ] Selecionar datasets públicos adequados.
* [ ] Avaliar qualidade e diversidade das imagens.
* [ ] Preparar as classes necessárias.
* [ ] Complementar os dados com imagens específicas de ambientes aquáticos.
* [ ] Avaliar necessidade de criação de dataset próprio.

### Fase 2 — Treinamento

* [ ] Configurar ambiente com GPU adequada.
* [ ] Realizar fine-tuning do modelo.
* [ ] Testar diferentes parâmetros.
* [ ] Avaliar diferentes versões do YOLO.
* [ ] Comparar resultados.

### Fase 3 — Validação

* [ ] Criar conjunto de testes independente.
* [ ] Testar pessoas de frente.
* [ ] Testar pessoas de costas.
* [ ] Testar diferentes distâncias.
* [ ] Testar diferentes ângulos.
* [ ] Testar diferentes condições de iluminação.
* [ ] Avaliar falsos positivos.
* [ ] Avaliar falsos negativos.
* [ ] Medir precisão, recall e mAP.

### Fase 4 — Protótipo

* [ ] Integrar câmera.
* [ ] Integrar processamento.
* [ ] Implementar mecanismo de decisão.
* [ ] Integrar alertas sonoros.
* [ ] Integrar alertas visuais.
* [ ] Criar registro dos eventos.

### Fase 5 — Hardware Embarcado

* [ ] Avaliar Raspberry Pi ou hardware equivalente.
* [ ] Integrar Arduino quando necessário.
* [ ] Avaliar desempenho do modelo em hardware limitado.
* [ ] Otimizar consumo de recursos.
* [ ] Avaliar latência.

### Fase 6 — Evolução

* [ ] Identificação de diferentes situações de risco.
* [ ] Monitoramento de comportamento.
* [ ] Integração com Smart Home.
* [ ] Notificações remotas.
* [ ] Dashboard de monitoramento.
* [ ] Histórico de eventos.
* [ ] Avaliação de funcionamento em ambiente real.

---

## 📚 Aprendizados

O desenvolvimento do SafePoolEx proporcionou aprendizado em diferentes áreas da tecnologia.

Entre os principais conhecimentos trabalhados estão:

* Análise de requisitos;
* Pesquisa tecnológica;
* Inteligência Artificial;
* Machine Learning;
* Deep Learning;
* Visão Computacional;
* Detecção de objetos;
* Arquitetura YOLO;
* Datasets;
* Fine-tuning;
* Python;
* OpenCV;
* IoT;
* Hardware embarcado;
* Banco de dados;
* Controle de versão;
* Documentação técnica;
* Análise de limitações técnicas.

Um dos principais aprendizados foi compreender que **desenvolver uma solução baseada em Inteligência Artificial envolve muito mais do que escolher um modelo pronto**.

A qualidade do dataset, a diversidade das amostras, a infraestrutura disponível, o treinamento, os testes e a validação são elementos fundamentais para determinar se um modelo pode ser utilizado de maneira confiável.

---

## 🧩 Principais Desafios

| Desafio                                | Impacto                                         |
| -------------------------------------- | ----------------------------------------------- |
| Diferenciação entre adultos e crianças | Exigiu treinamento específico                   |
| Variação de distância                  | Pode afetar a classificação                     |
| Pessoas de costas                      | Aumenta a dificuldade de identificação          |
| Diferentes ângulos                     | Exige maior diversidade no dataset              |
| Iluminação                             | Pode interferir na detecção                     |
| Reflexos da água                       | Podem gerar dificuldades na Visão Computacional |
| Dataset adequado                       | Necessário para melhorar a generalização        |
| Treinamento com GPU                    | Exige recursos computacionais                   |
| Hardware embarcado                     | Necessita otimização do modelo                  |
| Validação experimental                 | Necessita infraestrutura e conjunto de testes   |

---

## 🌱 Visão de Futuro

O SafePoolEx permanece como uma proposta com potencial de evolução para um sistema experimental de monitoramento inteligente.

Uma futura implementação poderia combinar:

```text
          VISÃO COMPUTACIONAL
                  │
                  ▼
          INTELIGÊNCIA ARTIFICIAL
                  │
                  ▼
             IoT / EDGE
                  │
        ┌─────────┴─────────┐
        ▼                   ▼
     ALERTA              REGISTRO
        │                   │
        └─────────┬─────────┘
                  ▼
            SMART HOME
```

O desenvolvimento futuro deverá priorizar principalmente a **qualidade da validação**, buscando demonstrar empiricamente o desempenho do sistema antes de qualquer aplicação prática.

---

## 📖 Contexto Acadêmico

O SafePoolEx foi desenvolvido no contexto da formação em **Análise e Desenvolvimento de Sistemas pela FATEC Botucatu**.

O trabalho teve como foco a investigação de uma aplicação prática de tecnologias emergentes para solucionar um problema real, combinando diferentes áreas da computação em uma única proposta.

Além do desenvolvimento acadêmico, o projeto contribuiu para a experiência prática em:

* Pesquisa;
* Desenvolvimento de software;
* Inteligência Artificial;
* Documentação;
* Análise de viabilidade;
* Tomada de decisões técnicas;
* Identificação de limitações;
* Planejamento de evolução tecnológica.

---

## 🏆 Status do Projeto

**Status atual:** 📚 Projeto acadêmico / Proposta de desenvolvimento

| Etapa                                  | Status          |
| -------------------------------------- | --------------- |
| Identificação do problema              | ✅ Concluída     |
| Pesquisa tecnológica                   | ✅ Concluída     |
| Estudo de Visão Computacional          | ✅ Concluído     |
| Estudo de modelos YOLO                 | ✅ Concluído     |
| Pesquisa de datasets                   | ✅ Realizada     |
| Definição da arquitetura               | ✅ Realizada     |
| Definição da estratégia de treinamento | ✅ Realizada     |
| Treinamento completo do modelo         | ⏳ Não concluído |
| Fine-tuning específico                 | ⏳ Futuro        |
| Validação robusta adulto × criança     | ⏳ Futuro        |
| Protótipo embarcado                    | ⏳ Futuro        |
| Testes em ambiente real                | ⏳ Futuro        |

---

## 🎓 Formação

**Ana Maria Zava**

**Tecnóloga em Análise e Desenvolvimento de Sistemas — FATEC Botucatu**

Formação concluída.

---

## 👩‍💻 Sobre a Autora

Profissional recém-formada em **Análise e Desenvolvimento de Sistemas**, com interesse em tecnologia, desenvolvimento de soluções, análise de requisitos, processos, suporte funcional, SQL, documentação técnica e Inteligência Artificial.

O SafePoolEx representa uma experiência acadêmica de investigação e desenvolvimento, demonstrando não apenas a aplicação de tecnologias, mas também a capacidade de **identificar limitações, avaliar viabilidade técnica e propor caminhos de evolução**.

---

## 📫 Contato

**Ana Maria Zava**

📧 **E-mail:** [anazavafatec@gmail.com](mailto:anazavafatec@gmail.com)

🔗 **LinkedIn:** https://www.linkedin.com/in/anamariazava/

🔗 **GitHub:** https://github.com/ANAMARIAZAVA

---

## 📌 Considerações Finais

O SafePoolEx representa uma proposta de aplicação de **Inteligência Artificial, Visão Computacional e IoT** em um problema real de segurança.

Mais do que apresentar um sistema como pronto, este projeto documenta o processo de investigação, as decisões tomadas, os desafios encontrados e as etapas necessárias para transformar a proposta em uma solução efetivamente validada.

A principal evolução necessária está relacionada ao treinamento e à validação do modelo de Inteligência Artificial, especialmente na diferenciação entre adultos e crianças em diferentes condições de captura.

Essa etapa permanece como uma oportunidade de continuidade do projeto, mediante disponibilidade de datasets adequados e infraestrutura computacional suficiente para treinamento e experimentação.

> **O objetivo deste repositório é apresentar com transparência aquilo que foi pesquisado e desenvolvido, diferenciando claramente os resultados alcançados das funcionalidades que permanecem como evolução futura.**

---

## ⭐ Projeto Acadêmico

**SafePoolEx — Sistema Inteligente de Prevenção de Afogamentos em Piscinas**

**FATEC Botucatu — Análise e Desenvolvimento de Sistemas**

**Autora:** Ana Maria Zava
