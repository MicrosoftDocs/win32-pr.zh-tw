---
description: ICE95 會檢查 Control table 和 BBControl 資料表，以確認該佈告欄控制項符合所有公告欄。
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14144c7739dfcc1f1b5e66d92d8e6c1c46ed49fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194393"
---
# <a name="ice95"></a><span data-ttu-id="60e88-103">ICE95</span><span class="sxs-lookup"><span data-stu-id="60e88-103">ICE95</span></span>

<span data-ttu-id="60e88-104">ICE95 會檢查 [Control table](control-table.md) 和 [BBControl 資料表](bbcontrol-table.md) ，以確認該佈告欄控制項符合所有公告欄。</span><span class="sxs-lookup"><span data-stu-id="60e88-104">ICE95 checks the [Control table](control-table.md) and [BBControl table](bbcontrol-table.md) to verify that the billboard controls fit onto all the billboards.</span></span>

## <a name="result"></a><span data-ttu-id="60e88-105">結果</span><span class="sxs-lookup"><span data-stu-id="60e88-105">Result</span></span>

<span data-ttu-id="60e88-106">如果下列任何一項為 true，表示佈告欄控制項無法符合佈告欄。</span><span class="sxs-lookup"><span data-stu-id="60e88-106">If any of the following are true, a billboard control fails to fit on a billboard.</span></span> <span data-ttu-id="60e88-107">ICE95 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="60e88-107">ICE95 posts the following warnings.</span></span>



| <span data-ttu-id="60e88-108">ICE95 警告</span><span class="sxs-lookup"><span data-stu-id="60e88-108">ICE95 warning</span></span>                                                                                                                                                                                                              | <span data-ttu-id="60e88-109">Description</span><span class="sxs-lookup"><span data-stu-id="60e88-109">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e88-110">BBControl 專案 ' \[ 1 \] . \[[BBControl] 資料表中的 [2] 不 \] 符合控制資料表中的所有佈告欄控制項。</span><span class="sxs-lookup"><span data-stu-id="60e88-110">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="60e88-111">X 座標超過最小佈告欄控制項寬度% s 的界限</span><span class="sxs-lookup"><span data-stu-id="60e88-111">The X coordinate exceeds the boundary of the minimum billboard control width %s</span></span>                   | <span data-ttu-id="60e88-112">控制項的 X 座標在佈告欄的寬度之外。</span><span class="sxs-lookup"><span data-stu-id="60e88-112">The control's X coordinate is outside the width of the billboard.</span></span>                          |
| <span data-ttu-id="60e88-113">BBControl 專案 ' \[ 1 \] . \[[BBControl] 資料表中的 [2] 不 \] 符合控制資料表中的所有佈告欄控制項。</span><span class="sxs-lookup"><span data-stu-id="60e88-113">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="60e88-114">Y 座標超過最小的佈告欄控制項高度% s 的界限</span><span class="sxs-lookup"><span data-stu-id="60e88-114">The Y coordinate exceeds the boundary of the minimum billboard control height %s</span></span>                  | <span data-ttu-id="60e88-115">控制項的 Y 座標位於佈告欄的底部。</span><span class="sxs-lookup"><span data-stu-id="60e88-115">The control's Y coordinate is below the bottom of the billboard.</span></span>                           |
| <span data-ttu-id="60e88-116">BBControl 專案 ' \[ 1 \] . \[[BBControl] 資料表中的 [2] 不 \] 符合控制資料表中的所有佈告欄控制項。</span><span class="sxs-lookup"><span data-stu-id="60e88-116">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="60e88-117">X 座標和寬度組合在一起，超過最小的佈告欄控制項寬度% s</span><span class="sxs-lookup"><span data-stu-id="60e88-117">The X coordinate and the width combined together exceeds the minimum billboard control width %s</span></span>   | <span data-ttu-id="60e88-118">控制項的 X 座標加上控制項的寬度，在佈告欄的寬度之外。</span><span class="sxs-lookup"><span data-stu-id="60e88-118">The control's X coordinate plus the control's width is outside the width of the billboard.</span></span> |
| <span data-ttu-id="60e88-119">BBControl 專案 ' \[ 1 \] . \[[BBControl] 資料表中的 [2] 不 \] 符合控制資料表中的所有佈告欄控制項。</span><span class="sxs-lookup"><span data-stu-id="60e88-119">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="60e88-120">Y 座標和高度組合在一起，超過最小的佈告欄控制項高度% s</span><span class="sxs-lookup"><span data-stu-id="60e88-120">The Y coordinate and the height combined together exceeds the minimum billboard control height %s</span></span> | <span data-ttu-id="60e88-121">控制項的 Y 座標加上控制項的高度，在佈告欄的底部。</span><span class="sxs-lookup"><span data-stu-id="60e88-121">The control's Y coordinate plus the control's height is below the bottom of the billboard.</span></span> |



 

## <a name="example"></a><span data-ttu-id="60e88-122">範例</span><span class="sxs-lookup"><span data-stu-id="60e88-122">Example</span></span>

<span data-ttu-id="60e88-123">ICE95 會報告下列範例警告：</span><span class="sxs-lookup"><span data-stu-id="60e88-123">ICE95 reports the following warnings for the example:</span></span>

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

<span data-ttu-id="60e88-124">控制資料表 (部分)  (部分) </span><span class="sxs-lookup"><span data-stu-id="60e88-124">Control Table (partial) (partial)</span></span>



| <span data-ttu-id="60e88-125">控制</span><span class="sxs-lookup"><span data-stu-id="60e88-125">Control</span></span>  | <span data-ttu-id="60e88-126">類型</span><span class="sxs-lookup"><span data-stu-id="60e88-126">Type</span></span>      | <span data-ttu-id="60e88-127">寬度</span><span class="sxs-lookup"><span data-stu-id="60e88-127">Width</span></span> | <span data-ttu-id="60e88-128">高度</span><span class="sxs-lookup"><span data-stu-id="60e88-128">Height</span></span> |
|----------|-----------|-------|--------|
| <span data-ttu-id="60e88-129">control1</span><span class="sxs-lookup"><span data-stu-id="60e88-129">control1</span></span> | <span data-ttu-id="60e88-130">廣告 牌</span><span class="sxs-lookup"><span data-stu-id="60e88-130">Billboard</span></span> | <span data-ttu-id="60e88-131">300</span><span class="sxs-lookup"><span data-stu-id="60e88-131">300</span></span>   | <span data-ttu-id="60e88-132">100</span><span class="sxs-lookup"><span data-stu-id="60e88-132">100</span></span>    |
| <span data-ttu-id="60e88-133">Control2</span><span class="sxs-lookup"><span data-stu-id="60e88-133">Control2</span></span> | <span data-ttu-id="60e88-134">廣告 牌</span><span class="sxs-lookup"><span data-stu-id="60e88-134">Billboard</span></span> | <span data-ttu-id="60e88-135">100</span><span class="sxs-lookup"><span data-stu-id="60e88-135">100</span></span>   | <span data-ttu-id="60e88-136">300</span><span class="sxs-lookup"><span data-stu-id="60e88-136">300</span></span>    |



 

[<span data-ttu-id="60e88-137">BBControl 資料表</span><span class="sxs-lookup"><span data-stu-id="60e88-137">BBControl table</span></span>](bbcontrol-table.md)



| <span data-ttu-id="60e88-138">廣告 牌\_</span><span class="sxs-lookup"><span data-stu-id="60e88-138">Billboard\_</span></span> | <span data-ttu-id="60e88-139">BBControl</span><span class="sxs-lookup"><span data-stu-id="60e88-139">BBControl</span></span>  | <span data-ttu-id="60e88-140">X</span><span class="sxs-lookup"><span data-stu-id="60e88-140">X</span></span>   | <span data-ttu-id="60e88-141">Y</span><span class="sxs-lookup"><span data-stu-id="60e88-141">Y</span></span>   | <span data-ttu-id="60e88-142">寬度</span><span class="sxs-lookup"><span data-stu-id="60e88-142">Width</span></span> | <span data-ttu-id="60e88-143">高度</span><span class="sxs-lookup"><span data-stu-id="60e88-143">Height</span></span> |
|-------------|------------|-----|-----|-------|--------|
| <span data-ttu-id="60e88-144">billboard1</span><span class="sxs-lookup"><span data-stu-id="60e88-144">billboard1</span></span>  | <span data-ttu-id="60e88-145">bbcontrol1</span><span class="sxs-lookup"><span data-stu-id="60e88-145">bbcontrol1</span></span> | <span data-ttu-id="60e88-146">200</span><span class="sxs-lookup"><span data-stu-id="60e88-146">200</span></span> | <span data-ttu-id="60e88-147">0</span><span class="sxs-lookup"><span data-stu-id="60e88-147">0</span></span>   | <span data-ttu-id="60e88-148">100</span><span class="sxs-lookup"><span data-stu-id="60e88-148">100</span></span>   | <span data-ttu-id="60e88-149">100</span><span class="sxs-lookup"><span data-stu-id="60e88-149">100</span></span>    |
| <span data-ttu-id="60e88-150">billboard1</span><span class="sxs-lookup"><span data-stu-id="60e88-150">billboard1</span></span>  | <span data-ttu-id="60e88-151">bbcontrol2</span><span class="sxs-lookup"><span data-stu-id="60e88-151">bbcontrol2</span></span> | <span data-ttu-id="60e88-152">0</span><span class="sxs-lookup"><span data-stu-id="60e88-152">0</span></span>   | <span data-ttu-id="60e88-153">200</span><span class="sxs-lookup"><span data-stu-id="60e88-153">200</span></span> | <span data-ttu-id="60e88-154">100</span><span class="sxs-lookup"><span data-stu-id="60e88-154">100</span></span>   | <span data-ttu-id="60e88-155">100</span><span class="sxs-lookup"><span data-stu-id="60e88-155">100</span></span>    |
| <span data-ttu-id="60e88-156">billboard1</span><span class="sxs-lookup"><span data-stu-id="60e88-156">billboard1</span></span>  | <span data-ttu-id="60e88-157">bbcontrol3</span><span class="sxs-lookup"><span data-stu-id="60e88-157">bbcontrol3</span></span> | <span data-ttu-id="60e88-158">50</span><span class="sxs-lookup"><span data-stu-id="60e88-158">50</span></span>  | <span data-ttu-id="60e88-159">0</span><span class="sxs-lookup"><span data-stu-id="60e88-159">0</span></span>   | <span data-ttu-id="60e88-160">100</span><span class="sxs-lookup"><span data-stu-id="60e88-160">100</span></span>   | <span data-ttu-id="60e88-161">50</span><span class="sxs-lookup"><span data-stu-id="60e88-161">50</span></span>     |
| <span data-ttu-id="60e88-162">billboard1</span><span class="sxs-lookup"><span data-stu-id="60e88-162">billboard1</span></span>  | <span data-ttu-id="60e88-163">bbcontrol4</span><span class="sxs-lookup"><span data-stu-id="60e88-163">bbcontrol4</span></span> | <span data-ttu-id="60e88-164">0</span><span class="sxs-lookup"><span data-stu-id="60e88-164">0</span></span>   | <span data-ttu-id="60e88-165">50</span><span class="sxs-lookup"><span data-stu-id="60e88-165">50</span></span>  | <span data-ttu-id="60e88-166">50</span><span class="sxs-lookup"><span data-stu-id="60e88-166">50</span></span>    | <span data-ttu-id="60e88-167">100</span><span class="sxs-lookup"><span data-stu-id="60e88-167">100</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="60e88-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="60e88-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60e88-169">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="60e88-169">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



