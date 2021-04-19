---
title: 'ID3DX12PipelineParserCallbacks PSCb 方法 (D3DX12 .h) '
description: 呼叫物件的圖元著色器子物件回呼，該物件會執行這個介面。
ms.assetid: 3397B018-C26A-426F-88BB-89013BACBEEA
keywords:
- PSCb 方法
- PSCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，PSCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c972702c215556b953797a6e332f8e86c480b094
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976458"
---
# <a name="id3dx12pipelineparsercallbackspscb-method"></a><span data-ttu-id="ec48c-106">ID3DX12PipelineParserCallbacks：:P SCb 方法</span><span class="sxs-lookup"><span data-stu-id="ec48c-106">ID3DX12PipelineParserCallbacks::PSCb method</span></span>

<span data-ttu-id="ec48c-107">呼叫物件的圖元著色器子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="ec48c-107">Calls the pixel shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec48c-108">語法</span><span class="sxs-lookup"><span data-stu-id="ec48c-108">Syntax</span></span>


```C++
void PSCb(
  [ref] const D3D12_SHADER_BYTECODE &PS
);
```



## <a name="parameters"></a><span data-ttu-id="ec48c-109">參數</span><span class="sxs-lookup"><span data-stu-id="ec48c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec48c-110">*PS* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="ec48c-110">*PS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ec48c-111">Type： **Const [**D3D12 \_ 著色器 \_ 位元組的位元組**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="ec48c-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="ec48c-112">從管線狀態資料流程剖析的圖元著色器子物件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ec48c-112">Details of the pixel shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec48c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec48c-113">Return value</span></span>

<span data-ttu-id="ec48c-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="ec48c-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec48c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec48c-115">Requirements</span></span>



| <span data-ttu-id="ec48c-116">需求</span><span class="sxs-lookup"><span data-stu-id="ec48c-116">Requirement</span></span> | <span data-ttu-id="ec48c-117">值</span><span class="sxs-lookup"><span data-stu-id="ec48c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ec48c-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ec48c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ec48c-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec48c-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="ec48c-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="ec48c-120">Library</span></span><br/> | <dl> <span data-ttu-id="ec48c-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec48c-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="ec48c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ec48c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="ec48c-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec48c-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec48c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec48c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec48c-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="ec48c-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="ec48c-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="ec48c-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="ec48c-127">**D3D12 \_ 著色器 \_ 位元組碼**</span><span class="sxs-lookup"><span data-stu-id="ec48c-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





