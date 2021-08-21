---
title: SynchronizedInput 控制項模式
description: 描述執行 ISynchronizedInputProvider 的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- 消費者介面自動化，執行 SynchronizedInput 控制項模式
- 消費者介面自動化，SynchronizedInput 控制項模式
- 消費者介面自動化、ISynchronizedInputProvider
- ISynchronizedInputProvider
- 執行消費者介面自動化 SynchronizedInput 控制項模式
- SynchronizedInput 控制項模式
- 控制項模式，ISynchronizedInputProvider
- 控制模式，消費者介面自動化執行 SynchronizedInput
- 控制項模式，SynchronizedInput
- 介面，ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91aa4ad93a30be26ebcbc463ade3a27d896d61727508965a86d1ed229b7d79be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114849"
---
# <a name="synchronizedinput-control-pattern"></a>SynchronizedInput 控制項模式

描述執行 [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider)的方針和慣例，包括屬性和方法的相關資訊。 **SynchronizedInput** 控制項模式可讓 Microsoft 消費者介面自動化用戶端應用程式將滑鼠或鍵盤輸入導向至特定的 UI 元素。

此控制項模式通常用於自動化測試腳本，以將滑鼠或鍵盤輸入傳送至特定的使用者介面元素，然後確認專案收到輸入。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**ISynchronizedInputProvider** 的必要成員](#required-members-for-isynchronizedinputprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **SynchronizedInput** 控制項模式時，請注意下列方針和慣例：

-   呼叫 [**ISynchronizedInputProvider：： StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) 方法時，消費者介面自動化提供者應該開始檢查指定類型的輸入，然後執行下列其中一個動作：
    -   當針對元素找到相符的輸入時，提供者應該引發 [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) 事件。
    -   當找到相符的輸入，但它到達不同的元素時，提供者應該引發 [**UIA \_ InputReachedOtherElementEventId**](uiauto-event-ids.md) 事件。
    -   當找到不符的輸入時，提供者應該捨棄輸入並引發 [**UIA \_ InputDiscardedEventId**](uiauto-event-ids.md) 事件。
-   如果消費者介面自動化提供者是針對目前專案以外的元素，則必須捨棄該輸入。
-   當專案接收到輸入時，或呼叫 [**ISynchronizedInputProvider：： Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) 方法時，提供者會停止檢查輸入並繼續正常執行。
-   如果提供者已在接聽輸入時呼叫 [**ISynchronizedInputProvider：： StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) ，則提供者應該傳回 [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md)。

## <a name="required-members-for-isynchronizedinputprovider"></a>**ISynchronizedInputProvider** 的必要成員

執行 [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) 介面需要下列屬性、方法和事件。



| 必要成員                                                                         | 成員類型 | 備註 |
|------------------------------------------------------------------------------------------|-------------|-------|
| [**StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | 方法      | 無  |
| [**取消**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | 方法      | 無  |
| [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) | 事件       | 無  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




