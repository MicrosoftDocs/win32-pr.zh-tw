---
title: 'Tab (Windows 功能區架構) '
description: 索引標籤包含相關控制項的群組。
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317076"
---
# <a name="tab-windows-ribbon-framework"></a><span data-ttu-id="a71a4-103">Tab (Windows 功能區架構) </span><span class="sxs-lookup"><span data-stu-id="a71a4-103">Tab (Windows Ribbon Framework)</span></span>

<span data-ttu-id="a71a4-104">索引標籤包含相關控制項的 [群組](windowsribbon-controls-group.md) 。</span><span class="sxs-lookup"><span data-stu-id="a71a4-104">A Tab contains [groups](windowsribbon-controls-group.md) of related controls.</span></span>

-   [<span data-ttu-id="a71a4-105">詳細資料</span><span class="sxs-lookup"><span data-stu-id="a71a4-105">Details</span></span>](#details)
-   [<span data-ttu-id="a71a4-106">索引標籤屬性</span><span class="sxs-lookup"><span data-stu-id="a71a4-106">Tab Properties</span></span>](#tab-properties)
-   [<span data-ttu-id="a71a4-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="a71a4-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="a71a4-108">詳細資料</span><span class="sxs-lookup"><span data-stu-id="a71a4-108">Details</span></span>

<span data-ttu-id="a71a4-109">功能區架構中有三種類型的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="a71a4-109">There are three types of Tab in the Ribbon framework.</span></span>



| <span data-ttu-id="a71a4-110">類型</span><span class="sxs-lookup"><span data-stu-id="a71a4-110">Type</span></span>               | <span data-ttu-id="a71a4-111">Description</span><span class="sxs-lookup"><span data-stu-id="a71a4-111">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a71a4-112">**核心索引標籤**</span><span class="sxs-lookup"><span data-stu-id="a71a4-112">**Core tab**</span></span>       | <span data-ttu-id="a71a4-113">用來組織應用程式預設功能的核心索引標籤。</span><span class="sxs-lookup"><span data-stu-id="a71a4-113">Core tabs that organize the default functions of the application.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="a71a4-114">**內容索引標籤**</span><span class="sxs-lookup"><span data-stu-id="a71a4-114">**Contextual tab**</span></span> | <span data-ttu-id="a71a4-115">在特定檔或工作區狀態期間顯示的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="a71a4-115">Tabs that are displayed during specific document or workspace states.</span></span> <span data-ttu-id="a71a4-116">例如，如果使用者選取特定物件類型（例如資料表標頭中包含的影像），則可能會顯示各種內容索引標籤，以同時公開資料表和影像功能。</span><span class="sxs-lookup"><span data-stu-id="a71a4-116">For example, if a user selects a particular object type, such as an image contained in the header of a table, then various contextual tabs might be displayed that expose both table and image functionality.</span></span> |
| <span data-ttu-id="a71a4-117">**模式索引標籤**</span><span class="sxs-lookup"><span data-stu-id="a71a4-117">**Modal tab**</span></span>      | <span data-ttu-id="a71a4-118">在特定檔或工作區 [應用程式模式](ribbon-applicationmodes.md)期間顯示的核心索引標籤，例如 [預覽列印]。</span><span class="sxs-lookup"><span data-stu-id="a71a4-118">Core tabs that are displayed during a specific document or workspace [application mode](ribbon-applicationmodes.md), such as print preview.</span></span>                                                                                                                                        |



 

<span data-ttu-id="a71a4-119">下列螢幕擷取畫面顯示 Windows 7 繪圖的核心索引標籤。</span><span class="sxs-lookup"><span data-stu-id="a71a4-119">The following screen shot shows a core Tab from Windows 7 Paint.</span></span>

![顯示核心索引標籤控制項的螢幕擷取畫面。](images/controls/coretab.png)

## <a name="tab-properties"></a><span data-ttu-id="a71a4-121">索引標籤屬性</span><span class="sxs-lookup"><span data-stu-id="a71a4-121">Tab Properties</span></span>

<span data-ttu-id="a71a4-122">功能區架構會定義索引標籤控制項的 [屬性索引鍵](windowsribbon-reference-properties.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="a71a4-122">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab control.</span></span>

<span data-ttu-id="a71a4-123">通常會在功能區 UI 中更新索引標籤屬性，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="a71a4-123">Typically, a Tab property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="a71a4-124">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="a71a4-124">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="a71a4-125">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="a71a4-125">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="a71a4-126">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="a71a4-126">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="a71a4-127">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="a71a4-127">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="a71a4-128">下表列出與索引標籤控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a71a4-128">The following table lists the property keys that are associated with the Tab control.</span></span>



| <span data-ttu-id="a71a4-129">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="a71a4-129">Property Key</span></span>                                                                                     | <span data-ttu-id="a71a4-130">備註</span><span class="sxs-lookup"><span data-stu-id="a71a4-130">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="a71a4-131">UI \_ PKEY \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="a71a4-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="a71a4-132">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="a71a4-132">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="a71a4-133">UI \_ PKEY \_ 按鍵提示</span><span class="sxs-lookup"><span data-stu-id="a71a4-133">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="a71a4-134">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="a71a4-134">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="a71a4-135">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="a71a4-135">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="a71a4-136">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="a71a4-136">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="a71a4-137">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="a71a4-137">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="a71a4-138">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="a71a4-138">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a71a4-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="a71a4-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a71a4-140">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="a71a4-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="a71a4-141">**Tab 標記元素**</span><span class="sxs-lookup"><span data-stu-id="a71a4-141">**Tab markup element**</span></span>](windowsribbon-element-tab.md)
</dt> </dl>

 

 
