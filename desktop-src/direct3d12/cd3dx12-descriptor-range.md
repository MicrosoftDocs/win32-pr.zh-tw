---
title: 'CD3DX12_DESCRIPTOR_RANGE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 描述項 \_ 範圍結構。
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- CD3DX12_DESCRIPTOR_RANGE 結構
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b511af1766daaefa7f92d33b71841b3a69c99927
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974841"
---
# <a name="cd3dx12_descriptor_range-structure"></a><span data-ttu-id="0255f-104">CD3DX12 \_ 描述項 \_ 範圍結構</span><span class="sxs-lookup"><span data-stu-id="0255f-104">CD3DX12\_DESCRIPTOR\_RANGE structure</span></span>

<span data-ttu-id="0255f-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) 結構。</span><span class="sxs-lookup"><span data-stu-id="0255f-105">A helper structure to enable easy initialization of a [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0255f-106">語法</span><span class="sxs-lookup"><span data-stu-id="0255f-106">Syntax</span></span>


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a><span data-ttu-id="0255f-107">成員</span><span class="sxs-lookup"><span data-stu-id="0255f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0255f-108">**CD3DX12 \_ 描述項 \_ 範圍 ()**</span><span class="sxs-lookup"><span data-stu-id="0255f-108">**CD3DX12\_DESCRIPTOR\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="0255f-109">建立新的、未初始化的 D3DX12 描述項 \_ \_ 範圍實例。</span><span class="sxs-lookup"><span data-stu-id="0255f-109">Creates a new, uninitialized, instance of a D3DX12\_DESCRIPTOR\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="0255f-110">**明確的 CD3DX12 \_ 描述項 \_ 範圍 (const D3D12 \_ 描述項 \_ 範圍 &o)**</span><span class="sxs-lookup"><span data-stu-id="0255f-110">**explicit CD3DX12\_DESCRIPTOR\_RANGE(const D3D12\_DESCRIPTOR\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="0255f-111">建立 D3DX12 描述元範圍的新 \_ 實例 \_ ，並以另一個 [**D3D12 \_ 描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="0255f-111">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initialized with the contents of another [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0255f-112">**CD3DX12 \_ 描述項 \_ 範圍 (D3D12 \_ 描述項 \_ 範圍 \_ 類型 RANGETYPE、uint NUMDESCRIPTORS、UINT baseShaderRegister、UINT RegisterSpace = 0、UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加)**</span><span class="sxs-lookup"><span data-stu-id="0255f-112">**CD3DX12\_DESCRIPTOR\_RANGE(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="0255f-113">建立 D3DX12 描述項範圍的新 \_ 實例 \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="0255f-113">Creates a new instance of a D3DX12\_DESCRIPTOR\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="0255f-114">[**D3D12 \_描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="0255f-114">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="0255f-115">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="0255f-115">UINT numDescriptors</span></span>

<span data-ttu-id="0255f-116">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="0255f-116">UINT baseShaderRegister</span></span>

<span data-ttu-id="0255f-117">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="0255f-117">UINT registerSpace = 0</span></span>

<span data-ttu-id="0255f-118">UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加</span><span class="sxs-lookup"><span data-stu-id="0255f-118">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="0255f-119">**內嵌 Init (D3D12 \_ 描述項 \_ 範圍 \_ 類型 RangeType、UINT NumDescriptors、UINT BaseShaderRegister、UINT registerSpace = 0、UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加)**</span><span class="sxs-lookup"><span data-stu-id="0255f-119">**inline Init(D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="0255f-120">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="0255f-120">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="0255f-121">[**D3D12 \_描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="0255f-121">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="0255f-122">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="0255f-122">UINT numDescriptors</span></span>

<span data-ttu-id="0255f-123">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="0255f-123">UINT baseShaderRegister</span></span>

<span data-ttu-id="0255f-124">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="0255f-124">UINT registerSpace = 0</span></span>

<span data-ttu-id="0255f-125">UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加</span><span class="sxs-lookup"><span data-stu-id="0255f-125">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> <dt>

<span data-ttu-id="0255f-126">**靜態內嵌 Init (D3D12 \_ 描述元 \_ 範圍 &範圍、D3D12 \_ 描述項 \_ 範圍 \_ 類型 RANGETYPE、UINT NUMDESCRIPTORS、UINT baseShaderRegister、UINT RegisterSpace = 0、uint offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加)**</span><span class="sxs-lookup"><span data-stu-id="0255f-126">**static inline Init(D3D12\_DESCRIPTOR\_RANGE &range, D3D12\_DESCRIPTOR\_RANGE\_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND)**</span></span>
</dt> <dd>

<span data-ttu-id="0255f-127">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="0255f-127">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="0255f-128">[**D3D12 \_描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &範圍</span><span class="sxs-lookup"><span data-stu-id="0255f-128">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &range</span></span>

<span data-ttu-id="0255f-129">[**D3D12 \_描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span><span class="sxs-lookup"><span data-stu-id="0255f-129">[**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType</span></span>

<span data-ttu-id="0255f-130">UINT numDescriptors</span><span class="sxs-lookup"><span data-stu-id="0255f-130">UINT numDescriptors</span></span>

<span data-ttu-id="0255f-131">UINT baseShaderRegister</span><span class="sxs-lookup"><span data-stu-id="0255f-131">UINT baseShaderRegister</span></span>

<span data-ttu-id="0255f-132">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="0255f-132">UINT registerSpace = 0</span></span>

<span data-ttu-id="0255f-133">UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加</span><span class="sxs-lookup"><span data-stu-id="0255f-133">UINT offsetInDescriptorsFromTableStart = D3D12\_DESCRIPTOR\_RANGE\_OFFSET\_APPEND</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0255f-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="0255f-134">Requirements</span></span>



| <span data-ttu-id="0255f-135">需求</span><span class="sxs-lookup"><span data-stu-id="0255f-135">Requirement</span></span> | <span data-ttu-id="0255f-136">值</span><span class="sxs-lookup"><span data-stu-id="0255f-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0255f-137">標頭</span><span class="sxs-lookup"><span data-stu-id="0255f-137">Header</span></span><br/> | <dl> <span data-ttu-id="0255f-138"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="0255f-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0255f-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0255f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0255f-140">**D3D12 \_ 描述元 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="0255f-140">**D3D12\_DESCRIPTOR\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[<span data-ttu-id="0255f-141">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="0255f-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





