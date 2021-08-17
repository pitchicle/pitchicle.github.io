---
layout: post
title: 'CBB Staining의 원리'
author: kwanghyuck.jung
comments: true
date: 2021-08-15 12:05
use_math: true
tags: [biology,molecular-biology]
---

**CBB Staining의 원리** - 32기 정광혁



CBB staining은 단백질 전기영동 과정인 SDS-PAGE 과정의 일부로, 염색약을 투입해 염색시키는 과정을 말합니다. 이 글에서는 SDS-PAGE에서 자세히 다루지 않았던 CBB staining과 Destaining에 대해 알아보고자 합니다.



**1. CBB(Coomassie Brilliant Blue)란?**

CBB는 Coomassie Brilliant Blue의 약자로, 단백질을 고정하는 데 사용되는 염색약입니다. 이 물질의 구조식은 오른쪽 그림과 같습니다. CBB는 두 가지 종류로 나뉩니다. Coomassie Brilliant Blue G-250과 Coomassie Brilliant Blue R-250입니다. 아래 그림에서 왼쪽에 위치한 물질은 G-250, 오른쪽에 위치한 물질은 R-250입니다. R-250에 두 개의 메틸기(-CH3)를 더하면 G-250의 구조와 같게 됩니다.

두 염색약의 색은 용액의 산성도에 의해 좌우됩니다. 0보다 작은 pH를 갖는 용액에서 용액은 465nm의 최대 흡수 파장(λmax)을 갖는 붉은색을 띠게 됩니다. pH가 1에 가까울 때 염료는 620nm의 최대 흡수 파장을 가지며 초록색을 띱니다. pH가 2 이상일 때는 최대 흡수 파장 595nm를 가지며 하늘색으로 변합니다.

염색약의 색이 달라지는 현상은 염료 분자가 갖는 서로 다른 전하량 때문입니다. 붉은색을 띨 때 세 개의 질소 원자는 모두 양전하를 가집니다. 이 경우 분자는 +1가의 양이온이 됩니다. 초록색을 띨 때는 Diphenylamine에 결합한 질소 원자 하나만이 양전하를 가져서 알짜 전하량이 0인 상태입니다. 파란색을 띠는 경우 분자는 –1가의 음이온입니다.

CBB는 단백질의 아미노기, 카르복실기와 정전기적 인력으로 결합하여 단백질-염료 복합체(protein-dye complex)를 형성합니다. 생성된 단백질-염료 복합체는 파란색 계열의 음전하를 띠는 분자들이 산성 환경에서도 안정적으로 존재할 수 있도록 합니다.

![]()![image-20210815000412603](C:\Users\정광혁\AppData\Roaming\Typora\typora-user-images\image-20210815000412603.png)

**2. SDS-PAGE에서 CBB Staining**

전기영동을 모두 마치고 나면 겔을 증류수로 세척(washing)한 다음 겔에 Staining Solution을 첨가하여 염색을 시작하게 됩니다. Staining Solution에는 메탄올(Methanol)과 아세트산(Acetic acid), 그리고 CBB-G250이 포함되어 있습니다.

음전하를 가지는 CBB-G250은 단백질과 복합체를 형성하여 단백질에 음전하를 기여하게 됩니다. 이때 CBB가 염료로 작용할 수 있는 것은 CBB가 단백질을 구성하는 일부 아미노산과 결합하기 때문입니다. Arg, Lys와는 정전기적인 인력을, Trp, Tyr, His, Phe과는 소수성 결합을 이룹니다. 그 결과 CBB는 단백질과 비특이적으로 결합을 형성하게 됩니다.

Staining Solution에 포함된 메탄올과 아세트산의 첨가는 단백질의 소수성 부분을 노출하게 해 염료와 상호작용할 수 있게끔 단백질을 변성시킵니다. 이 과정에서 SDS는 빠르게 제거됩니다.

 오직 메탄올만을 첨가했을 때도 단백질은 염료에 고정될 수 있습니다. 그러나 이 과정은 아세트산이 포함되었을 때보다 오래 걸리게 됩니다. 아세트산이 존재하는 조건에서 많은 단백질들은 등전점(pI) 아래에 위치하게 되어 아르지닌, 라이신, 아미노 말단 등은 양전하를 띠게 됩니다. 이는 단백질 전체의 양전하에 기여하고, CBB와 같은 염료에 대한 결합을 촉진합니다. 염료들은 음전하성 계면활성제이기에, 단백질의 양전하와 상호작용이 발생하게 됩니다.



**3. SDS-PAGE에서의 Destaining**

 탈염(Destaining) 과정은 염색한 겔을 증류수로 세척한 후 여기에 Destaining Solution을 투입하여 이루어지게 됩니다. Destaining Solution은 Staining Solution과 아주 유사하게 Methanol과 Acetic Acid만으로 이루어져 있습니다. 단백질이 아닌 곳에서는 염료의 결합이 발생하지 않기 때문에 남은 염료들을 Destaining Solution에 용해해 제거하면 됩니다.



**4. 참고 문헌**

\- 제목 이미지 출처 : Differential induction of allergy responses by low molecular weight wheat proteins from six wheat cultivars - Scientific Figure on ResearchGate. Available from: https://www.researchgate.net/figure/SDS-PAGE-of-crude-wheat-antigens-Coomassie-brilliant-blue-staining-of-proteins-from-hard_fig1_315719741 [accessed 28 Feb, 2021]

\- https://pubmed.ncbi.nlm.nih.gov/30097924/ (The Roles of Acetic Acid and Methanol During Fixing and Staining Proteins in an SDS-Polyacrylamide Electrophoresis Gel)

\- 사진 자료는 위키백과의 Coomassie Blue 항목을 참조하였습니다.