---
description: 組合器轉換
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: 組合器轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550730"
---
# <a name="compositor-transition"></a><span data-ttu-id="d8743-103">組合器轉換</span><span class="sxs-lookup"><span data-stu-id="d8743-103">Compositor Transition</span></span>

> [!Note]  
> <span data-ttu-id="d8743-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d8743-104">\[Deprecated.</span></span> <span data-ttu-id="d8743-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d8743-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d8743-106">組合器轉換會在背景將 subrectangle 從前景合成至指定的矩形，而不會改變背景的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="d8743-106">The Compositor transition composites a subrectangle from the foreground into a designated rectangle on the background, without altering the rest of the background.</span></span> <span data-ttu-id="d8743-107">使用這項轉換來建立分割畫面或圖片圖片效果。</span><span class="sxs-lookup"><span data-stu-id="d8743-107">Use this transition to create split-screen or picture-in-picture effects.</span></span>

<span data-ttu-id="d8743-108">下圖顯示組合器轉換：</span><span class="sxs-lookup"><span data-stu-id="d8743-108">The following image shows the compositor transition:</span></span>

![組合器轉換](images/trans-compositor.png)

<span data-ttu-id="d8743-110">類別識別碼 (CLSID) ： {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span><span class="sxs-lookup"><span data-stu-id="d8743-110">Class ID (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span></span>

<span data-ttu-id="d8743-111">CLSID 變數名稱： CLSID \_ DxtCompositor</span><span class="sxs-lookup"><span data-stu-id="d8743-111">CLSID Variable Name: CLSID\_DxtCompositor</span></span>

<span data-ttu-id="d8743-112">易記名稱： "DxtCompositor"</span><span class="sxs-lookup"><span data-stu-id="d8743-112">Friendly Name: "DxtCompositor"</span></span>

<span data-ttu-id="d8743-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d8743-113">Properties</span></span>



| <span data-ttu-id="d8743-114">屬性</span><span class="sxs-lookup"><span data-stu-id="d8743-114">Property</span></span>   | <span data-ttu-id="d8743-115">類型</span><span class="sxs-lookup"><span data-stu-id="d8743-115">Type</span></span> | <span data-ttu-id="d8743-116">預設</span><span class="sxs-lookup"><span data-stu-id="d8743-116">Default</span></span> | <span data-ttu-id="d8743-117">描述</span><span class="sxs-lookup"><span data-stu-id="d8743-117">Description</span></span>                                                    |
|------------|------|---------|----------------------------------------------------------------|
| <span data-ttu-id="d8743-118">高度</span><span class="sxs-lookup"><span data-stu-id="d8743-118">Height</span></span>     | <span data-ttu-id="d8743-119">long</span><span class="sxs-lookup"><span data-stu-id="d8743-119">long</span></span> | <span data-ttu-id="d8743-120">0</span><span class="sxs-lookup"><span data-stu-id="d8743-120">0</span></span>       | <span data-ttu-id="d8743-121">目標矩形的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8743-121">Height of the target rectangle, in pixels.</span></span>                     |
| <span data-ttu-id="d8743-122">OffsetX</span><span class="sxs-lookup"><span data-stu-id="d8743-122">OffsetX</span></span>    | <span data-ttu-id="d8743-123">long</span><span class="sxs-lookup"><span data-stu-id="d8743-123">long</span></span> | <span data-ttu-id="d8743-124">0</span><span class="sxs-lookup"><span data-stu-id="d8743-124">0</span></span>       | <span data-ttu-id="d8743-125">目標矩形的水準位移（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8743-125">Horizontal offset of the target rectangle, in pixels.</span></span>          |
| <span data-ttu-id="d8743-126">OffsetY</span><span class="sxs-lookup"><span data-stu-id="d8743-126">OffsetY</span></span>    | <span data-ttu-id="d8743-127">long</span><span class="sxs-lookup"><span data-stu-id="d8743-127">long</span></span> | <span data-ttu-id="d8743-128">0</span><span class="sxs-lookup"><span data-stu-id="d8743-128">0</span></span>       | <span data-ttu-id="d8743-129">目標矩形的垂直位移（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8743-129">Vertical offset of the target rectangle, in pixels.</span></span>            |
| <span data-ttu-id="d8743-130">SrcHeight</span><span class="sxs-lookup"><span data-stu-id="d8743-130">SrcHeight</span></span>  | <span data-ttu-id="d8743-131">long</span><span class="sxs-lookup"><span data-stu-id="d8743-131">long</span></span> | <span data-ttu-id="d8743-132">0</span><span class="sxs-lookup"><span data-stu-id="d8743-132">0</span></span>       | <span data-ttu-id="d8743-133">來源的 subrectangle 高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8743-133">The height of the subrectangle on the source, in pixels.</span></span>       |
| <span data-ttu-id="d8743-134">SrcOffsetX</span><span class="sxs-lookup"><span data-stu-id="d8743-134">SrcOffsetX</span></span> | <span data-ttu-id="d8743-135">long</span><span class="sxs-lookup"><span data-stu-id="d8743-135">long</span></span> | <span data-ttu-id="d8743-136">0</span><span class="sxs-lookup"><span data-stu-id="d8743-136">0</span></span>       | <span data-ttu-id="d8743-137">Subrectangle 在來源上的 x 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8743-137">The x-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="d8743-138">SrcOffsetY</span><span class="sxs-lookup"><span data-stu-id="d8743-138">SrcOffsetY</span></span> | <span data-ttu-id="d8743-139">long</span><span class="sxs-lookup"><span data-stu-id="d8743-139">long</span></span> | <span data-ttu-id="d8743-140">0</span><span class="sxs-lookup"><span data-stu-id="d8743-140">0</span></span>       | <span data-ttu-id="d8743-141">Subrectangle 在來源上的 y 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8743-141">The y-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="d8743-142">SrcWidth</span><span class="sxs-lookup"><span data-stu-id="d8743-142">SrcWidth</span></span>   | <span data-ttu-id="d8743-143">long</span><span class="sxs-lookup"><span data-stu-id="d8743-143">long</span></span> | <span data-ttu-id="d8743-144">0</span><span class="sxs-lookup"><span data-stu-id="d8743-144">0</span></span>       | <span data-ttu-id="d8743-145">來源上的 subrectangle 寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8743-145">The width of the subrectangle on the source, in pixels.</span></span>        |
| <span data-ttu-id="d8743-146">寬度</span><span class="sxs-lookup"><span data-stu-id="d8743-146">Width</span></span>      | <span data-ttu-id="d8743-147">long</span><span class="sxs-lookup"><span data-stu-id="d8743-147">long</span></span> | <span data-ttu-id="d8743-148">0</span><span class="sxs-lookup"><span data-stu-id="d8743-148">0</span></span>       | <span data-ttu-id="d8743-149">目標矩形的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8743-149">Width of the target rectangle, in pixels.</span></span>                      |



 

<span data-ttu-id="d8743-150">下圖說明這些屬性：</span><span class="sxs-lookup"><span data-stu-id="d8743-150">The following diagram illustrates these properties:</span></span>

![組合器屬性](images/compmeasure.png)

## <a name="related-topics"></a><span data-ttu-id="d8743-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8743-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8743-153">轉換和效果</span><span class="sxs-lookup"><span data-stu-id="d8743-153">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> </dl>

 

 



