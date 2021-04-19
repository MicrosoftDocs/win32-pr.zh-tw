---
title: 'CD3DX12_DESCRIPTOR_RANGE1 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 描述項 \_ RANGE1 結構。
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- CD3DX12_DESCRIPTOR_RANGE1 結構
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981813"
---
# <a name="cd3dx12_descriptor_range1-structure"></a><span data-ttu-id="7b6e6-104">CD3DX12 \_ 描述項 \_ RANGE1 結構</span><span class="sxs-lookup"><span data-stu-id="7b6e6-104">CD3DX12\_DESCRIPTOR\_RANGE1 structure</span></span>

<span data-ttu-id="7b6e6-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) 結構。</span><span class="sxs-lookup"><span data-stu-id="7b6e6-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b6e6-106">語法</span><span class="sxs-lookup"><span data-stu-id="7b6e6-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="7b6e6-107">成員</span><span class="sxs-lookup"><span data-stu-id="7b6e6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b6e6-108">**CD3DX12 \_ 描述項 \_ RANGE1 ()**</span><span class="sxs-lookup"><span data-stu-id="7b6e6-108">**CD3DX12\_DESCRIPTOR\_RANGE1()**</span></span>
</dt> <dd>

<span data-ttu-id="7b6e6-109">建立新的、未初始化的 CD3DX12 描述項 \_ \_ RANGE1 實例。</span><span class="sxs-lookup"><span data-stu-id="7b6e6-109">Creates a new, uninitialized, instance of a CD3DX12\_DESCRIPTOR\_RANGE1.</span></span>

</dd> <dt>

<span data-ttu-id="7b6e6-110">**明確的 CD3DX12 \_ 描述項 \_ range1 (const D3D12 \_ 描述項 \_ range1 &o)**</span><span class="sxs-lookup"><span data-stu-id="7b6e6-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE1(const D3D12\_DESCRIPTOR\_RANGE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="7b6e6-111">建立 CD3DX12 描述項 range1 的新 \_ 實例 \_ ，並以另一個 [**D3D12 \_ 描述項 \_ range1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="7b6e6-111">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b6e6-112">**CD3DX12 \_ 描述項 \_ RANGE1 (D3D12 \_ 描述項 \_ 範圍 \_ 類型 RANGETYPE、uint NUMDESCRIPTORS、UINT baseShaderRegister、UINT registerSpace = 0、D3D12 \_ 描述元 \_ 範圍 \_ 旗標 = D3D12 \_ 描述項 \_ 範圍旗標 \_ \_ 無、UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加)**</span><span class="sxs-lookup"><span data-stu-id="7b6e6-112">**CD3DX12\_DESCRIPTOR\_RANGE1(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="7b6e6-113">建立 CD3DX12 描述項 RANGE1 的新 \_ 實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="7b6e6-113">Creates a new instance of a CD3DX12\_DESCRIPTOR\_RANGE1, initializing the following parameters:</span></span>

<span data-ttu-id="7b6e6-114">[**D3D12 \_描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="7b6e6-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="7b6e6-115">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="7b6e6-115">UINT numDescriptors</span></span>

<span data-ttu-id="7b6e6-116">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="7b6e6-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="7b6e6-117">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="7b6e6-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="7b6e6-118">[**D3D12 \_描述項 \_ 範圍 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) 標旗標 = D3D12 \_ 描述項 \_ 範圍旗標 \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="7b6e6-118">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="7b6e6-119">UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加</span><span class="sxs-lookup"><span data-stu-id="7b6e6-119">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="7b6e6-120">**內嵌 Init (D3D12 \_ 描述項 \_ 範圍 \_ 類型 RangeType、UINT NumDescriptors、UINT BaseShaderRegister、uint registerSpace = 0、D3D12 \_ 描述元 \_ 範圍 \_ 旗標 = D3D12 描述項範圍旗標 \_ \_ \_ \_ 無、UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加)**</span><span class="sxs-lookup"><span data-stu-id="7b6e6-120">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="7b6e6-121">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="7b6e6-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7b6e6-122">[**D3D12 \_描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="7b6e6-122">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="7b6e6-123">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="7b6e6-123">UINT numDescriptors</span></span>

<span data-ttu-id="7b6e6-124">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="7b6e6-124">UINT baseShaderRegister</span></span>

<span data-ttu-id="7b6e6-125">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="7b6e6-125">UINT registerSpace = 0</span></span>

<span data-ttu-id="7b6e6-126">[**D3D12 \_描述項 \_ 範圍 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) 標旗標 = D3D12 \_ 描述項 \_ 範圍旗標 \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="7b6e6-126">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="7b6e6-127">UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加</span><span class="sxs-lookup"><span data-stu-id="7b6e6-127">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="7b6e6-128">**靜態內嵌 Init (D3D12 \_ 描述項 \_ RANGE1 &範圍、D3D12 \_ 描述項 \_ 範圍 \_ 類型 RANGETYPE、UINT NUMDESCRIPTORS、uint baseShaderRegister、UINT registerSpace = 0、D3D12 \_ 描述項 \_ 範圍 \_ 旗標旗標 = D3D12 描述項範圍 \_ 旗標 \_ \_ \_ 無、uint offsetInDescriptorsFromTableStart = \_ \_ \_ \_ D3D12 描述項範圍位移附加)**</span><span class="sxs-lookup"><span data-stu-id="7b6e6-128">**static inline Init(D3D12\_DESCRIPTOR\_RANGE1 &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12\_DESCRIPTOR\_RANGE\_FLAGS flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="7b6e6-129">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="7b6e6-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="7b6e6-130">[**D3D12 \_描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &範圍</span><span class="sxs-lookup"><span data-stu-id="7b6e6-130">[**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &range</span></span>

<span data-ttu-id="7b6e6-131">[**D3D12 \_描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="7b6e6-131">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="7b6e6-132">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="7b6e6-132">UINT numDescriptors</span></span>

<span data-ttu-id="7b6e6-133">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="7b6e6-133">UINT baseShaderRegister</span></span>

<span data-ttu-id="7b6e6-134">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="7b6e6-134">UINT registerSpace = 0</span></span>

<span data-ttu-id="7b6e6-135">[**D3D12 \_描述項 \_ 範圍 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) 標旗標 = D3D12 \_ 描述項 \_ 範圍旗標 \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="7b6e6-135">[**D3D12\_DESCRIPTOR\_RANGE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = D3D12\_DESCRIPTOR\_RANGE\_FLAG\_NONE</span></span>

<span data-ttu-id="7b6e6-136">UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加</span><span class="sxs-lookup"><span data-stu-id="7b6e6-136">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b6e6-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b6e6-137">Requirements</span></span>



| <span data-ttu-id="7b6e6-138">需求</span><span class="sxs-lookup"><span data-stu-id="7b6e6-138">Requirement</span></span> | <span data-ttu-id="7b6e6-139">值</span><span class="sxs-lookup"><span data-stu-id="7b6e6-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7b6e6-140">標頭</span><span class="sxs-lookup"><span data-stu-id="7b6e6-140">Header</span></span><br/> | <dl> <span data-ttu-id="7b6e6-141"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="7b6e6-141"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b6e6-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b6e6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b6e6-143">**D3D12 \_ 描述項 \_ RANGE1**</span><span class="sxs-lookup"><span data-stu-id="7b6e6-143">**D3D12\_DESCRIPTOR\_RANGE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[<span data-ttu-id="7b6e6-144">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="7b6e6-144">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





