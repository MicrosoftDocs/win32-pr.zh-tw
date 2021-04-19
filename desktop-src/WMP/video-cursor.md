---
title: 影片。游標
description: Cursor 屬性指定或抓取滑鼠停留在影片的可點按區域時，所使用的資料指標值。
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- VIDEO. cursor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c23ab90b974ad5a7f9cfaf9fcc598371cd0697f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980124"
---
# <a name="videocursor"></a><span data-ttu-id="21631-104">影片。游標</span><span class="sxs-lookup"><span data-stu-id="21631-104">VIDEO.cursor</span></span>

<span data-ttu-id="21631-105">**Cursor** 屬性指定或抓取滑鼠停留在影片的可點按區域時，所使用的資料指標值。</span><span class="sxs-lookup"><span data-stu-id="21631-105">The **cursor** attribute specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="21631-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="21631-106">Possible Values</span></span>

<span data-ttu-id="21631-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="21631-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="21631-108">值</span><span class="sxs-lookup"><span data-stu-id="21631-108">Value</span></span>            | <span data-ttu-id="21631-109">描述</span><span class="sxs-lookup"><span data-stu-id="21631-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="21631-110">系統</span><span class="sxs-lookup"><span data-stu-id="21631-110">system</span></span>           | <span data-ttu-id="21631-111">平臺相依游標 (通常是箭號) 。</span><span class="sxs-lookup"><span data-stu-id="21631-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="21631-112">手</span><span class="sxs-lookup"><span data-stu-id="21631-112">hand</span></span>             | <span data-ttu-id="21631-113">手。</span><span class="sxs-lookup"><span data-stu-id="21631-113">Hand.</span></span>                                                                                       |
| <span data-ttu-id="21631-114">help</span><span class="sxs-lookup"><span data-stu-id="21631-114">help</span></span>             | <span data-ttu-id="21631-115">有問號的箭號可用來指出說明。</span><span class="sxs-lookup"><span data-stu-id="21631-115">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="21631-116">sizeall</span><span class="sxs-lookup"><span data-stu-id="21631-116">sizeall</span></span>          | <span data-ttu-id="21631-117">四指向的箭號，指向北、南、東和西。</span><span class="sxs-lookup"><span data-stu-id="21631-117">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="21631-118">sizenesw</span><span class="sxs-lookup"><span data-stu-id="21631-118">sizenesw</span></span>         | <span data-ttu-id="21631-119">指向東北和西南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="21631-119">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="21631-120">sizens</span><span class="sxs-lookup"><span data-stu-id="21631-120">sizens</span></span>           | <span data-ttu-id="21631-121">指向北和南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="21631-121">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="21631-122">sizenwse</span><span class="sxs-lookup"><span data-stu-id="21631-122">sizenwse</span></span>         | <span data-ttu-id="21631-123">雙指向箭號，指向西北和東南部。</span><span class="sxs-lookup"><span data-stu-id="21631-123">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="21631-124">sizewe</span><span class="sxs-lookup"><span data-stu-id="21631-124">sizewe</span></span>           | <span data-ttu-id="21631-125">指向 west 和東的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="21631-125">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="21631-126">uparrow</span><span class="sxs-lookup"><span data-stu-id="21631-126">uparrow</span></span>          | <span data-ttu-id="21631-127">垂直箭號向上。</span><span class="sxs-lookup"><span data-stu-id="21631-127">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="21631-128">\*ani 或 \* 中</span><span class="sxs-lookup"><span data-stu-id="21631-128">\*.ani or \*.cur</span></span> | <span data-ttu-id="21631-129">任何 ani 或..................................)  (</span><span class="sxs-lookup"><span data-stu-id="21631-129">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="21631-130">備註</span><span class="sxs-lookup"><span data-stu-id="21631-130">Remarks</span></span>

<span data-ttu-id="21631-131">基於轉譯目的，系統是預設的資料指標。</span><span class="sxs-lookup"><span data-stu-id="21631-131">For rendering purposes, system is the default cursor.</span></span> <span data-ttu-id="21631-132">從此屬性抓取的預設值為 "" (空白字串) 。</span><span class="sxs-lookup"><span data-stu-id="21631-132">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="21631-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="21631-133">Requirements</span></span>



| <span data-ttu-id="21631-134">需求</span><span class="sxs-lookup"><span data-stu-id="21631-134">Requirement</span></span> | <span data-ttu-id="21631-135">值</span><span class="sxs-lookup"><span data-stu-id="21631-135">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="21631-136">版本</span><span class="sxs-lookup"><span data-stu-id="21631-136">Version</span></span><br/> | <span data-ttu-id="21631-137">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="21631-137">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="21631-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21631-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21631-139">**影片元素**</span><span class="sxs-lookup"><span data-stu-id="21631-139">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





