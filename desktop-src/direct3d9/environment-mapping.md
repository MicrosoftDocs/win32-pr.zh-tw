---
description: 環境對應是一種在不使用光線追蹤的情況下，模擬高度反射表面的技巧。
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: " (Direct3D 9) 的環境對應"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a07d53028e200d273206f149ea12c07afa6dbc4ad47f8232e64cddf7582a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122218"
---
# <a name="environment-mapping-direct3d-9"></a> (Direct3D 9) 的環境對應

環境對應是一種在不使用光線追蹤的情況下，模擬高度反射表面的技巧。 在實務上，環境對應會套用特殊材質圖，其中包含物件周圍之場景的影像。 結果近似于反射表面的外觀，夠近一點可欺騙，而不會產生任何與光線追蹤相關的複雜計算。

下圖示范稱為球形環境對應的環境對應類型。 如需詳細資訊，請參閱 [球形環境對應](spherical-environment-mapping.md)。

![已套用材質的茶壺圖例，反映了周圍的周圍](images/spheremapped-teapot.png)

此影像中的茶壺會反映其周圍的情況;這實際上是套用至物件的材質。 由於環境對應會使用材質，並結合了特別計算的材質座標，因此可以即時執行。

本節提供有關使用 Direct3D 來執行兩個常見的環境對應類型的資訊。 在整個圖形產業中使用的環境對應有許多種，但下列主題以兩個最常見的表單為目標：三個最常見的表單：三種環境對應和球面環境對應。

-   [三次環境對應](cubic-environment-mapping.md)
-   [球形環境對應](spherical-environment-mapping.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元管線](pixel-pipeline.md)
</dt> </dl>

 

 



