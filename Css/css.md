# CSS

## Seletores

- Universal:

        * {
            // aplica estilos a todos os elementos da pagina
        }
---
## Propriedades:
    
- font-family: ("Nova fonte"), (caso indisponível usar esta)

        font-family: "Lato", sans-serif;


- background-image: (imagem), (imagem abaixo), (imagem abaixo)...

    - Linear-gradient: (opcional: direcionamento), (cor inicial), (próxima cor)...


            background-image: linear-gradient(
                to right bottom,
                rgba(126, 213, 111, 0.8),
                rgba(40, 180, 131, 0.8)
            ), url(../img/hero.jpg);

- clip-path: (poligon)
    - poligon: (coordenadas dos pontos de corte)

            //Mais exemplos em: bennettfeely.com/clippy
            clip-path: polygon(0 0, 100% 0, 100% 75vh, 0 100%);
---    
### Categorias de Propriedades:

- fontes:
    
    | Propriedade | Descrição          |
    |-------------|--------------------|
    | font-family | tipo de fonte      |
    | font-weight | espessura da fonte |
    | font-size   | tamanho da fonte   |
    | line-height | altura da fonte    |
    | color       | cor da fonte       |

- backgound:
    
    | Propriedade         | Descrição                   |
    |---------------------|-----------------------------|
    | background-image    | imagem de fundo             |
    | background-size     | tamanho do fundo            |
    | background-position | ponto de ancoragem do fundo |

---
### Unidades de grandeza:

- Absolutas

    | Unidade | Descrição    |
    |---------|--------------|
    | px      | pixels       |

- Relativas

    | Unidade | Descrição                | Fator          |
    |---------|--------------------------|----------------|
    | em      | tamanho do elemento      | multiplicativo |
    | rem     | tamanho do elemento raiz | multiplicativo |
    | vh      | altura da viewport       | percentual     |
    | vw      | largura da viewport      | percentual     |
    | %       | relativo ao elemento pai | percentual     |
    | cover   | cobre toda a viewport    | -------------- |

