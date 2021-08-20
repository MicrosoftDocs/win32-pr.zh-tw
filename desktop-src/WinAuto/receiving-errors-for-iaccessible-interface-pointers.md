---
title: 接收 IAccessible 介面指標的錯誤
description: 本主題說明您可能會收到 IAccessible 介面指標錯誤的情況。
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d36a29c688966526d5431e1fe2f643e39b378779d122d22f38dea2089a5191c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115139"
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

 

 




