---
title: 'ID3DX12PipelineParserCallbacks SampleMaskCb 方法 (D3DX12 .h) '
description: 呼叫物件的範例遮罩子物件回呼，該物件會執行這個介面。
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- SampleMaskCb 方法
- SampleMaskCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，SampleMaskCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0124b228056089e21c078ffce25ce59eef0e3dee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992527"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a><span data-ttu-id="f7a21-106">ID3DX12PipelineParserCallbacks：： SampleMaskCb 方法</span><span class="sxs-lookup"><span data-stu-id="f7a21-106">ID3DX12PipelineParserCallbacks::SampleMaskCb method</span></span>

<span data-ttu-id="f7a21-107">呼叫物件的範例遮罩子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="f7a21-107">Calls the sample mask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a21-108">語法</span><span class="sxs-lookup"><span data-stu-id="f7a21-108">Syntax</span></span>


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a><span data-ttu-id="f7a21-109">參數</span><span class="sxs-lookup"><span data-stu-id="f7a21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7a21-110">*SampleMask*</span><span class="sxs-lookup"><span data-stu-id="f7a21-110">*SampleMask*</span></span> 
</dt> <dd>

<span data-ttu-id="f7a21-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="f7a21-111">Type: **UINT**</span></span>

<span data-ttu-id="f7a21-112">從管線狀態資料流程剖析的範例遮罩子物件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f7a21-112">Details of the sample mask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7a21-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7a21-113">Return value</span></span>

<span data-ttu-id="f7a21-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="f7a21-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7a21-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7a21-115">Requirements</span></span>



| <span data-ttu-id="f7a21-116">需求</span><span class="sxs-lookup"><span data-stu-id="f7a21-116">Requirement</span></span> | <span data-ttu-id="f7a21-117">值</span><span class="sxs-lookup"><span data-stu-id="f7a21-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a21-118">標頭</span><span class="sxs-lookup"><span data-stu-id="f7a21-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f7a21-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7a21-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="f7a21-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="f7a21-120">Library</span></span><br/> | <dl> <span data-ttu-id="f7a21-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7a21-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="f7a21-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f7a21-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="f7a21-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7a21-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7a21-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7a21-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7a21-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="f7a21-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f7a21-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="f7a21-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





