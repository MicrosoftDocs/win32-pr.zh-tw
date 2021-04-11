---
title: 快取消費者介面自動化屬性和控制項模式
description: 使用 Microsoft 消費者介面自動化時，用戶端通常需要針對多個自動化元素取出多個屬性。
ms.assetid: 948b3bb9-75a9-4197-9680-e6fe7bb86feb
keywords:
- 快取，消費者介面自動化屬性
- 快取，屬性
- 快取，消費者介面自動化控制項模式
- 快取、控制項模式
- 消費者介面自動化，快取屬性
- 消費者介面自動化，屬性快取
- 用戶端，快取消費者介面自動化屬性
- 用戶端，快取消費者介面自動化控制項模式
- 消費者介面自動化，快取控制項模式
- 消費者介面自動化，控制項模式快取
- 控制項模式，快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f75a7dc9491565fdfdc0ecc73808c2fb6a9d82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372004"
---
# <a name="caching-ui-automation-properties-and-control-patterns"></a>快取消費者介面自動化屬性和控制項模式

使用 Microsoft 消費者介面自動化時，用戶端通常需要針對多個自動化元素取出多個屬性。 用戶端可以使用屬性抓取方法（例如 [**IUIAutomationElement：： CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) 或 [**CurrentAccessKey**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentaccesskey)），一次取出一個元素的個別屬性。 不過，這個方法的速度很慢且沒有效率，因為它需要針對每個要抓取的屬性進行跨進程呼叫。 為了改善效能，用戶端可以使用快取 (也稱為大量提取) 消費者介面自動化的功能。 快取可讓用戶端使用單一方法呼叫來取得所有所需專案的所有所需屬性。 然後，用戶端可以視需要從快取中取出個別的屬性，並可定期取得快取的新快照集，通常是為了回應在 UI 中表示變更的事件。

應用程式可以在使用方法（例如 [**IUIAutomation：： ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache)、 [**IUIAutomationTreeWalker：： GetFirstChildElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelementbuildcache)或 [**IUIAutomationElement：： FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache)）抓取消費者介面自動化專案時，要求快取。

當您在訂閱事件時指定快取要求時，也會發生快取。 傳遞至事件處理常式做為事件來源的消費者介面自動化專案包含快取的屬性和快取要求所指定的控制項模式。 訂閱事件之後對快取要求所做的任何變更都不會有任何作用。

本主題包含下列各節。

-   [快取要求](#cache-requests)
    -   [指定要快取的屬性和控制項模式](#specifying-property-and-control-patterns-to-cache)
    -   [指定快取要求的範圍和篩選](#specifying-the-scoping-and-filtering-of-a-caching-request)
    -   [元素參考的強度](#strength-of-element-references)
-   [擷取快取的子系和父代](#retrieving-cached-children-and-parents)
-   [正在抓取快取的新快照集](#retrieving-a-new-snapshot-of-the-cache)
-   [範例](#examples)
-   [相關主題](#related-topics)

## <a name="cache-requests"></a>快取要求

快取牽涉到判斷要抓取哪些屬性，以及要從中取出哪些專案，然後再使用這項資訊來建立快取要求。 只要用戶端取得 UI 專案的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面，消費者介面自動化就會快取快取要求中所指定的資訊。

若要建立快取要求，請先使用 [**IUIAutomation：： CreateCacheRequest**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createcacherequest) 方法來取出 [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) 介面指標。 接下來，使用 **IUIAutomationCacheRequest** 的方法來設定快取要求。

### <a name="specifying-property-and-control-patterns-to-cache"></a>指定要快取的屬性和控制項模式

您可以藉由呼叫 [**IUIAutomationCacheRequest：： AddProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addproperty)來指定要快取的屬性。 您可以藉由呼叫 [**IUIAutomationCacheRequest：： AddPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addpattern)來指定要快取的控制項模式。 快取控制項模式時，不會自動快取其屬性;您必須使用 **AddProperty** 來指定想要快取的屬性。

您可以取得控制項模式屬性 (例如， [值](uiauto-implementingvalue.md) 控制項模式的 value 屬性) ，而不需要將整個控制項模式取出至快取中。 只有當您需要使用控制項模式方法時，才必須抓取控制項模式。

### <a name="specifying-the-scoping-and-filtering-of-a-caching-request"></a>指定快取要求的範圍和篩選

您可以在使用要求之前設定 [**IUIAutomationCacheRequest：： treescope.children**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) 屬性，以指定要快取其屬性和控制項模式的元素。 範圍相對於傳遞快取要求的方法所抓取的元素。 例如，如果您只設定 [**Treescope.children \_ 子**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)系，然後取出消費者介面自動化專案，則會快取該專案之子系的屬性和控制項模式，但不會快取專案本身的屬性和控制項模式。 為了確保針對抓取的元素本身進行快取，您必須在 **IUIAutomationCacheRequest：： treescope.children** 屬性中包含 **treescope.children \_ 元素**。 您無法將範圍設定為 **Treescope.children \_ Parent** 或 **treescope.children \_ 祖** 系。 不過，快取子項目時即會快取父項目；請參閱本主題中的＜擷取快取的子系和父代＞。

快取的範圍也會受到 [**IUIAutomationCacheRequest：： TreeFilter**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treefilter) 屬性的影響。 根據預設，只會針對出現在消費者介面自動化樹狀結構之控制項視圖中的元素執行快取。 不過，您可以變更此屬性，將快取套用至所有項目，或是只套用至內容檢視中顯示的項目。

### <a name="strength-of-element-references"></a>元素參考的強度

當您取得 automation 專案時，根據預設，您可以存取該專案的所有屬性和控制項模式，包括未快取的屬性和控制項模式。 不過，您可以藉由將 [**IUIAutomationCacheRequest：： AutomationElementMode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_automationelementmode) 屬性設定為 **AutomationElementMode \_ None**，來指定元素的參考只參考快取的資料。 在此情況下，您無法存取任何未快取的屬性，也無法控制所抓取專案的模式。 這表示您無法存取任何目前的屬性，例如 [**IUIAutomationElement：： CurrentIsEnabled**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisenabled) ，或使用 [**IUIAutomationElement：： GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)取得控制項模式。 在快取的控制項模式中，您無法呼叫在控制項上執行動作的方法，例如 [**IUIAutomationInvokePattern：： Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke)。

可能不需要物件之完整參考的應用程式範例是螢幕讀取器，它可能會預先提取視窗中專案的名稱和控制項類型屬性，而不需要 automation 元素物件本身。

## <a name="retrieving-cached-children-and-parents"></a>擷取快取的子系和父代

當您透過要求的 [**IUIAutomationCacheRequest：： treescope.children**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) 屬性抓取 automation 元素並要求該元素之子系的快取時，可以在您所抓取的元素上呼叫 [**IUIAutomationElement：： GetCachedChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedchildren) ，以取得子項目。

如果 [**treescope.children \_**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) 專案包含在快取要求的範圍內，您可以在任何子項目上呼叫 [**IUIAutomationElement：： GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent) ，以抓取要求的根項目。

> [!Note]  
> 您無法快取要求之根項目的父代或祖系。

 

## <a name="retrieving-a-new-snapshot-of-the-cache"></a>正在抓取快取的新快照集

只有在 UI 中沒有任何變更時，快取才有效。 您的應用程式會負責抓取快取的新快照集（通常是為了回應事件）。

如果您使用快取要求訂閱事件，則每當呼叫事件處理常式時，就會取得快取的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 新快照集作為事件的來源。 您也可以藉由呼叫 [**IUIAutomationElement：： BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache)，來取得專案的快取資訊的新快照。 您可以傳入原始 [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) ，以取得先前快取的所有資訊的新快照。

抓取快取的新快照集並不會修改任何現有 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 參考的屬性。

## <a name="examples"></a>範例

如需示範如何使用消費者介面自動化之快取功能的程式碼範例，請參閱 [如何使用](uiauto-howto-use-caching.md)快取。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[取得 UI 自動化項目](uiauto-obtainingelements.md)
</dt> <dt>

[UI 自動化屬性概觀](uiauto-propertiesoverview.md)
</dt> </dl>

 

 




