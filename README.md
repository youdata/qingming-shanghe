# 清明上河图 · Along the River during the Qingming Festival

张择端《清明上河图》（北京故宫博物院藏） — a narrated deep-zoom tour (in English), as a static page.

Zhang Zeduan's handscroll of the Northern Song capital (ink and light colour on silk, 24.8 × 528.7 cm, Palace Museum, Beijing), read from right to left: the countryside, the grain boats, the Rainbow Bridge, the streets, the city gate and the shops inside the walls, and the seals at the end. The whole scan is one canvas (121,531 × 5,457 px, the mounting and seals included), with a guided tour of 20 saved views.

Live: https://youdata.github.io/qingming-shanghe/
Chinese version: https://youdata.github.io/qingming-shanghe-zh/ (it reads this site's tiles).

The image pyramid is a tile folder (`qingming/`: `header.idx` + `{z}/{x}/{y}.png`), so any static host serves it. Its fonts are in `fonts/`, trimmed to the page's characters. The narrated video is not included.

## How it is made

From `infographic-examples/qingming-documentary/build.mjs`, with rx (`~/rx-cli`):

```sh
node build.mjs                                                     # → qingming-documentary.json
rx export qingming-documentary.json --out site --app /rx-graphic-editor/web/index.html --canvas --lock-layers --tiles dir
rx publish site --to github:youdata/qingming-shanghe --yes
```
