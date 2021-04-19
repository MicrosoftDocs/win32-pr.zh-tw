---
title: 'CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS 結構 (D3dx12 .h) '
description: 協助程式結構，用來將轉譯目標格式描述為適合資料流程描述的單一物件。
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991443"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a><span data-ttu-id="9ec7a-104">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 轉譯 \_ 目標 \_ 格式結構</span><span class="sxs-lookup"><span data-stu-id="9ec7a-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS structure</span></span>

<span data-ttu-id="9ec7a-105">協助程式結構，用來將轉譯目標格式描述為適合資料流程描述的單一物件。</span><span class="sxs-lookup"><span data-stu-id="9ec7a-105">A helper structure used to describe the render target formats as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ec7a-106">語法</span><span class="sxs-lookup"><span data-stu-id="9ec7a-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a><span data-ttu-id="9ec7a-107">成員</span><span class="sxs-lookup"><span data-stu-id="9ec7a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ec7a-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 轉譯 \_ 目標 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="9ec7a-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>
</dt> <dd>

<span data-ttu-id="9ec7a-109">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程轉譯 \_ \_ 目標 \_ 格式的新、未初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="9ec7a-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS.</span></span>

</dd> <dt>

<span data-ttu-id="9ec7a-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 轉譯 \_ 目標 \_ 格式 (D3D12 \_ RT \_ 格式 \_ 陣列 const &i)**</span><span class="sxs-lookup"><span data-stu-id="9ec7a-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS(D3D12\_RT\_FORMAT\_ARRAY const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="9ec7a-111">建立 CD3DX12 \_ 管線 \_ 狀態資料流程轉譯目標格式的新實例 \_ \_ \_ \_ ，並以 **D3D12 管線狀態子物件類型的 \_ 管線狀態子物件類型轉譯 \_ \_ \_ \_ \_ 目標 \_ 格式** 和子物件資料（ [**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)結構）進行初始化。 </span><span class="sxs-lookup"><span data-stu-id="9ec7a-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_RENDER\_TARGET\_FORMATS** and subobject data copied from *i*, a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9ec7a-112">**operator = (D3D12 \_ RT \_ 格式 \_ 陣列 const& i)**</span><span class="sxs-lookup"><span data-stu-id="9ec7a-112">**operator=(D3D12\_RT\_FORMAT\_ARRAY const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="9ec7a-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="9ec7a-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="9ec7a-114">**運算子 D3D12 \_ RT \_ 格式 \_ 陣列 () 常數**</span><span class="sxs-lookup"><span data-stu-id="9ec7a-114">**operator D3D12\_RT\_FORMAT\_ARRAY() const**</span></span>
</dt> <dd>

<span data-ttu-id="9ec7a-115">隱含轉換成 [**D3D12 \_ RT \_ 格式 \_ 陣列**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) 結構。</span><span class="sxs-lookup"><span data-stu-id="9ec7a-115">Implicit conversion to a [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ec7a-116">備註</span><span class="sxs-lookup"><span data-stu-id="9ec7a-116">Remarks</span></span>

<span data-ttu-id="9ec7a-117">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 轉譯 \_ 目標 \_ 格式是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="9ec7a-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
```



## <a name="requirements"></a><span data-ttu-id="9ec7a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ec7a-118">Requirements</span></span>



| <span data-ttu-id="9ec7a-119">需求</span><span class="sxs-lookup"><span data-stu-id="9ec7a-119">Requirement</span></span> | <span data-ttu-id="9ec7a-120">值</span><span class="sxs-lookup"><span data-stu-id="9ec7a-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec7a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9ec7a-121">Header</span></span><br/> | <dl> <span data-ttu-id="9ec7a-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="9ec7a-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ec7a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ec7a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec7a-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="9ec7a-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="9ec7a-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="9ec7a-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="9ec7a-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="9ec7a-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

