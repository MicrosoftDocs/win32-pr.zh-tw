---
title: 接收 IAccessible 介面指標的錯誤
description: 本主題說明您可能會收到 IAccessible 介面指標錯誤的情況。
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d3bd9e39dae9c5de9ad1644e5955bd5fb90d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840431"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a>接收 IAccessible 介面指標的錯誤

本主題說明您可能會收到 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標錯誤的情況。 當使用者關閉物件所屬的應用程式，或是使用者透過使用者介面關閉控制項時， **IAccessible** 函式可能會傳回 **IAccessible** 介面指標的錯誤。

## <a name="user-closes-an-application"></a>使用者關閉應用程式

如果使用者關閉包含 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標指向之物件的應用程式，則未來對該物件的所有呼叫都會傳回錯誤碼。 錯誤（如 **共同 \_ 電子 \_ OBJNOTCONNECTED**）將會指出物件不再存在。 這適用于所有 **IAccessible** 介面指標。

## <a name="user-dismisses-a-control"></a>使用者關閉控制項

如果使用者關閉控制項 (例如，按下按下按鈕) ，用戶端仍然可以在此物件上呼叫 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法和屬性，因為物件尚未釋放。 不過，未來的呼叫將會收到錯誤訊息。

這種情況適用于下列函數和方法：

-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**IAccessible：： get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**IAccessible：： get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




