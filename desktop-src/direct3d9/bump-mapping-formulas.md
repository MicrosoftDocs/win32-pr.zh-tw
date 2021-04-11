---
description: Direct3D 會將下列公式套用至每個放大地圖圖元中的 DU 和 DV 元件。
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: " (Direct3D 9) 的凹凸對應公式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436aee9689d78b8b706bb98d908f2e3fbc05ca6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111664"
---
# <a name="bump-mapping-formulas-direct3d-9"></a> (Direct3D 9) 的凹凸對應公式

Direct3D 會在每個放大地圖圖元中，將下列公式套用至 D<sub>U</sub> 和 d<sub>V</sub> 元件。

![凹凸對應矩陣轉換的公式](images/dudv-transform.png)

在這些公式中，D<sub>u</sub> 和 d<sub>V</sub> 變數會直接從凹凸地圖圖元中取得，並以2x2 矩陣進行轉換，以產生輸出 delta 值 D<sub>U</sub>' 和 d<sub>v</sub>'。 系統會使用輸出值來修改在下一個材質階段中處理環境對應的材質座標。 轉換矩陣的係數是透過 D3DTSS \_ BUMPENVMAT00、D3DTSS \_ BUMPENVMAT10、D3DTSS \_ BUMPENVMAT01 和 D3DTSS \_ BUMPENVMAT11 材質階段狀態來設定。

除了「您」和「v delta」值之外，系統也可以計算用來在下一個混色階段 lambert 環境地圖色彩的亮度值，如下列公式所示。

![輸出亮度的公式，從縮放因數和位移計算](images/l-transform.png)

在此公式中，L ' 是要計算的輸出亮度。 L 變數是從凹凸地圖圖元取得的亮度值，會乘以縮放因數、S，以及變數 O 中的值位移。D3DTSS \_ BUMPENVLSCALE 和 D3DTSS \_ BUMPENVLOFFSET 材質階段狀態會控制公式中 S 和 O 變數的值。 此公式僅適用于包含 [凹凸對應] 之階段的材質混合作業設定為 [D3DTOP BUMPENVMAPLUMINANCE] 時 \_ 。 使用 D3DTOP \_ BUMPENVMAP 時，系統會針對 L ' 使用1.0 的值。

計算輸出 delta 值 D<sub>U</sub>' 和 D<sub>V</sub>' 之後，系統會將它們新增至下一個材質階段中的材質座標，並依亮度 modulates 所選的色彩，以產生套用至多邊形的色彩。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[凹凸對應](bump-mapping.md)
</dt> </dl>

 

 



