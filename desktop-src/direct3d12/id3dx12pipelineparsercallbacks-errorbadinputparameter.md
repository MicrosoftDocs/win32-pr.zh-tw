---
title: 'ID3DX12PipelineParserCallbacks ErrorBadInputParameter 方法 (D3DX12 .h) '
description: 呼叫實此介面之物件的錯誤輸入參數錯誤回呼。
ms.assetid: CB1F9A77-B120-4D72-99D3-16594E668520
keywords:
- ErrorBadInputParameter 方法
- ErrorBadInputParameter 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，ErrorBadInputParameter 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorBadInputParameter
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5181e8d9fb83b7338adc3af5c0ce44aec1b447d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975696"
---
# <a name="id3dx12pipelineparsercallbackserrorbadinputparameter-method"></a><span data-ttu-id="e8a70-106">ID3DX12PipelineParserCallbacks：： ErrorBadInputParameter 方法</span><span class="sxs-lookup"><span data-stu-id="e8a70-106">ID3DX12PipelineParserCallbacks::ErrorBadInputParameter method</span></span>

<span data-ttu-id="e8a70-107">呼叫實此介面之物件的錯誤輸入參數錯誤回呼。</span><span class="sxs-lookup"><span data-stu-id="e8a70-107">Calls the bad input parameter error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a70-108">語法</span><span class="sxs-lookup"><span data-stu-id="e8a70-108">Syntax</span></span>


```C++
void ErrorBadInputParameter(
   
        UINT
           ParameterIndex
);
```



## <a name="parameters"></a><span data-ttu-id="e8a70-109">參數</span><span class="sxs-lookup"><span data-stu-id="e8a70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8a70-110">*ParameterIndex*</span><span class="sxs-lookup"><span data-stu-id="e8a70-110">*ParameterIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a70-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="e8a70-111">Type: **UINT**</span></span>

<span data-ttu-id="e8a70-112">包含不正確輸入之參數的位置。</span><span class="sxs-lookup"><span data-stu-id="e8a70-112">The position of the parameter that contains bad input.</span></span> <span data-ttu-id="e8a70-113">最左邊的參數位於位置1，而不是位置0。</span><span class="sxs-lookup"><span data-stu-id="e8a70-113">The left-most parameter is at position 1, not position 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8a70-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8a70-114">Return value</span></span>

<span data-ttu-id="e8a70-115">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="e8a70-115">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8a70-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8a70-116">Requirements</span></span>



| <span data-ttu-id="e8a70-117">需求</span><span class="sxs-lookup"><span data-stu-id="e8a70-117">Requirement</span></span> | <span data-ttu-id="e8a70-118">值</span><span class="sxs-lookup"><span data-stu-id="e8a70-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a70-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e8a70-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e8a70-120"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8a70-120"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="e8a70-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="e8a70-121">Library</span></span><br/> | <dl> <span data-ttu-id="e8a70-122"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8a70-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="e8a70-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e8a70-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="e8a70-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8a70-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8a70-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8a70-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a70-126">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="e8a70-126">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e8a70-127">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="e8a70-127">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





