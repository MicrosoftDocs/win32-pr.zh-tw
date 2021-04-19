---
title: 'D3DX12ParsePipelineStream 函式 (D3dx12) '
description: 剖析管線狀態資料流程描述，針對每個已剖析的子物件實例呼叫使用者定義的回呼。
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- D3DX12ParsePipelineStream 函式
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997613"
---
# <a name="d3dx12parsepipelinestream-function"></a><span data-ttu-id="3b5e6-104">D3DX12ParsePipelineStream 函式</span><span class="sxs-lookup"><span data-stu-id="3b5e6-104">D3DX12ParsePipelineStream function</span></span>

<span data-ttu-id="3b5e6-105">剖析管線狀態資料流程描述，針對每個已剖析的子物件實例呼叫使用者定義的回呼。</span><span class="sxs-lookup"><span data-stu-id="3b5e6-105">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b5e6-106">語法</span><span class="sxs-lookup"><span data-stu-id="3b5e6-106">Syntax</span></span>


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a><span data-ttu-id="3b5e6-107">參數</span><span class="sxs-lookup"><span data-stu-id="3b5e6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b5e6-108">*Desc* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="3b5e6-108">*Desc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3b5e6-109">類型： **Const [**D3D12 \_ 管線 \_ 狀態 \_ 資料流程 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span><span class="sxs-lookup"><span data-stu-id="3b5e6-109">Type: **const [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span></span>

<span data-ttu-id="3b5e6-110">要剖析的管線狀態資料流程描述。</span><span class="sxs-lookup"><span data-stu-id="3b5e6-110">The pipeline state stream description to parse.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e6-111">*pCallbacks*</span><span class="sxs-lookup"><span data-stu-id="3b5e6-111">*pCallbacks*</span></span> 
</dt> <dd>

<span data-ttu-id="3b5e6-112">類型： **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b5e6-112">Type: **[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span></span>

<span data-ttu-id="3b5e6-113">結構，指定要針對每個子物件類型呼叫的回呼，以及在發生剖析錯誤時呼叫的其他回呼。</span><span class="sxs-lookup"><span data-stu-id="3b5e6-113">A structure that specifies the callbacks to call for each subobject type and additional callbacks to call in the event of a parsing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b5e6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b5e6-114">Return value</span></span>

<span data-ttu-id="3b5e6-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b5e6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b5e6-116">如果遇到不明的子物件類型，這個方法會傳回 HRESULT 成功 (**S \_ OK** 或 **E \_ INVALIDARG** 錯誤，如果資料流程描述是空的、null 或包含重複的子物件 (包括衍生子物件) 或 *pCallbacks* 為 null。</span><span class="sxs-lookup"><span data-stu-id="3b5e6-116">This method returns an HRESULT success (**S\_OK** or **E\_INVALIDARG** error if an unknown subobject type is encountered, if the stream description is empty, null, or contains duplicate subobjects (including derived subobjects), or if *pCallbacks* is null.</span></span> <span data-ttu-id="3b5e6-117">在傳回電子 INVALIDARG 的每個案例中 \_ ，會先呼叫相對應的回呼。</span><span class="sxs-lookup"><span data-stu-id="3b5e6-117">In each case that E\_INVALIDARG is returned, a corresponding callback is first called.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b5e6-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b5e6-118">Requirements</span></span>



| <span data-ttu-id="3b5e6-119">需求</span><span class="sxs-lookup"><span data-stu-id="3b5e6-119">Requirement</span></span> | <span data-ttu-id="3b5e6-120">值</span><span class="sxs-lookup"><span data-stu-id="3b5e6-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3b5e6-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3b5e6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3b5e6-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b5e6-122"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="3b5e6-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="3b5e6-123">Library</span></span><br/> | <dl> <span data-ttu-id="3b5e6-124"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b5e6-124"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="3b5e6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3b5e6-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3b5e6-126"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b5e6-126"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b5e6-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b5e6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b5e6-128">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="3b5e6-128">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





