---
title: 'CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，用來將 blend 描述描述為適合資料流程描述的單一物件。
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251be9cc1423babc58e1d3c3be87c5345308874
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974840"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a><span data-ttu-id="35f77-104">CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ BLEND \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="35f77-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC structure</span></span>

<span data-ttu-id="35f77-105">協助程式結構，用來將 blend 描述描述為適合資料流程描述的單一物件。</span><span class="sxs-lookup"><span data-stu-id="35f77-105">A helper structure used to describe a blend description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="35f77-106">語法</span><span class="sxs-lookup"><span data-stu-id="35f77-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="35f77-107">成員</span><span class="sxs-lookup"><span data-stu-id="35f77-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="35f77-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ BLEND \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="35f77-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="35f77-109">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ BLEND \_ DESC 的新、未初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="35f77-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="35f77-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ BLEND \_ desc (CD3DX12 \_ BLEND \_ DESC const &i)**</span><span class="sxs-lookup"><span data-stu-id="35f77-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC(CD3DX12\_BLEND\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="35f77-111">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 BLEND DESC 的新實例 \_ \_ ，並使用 **D3D12 管線狀態子物件 \_ \_ \_ \_ 類型 \_ BLEND** 和從 *i* 複製的子物件資料（ [**CD3DX12 \_ BLEND \_ DESC**](cd3dx12-blend-desc.md) 結構）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="35f77-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_BLEND** and subobject data copied from *i*, a [**CD3DX12\_BLEND\_DESC**](cd3dx12-blend-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="35f77-112">**operator = (CD3DX12 \_ BLEND \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="35f77-112">**operator=(CD3DX12\_BLEND\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="35f77-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="35f77-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="35f77-114">**運算子 CD3DX12 \_ BLEND \_ DESC () const**</span><span class="sxs-lookup"><span data-stu-id="35f77-114">**operator CD3DX12\_BLEND\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="35f77-115">隱含轉換成 [**CD3DX12 \_ BLEND \_ DESC**](cd3dx12-blend-desc.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="35f77-115">Implicit conversion to a [**CD3DX12\_BLEND\_DESC**](cd3dx12-blend-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35f77-116">備註</span><span class="sxs-lookup"><span data-stu-id="35f77-116">Remarks</span></span>

<span data-ttu-id="35f77-117">CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ BLEND \_ DESC 是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="35f77-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="35f77-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="35f77-118">Requirements</span></span>



| <span data-ttu-id="35f77-119">需求</span><span class="sxs-lookup"><span data-stu-id="35f77-119">Requirement</span></span> | <span data-ttu-id="35f77-120">值</span><span class="sxs-lookup"><span data-stu-id="35f77-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="35f77-121">標頭</span><span class="sxs-lookup"><span data-stu-id="35f77-121">Header</span></span><br/> | <dl> <span data-ttu-id="35f77-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="35f77-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f77-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35f77-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f77-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="35f77-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="35f77-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="35f77-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="35f77-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="35f77-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

