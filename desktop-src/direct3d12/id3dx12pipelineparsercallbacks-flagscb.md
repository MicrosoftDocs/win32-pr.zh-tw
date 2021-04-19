---
title: 'ID3DX12PipelineParserCallbacks FlagsCb 方法 (D3DX12 .h) '
description: 呼叫物件的旗標子物件回呼，該物件會執行這個介面。
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- FlagsCb 方法
- FlagsCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，FlagsCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30ac5a0ca3a749144e263a1d993166b8e13ddac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993895"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a><span data-ttu-id="dcbc6-106">ID3DX12PipelineParserCallbacks：： FlagsCb 方法</span><span class="sxs-lookup"><span data-stu-id="dcbc6-106">ID3DX12PipelineParserCallbacks::FlagsCb method</span></span>

<span data-ttu-id="dcbc6-107">呼叫物件的旗標子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="dcbc6-107">Calls the flags subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcbc6-108">語法</span><span class="sxs-lookup"><span data-stu-id="dcbc6-108">Syntax</span></span>


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="dcbc6-109">參數</span><span class="sxs-lookup"><span data-stu-id="dcbc6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcbc6-110">*旗標*</span><span class="sxs-lookup"><span data-stu-id="dcbc6-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="dcbc6-111">類型： **[ **D3D12 \_ 管線 \_ 狀態 \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span><span class="sxs-lookup"><span data-stu-id="dcbc6-111">Type: **[**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span></span>

<span data-ttu-id="dcbc6-112">從管線狀態資料流程剖析之旗標子物件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dcbc6-112">Details of the flags subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcbc6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="dcbc6-113">Return value</span></span>

<span data-ttu-id="dcbc6-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="dcbc6-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcbc6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcbc6-115">Requirements</span></span>



| <span data-ttu-id="dcbc6-116">需求</span><span class="sxs-lookup"><span data-stu-id="dcbc6-116">Requirement</span></span> | <span data-ttu-id="dcbc6-117">值</span><span class="sxs-lookup"><span data-stu-id="dcbc6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dcbc6-118">標頭</span><span class="sxs-lookup"><span data-stu-id="dcbc6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dcbc6-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="dcbc6-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="dcbc6-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="dcbc6-120">Library</span></span><br/> | <dl> <span data-ttu-id="dcbc6-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcbc6-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="dcbc6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="dcbc6-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="dcbc6-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcbc6-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcbc6-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dcbc6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcbc6-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="dcbc6-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="dcbc6-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="dcbc6-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="dcbc6-127">**D3D12 \_ 管線 \_ 狀態 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="dcbc6-127">**D3D12\_PIPELINE\_STATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





