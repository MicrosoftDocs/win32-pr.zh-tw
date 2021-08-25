---
title: 產生適當的 WinEvents
description: 伺服器開發人員必須確保為所有 UI 元素產生適當的 WinEvents，包括以視窗為基礎的 UI 元素、無視窗 UI 元素，以及具有高度自訂行為的 UI 元素。
ms.assetid: 253e0162-20e6-4e89-b563-aae9cf7e53a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e148578f55f59d2827fd13a637baf5139c3f934ddf24059e437185c15349b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860388"
---
# <a name="generating-appropriate-winevents"></a>產生適當的 WinEvents

伺服器開發人員必須確保為所有 UI 元素產生適當的 WinEvents，包括以視窗為基礎的 UI 元素、無視窗 UI 元素，以及具有高度自訂行為的 UI 元素。

使用者會為標準的 **HWND** 型 UI 元素提供預設的 new-winevent 支援。 因為使用者會自動產生這些事件，所以伺服器只需要針對自訂控制項、無視窗專案，或是使用者尚未產生其事件的控制項產生事件。

若要傳送事件，伺服器會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 並傳遞事件常數、物件識別碼，以及可以回應用戶端要求之視窗的 **HWND** ，以取得詳細資訊。 需要引發的事件會根據 UI 元素的類型而有所不同。 有一些應針對所有控制項傳送的一般事件，以及應該只針對適當的 UI 元素傳送的特定事件。

## <a name="general-events"></a>一般事件

您可以針對所有 UI 元素傳送一般 WinEvents。 其中包含：

-   [**活動 \_建立 \_**](event-constants.md) 物件時建立 (的物件) 
-   [**活動 \_物件 \_**](event-constants.md) 終結時 (物件終結) 
-   [**活動 \_顯示 \_**](event-constants.md) 物件時顯示 (的物件) 
-   [**活動 \_隱藏 \_**](event-constants.md) 物件時隱藏 (物件) 

## <a name="specific-events"></a>特定事件

您也可以針對特定類型的 UI 元素傳送特定的 WinEvents。 例如，針對允許使用者進行選取的控制項（例如清單方塊），使用 [**事件 \_ 物件 \_ 選擇**](event-constants.md) 。

如需特定 UI 元素類型所預期的事件的詳細資訊，請參閱下列資源：

-   [附錄 A：支援的消費者介面元素參考](appendix-a--supported-user-interface-elements-reference.md)。 本附錄包含由 Microsoft Active Accessibility 公開之系統產生之 UI 元素的相關資訊。 每個控制項的檔包含可由 UI 元素產生的事件相關資訊。
-   [事件常數](event-constants.md)。 本主題包含作業系統和伺服器應用程式所產生之事件的相關資訊。
-    (AccEvent.exe) 可存取的事件監看員。 此工具會顯示使用者針對特定 UI 元素傳送的事件。 您可以使用此工具來瞭解 UI 元素可以預期的事件。 如需詳細資訊，請參閱 [可存取的事件](accessible-event-watcher.md)監看員。

 

 




