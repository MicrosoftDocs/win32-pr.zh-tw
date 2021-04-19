---
title: 'ID3DX12PipelineParserCallbacks RootSignatureCb 方法 (D3DX12 .h) '
description: 呼叫物件的根簽章子物件回呼，該物件會執行這個介面。
ms.assetid: FD467001-41B1-4A73-8E54-12C6B5EEAC3E
keywords:
- RootSignatureCb 方法
- RootSignatureCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，RootSignatureCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RootSignatureCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78160ff1e61432a0711876934215ff15afb918de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986075"
---
# <a name="id3dx12pipelineparsercallbacksrootsignaturecb-method"></a><span data-ttu-id="89d04-106">ID3DX12PipelineParserCallbacks：： RootSignatureCb 方法</span><span class="sxs-lookup"><span data-stu-id="89d04-106">ID3DX12PipelineParserCallbacks::RootSignatureCb method</span></span>

<span data-ttu-id="89d04-107">呼叫物件的根簽章子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="89d04-107">Calls the root signature subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d04-108">語法</span><span class="sxs-lookup"><span data-stu-id="89d04-108">Syntax</span></span>


```C++
void RootSignatureCb(
   ID3D12RootSignature *RootSignature
);
```



## <a name="parameters"></a><span data-ttu-id="89d04-109">參數</span><span class="sxs-lookup"><span data-stu-id="89d04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89d04-110">*RootSignature*</span><span class="sxs-lookup"><span data-stu-id="89d04-110">*RootSignature*</span></span> 
</dt> <dd>

<span data-ttu-id="89d04-111">類型： **[ **ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***</span><span class="sxs-lookup"><span data-stu-id="89d04-111">Type: **[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***</span></span>

<span data-ttu-id="89d04-112">從管線狀態資料流程剖析之根簽章子物件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="89d04-112">Details of the root signature subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89d04-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="89d04-113">Return value</span></span>

<span data-ttu-id="89d04-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="89d04-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="89d04-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="89d04-115">Requirements</span></span>



| <span data-ttu-id="89d04-116">需求</span><span class="sxs-lookup"><span data-stu-id="89d04-116">Requirement</span></span> | <span data-ttu-id="89d04-117">值</span><span class="sxs-lookup"><span data-stu-id="89d04-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="89d04-118">標頭</span><span class="sxs-lookup"><span data-stu-id="89d04-118">Header</span></span><br/>  | <dl> <span data-ttu-id="89d04-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="89d04-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="89d04-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="89d04-120">Library</span></span><br/> | <dl> <span data-ttu-id="89d04-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="89d04-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="89d04-122">DLL</span><span class="sxs-lookup"><span data-stu-id="89d04-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="89d04-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89d04-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89d04-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89d04-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d04-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="89d04-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="89d04-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="89d04-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="89d04-127">**ID3D12RootSignature**</span><span class="sxs-lookup"><span data-stu-id="89d04-127">**ID3D12RootSignature**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> </dl>

 

