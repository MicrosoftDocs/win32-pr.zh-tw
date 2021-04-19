---
title: BUTTONGROUP 資料指標
description: Cursor 屬性指定或抓取當滑鼠停留在 BUTTONGROUP 的按鈕上時，所顯示的游標類型。
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- BUTTONGROUP. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b3de12950aed383f48dcde5d8978724037f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977565"
---
# <a name="buttongroupcursor"></a><span data-ttu-id="e7ad0-104">BUTTONGROUP 資料指標</span><span class="sxs-lookup"><span data-stu-id="e7ad0-104">BUTTONGROUP.cursor</span></span>

<span data-ttu-id="e7ad0-105">**Cursor** 屬性指定或抓取當滑鼠停留在 **BUTTONGROUP** 的按鈕上時，所顯示的游標類型。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-105">The **cursor** attribute specifies or retrieves the type of cursor that appears when the mouse is over a button in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="e7ad0-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="e7ad0-106">Possible Values</span></span>

<span data-ttu-id="e7ad0-107">這個屬性是包含下列其中一個值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="e7ad0-108">值</span><span class="sxs-lookup"><span data-stu-id="e7ad0-108">Value</span></span>            | <span data-ttu-id="e7ad0-109">描述</span><span class="sxs-lookup"><span data-stu-id="e7ad0-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ad0-110">系統</span><span class="sxs-lookup"><span data-stu-id="e7ad0-110">system</span></span>           | <span data-ttu-id="e7ad0-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-111">Default.</span></span> <span data-ttu-id="e7ad0-112">平臺相依游標 (通常是箭號) 。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="e7ad0-113">手</span><span class="sxs-lookup"><span data-stu-id="e7ad0-113">hand</span></span>             | <span data-ttu-id="e7ad0-114">手。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="e7ad0-115">help</span><span class="sxs-lookup"><span data-stu-id="e7ad0-115">help</span></span>             | <span data-ttu-id="e7ad0-116">有問號的箭號可用來指出說明。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="e7ad0-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="e7ad0-117">sizeall</span></span>          | <span data-ttu-id="e7ad0-118">四指向的箭號，指向北、南、東和西。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="e7ad0-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="e7ad0-119">sizenesw</span></span>         | <span data-ttu-id="e7ad0-120">指向東北和西南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="e7ad0-121">sizens</span><span class="sxs-lookup"><span data-stu-id="e7ad0-121">sizens</span></span>           | <span data-ttu-id="e7ad0-122">指向北和南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="e7ad0-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="e7ad0-123">sizenwse</span></span>         | <span data-ttu-id="e7ad0-124">雙指向箭號，指向西北和東南部。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="e7ad0-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="e7ad0-125">sizewe</span></span>           | <span data-ttu-id="e7ad0-126">指向 west 和東的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="e7ad0-127">uparrow</span><span class="sxs-lookup"><span data-stu-id="e7ad0-127">uparrow</span></span>          | <span data-ttu-id="e7ad0-128">垂直箭號向上。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="e7ad0-129">\*ani 或 \* 中</span><span class="sxs-lookup"><span data-stu-id="e7ad0-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="e7ad0-130">任何 ani 或..................................)  (</span><span class="sxs-lookup"><span data-stu-id="e7ad0-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e7ad0-131">備註</span><span class="sxs-lookup"><span data-stu-id="e7ad0-131">Remarks</span></span>

<span data-ttu-id="e7ad0-132">指定的資料指標會套用至 **BUTTONGROUP** 中的所有按鈕。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-132">The cursor specified applies to all buttons in the **BUTTONGROUP**.</span></span>

<span data-ttu-id="e7ad0-133">如果您指定不正確資料指標值，它會維持在先前設定的值。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-133">If you specify an invalid cursor value, it remains at the previously set value.</span></span>

<span data-ttu-id="e7ad0-134">資料指標檔名稱路徑會被忽略，因此游標檔必須位於預設目錄中。</span><span class="sxs-lookup"><span data-stu-id="e7ad0-134">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ad0-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7ad0-135">Requirements</span></span>



| <span data-ttu-id="e7ad0-136">需求</span><span class="sxs-lookup"><span data-stu-id="e7ad0-136">Requirement</span></span> | <span data-ttu-id="e7ad0-137">值</span><span class="sxs-lookup"><span data-stu-id="e7ad0-137">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e7ad0-138">版本</span><span class="sxs-lookup"><span data-stu-id="e7ad0-138">Version</span></span><br/> | <span data-ttu-id="e7ad0-139">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="e7ad0-139">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7ad0-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7ad0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ad0-141">**BUTTONGROUP 元素**</span><span class="sxs-lookup"><span data-stu-id="e7ad0-141">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





