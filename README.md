# Apresentação FAT -- Radar Banda C Vaisala WRS300 (SSPA / RVP10)

Este repositório contém os arquivos-fonte em **LaTeX Beamer** para a apresentação técnica de **Teste de Aceitação em Fábrica (FAT - *Factory Acceptance Test*)** do radar meteorológico **Vaisala WRS300 (Banda C Estado Sólido SSPA)** equipado com o processador digital **Vaisala RVP10**, controlador **RCP8** e ambiente de software **IRIS**.

A estrutura do Beamer foi padronizada no tema `Madrid` (16:9) com paleta de cores corporativa e acadêmica (Vaisala / UFPR), integrando conceitos fundamentais de compressão de pulso, mitigação de ground clutter e transição de sistemas valvulados para estado sólido.

---

## 🚀 Como Abrir e Compilar no Overleaf

1. Faça o download deste repositório como arquivo `.ZIP` (ou clone o repositório).
2. Acesse sua conta no [Overleaf](https://www.overleaf.com/).
3. Clique em **New Project** $\rightarrow$ **Upload Project**.
4. Selecione o arquivo `.ZIP` baixado.
5. Defina o compilador como **pdfLaTeX** (padrão) e compile `main.tex`.

---

## 📑 Estrutura da Apresentação

1. **Escopo, Objetivos e Paradigma Tecnológico:**
   - Objetivos do FAT e critérios de aceitação fabril.
   - Comparativo detalhado: **Radar Valvulado (*Magnetron/Klystron*) vs. Estado Sólido (*SSPA*)**.
   - O Paradigma SST: Desafios de compressão de pulso, $PSLR$, mascaramento por ground clutter e modulações avançadas.
2. **Arquitetura, Mecânica e Segurança:**
   - Diagrama de blocos do WRS300, RVP10, RCP8 e IRIS.
   - Inspeção de correias, sensores de proximidade de $5\text{ mm}$, guias de onda e desidratador.
   - Alinhamento angular de elevação (fio de prumo a $\pm 0.05^\circ$) e fins de curso ($-3.5^\circ$ e $+112^\circ$).
   - Loop de emergência (*E-Stop*), *Interlock* do radome (2 canais NC) e PPU.
3. **Transmissor SSPA e Calibração de Fase:**
   - Sintonia de fase dos módulos amplificadores WRN311 ($\Phi_{DP} \le \pm 5^\circ$) via `Bitex` e `Ascope`.
   - Medição de potência de transmissão e pureza espectral em Banda C ($\approx 5.6\text{ GHz}$).
4. **Receptor Digital RVP10 e Calibrações:**
   - Calibração de refletividade ($Z$) com sensor térmico e rotina `zauto`.
   - Calibração polarimétrica de $Z_{DR}$ (`zdrcal` / *Birdbath scan*) e $L_{DR}$ / Alinhamento solar (`suncal`).
5. **Software IRIS, Supervisão BITE e Cibersegurança:**
   - Painel de telemetria remota `Bitex` (General, Transceiver, Antenna/Pedestal).
   - Agendamento de varreduras (`TSC Monitor`), daemons RDA (`ps_iris`) e produtos polarimétricos.
   - Diagnósticos, scripts de coleta (`collect_irisrda_logs`), backup e conformidade com **OWASP ASVS**.
6. **Matriz de Conformidade e Transição para o SAT:**
   - Matriz consolidada de aprovação do FAT.
   - Requisitos de infraestrutura e planejamento do *Site Acceptance Test* (SAT).

---

## 📚 Documentos de Referência Vaisala
- `M212986EN-C`: *Vaisala Weather Radar WRS300 (Troubleshooting, Calibration, Installation, Maintenance, Operation)*
- `M212604EN`: *RVP10 User Guide*
- `M212925EN`: *IRIS and RDA Utilities Guide*
- `M212923EN`: *RCP8 User Guide*
