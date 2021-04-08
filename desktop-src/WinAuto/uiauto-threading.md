---
title: 瞭解執行緒問題
description: 本主題說明 Microsoft 消費者介面自動化用戶端的常見執行緒案例，並說明如何避免用戶端不正確地使用執行緒時可能發生的問題。
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- 用戶端，消費者介面自動化執行緒問題
- 用戶端，執行緒問題
- 用戶端，事件處理常式執行緒模型
- 用戶端，消費者介面自動化事件處理常式執行緒模型
- 用戶端，消費者介面自動化親和性
- 用戶端、親和性
- 消費者介面自動化，執行緒問題
- 消費者介面自動化，事件處理常式執行緒模型
- 消費者介面自動化，親和性
- 執行緒問題
- 事件處理常式執行緒模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023529"
---
# <a name="understanding-threading-issues"></a>瞭解執行緒問題

本主題說明 Microsoft 消費者介面自動化用戶端的常見執行緒案例，並說明如何避免用戶端不正確地使用執行緒時可能發生的問題。

本主題包含下列幾節：

-   [消費者介面自動化和 UI 執行緒](#ui-automation-and-the-ui-thread)
-   [事件處理常式的執行緒模型](#threading-model-for-event-handlers)
-   [64位 Windows 上的 COM 單元親和性](#com-apartment-affinity-on-64-bit-windows)
-   [相關主題](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a>消費者介面自動化和 UI 執行緒

由於消費者介面自動化使用 Windows 訊息的方式，因此當用戶端應用程式嘗試在 UI 執行緒上與其本身的 UI 互動時，就會發生衝突。 這些衝突可能會導致效能變慢，或甚至導致應用程式停止回應。

如果您的用戶端應用程式要與桌面上的所有元素互動，包括它自己的 UI，您應該從個別的執行緒進行所有的消費者介面自動化呼叫。 這包括尋找元素，例如使用 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) 或 [**IUIAutomationElement：： FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) 方法，以及使用控制項模式。 這個執行緒不應該擁有任何視窗，而且應該是元件物件模型 (COM) 多執行緒的單元 (MTA) 模型執行緒， (使用 **COINIT \_ 多執行緒** 旗標呼叫 [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)來初始化 COM。 ) 

您可以安全地在消費者介面自動化事件處理常式中進行消費者介面自動化呼叫，因為在非 UI 執行緒上一律會呼叫事件處理常式。 不過，在訂閱可能源自用戶端應用程式 UI 的事件時，您必須在非 UI 執行緒上呼叫 [**IUIAutomation：： AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)或相關的方法， (也應該是) 的 MTA 執行緒。 在相同執行緒上移除事件處理常式。

消費者介面自動化用戶端不應該使用多個執行緒來新增或移除事件處理常式。 如果在相同的用戶端進程中新增或移除一個事件處理常式，可能會導致未預期的行為。

## <a name="threading-model-for-event-handlers"></a>事件處理常式的執行緒模型

消費者介面自動化的用戶端應該針對可執行事件處理常式的執行緒使用 COM MTA 執行緒模型。 使用單一執行緒的單元 (STA) 模型可能會造成問題，例如防止用戶端從執行緒移除事件處理常式。

## <a name="com-apartment-affinity-on-64-bit-windows"></a>64位 Windows 上的 COM 單元親和性

根據 COM 規格，遠端物件的存留期是由呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數以建立物件的單元存留期來控管。 當原始的單元關閉時，也會釋放遠端物件。

針對消費者介面自動化用戶端，此 COM 行為可能表示32位專案所使用的 UIAutomationCore.dll) 所建立的遠端32/64 協助程式 (的存留期，是由建立元素之執行緒的單位存留期所控管。 如果消費者介面自動化用戶端將專案封送處理至另一個執行緒，則當原始的單元關閉時，該專案可能會失效。 消費者介面自動化的用戶端應該在使用封送處理的自動化專案時攔截錯誤，以正常方式處理這些問題。

具有64位元素的32位消費者介面自動化用戶端可能會發生相同的問題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[取得 UI 自動化項目](uiauto-obtainingelements.md)
</dt> <dt>

[訂閱消費者介面自動化事件](uiauto-eventsforclients.md)
</dt> <dt>

[UI 自動化事件概觀](uiauto-eventsoverview.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[資訊： OLE 執行緒模型的描述和運作方式](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 