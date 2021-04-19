---
title: CUSTOMSLIDER 資料指標
description: Cursor 屬性指定或抓取當滑鼠停留在滑杆上時所顯示的滑杆控制項游標值。
ms.assetid: 965c21ab-18a0-4459-9d5b-0a35ea2c212f
keywords:
- CUSTOMSLIDER. cursor Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e836dc7ec6efececf81789efe43d8b19d0df1783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999509"
---
# <a name="customslidercursor"></a><span data-ttu-id="6aa48-104">CUSTOMSLIDER 資料指標</span><span class="sxs-lookup"><span data-stu-id="6aa48-104">CUSTOMSLIDER.cursor</span></span>

<span data-ttu-id="6aa48-105">**Cursor** 屬性指定或抓取當滑鼠停留在滑杆上時所顯示的滑杆控制項游標值。</span><span class="sxs-lookup"><span data-stu-id="6aa48-105">The **cursor** attribute specifies or retrieves the value of the slider control cursor that appears when the mouse is over the slider.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="6aa48-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="6aa48-106">Possible Values</span></span>

<span data-ttu-id="6aa48-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="6aa48-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="6aa48-108">值</span><span class="sxs-lookup"><span data-stu-id="6aa48-108">Value</span></span>            | <span data-ttu-id="6aa48-109">描述</span><span class="sxs-lookup"><span data-stu-id="6aa48-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa48-110">系統</span><span class="sxs-lookup"><span data-stu-id="6aa48-110">system</span></span>           | <span data-ttu-id="6aa48-111">平臺相依游標 (通常是箭號) 。</span><span class="sxs-lookup"><span data-stu-id="6aa48-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="6aa48-112">手</span><span class="sxs-lookup"><span data-stu-id="6aa48-112">hand</span></span>             | <span data-ttu-id="6aa48-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="6aa48-113">Default.</span></span> <span data-ttu-id="6aa48-114">資料指標是手。</span><span class="sxs-lookup"><span data-stu-id="6aa48-114">Cursor is a hand.</span></span>                                                                  |
| <span data-ttu-id="6aa48-115">help</span><span class="sxs-lookup"><span data-stu-id="6aa48-115">help</span></span>             | <span data-ttu-id="6aa48-116">有問號的箭號可用來指出說明。</span><span class="sxs-lookup"><span data-stu-id="6aa48-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="6aa48-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="6aa48-117">sizeall</span></span>          | <span data-ttu-id="6aa48-118">四指向的箭號，指向北、南、東和西。</span><span class="sxs-lookup"><span data-stu-id="6aa48-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="6aa48-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="6aa48-119">sizenesw</span></span>         | <span data-ttu-id="6aa48-120">指向東北和西南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="6aa48-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="6aa48-121">sizens</span><span class="sxs-lookup"><span data-stu-id="6aa48-121">sizens</span></span>           | <span data-ttu-id="6aa48-122">指向北和南的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="6aa48-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="6aa48-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="6aa48-123">sizenwse</span></span>         | <span data-ttu-id="6aa48-124">雙指向箭號，指向西北和東南部。</span><span class="sxs-lookup"><span data-stu-id="6aa48-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="6aa48-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="6aa48-125">sizewe</span></span>           | <span data-ttu-id="6aa48-126">指向 west 和東的雙指向箭號。</span><span class="sxs-lookup"><span data-stu-id="6aa48-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="6aa48-127">uparrow</span><span class="sxs-lookup"><span data-stu-id="6aa48-127">uparrow</span></span>          | <span data-ttu-id="6aa48-128">垂直箭號向上。</span><span class="sxs-lookup"><span data-stu-id="6aa48-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="6aa48-129">\*ani 或 \* 中</span><span class="sxs-lookup"><span data-stu-id="6aa48-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="6aa48-130">任何 ani 或..................................)  (</span><span class="sxs-lookup"><span data-stu-id="6aa48-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6aa48-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="6aa48-131">Requirements</span></span>



| <span data-ttu-id="6aa48-132">需求</span><span class="sxs-lookup"><span data-stu-id="6aa48-132">Requirement</span></span> | <span data-ttu-id="6aa48-133">值</span><span class="sxs-lookup"><span data-stu-id="6aa48-133">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6aa48-134">版本</span><span class="sxs-lookup"><span data-stu-id="6aa48-134">Version</span></span><br/> | <span data-ttu-id="6aa48-135">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="6aa48-135">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6aa48-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6aa48-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aa48-137">**CUSTOMSLIDER 元素**</span><span class="sxs-lookup"><span data-stu-id="6aa48-137">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> </dl>

 

 





