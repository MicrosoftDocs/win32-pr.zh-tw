---
title: 滑杆。游標
description: Cursor 屬性會指定或抓取值，指出當滑鼠停留在滑杆控制項上時，所顯示的游標。
ms.assetid: 5b96a20c-b3a6-4e08-95b2-32937bb15cc6
keywords:
- 滑杆. cursor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc8f581d7d087545e666565dd03f649112064d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985545"
---
# <a name="slidercursor"></a><span data-ttu-id="43d26-104">滑杆。游標</span><span class="sxs-lookup"><span data-stu-id="43d26-104">SLIDER.cursor</span></span>

<span data-ttu-id="43d26-105">**Cursor** 屬性會指定或抓取值，指出當滑鼠停留在滑杆控制項上時，所顯示的游標。</span><span class="sxs-lookup"><span data-stu-id="43d26-105">The **cursor** attribute specifies or retrieves a value indicating which cursor appears when the mouse is over the slider control.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="43d26-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="43d26-106">Possible Values</span></span>

<span data-ttu-id="43d26-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="43d26-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="43d26-108">值</span><span class="sxs-lookup"><span data-stu-id="43d26-108">Value</span></span>            | <span data-ttu-id="43d26-109">描述</span><span class="sxs-lookup"><span data-stu-id="43d26-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="43d26-110">系統</span><span class="sxs-lookup"><span data-stu-id="43d26-110">system</span></span>           | <span data-ttu-id="43d26-111">平臺相依游標 (通常是箭號) 。</span><span class="sxs-lookup"><span data-stu-id="43d26-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="43d26-112">手</span><span class="sxs-lookup"><span data-stu-id="43d26-112">hand</span></span>             | <span data-ttu-id="43d26-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="43d26-113">Default.</span></span> <span data-ttu-id="43d26-114">手。</span><span class="sxs-lookup"><span data-stu-id="43d26-114">Hand.</span></span>                                                                              |
| <span data-ttu-id="43d26-115">help</span><span class="sxs-lookup"><span data-stu-id="43d26-115">help</span></span>             | <span data-ttu-id="43d26-116">有問號的箭號可用來指出說明。</span><span class="sxs-lookup"><span data-stu-id="43d26-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="43d26-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="43d26-117">sizeall</span></span>          | <span data-ttu-id="43d26-118">四指向的箭號，指向北、南、東和西。</span><span class="sxs-lookup"><span data-stu-id="43d26-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="43d26-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="43d26-119">sizenesw</span></span>         | <span data-ttu-id="43d26-120">指向東北和西南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="43d26-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="43d26-121">sizens</span><span class="sxs-lookup"><span data-stu-id="43d26-121">sizens</span></span>           | <span data-ttu-id="43d26-122">指向北和南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="43d26-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="43d26-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="43d26-123">sizenwse</span></span>         | <span data-ttu-id="43d26-124">雙指向箭號，指向西北和東南部。</span><span class="sxs-lookup"><span data-stu-id="43d26-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="43d26-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="43d26-125">sizewe</span></span>           | <span data-ttu-id="43d26-126">指向 west 和東的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="43d26-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="43d26-127">uparrow</span><span class="sxs-lookup"><span data-stu-id="43d26-127">uparrow</span></span>          | <span data-ttu-id="43d26-128">垂直箭號向上。</span><span class="sxs-lookup"><span data-stu-id="43d26-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="43d26-129">\*ani 或 \* 中</span><span class="sxs-lookup"><span data-stu-id="43d26-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="43d26-130">任何 ani 或..................................)  (</span><span class="sxs-lookup"><span data-stu-id="43d26-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="43d26-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="43d26-131">Requirements</span></span>



| <span data-ttu-id="43d26-132">需求</span><span class="sxs-lookup"><span data-stu-id="43d26-132">Requirement</span></span> | <span data-ttu-id="43d26-133">值</span><span class="sxs-lookup"><span data-stu-id="43d26-133">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="43d26-134">版本</span><span class="sxs-lookup"><span data-stu-id="43d26-134">Version</span></span><br/> | <span data-ttu-id="43d26-135">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="43d26-135">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43d26-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43d26-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d26-137">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="43d26-137">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





