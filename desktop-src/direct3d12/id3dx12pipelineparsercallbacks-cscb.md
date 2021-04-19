---
title: 'ID3DX12PipelineParserCallbacks CSCb 方法 (D3DX12 .h) '
description: 呼叫物件的計算著色器子物件回呼，該物件會執行這個介面。
ms.assetid: DE1ABA3D-D372-4D7F-9DB6-4E3360EAFAC2
keywords:
- CSCb 方法
- CSCb 方法，ID3DX12PipelineParserCallbacks 介面
- ID3DX12PipelineParserCallbacks 介面，CSCb 方法
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27dcf175d153211e06864cb73139b03f868d15db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992732"
---
# <a name="id3dx12pipelineparsercallbackscscb-method"></a><span data-ttu-id="dda44-106">ID3DX12PipelineParserCallbacks：： CSCb 方法</span><span class="sxs-lookup"><span data-stu-id="dda44-106">ID3DX12PipelineParserCallbacks::CSCb method</span></span>

<span data-ttu-id="dda44-107">呼叫物件的計算著色器子物件回呼，該物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="dda44-107">Calls the compute shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="dda44-108">語法</span><span class="sxs-lookup"><span data-stu-id="dda44-108">Syntax</span></span>


```C++
void CSCb(
  [ref] const D3D12_SHADER_BYTECODE &CS
);
```



## <a name="parameters"></a><span data-ttu-id="dda44-109">參數</span><span class="sxs-lookup"><span data-stu-id="dda44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dda44-110">*CS* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="dda44-110">*CS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="dda44-111">Type： **Const [**D3D12 \_ 著色器 \_ 位元組的位元組**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="dda44-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="dda44-112">從管線狀態資料流程剖析的計算著色器子物件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dda44-112">Details of the compute shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dda44-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="dda44-113">Return value</span></span>

<span data-ttu-id="dda44-114">不傳回任何專案。</span><span class="sxs-lookup"><span data-stu-id="dda44-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="dda44-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="dda44-115">Requirements</span></span>



| <span data-ttu-id="dda44-116">需求</span><span class="sxs-lookup"><span data-stu-id="dda44-116">Requirement</span></span> | <span data-ttu-id="dda44-117">值</span><span class="sxs-lookup"><span data-stu-id="dda44-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dda44-118">標頭</span><span class="sxs-lookup"><span data-stu-id="dda44-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dda44-119"><dt>D3DX12。h</dt></span><span class="sxs-lookup"><span data-stu-id="dda44-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="dda44-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="dda44-120">Library</span></span><br/> | <dl> <span data-ttu-id="dda44-121"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dda44-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="dda44-122">DLL</span><span class="sxs-lookup"><span data-stu-id="dda44-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="dda44-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dda44-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dda44-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dda44-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda44-125">Direct3D 12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="dda44-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="dda44-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="dda44-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="dda44-127">**D3D12 \_ 著色器 \_ 位元組碼**</span><span class="sxs-lookup"><span data-stu-id="dda44-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





