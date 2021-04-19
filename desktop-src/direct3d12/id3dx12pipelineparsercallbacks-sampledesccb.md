---
title: 'ID3DX12PipelineParserCallbacks SampleDescCb 方法 (D3DX12 .h) '
description: 呼叫物件的範例描述子物件回呼，該物件會執行這個介面。
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- SampleDescCb 方法
- SampleDescCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，SampleDescCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0644837720dd8c81dc1c7577a1d6506ebdf61c24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988165"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a><span data-ttu-id="a6f89-106">ID3DX12PipelineParserCallbacks：： SampleDescCb 方法</span><span class="sxs-lookup"><span data-stu-id="a6f89-106">ID3DX12PipelineParserCallbacks::SampleDescCb method</span></span>

<span data-ttu-id="a6f89-107">呼叫物件的範例描述子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="a6f89-107">Calls the sample description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6f89-108">語法</span><span class="sxs-lookup"><span data-stu-id="a6f89-108">Syntax</span></span>


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a6f89-109">參數</span><span class="sxs-lookup"><span data-stu-id="a6f89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6f89-110">*SampleDesc* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="a6f89-110">*SampleDesc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f89-111">類型： **Const [**DXGI \_ 範例 \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span><span class="sxs-lookup"><span data-stu-id="a6f89-111">Type: **const [**DXGI\_SAMPLE\_DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span></span>

<span data-ttu-id="a6f89-112">從管線狀態資料流程剖析之範例說明子物件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a6f89-112">Details of the sample description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6f89-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6f89-113">Return value</span></span>

<span data-ttu-id="a6f89-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="a6f89-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6f89-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6f89-115">Requirements</span></span>



| <span data-ttu-id="a6f89-116">需求</span><span class="sxs-lookup"><span data-stu-id="a6f89-116">Requirement</span></span> | <span data-ttu-id="a6f89-117">值</span><span class="sxs-lookup"><span data-stu-id="a6f89-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f89-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a6f89-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a6f89-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6f89-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="a6f89-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="a6f89-120">Library</span></span><br/> | <dl> <span data-ttu-id="a6f89-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6f89-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="a6f89-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a6f89-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="a6f89-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6f89-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6f89-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6f89-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f89-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="a6f89-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="a6f89-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="a6f89-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="a6f89-127">**DXGI \_ 範例 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a6f89-127">**DXGI\_SAMPLE\_DESC**</span></span>](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

