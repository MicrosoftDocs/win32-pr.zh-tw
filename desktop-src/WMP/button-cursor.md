---
title: 按鈕。游標
description: Cursor 屬性會指定或抓取滑鼠指標停留在按鈕上時所顯示的游標。
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- Cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2641491a5a73498da2c43fd74d4187b5594e177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998393"
---
# <a name="buttoncursor"></a><span data-ttu-id="4d58d-104">按鈕。游標</span><span class="sxs-lookup"><span data-stu-id="4d58d-104">BUTTON.cursor</span></span>

<span data-ttu-id="4d58d-105">**Cursor** 屬性會指定或抓取滑鼠指標停留在 **按鈕** 上時所顯示的游標。</span><span class="sxs-lookup"><span data-stu-id="4d58d-105">The **cursor** attribute specifies or retrieves the cursor that appears when the mouse pointer hovers over the **BUTTON**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="4d58d-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="4d58d-106">Possible Values</span></span>

<span data-ttu-id="4d58d-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="4d58d-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="4d58d-108">值</span><span class="sxs-lookup"><span data-stu-id="4d58d-108">Value</span></span>            | <span data-ttu-id="4d58d-109">描述</span><span class="sxs-lookup"><span data-stu-id="4d58d-109">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d58d-110">系統</span><span class="sxs-lookup"><span data-stu-id="4d58d-110">system</span></span>           | <span data-ttu-id="4d58d-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="4d58d-111">Default.</span></span> <span data-ttu-id="4d58d-112">平臺相依游標 (通常是箭號) 。</span><span class="sxs-lookup"><span data-stu-id="4d58d-112">Platform-dependent cursor (usually an arrow).</span></span>                                     |
| <span data-ttu-id="4d58d-113">手</span><span class="sxs-lookup"><span data-stu-id="4d58d-113">hand</span></span>             | <span data-ttu-id="4d58d-114">手。</span><span class="sxs-lookup"><span data-stu-id="4d58d-114">Hand.</span></span>                                                                                      |
| <span data-ttu-id="4d58d-115">help</span><span class="sxs-lookup"><span data-stu-id="4d58d-115">help</span></span>             | <span data-ttu-id="4d58d-116">有問號的箭號可用來指出說明。</span><span class="sxs-lookup"><span data-stu-id="4d58d-116">Arrow with question mark indicating Help is available.</span></span>                                     |
| <span data-ttu-id="4d58d-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="4d58d-117">sizeall</span></span>          | <span data-ttu-id="4d58d-118">四指向的箭號，指向北、南、東和西。</span><span class="sxs-lookup"><span data-stu-id="4d58d-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                  |
| <span data-ttu-id="4d58d-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="4d58d-119">sizenesw</span></span>         | <span data-ttu-id="4d58d-120">指向東北和西南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="4d58d-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                     |
| <span data-ttu-id="4d58d-121">sizens</span><span class="sxs-lookup"><span data-stu-id="4d58d-121">sizens</span></span>           | <span data-ttu-id="4d58d-122">指向北和南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="4d58d-122">Double-pointed arrow pointing north and south.</span></span>                                             |
| <span data-ttu-id="4d58d-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="4d58d-123">sizenwse</span></span>         | <span data-ttu-id="4d58d-124">雙指向箭號，指向西北和東南部。</span><span class="sxs-lookup"><span data-stu-id="4d58d-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                     |
| <span data-ttu-id="4d58d-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="4d58d-125">sizewe</span></span>           | <span data-ttu-id="4d58d-126">指向 west 和東的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="4d58d-126">Double-pointed arrow pointing west and east.</span></span>                                               |
| <span data-ttu-id="4d58d-127">uparrow</span><span class="sxs-lookup"><span data-stu-id="4d58d-127">uparrow</span></span>          | <span data-ttu-id="4d58d-128">垂直箭號向上。</span><span class="sxs-lookup"><span data-stu-id="4d58d-128">Vertical arrow pointing upward.</span></span>                                                            |
| <span data-ttu-id="4d58d-129">\*ani 或 \* 中</span><span class="sxs-lookup"><span data-stu-id="4d58d-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="4d58d-130">任何 ani 或............)  (.....................。</span><span class="sxs-lookup"><span data-stu-id="4d58d-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4d58d-131">備註</span><span class="sxs-lookup"><span data-stu-id="4d58d-131">Remarks</span></span>

<span data-ttu-id="4d58d-132">如果系統無法辨識指定的資料指標值，則資料指標值會維持在先前設定的值。</span><span class="sxs-lookup"><span data-stu-id="4d58d-132">If the system does not recognize the cursor value specified, the cursor value remains at the previously set value.</span></span>

<span data-ttu-id="4d58d-133">資料指標檔名稱路徑會被忽略，因此游標檔必須位於預設目錄中。</span><span class="sxs-lookup"><span data-stu-id="4d58d-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d58d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d58d-134">Requirements</span></span>



| <span data-ttu-id="4d58d-135">需求</span><span class="sxs-lookup"><span data-stu-id="4d58d-135">Requirement</span></span> | <span data-ttu-id="4d58d-136">值</span><span class="sxs-lookup"><span data-stu-id="4d58d-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4d58d-137">版本</span><span class="sxs-lookup"><span data-stu-id="4d58d-137">Version</span></span><br/> | <span data-ttu-id="4d58d-138">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="4d58d-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d58d-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d58d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d58d-140">**BUTTON 元素**</span><span class="sxs-lookup"><span data-stu-id="4d58d-140">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





