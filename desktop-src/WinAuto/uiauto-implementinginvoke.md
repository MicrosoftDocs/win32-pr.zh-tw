---
title: Invoke 控制項模式
description: 描述執行 IInvokeProvider 的方針和慣例，包括方法的相關資訊。
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- 消費者介面自動化，執行調用控制項模式
- 消費者介面自動化，叫用控制項模式
- 消費者介面自動化、IInvokeProvider
- IInvokeProvider
- 執行消費者介面自動化叫用控制項模式
- 叫用控制項模式
- 控制項模式，IInvokeProvider
- 控制項模式，執行消費者介面自動化叫用
- 控制項模式，Invoke
- 介面，IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839807"
---
# <a name="invoke-control-pattern"></a>Invoke 控制項模式

描述執行 [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)的方針和慣例，包括方法的相關資訊。 叫 **用控制項模式** 是用來支援在啟用時不會維持狀態的控制項，而是會起始或執行單一明確的動作。

維護狀態的控制項（例如核取方塊和選項按鈕）必須改為分別執行 [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) 和 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) 。 如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IInvokeProvider** 的必要成員](#required-members-for-iinvokeprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在實作為 **Invoke** 控制項模式時，請注意下列方針和慣例：

-   如果不是透過另一個控制項模式提供者來公開相同的行為，則控制項會執行 [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) 。 例如，如果控制項的 [**IUIAutomationInvokePattern：： Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) 方法執行的動作與 [**IUIAutomationExpandCollapsePattern：： Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) 或 [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) 方法相同，則控制項不應執行 **IInvokeProvider**。
-   通常按一下、按兩下或按 ENTER、使用預先定義的鍵盤快速鍵，或其他按鈕組合，就可以叫用控制項。
-   叫用 **的事件 (** UIA 叫用 [**\_ \_ InvokedEventId**](uiauto-event-ids.md)) 事件會在已啟動的控制項上引發，而控制項已啟用 (做為回應，以執行其相關聯的動作) 。 在可能的情況下，應該是在控制項完成該動作並返回，且沒有發生封鎖時才會引發該事件。 在下列情況 **下，必須** 先引發叫用的事件 (UIA 叫用 **\_ \_ InvokedEventId**) ，才能在下列案例中提供 **Invoke** 要求：
    -   無法或不適合等待至動作完成。
    -   動作需要使用者互動。
    -   動作費時，且會導致發出呼叫的用戶端長時間凍結。
-   如果叫用控制項有顯著的副作用，則應該透過 **HelpText** 屬性來公開這些副作用。 例如，即使 [**IUIAutomationInvokePattern：： invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) 未與選取專案相關聯， **invoke** 仍可能造成另一個控制項被選取。
-   停留 (或滑鼠停留) 效果通常不會構成叫用 **的事件。** 不過，執行動作 (而不是造成視覺效果) 以停留狀態為基礎的控制項，應該支援叫用 **控制項模式** 。
    > [!Note]  
    > 如果控制項的叫用是與滑鼠相關的副作用所造成的，便會將這個實作視為協助工具問題。

     

-   叫用控制項和選擇項目不同。 但是，依據控制項而定，叫用某些控制項可能會有造成此項目受到選取的副作用。 例如，在 [我的檔] 資料夾中叫用 Microsoft Word 檔案清單專案時，會選取該專案並開啟檔。
-   元素可能會在叫用時立即從 Microsoft 消費者介面自動化樹狀結構中消失。 要求事件回呼所提供的項目資訊，可能會因此而失敗。 建議的解決方法是預先擷取快取的資訊。
-   控制項可以實作多個控制項模式。 例如，Microsoft Excel 工具列上的 [ **填滿色彩** ] 控制項可同時實作為 Invoke 和 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。 ExpandCollapse 控制項模式會公開功能表 **，而叫用控制項模式** 會以選擇的色彩填滿現用選取範圍。

## <a name="required-members-for-iinvokeprovider"></a>**IInvokeProvider** 的必要成員

以下是執行 [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) 介面的必要方法。



| 必要成員                                | 成員類型 | 備註                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**調用**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | 方法      | **Invoke** 是非同步呼叫，必須在不封鎖的情況下立即傳回。<br/> 對於叫用時直接或間接啟動強制回應對話方塊的控制項，此行為尤其重要。 任何引發事件的使用者介面自動化用戶端都會維持封鎖的狀態，直到強制回應對話方塊關閉為止。 <br/> |



 

此控制項模式沒有任何相關聯的屬性或事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> <dt>

[**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)
</dt> </dl>

 

 





