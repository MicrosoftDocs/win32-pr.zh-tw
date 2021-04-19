---
title: Split Button
description: '[分割] 按鈕是複合控制項，使用者可以選取系結至主要按鈕的預設值，或從下拉式清單中顯示的互斥值清單中，選取系結至次要按鈕的清單。'
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b78aa261eebb24404eeaf8b3fdad7f630331f58
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106969734"
---
# <a name="split-button"></a><span data-ttu-id="66597-103">Split Button</span><span class="sxs-lookup"><span data-stu-id="66597-103">Split Button</span></span>

<span data-ttu-id="66597-104">[分割] 按鈕是複合控制項，使用者可以選取系結至主要按鈕的預設值，或從下拉式清單中顯示的互斥值清單中，選取系結至次要按鈕的清單。</span><span class="sxs-lookup"><span data-stu-id="66597-104">The Split Button is a composite control with which the user can select a default value bound to a primary button, or select from a list of mutually exclusive values displayed in a drop-down list bound to a secondary button.</span></span>

-   [<span data-ttu-id="66597-105">簡介</span><span class="sxs-lookup"><span data-stu-id="66597-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="66597-106">分割按鈕屬性</span><span class="sxs-lookup"><span data-stu-id="66597-106">Split Button Properties</span></span>](#split-button-properties)
-   [<span data-ttu-id="66597-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="66597-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="66597-108">簡介</span><span class="sxs-lookup"><span data-stu-id="66597-108">Introduction</span></span>

<span data-ttu-id="66597-109">如果有明顯的預設值可供使用，而且個別專案可以用影像、文字或兩者表示，則這個控制項非常適合用來公開密切相關的專案。</span><span class="sxs-lookup"><span data-stu-id="66597-109">This control is useful for exposing closely related items in cases where an obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="66597-110">下列螢幕擷取畫面說明功能區分割按鈕。</span><span class="sxs-lookup"><span data-stu-id="66597-110">The following screen shot illustrates the Ribbon Split Button.</span></span>

![範例功能區中 splitbutton 控制項的螢幕擷取畫面。](images/controls/splitbutton.png)

## <a name="split-button-properties"></a><span data-ttu-id="66597-112">分割按鈕屬性</span><span class="sxs-lookup"><span data-stu-id="66597-112">Split Button Properties</span></span>

<span data-ttu-id="66597-113">功能區架構會針對分割按鈕控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="66597-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Split Button control.</span></span>

<span data-ttu-id="66597-114">一般來說，在功能區 UI 中，會透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效，以更新分割按鈕屬性。</span><span class="sxs-lookup"><span data-stu-id="66597-114">Typically, a Split Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="66597-115">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="66597-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="66597-116">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="66597-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="66597-117">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="66597-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="66597-118">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="66597-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="66597-119">下表列出與分割按鈕控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="66597-119">The following table lists the property keys that are associated with the Split Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66597-120">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="66597-120">Property Key</span></span></th>
<th><span data-ttu-id="66597-121">備註</span><span class="sxs-lookup"><span data-stu-id="66597-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66597-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="66597-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="66597-123">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="66597-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span><br/> <span data-ttu-id="66597-124">如果停用所有子專案，架構會將 <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> 設定為 false (0) 。</span><span class="sxs-lookup"><span data-stu-id="66597-124">If all child items are disabled, the framework sets <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> to false (0).</span></span> <span data-ttu-id="66597-125">否則，如果已啟用一個或多個子專案，UI_PKEY_Enabled 會設定為 true (-1) 。</span><span class="sxs-lookup"><span data-stu-id="66597-125">Otherwise, if one or more child items are enabled, UI_PKEY_Enabled is set to true (-1).</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="66597-126">在啟用或停用一個或多個子專案之後，分割按鈕控制項的 <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> 屬性應該會失效。</span><span class="sxs-lookup"><span data-stu-id="66597-126">The <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> property for the Split Button control should be invalidated after one or more child items are enabled or disabled.</span></span> <span data-ttu-id="66597-127">這可確保架構會查詢更新的屬性值，並在功能區 UI 中重新整理分割按鈕控制項的狀態。</span><span class="sxs-lookup"><span data-stu-id="66597-127">This ensures that the framework queries the updated property value and refreshes the state of the Split Button control in the ribbon UI.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66597-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="66597-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="66597-129">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="66597-129">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66597-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="66597-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="66597-131">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="66597-131">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66597-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="66597-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="66597-133">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="66597-133">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="66597-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="66597-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66597-135">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="66597-135">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="66597-136">**SplitButton 標記元素**</span><span class="sxs-lookup"><span data-stu-id="66597-136">**SplitButton markup element**</span></span>](windowsribbon-element-splitbutton.md)
</dt> </dl>