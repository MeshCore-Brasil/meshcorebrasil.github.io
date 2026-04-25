Somos uma iniciativa comunitária para estabelecer uma rede de comunicação descentralizada baseada no protocolo [MeshCore](https://meshcore.io), uma rede que não exige licença e **não depende da Internet**. Utilizamos transmissores LoRa (Long Range), que são de baixo custo e fácil acesso, na faixa de radiação restrita de 915 a 928 MHz.

Esta página tem como objetivo servir a comunidade com configurações de referência e ferramentas úteis.

## Configuração Recomendada

| Parâmetro | Valor |
|-----------|-------|
| **Preset** | Australia: SA, WA |
| **Frequência** | 923.125 MHz |
| **Largura de Banda** | 62.5 kHz |
| **Spreading Factor (SF)** | 8 |
| **Coding Rate (CR)** | 8 |

Para usar essas configurações:

1. Abre o aplicativo MeshCore (se estiver usando celular) ou o [cliente web](https://app.meshcore.nz/) (se estiver usando o computador).
2. Clique no ícone ⚙️ na barra superior.
3. Em **Radio Settings**, clique em **Choose Preset** e selecione **"Australia: SA, WA"**.
4. Verifique se os parâmetros estão conforme a tabela acima.
5. Clique no ícone ✔ no canto superior direito da tela.

## Nosso Canal no Telegram

Entre no nosso grupo do Telegram, **[@MeshCoreBrasil](https://t.me/meshcorebrasil)**. Ali você pode:

- 💬 Tirar dúvidas com outros usuários
- 🗺️ Mapear nós da sua região
- 📢 Receber atualizações e avisos
- 🤝 Fazer contatos locais

## Ferramentas

### Mapas e Análise de Tráfego

- [Map MeshCore.io](https://map.meshcore.io/?zoom=5&lat=-14.8600&lon=-57.1289): Mapa oficial do MeshCore. Necessita que os dispositivos sejam adicionados manualmente.
- [Let's Mesh Analyzer](https://analyzer.letsmesh.net/packets?region=GRU,SOD): Mapa e analisador de pacotes em tempo real. Centrado na região de São Paulo, mas pode ser configurado para mostrar outras regiões.
- [MeshMapper](https://www.meshmapper.net/): Ferramenta de _wardriving_, cujo app pode ser usado no carro para descobrir repetidoras enquanto se dirige.

### Análise de visadas e relevo

- [Radio Mobile Online](https://www.ve2dbe.com/rmonline_s.asp): Ferramenta consagrada entre os radioamadores para análise de conectividade, cobertura, entre outras utilidades. Criada por Roger Coudé (VE2DBE).
- [Elevation Finder](https://droidgren.github.io/elevation_finder/): Mostra os pontos mais altos numa determinada região.
- [Rservis](https://nbp.rservis.net/): Calculadora de visada, exibe também Zona de Fresnel para frequência escolhida.
- [Solwise Elevation Tool](https://www.solwise.co.uk/wireless-elevationtool.html): Outra calculadora de visada. Fácil de usar e com perfis claros.

### Normalizador de Nomes para Repetidoras

Este formulário ajuda a gerar nomes padronizados para repetidoras MeshCore seguindo a convenção estabelecida pela rede.

<form class="repeater-form">
    <div class="form-group">
        <label for="city-name">
            <strong>Nome da Cidade</strong>
        </label>
        <input type="text" id="city-name" 
               placeholder="Ex: Sorocaba, São Paulo, Campinas..."
               autocomplete="off">
        <span class="form-hint">Digite o nome completo da cidade. A abreviação será gerada automaticamente.</span>
        <div class="abbreviation-display">
            <span class="abbreviation-label">Abreviação:</span>
            <span id="city-abbreviation" class="abbreviation-value">---</span>
        </div>
    </div>
    
    <div class="form-group">
        <label for="regional-id">
            <strong>Identificador Regional</strong> (bairro ou referência)
        </label>
        <input type="text" id="regional-id" 
               placeholder="Ex: Centro, VilaNova, Itapecerica"
               autocomplete="off">
        <span class="form-hint">Nome do bairro, região ou ponto de referência. Palavras juntas com iniciais maiúsculas (ex: VilaNova)</span>
    </div>
    
    <div class="form-group">
        <label for="pubkey">
            <strong>Public Key do Dispositivo</strong> (primeiros 4 dígitos)
        </label>
        <input type="text" id="pubkey" 
               placeholder="Ex: A1B2"
               maxlength="4"
               autocomplete="off"
               value="1234">
        <span class="form-hint">Encontre no app Meshtastic em: Configurações → LoRa Radio → Public Key</span>
    </div>
    
    <div class="form-buttons">
        <button type="button" id="generate-btn" class="md-button md-button--primary">
            Gerar Nome
        </button>
        <button type="button" id="reset-btn" class="md-button">
            Limpar
        </button>
    </div>
</form>

<div id="error-message" class="error-box" style="display: none;"></div>

<div id="result" class="result-box" style="display: none;">
    <h3>Nome Gerado</h3>
    <div class="generated-name-container">
        <span id="generated-name" class="generated-name"></span>
        <button type="button" id="copy-btn" class="copy-button" title="Copiar para área de transferência">
            📋 Copiar
        </button>
    </div>
</div>

Os nomes das repetidoras seguem o formato:

```
<CIDADE>-<REGIONAL>-<PUBKEY>
```

Onde:

- **CIDADE**: Abreviação de **3 letras maiúsculas** da cidade (gerada automaticamente)
- **REGIONAL**: Identificador regional como bairro, ponto de referência ou localidade (maiúsculo)
- **PUBKEY**: Primeiros **4 dígitos** da chave pública (public key) do dispositivo em hexadecimal (maiúsculo)

Exemplos:

| Nome | Descrição |
|------|-----------|
| `SOR-SAOBENTO-A1B2` | Repetidora no mosteiro São Bento de Sorocaba |
| `SAO-PAULISTA-9D4E` | Repetidora na Paulista, São Paulo |
| `SBC-VILANOVA-3C7D` | Repetidora na Vila Nova, São Paulo |



---

*Última atualização: Abril 2026*
