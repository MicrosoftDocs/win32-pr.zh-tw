---
title: 'ID3DX12PipelineParserCallbacks StreamOutputCb 方法 (D3DX12 .h) '
description: 呼叫物件的資料流程輸出描述子物件回呼，該物件會執行這個介面。
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- StreamOutputCb 方法
- StreamOutputCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，StreamOutputCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae32f084edd2b6af374aa9b1cac4e563ef8a2eb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998579"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a><span data-ttu-id="9ac1f-106">ID3DX12PipelineParserCallbacks：： StreamOutputCb 方法</span><span class="sxs-lookup"><span data-stu-id="9ac1f-106">ID3DX12PipelineParserCallbacks::StreamOutputCb method</span></span>

<span data-ttu-id="9ac1f-107">呼叫物件的資料流程輸出描述子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="9ac1f-107">Calls the stream output description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ac1f-108">語法</span><span class="sxs-lookup"><span data-stu-id="9ac1f-108">Syntax</span></span>


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a><span data-ttu-id="9ac1f-109">參數</span><span class="sxs-lookup"><span data-stu-id="9ac1f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ac1f-110">*>streamoutput* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="9ac1f-110">*StreamOutput* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac1f-111">Type： **Const [**D3D12 \_ 資料流程 \_ 輸出 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span><span class="sxs-lookup"><span data-stu-id="9ac1f-111">Type: **const [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span></span>

<span data-ttu-id="9ac1f-112">從管線狀態資料流程剖析之資料流程輸出描述子物件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9ac1f-112">Details of the stream output description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ac1f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ac1f-113">Return value</span></span>

<span data-ttu-id="9ac1f-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="9ac1f-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ac1f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ac1f-115">Requirements</span></span>



| <span data-ttu-id="9ac1f-116">需求</span><span class="sxs-lookup"><span data-stu-id="9ac1f-116">Requirement</span></span> | <span data-ttu-id="9ac1f-117">值</span><span class="sxs-lookup"><span data-stu-id="9ac1f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac1f-118">標頭</span><span class="sxs-lookup"><span data-stu-id="9ac1f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9ac1f-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="9ac1f-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="9ac1f-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="9ac1f-120">Library</span></span><br/> | <dl> <span data-ttu-id="9ac1f-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ac1f-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="9ac1f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9ac1f-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="9ac1f-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ac1f-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ac1f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ac1f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ac1f-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="9ac1f-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="9ac1f-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="9ac1f-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="9ac1f-127">**D3D12 \_ 資料流程 \_ 輸出 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9ac1f-127">**D3D12\_STREAM\_OUTPUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





