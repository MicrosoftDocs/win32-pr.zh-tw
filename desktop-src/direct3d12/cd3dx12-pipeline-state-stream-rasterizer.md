---
title: 'CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER 結構 (D3dx12 .h) '
description: 協助程式結構，用來將轉譯器描述描述為適合資料流程描述的單一物件。
ms.assetid: 650C2DA3-63FB-44D1-BE9A-E21E13DA24DB
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f656ad354430b00e757ece0aa2ce482de1f06e2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989184"
---
# <a name="cd3dx12_pipeline_state_stream_rasterizer-structure"></a><span data-ttu-id="0d139-104">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程轉譯器 \_ 結構</span><span class="sxs-lookup"><span data-stu-id="0d139-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER structure</span></span>

<span data-ttu-id="0d139-105">協助程式結構，用來將轉譯器描述描述為適合資料流程描述的單一物件。</span><span class="sxs-lookup"><span data-stu-id="0d139-105">A helper structure used to describe a rasterizer description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d139-106">語法</span><span class="sxs-lookup"><span data-stu-id="0d139-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER {
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER(CD3DX12_RASTERIZER_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER operator=(CD3DX12_RASTERIZER_DESC const& i);
                                           operator CD3DX12_RASTERIZER_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="0d139-107">成員</span><span class="sxs-lookup"><span data-stu-id="0d139-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0d139-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流 \_ 轉譯器**</span><span class="sxs-lookup"><span data-stu-id="0d139-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**</span></span>
</dt> <dd>

<span data-ttu-id="0d139-109">建立 CD3DX12 \_ 管線狀態資料流程轉譯器的新、未初始化的實例 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="0d139-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER.</span></span>

</dd> <dt>

<span data-ttu-id="0d139-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 串流轉譯器 (CD3DX12 轉譯器 \_ \_ \_ DESC const &i)**</span><span class="sxs-lookup"><span data-stu-id="0d139-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER(CD3DX12\_RASTERIZER\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="0d139-111">建立 CD3DX12 管線狀態資料流程轉譯器的新實例 \_ \_ \_ \_ ，並使用 **D3D12 \_ 管線狀態子物件 \_ \_ \_ 類型 \_** 轉譯器和從 *i* 複製的子物件資料（CD3DX12 的轉譯器 [**\_ \_ DESC**](cd3dx12-rasterizer-desc.md) 結構）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="0d139-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_RASTERIZER** and subobject data copied from *i*, a [**CD3DX12\_RASTERIZER\_DESC**](cd3dx12-rasterizer-desc.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0d139-112">**operator = (CD3DX12 轉譯器 \_ \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="0d139-112">**operator=(CD3DX12\_RASTERIZER\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="0d139-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="0d139-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="0d139-114">**運算子 CD3DX12 轉譯器 \_ \_ DESC () const**</span><span class="sxs-lookup"><span data-stu-id="0d139-114">**operator CD3DX12\_RASTERIZER\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="0d139-115">隱含轉換成 [**CD3DX12 的 \_ 光柵器 \_ DESC**](cd3dx12-rasterizer-desc.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="0d139-115">Implicit conversion to a [**CD3DX12\_RASTERIZER\_DESC**](cd3dx12-rasterizer-desc.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d139-116">備註</span><span class="sxs-lookup"><span data-stu-id="0d139-116">Remarks</span></span>

<span data-ttu-id="0d139-117">CD3DX12 \_ 管線 \_ 狀態 \_ 串流轉譯器 \_ 是 [**CD3DX12 \_ 管線 \_ 狀態 \_ \_ 資料流程**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="0d139-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_RASTERIZER_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
          
```



## <a name="requirements"></a><span data-ttu-id="0d139-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d139-118">Requirements</span></span>



| <span data-ttu-id="0d139-119">需求</span><span class="sxs-lookup"><span data-stu-id="0d139-119">Requirement</span></span> | <span data-ttu-id="0d139-120">值</span><span class="sxs-lookup"><span data-stu-id="0d139-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0d139-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0d139-121">Header</span></span><br/> | <dl> <span data-ttu-id="0d139-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d139-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d139-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d139-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d139-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="0d139-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="0d139-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="0d139-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="0d139-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="0d139-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

