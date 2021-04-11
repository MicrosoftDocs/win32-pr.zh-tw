---
title: '群組 (Windows 功能區架構) '
description: 群組會在索引標籤中組織相關的命令和控制項。
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903bd422d11fea81ed03a48bf8e9437f9caab699
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383757"
---
# <a name="group-windows-ribbon-framework"></a><span data-ttu-id="4c1b9-103">群組 (Windows 功能區架構) </span><span class="sxs-lookup"><span data-stu-id="4c1b9-103">Group (Windows Ribbon Framework)</span></span>

<span data-ttu-id="4c1b9-104">群組會在索引標籤中組織相關[的命令和控制項。](windowsribbon-controls-tab.md)</span><span class="sxs-lookup"><span data-stu-id="4c1b9-104">The Group organizes related Commands and controls within a [Tab](windowsribbon-controls-tab.md).</span></span>

-   [<span data-ttu-id="4c1b9-105">詳細資料</span><span class="sxs-lookup"><span data-stu-id="4c1b9-105">Details</span></span>](#details)
-   [<span data-ttu-id="4c1b9-106">群組屬性</span><span class="sxs-lookup"><span data-stu-id="4c1b9-106">Group Properties</span></span>](#group-properties)
-   [<span data-ttu-id="4c1b9-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c1b9-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="4c1b9-108">詳細資料</span><span class="sxs-lookup"><span data-stu-id="4c1b9-108">Details</span></span>

<span data-ttu-id="4c1b9-109">下列螢幕擷取畫面說明功能區群組控制項。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-109">The following screen shot illustrates the Ribbon Group control.</span></span>

![具有顯示群組之標注的螢幕擷取畫面。](images/controls/group.png)

## <a name="group-properties"></a><span data-ttu-id="4c1b9-111">群組屬性</span><span class="sxs-lookup"><span data-stu-id="4c1b9-111">Group Properties</span></span>

<span data-ttu-id="4c1b9-112">功能區架構會針對群組控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Group control.</span></span>

<span data-ttu-id="4c1b9-113">一般而言，群組屬性會在功能區 UI 中更新，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-113">Typically, a Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="4c1b9-114">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="4c1b9-115">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="4c1b9-116">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="4c1b9-117">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="4c1b9-118">下表列出與群組控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-118">The following table lists the property keys that are associated with the Group control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4c1b9-119">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="4c1b9-119">Property Key</span></span></th>
<th><span data-ttu-id="4c1b9-120">備註</span><span class="sxs-lookup"><span data-stu-id="4c1b9-120">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c1b9-121"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="4c1b9-121"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="4c1b9-122">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-122">Can only be updated through invalidation.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c1b9-123">架構要求群組控制項的 <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> 值的開頭必須是大寫字母 Z。如果 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler：： UpdateProperty</strong></a> 回呼方法中的應用程式所提供的值不是以字母 Z 開頭，則會忽略此值，而值會由架構產生。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-123">The framework requires that the value of <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> for a Group control begins with the upper-case letter Z. If the value supplied by the application in the <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler::UpdateProperty</strong></a> callback method does not begin with the letter Z, this value is ignored and a value is generated by the framework instead.</span></span> <span data-ttu-id="4c1b9-124">Framework 值是字母 Z，後面接著以1開始的數值，並視需要順序遞增，以供後續的群組控制項 (Z1、Z2、...、Zx) 。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-124">The framework value is the letter Z followed by a numeric value starting at 1 and increasing sequentially, as required, for subsequent Group controls (Z1, Z2, ..., Zx).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c1b9-125"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="4c1b9-125"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="4c1b9-126">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-126">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c1b9-127"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="4c1b9-127"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="4c1b9-128">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-128">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c1b9-129"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="4c1b9-129"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="4c1b9-130">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c1b9-131"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="4c1b9-131"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="4c1b9-132">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c1b9-133"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="4c1b9-133"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="4c1b9-134">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c1b9-135"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="4c1b9-135"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="4c1b9-136">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c1b9-137"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="4c1b9-137"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="4c1b9-138">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="4c1b9-138">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4c1b9-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c1b9-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c1b9-140">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="4c1b9-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="4c1b9-141">**Group 元素**</span><span class="sxs-lookup"><span data-stu-id="4c1b9-141">**Group element**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

