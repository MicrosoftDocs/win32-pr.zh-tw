---
title: 'ID3DX12PipelineParserCallbacks DepthStencilStateCb 方法 (D3DX12 .h)  (DSV) '
description: 呼叫物件的深度樣板值格式物件回呼，該物件會執行這個介面。
ms.assetid: BDD3AB24-34C6-41C8-984D-78A45867BF24
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
ms.openlocfilehash: fd40b138c357c143deafffe01252b3c8b3e87cda
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106995129"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h-for-depth-stencil-value"></a><span data-ttu-id="df4a8-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb 方法 (D3DX12 .h) 取得深度樣板值</span><span class="sxs-lookup"><span data-stu-id="df4a8-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h) for depth stencil value</span></span>

<span data-ttu-id="df4a8-107">呼叫物件的深度樣板值格式物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="df4a8-107">Calls the depth stencil value format subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="df4a8-108">語法</span><span class="sxs-lookup"><span data-stu-id="df4a8-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="df4a8-109">參數</span><span class="sxs-lookup"><span data-stu-id="df4a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df4a8-110">*DepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="df4a8-110">*DepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="df4a8-111">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="df4a8-111">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="df4a8-112">從管線狀態資料流程剖析的深度樣板值格式子物件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="df4a8-112">Details of the depth stencil value format subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df4a8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="df4a8-113">Return value</span></span>

<span data-ttu-id="df4a8-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="df4a8-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="df4a8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="df4a8-115">Requirements</span></span>



| <span data-ttu-id="df4a8-116">需求</span><span class="sxs-lookup"><span data-stu-id="df4a8-116">Requirement</span></span> | <span data-ttu-id="df4a8-117">值</span><span class="sxs-lookup"><span data-stu-id="df4a8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="df4a8-118">標頭</span><span class="sxs-lookup"><span data-stu-id="df4a8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="df4a8-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="df4a8-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="df4a8-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="df4a8-120">Library</span></span><br/> | <dl> <span data-ttu-id="df4a8-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="df4a8-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="df4a8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="df4a8-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="df4a8-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df4a8-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df4a8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df4a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df4a8-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="df4a8-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="df4a8-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="df4a8-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="df4a8-127">**DXGI \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="df4a8-127">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

