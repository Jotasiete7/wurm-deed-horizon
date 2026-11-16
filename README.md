# Wurm Deed Horizon

Gerenciador local e offline-first de **upkeep** para assentamentos (*deeds*) do **Wurm Online**, com leitura automática de *Settlement Billboards* por texto ou imagem (OCR), projeção em tempo real do cofre e planejador de depósitos.

> **100% Local & Privado:** Todos os dados ficam salvos apenas no `localStorage` do seu navegador. Nenhuma informação das suas deeds é enviada para servidores externos.

---

## Como usar

1. Baixe o repositório ou clone na sua máquina.
2. Dê um clique duplo em `Abrir-Deed-Tracker.bat` (ou abra `Deed-Horizon.html` diretamente no navegador).
3. No Wurm Online, abra o **Settlement Billboard** da sua deed:
   - Tire um recorte da janela (`Win + Shift + S`) e pressione **`Ctrl + V`** em qualquer lugar da página (o OCR lê automaticamente via Tesseract.js), **ou**
   - Arraste uma imagem do billboard para a janela, **ou**
   - Cole o texto do billboard na aba **Billboard** do painel lateral.

Se quiser explorar a interface antes de adicionar suas deeds, clique em **"Testar com exemplo"** na tela inicial para carregar dados fictícios de demonstração.

---

## Principais Recursos

- **Trilha de Horizonte**: linha do tempo visual mostrando a proximidade do vencimento de cada deed em relação à meta configurável (padrão `195d`).
- **Cofre Estimado em Tempo Real**: calcula quanto já foi consumido desde o último print/snapshot e separa o valor em **chips**.
- **Depósito Rápido & Desfazer**: registre depósitos de moedas (`g/s/c/i`) com atualização instantânea de dias restantes e histórico com opção de desfazer.
- **Planejador de Orçamento (*Water-Filling*)**: informe quanto de prata/ouro você tem disponível e o algoritmo distribui as moedas priorizando as deeds mais próximas de vencer para equilibrar o horizonte.
- **Organização & Alertas**:
  - Filtros por **Todas**, **Minhas**, **Parceiros** e **Abaixo da meta**.
  - Alerta visual para deeds com **Tile per Creature Ratio** abaixo de `15.0`.
  - Exportação de lembrete de vencimento para agenda (`.ics`).
  - Idioma alternável (`PT` / `EN`) e meta de dias editável no menu `⋯`.

---

## Estrutura de Arquivos

- `Deed-Horizon.html` — Aplicação principal (interface Matte Carbon & Swiss Grid, zero dependências de build).
- `Abrir-Deed-Tracker.bat` — Atalho para abrir o painel no navegador padrão (Windows).
- `.gitignore` — Protege pastas de dados locais (`meus_dados/`) e backups `.json` caso você versione melhorias no seu fork.

### Dica de Backup & Snapshot Local

Pelo menu **`⋯`** no canto superior direito você pode:
- **Exportar / Importar backup (`.json`)** para guardar suas deeds ou migrar de navegador/PC.
- **Exportar snapshot local (`.js`)**: salva um arquivo `minhas_deeds.js`. Se você colocá-lo em `meus_dados/minhas_deeds.js` (pasta ignorada pelo `.gitignore`), o `Deed-Horizon.html` carrega suas deeds automaticamente como seed inicial mesmo se o cache do navegador for limpo.
