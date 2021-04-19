---
title: 'ID3DX12PipelineParserCallbacks RasterizerStateCb 方法 (D3DX12 .h) '
description: 呼叫執行此介面之物件的轉譯器狀態原因子物件回呼。
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- RasterizerStateCb 方法
- RasterizerStateCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，RasterizerStateCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a970e8061ed9199ba5a6a334c7b670218e93936
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985896"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a><span data-ttu-id="7ddef-106">ID3DX12PipelineParserCallbacks：： RasterizerStateCb 方法</span><span class="sxs-lookup"><span data-stu-id="7ddef-106">ID3DX12PipelineParserCallbacks::RasterizerStateCb method</span></span>

<span data-ttu-id="7ddef-107">呼叫執行此介面之物件的轉譯器狀態原因子物件回呼。</span><span class="sxs-lookup"><span data-stu-id="7ddef-107">Calls the rasterizer state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ddef-108">語法</span><span class="sxs-lookup"><span data-stu-id="7ddef-108">Syntax</span></span>


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="7ddef-109">參數</span><span class="sxs-lookup"><span data-stu-id="7ddef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ddef-110">*RasterizerState* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="7ddef-110">*RasterizerState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7ddef-111">類型： **Const [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)** 轉譯器 DESC</span><span class="sxs-lookup"><span data-stu-id="7ddef-111">Type: **const [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span></span>

<span data-ttu-id="7ddef-112">從管線狀態資料流程剖析的轉譯器狀態原因子物件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7ddef-112">Details of the rasterizer state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ddef-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ddef-113">Return value</span></span>

<span data-ttu-id="7ddef-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="7ddef-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ddef-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ddef-115">Requirements</span></span>



| <span data-ttu-id="7ddef-116">需求</span><span class="sxs-lookup"><span data-stu-id="7ddef-116">Requirement</span></span> | <span data-ttu-id="7ddef-117">值</span><span class="sxs-lookup"><span data-stu-id="7ddef-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ddef-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7ddef-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7ddef-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ddef-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="7ddef-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="7ddef-120">Library</span></span><br/> | <dl> <span data-ttu-id="7ddef-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ddef-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="7ddef-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7ddef-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7ddef-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ddef-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ddef-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ddef-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ddef-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="7ddef-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="7ddef-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="7ddef-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="7ddef-127">**D3D12 轉譯器 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="7ddef-127">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





