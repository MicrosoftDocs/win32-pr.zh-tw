---
title: BUTTONELEMENT 資料指標
description: Cursor 屬性會指定或抓取滑鼠移到 BUTTONELEMENT 上時所顯示的 BUTTONELEMENT 資料指標值。
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- BUTTONELEMENT. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979613"
---
# <a name="buttonelementcursor"></a><span data-ttu-id="327ff-104">BUTTONELEMENT 資料指標</span><span class="sxs-lookup"><span data-stu-id="327ff-104">BUTTONELEMENT.cursor</span></span>

<span data-ttu-id="327ff-105">**Cursor** 屬性會指定或抓取滑鼠移到 **BUTTONELEMENT** 上時所顯示的 **BUTTONELEMENT** 資料指標值。</span><span class="sxs-lookup"><span data-stu-id="327ff-105">The **cursor** attribute specifies or retrieves the value of the **BUTTONELEMENT** cursor that appears when the mouse is over the **BUTTONELEMENT**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="327ff-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="327ff-106">Possible Values</span></span>

<span data-ttu-id="327ff-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="327ff-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="327ff-108">值</span><span class="sxs-lookup"><span data-stu-id="327ff-108">Value</span></span>            | <span data-ttu-id="327ff-109">描述</span><span class="sxs-lookup"><span data-stu-id="327ff-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="327ff-110">系統</span><span class="sxs-lookup"><span data-stu-id="327ff-110">system</span></span>           | <span data-ttu-id="327ff-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="327ff-111">Default.</span></span> <span data-ttu-id="327ff-112">平臺相依游標 (通常是箭號) 。</span><span class="sxs-lookup"><span data-stu-id="327ff-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="327ff-113">手</span><span class="sxs-lookup"><span data-stu-id="327ff-113">hand</span></span>             | <span data-ttu-id="327ff-114">手。</span><span class="sxs-lookup"><span data-stu-id="327ff-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="327ff-115">help</span><span class="sxs-lookup"><span data-stu-id="327ff-115">help</span></span>             | <span data-ttu-id="327ff-116">有問號的箭號可用來指出說明。</span><span class="sxs-lookup"><span data-stu-id="327ff-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="327ff-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="327ff-117">sizeall</span></span>          | <span data-ttu-id="327ff-118">四指向的箭號，指向北、南、東和西。</span><span class="sxs-lookup"><span data-stu-id="327ff-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="327ff-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="327ff-119">sizenesw</span></span>         | <span data-ttu-id="327ff-120">指向東北和西南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="327ff-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="327ff-121">sizens</span><span class="sxs-lookup"><span data-stu-id="327ff-121">sizens</span></span>           | <span data-ttu-id="327ff-122">指向北和南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="327ff-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="327ff-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="327ff-123">sizenwse</span></span>         | <span data-ttu-id="327ff-124">雙指向箭號，指向西北和東南部。</span><span class="sxs-lookup"><span data-stu-id="327ff-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="327ff-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="327ff-125">sizewe</span></span>           | <span data-ttu-id="327ff-126">指向 west 和東的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="327ff-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="327ff-127">uparrow</span><span class="sxs-lookup"><span data-stu-id="327ff-127">uparrow</span></span>          | <span data-ttu-id="327ff-128">垂直箭號向上。</span><span class="sxs-lookup"><span data-stu-id="327ff-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="327ff-129">\*ani 或 \* 中</span><span class="sxs-lookup"><span data-stu-id="327ff-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="327ff-130">任何 ani 或..................................)  (</span><span class="sxs-lookup"><span data-stu-id="327ff-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="327ff-131">備註</span><span class="sxs-lookup"><span data-stu-id="327ff-131">Remarks</span></span>

<span data-ttu-id="327ff-132">如果指定了不正確值，則會保留先前的值。</span><span class="sxs-lookup"><span data-stu-id="327ff-132">If an invalid value is specified, the previous value is maintained.</span></span>

<span data-ttu-id="327ff-133">資料指標檔名稱路徑會被忽略，因此游標檔必須位於預設目錄中。</span><span class="sxs-lookup"><span data-stu-id="327ff-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="327ff-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="327ff-134">Requirements</span></span>



| <span data-ttu-id="327ff-135">需求</span><span class="sxs-lookup"><span data-stu-id="327ff-135">Requirement</span></span> | <span data-ttu-id="327ff-136">值</span><span class="sxs-lookup"><span data-stu-id="327ff-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="327ff-137">版本</span><span class="sxs-lookup"><span data-stu-id="327ff-137">Version</span></span><br/> | <span data-ttu-id="327ff-138">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="327ff-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="327ff-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="327ff-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="327ff-140">**BUTTONELEMENT 元素**</span><span class="sxs-lookup"><span data-stu-id="327ff-140">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> </dl>

 

 





