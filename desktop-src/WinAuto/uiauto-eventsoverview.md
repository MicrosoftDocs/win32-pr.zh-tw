---
title: UI 自動化事件概觀
description: Microsoft 消費者介面自動化事件通知是輔助技術的主要功能，例如螢幕閱讀程式和螢幕放大鏡。
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- 消費者介面自動化，事件總覽
- 消費者介面自動化，事件類別目錄
- 消費者介面自動化，事件通知
- 事件通知
- 事件，類別
- 事件，事件通知
- 屬性變更事件
- 元素動作事件
- 結構變更事件
- 全域桌面變更事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ddd61ed72ae0e92a13f6b59b493427fd7be421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315274"
---
# <a name="ui-automation-events-overview"></a>UI 自動化事件概觀

Microsoft 消費者介面自動化事件通知是輔助技術的主要功能，例如螢幕閱讀程式和螢幕放大鏡。 這些消費者介面自動化的用戶端會在 UI 中發生問題時追蹤消費者介面自動化提供者所引發的事件，並使用資訊來通知終端使用者。

藉由允許提供者應用程式選擇性地引發事件來改善效率，取決於是否有用戶端訂閱那些事件或完全沒有，前提是沒有用戶端正在接聽任何事件。

UI 自動化事件分成下列類別。



| 事件類別目錄        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 屬性變更       | 當消費者介面自動化元素或控制項模式上的屬性變更時引發。 例如，如果用戶端需要監視應用程式的核取方塊控制項，則可以註冊來接聽 [**IUIAutomationTogglePattern：： CurrentToggleState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) 屬性上的屬性變更事件。 當選取或取消選取核取方塊控制項時，提供者會引發事件，而且用戶端可視需要採取動作。 |
| 項目動作        | 當使用者或程式設計活動的 UI 結果變更時引發，例如，按一下按鈕或透過 [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)叫用時。                                                                                                                                                                                                                                                     |
| 結構變更      | 當消費者介面自動化樹狀結構的結構變更時引發。 當新的 UI 項目顯示、隱藏或從桌面上移除時，結構會變更。                                                                                                                                                                                                                                                                                                              |
| 全域桌面變更 | 發生用戶端感興趣的全域動作時 (例如，焦點從一個項目移到另一個項目時，或當視窗關閉時) 引發。                                                                                                                                                                                                                                                                                                                      |
| 通知          | 當應用程式呼叫 [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) 函式時引發。 [**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) 表示通知的類型。                                                                                                                                                                                                                                                 |



 

某些事件並不一定表示 UI 的狀態已經變更。 例如，如果使用者索引標籤是文字輸入欄位，然後按一下按鈕來更新欄位，則會引發 UIA 的 [**\_ 文字 \_ TextChangedEventId**](uiauto-event-ids.md) 事件，即使使用者未實際變更文字也是一樣。 在處理事件時，用戶端應用程式可能需要在採取動作之前檢查是否有任何實際變更。

即使 UI 的狀態未變更，也可能引發下列事件。

-   [**UIA \_AutomationPropertyChangedEventId**](uiauto-event-ids.md) (取決於已變更的屬性) 
-   [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)
-   [**UIA \_ 選取專案 \_ InvalidatedEventId**](uiauto-event-ids.md)
-   [**UIA \_ 文字 \_ TextChangedEventId**](uiauto-event-ids.md)

如需所有消費者介面自動化事件的說明，請參閱 [事件識別碼](uiauto-event-ids.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[訂閱消費者介面自動化事件](uiauto-eventsforclients.md)
</dt> </dl>

 

 