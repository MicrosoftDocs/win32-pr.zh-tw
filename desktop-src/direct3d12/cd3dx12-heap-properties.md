---
title: 'CD3DX12_HEAP_PROPERTIES 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 堆積 \_ 屬性結構。
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- CD3DX12_HEAP_PROPERTIES 結構
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_PROPERTIES
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc5f5cee6bf70aad064396589aad8a483f2c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997240"
---
# <a name="cd3dx12_heap_properties-structure"></a><span data-ttu-id="c87c5-104">CD3DX12 \_ 堆積 \_ 屬性結構</span><span class="sxs-lookup"><span data-stu-id="c87c5-104">CD3DX12\_HEAP\_PROPERTIES structure</span></span>

<span data-ttu-id="c87c5-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 堆積 \_ 屬性**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) 結構。</span><span class="sxs-lookup"><span data-stu-id="c87c5-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c87c5-106">語法</span><span class="sxs-lookup"><span data-stu-id="c87c5-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_PROPERTIES  : public D3D12_HEAP_PROPERTIES{
       CD3DX12_HEAP_PROPERTIES();
       explicit CD3DX12_HEAP_PROPERTIES(const D3D12_HEAP_PROPERTIES &o);
       CD3DX12_HEAP_PROPERTIES(D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1);
       explicit CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1);
       operator const D3D12_HEAP_PROPERTIES&() const;
  bool inline operator==( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
  bool inline operator!=( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
};
```



## <a name="members"></a><span data-ttu-id="c87c5-107">成員</span><span class="sxs-lookup"><span data-stu-id="c87c5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c87c5-108">**CD3DX12 \_ 堆積 \_ 屬性 ()**</span><span class="sxs-lookup"><span data-stu-id="c87c5-108">**CD3DX12\_HEAP\_PROPERTIES()**</span></span>
</dt> <dd>

<span data-ttu-id="c87c5-109">建立 CD3DX12 堆積屬性的新、未初始化的 \_ 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c87c5-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_PROPERTIES.</span></span>

</dd> <dt>

<span data-ttu-id="c87c5-110">**明確的 CD3DX12 \_ 堆積 \_ 屬性 (const D3D12 \_ 堆積 \_ 屬性 &o)**</span><span class="sxs-lookup"><span data-stu-id="c87c5-110">**explicit CD3DX12\_HEAP\_PROPERTIES(const D3D12\_HEAP\_PROPERTIES &o)**</span></span>
</dt> <dd>

<span data-ttu-id="c87c5-111">建立 CD3DX12 堆積屬性的新實例 \_ \_ ，並以另一個 [**D3D12 \_ 堆積 \_ 屬性**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="c87c5-111">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initialized with the contents of another [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c87c5-112">**CD3DX12 \_ 堆積 \_ 屬性 (D3D12 \_ CPU \_ 頁面 \_ 屬性 cpuPageProperty、D3D12 \_ 記憶體 \_ 集區 MEMORYPOOLPREFERENCE、UINT creationNodeMask = 1、UINT nodeMask = 1)**</span><span class="sxs-lookup"><span data-stu-id="c87c5-112">**CD3DX12\_HEAP\_PROPERTIES(D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="c87c5-113">建立 CD3DX12 堆積屬性的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="c87c5-113">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="c87c5-114">[**D3D12 \_CPU \_ 頁面 \_ 屬性**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="c87c5-114">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="c87c5-115">[**D3D12 \_記憶體 \_ 集**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) 區 memoryPoolPreference</span><span class="sxs-lookup"><span data-stu-id="c87c5-115">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="c87c5-116"> (opt) UINT creationNodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="c87c5-116">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="c87c5-117"> (opt) UINT nodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="c87c5-117">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="c87c5-118">**明確的 CD3DX12 \_ 堆積 \_ 屬性 (D3D12 \_ 堆積 \_ 類型 type、uint CREATIONNODEMASK = 1、uint nodeMask = 1)**</span><span class="sxs-lookup"><span data-stu-id="c87c5-118">**explicit CD3DX12\_HEAP\_PROPERTIES(D3D12\_HEAP\_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="c87c5-119">建立 CD3DX12 堆積屬性的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="c87c5-119">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="c87c5-120">[**D3D12 \_堆積 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) 類型</span><span class="sxs-lookup"><span data-stu-id="c87c5-120">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="c87c5-121"> (opt) UINT creationNodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="c87c5-121">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="c87c5-122"> (opt) UINT nodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="c87c5-122">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="c87c5-123">**運算子 const D3D12 \_ 堆積 \_ 屬性& () const**</span><span class="sxs-lookup"><span data-stu-id="c87c5-123">**operator const D3D12\_HEAP\_PROPERTIES&() const**</span></span>
</dt> <dd>

<span data-ttu-id="c87c5-124">針對父結構類型定義 & 的傳址運算子。</span><span class="sxs-lookup"><span data-stu-id="c87c5-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="c87c5-125">**內嵌運算子 = = ( const D3D12 \_ 堆積 \_ 屬性& l，const D3D12 \_ 堆積 \_ 屬性& r )**</span><span class="sxs-lookup"><span data-stu-id="c87c5-125">**inline operator==( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="c87c5-126">\_ \_ 根據所有成員欄位的相等，測試指定的 D3D12 堆積屬性實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="c87c5-126">Tests for equality between the specified D3D12\_HEAP\_PROPERTIES instances, based on equality of all member fields.</span></span>

</dd> <dt>

<span data-ttu-id="c87c5-127">**內嵌運算子！ = ( 常數 D3D12 \_ 堆積 \_ 屬性& l，const D3D12 \_ 堆積 \_ 屬性& r )**</span><span class="sxs-lookup"><span data-stu-id="c87c5-127">**inline operator!=( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="c87c5-128">測試指定的 D3D12 \_ 堆積屬性實例是否不相等 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c87c5-128">Tests for inequality between the specified D3D12\_HEAP\_PROPERTIES instances.</span></span> <span data-ttu-id="c87c5-129">採用 **operator = =** 值的反向實作為實值。</span><span class="sxs-lookup"><span data-stu-id="c87c5-129">Implemented by taking the inverse of the **operator==** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c87c5-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="c87c5-130">Requirements</span></span>



| <span data-ttu-id="c87c5-131">需求</span><span class="sxs-lookup"><span data-stu-id="c87c5-131">Requirement</span></span> | <span data-ttu-id="c87c5-132">值</span><span class="sxs-lookup"><span data-stu-id="c87c5-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c87c5-133">標頭</span><span class="sxs-lookup"><span data-stu-id="c87c5-133">Header</span></span><br/> | <dl> <span data-ttu-id="c87c5-134"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="c87c5-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c87c5-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c87c5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c87c5-136">**D3D12 \_ 堆積 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="c87c5-136">**D3D12\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[<span data-ttu-id="c87c5-137">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="c87c5-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





