---
title: 'ID3DX12PipelineParserCallbacks IBStripCutValueCb 方法 (D3DX12 .h) '
description: 呼叫物件的索引緩衝區帶剪值子物件回呼，該物件會執行這個介面。
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- IBStripCutValueCb 方法
- IBStripCutValueCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，IBStripCutValueCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79fca93e76f43b97ffc8e133594805214fe84cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992334"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a><span data-ttu-id="7d4db-106">ID3DX12PipelineParserCallbacks：： IBStripCutValueCb 方法</span><span class="sxs-lookup"><span data-stu-id="7d4db-106">ID3DX12PipelineParserCallbacks::IBStripCutValueCb method</span></span>

<span data-ttu-id="7d4db-107">呼叫物件的索引緩衝區帶剪值子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="7d4db-107">Calls the index buffer strip-cut value subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d4db-108">語法</span><span class="sxs-lookup"><span data-stu-id="7d4db-108">Syntax</span></span>


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a><span data-ttu-id="7d4db-109">參數</span><span class="sxs-lookup"><span data-stu-id="7d4db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d4db-110">*IBStripCutValue*</span><span class="sxs-lookup"><span data-stu-id="7d4db-110">*IBStripCutValue*</span></span> 
</dt> <dd>

<span data-ttu-id="7d4db-111">類型： **[ **D3D12 \_ 索引 \_ 緩衝區 \_ 帶 \_ 剪 \_ 值**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span><span class="sxs-lookup"><span data-stu-id="7d4db-111">Type: **[**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span></span>

<span data-ttu-id="7d4db-112">從管線狀態資料流程剖析的索引緩衝區區域/剪下值子物件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7d4db-112">Details of the index buffer strip-cut value subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d4db-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d4db-113">Return value</span></span>

<span data-ttu-id="7d4db-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="7d4db-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d4db-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d4db-115">Requirements</span></span>



| <span data-ttu-id="7d4db-116">需求</span><span class="sxs-lookup"><span data-stu-id="7d4db-116">Requirement</span></span> | <span data-ttu-id="7d4db-117">值</span><span class="sxs-lookup"><span data-stu-id="7d4db-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7d4db-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7d4db-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7d4db-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d4db-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="7d4db-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="7d4db-120">Library</span></span><br/> | <dl> <span data-ttu-id="7d4db-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d4db-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="7d4db-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7d4db-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7d4db-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d4db-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d4db-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d4db-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d4db-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="7d4db-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="7d4db-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="7d4db-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="7d4db-127">**D3D12 \_ 索引 \_ 緩衝區 \_ 帶 \_ 剪 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="7d4db-127">**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





