---
title: 'ID3DX12PipelineParserCallbacks 介面 (D3DX12 .h) '
description: 表示 D3DX12parsePipelineStream helper 函式所使用之剖析器和錯誤回呼集合的介面。
ms.assetid: CBC04D17-2E19-4755-B1CB-FC42BF5083E5
keywords:
- ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，說明
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0061746da589c30e4745dfa3e4dc573f7b5d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986112"
---
# <a name="id3dx12pipelineparsercallbacks-interface"></a><span data-ttu-id="3ecc4-105">ID3DX12PipelineParserCallbacks 介面</span><span class="sxs-lookup"><span data-stu-id="3ecc4-105">ID3DX12PipelineParserCallbacks interface</span></span>

<span data-ttu-id="3ecc4-106">表示 [**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md) helper 函式所使用之剖析器和錯誤回呼集合的介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-106">An interface that represents a collection of parser and error callbacks used by the [**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md) helper function.</span></span>

-   [<span data-ttu-id="3ecc4-107">方法</span><span class="sxs-lookup"><span data-stu-id="3ecc4-107">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3ecc4-108">方法</span><span class="sxs-lookup"><span data-stu-id="3ecc4-108">Methods</span></span>

<span data-ttu-id="3ecc4-109">**ID3DX12PipelineParserCallbacks** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-109">The **ID3DX12PipelineParserCallbacks** interface has these methods.</span></span>



| <span data-ttu-id="3ecc4-110">方法</span><span class="sxs-lookup"><span data-stu-id="3ecc4-110">Method</span></span>                                                                                    | <span data-ttu-id="3ecc4-111">描述</span><span class="sxs-lookup"><span data-stu-id="3ecc4-111">Description</span></span>                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ecc4-112">**BlendStateCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-112">**BlendStateCb**</span></span>](id3dx12pipelineparsercallbacks-blendstatecb.md)                       | <span data-ttu-id="3ecc4-113">呼叫物件的 blend 狀態原因子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-113">Calls the blend state description subobject callback of an object that implements this interface.</span></span><br/>                                                                 |
| [<span data-ttu-id="3ecc4-114">**CachedPSOCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-114">**CachedPSOCb**</span></span>](id3dx12pipelineparsercallbacks-cachedpsocb.md)                         | <span data-ttu-id="3ecc4-115">呼叫 (管線狀態物件的快取 PSO，) 執行此介面之物件的子物件回呼。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-115">Calls the cached PSO (Pipeline State Object) subobject callback of an object that implements this interface.</span></span><br/>                                                      |
| [<span data-ttu-id="3ecc4-116">**CSCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-116">**CSCb**</span></span>](id3dx12pipelineparsercallbacks-cscb.md)                                       | <span data-ttu-id="3ecc4-117">呼叫物件的計算著色器子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-117">Calls the compute shader subobject callback of an object that implements this interface.</span></span><br/>                                                                          |
| [<span data-ttu-id="3ecc4-118">**DepthStencilState1Cb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-118">**DepthStencilState1Cb**</span></span>](id3dx12pipelineparsercallbacks-depthstencilstate1cb.md)       | <span data-ttu-id="3ecc4-119">呼叫物件的深度樣板狀態 ([**D3D12 深度樣板) \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) ，此物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-119">Calls the depth stencil state ([**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) subobject callback of an object that implements this interface.</span></span><br/> |
| [<span data-ttu-id="3ecc4-120">**DepthStencilStateCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-120">**DepthStencilStateCb**</span></span>](id3dx12pipelineparsercallbacks-dsvformatcb.md)                 | <span data-ttu-id="3ecc4-121">呼叫物件的深度樣板值格式物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-121">Calls the depth stencil value format subobject callback of an object that implements this interface.</span></span><br/>                                                              |
| [<span data-ttu-id="3ecc4-122">**DepthStencilStateCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-122">**DepthStencilStateCb**</span></span>](id3dx12pipelineparsercallbacks-depthstencilstatecb.md)         | <span data-ttu-id="3ecc4-123">呼叫物件的深度樣板狀態子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-123">Calls the depth stencil state subobject callback of an object that implements this interface.</span></span><br/>                                                                     |
| [<span data-ttu-id="3ecc4-124">**DSCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-124">**DSCb**</span></span>](id3dx12pipelineparsercallbacks-dscb.md)                                       | <span data-ttu-id="3ecc4-125">呼叫物件的網域著色器子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-125">Calls the domain shader subobject callback of an object that implements this interface.</span></span><br/>                                                                           |
| [<span data-ttu-id="3ecc4-126">**ErrorBadInputParameter**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-126">**ErrorBadInputParameter**</span></span>](id3dx12pipelineparsercallbacks-errorbadinputparameter.md)   | <span data-ttu-id="3ecc4-127">呼叫實此介面之物件的錯誤輸入參數錯誤回呼。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-127">Calls the bad input parameter error callback of an object that implements this interface.</span></span><br/>                                                                         |
| [<span data-ttu-id="3ecc4-128">**ErrorDuplicateSubobject**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-128">**ErrorDuplicateSubobject**</span></span>](id3dx12pipelineparsercallbacks-errorduplicatesubobject.md) | <span data-ttu-id="3ecc4-129">呼叫物件的重複子物件錯誤回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-129">Calls the duplicate subobject error callback of an object that implements this interface.</span></span><br/>                                                                         |
| [<span data-ttu-id="3ecc4-130">**ErrorUnknownSubobject**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-130">**ErrorUnknownSubobject**</span></span>](id3dx12pipelineparsercallbacks-errorunknownsubobject.md)     | <span data-ttu-id="3ecc4-131">呼叫物件的未知子物件錯誤回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-131">Calls the unknown subobject error callback of an object that implements this interface.</span></span><br/>                                                                           |
| [<span data-ttu-id="3ecc4-132">**FlagsCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-132">**FlagsCb**</span></span>](id3dx12pipelineparsercallbacks-flagscb.md)                                 | <span data-ttu-id="3ecc4-133">呼叫物件的旗標子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-133">Calls the flags subobject callback of an object that implements this interface.</span></span><br/>                                                                                   |
| [<span data-ttu-id="3ecc4-134">**GSCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-134">**GSCb**</span></span>](id3dx12pipelineparsercallbacks-gscb.md)                                       | <span data-ttu-id="3ecc4-135">呼叫物件的幾何著色器子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-135">Calls the geometry shader subobject callback of an object that implements this interface.</span></span><br/>                                                                         |
| [<span data-ttu-id="3ecc4-136">**HSCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-136">**HSCb**</span></span>](id3dx12pipelineparsercallbacks-hscb.md)                                       | <span data-ttu-id="3ecc4-137">呼叫物件的輪廓著色器子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-137">Calls the hull shader subobject callback of an object that implements this interface.</span></span><br/>                                                                             |
| [<span data-ttu-id="3ecc4-138">**IBStripCutValueCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-138">**IBStripCutValueCb**</span></span>](id3dx12pipelineparsercallbacks-ibstripcutvaluecb.md)             | <span data-ttu-id="3ecc4-139">呼叫物件的索引緩衝區帶剪值子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-139">Calls the index buffer strip-cut value subobject callback of an object that implements this interface.</span></span><br/>                                                            |
| [<span data-ttu-id="3ecc4-140">**InputLayoutCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-140">**InputLayoutCb**</span></span>](id3dx12pipelineparsercallbacks-inputlayoutcb.md)                     | <span data-ttu-id="3ecc4-141">呼叫物件的輸入版面配置子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-141">Calls the input layout subobject callback of an object that implements this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="3ecc4-142">**NodemaskCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-142">**NodemaskCb**</span></span>](id3dx12pipelineparsercallbacks-nodemaskcb.md)                           | <span data-ttu-id="3ecc4-143">呼叫物件的 nodemask 子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-143">Calls the nodemask subobject callback of an object that implements this interface.</span></span><br/>                                                                                |
| [<span data-ttu-id="3ecc4-144">**PrimitiveTopologyTypeCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-144">**PrimitiveTopologyTypeCb**</span></span>](id3dx12pipelineparsercallbacks-primitivetopologytypecb.md) | <span data-ttu-id="3ecc4-145">呼叫基底拓撲類型物件的子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-145">Calls the primitive topology type subobject callback of an object that implements this interface.</span></span><br/>                                                                 |
| [<span data-ttu-id="3ecc4-146">**PSCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-146">**PSCb**</span></span>](id3dx12pipelineparsercallbacks-pscb.md)                                       | <span data-ttu-id="3ecc4-147">呼叫物件的圖元著色器子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-147">Calls the pixel shader subobject callback of an object that implements this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="3ecc4-148">**RasterizerStateCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-148">**RasterizerStateCb**</span></span>](id3dx12pipelineparsercallbacks-rasterizerstatecb.md)             | <span data-ttu-id="3ecc4-149">呼叫執行此介面之物件的轉譯器狀態原因子物件回呼。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-149">Calls the rasterizer state description subobject callback of an object that implements this interface.</span></span><br/>                                                            |
| [<span data-ttu-id="3ecc4-150">**RootSignatureCB**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-150">**RootSignatureCB**</span></span>](id3dx12pipelineparsercallbacks-rootsignaturecb.md)                 | <span data-ttu-id="3ecc4-151">呼叫物件的根簽章子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-151">Calls the root signature subobject callback of an object that implements this interface.</span></span><br/>                                                                          |
| [<span data-ttu-id="3ecc4-152">**RTVFormatsCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-152">**RTVFormatsCb**</span></span>](id3dx12pipelineparsercallbacks-rtvformatscb.md)                       | <span data-ttu-id="3ecc4-153">呼叫物件的呈現目標格式陣列子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-153">Calls the render target format array subobject callback of an object that implements this interface.</span></span><br/>                                                              |
| [<span data-ttu-id="3ecc4-154">**SampleDescCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-154">**SampleDescCb**</span></span>](id3dx12pipelineparsercallbacks-sampledesccb.md)                       | <span data-ttu-id="3ecc4-155">呼叫物件的範例描述子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-155">Calls the sample description subobject callback of an object that implements this interface.</span></span><br/>                                                                      |
| [<span data-ttu-id="3ecc4-156">**SampleMaskCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-156">**SampleMaskCb**</span></span>](id3dx12pipelineparsercallbacks-samplemaskcb.md)                       | <span data-ttu-id="3ecc4-157">呼叫物件的範例遮罩子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-157">Calls the sample mask subobject callback of an object that implements this interface.</span></span><br/>                                                                             |
| [<span data-ttu-id="3ecc4-158">**StreamOutputCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-158">**StreamOutputCb**</span></span>](id3dx12pipelineparsercallbacks-streamoutputcb.md)                   | <span data-ttu-id="3ecc4-159">呼叫物件的資料流程輸出描述子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-159">Calls the stream output description subobject callback of an object that implements this interface.</span></span><br/>                                                               |
| [<span data-ttu-id="3ecc4-160">**VSCb**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-160">**VSCb**</span></span>](id3dx12pipelineparsercallbacks-vscb.md)                                       | <span data-ttu-id="3ecc4-161">呼叫物件的頂點著色器子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="3ecc4-161">Calls the vertex shader subobject callback of an object that implements this interface.</span></span><br/>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="3ecc4-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ecc4-162">Requirements</span></span>



| <span data-ttu-id="3ecc4-163">需求</span><span class="sxs-lookup"><span data-stu-id="3ecc4-163">Requirement</span></span> | <span data-ttu-id="3ecc4-164">值</span><span class="sxs-lookup"><span data-stu-id="3ecc4-164">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3ecc4-165">標頭</span><span class="sxs-lookup"><span data-stu-id="3ecc4-165">Header</span></span><br/>  | <dl> <span data-ttu-id="3ecc4-166"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ecc4-166"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="3ecc4-167">程式庫</span><span class="sxs-lookup"><span data-stu-id="3ecc4-167">Library</span></span><br/> | <dl> <span data-ttu-id="3ecc4-168"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ecc4-168"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="3ecc4-169">DLL</span><span class="sxs-lookup"><span data-stu-id="3ecc4-169">DLL</span></span><br/>     | <dl> <span data-ttu-id="3ecc4-170"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ecc4-170"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ecc4-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ecc4-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ecc4-172">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="3ecc4-172">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="3ecc4-173">**D3DX12parsePipelineStream**</span><span class="sxs-lookup"><span data-stu-id="3ecc4-173">**D3DX12parsePipelineStream**</span></span>](d3dx12parsepipelinestream.md)
</dt> </dl>

 

 





