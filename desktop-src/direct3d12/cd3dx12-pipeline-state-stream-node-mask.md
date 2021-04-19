---
title: 'CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK 結構 (D3dx12 .h) '
description: 用來將節點遮罩描述為適用于資料流程描述之單一物件的 helper 結構。
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c364ecd20459d8c20bdd3d30b969cc3b9ae46d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982863"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a><span data-ttu-id="751f9-104">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 節點 \_ 遮罩結構</span><span class="sxs-lookup"><span data-stu-id="751f9-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK structure</span></span>

<span data-ttu-id="751f9-105">用來將節點遮罩描述為適用于資料流程描述之單一物件的 helper 結構。</span><span class="sxs-lookup"><span data-stu-id="751f9-105">A helper structure used to describe a node mask as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="751f9-106">語法</span><span class="sxs-lookup"><span data-stu-id="751f9-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK {
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK operator=(UINT const& i);
                                          operator UINT() const;
};
```



## <a name="members"></a><span data-ttu-id="751f9-107">成員</span><span class="sxs-lookup"><span data-stu-id="751f9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="751f9-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 節點 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="751f9-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK**</span></span>
</dt> <dd>

<span data-ttu-id="751f9-109">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 節點 \_ 遮罩的新、未初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="751f9-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK.</span></span>

</dd> <dt>

<span data-ttu-id="751f9-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 節點 \_ 遮罩 (UINT const &i)**</span><span class="sxs-lookup"><span data-stu-id="751f9-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK(UINT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="751f9-111">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程節點遮罩的新實例 \_ \_ ，並使用 **D3D12 管線狀態子物件 \_ \_ \_ \_ 類型 \_ 節點 \_ 遮罩** 的子物件類型和從 *i* 複製的子物件資料（ **UINT** 節點遮罩）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="751f9-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_NODE\_MASK** and subobject data copied from *i*, a **UINT** node mask.</span></span>

</dd> <dt>

<span data-ttu-id="751f9-112">**operator = (UINT const& i)**</span><span class="sxs-lookup"><span data-stu-id="751f9-112">**operator=(UINT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="751f9-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="751f9-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="751f9-114">**運算子 UINT () const**</span><span class="sxs-lookup"><span data-stu-id="751f9-114">**operator UINT() const**</span></span>
</dt> <dd>

<span data-ttu-id="751f9-115">隱含轉換成 **UINT** 節點遮罩。</span><span class="sxs-lookup"><span data-stu-id="751f9-115">Implicit conversion to a **UINT** node mask.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="751f9-116">備註</span><span class="sxs-lookup"><span data-stu-id="751f9-116">Remarks</span></span>

<span data-ttu-id="751f9-117">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 節點 \_ 遮罩是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="751f9-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
```



## <a name="requirements"></a><span data-ttu-id="751f9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="751f9-118">Requirements</span></span>



| <span data-ttu-id="751f9-119">需求</span><span class="sxs-lookup"><span data-stu-id="751f9-119">Requirement</span></span> | <span data-ttu-id="751f9-120">值</span><span class="sxs-lookup"><span data-stu-id="751f9-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="751f9-121">標頭</span><span class="sxs-lookup"><span data-stu-id="751f9-121">Header</span></span><br/> | <dl> <span data-ttu-id="751f9-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="751f9-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="751f9-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="751f9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="751f9-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="751f9-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="751f9-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="751f9-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="751f9-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="751f9-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

