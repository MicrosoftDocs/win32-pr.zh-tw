---
title: 'ID3DX12PipelineParserCallbacks PrimitiveTopologyTypeCb 方法 (D3DX12 .h) '
description: 呼叫基底拓撲類型物件的子物件回呼，該物件會執行這個介面。
ms.assetid: FF9D8D5C-3A6A-40D8-8EA4-3EA305EB4568
keywords:
- PrimitiveTopologyTypeCb 方法
- PrimitiveTopologyTypeCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，PrimitiveTopologyTypeCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PrimitiveTopologyTypeCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01a2d73edd6ac94719905757d75a756c905c832
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999973"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a><span data-ttu-id="7eedc-106">ID3DX12PipelineParserCallbacks：:P rimitiveTopologyTypeCb 方法</span><span class="sxs-lookup"><span data-stu-id="7eedc-106">ID3DX12PipelineParserCallbacks::PrimitiveTopologyTypeCb method</span></span>

<span data-ttu-id="7eedc-107">呼叫基底拓撲類型物件的子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="7eedc-107">Calls the primitive topology type subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eedc-108">語法</span><span class="sxs-lookup"><span data-stu-id="7eedc-108">Syntax</span></span>


```C++
void PrimitiveTopologyTypeCb(
   D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType
);
```



## <a name="parameters"></a><span data-ttu-id="7eedc-109">參數</span><span class="sxs-lookup"><span data-stu-id="7eedc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eedc-110">*PrimitiveTopologyType*</span><span class="sxs-lookup"><span data-stu-id="7eedc-110">*PrimitiveTopologyType*</span></span> 
</dt> <dd>

<span data-ttu-id="7eedc-111">類型： **[ **D3D12 \_ 基本 \_ 拓撲 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**</span><span class="sxs-lookup"><span data-stu-id="7eedc-111">Type: **[**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**</span></span>

<span data-ttu-id="7eedc-112">從管線狀態資料流程剖析之基本拓撲類型子物件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7eedc-112">Details of the primitive topology type subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eedc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7eedc-113">Return value</span></span>

<span data-ttu-id="7eedc-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="7eedc-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eedc-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7eedc-115">Requirements</span></span>



| <span data-ttu-id="7eedc-116">需求</span><span class="sxs-lookup"><span data-stu-id="7eedc-116">Requirement</span></span> | <span data-ttu-id="7eedc-117">值</span><span class="sxs-lookup"><span data-stu-id="7eedc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7eedc-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7eedc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7eedc-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="7eedc-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="7eedc-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="7eedc-120">Library</span></span><br/> | <dl> <span data-ttu-id="7eedc-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7eedc-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="7eedc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7eedc-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7eedc-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eedc-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eedc-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7eedc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eedc-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="7eedc-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="7eedc-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="7eedc-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="7eedc-127">**D3D12 \_ 基本 \_ 拓撲 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="7eedc-127">**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 





