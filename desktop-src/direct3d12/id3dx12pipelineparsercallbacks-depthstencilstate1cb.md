---
title: 'ID3DX12PipelineParserCallbacks DepthStencilState1Cb 方法 (D3DX12 .h) '
description: 呼叫物件的深度樣板狀態 (D3D12 \_ 深度樣板 \_ \_) DESC1，此物件會執行這個介面。
ms.assetid: C1AE06E5-B1FF-44C2-9C56-1540B97AD883
keywords:
- DepthStencilState1Cb 方法
- DepthStencilState1Cb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，DepthStencilState1Cb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilState1Cb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a42cf85f60dcf27a5751f77a346931bfad6b03e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988166"
---
# <a name="id3dx12pipelineparsercallbacksdepthstencilstate1cb-method"></a><span data-ttu-id="6982d-106">ID3DX12PipelineParserCallbacks：:D epthStencilState1Cb 方法</span><span class="sxs-lookup"><span data-stu-id="6982d-106">ID3DX12PipelineParserCallbacks::DepthStencilState1Cb method</span></span>

<span data-ttu-id="6982d-107">呼叫物件的深度樣板狀態 ([**D3D12 深度樣板) \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) ，此物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="6982d-107">Calls the depth stencil state ([**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6982d-108">語法</span><span class="sxs-lookup"><span data-stu-id="6982d-108">Syntax</span></span>


```C++
void DepthStencilState1Cb(
  [ref] const D3D12_DEPTH_STENCIL_DESC1 &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="6982d-109">參數</span><span class="sxs-lookup"><span data-stu-id="6982d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6982d-110">*DepthStencilState* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="6982d-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6982d-111">Type： **Const [**D3D12 \_ DEPTH \_ 樣板 \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**</span><span class="sxs-lookup"><span data-stu-id="6982d-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**</span></span>

<span data-ttu-id="6982d-112">從管線狀態資料流程剖析的深度樣板狀態子物件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6982d-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6982d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6982d-113">Return value</span></span>

<span data-ttu-id="6982d-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="6982d-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6982d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6982d-115">Requirements</span></span>



| <span data-ttu-id="6982d-116">需求</span><span class="sxs-lookup"><span data-stu-id="6982d-116">Requirement</span></span> | <span data-ttu-id="6982d-117">值</span><span class="sxs-lookup"><span data-stu-id="6982d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6982d-118">標頭</span><span class="sxs-lookup"><span data-stu-id="6982d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6982d-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="6982d-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="6982d-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="6982d-120">Library</span></span><br/> | <dl> <span data-ttu-id="6982d-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6982d-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="6982d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6982d-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6982d-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6982d-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6982d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6982d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6982d-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="6982d-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="6982d-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="6982d-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="6982d-127">**D3D12 \_ 深度 \_ 樣板 \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="6982d-127">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> </dl>

 

 





