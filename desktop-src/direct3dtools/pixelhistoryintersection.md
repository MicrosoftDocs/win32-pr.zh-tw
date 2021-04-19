---
description: 表示特定的相關資訊。
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixelHistoryIntersection 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972754"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span data-ttu-id="a6a61-103"><span id="vspixengine.pixelhistoryintersection"></span>PixelHistoryIntersection 結構</span><span class="sxs-lookup"><span data-stu-id="a6a61-103"><span id="vspixengine.pixelhistoryintersection"></span>PixelHistoryIntersection structure</span></span>

<span data-ttu-id="a6a61-104">代表特定的相關資訊</span><span class="sxs-lookup"><span data-stu-id="a6a61-104">Represents information about a particular</span></span>

## <a name="syntax"></a><span data-ttu-id="a6a61-105">語法</span><span class="sxs-lookup"><span data-stu-id="a6a61-105">Syntax</span></span>


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a><span data-ttu-id="a6a61-106">成員</span><span class="sxs-lookup"><span data-stu-id="a6a61-106">Members</span></span>

<span data-ttu-id="a6a61-107">**frameNumber**</span><span class="sxs-lookup"><span data-stu-id="a6a61-107">**frameNumber**</span></span>  
<span data-ttu-id="a6a61-108">使用這項作業 assocaited 的圖形事件架構。</span><span class="sxs-lookup"><span data-stu-id="a6a61-108">The frame of the graphics event assocaited with this operation.</span></span>

<span data-ttu-id="a6a61-109">**開齋節**</span><span class="sxs-lookup"><span data-stu-id="a6a61-109">**eid**</span></span>  
<span data-ttu-id="a6a61-110">與這項作業相關聯之圖形事件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6a61-110">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="a6a61-111">**renderTargetPtr**</span><span class="sxs-lookup"><span data-stu-id="a6a61-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="a6a61-112">原本與此作業) 的已捕捉應用程式內 (的呈現目標。</span><span class="sxs-lookup"><span data-stu-id="a6a61-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="a6a61-113">**eventType**</span><span class="sxs-lookup"><span data-stu-id="a6a61-113">**eventType**</span></span>  
<span data-ttu-id="a6a61-114">與這項作業相關聯的事件種類 (具體而言，此事件是否為繪製呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="a6a61-114">The kind of event associated with this operation (specifically, whether this event is a draw call).</span></span>

<span data-ttu-id="a6a61-115">**點**</span><span class="sxs-lookup"><span data-stu-id="a6a61-115">**point**</span></span>  
<span data-ttu-id="a6a61-116">畫面格緩衝區中圖元的座標。</span><span class="sxs-lookup"><span data-stu-id="a6a61-116">The coordinates of the pixel in the framebuffer.</span></span>

<span data-ttu-id="a6a61-117">**bAssemblerStageGeneratesInstanceID**</span><span class="sxs-lookup"><span data-stu-id="a6a61-117">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="a6a61-118">如果輸入組合語言產生實例識別碼，則為 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="a6a61-118">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="a6a61-119">**flags**</span><span class="sxs-lookup"><span data-stu-id="a6a61-119">**flags**</span></span>  
<span data-ttu-id="a6a61-120">PIXELHISTORYFLAGS 值的組合。</span><span class="sxs-lookup"><span data-stu-id="a6a61-120">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="a6a61-121">如需詳細資訊，請參閱 PIXELHISTORYFLAGS 列舉。</span><span class="sxs-lookup"><span data-stu-id="a6a61-121">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="a6a61-122">**fbInitialRed**</span><span class="sxs-lookup"><span data-stu-id="a6a61-122">**fbInitialRed**</span></span>  
<span data-ttu-id="a6a61-123">畫面格緩衝區：在合併任何圖元著色器輸出之前，畫面格緩衝區的紅色色彩元件值;也就是在此框架的開頭。</span><span class="sxs-lookup"><span data-stu-id="a6a61-123">Framebuffer: value of red color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="a6a61-124">**fbInitialGreen**</span><span class="sxs-lookup"><span data-stu-id="a6a61-124">**fbInitialGreen**</span></span>  
<span data-ttu-id="a6a61-125">畫面格緩衝區：在合併任何圖元著色器輸出之前，畫面格緩衝區的綠色色彩元件值;也就是在此框架的開頭。</span><span class="sxs-lookup"><span data-stu-id="a6a61-125">Framebuffer: value of green color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="a6a61-126">**fbInitialBlue**</span><span class="sxs-lookup"><span data-stu-id="a6a61-126">**fbInitialBlue**</span></span>  
<span data-ttu-id="a6a61-127">畫面格緩衝區：合併任何圖元著色器輸出之前的畫面格緩衝區藍色色彩元件值;也就是在此框架的開頭。</span><span class="sxs-lookup"><span data-stu-id="a6a61-127">Framebuffer: value of blue color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="a6a61-128">**fbInitialAlpha**</span><span class="sxs-lookup"><span data-stu-id="a6a61-128">**fbInitialAlpha**</span></span>  
<span data-ttu-id="a6a61-129">畫面格緩衝區：在合併任何圖元著色器輸出之前，畫面格緩衝區 Alpha 色彩元件的值;也就是在此框架的開頭。</span><span class="sxs-lookup"><span data-stu-id="a6a61-129">Framebuffer: value of alpha color component of framebuffer before any pixel shader output is merged; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="a6a61-130">**LabelFBInitialRed**</span><span class="sxs-lookup"><span data-stu-id="a6a61-130">**LabelFBInitialRed**</span></span>  
<span data-ttu-id="a6a61-131">COM 字串，其中包含與畫面格緩衝區的紅色色彩元件相關聯的標籤名稱（任何圖元網底之前）;也就是在此框架的開頭。</span><span class="sxs-lookup"><span data-stu-id="a6a61-131">A COM string containing the name of the label associated with the red color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="a6a61-132">**LabelFBInitialGreen**</span><span class="sxs-lookup"><span data-stu-id="a6a61-132">**LabelFBInitialGreen**</span></span>  
<span data-ttu-id="a6a61-133">COM 字串，其中包含與畫面格緩衝區的綠色色彩元件相關聯的標籤名稱（任何圖元網底之前）;也就是在此框架的開頭。</span><span class="sxs-lookup"><span data-stu-id="a6a61-133">A COM string containing the name of the label associated with the green color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="a6a61-134">**LabelFBInitialBlue**</span><span class="sxs-lookup"><span data-stu-id="a6a61-134">**LabelFBInitialBlue**</span></span>  
<span data-ttu-id="a6a61-135">COM 字串，其中包含與畫面格緩衝區的藍色色彩元件相關聯的標籤名稱（任何圖元網底之前）;也就是在此框架的開頭。</span><span class="sxs-lookup"><span data-stu-id="a6a61-135">A COM string containing the name of the label associated with the blue color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="a6a61-136">**LabelFBInitialAlpha**</span><span class="sxs-lookup"><span data-stu-id="a6a61-136">**LabelFBInitialAlpha**</span></span>  
<span data-ttu-id="a6a61-137">COM 字串，其中包含與畫面格緩衝區的 Alpha 色彩元件相關聯的標籤名稱（任何圖元網底之前）;也就是在此框架的開頭。</span><span class="sxs-lookup"><span data-stu-id="a6a61-137">A COM string containing the name of the label associated with the alpha color component of the framebuffer before any pixel shading; that is, at the beginning of this frame.</span></span>

<span data-ttu-id="a6a61-138">**fbRed**</span><span class="sxs-lookup"><span data-stu-id="a6a61-138">**fbRed**</span></span>  
<span data-ttu-id="a6a61-139">畫面格緩衝區：合併所有圖元著色器輸出之後，畫面格緩衝區的紅色色彩元件值;也就是最後的畫面格緩衝區色彩。</span><span class="sxs-lookup"><span data-stu-id="a6a61-139">Framebuffer: value of red color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="a6a61-140">**fbGreen**</span><span class="sxs-lookup"><span data-stu-id="a6a61-140">**fbGreen**</span></span>  
<span data-ttu-id="a6a61-141">畫面格緩衝區：合併所有圖元著色器輸出之後，畫面格緩衝區的綠色色彩元件值;也就是最後的畫面格緩衝區色彩。</span><span class="sxs-lookup"><span data-stu-id="a6a61-141">Framebuffer: value of green color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="a6a61-142">**fbBlue**</span><span class="sxs-lookup"><span data-stu-id="a6a61-142">**fbBlue**</span></span>  
<span data-ttu-id="a6a61-143">畫面格緩衝區：合併所有圖元著色器輸出之後，畫面格緩衝區藍色色彩元件的值;也就是最後的畫面格緩衝區色彩。</span><span class="sxs-lookup"><span data-stu-id="a6a61-143">Framebuffer: value of blue color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="a6a61-144">**fbAlpha**</span><span class="sxs-lookup"><span data-stu-id="a6a61-144">**fbAlpha**</span></span>  
<span data-ttu-id="a6a61-145">畫面格緩衝區：合併所有圖元著色器輸出之後，畫面格緩衝區 Alpha 色彩元件的值;也就是最後的畫面格緩衝區色彩。</span><span class="sxs-lookup"><span data-stu-id="a6a61-145">Framebuffer: value of alpha color component of framebuffer after all pixel shader output is merged; that is, the final framebuffer color.</span></span>

<span data-ttu-id="a6a61-146">**LabelFBRed**</span><span class="sxs-lookup"><span data-stu-id="a6a61-146">**LabelFBRed**</span></span>  
<span data-ttu-id="a6a61-147">COM 字串，其中包含與畫面格緩衝區的紅色色彩元件相關聯的標籤名稱（在所有圖元陰影之後）;也就是最後的畫面格緩衝區色彩。</span><span class="sxs-lookup"><span data-stu-id="a6a61-147">A COM string containing the name of the label associated with the red color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="a6a61-148">**LabelFBGreen**</span><span class="sxs-lookup"><span data-stu-id="a6a61-148">**LabelFBGreen**</span></span>  
<span data-ttu-id="a6a61-149">COM 字串，其中包含與畫面格緩衝區的綠色色彩元件相關聯的標籤名稱（在所有圖元陰影之後）;也就是最後的畫面格緩衝區色彩。</span><span class="sxs-lookup"><span data-stu-id="a6a61-149">A COM string containing the name of the label associated with the green color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="a6a61-150">**LabelFBBlue**</span><span class="sxs-lookup"><span data-stu-id="a6a61-150">**LabelFBBlue**</span></span>  
<span data-ttu-id="a6a61-151">COM 字串，其中包含與畫面格緩衝區的藍色色彩元件相關聯的標籤名稱（在所有圖元陰影之後）;也就是最後的畫面格緩衝區色彩。</span><span class="sxs-lookup"><span data-stu-id="a6a61-151">A COM string containing the name of the label associated with the blue color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="a6a61-152">**LabelFBAlpha**</span><span class="sxs-lookup"><span data-stu-id="a6a61-152">**LabelFBAlpha**</span></span>  
<span data-ttu-id="a6a61-153">COM 字串，其中包含與畫面格緩衝區的 Alpha 色彩元件相關聯的標籤名稱（在所有圖元陰影之後）;也就是最後的畫面格緩衝區色彩。</span><span class="sxs-lookup"><span data-stu-id="a6a61-153">A COM string containing the name of the label associated with the alpha color component of the framebuffer after all pixel shading; that is, the final framebuffer color.</span></span>

<span data-ttu-id="a6a61-154">**pixelKillReason**</span><span class="sxs-lookup"><span data-stu-id="a6a61-154">**pixelKillReason**</span></span>  
<span data-ttu-id="a6a61-155">指定圖元的色彩比重被終止的原因。</span><span class="sxs-lookup"><span data-stu-id="a6a61-155">Specifies the reason that the pixel's color contribution was killed.</span></span>

<span data-ttu-id="a6a61-156">**HResult**</span><span class="sxs-lookup"><span data-stu-id="a6a61-156">**HResult**</span></span>  
<span data-ttu-id="a6a61-157">如果發生錯誤，則包含指定錯誤的 DirectX HRESULT。</span><span class="sxs-lookup"><span data-stu-id="a6a61-157">If an error occurred, contains the DirectX HRESULT that specifies the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a61-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6a61-158">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a6a61-159">標頭</span><span class="sxs-lookup"><span data-stu-id="a6a61-159">Header</span></span></p></td><td><span data-ttu-id="a6a61-160">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="a6a61-160">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



