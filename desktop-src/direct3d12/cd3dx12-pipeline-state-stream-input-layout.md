---
title: 'CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT 結構 (D3dx12 .h) '
description: 用來將輸入配置描述為適用于資料流程描述之單一物件的 helper 結構。
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991445"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a><span data-ttu-id="541a2-104">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 輸入 \_ 版面配置結構</span><span class="sxs-lookup"><span data-stu-id="541a2-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT structure</span></span>

<span data-ttu-id="541a2-105">用來將輸入配置描述為適用于資料流程描述之單一物件的 helper 結構。</span><span class="sxs-lookup"><span data-stu-id="541a2-105">A helper structure used to describe an input layout as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="541a2-106">語法</span><span class="sxs-lookup"><span data-stu-id="541a2-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a><span data-ttu-id="541a2-107">成員</span><span class="sxs-lookup"><span data-stu-id="541a2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="541a2-108">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 輸入 \_ 版面配置**</span><span class="sxs-lookup"><span data-stu-id="541a2-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>
</dt> <dd>

<span data-ttu-id="541a2-109">建立 CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 輸入配置的新、未初始化的實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="541a2-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT.</span></span>

</dd> <dt>

<span data-ttu-id="541a2-110">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 輸入 \_ 版面配置 (D3D12 \_ 輸入 \_ 版面配置 \_ DESC const &i)**</span><span class="sxs-lookup"><span data-stu-id="541a2-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT(D3D12\_INPUT\_LAYOUT\_DESC const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="541a2-111">建立 CD3DX12 \_ 管線狀態資料流程輸入配置的新實例 \_ \_ \_ \_ ，並使用 **D3D12 管線狀態子物件 \_ \_ \_ \_ 類型 \_ 輸入 \_** 配置和從 *i* 複製的子物件資料（ [**D3D12 輸入配置 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) 結構）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="541a2-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_INPUT\_LAYOUT** and subobject data copied from *i*, a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="541a2-112">**operator = (D3D12 \_ 輸入 \_ 版面配置 \_ DESC const& i)**</span><span class="sxs-lookup"><span data-stu-id="541a2-112">**operator=(D3D12\_INPUT\_LAYOUT\_DESC const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="541a2-113">複製指派運算子。</span><span class="sxs-lookup"><span data-stu-id="541a2-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="541a2-114">**operator D3D12 \_ 輸入 \_ 版面配置 \_ DESC () const**</span><span class="sxs-lookup"><span data-stu-id="541a2-114">**operator D3D12\_INPUT\_LAYOUT\_DESC() const**</span></span>
</dt> <dd>

<span data-ttu-id="541a2-115">隱含轉換成 [**D3D12 \_ 輸入版面 \_ 配置 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="541a2-115">Implicit conversion to a [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="541a2-116">備註</span><span class="sxs-lookup"><span data-stu-id="541a2-116">Remarks</span></span>

<span data-ttu-id="541a2-117">CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 輸入配置 \_ 是 [**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_**](cd3dx12-pipeline-state-stream-subobject.md) 子物件範本的 typedef 特製化，其定義如下：</span><span class="sxs-lookup"><span data-stu-id="541a2-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
```



## <a name="requirements"></a><span data-ttu-id="541a2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="541a2-118">Requirements</span></span>



| <span data-ttu-id="541a2-119">需求</span><span class="sxs-lookup"><span data-stu-id="541a2-119">Requirement</span></span> | <span data-ttu-id="541a2-120">值</span><span class="sxs-lookup"><span data-stu-id="541a2-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="541a2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="541a2-121">Header</span></span><br/> | <dl> <span data-ttu-id="541a2-122"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="541a2-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="541a2-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="541a2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="541a2-124">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="541a2-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="541a2-125">**CD3DX12 \_ 管線 \_ 狀態 \_ 資料流程 \_ 子物件**</span><span class="sxs-lookup"><span data-stu-id="541a2-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="541a2-126">**D3D12 \_ 管線 \_ 狀態子物件 \_ \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="541a2-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

