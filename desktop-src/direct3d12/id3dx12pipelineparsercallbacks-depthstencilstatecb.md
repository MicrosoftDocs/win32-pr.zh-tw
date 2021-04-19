---
title: 'ID3DX12PipelineParserCallbacks DepthStencilStateCb 方法 (D3DX12 .h) '
description: 呼叫物件的深度樣板狀態子物件回呼，該物件會執行這個介面。
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
keywords:
- DepthStencilStateCb 方法
- DepthStencilStateCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，DepthStencilStateCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 913dbddef0c509174d3600798a6e1380d6098808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988167"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a><span data-ttu-id="0d245-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb 方法 (D3DX12 .h) </span><span class="sxs-lookup"><span data-stu-id="0d245-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h)</span></span>

<span data-ttu-id="0d245-107">呼叫物件的深度樣板狀態子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="0d245-107">Calls the depth stencil state subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d245-108">語法</span><span class="sxs-lookup"><span data-stu-id="0d245-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="0d245-109">參數</span><span class="sxs-lookup"><span data-stu-id="0d245-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d245-110">*DepthStencilState* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="0d245-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0d245-111">類型：**常數 [**D3D12 \_ 深度 \_ 樣板 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span><span class="sxs-lookup"><span data-stu-id="0d245-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span></span>

<span data-ttu-id="0d245-112">從管線狀態資料流程剖析的深度樣板狀態子物件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0d245-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d245-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d245-113">Return value</span></span>

<span data-ttu-id="0d245-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="0d245-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d245-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d245-115">Requirements</span></span>



| <span data-ttu-id="0d245-116">需求</span><span class="sxs-lookup"><span data-stu-id="0d245-116">Requirement</span></span> | <span data-ttu-id="0d245-117">值</span><span class="sxs-lookup"><span data-stu-id="0d245-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0d245-118">標頭</span><span class="sxs-lookup"><span data-stu-id="0d245-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0d245-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d245-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="0d245-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="0d245-120">Library</span></span><br/> | <dl> <span data-ttu-id="0d245-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d245-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="0d245-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0d245-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d245-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d245-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d245-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d245-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d245-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="0d245-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="0d245-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="0d245-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="0d245-127">**D3D12 \_ 深度 \_ 樣板 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="0d245-127">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





