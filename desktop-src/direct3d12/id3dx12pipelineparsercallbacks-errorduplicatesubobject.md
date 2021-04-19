---
title: 'ID3DX12PipelineParserCallbacks ErrorDuplicateSubobject 方法 (D3DX12 .h) '
description: 呼叫物件的重複子物件錯誤回呼，該物件會執行這個介面。
ms.assetid: 625C72C4-7BFB-4DAD-8D39-EDDBC7189499
keywords:
- ErrorDuplicateSubobject 方法
- ErrorDuplicateSubobject 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，ErrorDuplicateSubobject 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorDuplicateSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b00dae4675ff05a43e566a8ead815ea24f6c16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992731"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a><span data-ttu-id="b8441-106">ID3DX12PipelineParserCallbacks：： ErrorDuplicateSubobject 方法</span><span class="sxs-lookup"><span data-stu-id="b8441-106">ID3DX12PipelineParserCallbacks::ErrorDuplicateSubobject method</span></span>

<span data-ttu-id="b8441-107">呼叫物件的重複子物件錯誤回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="b8441-107">Calls the duplicate subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8441-108">語法</span><span class="sxs-lookup"><span data-stu-id="b8441-108">Syntax</span></span>


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a><span data-ttu-id="b8441-109">參數</span><span class="sxs-lookup"><span data-stu-id="b8441-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8441-110">*DuplicateType*</span><span class="sxs-lookup"><span data-stu-id="b8441-110">*DuplicateType*</span></span> 
</dt> <dd>

<span data-ttu-id="b8441-111">類型： **[ **D3D12 \_ 管線 \_ 狀態 \_ \_** 子物件類型](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**</span><span class="sxs-lookup"><span data-stu-id="b8441-111">Type: **[**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**</span></span>

<span data-ttu-id="b8441-112">已複製的子物件類型。</span><span class="sxs-lookup"><span data-stu-id="b8441-112">The subobject type that was duplicated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8441-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8441-113">Return value</span></span>

<span data-ttu-id="b8441-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="b8441-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8441-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8441-115">Requirements</span></span>



| <span data-ttu-id="b8441-116">需求</span><span class="sxs-lookup"><span data-stu-id="b8441-116">Requirement</span></span> | <span data-ttu-id="b8441-117">值</span><span class="sxs-lookup"><span data-stu-id="b8441-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8441-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b8441-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b8441-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8441-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b8441-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="b8441-120">Library</span></span><br/> | <dl> <span data-ttu-id="b8441-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8441-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8441-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b8441-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="b8441-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8441-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8441-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8441-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8441-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="b8441-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b8441-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="b8441-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="b8441-127">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="b8441-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

