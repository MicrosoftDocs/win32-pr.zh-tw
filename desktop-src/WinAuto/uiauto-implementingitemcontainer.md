---
title: '>itemcontainer 控制項模式'
description: 描述執行 IItemContainerProvider 的方針和慣例，包括方法的相關資訊。 >itemcontainer 控制項模式用來支援專案虛擬化。
ms.assetid: 6f3dd94e-3563-4a13-9db9-5928a02bab77
keywords:
- 消費者介面自動化，執行 >itemcontainer 控制項模式
- 消費者介面自動化，>itemcontainer 控制項模式
- 消費者介面自動化、IItemContainerProvider
- IItemContainerProvider
- 執行消費者介面自動化 >itemcontainer 控制項模式
- '>itemcontainer 控制項模式'
- 控制項模式，IItemContainerProvider
- 控制模式，消費者介面自動化執行 >itemcontainer
- 控制項模式，>itemcontainer
- 介面，IItemContainerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55246abde51e7053bf0c3266ccbe9c2b080b2fe7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672659"
---
# <a name="itemcontainer-control-pattern"></a>>itemcontainer 控制項模式

描述執行 [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider)的方針和慣例，包括方法的相關資訊。 **>itemcontainer** 控制項模式用來支援專案虛擬化。

包含大量子專案的控制項可以使用虛擬化來有效率地管理專案。 利用虛擬化，控制項在任何指定時間只會在記憶體中維護完整的資訊。 通常，子集只會包含使用者目前可見的專案。 其餘虛擬化專案的完整資訊會保存在儲存體中，並載入記憶體中或已實現（例如，當使用者可以看到新專案時）。

例如，下圖顯示包含上千個虛擬化專案的清單方塊。 因為控制項只會針對目前可見的子專案維護完整的資訊，所以提供者只能針對 100-127 的專案公開 Microsoft 消費者介面自動化元素。

![顯示清單方塊中已虛擬化且未虛擬化專案的圖表](images/virtualizeditems.jpg)

使用虛擬化的控制項代表一項挑戰，因為只會在消費者介面自動化樹狀結構中，以消費者介面自動化元素的形式完全提供 (的已解除虛擬化) 專案。 虛擬化專案不存在於樹狀結構中，因此無法使用這些專案的相關資訊。

為了提供虛擬化專案的相關資訊，提供者會執行公開 [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider)介面的 **>itemcontainer** 控制項模式。 [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty)方法會根據特定屬性的值（例如 **Name**、 **AutomationId** 或 **IsSelected**）來尋找子專案。 如果專案已虛擬化， **FindItemByProperty** 會抓取專案的消費者介面自動化預留位置元素。 預留位置元素是 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面的實作為支援 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式。

[**IVirtualizedItemProvider：：意識**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize)方法可讓用戶端要求實現虛擬化專案，藉此公開專案的完整消費者介面自動化專案，讓所有必要的屬性和模式都可以使用。

雖然 **>itemcontainer** 控制項模式的主要目的是要支援虛擬化的容器案例，但它可以由任何可依名稱抓取子專案的容器來執行，而不論容器是否使用虛擬化。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [IItemContainerProvider 的必要成員](#required-members-for-iitemcontainerprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **>itemcontainer** 控制項模式時，請注意下列方針和慣例：

-   任何可以包含虛擬化專案的控制項都必須支援 **>itemcontainer** 控制項模式。 任何支援根據屬性值抓取專案的容器都可以支援此模式，不論容器是否使用虛擬化。
-   當容器已虛擬化時，其他控制項模式（例如 [選取專案](uiauto-implementingselection.md)、 [資料表](uiauto-implementingtable.md)和 [方格](uiauto-implementinggrid.md) ）可能會受到影響。 例如， [**ISelectionProvider：： GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) 方法可能只支援位於視口中的元素，或僅支援目前未虛擬化的選取專案。
-   [滾動](uiauto-implementingscroll.md)條控制項模式應該不會受到虛擬化的影響。
-   虛擬化專案沒有可用的專案計數或索引資訊。 如有必要，虛擬化控制項可以使用 **DescribedBy** 或 **ItemStatus** 屬性來提供此資訊。
-   控制項開發人員應記錄併發布所有消費者介面自動化屬性的詳細資料，以及使用虛擬化所影響的控制項模式。 雖然 >itemcontainer 和 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式提供基本支援，但它們可能不支援某些虛擬化行為。

下列指導方針和需求適用于 [**IItemContainerProvider：： FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) 方法。

-   雖然並非必要，但 Microsoft 強烈建議 [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) 支援 **Name**、 **AutomationId** 和 **IsSelected** 屬性。
-   如果需要跨越多個物件來尋找相符的物件， [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty)可能會變慢。
-   您可以重複呼叫 [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) ，以依序尋找專案。 只要每個專案只傳回一次，專案就可以依任何順序排列。
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) 可實作為只尋找出現在消費者介面自動化樹狀結構的控制項或內容視圖中的元素。 可以略過只出現在原始視圖中的專案，以避免將多個只代表「專案」一部分的元素，提供給使用者。
-   當搜尋準則符合虛擬化專案時，提供者可以傳回支援 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式的預留位置元素。 下列指導方針適用于預留位置元素：
    -   抓取虛擬化專案的預留位置專案時，不能造成 UI 變更。
    -   預留位置元素必須是其他子專案的對等專案， (需要有結構變更的事件) 。
    -   在可能的情況下，提供者可以建立完整的 automation 元素，而不是預留位置。
-   當搜尋準則符合非虛擬化專案時，提供者必須傳回實際的元素，而不是預留位置。
-   如果找不到任何專案， [**IItemContainerProvider：： FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) 應該將 *pFound* 參數設定為 **Null** ，並傳回 **S \_ OK**。
-   當 *propertyId* 參數是0時，提供者應該在 *pStartAfter* 之後傳回下一個專案。
-   如果 *pStartAfter* 參數為 **Null** ，而 *propertyId* 為0，則提供者應該傳回容器中的第一個專案。
-   當 *propertyId* 參數是0時，會忽略 value 參數。

下列指導方針和需求適用于消費者介面自動化樹狀結構中虛擬化專案的預留位置元素。

-   雖然我們鼓勵提供者為預留位置元素支援更多屬性和控制項模式，但是只需要 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式。
-   當再次呼叫 [**IItemContainerProvider：： FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) 時，提供者可能會使先前的預留位置元素失效。  (如果用戶端需要瞭解預留位置元素，就應該立即這麼做;否則，如果再次呼叫 **FindItemByProperty** ，或因為任何原因而改變，則元素可能會失效。 ) 
-   UI 動作（例如滾動或調整大小）可能會導致容器的視口變更，而且會顯示一組新的子專案。 在此情況下，消費者介面自動化樹狀結構中可能無法使用先前抓取的預留位置元素。
-   提供者不應虛擬化 UI 元素，這些專案可在容器物件的元件區中使用。

## <a name="required-members-for-iitemcontainerprovider"></a>IItemContainerProvider 的必要成員

以下是執行 [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) 介面的必要方法。



| 必要成員                                                               | 成員類型 | 備註 |
|--------------------------------------------------------------------------------|-------------|-------|
| [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) | 方法      | 無  |



 

**>itemcontainer** 控制項模式沒有相關聯的屬性或事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> <dt>

[VirtualizedItem 控制項模式](uiauto-implementingvirtualizeditem.md)
</dt> </dl>

 

 




