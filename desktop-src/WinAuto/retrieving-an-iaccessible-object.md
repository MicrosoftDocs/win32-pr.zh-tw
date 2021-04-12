---
title: 正在抓取 IAccessible 物件
description: Microsoft Active Accessibility 提供可讓用戶端取出可存取物件的 AccessibleObjectFromWindow 和 AccessibleObjectFromPoint 等功能。
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300275"
---
# <a name="retrieving-an-iaccessible-object"></a>正在抓取 IAccessible 物件

Microsoft Active Accessibility 提供可讓用戶端取出可存取物件的 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 和 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) 等功能。 這些函式會傳回 [**IDispatch**](idispatch-interface.md) 或 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標，用戶端可以透過此指標取得可存取物件的相關資訊。

當用戶端呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 或任何其他 **AccessibleObjectFrom * * * X* 函式以抓取物件的介面時，Microsoft Active Accessibility 會將 [**WM \_ GETOBJECT**](wm-getobject.md) 視窗訊息傳送至適當應用程式內適用的視窗程式。 若要提供資訊給用戶端，伺服器必須回應 **WM \_ GETOBJECT** message。

若要收集有關 UI 元素的特定資訊，用戶端必須先取得元素的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。 若要取出專案的 **IAccessible** 物件，用戶端可以使用下列其中一項功能：

-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

**若要取出 IAccessible 介面指標**

1.  用戶端會呼叫其中一個 **AccessibleObjectFrom * * * X* 函數。
2.  Oleacc.dll 將 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息傳送至伺服器。
3.  伺服器會決定哪個 UI 元素對應至要求。
4.  伺服器會傳回零以要求 Oleacc.dll proxy。

    Or

    傳回 (原生執行) 的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件。 若要這樣做，它會：

    -   為元素結構 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件。
    -   呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 來封送處理物件的指標。
    -   傳回要 Oleacc.dll 的 LRESULT。

5.  Oleacc.dll 會檢查來自 [**WM \_ GETOBJECT**](wm-getobject.md)的傳回值。

    如果為零，Oleacc.dll 會建立 proxy 物件，並將它傳回給用戶端。

    Or

    如果非零，Oleacc.dll 會呼叫 [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) 來 unmarshal 原生 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件指標，並將它傳回給用戶端。

 

 




