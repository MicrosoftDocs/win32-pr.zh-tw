---
title: 'CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE 結構 (D3dx12 .h) '
description: 協助程式結構，用來將索引緩衝區區域剪下值描述為適合資料流程描述的單一物件。
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c14924828c924b3bbbca3bb1a5f822437ec4c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976461"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a><span data-ttu-id="da1d9-104">CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ IB \_ 帶 \_ 剪下 \_ 值結構</span><span class="sxs-lookup"><span data-stu-id="da1d9-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE structure</span></span>

<span data-ttu-id="da1d9-105">協助程式結構，用來將索引緩衝區區域剪下值描述為適合資料流程描述的單一物件。</span><span class="sxs-lookup"><span data-stu-id="da1d9-105">A helper structure used to describe the index buffer strip cut value as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="da1d9-106">語法</span><span class="sxs-lookup"><span data-stu-id="da1d9-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a><span data-ttu-id="da1d9-107">成員</span><span class="sxs-lookup"><span data-stu-id="da1d9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="da1d9-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ IB \_ 帶 \_ 剪 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="da1d9-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>
</dt> <dd>

<span data-ttu-id="da1d9-109">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ IB \_ 帶 \_ 剪 \_ 值的新、未初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="da1d9-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE.</span></span>

</dd> <dt>

<span data-ttu-id="da1d9-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ IB \_ 區域 \_ 剪下 \_ 值 (D3D12 \_ 索引 \_ 緩衝區 \_ 帶剪下 \_ \_ 值 const &i)**</span><span class="sxs-lookup"><span data-stu-id="da1d9-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="da1d9-111">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ IB 區域 \_ 剪下值的新 \_ 實例 \_ ，並以 **D3D12 管線狀態子物件類型的 \_ 管線狀態子物件 \_ \_ \_ 類型 \_ IB 區域剪下 \_ \_ \_ 值** 和子物件資料（ [**D3D12 \_ 索引 \_ 緩衝區 \_ 帶 \_ 剪 \_ 值**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)結構）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="da1d9-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_IB\_STRIP\_CUT\_VALUE** and subobject data copied from *i*, a [**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) structure.</span></span>

</dd> <dt>

<span data-ttu-id="da1d9-112">**operator = (D3D12 \_ 索引 \_ 緩衝區 \_ 帶 \_ 剪下 \_ 值 const& i)**</span><span class="sxs-lookup"><span data-stu-id="da1d9-112">**operator=(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="da1d9-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="da1d9-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="da1d9-114">**運算子 D3D12 \_ 索引 \_ 緩衝區 \_ 帶 \_ () 常數的剪下 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="da1d9-114">**operator D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE() const**</span></span>
</dt> <dd>

<span data-ttu-id="da1d9-115">隱含轉換成 [**D3D12 \_ 索引 \_ 緩衝區帶的剪下 \_ \_ \_ 值**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) 結構。</span><span class="sxs-lookup"><span data-stu-id="da1d9-115">Implicit conversion to a [**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da1d9-116">備註</span><span class="sxs-lookup"><span data-stu-id="da1d9-116">Remarks</span></span>

<span data-ttu-id="da1d9-117">CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ IB \_ 區域 \_ 剪下 \_ 值是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="da1d9-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
```



## <a name="requirements"></a><span data-ttu-id="da1d9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="da1d9-118">Requirements</span></span>



| <span data-ttu-id="da1d9-119">需求</span><span class="sxs-lookup"><span data-stu-id="da1d9-119">Requirement</span></span> | <span data-ttu-id="da1d9-120">值</span><span class="sxs-lookup"><span data-stu-id="da1d9-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="da1d9-121">標頭</span><span class="sxs-lookup"><span data-stu-id="da1d9-121">Header</span></span><br/> | <dl> <span data-ttu-id="da1d9-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="da1d9-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da1d9-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da1d9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da1d9-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="da1d9-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="da1d9-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="da1d9-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="da1d9-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="da1d9-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

