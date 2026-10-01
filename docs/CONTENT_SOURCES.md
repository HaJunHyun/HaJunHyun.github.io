# Profile and PReFlow content sources

Verified on October 1, 2026.

## Profile

- [SIML people](https://siml.kaist.ac.kr/people/): Junhyun Ha, MS student, `junhyunha@kaist.ac.kr`.
- [SIML](https://siml.kaist.ac.kr/): lab name and KAIST AI affiliation.
- [Juho Lee](https://juho-lee.github.io/): advisor homepage; the advising relationship was also supplied by the site owner.
- The homepage uses Gravatar's existing `mp` (mystery-person) default avatar, a white silhouette on a gray background.
- [Avatar documentation](https://docs.gravatar.com/sdk/images/#default-image) and [image source](https://www.gravatar.com/avatar/00000000000000000000000000000000?d=mp&f=y&s=512).
- The image is stored unchanged as `assets/img/avatar-default.jpg`.

## Publication and explainer

- [arXiv abstract](https://arxiv.org/abs/2609.36812)
- [Version 1 PDF](https://arxiv.org/pdf/2609.36812v1)
- [Version 1 source](https://arxiv.org/src/2609.36812v1)
- Paper license: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- Publication status: arXiv preprint.
- Author order and spelling follow the paper: Junhyun Ha, Juho Lee, Byungwoo Park.
- The explainer is original prose based on v1. Equations follow Sections 2 and 3; results follow Section 5, Table 1, and Appendix D.
- The ideal joint optimum and the practical greedy-selection approximation are distinguished.
- Aggregate benchmark results use eight seeds for PReFlow; the displayed learning curves use three.

## Figure provenance

The original figure PDFs were rasterized directly to PNG without changing their scientific content.

| Website asset                                | arXiv source asset                   | Paper figure |
| -------------------------------------------- | ------------------------------------ | ------------ |
| `assets/img/preflow/method-result.png`       | `Figures/fig_method_result.pdf`      | 1            |
| `assets/img/publication_preview/preflow.png` | `Figures/fig_toy_qvpo.pdf`           | 2            |
| `assets/img/preflow/online-comp.png`         | `Figures/fig_online_comp.pdf`        | 3            |
| `assets/img/preflow/flowstep-cost-bars.png`  | `Figures/fig_flowstep_cost_bars.pdf` | 4            |

The post uses the stock al-folio Distill layout. The requested [TRQAM article](https://yonghdong.github.io/blog/trqam/) informed the explanatory format;
its prose, figures, and implementation were not copied.
