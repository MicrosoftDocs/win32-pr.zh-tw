---
title: In-Ribbon 資源庫
description: In-Ribbon 圖庫是一個控制項，可在功能區中顯示相關專案或命令的集合。 如果資源庫中有太多專案，則會提供展開箭號，以在展開的窗格中顯示集合的其餘部分。
ms.assetid: d608dd0d-a0af-49a6-a129-7115195c0df2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef644128204fa0b20284dbb63368ef530b0dd0b3
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106996170"
---
# <a name="in-ribbon-gallery"></a><span data-ttu-id="e5758-104">In-Ribbon 資源庫</span><span class="sxs-lookup"><span data-stu-id="e5758-104">In-Ribbon Gallery</span></span>

<span data-ttu-id="e5758-105">In-Ribbon 圖庫是一個控制項，可在功能區中顯示相關專案或命令的集合。</span><span class="sxs-lookup"><span data-stu-id="e5758-105">The In-Ribbon Gallery is a control that displays a collection of related items or Commands in the Ribbon.</span></span> <span data-ttu-id="e5758-106">如果資源庫中有太多專案，則會提供展開箭號，以在展開的窗格中顯示集合的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="e5758-106">If there are too many items in the gallery, an expand arrow is provided to display the rest of the collection in an expanded pane.</span></span>

-   [<span data-ttu-id="e5758-107">詳細資料</span><span class="sxs-lookup"><span data-stu-id="e5758-107">Details</span></span>](#details)
-   [<span data-ttu-id="e5758-108">功能區元件庫屬性</span><span class="sxs-lookup"><span data-stu-id="e5758-108">In-Ribbon Gallery Properties</span></span>](#in-ribbon-gallery-properties)
-   [<span data-ttu-id="e5758-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5758-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="e5758-110">詳細資料</span><span class="sxs-lookup"><span data-stu-id="e5758-110">Details</span></span>

<span data-ttu-id="e5758-111">下列螢幕擷取畫面說明 Microsoft 小畫家中的功能區 In-Ribbon 資源庫控制項。</span><span class="sxs-lookup"><span data-stu-id="e5758-111">The following screen shot illustrates the Ribbon In-Ribbon Gallery control in Microsoft Paint.</span></span>

![microsoft 油漆功能區中 inribbongallery 控制項的螢幕擷取畫面。](images/controls/inribbongallery.png)

## <a name="in-ribbon-gallery-properties"></a><span data-ttu-id="e5758-113">In-Ribbon 資源庫屬性</span><span class="sxs-lookup"><span data-stu-id="e5758-113">In-Ribbon Gallery Properties</span></span>

<span data-ttu-id="e5758-114">功能區架構會為 In-Ribbon 資源庫控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="e5758-114">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the In-Ribbon Gallery control.</span></span>

<span data-ttu-id="e5758-115">通常會在功能區 UI 中更新 In-Ribbon 資源庫屬性，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="e5758-115">Typically, an In-Ribbon Gallery property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="e5758-116">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="e5758-116">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="e5758-117">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="e5758-117">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="e5758-118">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="e5758-118">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="e5758-119">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="e5758-119">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="e5758-120">下表列出與 In-Ribbon 資源庫控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e5758-120">The following table lists the property keys that are associated with the In-Ribbon Gallery control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5758-121">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="e5758-121">Property Key</span></span></th>
<th><span data-ttu-id="e5758-122">備註</span><span class="sxs-lookup"><span data-stu-id="e5758-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5758-123"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="e5758-123"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="e5758-124">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="e5758-124">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5758-125"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="e5758-125"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="e5758-126">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="e5758-126">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5758-127"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="e5758-127"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="e5758-128">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="e5758-128">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5758-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="e5758-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="e5758-130">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="e5758-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5758-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="e5758-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="e5758-132">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="e5758-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5758-133"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="e5758-133"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="e5758-134">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="e5758-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5758-135"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="e5758-135"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="e5758-136">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="e5758-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5758-137"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a> (僅適用于專案資源庫) </span><span class="sxs-lookup"><span data-stu-id="e5758-137"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(only valid for an item gallery)</span></span><br/></td>
<td><span data-ttu-id="e5758-138">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="e5758-138">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e5758-139">如果與控制項相關聯的命令透過呼叫 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework：： InvalidateUICommand</strong></a>而失效，則架構 <code>UI_INVALIDATIONS_VALUE</code> 會在傳遞做為 <em>旗標</em>的值時查詢此屬性。</span><span class="sxs-lookup"><span data-stu-id="e5758-139">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5758-140"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="e5758-140"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="e5758-141">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="e5758-141">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5758-142"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="e5758-142"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="e5758-143">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="e5758-143">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5758-144"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="e5758-144"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="e5758-145">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="e5758-145">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5758-146"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="e5758-146"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="e5758-147">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="e5758-147">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e5758-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5758-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5758-149">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="e5758-149">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="e5758-150">**InRibbonGallery 元素**</span><span class="sxs-lookup"><span data-stu-id="e5758-150">**InRibbonGallery element**</span></span>](windowsribbon-element-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="e5758-151">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="e5758-151">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="e5758-152">資源庫範例</span><span class="sxs-lookup"><span data-stu-id="e5758-152">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

