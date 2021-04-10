---
title: Drop-Down 按鈕
description: '[Drop-Down] 按鈕包含一個按鈕，當按下時，就會顯示互斥專案的下拉式清單。'
ms.assetid: 41c5da07-43f7-4544-83be-248941cb8633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87e6a776dd705fe503e5e93ec601baf6cc2b3cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316630"
---
# <a name="drop-down-button"></a><span data-ttu-id="2a895-103">Drop-Down 按鈕</span><span class="sxs-lookup"><span data-stu-id="2a895-103">Drop-Down Button</span></span>

<span data-ttu-id="2a895-104">[Drop-Down] 按鈕包含一個按鈕，當按下時，就會顯示互斥專案的下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="2a895-104">The Drop-Down Button consists of a button that when clicked displays a drop-down list of mutually exclusive items.</span></span>

-   [<span data-ttu-id="2a895-105">詳細資料</span><span class="sxs-lookup"><span data-stu-id="2a895-105">Details</span></span>](#details)
-   [<span data-ttu-id="2a895-106">下拉式按鈕屬性</span><span class="sxs-lookup"><span data-stu-id="2a895-106">Drop-Down Button Properties</span></span>](#drop-down-button-properties)
-   [<span data-ttu-id="2a895-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a895-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="2a895-108">詳細資料</span><span class="sxs-lookup"><span data-stu-id="2a895-108">Details</span></span>

<span data-ttu-id="2a895-109">如果沒有明顯的預設值可供使用，而且可以使用影像、文字或兩者來表示個別專案，此控制項就很適合用來公開密切相關的專案。</span><span class="sxs-lookup"><span data-stu-id="2a895-109">This control is useful for exposing closely related items in cases where no obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="2a895-110">下列螢幕擷取畫面說明範例功能區中的功能區 Drop-Down 按鈕。</span><span class="sxs-lookup"><span data-stu-id="2a895-110">The following screen shot illustrates the Ribbon Drop-Down Button in a sample Ribbon.</span></span>

![範例功能區中 dropdownbutton 控制項的螢幕擷取畫面。](images/controls/dropdownbutton.png)

## <a name="drop-down-button-properties"></a><span data-ttu-id="2a895-112">Drop-Down 按鈕屬性</span><span class="sxs-lookup"><span data-stu-id="2a895-112">Drop-Down Button Properties</span></span>

<span data-ttu-id="2a895-113">功能區架構會為 Drop-Down 按鈕控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="2a895-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Button control.</span></span>

<span data-ttu-id="2a895-114">一般來說，在功能區 UI 中會更新 Drop-Down 按鈕屬性，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="2a895-114">Typically, a Drop-Down Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="2a895-115">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="2a895-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="2a895-116">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="2a895-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="2a895-117">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="2a895-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="2a895-118">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="2a895-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="2a895-119">下表列出與 Drop-Down 按鈕控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2a895-119">The following table lists the property keys that are associated with the Drop-Down Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a895-120">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="2a895-120">Property Key</span></span></th>
<th><span data-ttu-id="2a895-121">備註</span><span class="sxs-lookup"><span data-stu-id="2a895-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a895-122"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="2a895-122"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="2a895-123">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="2a895-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a895-124"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="2a895-124"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="2a895-125">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="2a895-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span><br/> <span data-ttu-id="2a895-126">如果停用所有子專案，架構會將 <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> 設定為 false (0) 。</span><span class="sxs-lookup"><span data-stu-id="2a895-126">If all child items are disabled, the framework sets <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> to false (0).</span></span> <span data-ttu-id="2a895-127">否則，如果已啟用一個或多個子專案，UI_PKEY_Enabled 會設定為 true (-1) 。</span><span class="sxs-lookup"><span data-stu-id="2a895-127">Otherwise, if one or more child items are enabled, UI_PKEY_Enabled is set to true (-1).</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="2a895-128">在啟用或停用一個或多個子專案之後，Drop-Down 按鈕控制項的 <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> 屬性應該會失效。</span><span class="sxs-lookup"><span data-stu-id="2a895-128">The <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> property for the Drop-Down Button control should be invalidated after one or more child items are enabled or disabled.</span></span> <span data-ttu-id="2a895-129">這可確保架構會查詢更新的屬性值，並在功能區 UI 中重新整理 Drop-Down 按鈕控制項的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a895-129">This ensures that the framework queries the updated property value and refreshes the state of the Drop-Down Button control in the ribbon UI.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a895-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="2a895-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="2a895-131">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="2a895-131">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a895-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="2a895-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="2a895-133">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2a895-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a895-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="2a895-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="2a895-135">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2a895-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a895-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="2a895-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="2a895-137">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2a895-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a895-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="2a895-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="2a895-139">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2a895-139">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a895-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span><span class="sxs-lookup"><span data-stu-id="2a895-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span></span></td>
<td><span data-ttu-id="2a895-141">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="2a895-141">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="2a895-142">如果與控制項相關聯的命令透過呼叫 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework：： InvalidateUICommand</strong></a>而失效，則架構 <code>UI_INVALIDATIONS_VALUE</code> 會在傳遞做為 <em>旗標</em>的值時查詢此屬性。</span><span class="sxs-lookup"><span data-stu-id="2a895-142">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a895-143"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="2a895-143"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="2a895-144">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2a895-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a895-145"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="2a895-145"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="2a895-146">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2a895-146">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a895-147"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="2a895-147"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="2a895-148">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2a895-148">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a895-149"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="2a895-149"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="2a895-150">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2a895-150">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2a895-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a895-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a895-152">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="2a895-152">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="2a895-153">**DropDownButton 標記元素**</span><span class="sxs-lookup"><span data-stu-id="2a895-153">**DropDownButton markup element**</span></span>](windowsribbon-element-dropdownbutton.md)
</dt> </dl>