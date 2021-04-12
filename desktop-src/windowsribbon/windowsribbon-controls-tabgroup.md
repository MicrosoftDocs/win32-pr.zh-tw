---
title: Tab 群組
description: 索引標籤群組是在執行時間根據檔或工作區狀態隱藏或顯示的內容控制項。 此索引標籤群組包含一組內容相關的索引標籤控制項。
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316009"
---
# <a name="tab-group"></a><span data-ttu-id="2a561-104">Tab 群組</span><span class="sxs-lookup"><span data-stu-id="2a561-104">Tab Group</span></span>

<span data-ttu-id="2a561-105">索引標籤群組是在執行時間根據檔或工作區狀態隱藏或顯示的內容控制項。</span><span class="sxs-lookup"><span data-stu-id="2a561-105">A Tab Group is a contextual control that is hidden or displayed at run time, based on a document or workspace state.</span></span> <span data-ttu-id="2a561-106">此索引標籤群組包含一組內容相關的 [選項卡](windowsribbon-controls-tab.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="2a561-106">The Tab Group contains a set of context-related [Tab](windowsribbon-controls-tab.md) controls.</span></span>

-   [<span data-ttu-id="2a561-107">詳細資料</span><span class="sxs-lookup"><span data-stu-id="2a561-107">Details</span></span>](#details)
-   [<span data-ttu-id="2a561-108">索引標籤群組屬性</span><span class="sxs-lookup"><span data-stu-id="2a561-108">Tab Group Properties</span></span>](#tab-group-properties)
-   [<span data-ttu-id="2a561-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a561-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="2a561-110">詳細資料</span><span class="sxs-lookup"><span data-stu-id="2a561-110">Details</span></span>

<span data-ttu-id="2a561-111">一般而言，在特定檔或工作區狀態期間，例如當使用者選取特定物件類型時，會顯示索引標籤群組。</span><span class="sxs-lookup"><span data-stu-id="2a561-111">Typically, a Tab Group is displayed during specific document or workspace states, such as when a user selects a particular object type.</span></span> <span data-ttu-id="2a561-112">例如，選取包含在資料表標頭中的影像時，可能需要顯示各種內容索引標籤，以同時公開資料表和影像功能。</span><span class="sxs-lookup"><span data-stu-id="2a561-112">For example, the selection of an image contained in the header of a table might require various contextual tabs to be displayed that expose both table and image functionality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a561-113">索引標籤群組不支援 [應用程式模式](ribbon-applicationmodes.md)。</span><span class="sxs-lookup"><span data-stu-id="2a561-113">A Tab Group does not support [application modes](ribbon-applicationmodes.md).</span></span> <span data-ttu-id="2a561-114">不過，您可以在索引標籤群組內 [的個別索引](windowsribbon-controls-tab.md) 標籤控制項。</span><span class="sxs-lookup"><span data-stu-id="2a561-114">However, the individual [Tab](windowsribbon-controls-tab.md) controls within a Tab Group may.</span></span>

 

<span data-ttu-id="2a561-115">下列螢幕擷取畫面顯示 Windows 7 繪圖 [的內容](windowsribbon-controls-tab.md) 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2a561-115">The following screen shot shows a contextual [Tab](windowsribbon-controls-tab.md) from Windows 7 Paint.</span></span>

![顯示內容索引標籤控制項的螢幕擷取畫面。](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a><span data-ttu-id="2a561-117">索引標籤群組屬性</span><span class="sxs-lookup"><span data-stu-id="2a561-117">Tab Group Properties</span></span>

<span data-ttu-id="2a561-118">功能區架構會為索引標籤群組控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="2a561-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab Group control.</span></span>

<span data-ttu-id="2a561-119">一般而言，功能區 UI 中的索引標籤群組屬性會透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法，使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="2a561-119">Typically, a Tab Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="2a561-120">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="2a561-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="2a561-121">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="2a561-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="2a561-122">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="2a561-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="2a561-123">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="2a561-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="2a561-124">下表列出與 [索引標籤] 群組控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2a561-124">The following table lists the property keys that are associated with the Tab Group control.</span></span>



| <span data-ttu-id="2a561-125">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="2a561-125">Property Key</span></span>                                                                                     | <span data-ttu-id="2a561-126">備註</span><span class="sxs-lookup"><span data-stu-id="2a561-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a561-127">UI \_ PKEY \_ CoNtextAvailable</span><span class="sxs-lookup"><span data-stu-id="2a561-127">UI\_PKEY\_ContextAvailable</span></span>](windowsribbon-reference-properties-uipkey-contextavailable.md)     | <span data-ttu-id="2a561-128">支援 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 和 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)。</span><span class="sxs-lookup"><span data-stu-id="2a561-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="2a561-129">UI \_ PKEY \_ 按鍵提示</span><span class="sxs-lookup"><span data-stu-id="2a561-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="2a561-130">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2a561-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="2a561-131">UI \_ PKEY \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="2a561-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="2a561-132">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2a561-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="2a561-133">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="2a561-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="2a561-134">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2a561-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="2a561-135">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="2a561-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="2a561-136">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2a561-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="2a561-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a561-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a561-138">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="2a561-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="2a561-139">**TabGroup 標記元素**</span><span class="sxs-lookup"><span data-stu-id="2a561-139">**TabGroup markup element**</span></span>](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 