# PS5 HDMI Converter — Conversor HDMI PS5

Utilitário de bancada para **converter o tipo de HDMI gravado na NOR do PS5**
entre **Realtek**, **Panasonic** e **Nuvoton**, recalculando o checksum do bloco
para o console não bipar.

> Programa de bancada para técnicos.

**Software e finalização do offset por Felipe Calmon (InfinityGames).**
**Estudos do Offset do HDMI do PS5: TXD Games e Thiago Max.**

O programa funciona em **três idiomas — Português, English e Español** — com
troca de idioma **na hora**, e faz **leitura e gravação da NOR** direto pelo
RP2040.

![Conversor HDMI PS5](docs/screenshot.png)

---

## O que o programa faz

- **Três idiomas:** Português, English e Español, selecionáveis na hora pelo
  menu no topo.
- **Lê e grava a NOR** do PS5 direto por um **RP2040** (Raspberry Pi Pico /
  Pico Zero) — além de abrir/salvar arquivo `.bin`.
- Reconhece o tipo de HDMI na NOR (**Realtek / Panasonic / Nuvoton**) e
  **converte** entre eles.
- **Recalcula o checksum** do bloco HDMI — sem isso, o console bipa / não dá
  vídeo.
- Aceita **somente NOR de PS5** (W25Q16, 2 MB); valida o dump e **mostra a
  identidade da placa** (modelo, serial, SKU, MAC LAN/WiFi/Bluetooth, SOCUID,
  firmware, slot ativo) para você confirmar que leu certo.
- **Não altera identidade** (MAC, serial, SOCUID) **nem o módulo WiFi** — mexe
  só no setor do HDMI.
- **Grava o firmware no RP2040** (modo BOOTSEL) e mostra o **diagrama de
  ligação** dos fios — tudo dentro do programa.
- Interface escura, simples, feita para bancada.

## Download

Baixe o executável mais recente na aba **[Releases](../../releases)**.
Não precisa instalar — é só abrir.

### Como usar (resumo)

1. Escolha a fonte: abra um `.bin` de 2 MB **ou** leia o chip pelo RP2040.
2. Confira a **identidade da placa** que aparece na tela.
3. Converta para o tipo desejado. **O tipo tem que casar com o hardware** — o CI
   físico da placa ou o interposer que estiver instalado.
4. Salve o `.bin` ou grave de volta na NOR.

## Créditos

- **Estudos do HDMI do PS5:** **TXD Games** e **Thiago Max**.
- **Software e finalização do offset:** **Felipe Calmon** — InfinityGames.

**Onde comprar o Interposer Realtek:** <https://infinitygames.com.br/realtek/>

## Aviso

Ferramenta de bancada — use por sua conta e risco. O tipo de HDMI declarado
precisa corresponder ao CI físico (ou ao interposer) da placa, senão o console
não dá vídeo.

---

© 2026 Felipe Calmon — InfinityGames. Todos os direitos reservados.
