---
title: 'ID3DX12PipelineParserCallbacks NodemaskCb 方法 (D3DX12 .h) '
description: 呼叫物件的 nodemask 子物件回呼，該物件會執行這個介面。
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- NodemaskCb 方法
- NodemaskCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，NodemaskCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf1cc03f60259c395ca8c459ddd5a308e3dcd6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106995894"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a><span data-ttu-id="5283e-106">ID3DX12PipelineParserCallbacks：： NodemaskCb 方法</span><span class="sxs-lookup"><span data-stu-id="5283e-106">ID3DX12PipelineParserCallbacks::NodemaskCb method</span></span>

<span data-ttu-id="5283e-107">呼叫物件的 nodemask 子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="5283e-107">Calls the nodemask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5283e-108">語法</span><span class="sxs-lookup"><span data-stu-id="5283e-108">Syntax</span></span>


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a><span data-ttu-id="5283e-109">參數</span><span class="sxs-lookup"><span data-stu-id="5283e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5283e-110">*Nodemask*</span><span class="sxs-lookup"><span data-stu-id="5283e-110">*Nodemask*</span></span> 
</dt> <dd>

<span data-ttu-id="5283e-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="5283e-111">Type: **UINT**</span></span>

<span data-ttu-id="5283e-112">從管線狀態資料流程剖析的 nodemask 子物件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5283e-112">Details of the nodemask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5283e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5283e-113">Return value</span></span>

<span data-ttu-id="5283e-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="5283e-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5283e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5283e-115">Requirements</span></span>



| <span data-ttu-id="5283e-116">需求</span><span class="sxs-lookup"><span data-stu-id="5283e-116">Requirement</span></span> | <span data-ttu-id="5283e-117">值</span><span class="sxs-lookup"><span data-stu-id="5283e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5283e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="5283e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5283e-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="5283e-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="5283e-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="5283e-120">Library</span></span><br/> | <dl> <span data-ttu-id="5283e-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5283e-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="5283e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5283e-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5283e-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5283e-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5283e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5283e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5283e-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="5283e-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5283e-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="5283e-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





