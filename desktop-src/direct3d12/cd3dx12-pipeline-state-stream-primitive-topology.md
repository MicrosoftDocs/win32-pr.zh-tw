---
title: 'CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY 結構 (D3dx12 .h) '
description: 用來將基本拓撲描述為適用于資料流程描述之單一物件的 helper 結構。
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976691"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a><span data-ttu-id="c7f8e-104">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 基本 \_ 拓撲結構</span><span class="sxs-lookup"><span data-stu-id="c7f8e-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY structure</span></span>

<span data-ttu-id="c7f8e-105">用來將基本拓撲描述為適用于資料流程描述之單一物件的 helper 結構。</span><span class="sxs-lookup"><span data-stu-id="c7f8e-105">A helper structure used to describe the primitive topology as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7f8e-106">語法</span><span class="sxs-lookup"><span data-stu-id="c7f8e-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a><span data-ttu-id="c7f8e-107">成員</span><span class="sxs-lookup"><span data-stu-id="c7f8e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7f8e-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 基本 \_ 拓撲**</span><span class="sxs-lookup"><span data-stu-id="c7f8e-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>
</dt> <dd>

<span data-ttu-id="c7f8e-109">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 基本 \_ 拓撲的新、未初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="c7f8e-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY.</span></span>

</dd> <dt>

<span data-ttu-id="c7f8e-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 基本 \_ 拓撲 (D3D12 \_ 基本 \_ 拓撲 \_ 類型 const &i)**</span><span class="sxs-lookup"><span data-stu-id="c7f8e-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="c7f8e-111">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程基本拓撲的新實例 \_ ，並 \_ 初始化為 **D3D12 管線狀態子物件 \_ \_ \_ \_ 類型 \_ 基本 \_ 拓撲** 的子物件類型，以及從 *i* 複製的子物件資料， [**D3D12 \_ 基本 \_ 拓撲 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) 結構。</span><span class="sxs-lookup"><span data-stu-id="c7f8e-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_PRIMITIVE\_TOPOLOGY** and subobject data copied from *i*, a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c7f8e-112">**operator = (D3D12 \_ 基本 \_ 拓撲 \_ 類型 const& i)**</span><span class="sxs-lookup"><span data-stu-id="c7f8e-112">**operator=(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="c7f8e-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="c7f8e-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="c7f8e-114">**運算子 D3D12 \_ 基本 \_ 拓撲 \_ 類型 () 常數**</span><span class="sxs-lookup"><span data-stu-id="c7f8e-114">**operator D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE() const**</span></span>
</dt> <dd>

<span data-ttu-id="c7f8e-115">隱含轉換成 [**D3D12 \_ 基本 \_ 拓撲 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) 結構。</span><span class="sxs-lookup"><span data-stu-id="c7f8e-115">Implicit conversion to a [**D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7f8e-116">備註</span><span class="sxs-lookup"><span data-stu-id="c7f8e-116">Remarks</span></span>

<span data-ttu-id="c7f8e-117">CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 基本 \_ 拓撲是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="c7f8e-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a><span data-ttu-id="c7f8e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7f8e-118">Requirements</span></span>



| <span data-ttu-id="c7f8e-119">需求</span><span class="sxs-lookup"><span data-stu-id="c7f8e-119">Requirement</span></span> | <span data-ttu-id="c7f8e-120">值</span><span class="sxs-lookup"><span data-stu-id="c7f8e-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c7f8e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c7f8e-121">Header</span></span><br/> | <dl> <span data-ttu-id="c7f8e-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7f8e-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7f8e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7f8e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f8e-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="c7f8e-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="c7f8e-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="c7f8e-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="c7f8e-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="c7f8e-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

