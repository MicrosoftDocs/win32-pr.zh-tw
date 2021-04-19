---
description: 代表圖元歷程記錄的相關資訊。
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixelHistoryOperation 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973136"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span data-ttu-id="de866-103"><span id="vspixengine.pixelhistoryoperation"></span>PixelHistoryOperation 結構</span><span class="sxs-lookup"><span data-stu-id="de866-103"><span id="vspixengine.pixelhistoryoperation"></span>PixelHistoryOperation structure</span></span>

<span data-ttu-id="de866-104">代表圖元歷程記錄的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="de866-104">Represents information about pixel history.</span></span>

## <a name="syntax"></a><span data-ttu-id="de866-105">語法</span><span class="sxs-lookup"><span data-stu-id="de866-105">Syntax</span></span>


```C++
} PixelHistoryOperation;
```

## <a name="members"></a><span data-ttu-id="de866-106">成員</span><span class="sxs-lookup"><span data-stu-id="de866-106">Members</span></span>

<span data-ttu-id="de866-107">**開齋節**</span><span class="sxs-lookup"><span data-stu-id="de866-107">**eid**</span></span>  
<span data-ttu-id="de866-108">與這項作業相關聯之圖形事件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="de866-108">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="de866-109">**五 氯 酚**</span><span class="sxs-lookup"><span data-stu-id="de866-109">**PCP**</span></span>  
<span data-ttu-id="de866-110">與此作業相關聯的已壓縮呼叫。</span><span class="sxs-lookup"><span data-stu-id="de866-110">Packed calls associated with this operation.</span></span>

<span data-ttu-id="de866-111">**renderTargetPtr**</span><span class="sxs-lookup"><span data-stu-id="de866-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="de866-112">原本與此作業) 的已捕捉應用程式內 (的呈現目標。</span><span class="sxs-lookup"><span data-stu-id="de866-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="de866-113">**iPrim**</span><span class="sxs-lookup"><span data-stu-id="de866-113">**iPrim**</span></span>  
<span data-ttu-id="de866-114">與 jumpbox 他的作業相關聯的實際基本類型索引。</span><span class="sxs-lookup"><span data-stu-id="de866-114">The index of the actual primitive associated witht his operation.</span></span>

<span data-ttu-id="de866-115">**numPrims**</span><span class="sxs-lookup"><span data-stu-id="de866-115">**numPrims**</span></span>  
<span data-ttu-id="de866-116">與這項作業相關聯之基本專案的總數。</span><span class="sxs-lookup"><span data-stu-id="de866-116">The total number of primitives associated with this operation.</span></span>

<span data-ttu-id="de866-117">**numVertsPerPrim**</span><span class="sxs-lookup"><span data-stu-id="de866-117">**numVertsPerPrim**</span></span>  
<span data-ttu-id="de866-118">每個基本的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="de866-118">The number of vertices per primitive.</span></span>

<span data-ttu-id="de866-119">**iInstance**</span><span class="sxs-lookup"><span data-stu-id="de866-119">**iInstance**</span></span>  
<span data-ttu-id="de866-120">轉譯實例時，與這項作業相關聯之實際實例的實例編號。</span><span class="sxs-lookup"><span data-stu-id="de866-120">When rendering instances, the instance number of the actual instance associated with this operation.</span></span>

<span data-ttu-id="de866-121">**iInstanceCount**</span><span class="sxs-lookup"><span data-stu-id="de866-121">**iInstanceCount**</span></span>  
<span data-ttu-id="de866-122">轉譯實例時，與這項作業相關聯的實例總數。</span><span class="sxs-lookup"><span data-stu-id="de866-122">When rendering instances, the total number of instances associated with this operation.</span></span>

<span data-ttu-id="de866-123">**bAssemblerStageGeneratesInstanceID**</span><span class="sxs-lookup"><span data-stu-id="de866-123">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="de866-124">如果輸入組合語言產生實例識別碼，則為 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="de866-124">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="de866-125">**flags**</span><span class="sxs-lookup"><span data-stu-id="de866-125">**flags**</span></span>  
<span data-ttu-id="de866-126">PIXELHISTORYFLAGS 值的組合。</span><span class="sxs-lookup"><span data-stu-id="de866-126">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="de866-127">如需詳細資訊，請參閱 PIXELHISTORYFLAGS 列舉。</span><span class="sxs-lookup"><span data-stu-id="de866-127">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="de866-128">**pVSFile**</span><span class="sxs-lookup"><span data-stu-id="de866-128">**pVSFile**</span></span>  
<span data-ttu-id="de866-129">圖元著色器位元組資料流程的 FILEPTR。</span><span class="sxs-lookup"><span data-stu-id="de866-129">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="de866-130">這會傳回，以便進行 debug。</span><span class="sxs-lookup"><span data-stu-id="de866-130">This is passed back in order to debug.</span></span>

<span data-ttu-id="de866-131">**pGSFile**</span><span class="sxs-lookup"><span data-stu-id="de866-131">**pGSFile**</span></span>  
<span data-ttu-id="de866-132">幾何著色器位元組資料流程的 FILEPTR。</span><span class="sxs-lookup"><span data-stu-id="de866-132">A FILEPTR for the geometry shader byte stream.</span></span> <span data-ttu-id="de866-133">這會傳回，以便進行 debug。</span><span class="sxs-lookup"><span data-stu-id="de866-133">This is passed back in order to debug.</span></span>

<span data-ttu-id="de866-134">**pPSFile**</span><span class="sxs-lookup"><span data-stu-id="de866-134">**pPSFile**</span></span>  
<span data-ttu-id="de866-135">圖元著色器位元組資料流程的 FILEPTR。</span><span class="sxs-lookup"><span data-stu-id="de866-135">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="de866-136">這會傳回，以便進行 debug。</span><span class="sxs-lookup"><span data-stu-id="de866-136">This is passed back in order to debug.</span></span>

<span data-ttu-id="de866-137">**pHSFile**</span><span class="sxs-lookup"><span data-stu-id="de866-137">**pHSFile**</span></span>  
<span data-ttu-id="de866-138">輪廓著色器位元組資料流程的 FILEPTR。</span><span class="sxs-lookup"><span data-stu-id="de866-138">A FILEPTR for the hull shader byte stream.</span></span> <span data-ttu-id="de866-139">這會傳回，以便進行 debug。</span><span class="sxs-lookup"><span data-stu-id="de866-139">This is passed back in order to debug.</span></span>

<span data-ttu-id="de866-140">**pDSFile**</span><span class="sxs-lookup"><span data-stu-id="de866-140">**pDSFile**</span></span>  
<span data-ttu-id="de866-141">網域著色器位元組資料流程的 FILEPTR。</span><span class="sxs-lookup"><span data-stu-id="de866-141">A FILEPTR for the domain shader byte stream.</span></span> <span data-ttu-id="de866-142">這會傳回，以便進行 debug。</span><span class="sxs-lookup"><span data-stu-id="de866-142">This is passed back in order to debug.</span></span>

<span data-ttu-id="de866-143">**pCSFile**</span><span class="sxs-lookup"><span data-stu-id="de866-143">**pCSFile**</span></span>  
<span data-ttu-id="de866-144">計算著色器位元組資料流程的 FILEPTR。</span><span class="sxs-lookup"><span data-stu-id="de866-144">A FILEPTR for the compute shader byte stream.</span></span> <span data-ttu-id="de866-145">這會傳回，以便進行 debug。</span><span class="sxs-lookup"><span data-stu-id="de866-145">This is passed back in order to debug.</span></span>

<span data-ttu-id="de866-146">**VertexShaderFile**</span><span class="sxs-lookup"><span data-stu-id="de866-146">**VertexShaderFile**</span></span>  
<span data-ttu-id="de866-147">COM 字串，其中包含頂點著色器原始程式檔的 filepath。</span><span class="sxs-lookup"><span data-stu-id="de866-147">A COM string containing the filepath of the vertex shader source file.</span></span>

<span data-ttu-id="de866-148">**PixelShaderFile**</span><span class="sxs-lookup"><span data-stu-id="de866-148">**PixelShaderFile**</span></span>  
<span data-ttu-id="de866-149">COM 字串，其中包含圖元著色器原始程式檔的 filepath。</span><span class="sxs-lookup"><span data-stu-id="de866-149">A COM string containing the filepath of the pixel shader source file.</span></span>

<span data-ttu-id="de866-150">**GeometryShaderFile**</span><span class="sxs-lookup"><span data-stu-id="de866-150">**GeometryShaderFile**</span></span>  
<span data-ttu-id="de866-151">COM 字串，其中包含幾何著色器原始程式檔的 filepath。</span><span class="sxs-lookup"><span data-stu-id="de866-151">A COM string containing the filepath of the geometry shader source file.</span></span>

<span data-ttu-id="de866-152">**HullShaderFile**</span><span class="sxs-lookup"><span data-stu-id="de866-152">**HullShaderFile**</span></span>  
<span data-ttu-id="de866-153">COM 字串，其中包含輪廓著色器原始程式檔的 filepath。</span><span class="sxs-lookup"><span data-stu-id="de866-153">A COM string containing the filepath of the hull shader source file.</span></span>

<span data-ttu-id="de866-154">**DomainShaderFile**</span><span class="sxs-lookup"><span data-stu-id="de866-154">**DomainShaderFile**</span></span>  
<span data-ttu-id="de866-155">COM 字串，其中包含網域著色器原始程式檔的 filepath。</span><span class="sxs-lookup"><span data-stu-id="de866-155">A COM string containing the filepath of the domain shader source file.</span></span>

<span data-ttu-id="de866-156">**psRed**</span><span class="sxs-lookup"><span data-stu-id="de866-156">**psRed**</span></span>  
<span data-ttu-id="de866-157">圖元著色器輸出：紅色色彩元件的值。</span><span class="sxs-lookup"><span data-stu-id="de866-157">Pixel shader output: value of red color component.</span></span>

<span data-ttu-id="de866-158">**psGreen**</span><span class="sxs-lookup"><span data-stu-id="de866-158">**psGreen**</span></span>  
<span data-ttu-id="de866-159">圖元著色器輸出：綠色色彩元件的值。</span><span class="sxs-lookup"><span data-stu-id="de866-159">Pixel shader output: value of green color component.</span></span>

<span data-ttu-id="de866-160">**psBlue**</span><span class="sxs-lookup"><span data-stu-id="de866-160">**psBlue**</span></span>  
<span data-ttu-id="de866-161">圖元著色器輸出：藍色色彩元件的值</span><span class="sxs-lookup"><span data-stu-id="de866-161">Pixel shader output: value of blue color component</span></span>

<span data-ttu-id="de866-162">**psAlpha**</span><span class="sxs-lookup"><span data-stu-id="de866-162">**psAlpha**</span></span>  
<span data-ttu-id="de866-163">圖元著色器輸出： Alpha 色彩元件的值</span><span class="sxs-lookup"><span data-stu-id="de866-163">Pixel shader output: value of alpha color component</span></span>

<span data-ttu-id="de866-164">**LabelPSRed**</span><span class="sxs-lookup"><span data-stu-id="de866-164">**LabelPSRed**</span></span>  
<span data-ttu-id="de866-165">COM 字串，其中包含與圖元著色器輸出的紅色色彩元件相關聯的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="de866-165">A COM string containing the name of the label associated with the red color component of the pixel shader output.</span></span>

<span data-ttu-id="de866-166">**LabelPSGreen**</span><span class="sxs-lookup"><span data-stu-id="de866-166">**LabelPSGreen**</span></span>  
<span data-ttu-id="de866-167">COM 字串，其中包含與圖元著色器輸出的綠色色彩元件相關聯的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="de866-167">A COM string containing the name of the label associated with the green color component of the pixel shader output.</span></span>

<span data-ttu-id="de866-168">**LabelPSBlue**</span><span class="sxs-lookup"><span data-stu-id="de866-168">**LabelPSBlue**</span></span>  
<span data-ttu-id="de866-169">COM 字串，其中包含與圖元著色器輸出的藍色色彩元件相關聯的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="de866-169">A COM string containing the name of the label associated with the blue color component of the pixel shader output.</span></span>

<span data-ttu-id="de866-170">**LabelPSAlpha**</span><span class="sxs-lookup"><span data-stu-id="de866-170">**LabelPSAlpha**</span></span>  
<span data-ttu-id="de866-171">COM 字串，其中包含與圖元著色器輸出的 Alpha 色彩元件相關聯的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="de866-171">A COM string containing the name of the label associated with the alpha color component of the pixel shader output.</span></span>

<span data-ttu-id="de866-172">**pixelKillReason**</span><span class="sxs-lookup"><span data-stu-id="de866-172">**pixelKillReason**</span></span>  
<span data-ttu-id="de866-173">圖元著色器輸出：已終止圖元輸出的原因。</span><span class="sxs-lookup"><span data-stu-id="de866-173">Pixel shader output: reason the pixel output was killed.</span></span>

<span data-ttu-id="de866-174">**pixelOccluded**</span><span class="sxs-lookup"><span data-stu-id="de866-174">**pixelOccluded**</span></span>  
<span data-ttu-id="de866-175">如果圖元是 pixels occluded，則為 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="de866-175">true if the pixel is occluded; otherwise, false.</span></span>

<span data-ttu-id="de866-176">**fbRed**</span><span class="sxs-lookup"><span data-stu-id="de866-176">**fbRed**</span></span>  
<span data-ttu-id="de866-177">畫面格緩衝區：合併圖元著色器輸出之前，畫面格緩衝區的紅色色彩元件的值。</span><span class="sxs-lookup"><span data-stu-id="de866-177">Framebuffer: value of red color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="de866-178">**fbGreen**</span><span class="sxs-lookup"><span data-stu-id="de866-178">**fbGreen**</span></span>  
<span data-ttu-id="de866-179">畫面格緩衝區：合併圖元著色器輸出之前，畫面格緩衝區的綠色色彩元件的值。</span><span class="sxs-lookup"><span data-stu-id="de866-179">Framebuffer: value of green color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="de866-180">**fbBlue**</span><span class="sxs-lookup"><span data-stu-id="de866-180">**fbBlue**</span></span>  
<span data-ttu-id="de866-181">畫面格緩衝區：合併圖元著色器輸出之前的畫面格緩衝區藍色色彩元件值。</span><span class="sxs-lookup"><span data-stu-id="de866-181">Framebuffer: value of blue color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="de866-182">**fbAlpha**</span><span class="sxs-lookup"><span data-stu-id="de866-182">**fbAlpha**</span></span>  
<span data-ttu-id="de866-183">畫面格緩衝區：合併圖元著色器輸出之前，畫面格緩衝區 Alpha 色彩元件的值。</span><span class="sxs-lookup"><span data-stu-id="de866-183">Framebuffer: value of alpha color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="de866-184">**LabelFBRed**</span><span class="sxs-lookup"><span data-stu-id="de866-184">**LabelFBRed**</span></span>  
<span data-ttu-id="de866-185">COM 字串，其中包含與畫面格緩衝區的紅色色彩元件相關聯的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="de866-185">A COM string containing the name of the label associated with the red color component of the framebuffer.</span></span>

<span data-ttu-id="de866-186">**LabelFBGreen**</span><span class="sxs-lookup"><span data-stu-id="de866-186">**LabelFBGreen**</span></span>  
<span data-ttu-id="de866-187">COM 字串，其中包含與畫面格緩衝區的綠色色彩元件相關聯的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="de866-187">A COM string containing the name of the label associated with the green color component of the framebuffer.</span></span>

<span data-ttu-id="de866-188">**LabelFBBlue**</span><span class="sxs-lookup"><span data-stu-id="de866-188">**LabelFBBlue**</span></span>  
<span data-ttu-id="de866-189">COM 字串，其中包含與畫面格緩衝區的藍色色彩元件相關聯的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="de866-189">A COM string containing the name of the label associated with the blue color component of the framebuffer.</span></span>

<span data-ttu-id="de866-190">**LabelFBAlpha**</span><span class="sxs-lookup"><span data-stu-id="de866-190">**LabelFBAlpha**</span></span>  
<span data-ttu-id="de866-191">COM 字串，其中包含與畫面格緩衝區的 Alpha 色彩元件相關聯的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="de866-191">A COM string containing the name of the label associated with the alpha color component of the framebuffer.</span></span>

<span data-ttu-id="de866-192">**拓撲**</span><span class="sxs-lookup"><span data-stu-id="de866-192">**topology**</span></span>  
<span data-ttu-id="de866-193">繪製呼叫的頂點拓撲 (三角形清單、三角形區域等) 。</span><span class="sxs-lookup"><span data-stu-id="de866-193">The vertex topology of the draw calls (triangle list, triangle strip, etc).</span></span>

<span data-ttu-id="de866-194">**頂點**</span><span class="sxs-lookup"><span data-stu-id="de866-194">**vertices**</span></span>  
<span data-ttu-id="de866-195">COM 字串，包含從這個基本物件開始的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="de866-195">A COM string containing the vertex buffer starting at this primitive.</span></span> <span data-ttu-id="de866-196">頂點緩衝區會遵循管線階段中指定的輸入配置格式。</span><span class="sxs-lookup"><span data-stu-id="de866-196">The vertex buffer follows the input layout format specified in the pipeline stage.</span></span>

<span data-ttu-id="de866-197">**vertexSize**</span><span class="sxs-lookup"><span data-stu-id="de866-197">**vertexSize**</span></span>  
<span data-ttu-id="de866-198">單一頂點的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="de866-198">The size of a single vertex in bytes.</span></span>

<span data-ttu-id="de866-199">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="de866-199">**InputLayout**</span></span>  
<span data-ttu-id="de866-200">COM 字串，其中包含與繪製呼叫相關聯的 InputLayoutStruct 結構序列。</span><span class="sxs-lookup"><span data-stu-id="de866-200">A COM string containing a sequence of InputLayoutStruct structures associated with the draw call.</span></span>

<span data-ttu-id="de866-201">**HResult**</span><span class="sxs-lookup"><span data-stu-id="de866-201">**HResult**</span></span>  
<span data-ttu-id="de866-202">DirectX Hresult。</span><span class="sxs-lookup"><span data-stu-id="de866-202">The DirectX Hresult.</span></span> <span data-ttu-id="de866-203">發生問題時，這可以用來顯示錯誤。</span><span class="sxs-lookup"><span data-stu-id="de866-203">In the event of a problem this can be used to display the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="de866-204">規格需求</span><span class="sxs-lookup"><span data-stu-id="de866-204">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="de866-205">標頭</span><span class="sxs-lookup"><span data-stu-id="de866-205">Header</span></span></p></td><td><span data-ttu-id="de866-206">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="de866-206">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



