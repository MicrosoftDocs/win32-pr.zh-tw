---
title: Active Accessibility 的運作方式
description: Microsoft Active Accessibility 的設計目的是協助協助工具輔助，稱為用戶端，與其他應用程式和作業系統的標準和自訂 UI 元素互動。
ms.assetid: 29325f0a-c6ca-42b1-b85d-2671f7041034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdeffcebd96ffba804bfc24672bf867028e9b0c7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "103841844"
---
# <a name="how-active-accessibility-works"></a>Active Accessibility 的運作方式

Microsoft Active Accessibility 的設計目的是協助協助工具輔助，稱為 *用戶端*，與其他應用程式和作業系統的標準和自訂 UI 元素互動。 Microsoft Active Accessibility 用戶端是任何使用 Microsoft Active Accessibility 來存取、識別或操作應用程式 UI 元素的程式。 用戶端包括協助工具輔助、自動化測試控管，以及某些以電腦為基礎的定型應用程式。

使用 Microsoft Active Accessibility，用戶端應用程式可以：

-   查詢資訊;例如，關於特定位置的 UI 元素。
-   當資訊變更時接收通知;例如，當控制項變成灰色或文字字串變更時。
-   執行會影響使用者介面或檔內容的動作;例如，按一下 [推送] 按鈕、下拉式功能表，然後選擇功能表命令。

與用戶端互動和提供資訊的應用程式稱為「 *伺服器*」。 伺服器使用 Microsoft Active Accessibility 將其 UI 元素的相關資訊提供給用戶端。 任何使用 Microsoft Active Accessibility 來公開其使用者介面相關資訊的控制項、模組或應用程式都會被視為 Microsoft Active Accessibility 伺服器。 伺服器會傳送事件通知來與用戶端通訊 (例如呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)) 和回應用戶端要求以存取 UI 元素 (例如處理從 [*OLEACC*](uiauto-glossary.md)) 傳送的 [**WM \_ GETOBJECT**](wm-getobject.md)訊息。 伺服器會透過 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面公開資訊。

使用 Microsoft Active Accessibility 時，伺服器應用程式可以：

-   提供其自訂使用者介面物件的相關資訊，以及其用戶端視窗的內容。
-   在使用者介面變更時傳送通知。

例如，若要讓使用者從 word 處理器自訂工具列中選取命令 verbally，語音辨識程式必須具有該工具列的相關資訊。 因此，該字處理器必須讓該資訊可供使用。 Microsoft Active Accessibility 提供方法，讓字處理器公開其自訂工具列的相關資訊，以及讓語音辨識程式取得該資訊。

### <a name="client-applications-and-active-accessibility"></a>用戶端應用程式和 Active Accessibility

當伺服器 UI 已變更，讓它可以將該資訊傳送給使用者時，必須通知 Microsoft Active Accessibility 用戶端。 為了確保用戶端會收到 UI 變更的相關資訊，它會使用稱為「視窗事件」或「WinEvents」的機制來註冊，以接收通知。 如需詳細資訊，請參閱 [WinEvents](winevents-infrastructure.md)。

為了瞭解和操作特定的 UI 專案，用戶端會使用 Microsoft Active Accessibility 元件物件模型 (COM) 介面 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)。

用戶端可以透過下列四種方式，取得 UI 元素的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件：

-   呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 並傳遞 UI 元素的視窗控制碼。
-   呼叫 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) 並傳遞位於 UI 元素周框內的螢幕位置。
-   設定 New-winevent 勾點、接收通知，然後呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) ，以抓取產生事件之 UI 元素的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。
-   呼叫 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法（例如 [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) 或 [**get \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) ）移至不同的 **IAccessible** 物件。

 

 




