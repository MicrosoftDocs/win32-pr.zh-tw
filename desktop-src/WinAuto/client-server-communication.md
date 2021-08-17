---
title: 用戶端/伺服器通訊
description: WinEvents 機制提供一種方式，讓伺服器能夠輕鬆與 Microsoft Active Accessibility 用戶端進行通訊。
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896b6f6688e0e2929ebb351fe9d7cc210803768a8031faa44a8aca8127b12002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133931"
---
# <a name="clientserver-communication"></a>用戶端/伺服器通訊

[WinEvents](winevents-overview.md)機制提供一種方式，讓伺服器能夠輕鬆與 Microsoft Active Accessibility 用戶端進行通訊。 用戶端通常會藉由回應 WinEvents (來收集資訊，例如，遵循焦點) ，但是隨時都可自由地從伺服器要求資訊。

若要要求產生 New-winevent 之可存取物件的資訊，用戶端必須處理事件，並使用相關的可存取物件建立連接。 若要這樣做，用戶端會執行下列六個步驟：

-   伺服器會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) ，以針對其使用者介面元素的每個變更產生 new-winevent 通知。
-   使用者中的 New-winevent 管理程式碼會判斷是否有任何用戶端應用程式使用 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) [*註冊 new-winevent 攔截*](/windows/desktop/api/Winuser/nc-winuser-wineventproc)函式，並呼叫已註冊的回呼函式。
-   在其回呼函式中，用戶端會藉由呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) 或其他可存取的物件抓取函式，要求存取產生事件的物件。 如需詳細資訊，請參閱 [取出 IAccessible 物件](retrieving-an-iaccessible-object.md)。
-   此 Microsoft Active Accessibility API 會將一個 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息傳送給伺服器應用程式，以抓取可存取的物件。
-   為了回應 [**WM \_ GETOBJECT**](wm-getobject.md)，伺服器應用程式會傳回零或傳回值，作為產生事件之物件的一次性參考。
-   如果伺服器傳回零，Microsoft Active Accessibility 會建立 proxy 物件，並將其位址提供給用戶端。 否則，Microsoft Active Accessibility 會使用這個參考來取出物件介面（例如 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 或 [**IDispatch**](idispatch-interface.md)）的位址，並將該位址提供給用戶端。

一旦用戶端有介面位址之後，就可以呼叫可存取物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法，以取得資訊。

## <a name="in-this-section"></a>本節內容

-   [WinEvents 和 Active Accessibility](winevents-overview.md)
-   [WM \_ GETOBJECT 的運作方式](how-wm-getobject-works.md)
-   [正在抓取 IAccessible 物件](retrieving-an-iaccessible-object.md)

 

 




