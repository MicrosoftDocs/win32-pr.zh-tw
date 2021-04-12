---
title: 防止在攔截函式中重新進入
description: 當攔截函式處理事件時，可能會觸發其他事件，這可能會導致攔截函式在原始事件的處理完成前重新輸入。
ms.assetid: 2382e7a4-82df-423a-8479-66e28baf8105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e2b0dc6f8951bf48ce3fecabd3a81bd345388d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376236"
---
# <a name="guarding-against-reentrancy-in-hook-functions"></a>防止在攔截函式中重新進入

當攔截函式處理事件時，可能會觸發其他事件，這可能會導致攔截函式在原始事件的處理完成前重新輸入。 在攔截函式中重新進入的問題是，除非攔截函式處理這種情況，否則不會順序完成事件。

例如，假設螢幕讀取程式中的攔截函式正在處理編輯控制項的 [**事件 \_ 物件 \_ VALUECHANGE**](event-constants.md) 事件。 如果在處理第一個值變更事件時，攔截函式是重新輸入來處理後續的值變更事件，第二個事件則是在第一個事件之前完成。 這種情況會導致螢幕讀取器將不正確的資訊傳達給使用者。

由於事件處理會中斷，因此每當攔截函式呼叫會導致擁有線程的訊息佇列被檢查的函式時，可能會收到其他事件。 當在攔截函式中呼叫下列任一項時，就會發生這種情況：

-   Windows [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)、 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage)、 [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea)、 [**對話方塊**](/windows/desktop/api/winuser/nf-winuser-dialogboxa)或 [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) 函數
-   Microsoft Active Accessibility 函式 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)、 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)、 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面或其他元件物件模型 (COM) 屬性或跨進程界限的方法

因為攔截函式會呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) 和 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法，所以無法避免重新進入。 唯一的解決方法是讓用戶端開發人員在攔截函式中新增程式碼，以偵測進入，並在攔截器函式重新輸入時採取適當的動作。

 

 