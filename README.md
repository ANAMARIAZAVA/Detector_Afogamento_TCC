# 🏊‍♂️ SafePoolEx - Sistema Inteligente de Prevenção de Afogamentos em Piscinas

> **Projeto Acadêmico (TCC) | FATEC Botucatu — Análise e Desenvolvimento de Sistemas**

O **SafePoolEx** é um sistema acessível e inteligente voltado para o monitoramento contínuo de áreas aquáticas residenciais e comerciais. Utilizando Inteligência Artificial (Visão Computacional) e Internet das Coisas (IoT), o projeto visa prevenir acidentes por afogamento através da detecção precoce de situações de risco e emissão de alertas em tempo real, com foco especial em crianças e animais de estimação.

---

## 🎯 Objetivos do Projeto

### **Objetivo Geral**
Desenvolver uma solução de baixo custo que utilize IA e sensores para monitorar piscinas, prevenindo acidentes por meio da identificação de cenários de risco e acionamento automático de alertas sonoros e visuais.

### **Objetivos Específicos**
* **Detecção Inteligente:** Aplicar modelos de Visão Computacional (YOLO) para identificar e diferenciar adultos, crianças e pets próximos à piscina.
* **Alertas em Tempo Real:** Disparar sirenes e sinalizações visuais imediatamente ao detectar uma aproximação não supervisionada.
* **Solução Acessível:** Projetar uma arquitetura de baixo custo viável para o mercado brasileiro.
* **Pesquisa e Benchmark:** Mapear e comparar as soluções tecnológicas existentes no mercado de segurança aquática.

---

## 🧐 Problema Abordado

Os afogamentos em piscinas representam uma das principais causas de acidentes fatais em ambientes residenciais, afetando desproporcionalmente crianças. A ausência de supervisão humana constante potencializa esses riscos. O SafePoolEx atua como uma camada de segurança ativa e automatizada para mitigar essas falhas de atenção.

---

## 🧠 Base Teórica e Arquitetura de IA

O projeto fundamenta-se nos seguintes conceitos computacionais:
* **Deep Learning (DL) & Visão Computacional:** Processamento e análise de fluxos de vídeo em tempo real para interpretação de cenários não estruturados.
* **YOLO (You Only Look Once):** Arquitetura de rede neural convolucional de ponta, otimizada para detecção e classificação de objetos com alta velocidade e precisão.
* **Machine Learning (ML):** Aprendizado com dados estruturados para tomada de decisão e refinamento de alertas.

---

## 🛠️ Tecnologias e Ferramentas

* **Linguagem de Programação:** Python 3.8+
* **Frameworks de IA:** Ultralytics YOLO (YOLOv5 / YOLOv8), OpenCV
* **Ambiente de Desenvolvimento:** VS Code, Google Colab (Treinamento com aceleração por GPU)
* **Hardware (Protótipo & Fase Embarcada):** Notebook, Câmeras IP/Local, Raspberry Pi (meta futura), Arduino
* **Banco de Dados:** MySQL (Projetado para persistência de métricas e histórico de eventos)
* **Controle de Versão:** Git e GitHub

---

## 📍 Dataset e Estratégia de Treinamento

* **Dataset Principal:** Combinação de bases públicas focadas em detecção infantil (como o *YOLO-CDD*) com um dataset customizado para cenários aquáticos.
* **Variabilidade das Amostras:** Treinamento planejado considerando variações de iluminação, ângulos de câmera, reflexos na água e diferentes condições ambientais.

---

## 💡 Transparência e Desafios Técnicos (Trade-offs)

O desenvolvimento prático envolveu decisões estratégicas diante de restrições técnicas:

1. **Infraestrutura e Hardware:** Dada a ausência de uma GPU dedicada local para treinamento pesado, utilizou-se o ambiente do **Google Colab** para execução dos scripts.
2. **Escolha da Variante (YOLOv8 Nano):** Optou-se pela versão *Nano* (`yolov8n`) para priorizar alta taxa de quadros por segundo (FPS) e menor latência, permitindo rodar em hardwares mais limitados.
3. **Reconhecimento Acadêmico:** A fundamentação teórica e a modelagem do sistema resultaram em um artigo científico aceito e publicado na revista acadêmica da FATEC.

---

## 🚀 Roadmap e Visão de Futuro

- [x] Prova de conceito e validação do modelo YOLO em ambiente de testes.
- [x] Elaboração e aprovação do artigo científico sobre o projeto.
- [ ] Fine-tuning da rede neural com dataset exclusivo de piscinas complexas.
- [ ] Integração do modelo no hardware embarcado (Raspberry Pi + Arduino).
- [ ] Expansão da detecção para identificar adultos em situação de risco (ex: mal súbito).
- [ ] Integração com assistentes virtuais e plataformas de casas inteligentes (*Smart Home*).

---

## ✒️ Autora e Contato

**Ana Maria Zava**  
*Graduanda em Análise e Desenvolvimento de Sistemas — FATEC Botucatu*  
📧 **Contato:** [anazavafatec@gmail.com](mailto:anazavafatec@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/anamariazava/) | [GitHub Profile](https://github.com/ANAMARIAZAVA)
