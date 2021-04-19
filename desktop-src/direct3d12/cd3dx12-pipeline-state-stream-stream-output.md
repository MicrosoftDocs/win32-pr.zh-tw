---
title: 'CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT 結構 (D3dx12 .h) '
description: 協助程式結構，用來將資料流程輸出描述當做適合資料流程描述的單一物件來描述。
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acc8f7bf059c4eee72b0b22abfc424ee82ffd2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986724"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a><span data-ttu-id="0d919-104">CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 資料流程 \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="0d919-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT structure</span></span>

<span data-ttu-id="0d919-105">協助程式結構，用來將資料流程輸出描述當做適合資料流程描述的單一物件來描述。</span><span class="sxs-lookup"><span data-stu-id="0d919-105">A helper structure used to describe the stream output description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d919-106">語法</span><span class="sxs-lookup"><span data-stu-id="0d919-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="0d919-107">成員</span><span class="sxs-lookup"><span data-stu-id="0d919-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0d919-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="0d919-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="0d919-109">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 資料流程 \_ 輸出的新、未初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="0d919-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT.</span></span>

</dd> <dt>

<span data-ttu-id="0d919-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 資料流程 \_ 輸出 (D3D12 \_ 資料流程 \_ 輸出 \_ DESC const &i)**</span><span class="sxs-lookup"><span data-stu-id="0d919-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT(D3D12\_STREAM\_OUTPUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="0d919-111">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程資料流程輸出的新實例 \_ \_ ，並使用 **D3D12 管線狀態子物件 \_ \_ \_ \_ 類型 \_ 資料流程 \_ 輸出** 和從 *i* 複製的子物件資料（ [**D3D12 \_ 資料流程 \_ 輸出 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) 結構）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="0d919-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_STREAM\_OUTPUT** and subobject data copied from *i*, a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0d919-112">**operator = (D3D12 \_ 資料流程 \_ 輸出 \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="0d919-112">**operator=(D3D12\_STREAM\_OUTPUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="0d919-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="0d919-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="0d919-114">**運算子 D3D12 \_ 資料流程 \_ 輸出 \_ DESC () 常數**</span><span class="sxs-lookup"><span data-stu-id="0d919-114">**operator D3D12\_STREAM\_OUTPUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="0d919-115">隱含轉換成 [**D3D12 \_ 資料流程 \_ 輸出 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="0d919-115">Implicit conversion to a [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d919-116">備註</span><span class="sxs-lookup"><span data-stu-id="0d919-116">Remarks</span></span>

<span data-ttu-id="0d919-117">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 資料流程 \_ 輸出是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="0d919-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
```



## <a name="requirements"></a><span data-ttu-id="0d919-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d919-118">Requirements</span></span>



| <span data-ttu-id="0d919-119">需求</span><span class="sxs-lookup"><span data-stu-id="0d919-119">Requirement</span></span> | <span data-ttu-id="0d919-120">值</span><span class="sxs-lookup"><span data-stu-id="0d919-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0d919-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0d919-121">Header</span></span><br/> | <dl> <span data-ttu-id="0d919-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d919-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d919-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d919-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d919-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="0d919-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="0d919-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="0d919-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="0d919-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="0d919-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

