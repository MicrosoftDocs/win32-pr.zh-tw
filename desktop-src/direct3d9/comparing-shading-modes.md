---
description: 在平面陰影模式中，會顯示下列金字塔與相鄰臉部之間的尖邊緣。 不過，在 Gouraud 網底模式中，會在邊緣插入網底值，最後的外觀會是曲線表面。
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: 比較 (Direct3D 9) 的陰影模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df53df2751dc184cbb8246f47a56fbb2b3320e96432b664524a2e30018adc15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911648"
---
# <a name="comparing-shading-modes-direct3d-9"></a>比較 (Direct3D 9) 的陰影模式

在平面陰影模式中，會顯示下列金字塔與相鄰臉部之間的尖邊緣。 不過，在 Gouraud 網底模式中，會在邊緣插入網底值，最後的外觀會是曲線表面。

![金字塔的圖，其中包含指向臉部法線的尖邊和箭號](images/shade2.png)

Gouraud 陰影燈的平面表面比一般陰影更真實。 一般陰影模式中的臉部是一致的色彩，但 Gouraud 陰影可讓光線更正確地落在表面上。 如果有鄰近的點來源，此效果特別明顯。

Gouraud 陰影會平滑化多邊形之間的尖邊（以平面陰影顯示）。 不過，它可能會導致符合的波段，也就是不會在相鄰多邊形間順暢地混合的色彩或淺色的區段。 您的應用程式可以藉由增加物件中的多邊形數目、增加螢幕解析度或增加應用程式的色彩深度，來減少符合區的外觀。

Gouraud 陰影可能會遺漏一些詳細資料。 例如，在下圖中，焦點會完全包含在多邊形臉部內。

![多邊形臉部內的焦點圖例](images/gouraud.png)

在此情況下，Gouraud 陰影會在頂點之間進行插補，這會完全遺漏焦點;臉部會轉譯成焦點不存在。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[陰影](shading.md)
</dt> </dl>

 

 



