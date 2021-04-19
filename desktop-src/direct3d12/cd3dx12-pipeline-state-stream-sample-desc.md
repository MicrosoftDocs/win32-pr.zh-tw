---
title: 'CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，用來將範例描述描述為適合資料流程描述的單一物件。
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986770"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a><span data-ttu-id="6247a-104">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="6247a-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC structure</span></span>

<span data-ttu-id="6247a-105">協助程式結構，用來將範例描述描述為適合資料流程描述的單一物件。</span><span class="sxs-lookup"><span data-stu-id="6247a-105">A helper structure used to describe a sample description as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6247a-106">語法</span><span class="sxs-lookup"><span data-stu-id="6247a-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="6247a-107">成員</span><span class="sxs-lookup"><span data-stu-id="6247a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6247a-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6247a-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>
</dt> <dd>

<span data-ttu-id="6247a-109">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ DESC 的新、未初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="6247a-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="6247a-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ desc (DXGI \_ 範例 \_ desc const &i)**</span><span class="sxs-lookup"><span data-stu-id="6247a-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC(DXGI\_SAMPLE\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="6247a-111">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程範例 desc 的新實例 \_ \_ ，並使用 D3D12 管線狀態子物件類型的子物件類型、 **\_ \_ \_ \_ \_ 範例 \_ desc** 和從 *i* 複製的子物件資料（ [**DXGI \_ 範例 \_ desc**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) 結構）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="6247a-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_SAMPLE\_DESC** and subobject data copied from *i*, a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6247a-112">**operator = (DXGI \_ 範例 \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="6247a-112">**operator=(DXGI\_SAMPLE\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="6247a-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="6247a-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="6247a-114">**運算子 DXGI \_ 範例 \_ DESC () 常數**</span><span class="sxs-lookup"><span data-stu-id="6247a-114">**operator DXGI\_SAMPLE\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="6247a-115">隱含轉換成 [**DXGI \_ 範例 \_ DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) 結構。</span><span class="sxs-lookup"><span data-stu-id="6247a-115">Implicit conversion to a [**DXGI\_SAMPLE\_DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6247a-116">備註</span><span class="sxs-lookup"><span data-stu-id="6247a-116">Remarks</span></span>

<span data-ttu-id="6247a-117">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 範例 \_ DESC 是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="6247a-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
```



## <a name="requirements"></a><span data-ttu-id="6247a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6247a-118">Requirements</span></span>



| <span data-ttu-id="6247a-119">需求</span><span class="sxs-lookup"><span data-stu-id="6247a-119">Requirement</span></span> | <span data-ttu-id="6247a-120">值</span><span class="sxs-lookup"><span data-stu-id="6247a-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6247a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6247a-121">Header</span></span><br/> | <dl> <span data-ttu-id="6247a-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="6247a-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6247a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6247a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6247a-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="6247a-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="6247a-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="6247a-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="6247a-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6247a-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

