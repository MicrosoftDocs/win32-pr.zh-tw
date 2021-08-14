---
title: 如何在專案視圖中查詢虛擬化專案
description: 本主題說明如何使用 Microsoft 消費者介面自動化，在 [Windows 7 專案] 視圖中取出虛擬化專案的 UI 資訊。
ms.assetid: a0bff8a1-47b1-4750-8086-e2e65a79099e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9196d62e7aa93b21aed15b76b8ced6a9520b27fb5bcee74a0e0d4ddc510c86f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759241"
---
# <a name="how-to-query-a-virtualized-item-in-items-view"></a>如何在專案視圖中查詢虛擬化專案

本主題說明如何使用 Microsoft 消費者介面自動化，在 [Windows 7 專案] 視圖中取出虛擬化專案的 UI 資訊。 本主題包含下列各節。

> [!Note]  
> 本主題僅適用于 Windows 7。 請注意，本主題中所述的協助工具功能在 Windows 的未來版本中可能會有所變更。

 

-   [概觀](#overview)
-   [專案視圖樹狀結構](#items-view-tree-structure)
-   [虛擬化](#virtualization)
-   [取得所有專案的計數](#obtaining-a-count-of-all-items)
-   [取得與所有專案相關的專案索引](#obtaining-an-item-index-with-respect-to-all-items)
-   [取得 Vitualized 專案的參考](#obtaining-a-reference-to-a-vitualized-item)
-   [在螢幕上滾動虛擬專案](#scrolling-a-virtualized-item-on-screen)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

專案視圖是使用者介面元件，可讓使用者查看檔案和其他專案並與其互動。 在 Windows 7 中，[專案] 視圖會取代 [清單視圖] 控制項，以便在 Windows 檔案總管的預設視圖中呈現專案。 [專案] 視圖也會用於 [一般專案] 對話方塊中，[開始] 功能表搜尋結果，以及其他使用 Explorer 瀏覽器控制項的 Windows 7 UI 元素。 相較于清單視圖控制項，[專案] 視圖會為使用者提供下列優點：

-   Items View 可以用更實用、更理想且相關的方式來呈現專案，讓使用者可以更輕鬆、快速且 enjoyably 地尋找及整理專案。
-   專案視圖可以顯示具有不同效能特性之資料來源中的大型專案集，讓使用者能夠流覽和搜尋跨多個來源的整個專案集合。

下圖顯示 Windows 檔案總管中的專案視圖。

![顯示 windows explorer 和專案 view 元件的螢幕擷取畫面](images/itemsview.gif)

從開發人員的觀點來看，[專案] 視圖的一般結構和功能類似于清單視圖控制項。 主要差異在於專案視圖支援虛擬化，而清單視圖控制項則不支援。 此外，專案視圖會使用兩個新的消費者介面自動化介面，以確保可存取專案視圖所提供的虛擬化內容。 本主題的下列各節將說明這些介面。

如需消費者介面自動化中虛擬化的一般資訊，請參閱 [使用虛擬化專案](uiauto-workingwithvirtualizeditems.md)。

## <a name="items-view-tree-structure"></a>專案視圖樹狀結構

在消費者介面自動化樹狀結構中，專案視圖的最上層消費者介面自動化專案的名稱為 "ItemsView"，而控制項類型為 "list"。 在上圖中，ItemsView 消費者介面自動化元素以紅色框住。 各種消費者介面自動化專案都存在於 ItemsView 的最上層，但本檔中只會參考其他兩個消費者介面自動化元素：群組專案和清單專案。

群組專案是包含該群組所有清單專案的消費者介面自動化專案，其控制項類型是 "Group"，而其名稱會根據組名而有所不同。 在上圖中，第一個群組專案同時包含 "A-H (1) " 標頭和 "Folder" 清單專案，且其名稱為 "A-H"。

清單專案是代表視圖中分葉專案的消費者介面自動化專案，其控制項類型為「專案名稱」，而其名稱會根據專案名稱而有所不同。 在上圖中，清單元素是分葉元素，例如「資料夾」、「音樂」和「圖片」。 這三個消費者介面自動化專案是由本檔其餘部分中的「詞彙 ItemsView 元素」、「群組元素」和「專案組合」元素所參考。

## <a name="virtualization"></a>虛擬化

專案視圖會使用虛擬化，這表示不會從系統提取 view 可見區域以外的專案，也不會建立這些專案的 UI 標記法。 這些專案稱為 *虛擬化專案*。 因為它們不會建立，所以虛擬化專案沒有消費者介面自動化元素，因此當消費者介面自動化用戶端列舉樹狀結構時，不會出現在消費者介面自動化樹狀目錄中。 此外，消費者介面自動化控制項模式只會在可見的元素上運作。 例如，當用戶端呼叫 [**IUIAutomationSelectionPattern：： GetCurrentSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-getcurrentselection)方法時，[選取](uiauto-implementingselection.md)控制項模式只會傳回可見的選取專案。

專案視圖支援抓取下列虛擬化專案相關資訊的能力：

-   專案總數的計數，包括虛擬化專案
-   虛擬化專案的消費者介面自動化元素
-   已選取之虛擬化專案的消費者介面自動化元素

## <a name="obtaining-a-count-of-all-items"></a>取得所有專案的計數

用戶端可以使用 ItemsView 元素來取得所有專案的計數，以及所選取專案的計數。 ItemsView 元素提供兩種方式來取得這些計數。 第一個是取得 ItemsView 專案的 ItemStatus 屬性，而第二個則是從 ItemsView 元素取得自訂屬性。

ItemStatus 屬性是一個字串，可指定專案總數的計數和選取專案的計數（以逗號分隔）。 例如： "3 個專案，已選取1個專案"。 這個字串是當地語系化的，可直接傳達給使用者。

ItemsView 元素的自訂屬性包含專案計數的一個屬性，而另一個屬性則包含選取專案計數。 其中包括：

-   ItemCount \_ 屬性 \_ GUID (ABBF5C45-5CCC-47b7-BB4E-87CB87BBD162) -view 中所有唯一專案的計數。 如果依據多重值屬性分組 (MVP) 讓單一專案可以多次出現，則每個專案只會計算一次。

     (UIAutomationType： [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype)，程式設計名稱： "ItemCount" ) 

-   SelectedItemCount \_ 屬性 \_ GUID (92A053DA-2969-4021-BF27-514CFC2E4A69) -在 view 中選取的所有唯一專案計數。 如果依據多重值屬性分組 (MVP) 讓單一專案可以多次出現，則每個專案只會計算一次。

     (UIAutomationType： [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype)，程式設計名稱： "SelectedItemCount" ) 

這些自訂屬性是在 Shlguid 中定義，其中包含在 Windows 軟體開發套件 (SDK) 中，而這些屬性則是透過 [**IUIAutomationRegistrar：： RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty)方法來註冊。 消費者介面自動化用戶端會使用 **RegisterProperty** 來抓取自訂屬性 (PROPERTYIDs) 的屬性識別碼。

## <a name="obtaining-an-item-index-with-respect-to-all-items"></a>取得與所有專案相關的專案索引

用戶端可以取得專案的索引，方法是取得專案的 ItemStatus 屬性，或取得 [專案] 元素的自訂屬性。

ItemStatus 屬性是一個字串，其中包含與專案總數相關之專案的索引。 例如：「專案 1/3」。 這個字串是當地語系化的，可直接傳達給使用者。

下列自訂屬性會取得 [專案] 元素的專案索引：

-   ItemIndex \_ 屬性 \_ GUID (92A053DA-2969-4021-BF27-514CFC2E4A69) -專案的以1為基的絕對索引。 如果依據多重值屬性分組 (MVP) 讓單一專案可以出現兩次，則專案的每個外觀都會取得個別的索引。

     (UIAutomationType： [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype)，程式設計名稱： "ItemIndex" ) 

這個自訂屬性是在 Shlguid 中定義，其中包含在 Windows SDK 中，並透過 [**IUIAutomationRegistrar：： RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty)方法註冊。 消費者介面自動化用戶端會使用 **RegisterProperty** 來抓取自訂屬性 (PROPERTYIDs) 的屬性識別碼。

## <a name="obtaining-a-reference-to-a-vitualized-item"></a>取得 Vitualized 專案的參考

ItemsView 元素會將 [>itemcontainer](uiauto-implementingitemcontainer.md) 控制項模式 ([**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider)) 介面，以允許用戶端取得虛擬化專案的消費者介面自動化專案， (可見區域以外的專案) 。 ItemsView 可讓用戶端藉由搜尋名稱和選取屬性來尋找 [專案] 元素，嘗試搜尋任何其他屬性將會失敗。

虛擬專案只會將 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式實 ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) 介面) 。 因為虛擬化消費者介面自動化專案所代表的專案尚未存在，所以嘗試取得專案的任何其他控制項模式或屬性將會失敗。

專案組合和群組專案都已虛擬化，但是只能從 [>itemcontainer](uiauto-implementingitemcontainer.md) 控制項模式傳回專案組合元素。 由於呼叫 [**IUIAutomationItemContainerPattern：： FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) 方法會在 UI 執行緒上執行，而且會封鎖，因此在 **FindItemByProperty** 傳回之前，view 不會回應，而且提供者上的任何其他方法呼叫都必須等到 **FindItemByProperty** 完成為止。 在某些情況下， **FindItemByProperty** 必須在傳回之前處理整個資料集，這可能需要大量資源。 將 **Null** 指定為起始元素，會導致 **FindItemByProperty** 開始使用 view 中的第一個專案進行搜尋。

ItemsView 支援下列 [**FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty)屬性：

-   Name (UIA \_ NamePropertyId) -搜尋名稱完全符合指定字串的第一個專案。 搜尋是不區分大小寫的。 不支援萬用字元或部分相符。 如果指定了 **Null** 名稱，則會傳回起始元素之後的下一個專案。 指定 **Null** 名稱可讓消費者介面自動化用戶端列舉視圖中的所有專案;但是，不建議您列舉所有的專案，因為它會使 view 中的所有專案都能實現。
-   SelectionItem \_ IsSelected (UIA \_ SelectionItemIsSelectedPropertyId) —搜尋 SelectionItem \_ IsSelected 屬性符合指定值的第一個專案。 指定 **TRUE** 以尋找第一個選取的專案，或指定 **FALSE** 來尋找第一個未選取的專案。 列舉所有選取的專案時請小心，因為選取的專案數目可能很大，特別是當使用者已選取所有專案時。

## <a name="scrolling-a-virtualized-item-on-screen"></a>在螢幕上滾動虛擬專案

取得虛擬化 (的) 專案之消費者介面自動化專案的參考之後，用戶端就可以使用 [VirtualizedItem](uiauto-implementingvirtualizeditem.md)控制項模式的 [**IUIAutomationVirtualizeItemPattern：：**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) get-help 方法，將專案滾動至 view。 在瞭解專案之後，就會看到該專案，而且通常與 [專案組合] 元素相關聯的所有屬性和控制項模式都可供用戶端使用。

只有 [**IUIAutomationItemContainerPattern：： FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) 方法所取得的 [專案] 元素會公開 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式。 當螢幕上的專案在螢幕上滾動時，元素會變成無效，而且用戶端必須呼叫 **FindItemByProperty** 來取得螢幕上的參考。

您也可以使用 [滾動](uiauto-implementingscroll.md) 條控制項模式 (或使用捲軸) ，將專案移入和移出視野。 專案和群組會在進入視野時實現，並會在其離開視圖時進行虛擬化。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用虛擬化專案](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




