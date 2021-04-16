---
title: 最近的項目
description: '[最近使用的專案] 清單是應用程式功能表中的一個窗格，會顯示應用程式最近使用的 (MRU) 專案。'
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f78c01fc4d6cc830eba644f7dcf22b6fb03e82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104550941"
---
# <a name="recent-items"></a><span data-ttu-id="a2a18-103">最近的項目</span><span class="sxs-lookup"><span data-stu-id="a2a18-103">Recent Items</span></span>

<span data-ttu-id="a2a18-104">[最近使用的專案] 清單是 [應用程式功能表](windowsribbon-controls-applicationmenu.md) 中的一個窗格，會顯示應用程式最近使用的 (MRU) 專案。</span><span class="sxs-lookup"><span data-stu-id="a2a18-104">The Recent Items list is a pane in the [Application Menu](windowsribbon-controls-applicationmenu.md) that displays the most recently used (MRU) items for an application.</span></span>

-   [<span data-ttu-id="a2a18-105">詳細資料</span><span class="sxs-lookup"><span data-stu-id="a2a18-105">Details</span></span>](#details)
-   [<span data-ttu-id="a2a18-106">最近使用的專案屬性</span><span class="sxs-lookup"><span data-stu-id="a2a18-106">Recent Items Properties</span></span>](#recent-items-properties)
-   [<span data-ttu-id="a2a18-107">備註</span><span class="sxs-lookup"><span data-stu-id="a2a18-107">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="a2a18-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="a2a18-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="a2a18-109">詳細資料</span><span class="sxs-lookup"><span data-stu-id="a2a18-109">Details</span></span>

<span data-ttu-id="a2a18-110">下列螢幕擷取畫面說明 Windows 7) 的 [WordPad] 中的 [最近的專案] 清單。</span><span class="sxs-lookup"><span data-stu-id="a2a18-110">The following screen shot illustrates a Recent Items list from WordPad for Windows 7).</span></span>

![microsoft 油漆功能區中 [最近使用的專案] 清單的螢幕擷取畫面。](images/controls/recentitems.png)

<span data-ttu-id="a2a18-112">[應用程式功能表](windowsribbon-controls-applicationmenu.md)最多隻能有一個 [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)清單（以 **ApplicationMenu. RecentItems** 元素表示），以顯示最近使用過的檔、圖片、電影和其他使用者正在處理的專案。</span><span class="sxs-lookup"><span data-stu-id="a2a18-112">The [Application Menu](windowsribbon-controls-applicationmenu.md) can have at most one [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) list, represented by an **ApplicationMenu.RecentItems** element, for displaying recent documents, pictures, movies, and other projects a user has been working on.</span></span> <span data-ttu-id="a2a18-113">所列專案的數目範圍從零到標記中指定的最大數目，預設值為10。</span><span class="sxs-lookup"><span data-stu-id="a2a18-113">The number of listed items ranges from zero to the maximum number specified in markup, with a default value of ten.</span></span> <span data-ttu-id="a2a18-114">最近的專案會顯示為字串的編號清單，表示檔案名。</span><span class="sxs-lookup"><span data-stu-id="a2a18-114">The recent items are displayed as a numbered list of strings indicating file names.</span></span> <span data-ttu-id="a2a18-115">建議使用 [**LabelDescription**](windowsribbon-element-command-labeldescription.md) 屬性來提供檔案位置的完整路徑，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="a2a18-115">It is recommended that the [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) property be used to give the full path for the file location, as shown in the following screen shot .</span></span>

![[應用程式] 功能表中 [最近使用的專案] 清單的螢幕擷取畫面。](images/overviews/applicationmenu-menurecentitems.png)

<span data-ttu-id="a2a18-117">[**RecentItems**](windowsribbon-element-recentitems.md)元素具有 *EnablePinning* 屬性，如果設定為 `true` ，會在清單中的每個專案右邊顯示釘選圖示，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="a2a18-117">The [**RecentItems**](windowsribbon-element-recentitems.md) element has an *EnablePinning* attribute that, if set to `true`, displays a pin icon to the right of each item in the list, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="a2a18-118">如果未指定 *EnablePinning* 屬性，預設會啟用釘選。</span><span class="sxs-lookup"><span data-stu-id="a2a18-118">Pinning is enabled by default if the *EnablePinning* attribute is not specified.</span></span>

 

![最近專案釘選在應用程式功能表中的螢幕擷取畫面。](images/overviews/applicationmenu-menurecentitemspinned.png)

<span data-ttu-id="a2a18-120">釘選演算法的目的是要防止專案從 [ **最近的專案** ] 清單中下降。</span><span class="sxs-lookup"><span data-stu-id="a2a18-120">The pinning algorithm is intended to keep items from falling off the **Recent items** list.</span></span> <span data-ttu-id="a2a18-121">此演算法會產生下列行為：</span><span class="sxs-lookup"><span data-stu-id="a2a18-121">The algorithm produces the following behavior:</span></span>

-   <span data-ttu-id="a2a18-122">在 [ **最近使用的專案** ] 清單的頂端，一律會加入新專案。</span><span class="sxs-lookup"><span data-stu-id="a2a18-122">A new item is always added at the top of the **Recent items** list.</span></span>
-   <span data-ttu-id="a2a18-123">專案會在一段時間內于清單中下移。</span><span class="sxs-lookup"><span data-stu-id="a2a18-123">Items will move down in the list over time.</span></span> <span data-ttu-id="a2a18-124">一旦清單填滿 (達到 [標記) 中指定的最大專案數，當新專案新增至清單頂端時，較舊的專案就會落在清單底部。</span><span class="sxs-lookup"><span data-stu-id="a2a18-124">Once the list is full (reaches the maximum number of items specified in markup), older items fall off the bottom of the list as new items are added to the top of the list.</span></span>
-   <span data-ttu-id="a2a18-125">如果專案已出現在清單中的某處，但再次存取，則會移回清單的最上方。</span><span class="sxs-lookup"><span data-stu-id="a2a18-125">If an item already appears somewhere in the list but is accessed again, it moves back to the top of the list.</span></span>
-   <span data-ttu-id="a2a18-126">如果專案已釘選，它仍會往下移動清單，但不會落在底部。</span><span class="sxs-lookup"><span data-stu-id="a2a18-126">If an item is pinned, it will still travel down the list, but it will not fall off the bottom.</span></span> <span data-ttu-id="a2a18-127">相反地，當清單填滿之後，當新專案新增至清單時，釘選的專案上方第一個取消釘選的專案會下降。</span><span class="sxs-lookup"><span data-stu-id="a2a18-127">Instead, once the list is full, the first unpinned item above the pinned item will fall off when a new item is added to the list.</span></span>
-   <span data-ttu-id="a2a18-128">如果已釘選的專案數目達到專案數上限，則在取消固定專案之前，不會將任何新專案新增至清單。</span><span class="sxs-lookup"><span data-stu-id="a2a18-128">If the number of pinned items ever reaches the maximum number of items, then no new items will get added to the list until an item is unpinned.</span></span>

## <a name="recent-items-properties"></a><span data-ttu-id="a2a18-129">最近使用的專案屬性</span><span class="sxs-lookup"><span data-stu-id="a2a18-129">Recent Items Properties</span></span>

<span data-ttu-id="a2a18-130">功能區架構會為最近的 Items 控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="a2a18-130">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Recent Items control.</span></span>

<span data-ttu-id="a2a18-131">一般來說，功能區 UI 中的 [最近的專案] 屬性會透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效，藉此更新。</span><span class="sxs-lookup"><span data-stu-id="a2a18-131">Typically, a Recent Items property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="a2a18-132">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="a2a18-132">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="a2a18-133">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="a2a18-133">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="a2a18-134">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="a2a18-134">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="a2a18-135">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="a2a18-135">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="a2a18-136">下表列出與 [最近的專案] 控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a2a18-136">The following table lists the property keys that are associated with the Recent Items control.</span></span>



| <span data-ttu-id="a2a18-137">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="a2a18-137">Property Key</span></span>                                                                       | <span data-ttu-id="a2a18-138">備註</span><span class="sxs-lookup"><span data-stu-id="a2a18-138">Notes</span></span>                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="a2a18-139">UI \_ PKEY \_ 按鍵提示</span><span class="sxs-lookup"><span data-stu-id="a2a18-139">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)           | <span data-ttu-id="a2a18-140">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="a2a18-140">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="a2a18-141">UI \_ PKEY \_ RecentItems</span><span class="sxs-lookup"><span data-stu-id="a2a18-141">UI\_PKEY\_RecentItems</span></span>](windowsribbon-reference-properties-uipkey-recentitems.md) | <span data-ttu-id="a2a18-142">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="a2a18-142">Can only be updated through invalidation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a2a18-143">備註</span><span class="sxs-lookup"><span data-stu-id="a2a18-143">Remarks</span></span>

<span data-ttu-id="a2a18-144">[IApplicationDocumentLists：： GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist)方法可以用來取得功能區應用程式的 WINDOWS Shell MRU 清單。</span><span class="sxs-lookup"><span data-stu-id="a2a18-144">The [IApplicationDocumentLists::GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) method can be used to retrieve the Windows Shell MRU list for the Ribbon application.</span></span> <span data-ttu-id="a2a18-145">然後，應用程式可以使用這個方法所抓取的物件來建立功能區架構所需的資料，以填入 [應用程式功能表](windowsribbon-controls-applicationmenu.md)的 [**最近的專案**] 清單。</span><span class="sxs-lookup"><span data-stu-id="a2a18-145">The object retrieved by this method can then be used by the application to create the data required by the Ribbon framework to populate the **Recent items** list of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

> [!Note]  
> <span data-ttu-id="a2a18-146">使用這個方法時， *listtype* 應該具有值 `ADLT_RECENT` 。</span><span class="sxs-lookup"><span data-stu-id="a2a18-146">When using this method, *listtype* should have the value `ADLT_RECENT`.</span></span>

 

<span data-ttu-id="a2a18-147">如需如何在功能區架構應用程式中執行 MRU 專案清單的範例，請參閱 [HTMLEditRibbon 範例](windowsribbon-htmleditribbonsample.md)。</span><span class="sxs-lookup"><span data-stu-id="a2a18-147">For an example of how to implement an MRU items list in a Ribbon framework application, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2a18-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="a2a18-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2a18-149">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="a2a18-149">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="a2a18-150">**最近使用的專案標記元素**</span><span class="sxs-lookup"><span data-stu-id="a2a18-150">**Recent items markup element**</span></span>](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 