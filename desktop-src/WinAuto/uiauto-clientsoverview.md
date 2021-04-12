---
title: 消費者介面自動化用戶端總覽
description: 本主題說明在執行 Microsoft 消費者介面自動化用戶端應用程式時所涉及的主要工作。
ms.assetid: 536ccf03-2f52-49e5-a95f-ea56cf821779
keywords:
- 消費者介面自動化，用戶端總覽
- 用戶端，關於
- 用戶端、元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d4705d75a0a80c114e2b83f9625f827c75503b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375489"
---
# <a name="ui-automation-clients-overview"></a>消費者介面自動化用戶端總覽

本主題說明在執行 Microsoft 消費者介面自動化用戶端應用程式時所涉及的主要工作。

消費者介面自動化用戶端是任何使用消費者介面自動化 API 來存取 UI 專案相關資訊的應用程式，或是透過以程式設計方式操作其 UI 元素來控制應用程式的任何應用程式。 消費者介面自動化用戶端包括輔助技術應用程式，例如螢幕讀取器，它會取出 UI 元素的相關資訊，並以可供殘障人士使用的方式呈現資訊。 它們也包含語音辨識程式和軟體測試控管之類的應用程式，這些工具使用消費者介面自動化而不是滑鼠和鍵盤來「驅動」其他應用程式。

從消費者介面自動化的觀點來看，消費者介面自動化用戶端應用程式必須完成的主要工作包括下列各項：

1.  **取得 CUIAutomation 物件的實例。**

    UI 元素的相關資訊，以及 UI 元素功能的存取權，會由消費者介面自動化提供者公開給用戶端。 不過，用戶端應用程式無法直接與提供者搭配運作。 相反地，核心服務位於用戶端和提供者之間。 當用戶端呼叫消費者介面自動化 API 時，它實際上會呼叫消費者介面自動化核心服務，而該服務會接著呼叫提供者所執行的介面。

    若要取得核心消費者介面自動化服務的存取權，用戶端必須建立 [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) 物件的實例，並在物件上取出 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 介面指標。 **IUIAutomation** 指標是用戶端用來存取用戶端可用之所有消費者介面自動化功能的金鑰。 如需詳細資訊，請參閱 [建立 CUIAutomation 物件](uiauto-creatingcuiautomation.md)。

2.  **從消費者介面自動化樹狀結構取出 UI 元素的 IUIAutomationElement 介面。**

    消費者介面自動化會將個別的 UI 專案公開為執行 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面的物件。 專案的相關資訊可透過專案的 **IUIAutomationElement** 介面所公開的屬性提供給用戶端，並可存取專案的控制項模式。 控制項模式介面所公開的屬性和方法，可讓您存取控制項特定的資訊和功能。

    消費者介面自動化的專案物件會以階層式樹狀結構中的用戶端提供，稱為消費者介面自動化樹狀目錄。 用戶端會使用 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 介面所公開的方法來取得樹狀結構中 UI 元素的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面，以及抓取其他介面，用來搜尋樹狀結構中符合一組特定準則的元素。 如需詳細資訊，請參閱 [取得消費者介面自動化元素](uiauto-obtainingelements.md)。

    在抓取 UI 元素時，用戶端可以使用消費者介面自動化的快取功能來改善系統效能。 快取可讓用戶端指定一組要與元素一起抓取的屬性和控制項模式。 在單一進程調用中，消費者介面自動化會抓取元素和指定的屬性和控制項模式，然後將它們儲存在快取中。 如果沒有快取，則需要個別的進程調用來取得每個屬性或控制項模式。 如需詳細資訊，請參閱快取 [消費者介面自動化屬性和控制項模式](uiauto-cachingforclients.md)。

3.  **取出 UI 元素屬性，並叫用 UI 專案功能。**

    用戶端會使用 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面來取出專案的屬性和控制項模式。 介面包含每個屬性抓取方法的兩個版本—一個版本會從快取中抓取屬性，另一個版本會從提供者抓取屬性。 如需詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。

4.  **回應消費者介面自動化事件。**

    消費者介面自動化提供者會引發事件，以通知用戶端變更或重要的出現位置。 用戶端必須判斷所需的事件，然後執行並註冊事件處理介面，以接收和處理這些事件。 如需詳細資訊，請參閱 [訂閱消費者介面自動化事件](uiauto-eventsforclients.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> <dt>

[UI 自動化屬性概觀](uiauto-propertiesoverview.md)
</dt> <dt>

[UI 自動化事件概觀](uiauto-eventsoverview.md)
</dt> </dl>

 

 