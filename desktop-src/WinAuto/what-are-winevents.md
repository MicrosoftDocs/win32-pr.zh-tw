---
title: 什麼是 WinEvents
description: 當系統或使用者介面發生變更時，伺服器應用程式和作業系統會使用 WinEvents 來通知用戶端。
ms.assetid: 43723706-a173-4ddc-b135-824a7a8e8b40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97864f2b1464718680d781ad843345f1e46fce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968057"
---
# <a name="what-are-winevents"></a>什麼是 WinEvents？

當系統或使用者介面發生變更時，伺服器應用程式和作業系統會使用 WinEvents 來通知用戶端。

New-winevent 支援是 Windows 作業系統的一項功能，可提供下列功能：

-   用戶端用來註冊事件通知的簡單方式。
-   將用戶端程式代碼插入伺服器的機制。
-   將事件從伺服器路由傳送到感興趣的用戶端。
-   針對大部分的 **HWND** 型控制項自動產生事件。

**HWND** 型控制項的事件產生對伺服器開發人員來說特別重要。 Microsoft Active Accessibility 執行時間提供所有標準 UI 元素的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proxy。 同樣地，系統會在每次建立、終結、移動、調整大小或對 **HWND** 型控制項執行任何其他動作時，自動產生適當的 WinEvents。

系統會自動支援某些 WinEvents （包括一般 **HWND** 事件）。 Microsoft Active Accessibility 的伺服器支援其他類型的 WinEvents，例如特定控制項特定的狀態變更或選取事件。

當發生影響 UI 的事件時，伺服器可以藉由呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 函式，將事件通知廣播給所有感興趣的用戶端。 函式呼叫包含的資訊可識別發生的事件種類，以及套用事件的 UI 元素。 用戶端可以使用此資訊來取得 UI 專案的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件，並收集詳細資訊。

例如，若要通知用戶端控制項的名稱已變更，伺服器會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 並傳遞事件參數中的 [**事件 \_ 物件 \_ NAMECHANGE**](event-constants.md) 。 系統會藉由判斷哪些用戶端已註冊要接收該特定事件並呼叫其已註冊的回呼函式來回應。 如果沒有為事件註冊的用戶端，則伺服器對 **NotifyWinEvent** 的呼叫會相當於「無作業」，且效能影響可忽略。

伺服器會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) ，在事件發生之後向系統公告事件。 在事件發生之前，它們絕對不能通知系統事件。

用戶端會使用 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)來註冊回呼攔截函式，以通知事件。 用戶端會針對所有可能的事件設定單一攔截函式，或針對不同的事件範圍設定多個攔截函式。 如需詳細資訊，請參閱 [註冊](registering-a-hook-function.md)攔截函式。

當 Microsoft Active Accessibility 收到事件的通知時，它會呼叫任何針對該事件註冊的攔截函式，並從 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)傳遞參數。

 

 




