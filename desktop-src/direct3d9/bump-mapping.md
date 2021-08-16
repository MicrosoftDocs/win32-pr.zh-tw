---
description: 凹凸對應是一種特殊形式的反射或擴散環境對應，可模擬精確鑲嵌物件的反映，而不需要極高的多邊形計數。
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: " (Direct3D 9) 的凹凸對應"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb10a3a01ff3b7989cd7c44f95d6980cb08a86c00b3e9a0fc02173e349d4968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805825"
---
# <a name="bump-mapping-direct3d-9"></a> (Direct3D 9) 的凹凸對應

凹凸對應是一種特殊形式的反射或擴散環境對應，可模擬精確鑲嵌物件的反映，而不需要極高的多邊形計數。 Direct3D 所執行的自動調整對應可以精確描述為反射或擴散環境對應的每個圖元材質座標更動，因為您會在差異值方面提供有關放大圖分佈的資訊，而系統會將該值套用至下一個材質階段中環境對應的您和 v 材質座標。 Delta 值是以 [凹凸地圖介面] 的像素格式來編碼 (請參閱 [放大 [地圖像素格式](bump-map-pixel-formats.md) ]) 。

凹凸對應依賴于混合多重紋理。 這表示裝置必須至少支援兩個混合階段;一個用於凹凸地圖，另一個用於環境對應。 至少需要三個材質混合階段，才能套用額外的基底材質圖，也就是最常見的情況。 下圖顯示材質混合串聯中的基底材質、凹凸地圖和環境地圖之間的關聯性。

![材質混色 cascade 的圖表](images/bumpmap-tcascade.png)

您必須適當地備妥紋理階段，才能啟用凹凸對應。 下列主題將介紹「進行」對應，並提供如何在應用程式中使用它的詳細資料：

-   [凹凸地圖像素格式](bump-map-pixel-formats.md)
-   [凹凸對應公式](bump-mapping-formulas.md)
-   [使用凹凸對應](using-bump-mapping.md)

Direct3D 原本就不支援高度對應;它們只是方便的格式，可用於儲存和視覺化分佈資料。 您的應用程式可以儲存任何格式的輪廓資訊，甚至產生程式性的放大地圖。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元管線](pixel-pipeline.md)
</dt> </dl>

 

 



