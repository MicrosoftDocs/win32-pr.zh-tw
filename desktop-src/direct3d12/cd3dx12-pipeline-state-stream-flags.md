---
title: 'CD3DX12_PIPELINE_STATE_STREAM_FLAGS 結構 (D3dx12 .h) '
description: 用來將管線狀態旗標描述為適用于資料流程描述之單一物件的 helper 結構。
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034f4a63c774ca41f28fbe9e6c2945fddee47c4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986128"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a><span data-ttu-id="b1110-104">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 旗標結構</span><span class="sxs-lookup"><span data-stu-id="b1110-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS structure</span></span>

<span data-ttu-id="b1110-105">用來將管線狀態旗標描述為適用于資料流程描述之單一物件的 helper 結構。</span><span class="sxs-lookup"><span data-stu-id="b1110-105">A helper structure used to describe pipeline state flags as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1110-106">語法</span><span class="sxs-lookup"><span data-stu-id="b1110-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a><span data-ttu-id="b1110-107">成員</span><span class="sxs-lookup"><span data-stu-id="b1110-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b1110-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="b1110-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="b1110-109">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 旗標的新、未初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="b1110-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="b1110-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 旗標 (D3D12 \_ 管線 \_ 狀態 \_ 旗標 const &i)**</span><span class="sxs-lookup"><span data-stu-id="b1110-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS(D3D12\_PIPELINE\_STATE\_FLAGS const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="b1110-111">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程旗標的新實例 \_ ，並使用 **D3D12 \_ 管線狀態子物件 \_ \_ \_ 類型 \_ 旗標** 和從 *i* 複製的子物件資料（ [**D3D12 \_ 管線 \_ 狀態 \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) 結構）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="b1110-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_FLAGS** and subobject data copied from *i*, a [**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b1110-112">**operator = (D3D12 \_ 管線 \_ 狀態 \_ 旗標 const& i)**</span><span class="sxs-lookup"><span data-stu-id="b1110-112">**operator=(D3D12\_PIPELINE\_STATE\_FLAGS const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="b1110-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="b1110-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="b1110-114">**運算子 D3D12 \_ 管線 \_ 狀態 \_ 旗標 () 常數**</span><span class="sxs-lookup"><span data-stu-id="b1110-114">**operator D3D12\_PIPELINE\_STATE\_FLAGS() const**</span></span>
</dt> <dd>

<span data-ttu-id="b1110-115">隱含轉換成 [**D3D12 \_ 管線 \_ 狀態 \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) 結構。</span><span class="sxs-lookup"><span data-stu-id="b1110-115">Implicit conversion to a [**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1110-116">備註</span><span class="sxs-lookup"><span data-stu-id="b1110-116">Remarks</span></span>

<span data-ttu-id="b1110-117">CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 旗標是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="b1110-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
```



## <a name="requirements"></a><span data-ttu-id="b1110-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1110-118">Requirements</span></span>



| <span data-ttu-id="b1110-119">需求</span><span class="sxs-lookup"><span data-stu-id="b1110-119">Requirement</span></span> | <span data-ttu-id="b1110-120">值</span><span class="sxs-lookup"><span data-stu-id="b1110-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b1110-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b1110-121">Header</span></span><br/> | <dl> <span data-ttu-id="b1110-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1110-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1110-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1110-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1110-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="b1110-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b1110-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="b1110-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="b1110-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="b1110-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

