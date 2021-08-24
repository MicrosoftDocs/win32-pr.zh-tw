---
title: WinEvents 和 Active Accessibility 總覽
description: Microsoft Active Accessibility 伺服器會引發 WinEvents，以便在可存取的物件變更時通知用戶端。
ms.assetid: a2d486ee-84ef-4c44-a832-dbc0dae81542
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95507ff1b6cd56451dd7f9acc04014c6013a7179d536565b3518bccb9137e689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052176"
---
# <a name="winevents-and-active-accessibility"></a>WinEvents 和 Active Accessibility

Microsoft Active Accessibility 伺服器會引發 *WinEvents* ，以便在可存取的物件變更時通知用戶端。 在許多情況中，伺服器會通知用戶端有變更。 Microsoft Active Accessibility 所定義的每個 [事件常數](event-constants.md) 都會描述用戶端收到通知的條件。 例如，WinEvents 可能會發出信號：

- 建立或終結物件時。
- 當物件接收或失去焦點時。
- 當物件的狀態或位置變更時。
- 當物件的任何屬性變更時。

用戶端應用程式不會自動接收事件通知;他們必須藉由呼叫 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) 函式來指定想要接收的事件。 使用 **SetWinEventHook** 時，用戶端會註冊以接收一或多個事件，並設定攔截函式來處理指定的事件。 用戶端可以使用相同的攔截函式來處理多種類型的事件，也可以使用 multipe 攔截函式。 用戶端會針對每個需要註冊的攔截函式呼叫 **SetWinEventHook** 一次。

攔截函式位於用戶端的程式碼主體內、對應至用戶端進程的 DLL 中，或對應至伺服器進程的 DLL 中。 這兩種方法都有其優點和缺點。 如需詳細資訊，請參閱內部 [內容和跨內容](in-context-and-out-of-context-hook-functions.md)攔截函式。

若要通知用戶端發生事件，伺服器會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)。 系統會檢查是否有任何用戶端應用程式已設定事件的攔截函式，並視需要呼叫適當的攔截函式。

呼叫用戶端的攔截函式時，它會接收許多描述事件的參數，以及產生事件的物件。 為了取得產生事件之物件的存取權，用戶端攔截函式會呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)。

> [!NOTE]
> 如果沒有任何用戶端註冊接收 WinEvents，則對伺服器呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 的效能影響可說是微不足道。
>
> 伺服器只會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) ，以便在自己的可存取物件中進行變更;它們不會針對系統提供的使用者介面元素中的變更呼叫 **NotifyWinEvent** 。

## <a name="event-driven-communication"></a>Event-Driven 通訊

用戶端必須先註冊 New-winevent 勾點，才能接收 New-winevent 通知。 為了避免不必要的回呼並提高效能，建議用戶端只註冊所需接收的事件。

在攔截程式中，用戶端可以呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) ，以針對套用事件的元素抓取 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件。 使用這個物件，用戶端就可以開始呼叫 **IAccessible** 方法，以抓取資訊或與 UI 元素互動。

## <a name="related-topics"></a>相關主題

[WinEvents](winevents-infrastructure.md)
