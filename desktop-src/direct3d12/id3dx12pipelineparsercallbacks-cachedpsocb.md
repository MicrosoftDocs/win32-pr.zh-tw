---
title: 'ID3DX12PipelineParserCallbacks CachedPSOCb 方法 (D3DX12 .h) '
description: 呼叫 (管線狀態物件的快取 PSO，) 執行此介面之物件的子物件回呼。
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- CachedPSOCb 方法
- CachedPSOCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，CachedPSOCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c168635a66eff012768a1eabbc803c6986a2c43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998213"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a><span data-ttu-id="73fd5-106">ID3DX12PipelineParserCallbacks：： CachedPSOCb 方法</span><span class="sxs-lookup"><span data-stu-id="73fd5-106">ID3DX12PipelineParserCallbacks::CachedPSOCb method</span></span>

<span data-ttu-id="73fd5-107">呼叫 (管線狀態物件的快取 PSO，) 執行此介面之物件的子物件回呼。</span><span class="sxs-lookup"><span data-stu-id="73fd5-107">Calls the cached PSO (Pipeline State Object) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="73fd5-108">語法</span><span class="sxs-lookup"><span data-stu-id="73fd5-108">Syntax</span></span>


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a><span data-ttu-id="73fd5-109">參數</span><span class="sxs-lookup"><span data-stu-id="73fd5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73fd5-110">*CachedPSO* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="73fd5-110">*CachedPSO* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="73fd5-111">類型： **Const D3D12 快取的 [**\_ \_ 管線 \_ 狀態**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span><span class="sxs-lookup"><span data-stu-id="73fd5-111">Type: **const [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span></span>

<span data-ttu-id="73fd5-112">快取的 PSO (管線狀態物件的詳細資料，) 從管線狀態資料流程剖析的子物件。</span><span class="sxs-lookup"><span data-stu-id="73fd5-112">Details of the cached PSO (Pipeline State Object) subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73fd5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="73fd5-113">Return value</span></span>

<span data-ttu-id="73fd5-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="73fd5-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="73fd5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="73fd5-115">Requirements</span></span>



| <span data-ttu-id="73fd5-116">需求</span><span class="sxs-lookup"><span data-stu-id="73fd5-116">Requirement</span></span> | <span data-ttu-id="73fd5-117">值</span><span class="sxs-lookup"><span data-stu-id="73fd5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="73fd5-118">標頭</span><span class="sxs-lookup"><span data-stu-id="73fd5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="73fd5-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="73fd5-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="73fd5-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="73fd5-120">Library</span></span><br/> | <dl> <span data-ttu-id="73fd5-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="73fd5-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="73fd5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="73fd5-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="73fd5-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73fd5-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73fd5-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73fd5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73fd5-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="73fd5-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="73fd5-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="73fd5-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="73fd5-127">**D3D12 快取的 \_ \_ 管線 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="73fd5-127">**D3D12\_CACHED\_PIPELINE\_STATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





