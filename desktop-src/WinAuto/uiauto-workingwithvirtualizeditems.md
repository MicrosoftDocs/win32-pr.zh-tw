---
title: 使用虛擬化專案
description: 本主題說明如何使用 >itemcontainer 和 VirtualizedItem 控制項模式所提供的功能，來尋找和取得虛擬化專案的相關資訊。
ms.assetid: e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52
keywords:
- 用戶端，消費者介面自動化虛擬化專案
- 用戶端，虛擬化專案
- 用戶端、控制項模式
- 用戶端，VirtualizedItem 控制項模式
- 用戶端，>itemcontainer 控制項模式
- 用戶端，消費者介面自動化 VirtualizedItem 控制項模式
- 用戶端，消費者介面自動化控制模式
- 用戶端，消費者介面自動化 >itemcontainer 控制項模式
- 消費者介面自動化，虛擬化專案
- 消費者介面自動化，控制項模式
- 消費者介面自動化，VirtualizedItem 控制項模式
- 消費者介面自動化，>itemcontainer 控制項模式
- VirtualizedItem 控制項模式
- '>itemcontainer 控制項模式'
- 控制項模式，VirtualizedItem
- 控制項模式，>itemcontainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2c0e84f91af6bcaadef5af373b73057fb4a137480255f3ee1af4456e45eaf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570368"
---
# <a name="working-with-virtualized-items"></a>使用虛擬化專案

本主題說明如何使用 [>itemcontainer](uiauto-implementingitemcontainer.md) 和 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式所提供的功能，來尋找和取得虛擬化專案的相關資訊。

-   [虛擬化總覽](#overview-of-virtualization)
-   [控制項如何支援虛擬化](#how-a-control-supports-virtualization)
-   [用戶端如何尋找和實現虛擬化專案](#how-clients-find-and-realize-virtualized-items)
-   [範例](#example)
-   [相關主題](#related-topics)

## <a name="overview-of-virtualization"></a>虛擬化總覽

包含大量子專案的控制項可以使用虛擬化來有效率地管理專案。 利用虛擬化，控制項在任何指定時間只會在記憶體中維護完整的資訊。 通常，子集只會包含使用者目前可見的專案。 其餘虛擬化專案的完整資訊會保存在儲存體中，並載入記憶體中或已實現（例如，當使用者可以看到新專案時）。

使用虛擬化的控制項代表一項挑戰，因為只有在消費者介面自動化樹狀目錄中，以 Microsoft 消費者介面自動化專案的形式來提供正式的專案。 虛擬化專案不存在於樹狀結構中，因此用戶端無法使用這些專案的相關資訊。 為了抓取虛擬化專案的相關資訊，用戶端需要一種方式來強制消費者介面自動化傳遞要求，以實現控制項的專案。 在瞭解專案之後，消費者介面自動化可以為它們建立消費者介面自動化元素。 消費者介面自動化包含兩種可讓用戶端使用虛擬化專案的控制項模式： [>itemcontainer](uiauto-implementingitemcontainer.md) 和 [VirtualizedItem](uiauto-implementingvirtualizeditem.md)。

## <a name="how-a-control-supports-virtualization"></a>控制項如何支援虛擬化

任何可以包含虛擬化專案的控制項都必須支援 [>itemcontainer](uiauto-implementingitemcontainer.md) 控制項模式。 此外，任何可以虛擬化的專案都必須支援 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式。 >itemcontainer 和 VirtualizedItem 控制項模式所公開的功能，可透過 [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) 和 [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) 介面供用戶端存取。

## <a name="how-clients-find-and-realize-virtualized-items"></a>用戶端如何尋找和實現虛擬化專案

用戶端可以使用 [**IUIAutomationItemContainerPattern：： FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) 方法，根據特定屬性的值來搜尋容器中的子專案。 方法也可以取出容器中的第一個專案，或在指定專案之後的專案。 如果找到相符的子專案， **FindItemByProperty** 會抓取專案的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面。 但是，如果子專案已虛擬化，則 **IUIAutomationElement** 介面是預留位置。 當用戶端嘗試使用 **IUIAutomationElement** 介面來取出屬性值或呼叫尚未提供的方法時，就會發生 [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md)錯誤。 您可以透過預留位置取得哪些屬性或方法，取決於控制項的執行。 預留位置的唯一需求是支援 [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) 介面。

[**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md)錯誤是指用戶端可能會虛擬化專案的指示。 用戶端應藉由取得專案的 [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) 介面來回應，然後藉由呼叫 [**IUIAutomationVirtualizedItemPattern：：認識**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) 方法來實現專案。 如果成功，則 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面可完全正常運作，並提供所有適當的屬性。

視控制項的執行而定，呼叫 [**IUIAutomationVirtualizedItemPattern：：意識**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) 可能會導致控制項將專案滾動到視圖中。 不過，用戶端不應該依賴專案滾動或變成可見的專案。 為了確保可以看見專案，用戶端可以使用 [**IUIAutomationScrollItemPattern：： ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollitempattern-scrollintoview) 方法。

## <a name="example"></a>範例

如需示範如何使用消費者介面自動化的虛擬化支援的程式碼範例，請參閱 [如何取出虛擬化專案](uiauto-howto-retrieve-virtualized-item.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




