---
title: 'CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT 結構 (D3dx12 .h) '
description: 用來將深度樣板格式描述為適用于資料流程描述之單一物件的 helper 結構。
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dc7ae2703ac80ac155c04d42624a081723288bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106995895"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a><span data-ttu-id="455ea-104">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ 樣板 \_ 格式結構</span><span class="sxs-lookup"><span data-stu-id="455ea-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT structure</span></span>

<span data-ttu-id="455ea-105">用來將深度樣板格式描述為適用于資料流程描述之單一物件的 helper 結構。</span><span class="sxs-lookup"><span data-stu-id="455ea-105">A helper structure used to describe the depth stencil format as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="455ea-106">語法</span><span class="sxs-lookup"><span data-stu-id="455ea-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a><span data-ttu-id="455ea-107">成員</span><span class="sxs-lookup"><span data-stu-id="455ea-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="455ea-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ 樣板 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="455ea-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="455ea-109">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度樣板 \_ \_ 格式的新、未初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="455ea-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT.</span></span>

</dd> <dt>

<span data-ttu-id="455ea-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ 樣板 \_ 格式 (DXGI \_ 格式 const &i)**</span><span class="sxs-lookup"><span data-stu-id="455ea-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT(DXGI\_FORMAT const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="455ea-111">建立 CD3DX12 \_ 管線 \_ 狀態資料流程深度樣板格式的新實例 \_ \_ \_ \_ ，並以 **D3D12 管線狀態子物件 \_ \_ \_ \_ 類型深度樣板 \_ \_ \_ 格式** 的子物件類型和從 *i* 複製的子物件資料（ [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 列舉）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="455ea-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL\_FORMAT** and subobject data copied from *i*, a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="455ea-112">**operator = (DXGI \_ 格式 const& i)**</span><span class="sxs-lookup"><span data-stu-id="455ea-112">**operator=(DXGI\_FORMAT const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="455ea-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="455ea-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="455ea-114">**運算子 DXGI \_ 格式 () 常數**</span><span class="sxs-lookup"><span data-stu-id="455ea-114">**operator DXGI\_FORMAT() const**</span></span>
</dt> <dd>

<span data-ttu-id="455ea-115">隱含轉換成 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 列舉。</span><span class="sxs-lookup"><span data-stu-id="455ea-115">Implicit conversion to a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="455ea-116">備註</span><span class="sxs-lookup"><span data-stu-id="455ea-116">Remarks</span></span>

<span data-ttu-id="455ea-117">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 深度 \_ 樣板 \_ 格式是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="455ea-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
```



## <a name="requirements"></a><span data-ttu-id="455ea-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="455ea-118">Requirements</span></span>



| <span data-ttu-id="455ea-119">需求</span><span class="sxs-lookup"><span data-stu-id="455ea-119">Requirement</span></span> | <span data-ttu-id="455ea-120">值</span><span class="sxs-lookup"><span data-stu-id="455ea-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="455ea-121">標頭</span><span class="sxs-lookup"><span data-stu-id="455ea-121">Header</span></span><br/> | <dl> <span data-ttu-id="455ea-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="455ea-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="455ea-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="455ea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="455ea-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="455ea-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="455ea-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="455ea-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="455ea-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="455ea-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

