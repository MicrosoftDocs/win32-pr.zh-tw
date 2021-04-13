---
title: 訂閱消費者介面自動化事件
description: Microsoft 消費者介面自動化可讓用戶端訂閱感興趣的事件。 這項功能可讓您不需要持續輪詢系統中的 UI 元素，查看任何資訊、結構或狀態是否已變更，進而改善效能。
ms.assetid: 7019ecb8-6123-4e00-926c-6725d7e71385
keywords:
- 用戶端，消費者介面自動化事件
- 用戶端，消費者介面自動化的事件
- 消費者介面自動化，用戶端的事件
- 消費者介面自動化，用戶端事件
- 消費者介面自動化，訂閱事件
- 消費者介面自動化，訂用帳戶方法
- 消費者介面自動化，程式碼範例
- 消費者介面自動化，範例
- 消費者介面自動化，範例
- 訂閱 UI 自動化事件
- 事件，消費者介面自動化訂用帳戶
- 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a89df1b9d2afc401e07b6cd77d1307d912f11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301059"
---
# <a name="subscribing-to-ui-automation-events"></a>訂閱消費者介面自動化事件

Microsoft 消費者介面自動化可讓用戶端訂閱感興趣的事件。 這項功能可讓您不需要持續輪詢系統中的 UI 元素，查看任何資訊、結構或狀態是否已變更，進而改善效能。

同時也因為能夠只接聽定義範圍內的事件，而改善效率。 例如，用戶端可以接聽清單中專案、清單本身或整個對話方塊中的選取專案變更。

> [!Note]  
> 請勿假設所有可能的事件都是由消費者介面自動化提供者引發。 例如，並非所有屬性變更都會導致 Windows Forms 和 Microsoft Win32 控制項的標準 proxy 提供者引發事件。

 

如需更廣泛的消費者介面自動化事件查看，請參閱 [消費者介面自動化事件總覽](uiauto-eventsoverview.md)。

> [!Note]  
> 在執行事件處理常式之前，您應該先熟悉 [瞭解執行緒問題](uiauto-threading.md)中所述的執行緒問題。

 

本主題包含下列各節。

-   [註冊事件處理常式](#registering-event-handlers)
-   [範例](#examples)
-   [相關主題](#related-topics)

## <a name="registering-event-handlers"></a>註冊事件處理常式

用戶端應用程式會使用下列其中一個 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 方法，藉由註冊事件處理常式來訂閱特定種類的事件。



| 訂用帳戶方法                                                                                                                                                                                                | 事件類型       | 回呼介面                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------------------------------------------------------------------|
| [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)                                                                                                                            | 焦點變更     | [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)         |
| [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler)、 [ **AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray) | 屬性變更  | [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)   |
| [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)                                                                                                                    | 結構變更 | [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) |
| [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)                                                                                                                           | 通知     | [**IUIAutomationNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)         |
| [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)                                                                                                                                | 其他事件     | [**IUIAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)                                 |



 

當用戶端將所有子系的事件處理常式加入 (Treescope.children 下階) 時，消費者介面自動化只針對子樹的根目錄新增一個處理常式，而處理常式會接聽所有子代。 [**\_**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) 消費者介面自動化不會以遞迴方式加入事件處理常式。

當用戶端呼叫 [**IUIAutomation：： RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers) 方法時消費者介面自動化會從用戶端進程中移除所有事件處理常式。

若要接收和處理事件，您可以執行公開回呼介面的事件處理物件，而且您必須呼叫事件註冊方法（例如 [**IUIAutomation：： AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler)）來註冊物件。 回呼介面具有單一方法;當處理事件時，消費者介面自動化會呼叫這個方法。

在關機時，或當應用程式不再需要消費者介面自動化事件時，消費者介面自動化用戶端應該呼叫下列一或多個 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 方法。

> [!Note]  
> 消費者介面自動化用戶端不應該使用多個執行緒來新增或移除事件處理常式。 如果在相同的用戶端進程中新增或移除一個事件處理常式，可能會導致未預期的行為。

 



| 方法                                                                                                | 描述                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler)             | 取消註冊使用 [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)註冊的事件處理常式。                                                                                                                                  |
| [**RemoveFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler)         | 取消註冊使用 [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)註冊的事件處理常式。                                                                                                                              |
| [**RemovePropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler)   | 取消註冊使用 [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) 或 [**AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray)註冊的事件處理常式。 |
| [**RemoveStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler) | 取消註冊使用 [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)註冊的事件處理常式。                                                                                                                      |
| [**RemoveNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-removenotificationeventhandler)        | 取消註冊 weas 使用 [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)註冊的事件處理常式。                                                                                                                            |
| [**RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers)                         | 移除註冊所有已註冊的事件處理常式。                                                                                                                                                                                                                                      |



 

在取消訂閱處理常式之後，如果事件同時與取消訂閱事件的要求同時收到，就可能會將事件傳遞至事件處理常式。 最佳作法是遵循元件物件模型 (COM) 標準，並避免在其參考計數達到零時終結事件處理常式物件。 在取消訂閱事件之後立即終結事件處理常式，可能會在延遲傳遞事件時導致存取違規。

## <a name="examples"></a>範例

如需示範如何處理消費者介面自動化事件的程式碼範例，請參閱 [如何執行事件處理常式](uiauto-howto-implement-event-handlers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化事件概觀](uiauto-eventsoverview.md)
</dt> <dt>

[瞭解執行緒問題](uiauto-threading.md)
</dt> </dl>

 

 




