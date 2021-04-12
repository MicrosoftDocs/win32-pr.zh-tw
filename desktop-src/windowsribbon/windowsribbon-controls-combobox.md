---
title: 'Windows 功能區架構 (下拉式方塊) '
description: 下拉式方塊包含單一資料行清單方塊，其中包含與靜態或編輯控制項和下拉箭號結合的互斥專案或命令集合。
ms.assetid: 6b7de2ec-dcb7-44cb-b01f-db1ba0643499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c61c19963811d12557beafe3c5cff314c927ae7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464064"
---
# <a name="combo-box-windows-ribbon-framework"></a><span data-ttu-id="2d605-103">Windows 功能區架構 (下拉式方塊) </span><span class="sxs-lookup"><span data-stu-id="2d605-103">Combo Box (Windows Ribbon Framework)</span></span>

<span data-ttu-id="2d605-104">下拉式方塊包含單一資料行清單方塊，其中包含與靜態或編輯控制項和下拉箭號結合的互斥專案或命令集合。</span><span class="sxs-lookup"><span data-stu-id="2d605-104">The Combo Box consists of a single-column list box that contains a collection of mutually exclusive items or Commands combined with a static or edit control and a drop-down arrow.</span></span> <span data-ttu-id="2d605-105">當使用者按一下下拉式箭號時，就會顯示控制項的清單方塊部分。</span><span class="sxs-lookup"><span data-stu-id="2d605-105">The list box portion of the control is displayed when the user clicks the drop-down arrow.</span></span>

-   [<span data-ttu-id="2d605-106">詳細資料</span><span class="sxs-lookup"><span data-stu-id="2d605-106">Details</span></span>](#details)
-   [<span data-ttu-id="2d605-107">下拉式列示方塊屬性</span><span class="sxs-lookup"><span data-stu-id="2d605-107">Combo Box Properties</span></span>](#combo-box-properties)
-   [<span data-ttu-id="2d605-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d605-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="2d605-109">詳細資料</span><span class="sxs-lookup"><span data-stu-id="2d605-109">Details</span></span>

<span data-ttu-id="2d605-110">目前選取的專案或命令 (是否在 [靜態] 或 [編輯] 控制項中顯示清單方塊中的任何) 。</span><span class="sxs-lookup"><span data-stu-id="2d605-110">The currently selected item or Command (if any) in the list box is displayed in the static or edit control.</span></span> <span data-ttu-id="2d605-111">使用編輯控制項時，如果使用者輸入現有專案或命令的初始字元，清單方塊將會醒目提示具有這些初始字元的第一個專案，並在編輯控制項中自動完成專案。</span><span class="sxs-lookup"><span data-stu-id="2d605-111">With an edit control, if the user types the initial characters of an existing item or Command, the list box will highlight the first item with those initial characters and autocomplete the entry in the edit control.</span></span>

<span data-ttu-id="2d605-112">僅支援垂直控制軸或調整控點大小。</span><span class="sxs-lookup"><span data-stu-id="2d605-112">Supports a vertical gripper bar, or resizing handle, only.</span></span>

<span data-ttu-id="2d605-113">此控制項適用于公開簡單、密切相關的文字專案。</span><span class="sxs-lookup"><span data-stu-id="2d605-113">This control is useful for exposing simple, closely related text items.</span></span>

<span data-ttu-id="2d605-114">下列螢幕擷取畫面說明 Live Movie Maker 中的功能區下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="2d605-114">The following screen shot illustrates the Ribbon Combo Box in Live Movie Maker.</span></span>

![microsoft 油漆功能區中 combobox 控制項的螢幕擷取畫面。](images/controls/combobox.png)

## <a name="combo-box-properties"></a><span data-ttu-id="2d605-116">下拉式列示方塊屬性</span><span class="sxs-lookup"><span data-stu-id="2d605-116">Combo Box Properties</span></span>

<span data-ttu-id="2d605-117">功能區架構會為下拉式方塊控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="2d605-117">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Combo Box control.</span></span>

<span data-ttu-id="2d605-118">通常會在功能區 UI 中更新下拉式方塊屬性，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="2d605-118">Typically, a Combo Box property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="2d605-119">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="2d605-119">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="2d605-120">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="2d605-120">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="2d605-121">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="2d605-121">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="2d605-122">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="2d605-122">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="2d605-123">下表列出與下拉式方塊控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2d605-123">The following table lists the property keys that are associated with the Combo Box control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2d605-124">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="2d605-124">Property Key</span></span></th>
<th><span data-ttu-id="2d605-125">備註</span><span class="sxs-lookup"><span data-stu-id="2d605-125">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2d605-126"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="2d605-126"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="2d605-127">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="2d605-127">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2d605-128"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="2d605-128"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="2d605-129">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="2d605-129">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2d605-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="2d605-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="2d605-131">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="2d605-131">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2d605-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="2d605-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="2d605-133">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2d605-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2d605-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="2d605-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="2d605-135">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2d605-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2d605-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="2d605-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="2d605-137">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2d605-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2d605-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="2d605-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="2d605-139">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2d605-139">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2d605-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span><span class="sxs-lookup"><span data-stu-id="2d605-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span></span></td>
<td><span data-ttu-id="2d605-141">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="2d605-141">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2d605-142"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="2d605-142"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="2d605-143">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2d605-143">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2d605-144"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="2d605-144"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="2d605-145">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2d605-145">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2d605-146"><a href="windowsribbon-reference-properties-uipkey-stringvalue.md">UI_PKEY_StringValue</a></span><span class="sxs-lookup"><span data-stu-id="2d605-146"><a href="windowsribbon-reference-properties-uipkey-stringvalue.md">UI_PKEY_StringValue</a></span></span></td>
<td><span data-ttu-id="2d605-147">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="2d605-147">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="2d605-148">如果與控制項相關聯的命令透過呼叫 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework：： InvalidateUICommand</strong></a>而失效，則架構 <code>UI_INVALIDATIONS_VALUE</code> 會在傳遞做為 <em>旗標</em>的值時查詢此屬性。</span><span class="sxs-lookup"><span data-stu-id="2d605-148">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2d605-149"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="2d605-149"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="2d605-150">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2d605-150">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2d605-151"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="2d605-151"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="2d605-152">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="2d605-152">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2d605-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d605-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d605-154">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="2d605-154">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="2d605-155">**ComboBox 標記元素**</span><span class="sxs-lookup"><span data-stu-id="2d605-155">**ComboBox markup element**</span></span>](windowsribbon-element-combobox.md)
</dt> <dt>

[<span data-ttu-id="2d605-156">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="2d605-156">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="2d605-157">資源庫範例</span><span class="sxs-lookup"><span data-stu-id="2d605-157">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

