---
title: 'CD3DX12_RESOURCE_BARRIER 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 資源 \_ 關卡結構。
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- CD3DX12_RESOURCE_BARRIER 結構
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992353"
---
# <a name="cd3dx12_resource_barrier-structure"></a><span data-ttu-id="fee51-104">CD3DX12 \_ 資源 \_ 關卡結構</span><span class="sxs-lookup"><span data-stu-id="fee51-104">CD3DX12\_RESOURCE\_BARRIER structure</span></span>

<span data-ttu-id="fee51-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 資源 \_ 關卡**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) 結構。</span><span class="sxs-lookup"><span data-stu-id="fee51-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fee51-106">語法</span><span class="sxs-lookup"><span data-stu-id="fee51-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a><span data-ttu-id="fee51-107">成員</span><span class="sxs-lookup"><span data-stu-id="fee51-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fee51-108">**CD3DX12 \_ 資源 \_ 屏障 ()**</span><span class="sxs-lookup"><span data-stu-id="fee51-108">**CD3DX12\_RESOURCE\_BARRIER()**</span></span>
</dt> <dd>

<span data-ttu-id="fee51-109">建立 CD3DX12 資源屏障的新、未初始化的 \_ 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fee51-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_BARRIER.</span></span>

</dd> <dt>

<span data-ttu-id="fee51-110">**明確的 CD3DX12 \_ 資源 \_ 屏障 (const D3D12 \_ 資源 \_ 屏障 &o)**</span><span class="sxs-lookup"><span data-stu-id="fee51-110">**explicit CD3DX12\_RESOURCE\_BARRIER(const D3D12\_RESOURCE\_BARRIER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="fee51-111">建立 CD3DX12 資源屏障的新實例 \_ \_ ，並以另一個 [**D3D12 \_ 資源 \_ 屏障**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="fee51-111">Creates a new instance of a CD3DX12\_RESOURCE\_BARRIER, initialized with the contents of another [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).</span></span>

</dd> <dt>

<span data-ttu-id="fee51-112">**靜態內嵌轉換 (ID3D12Resource \* pResource、D3D12 \_ 資源 \_ 狀態 stateBefore、D3D12 \_ 資源 \_ 狀態 STATEAFTER、UINT subresource = D3D12 \_ 資源 \_ 屏障 \_ ALL \_ 子資源、D3D12 \_ 資源 \_ 屏障 \_ 旗標旗標 = D3D12 \_ 資源 \_ 屏障 \_ 旗標 \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="fee51-112">**static inline Transition(ID3D12Resource\* pResource, D3D12\_RESOURCE\_STATES stateBefore, D3D12\_RESOURCE\_STATES stateAfter, UINT subresource = D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES, D3D12\_RESOURCE\_BARRIER\_FLAGS flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="fee51-113">使用下列參數，在資源狀態之間轉換：</span><span class="sxs-lookup"><span data-stu-id="fee51-113">Transitions between resource states, using the following parameters:</span></span>

<span data-ttu-id="fee51-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*pResource</span><span class="sxs-lookup"><span data-stu-id="fee51-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

<span data-ttu-id="fee51-115">[**D3D12 \_資源 \_ 狀態**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore</span><span class="sxs-lookup"><span data-stu-id="fee51-115">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore</span></span>

<span data-ttu-id="fee51-116">[**D3D12 \_資源 \_ 狀態**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter</span><span class="sxs-lookup"><span data-stu-id="fee51-116">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter</span></span>

<span data-ttu-id="fee51-117"> (opt) UINT subresource = [ **D3D12 \_ 資源 \_ 屏障 \_ 所有 \_ 子資源**](constants.md)</span><span class="sxs-lookup"><span data-stu-id="fee51-117">(opt) UINT subresource = [**D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES**](constants.md)</span></span>

<span data-ttu-id="fee51-118"> (opt) [**D3D12 \_ 資源 \_ 屏障 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) 標旗標 = D3D12 \_ 資源 \_ 屏障 \_ 旗標 \_ 無</span><span class="sxs-lookup"><span data-stu-id="fee51-118">(opt) [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="fee51-119">**靜態內嵌別名 (ID3D12Resource \* pResourceBefore、ID3D12Resource \* pResourceAfter)**</span><span class="sxs-lookup"><span data-stu-id="fee51-119">**static inline Aliasing(ID3D12Resource\* pResourceBefore, ID3D12Resource\* pResourceAfter)**</span></span>
</dt> <dd>

<span data-ttu-id="fee51-120">在關卡轉換之前和之後建立資源的別名。</span><span class="sxs-lookup"><span data-stu-id="fee51-120">Creates aliases for the resource before and after the barrier transition.</span></span> <span data-ttu-id="fee51-121">參數：</span><span class="sxs-lookup"><span data-stu-id="fee51-121">Parameters:</span></span>

<span data-ttu-id="fee51-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*pResourceBefore</span><span class="sxs-lookup"><span data-stu-id="fee51-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceBefore</span></span>

<span data-ttu-id="fee51-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*pResourceAfter</span><span class="sxs-lookup"><span data-stu-id="fee51-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceAfter</span></span>

</dd> <dt>

<span data-ttu-id="fee51-124">**靜態內嵌 UAV (ID3D12Resource \* pResource)**</span><span class="sxs-lookup"><span data-stu-id="fee51-124">**static inline UAV(ID3D12Resource\* pResource)**</span></span>
</dt> <dd>

<span data-ttu-id="fee51-125">建立資源的未排序存取- (UAV) 。</span><span class="sxs-lookup"><span data-stu-id="fee51-125">Creates an unordered-access-view (UAV) for the resource.</span></span> <span data-ttu-id="fee51-126">參數：</span><span class="sxs-lookup"><span data-stu-id="fee51-126">Parameters:</span></span>

<span data-ttu-id="fee51-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \*pResource</span><span class="sxs-lookup"><span data-stu-id="fee51-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

</dd> <dt>

<span data-ttu-id="fee51-128">**operator const D3D12 \_ 資源 \_ 屏障& () const**</span><span class="sxs-lookup"><span data-stu-id="fee51-128">**operator const D3D12\_RESOURCE\_BARRIER&() const**</span></span>
</dt> <dd>

<span data-ttu-id="fee51-129">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="fee51-129">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fee51-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="fee51-130">Requirements</span></span>



| <span data-ttu-id="fee51-131">需求</span><span class="sxs-lookup"><span data-stu-id="fee51-131">Requirement</span></span> | <span data-ttu-id="fee51-132">值</span><span class="sxs-lookup"><span data-stu-id="fee51-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fee51-133">標頭</span><span class="sxs-lookup"><span data-stu-id="fee51-133">Header</span></span><br/> | <dl> <span data-ttu-id="fee51-134"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="fee51-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fee51-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fee51-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fee51-136">**D3D12 \_ 資源 \_ 屏障**</span><span class="sxs-lookup"><span data-stu-id="fee51-136">**D3D12\_RESOURCE\_BARRIER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[<span data-ttu-id="fee51-137">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="fee51-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





