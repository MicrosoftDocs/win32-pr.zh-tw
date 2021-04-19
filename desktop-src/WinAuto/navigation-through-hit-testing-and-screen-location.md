---
title: 流覽點擊測試和螢幕位置
description: 若要找出物件的子系，或判斷物件的大小，用戶端可以點擊螢幕上的測試點。
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967615"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a>流覽點擊測試和螢幕位置

若要找出物件的子系，或判斷物件的大小，用戶端可以點擊螢幕上的測試點。 有兩種方法可用：

-   [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible：： accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a>使用 IAccessible：： accHitTest

若要識別某個點是否在物件內、其子系內或兩者皆非，用戶端會呼叫父物件的 [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) 方法，並傳遞要進行點擊測試之點的螢幕座標。 下列清單描述一些一般案例：

-   如果物件的子系在指定點重迭， [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) 會抓取以視覺化方式呈現空間的最上層子系。
-   如果視窗涵蓋子系，或如果父代已裁剪子系，則點擊測試會抓取子系，即使看不到子系也是一樣。
-   如果在指定點找到的子系是可存取的物件，而不是子項目，則方法會傳回子系的 [**IDispatch**](idispatch-interface.md) 介面。

## <a name="using-iaccessibleacclocation"></a>使用 IAccessible：： accLocation

若要取得物件或其中一個物件子系的螢幕位置，用戶端會呼叫 [**IAccessible：： accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)。 這個方法會傳回指定物件之周框的座標。 如果物件不像矩形，則方法會傳回包含整個物件的最小矩形座標。

下圖說明非矩形物件的區域和其週框之間的關聯性。

![圖例顯示非矩形物件的區域 (圓形) 和其周框。](images/region.gif)

> [!Note]  
> [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) 比 [**IAccessible：： accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) 更為精確，因為它可讓用戶端以圖元為單位來決定物件的位置，而不是使用周框矩形。 此精確度很有用，例如，當應用程式透過追蹤滑鼠指標的位置來收集資訊時。

 

 

 




