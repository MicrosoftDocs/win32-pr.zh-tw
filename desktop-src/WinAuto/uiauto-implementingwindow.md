---
title: 視窗控制項模式
description: 描述執行 IWindowProvider 的方針和慣例，包括屬性、方法和事件的相關資訊。 Window 控制項模式支援在傳統 GUI 內提供基本視窗功能的控制項。
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- 消費者介面自動化，執行視窗控制項模式
- 消費者介面自動化、視窗控制項模式
- 消費者介面自動化、IWindowProvider
- IWindowProvider
- 執行消費者介面自動化 Window 控制項模式
- 視窗控制項模式
- 控制項模式，IWindowProvider
- 控制項模式，執行消費者介面自動化視窗
- 控制項模式，視窗
- 介面，IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311343"
---
# <a name="window-control-pattern"></a>視窗控制項模式

描述執行 [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)的方針和慣例，包括屬性、方法和事件的相關資訊。 **Window** 控制項模式支援在傳統 GUI 內提供基本視窗功能的控制項。

必須執行此控制項模式的控制項範例包括最上層應用程式視窗、多重文件介面 (MDI) 子視窗、可調整大小的分割窗格控制項、強制回應對話方塊和氣球說明視窗。 如需實作此控制項模式的控制項範例，請參閱 [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IWindowProvider** 的必要成員](#required-members-for-iwindowprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **Window** 控制項模式時，請注意下列方針和慣例：

-   為了支援使用 Microsoft 消費者介面自動化修改視窗大小和螢幕位置的功能，除了 [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)以外，控制項還必須執行 [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) 。
-   包含標題列的控制項和可讓控制項移動、調整大小、最大化、最小化或關閉的標題列元素，通常都必須執行 [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)。
-   工具提示快顯視窗和下拉式方塊或功能表下拉式清單等控制項通常不會執行 [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)。
-   氣球說明視窗與基本工具提示快顯視窗的差異在於布建類似視窗的 [ **關閉** ] 按鈕。
-   [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)不支援全螢幕模式，因為它是應用程式特有的功能，而不是一般的視窗行為。

## <a name="required-members-for-iwindowprovider"></a>**IWindowProvider** 的必要成員

執行 [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) 介面需要下列屬性、方法和事件。



| 必要成員                                                                            | 成員類型 | 備註                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**WindowInteractionState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | 屬性    | 不保證是 **WindowInteractionState \_ ReadyForUserInteraction** |
| [**IsModal**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | 屬性    | 無                                                                        |
| [**IsTopmost**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | 屬性    | 無                                                                        |
| [**CanMaximize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | 屬性    | 無                                                                        |
| [**CanMinimize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | 屬性    | 無                                                                        |
| [**WindowVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | 屬性    | 無                                                                        |
| [**關閉**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | 方法      | 無                                                                        |
| [**SetVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | 方法      | 無                                                                        |
| [**WaitForInputIdle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | 方法      | 無                                                                        |
| [**UIA \_ 視窗 \_ WindowClosedEventId**](uiauto-event-ids.md) | 事件       | 無                                                                        |
| [**UIA \_ 視窗 \_ WindowOpenedEventId**](uiauto-event-ids.md) | 事件       | 無                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化用戶端的控制項模式對應](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 




