---
title: 'CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER 結構 (D3dx12 .h) '
description: '\_ \_ \_ 從傳遞至對應成員函式的物件詳細資料，建立內部 CD3DX12 管線狀態資料流程物件。 此結構會實 ID3DX12PipelineParserCallbacks 介面。'
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cc6228f690abd677e1adc8552293e440452ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985867"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a><span data-ttu-id="ab6f3-105">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 剖析協助程式 \_ 結構</span><span class="sxs-lookup"><span data-stu-id="ab6f3-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_PARSE\_HELPER structure</span></span>

<span data-ttu-id="ab6f3-106">\_ \_ \_ 從傳遞至對應成員函式的物件詳細資料，建立內部 CD3DX12 管線狀態資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-106">Builds an internal CD3DX12\_PIPELINE\_STATE\_STREAM object from subobject details passed into the corresponding member functions.</span></span> <span data-ttu-id="ab6f3-107">此結構會實 [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-107">This struct implements the [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab6f3-108">語法</span><span class="sxs-lookup"><span data-stu-id="ab6f3-108">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER  : public ID3DX12PipelineParserCallbacks{
  CD3DX12_PIPELINE_STATE_STREAM1 PipelineStream;
  void                           FlagsCb(D3D12_PIPELINE_STATE_FLAGS Flags);
  void                           NodeMaskCb(UINT NodeMask);
  void                           RootSignatureCb(ID3D12RootSignature* pRootSignature);
  void                           InputLayoutCb(const D3D12_INPUT_LAYOUT_DESC& InputLayout);
  void                           IBStripCutValueCb(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue);
  void                           PrimitiveTopologyTypeCb(D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType);
  void                           VSCb(const D3D12_SHADER_BYTECODE& VS);
  void                           GSCb(const D3D12_SHADER_BYTECODE& GS);
  void                           StreamOutputCb(const D3D12_STREAM_OUTPUT_DESC& StreamOutput);
  void                           HSCb(const D3D12_SHADER_BYTECODE& HS);
  void                           DSCb(const D3D12_SHADER_BYTECODE& DS);
  void                           PSCb(const D3D12_SHADER_BYTECODE& PS);
  void                           CSCb(const D3D12_SHADER_BYTECODE& CS);
  void                           BlendStateCb(const D3D12_BLEND_DESC& BlendState);
  void                           DepthStencilStateCb(const D3D12_DEPTH_STENCIL_DESC& DepthStencilState);
  void                           DepthStencilState1Cb(const D3D12_DEPTH_STENCIL_DESC1& DepthStencilState);
  void                           DSVFormatCb(DXGI_FORMAT DSVFormat);
  void                           RasterizerStateCb(const D3D12_RASTERIZER_DESC& RasterizerState);
  void                           RTVFormatsCb(const D3D12_RT_FORMAT_ARRAY& RTVFormats);
  void                           SampleDescCb(const DXGI_SAMPLE_DESC& SampleDesc);
  void                           SampleMaskCb(UINT SampleMask);
  void                           ViewInstancingCb(const D3D12_VIEW_INSTANCING_DESC& ViewInstancingDesc);
  void                           CachedPSOCb(const D3D12_CACHED_PIPELINE_STATE& CachedPSO);
  void                           ErrorBadInputParameter(UINT);
  void                           ErrorDuplicateSubobject(D3D12_PIPELINE_STATE_SUBOBJECT_TYPE);
  void                           ErrorUnknownSubobject(UINT);
};
```



## <a name="members"></a><span data-ttu-id="ab6f3-109">成員</span><span class="sxs-lookup"><span data-stu-id="ab6f3-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="ab6f3-110">**PipelineStream**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-110">**PipelineStream**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-111">內部 [**CD3DX12 \_ 管線 \_ 狀態 \_ STREAM1**](cd3dx12-pipeline-state-stream1.md)。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-111">The internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md).</span></span> <span data-ttu-id="ab6f3-112">其目前的狀態代表已在此物件上呼叫之回呼方法的累積效果。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-112">Its current state represents the cumulative effect of callback methods that have been called on this object.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-113">**FlagsCb (D3D12 \_ 管線 \_ 狀態 \_ 旗標旗標)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-113">**FlagsCb(D3D12\_PIPELINE\_STATE\_FLAGS Flags)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-114">使用 *flags* 參數的值，初始化 **PipelineStream** 的 **旗標** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-114">Initializes the **Flags** member of **PipelineStream** using the value of the *Flags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-115">**NodeMaskCb (UINT NodeMask)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-115">**NodeMaskCb(UINT NodeMask)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-116">使用 *NodeMask* 參數的值，初始化 **PipelineStream** 的 **NodeMask** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-116">Initializes the **NodeMask** member of **PipelineStream** using the value of the *Nodemask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-117">**RootSignatureCb (ID3D12RootSignature \* pRootSignature)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-117">**RootSignatureCb(ID3D12RootSignature\* pRootSignature)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-118">使用 *pRootSignature* 參數的值，初始化 **PipelineStream** 的 **pRootSignature** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-118">Initializes the **pRootSignature** member of **PipelineStream** using the value of the *pRootSignature* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-119">**InputLayoutCb (const D3D12 \_ 輸入 \_ 版面配置 \_ DESC& InputLayout)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-119">**InputLayoutCb(const D3D12\_INPUT\_LAYOUT\_DESC& InputLayout)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-120">使用 *InputLayout* 參數的值，初始化 **PipelineStream** 的 **InputLayout** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-120">Initializes the **InputLayout** member of **PipelineStream** using the value of the *InputLayout* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-121">**IBStripCutValueCb (D3D12 \_ 索引 \_ 緩衝區 \_ 帶 \_ 剪 \_ 值 IBStripCutValue)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-121">**IBStripCutValueCb(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE IBStripCutValue)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-122">使用 *IBStripCutValue* 參數的值，初始化 **PipelineStream** 的 **IBStripCutValue** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-122">Initializes the **IBStripCutValue** member of **PipelineStream** using the value of the *IBStripCutValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-123">**PrimitiveTopologyTypeCb (D3D12 \_ 基本 \_ 拓撲 \_ 類型 PrimitiveTopologyType)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-123">**PrimitiveTopologyTypeCb(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE PrimitiveTopologyType)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-124">使用 *PrimitiveTopologyType* 參數的值，初始化 **PipelineStream** 的 **PrimitiveTopologyType** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-124">Initializes the **PrimitiveTopologyType** member of **PipelineStream** using the value of the *PrimitiveTopologyType* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-125">**VSCb (const D3D12 \_ 著色器 \_ 位元組& VS)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-125">**VSCb(const D3D12\_SHADER\_BYTECODE& VS)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-126">使用 *vs* 參數的值，初始化 **vs** (頂點著色器) **PipelineStream** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-126">Initializes the **VS** (vertex shader) member of **PipelineStream** using the value of the *VS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-127">**GSCb (const D3D12 \_ 著色器 \_ 位元組& GS)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-127">**GSCb(const D3D12\_SHADER\_BYTECODE& GS)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-128">使用 *gs* 參數的值，初始化 **PipelineStream** 的) 成員的 **gs** (幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-128">Initializes the **GS** (geometry shader) member of **PipelineStream** using the value of the *GS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-129">**StreamOutputCb (const D3D12 \_ STREAM \_ OUTPUT \_ DESC& >streamoutput)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-129">**StreamOutputCb(const D3D12\_STREAM\_OUTPUT\_DESC& StreamOutput)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-130">使用 *>streamoutput* 參數的值，初始化 **PipelineStream** 的 **>streamoutput** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-130">Initializes the **StreamOutput** member of **PipelineStream** using the value of the *StreamOutput* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-131">**HSCb (const D3D12 \_ 著色器 \_ 位元組& HS)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-131">**HSCb(const D3D12\_SHADER\_BYTECODE& HS)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-132">使用 *hs* 參數的值，將 **hs** (輪廓著色器) 成員 **PipelineStream** 。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-132">Initializes the **HS** (hull shader) member of **PipelineStream** using the value of the *HS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-133">**DSCb (const D3D12 \_ 著色器 \_ 位元組& DS)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-133">**DSCb(const D3D12\_SHADER\_BYTECODE& DS)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-134">使用 *ds* 參數的值，初始化 **PipelineStream** 的 **ds** (網域著色器) 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-134">Initializes the **DS** (domain shader) member of **PipelineStream** using the value of the *DS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-135">**PSCb (const D3D12 \_ 著色器 \_ 位元組& PS)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-135">**PSCb(const D3D12\_SHADER\_BYTECODE& PS)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-136">使用 *ps* 參數的值，初始化 **PipelineStream** 的 **ps** (圖元著色器) 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-136">Initializes the **PS** (pixel shader) member of **PipelineStream** using the value of the *PS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-137">**CSCb (const D3D12 \_ 著色器 \_ 位元組& CS)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-137">**CSCb(const D3D12\_SHADER\_BYTECODE& CS)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-138">使用 *cs* 參數的值，初始化 **PipelineStream** 的 **cs** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-138">Initializes the **CS** member of **PipelineStream** using the value of the *CS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-139">**BlendStateCb (const D3D12 \_ BLEND \_ DESC& BlendState)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-139">**BlendStateCb(const D3D12\_BLEND\_DESC& BlendState)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-140">使用 *BlendState* 參數的值，初始化 **PipelineStream** 的 **BlendState** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-140">Initializes the **BlendState** member of **PipelineStream** using the value of the *BlendState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-141">**DepthStencilStateCb (const D3D12 \_ DEPTH \_ 樣板 \_ DESC& DepthStencilState)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-141">**DepthStencilStateCb(const D3D12\_DEPTH\_STENCIL\_DESC& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-142">使用 *DepthStencilState* 參數的值（ [**D3D12 \_ 深度樣板 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)），初始化 **PipelineStream** 的 **DepthStencilState** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-142">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-143">**DepthStencilState1Cb (const D3D12 \_ DEPTH \_ 樣板 \_ DESC1& DepthStencilState)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-143">**DepthStencilState1Cb(const D3D12\_DEPTH\_STENCIL\_DESC1& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-144">使用 *DepthStencilState* 參數的值（ [**D3D12 \_ 深度樣板 \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)），初始化 **PipelineStream** 的 **DepthStencilState** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-144">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-145">**DSVFormatCb (DXGI \_ FORMAT DSVFormat)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-145">**DSVFormatCb(DXGI\_FORMAT DSVFormat)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-146">使用 *DSVFormat* 參數的值，初始化 **PipelineStream** 的 **DSVFormat** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-146">Initializes the **DSVFormat** member of **PipelineStream** using the value of the *DSVFormat* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-147">**RasterizerStateCb (const D3D12 轉譯器 \_ \_ DESC& RasterizerState)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-147">**RasterizerStateCb(const D3D12\_RASTERIZER\_DESC& RasterizerState)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-148">使用 *RasterizerState* 參數的值，初始化 **PipelineStream** 的 **RasterizerState** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-148">Initializes the **RasterizerState** member of **PipelineStream** using the value of the *RasterizerState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-149">**RTVFormatsCb (const D3D12 \_ RT \_ 格式 \_ 陣列& RTVFormats)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-149">**RTVFormatsCb(const D3D12\_RT\_FORMAT\_ARRAY& RTVFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-150">使用 *RTVFormats* 參數的值，初始化 **PipelineStream** 的 **RTVFormats** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-150">Initializes the **RTVFormats** member of **PipelineStream** using the value of the *RTVFormats* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-151">**SampleDescCb (const DXGI \_ 範例 \_ DESC& SampleDesc)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-151">**SampleDescCb(const DXGI\_SAMPLE\_DESC& SampleDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-152">使用 *SampleDesc* 參數的值，初始化 **PipelineStream** 的 **SampleDesc** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-152">Initializes the **SampleDesc** member of **PipelineStream** using the value of the *SampleDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-153">**SampleMaskCb (UINT SampleMask)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-153">**SampleMaskCb(UINT SampleMask)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-154">使用 *SampleMask* 參數的值，初始化 **PipelineStream** 的 **SampleMask** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-154">Initializes the **SampleMask** member of **PipelineStream** using the value of the *SampleMask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-155">**ViewInstancingCb (const D3D12 \_ VIEW \_ 實例 \_ DESC& ViewInstancingDesc)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-155">**ViewInstancingCb(const D3D12\_VIEW\_INSTANCING\_DESC& ViewInstancingDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-156">使用 *ViewInstancingDesc* 參數的值，初始化 **PipelineStream** 的 **ViewInstancingDesc** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-156">Initializes the **ViewInstancingDesc** member of **PipelineStream** using the value of the *ViewInstancingDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-157">**CachedPSOCb (const D3D12 快取 \_ \_ 管線 \_ 狀態& CachedPSO)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-157">**CachedPSOCb(const D3D12\_CACHED\_PIPELINE\_STATE& CachedPSO)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-158">使用 *CachedPSO* 參數的值，初始化 **PipelineStream** 的 **CachedPSO** 成員。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-158">Initializes the **CachedPSO** member of **PipelineStream** using the value of the *CachedPSO* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-159">**ErrorBadInputParameter (UINT)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-159">**ErrorBadInputParameter(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-160">不執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-160">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-161">**ErrorDuplicateSubobject (D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-161">**ErrorDuplicateSubobject(D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-162">不執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-162">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-163">**ErrorUnknownSubobject (UINT)**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-163">**ErrorUnknownSubobject(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-164">不執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-164">Does nothing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab6f3-165">備註</span><span class="sxs-lookup"><span data-stu-id="ab6f3-165">Remarks</span></span>

<span data-ttu-id="ab6f3-166">以第二個參數形式傳遞至 [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md)函式時，會從做為第一個參數傳遞的 [**D3D12 \_ 管線 \_ 狀態 \_ 資料流程 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)複製內部 [**CD3DX12 \_ 管線 \_ 狀態 \_ STREAM1**](cd3dx12-pipeline-state-stream1.md)物件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-166">When passed as the second parameter to the [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) function, the details of the internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md) object are cloned from the [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passed as the first parameter.</span></span> <span data-ttu-id="ab6f3-167">此進程會驗證來來源資料流描述。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-167">This process validates the source stream description.</span></span> <span data-ttu-id="ab6f3-168">如果 D3DX12ParsePipelineStream 傳回 **S \_ OK**，則來來源資料流描述和產生的 **CD3DX12 \_ 管線 \_ 狀態 \_ STREAM1PipelineStream** 都是有效的，否則兩者都無效。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-168">If D3DX12ParsePipelineStream returns **S\_OK**, then both the source stream description and the resulting **CD3DX12\_PIPELINE\_STATE\_STREAM1PipelineStream** are valid; otherwise both are invalid.</span></span> <span data-ttu-id="ab6f3-169">不正確資料流程和其他錯誤只會透過 D3DX12ParsePipelineStream 的傳回值回報;此結構會執行錯誤回呼來執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="ab6f3-169">Invalid streams and other errors are reported only through the return value of D3DX12ParsePipelineStream; this structure implements the error callbacks to do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab6f3-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab6f3-170">Requirements</span></span>



| <span data-ttu-id="ab6f3-171">需求</span><span class="sxs-lookup"><span data-stu-id="ab6f3-171">Requirement</span></span> | <span data-ttu-id="ab6f3-172">值</span><span class="sxs-lookup"><span data-stu-id="ab6f3-172">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6f3-173">標頭</span><span class="sxs-lookup"><span data-stu-id="ab6f3-173">Header</span></span><br/> | <dl> <span data-ttu-id="ab6f3-174"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab6f3-174"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab6f3-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab6f3-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab6f3-176">Direct3D 12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="ab6f3-176">Helper Structures for Direct3D 12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="ab6f3-177">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-177">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





