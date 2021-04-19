---
title: 'ID3DX12PipelineParserCallbacks ErrorUnknownSubobject 方法 (D3DX12 .h) '
description: 呼叫物件的未知子物件錯誤回呼，該物件會執行這個介面。
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- ErrorUnknownSubobject 方法
- ErrorUnknownSubobject 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，ErrorUnknownSubobject 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e294e3face085c5298f3cc624d7c0ef70dcf865
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988203"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a><span data-ttu-id="ff9eb-106">ID3DX12PipelineParserCallbacks：： ErrorUnknownSubobject 方法</span><span class="sxs-lookup"><span data-stu-id="ff9eb-106">ID3DX12PipelineParserCallbacks::ErrorUnknownSubobject method</span></span>

<span data-ttu-id="ff9eb-107">呼叫物件的未知子物件錯誤回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="ff9eb-107">Calls the unknown subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff9eb-108">語法</span><span class="sxs-lookup"><span data-stu-id="ff9eb-108">Syntax</span></span>


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a><span data-ttu-id="ff9eb-109">參數</span><span class="sxs-lookup"><span data-stu-id="ff9eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff9eb-110">*UnknownTypeValue*</span><span class="sxs-lookup"><span data-stu-id="ff9eb-110">*UnknownTypeValue*</span></span> 
</dt> <dd>

<span data-ttu-id="ff9eb-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="ff9eb-111">Type: **UINT**</span></span>

<span data-ttu-id="ff9eb-112">所嘗試子物件的無法辨識的子物件類型。</span><span class="sxs-lookup"><span data-stu-id="ff9eb-112">The unrecognized subobject type of the attempted subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff9eb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff9eb-113">Return value</span></span>

<span data-ttu-id="ff9eb-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="ff9eb-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff9eb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff9eb-115">Requirements</span></span>



| <span data-ttu-id="ff9eb-116">需求</span><span class="sxs-lookup"><span data-stu-id="ff9eb-116">Requirement</span></span> | <span data-ttu-id="ff9eb-117">值</span><span class="sxs-lookup"><span data-stu-id="ff9eb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff9eb-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ff9eb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ff9eb-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff9eb-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="ff9eb-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="ff9eb-120">Library</span></span><br/> | <dl> <span data-ttu-id="ff9eb-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff9eb-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="ff9eb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ff9eb-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="ff9eb-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff9eb-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff9eb-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff9eb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff9eb-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="ff9eb-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="ff9eb-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="ff9eb-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





