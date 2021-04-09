---
title: '按鈕 (Windows 功能區架構) '
description: 按鈕是使用者可以按一下來提供應用程式輸入的控制項。
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093596"
---
# <a name="button-windows-ribbon-framework"></a><span data-ttu-id="aee1f-103">按鈕 (Windows 功能區架構) </span><span class="sxs-lookup"><span data-stu-id="aee1f-103">Button (Windows Ribbon Framework)</span></span>

<span data-ttu-id="aee1f-104">按鈕是使用者可以按一下來提供應用程式輸入的控制項。</span><span class="sxs-lookup"><span data-stu-id="aee1f-104">The Button is a control the user can click to provide input to an application.</span></span>

-   [<span data-ttu-id="aee1f-105">簡介</span><span class="sxs-lookup"><span data-stu-id="aee1f-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="aee1f-106">按鈕屬性</span><span class="sxs-lookup"><span data-stu-id="aee1f-106">Button Properties</span></span>](#button-properties)
-   [<span data-ttu-id="aee1f-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="aee1f-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="aee1f-108">簡介</span><span class="sxs-lookup"><span data-stu-id="aee1f-108">Introduction</span></span>

<span data-ttu-id="aee1f-109">下列螢幕擷取畫面包含功能區按鈕元素的三個範例。</span><span class="sxs-lookup"><span data-stu-id="aee1f-109">The following screen shot contains three examples of the Ribbon Button element.</span></span>

![microsoft wordpad 功能區中按鈕控制項的螢幕擷取畫面。](images/controls/button.png)

## <a name="button-properties"></a><span data-ttu-id="aee1f-111">按鈕屬性</span><span class="sxs-lookup"><span data-stu-id="aee1f-111">Button Properties</span></span>

<span data-ttu-id="aee1f-112">功能區架構會為按鈕控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="aee1f-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Button control.</span></span>

<span data-ttu-id="aee1f-113">通常會在功能區 UI 中更新按鈕屬性，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="aee1f-113">Typically, a Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="aee1f-114">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="aee1f-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="aee1f-115">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="aee1f-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="aee1f-116">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="aee1f-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="aee1f-117">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="aee1f-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="aee1f-118">下表列出與按鈕控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="aee1f-118">The following table lists the property keys that are associated with the Button control.</span></span>



| <span data-ttu-id="aee1f-119">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="aee1f-119">Property Key</span></span>                                                                                             | <span data-ttu-id="aee1f-120">備註</span><span class="sxs-lookup"><span data-stu-id="aee1f-120">Notes</span></span>                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aee1f-121">UI \_ PKEY \_ 已啟用</span><span class="sxs-lookup"><span data-stu-id="aee1f-121">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                               | <span data-ttu-id="aee1f-122">支援 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 和 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)。</span><span class="sxs-lookup"><span data-stu-id="aee1f-122">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="aee1f-123">UI \_ PKEY \_ 按鍵提示</span><span class="sxs-lookup"><span data-stu-id="aee1f-123">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                 | <span data-ttu-id="aee1f-124">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="aee1f-124">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="aee1f-125">UI \_ PKEY \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="aee1f-125">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                                   | <span data-ttu-id="aee1f-126">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="aee1f-126">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="aee1f-127">UI \_ PKEY \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="aee1f-127">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)             | <span data-ttu-id="aee1f-128">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="aee1f-128">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="aee1f-129">UI \_ PKEY \_ LargeHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="aee1f-129">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | <span data-ttu-id="aee1f-130">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="aee1f-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="aee1f-131">UI \_ PKEY \_ LargeImage</span><span class="sxs-lookup"><span data-stu-id="aee1f-131">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)                         | <span data-ttu-id="aee1f-132">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="aee1f-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="aee1f-133">UI \_ PKEY \_ SmallHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="aee1f-133">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | <span data-ttu-id="aee1f-134">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="aee1f-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="aee1f-135">UI \_ PKEY \_ SmallImage</span><span class="sxs-lookup"><span data-stu-id="aee1f-135">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)                         | <span data-ttu-id="aee1f-136">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="aee1f-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="aee1f-137">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="aee1f-137">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | <span data-ttu-id="aee1f-138">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="aee1f-138">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="aee1f-139">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="aee1f-139">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | <span data-ttu-id="aee1f-140">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="aee1f-140">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="aee1f-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="aee1f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aee1f-142">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="aee1f-142">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="aee1f-143">**按鈕標記元素**</span><span class="sxs-lookup"><span data-stu-id="aee1f-143">**Button markup element**</span></span>](windowsribbon-element-button.md)
</dt> </dl>

 

 
