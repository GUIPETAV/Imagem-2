# Conversão de RGB para Escala de Cinza
No processamento de imagens RGB, cada pixel possui 3 canais de cores: Vermelho (R), Verde (G) e Azul (B), com valores de 0 a 255.

## Método `convert('L')`

O método `imagem.convert('L')` da biblioteca Pillow converte imagens RGB para escala de cinza usando a fórmula:

```python
L = R * 0.299 + G * 0.587 + B * 0.114
```

## Exemplos de Conversão

| Pixel RGB        | Cálculo                                      | Valor L |
|-----------------|---------------------------------------------|---------|
| RGB(255, 0, 0)  | 255 * 0.299 + 0 * 0.587 + 0 * 0.114 = 76  | 76      |
| RGB(0, 255, 0)  | 0 * 0.299 + 255 * 0.587 + 0 * 0.114 = 150 | 150     |
| RGB(0, 0, 255)  | 0 * 0.299 + 0 * 0.587 + 255 * 0.114 = 29  | 29      |

## Pesos e Percepção

Os pesos utilizados são baseados na sensibilidade do olho humano:
- Verde: 0.587 (mais sensível)
- Vermelho: 0.299 (sensibilidade média)
- Azul: 0.114 (menos sensível)

## Resultado
- Cada pixel da imagem resultante possui um único valor
- Escala varia de 0 (preto) a 255 (branco)
- Representa diferentes níveis de intensidade de cinza
