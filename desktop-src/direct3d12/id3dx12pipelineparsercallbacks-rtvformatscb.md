---
title: 'ID3DX12PipelineParserCallbacks RTVFormatsCb 方法 (D3DX12 .h) '
description: 呼叫物件的呈現目標格式陣列子物件回呼，該物件會執行這個介面。
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- RTVFormatsCb 方法
- RTVFormatsCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，RTVFormatsCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caaa1df508e1a448de3851d408f9aad5ac94d957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976720"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a><span data-ttu-id="d1946-106">ID3DX12PipelineParserCallbacks：： RTVFormatsCb 方法</span><span class="sxs-lookup"><span data-stu-id="d1946-106">ID3DX12PipelineParserCallbacks::RTVFormatsCb method</span></span>

<span data-ttu-id="d1946-107">呼叫物件的呈現目標格式陣列子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="d1946-107">Calls the render target format array subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1946-108">語法</span><span class="sxs-lookup"><span data-stu-id="d1946-108">Syntax</span></span>


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a><span data-ttu-id="d1946-109">參數</span><span class="sxs-lookup"><span data-stu-id="d1946-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1946-110">*RTVFormats* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="d1946-110">*RTVFormats* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d1946-111">Type： **Const [**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span><span class="sxs-lookup"><span data-stu-id="d1946-111">Type: **const [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span></span>

<span data-ttu-id="d1946-112">從管線狀態資料流程剖析之轉譯目標格式陣列子物件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d1946-112">Details of the render target format array subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1946-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1946-113">Return value</span></span>

<span data-ttu-id="d1946-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="d1946-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1946-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1946-115">Requirements</span></span>



| <span data-ttu-id="d1946-116">需求</span><span class="sxs-lookup"><span data-stu-id="d1946-116">Requirement</span></span> | <span data-ttu-id="d1946-117">值</span><span class="sxs-lookup"><span data-stu-id="d1946-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d1946-118">標頭</span><span class="sxs-lookup"><span data-stu-id="d1946-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d1946-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1946-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d1946-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="d1946-120">Library</span></span><br/> | <dl> <span data-ttu-id="d1946-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1946-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d1946-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d1946-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d1946-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1946-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1946-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1946-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1946-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="d1946-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d1946-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="d1946-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="d1946-127">**D3D12 \_ RT \_ 格式 \_ 陣列**</span><span class="sxs-lookup"><span data-stu-id="d1946-127">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





