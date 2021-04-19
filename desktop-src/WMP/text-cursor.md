---
title: TEXT. cursor
description: Cursor 屬性會指定或抓取值，指出當滑鼠停留在文字控制項上時，所顯示的游標。
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- TEXT. cursor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8cf7b135ed0a99b5c65f760a08e4e7083234674
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982528"
---
# <a name="textcursor"></a><span data-ttu-id="25032-104">TEXT. cursor</span><span class="sxs-lookup"><span data-stu-id="25032-104">TEXT.cursor</span></span>

<span data-ttu-id="25032-105">**Cursor** 屬性會指定或抓取值，指出當滑鼠停留在文字控制項上時，所顯示的游標。</span><span class="sxs-lookup"><span data-stu-id="25032-105">The **cursor** attribute specifies or retrieves a value indicating which cursor appears when the mouse is over the Text control.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="25032-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="25032-106">Possible Values</span></span>

<span data-ttu-id="25032-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="25032-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="25032-108">值</span><span class="sxs-lookup"><span data-stu-id="25032-108">Value</span></span>            | <span data-ttu-id="25032-109">描述</span><span class="sxs-lookup"><span data-stu-id="25032-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="25032-110">系統</span><span class="sxs-lookup"><span data-stu-id="25032-110">system</span></span>           | <span data-ttu-id="25032-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="25032-111">Default.</span></span> <span data-ttu-id="25032-112">平臺相依游標 (通常是箭號) 。</span><span class="sxs-lookup"><span data-stu-id="25032-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="25032-113">手</span><span class="sxs-lookup"><span data-stu-id="25032-113">hand</span></span>             | <span data-ttu-id="25032-114">手。</span><span class="sxs-lookup"><span data-stu-id="25032-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="25032-115">help</span><span class="sxs-lookup"><span data-stu-id="25032-115">help</span></span>             | <span data-ttu-id="25032-116">有問號的箭號可用來指出說明。</span><span class="sxs-lookup"><span data-stu-id="25032-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="25032-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="25032-117">sizeall</span></span>          | <span data-ttu-id="25032-118">四指向的箭號，指向北、南、東和西。</span><span class="sxs-lookup"><span data-stu-id="25032-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="25032-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="25032-119">sizenesw</span></span>         | <span data-ttu-id="25032-120">指向東北和西南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="25032-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="25032-121">sizens</span><span class="sxs-lookup"><span data-stu-id="25032-121">sizens</span></span>           | <span data-ttu-id="25032-122">指向北和南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="25032-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="25032-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="25032-123">sizenwse</span></span>         | <span data-ttu-id="25032-124">雙指向箭號，指向西北和東南部。</span><span class="sxs-lookup"><span data-stu-id="25032-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="25032-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="25032-125">sizewe</span></span>           | <span data-ttu-id="25032-126">指向 west 和東的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="25032-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="25032-127">uparrow</span><span class="sxs-lookup"><span data-stu-id="25032-127">uparrow</span></span>          | <span data-ttu-id="25032-128">垂直箭號向上。</span><span class="sxs-lookup"><span data-stu-id="25032-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="25032-129">\*ani 或 \* 中</span><span class="sxs-lookup"><span data-stu-id="25032-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="25032-130">任何 ani 或..................................)  (</span><span class="sxs-lookup"><span data-stu-id="25032-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

<span data-ttu-id="25032-131">如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="25032-131">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="25032-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="25032-132">Requirements</span></span>



| <span data-ttu-id="25032-133">需求</span><span class="sxs-lookup"><span data-stu-id="25032-133">Requirement</span></span> | <span data-ttu-id="25032-134">值</span><span class="sxs-lookup"><span data-stu-id="25032-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="25032-135">版本</span><span class="sxs-lookup"><span data-stu-id="25032-135">Version</span></span><br/> | <span data-ttu-id="25032-136">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="25032-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25032-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25032-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25032-138">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="25032-138">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





