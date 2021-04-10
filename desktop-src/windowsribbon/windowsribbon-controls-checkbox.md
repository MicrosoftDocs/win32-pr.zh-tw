---
title: 核取方塊
description: 核取方塊是使用者可按一下以提供應用程式輸入的控制項。 控制項提供以視覺化方式呈現的切換狀態。
ms.assetid: fe07aa5c-1818-41e2-b48d-5fefe50d733f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e283facf81e8c3d2adad670329fcf0cf168d09
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103683722"
---
# <a name="check-box"></a><span data-ttu-id="c603a-104">核取方塊</span><span class="sxs-lookup"><span data-stu-id="c603a-104">Check Box</span></span>

<span data-ttu-id="c603a-105">核取方塊是使用者可按一下以提供應用程式輸入的控制項。</span><span class="sxs-lookup"><span data-stu-id="c603a-105">The Check Box is a control the user can click to provide input to an application.</span></span> <span data-ttu-id="c603a-106">控制項提供以視覺化方式呈現的切換狀態。</span><span class="sxs-lookup"><span data-stu-id="c603a-106">The control provides a toggle state that is represented visually.</span></span>

-   [<span data-ttu-id="c603a-107">詳細資料</span><span class="sxs-lookup"><span data-stu-id="c603a-107">Details</span></span>](#details)
-   [<span data-ttu-id="c603a-108">核取方塊屬性</span><span class="sxs-lookup"><span data-stu-id="c603a-108">Check Box Properties</span></span>](#check-box-properties)
-   [<span data-ttu-id="c603a-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="c603a-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="c603a-110">詳細資料</span><span class="sxs-lookup"><span data-stu-id="c603a-110">Details</span></span>

<span data-ttu-id="c603a-111">此核取方塊不支援第三個或不定的狀態。</span><span class="sxs-lookup"><span data-stu-id="c603a-111">The Check Box does not support a tertiary, or indeterminate, state.</span></span>

<span data-ttu-id="c603a-112">下列螢幕擷取畫面說明功能區核取方塊元素。</span><span class="sxs-lookup"><span data-stu-id="c603a-112">The following screen shot illustrates the Ribbon Check Box element.</span></span>

![microsoft 油漆功能區中核取方塊控制項的螢幕擷取畫面。](images/controls/checkbox.png)

## <a name="check-box-properties"></a><span data-ttu-id="c603a-114">核取方塊屬性</span><span class="sxs-lookup"><span data-stu-id="c603a-114">Check Box Properties</span></span>

<span data-ttu-id="c603a-115">功能區架構會為核取方塊控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="c603a-115">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Check Box control.</span></span>

<span data-ttu-id="c603a-116">通常會在功能區 UI 中更新核取方塊屬性，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="c603a-116">Typically, a Check Box property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="c603a-117">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="c603a-117">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="c603a-118">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="c603a-118">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="c603a-119">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="c603a-119">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="c603a-120">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="c603a-120">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="c603a-121">下表列出與核取方塊控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c603a-121">The following table lists the property keys that are associated with the Check Box control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c603a-122">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="c603a-122">Property Key</span></span></th>
<th><span data-ttu-id="c603a-123">備註</span><span class="sxs-lookup"><span data-stu-id="c603a-123">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c603a-124"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span><span class="sxs-lookup"><span data-stu-id="c603a-124"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span></span></td>
<td><span data-ttu-id="c603a-125">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="c603a-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c603a-126">如果與控制項相關聯的命令透過呼叫 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework：： InvalidateUICommand</strong></a>而失效，則架構 <code>UI_INVALIDATIONS_VALUE</code> 會在傳遞做為 <em>旗標</em>的值時查詢此屬性。</span><span class="sxs-lookup"><span data-stu-id="c603a-126">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c603a-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="c603a-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="c603a-128">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="c603a-128">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c603a-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="c603a-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="c603a-130">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="c603a-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c603a-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="c603a-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="c603a-132">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="c603a-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c603a-133"><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></span><span class="sxs-lookup"><span data-stu-id="c603a-133"><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></span></span></td>
<td><span data-ttu-id="c603a-134">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="c603a-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c603a-135"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="c603a-135"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="c603a-136">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="c603a-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c603a-137"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="c603a-137"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="c603a-138">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="c603a-138">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c603a-139"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="c603a-139"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="c603a-140">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="c603a-140">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c603a-141"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="c603a-141"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="c603a-142">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="c603a-142">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c603a-143"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="c603a-143"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="c603a-144">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="c603a-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c603a-145"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="c603a-145"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="c603a-146">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="c603a-146">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c603a-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="c603a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c603a-148">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="c603a-148">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="c603a-149">**CheckBox 標記元素**</span><span class="sxs-lookup"><span data-stu-id="c603a-149">**CheckBox markup element**</span></span>](windowsribbon-element-checkbox.md)
</dt> </dl>

