---
title: 'CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK 結構 (D3dx12 .h) '
description: 用來將範例遮罩描述為適用于資料流程描述之單一物件的 helper 結構。
ms.assetid: 20116DA1-F56D-42CA-A846-42509FAF88C1
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a498bec1bbf8c4f55f320765272d04cbdd81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992539"
---
# <a name="cd3dx12_pipeline_state_stream_sample_mask-structure"></a><span data-ttu-id="2464e-104">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ 遮罩結構</span><span class="sxs-lookup"><span data-stu-id="2464e-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK structure</span></span>

<span data-ttu-id="2464e-105">用來將範例遮罩描述為適用于資料流程描述之單一物件的 helper 結構。</span><span class="sxs-lookup"><span data-stu-id="2464e-105">A helper structure used to describe a sample mask as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="2464e-106">語法</span><span class="sxs-lookup"><span data-stu-id="2464e-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK operator=(UINT const& i);
                                            operator UINT() const;
};
```



## <a name="members"></a><span data-ttu-id="2464e-107">成員</span><span class="sxs-lookup"><span data-stu-id="2464e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2464e-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="2464e-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK**</span></span>
</dt> <dd>

<span data-ttu-id="2464e-109">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ 遮罩的新、未初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="2464e-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK.</span></span>

</dd> <dt>

<span data-ttu-id="2464e-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ 遮罩 (UINT const &i)**</span><span class="sxs-lookup"><span data-stu-id="2464e-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK(UINT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="2464e-111">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程範例遮罩的新實例 \_ \_ ，並使用 **D3D12 管線狀態子物件 \_ \_ \_ \_ 類型 \_ 範例 \_ 遮罩** 的子物件類型和從 *i* 複製的子物件資料（ **UINT** 範例遮罩）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="2464e-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_SAMPLE\_MASK** and subobject data copied from *i*, a **UINT** sample mask.</span></span>

</dd> <dt>

<span data-ttu-id="2464e-112">**operator = (UINT const& i)**</span><span class="sxs-lookup"><span data-stu-id="2464e-112">**operator=(UINT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="2464e-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="2464e-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="2464e-114">**運算子 UINT () const**</span><span class="sxs-lookup"><span data-stu-id="2464e-114">**operator UINT() const**</span></span>
</dt> <dd>

<span data-ttu-id="2464e-115">隱含轉換成 **UINT** 範例遮罩。</span><span class="sxs-lookup"><span data-stu-id="2464e-115">Implicit conversion to a **UINT** sample mask.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2464e-116">備註</span><span class="sxs-lookup"><span data-stu-id="2464e-116">Remarks</span></span>

<span data-ttu-id="2464e-117">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ 遮罩是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="2464e-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
          
```



## <a name="requirements"></a><span data-ttu-id="2464e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2464e-118">Requirements</span></span>



| <span data-ttu-id="2464e-119">需求</span><span class="sxs-lookup"><span data-stu-id="2464e-119">Requirement</span></span> | <span data-ttu-id="2464e-120">值</span><span class="sxs-lookup"><span data-stu-id="2464e-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2464e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2464e-121">Header</span></span><br/> | <dl> <span data-ttu-id="2464e-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="2464e-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2464e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2464e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2464e-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="2464e-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="2464e-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="2464e-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="2464e-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="2464e-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

