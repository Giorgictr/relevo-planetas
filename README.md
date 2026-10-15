# Relevo da Lua, de Marte, de Mercúrio, de Ceres, de Vesta e de Titã em ladrilhos

Dados de relevo usados pela [Viagem pelo Espaço](https://giorgictr.github.io/viagem-pelo-espaco/), gerados por
`dados/gerar_relevo.py` daquele repositório a partir dos mosaicos globais do USGS Astrogeology Science Center
(Titã: dados da Cornell):

- **Lua**: LRO LOLA LDEM 118 m (NASA/GSFC).
- **Marte**: mistura HRSC e MOLA de 200 m (Mars Express, ESA/DLR/FU Berlin; Mars Global Surveyor, NASA).
- **Mercúrio**: MESSENGER MDIS 665 m (NASA/JHUAPL/Carnegie Institution).
- **Ceres**: Dawn FC HAMO DTM 137 m (NASA/JPL-Caltech/UCLA/MPS/DLR/IDA).
- **Vesta**: Dawn FC HAMO DTM 93 m (NASA/JPL-Caltech/UCLA/MPS/DLR/IDA). A altura inclui a forma achatada do corpo.
- **Titã**: Corlies et al. (2017), relevo da Cassini RADAR (altimetria, SARTopo e estéreo) interpolado, com o detalhe
  das faixas do radar somado (Cornell eCommons, doi:10.7298/m4dv-gv95, CC0); montado por `dados/preparar_tita.py`.

Esquema de ladrilhos igual ao do NASA Trek: no nível z há 2^(z+1) × 2^z ladrilhos de 180/2^z graus.
Cada ladrilho tem 259 × 259 amostras (257 nos cantos da grade e uma de borda de cada lado), em WebP sem perdas:
altura em metros = (R·256 + G − 32768) × passo[z], com `passo` no arquivo `<corpo>.json`, que também lista
o nível global e as regiões de destaque.
