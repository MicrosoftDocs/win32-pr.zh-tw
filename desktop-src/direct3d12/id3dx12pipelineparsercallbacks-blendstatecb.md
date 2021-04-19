---
title: 'ID3DX12PipelineParserCallbacks BlendStateCb 方法 (D3DX12 .h) '
description: 呼叫物件的 blend 狀態原因子物件回呼，該物件會執行這個介面。
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- BlendStateCb 方法
- BlendStateCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，BlendStateCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 119733fbe82203a6e423fb0ef9b07d3ecff70619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989209"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a><span data-ttu-id="5478b-106">ID3DX12PipelineParserCallbacks：： BlendStateCb 方法</span><span class="sxs-lookup"><span data-stu-id="5478b-106">ID3DX12PipelineParserCallbacks::BlendStateCb method</span></span>

<span data-ttu-id="5478b-107">呼叫物件的 blend 狀態原因子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="5478b-107">Calls the blend state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5478b-108">語法</span><span class="sxs-lookup"><span data-stu-id="5478b-108">Syntax</span></span>


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a><span data-ttu-id="5478b-109">參數</span><span class="sxs-lookup"><span data-stu-id="5478b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5478b-110">*BlendState* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="5478b-110">*BlendState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5478b-111">Type： **Const [**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**</span><span class="sxs-lookup"><span data-stu-id="5478b-111">Type: **const [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**</span></span>

<span data-ttu-id="5478b-112">從管線狀態資料流程剖析的 blend 狀態原因子物件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5478b-112">Details of the blend state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5478b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5478b-113">Return value</span></span>

<span data-ttu-id="5478b-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="5478b-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5478b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5478b-115">Requirements</span></span>



| <span data-ttu-id="5478b-116">需求</span><span class="sxs-lookup"><span data-stu-id="5478b-116">Requirement</span></span> | <span data-ttu-id="5478b-117">值</span><span class="sxs-lookup"><span data-stu-id="5478b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5478b-118">標頭</span><span class="sxs-lookup"><span data-stu-id="5478b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5478b-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="5478b-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="5478b-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="5478b-120">Library</span></span><br/> | <dl> <span data-ttu-id="5478b-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5478b-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="5478b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5478b-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5478b-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5478b-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5478b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5478b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5478b-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="5478b-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5478b-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="5478b-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="5478b-127">**D3D12 \_ BLEND \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="5478b-127">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





