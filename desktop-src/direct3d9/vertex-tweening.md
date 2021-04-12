---
description: 頂點補間會將兩個使用者提供的位置混合 (或法線) 。
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: " (Direct3D 9) 的頂點補間"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a5458e384fa69b91b1eab1623fb526d514591f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187494"
---
# <a name="vertex-tweening-direct3d-9"></a> (Direct3D 9) 的頂點補間

頂點補間會將兩個使用者提供的位置混合 (或法線) 。 補間與加權的頂點混合互相排斥。 補間是在光源和裁剪之前執行，並藉由將 D3DRS \_ VERTEXBLEND 設定為 D3DVBF 補間來啟用 \_ 。 產生的頂點位置是由下列各項計算：


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



使用相同的方法來計演算法線。 如需詳細資訊，請參閱 [使用 (Direct3D 9) 的頂點補間 ](using-vertex-tweening.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[幾何混合](geometry-blending.md)
</dt> </dl>

 

 



