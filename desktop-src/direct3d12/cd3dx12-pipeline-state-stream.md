---
title: 'CD3DX12_PIPELINE_STATE_STREAM 結構 (D3dx12 .h) '
description: '協助程式結構，可透過合併介面建立及處理圖形和計算管線狀態。 請參閱 D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ desc 和 D3D12 \_ 計算 \_ 管線 \_ 狀態 \_ desc。 |CD3DX12_PIPELINE_STATE_STREAM 結構 (D3dx12 .h) '
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- CD3DX12_PIPELINE_STATE_STREAM 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d52b9090fa1d3870027bbe360164627472c039e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974838"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a><span data-ttu-id="5f6ba-106">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程結構</span><span class="sxs-lookup"><span data-stu-id="5f6ba-106">CD3DX12\_PIPELINE\_STATE\_STREAM structure</span></span>

<span data-ttu-id="5f6ba-107">協助程式結構，可透過合併介面建立及處理圖形和計算管線狀態。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="5f6ba-108">請參閱 [**D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) 和 [**D3D12 \_ 計算 \_ 管線 \_ 狀態 \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="5f6ba-109">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程支援 Windows 10 Creators Update 和更新版本，但不支援秋季建立者更新的新功能，例如 view 實例。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-109">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer but doesn't support new features of the Fall Creators update, such as view instancing.</span></span> <span data-ttu-id="5f6ba-110">若要支援秋季建立者更新的功能，請改用 [**CD3DX12 \_ 管線 \_ 狀態 \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) 。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-110">To support features of the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f6ba-111">語法</span><span class="sxs-lookup"><span data-stu-id="5f6ba-111">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM {
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM();
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
  D3D12_GRAPHICS_PIPELINE_STATE_DESC                  GraphicsDescV0();
  D3D12_COMPUTE_PIPELINE_STATE_DESC                   ComputeDescV0();
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS                 Flags;
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK             NodeMask;
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE        pRootSignature;
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT          InputLayout;
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE    IBStripCutValue;
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY    PrimitiveTopologyType;
  CD3DX12_PIPELINE_STATE_STREAM_VS                    VS;
  CD3DX12_PIPELINE_STATE_STREAM_GS                    GS;
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT         StreamOutput;
  CD3DX12_PIPELINE_STATE_STREAM_HS                    HS;
  CD3DX12_PIPELINE_STATE_STREAM_DS                    DS;
  CD3DX12_PIPELINE_STATE_STREAM_PS                    PS;
  CD3DX12_PIPELINE_STATE_STREAM_CS                    CS;
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC            BlendState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1        DepthStencilState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT  DSVFormat;
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER            RasterizerState;
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC           SampleDesc;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK           SampleMask;
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO            CachedPSO;
};
```



## <a name="members"></a><span data-ttu-id="5f6ba-112">成員</span><span class="sxs-lookup"><span data-stu-id="5f6ba-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="5f6ba-113">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 ()**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-113">**CD3DX12\_PIPELINE\_STATE\_STREAM()**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-114">建立 CD3DX12 \_ 管線狀態資料流程的新、未初始化的 \_ 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-114">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-115">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 (const D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ desc& desc)**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-115">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-116">建立 CD3DX12 \_ 管線狀態資料流程的新實例 \_ \_ ，並以從 **CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程** 結構複製的值進行初始化。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-116">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-117">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 (const D3D12 \_ 計算 \_ 管線 \_ 狀態 \_ desc& DESC)**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-117">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-118">建立 CD3DX12 \_ 管線狀態資料流程的新實例 \_ \_ ，並以從 **CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程** 結構複製的值進行初始化。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-118">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-119">**GraphicsDescV0 ()**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-119">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-120">以傳值方式將 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程物件的內容傳回為 D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ DESC 結構。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-120">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="5f6ba-121">請注意，D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ DESC 不包含 **CS** 成員，因此此值會在轉換時遺失。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-121">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-122">**ComputeDescV0 ()**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-122">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-123">以傳值方式將 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程物件的內容傳回為 D3D12 \_ 計算 \_ 管線 \_ 狀態 \_ DESC 結構。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-123">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="5f6ba-124">請注意， \_ D3D12 \_ 計算 \_ 管線狀態 \_ DESC 不包含 **InputLayout**、 **IBStripCutValue**、 **PrimitiveTopologyType**、 **VS**、 **GS**、 **>streamoutput**、 **HS**、 **DS**、 **PS**、 **BlendState**、 **DepthStencilState**、 **DSVFormat**、 **RasterizerState**、 **NumRootSignature**、 **RTVFormats**、SampleDesc 或 **SampleMask** 成員，因此這些值會在轉換時遺失。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-124">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-125">**旗標**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-125">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-126">描述管線狀態旗標，這些旗標可控制功能，例如「工具調試」。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-126">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-127">**NodeMask**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-127">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-128">描述管線狀態節點遮罩，用來識別在多個介面卡案例中，PSO 適用之裝置)  (實體介面卡的節點;遮罩中的每個位都對應至單一節點。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-128">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="5f6ba-129">若為單一介面卡案例，請將此值設定為0。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-129">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-130">**pRootSignature**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-130">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-131">描述根簽章。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-131">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-132">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-132">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-133">描述輸入組合語言階段的輸入緩衝區格式</span><span class="sxs-lookup"><span data-stu-id="5f6ba-133">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-134">**IBStripCutValue**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-134">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-135">描述輸入緩衝區的特殊索引值，這個值表示使用三角形區域間拓撲時，剪下的 (不連續) 。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-135">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-136">**PrimitiveTopologyType**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-136">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-137">描述基本拓撲及其順序。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-137">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-138">**與**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-138">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-139">描述頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-139">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-140">**GS**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-140">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-141">描述幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-141">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-142">**>streamoutput**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-142">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-143">描述串流輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-143">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-144">**房 協**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-144">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-145">描述輪廓著色器。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-145">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-146">**Ds**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-147">描述網域著色器。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-147">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-148">**Ps**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-148">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-149">描述圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-149">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-150">**CS**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-150">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-151">描述計算著色器。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-151">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-152">**BlendState**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-152">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-153">描述 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-153">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-154">**DepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-154">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-155">描述深度範本的狀態。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-155">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-156">**DSVFormat**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-156">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-157">描述深度樣板格式。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-157">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-158">**RasterizerState**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-158">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-159">描述轉譯器的狀態。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-159">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-160">**RTVFormats**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-160">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-161">描述呈現目標格式。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-161">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-162">**SampleDesc**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-162">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-163">描述範例計數和品質。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-163">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-164">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-164">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-165">描述搭配 blend 狀態使用的範例遮罩。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-165">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="5f6ba-166">**CachedPSO**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-166">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="5f6ba-167">描述快取的 PSO。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-167">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f6ba-168">備註</span><span class="sxs-lookup"><span data-stu-id="5f6ba-168">Remarks</span></span>

<span data-ttu-id="5f6ba-169">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程支援 Windows 10 Creators Update 和更新版本，但不支援在 Windows 10 中加入的子物件類型（例如針對 view 實例）。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-169">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer, but doesn not support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="5f6ba-170">若要支援在秋季建立者更新中新增的子物件類型，請改用 [**CD3DX12 \_ 管線 \_ 狀態 \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) 。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-170">To support subobject types added in the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

<span data-ttu-id="5f6ba-171">此結構的可存取成員變數是 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程子物件範本的 typedef，它會將 \_ 子物件類型標記和子物件資料結合成適合資料流程描述的單一物件。</span><span class="sxs-lookup"><span data-stu-id="5f6ba-171">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="5f6ba-172">這些 typedef 包括：</span><span class="sxs-lookup"><span data-stu-id="5f6ba-172">Those typedefs are:</span></span>

<span data-ttu-id="5f6ba-173"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="5f6ba-173"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5f6ba-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f6ba-174">Requirements</span></span>



| <span data-ttu-id="5f6ba-175">需求</span><span class="sxs-lookup"><span data-stu-id="5f6ba-175">Requirement</span></span> | <span data-ttu-id="5f6ba-176">值</span><span class="sxs-lookup"><span data-stu-id="5f6ba-176">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5f6ba-177">標頭</span><span class="sxs-lookup"><span data-stu-id="5f6ba-177">Header</span></span><br/> | <dl> <span data-ttu-id="5f6ba-178"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f6ba-178"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f6ba-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f6ba-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f6ba-180">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="5f6ba-180">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5f6ba-181">**CD3DX12 \_ 管線 \_ 狀態 \_ STREAM1**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-181">**CD3DX12\_PIPELINE\_STATE\_STREAM1**</span></span>](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[<span data-ttu-id="5f6ba-182">**D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-182">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="5f6ba-183">**D3D12 \_ 計算 \_ 管線 \_ 狀態 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="5f6ba-183">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





