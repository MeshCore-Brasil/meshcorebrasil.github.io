# Configuração do MeshCore para o Brasil

Bem-vindo! Esta página contém os valores de referência para configurar o MeshCore no Brasil.

## Parâmetros de Rádio LoRa

| Parâmetro | Valor |
|-----------|-------|
| **Preset** | Australia: SA, WA |
| **Frequência** | 923.125 MHz |
| **Largura de Banda** | 62.5 kHz |
| **Spreading Factor (SF)** | 8 |
| **Coding Rate (CR)** | 8 |

## Como Configurar

1. Abra o MeshCore
2. Acesse as configurações de rádio
3. Selecione o preset **"Australia: SA, WA"**
4. Ajuste os parâmetros conforme a tabela acima
5. Salve e reinicie o dispositivo

## Observações Importantes

- **Frequência**: A frequência de 923.125 MHz está dentro da faixa de 915–928 MHz, permitida no Brasil para equipamentos de radiação restrita (até 1 watt) conforme regulamentação da Anatel.
- **Alcance**: Com SF 8 e banda estreita de 62.5 kHz, você terá um bom equilíbrio entre alcance e taxa de dados.
- **Interferência**: Evite canais congestionados e verifique se há outros dispositivos LoRa operando na mesma frequência na sua região.

## Recursos Úteis

- [Documentação oficial do MeshCore](https://github.com/meshtastic/firmware)
- [Mapa de nós MeshCore no Brasil](https://meshtastic.liy.app/)

---

*Última atualização: Abril 2026*
