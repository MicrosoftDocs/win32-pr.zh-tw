---
title: 'CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 結構 (D3dx12 .h) '
description: '用來將深度樣板描述描述為適用于資料流程描述之單一物件的 helper 結構。 |CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 結構 (D3dx12 .h) '
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee95e9e37ad1dfced119848c76f071564aaa9435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986725"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a><span data-ttu-id="97393-105">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ STENCIL1 結構</span><span class="sxs-lookup"><span data-stu-id="97393-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 structure</span></span>

<span data-ttu-id="97393-106">用來將深度樣板描述描述為適用于資料流程描述之單一物件的 helper 結構。</span><span class="sxs-lookup"><span data-stu-id="97393-106">A helper structure used to describe a depth stencil description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="97393-107">語法</span><span class="sxs-lookup"><span data-stu-id="97393-107">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a><span data-ttu-id="97393-108">成員</span><span class="sxs-lookup"><span data-stu-id="97393-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="97393-109">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ STENCIL1**</span><span class="sxs-lookup"><span data-stu-id="97393-109">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>
</dt> <dd>

<span data-ttu-id="97393-110">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ STENCIL1 的新、未初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="97393-110">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1.</span></span>

</dd> <dt>

<span data-ttu-id="97393-111">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ STENCIL1 (CD3DX12 \_ 深度 \_ 樣板 \_ DESC1 const &i)**</span><span class="sxs-lookup"><span data-stu-id="97393-111">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1(CD3DX12\_DEPTH\_STENCIL\_DESC1 const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="97393-112">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程深度 STENCIL1 的新實例 \_ \_ ，並使用 **D3D12 管線狀態子物件 \_ \_ \_ \_ 類型 \_ 深度 \_ STENCIL1** 的子物件類型和從 *i* 複製的子物件資料（ [**CD3DX12 \_ 深度 \_ 樣板 \_ DESC1**](cd3dx12-depth-stencil-desc1.md) 結構）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="97393-112">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** and subobject data copied from *i*, a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="97393-113">**operator = (CD3DX12 \_ DEPTH \_ 樣板 \_ DESC1 const& i)**</span><span class="sxs-lookup"><span data-stu-id="97393-113">**operator=(CD3DX12\_DEPTH\_STENCIL\_DESC1 const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="97393-114">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="97393-114">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="97393-115">**運算子 CD3DX12 \_ 深度 \_ 樣板 \_ DESC1 () 常數**</span><span class="sxs-lookup"><span data-stu-id="97393-115">**operator CD3DX12\_DEPTH\_STENCIL\_DESC1() const**</span></span>
</dt> <dd>

<span data-ttu-id="97393-116">隱含轉換成 [**CD3DX12 \_ 深度樣板 \_ \_ DESC1**](cd3dx12-depth-stencil-desc1.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="97393-116">Implicit conversion to a [**CD3DX12\_DEPTH\_STENCIL\_DESC1**](cd3dx12-depth-stencil-desc1.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97393-117">備註</span><span class="sxs-lookup"><span data-stu-id="97393-117">Remarks</span></span>

<span data-ttu-id="97393-118">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ STENCIL1 是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="97393-118">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1 is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
```



## <a name="requirements"></a><span data-ttu-id="97393-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="97393-119">Requirements</span></span>



| <span data-ttu-id="97393-120">需求</span><span class="sxs-lookup"><span data-stu-id="97393-120">Requirement</span></span> | <span data-ttu-id="97393-121">值</span><span class="sxs-lookup"><span data-stu-id="97393-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="97393-122">標頭</span><span class="sxs-lookup"><span data-stu-id="97393-122">Header</span></span><br/> | <dl> <span data-ttu-id="97393-123"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="97393-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97393-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97393-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97393-125">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="97393-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="97393-126">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="97393-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="97393-127">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="97393-127">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

