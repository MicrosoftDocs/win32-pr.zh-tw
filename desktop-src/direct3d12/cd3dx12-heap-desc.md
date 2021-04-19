---
title: 'CD3DX12_HEAP_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 堆積 \_ DESC 結構。
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- CD3DX12_HEAP_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b2537d2571355f26c46f03aed3489fb2b6069
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985868"
---
# <a name="cd3dx12_heap_desc-structure"></a><span data-ttu-id="31cd1-104">CD3DX12 \_ 堆積 \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="31cd1-104">CD3DX12\_HEAP\_DESC structure</span></span>

<span data-ttu-id="31cd1-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 堆積 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="31cd1-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="31cd1-106">語法</span><span class="sxs-lookup"><span data-stu-id="31cd1-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_DESC  : public D3D12_HEAP_DESC{
   CD3DX12_HEAP_DESC();
   explicit CD3DX12_HEAP_DESC(const D3D12_HEAP_DESC &o);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_PROPERTIES properties, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_TYPE type, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_PROPERTIES properties, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_TYPE type, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   operator const D3D12_HEAP_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="31cd1-107">成員</span><span class="sxs-lookup"><span data-stu-id="31cd1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="31cd1-108">**CD3DX12 \_ 堆積 \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="31cd1-108">**CD3DX12\_HEAP\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="31cd1-109">建立 CD3DX12 堆積 DESC 的新、未初始化的 \_ 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="31cd1-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="31cd1-110">**明確的 CD3DX12 \_ 堆積 \_ desc (const D3D12 \_ 堆積 \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="31cd1-110">**explicit CD3DX12\_HEAP\_DESC(const D3D12\_HEAP\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="31cd1-111">建立 CD3DX12 堆積 desc 的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ 堆積 \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="31cd1-111">Creates a new instance of a CD3DX12\_HEAP\_DESC, initialized with the contents of another [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="31cd1-112">**CD3DX12 \_ 堆積 \_ DESC (UINT64 大小，D3D12 \_ 堆積 \_ 屬性屬性，UINT64 對齊 = 0，D3D12 \_ 堆積 \_ 旗標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="31cd1-112">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_PROPERTIES properties, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="31cd1-113">建立 CD3DX12 堆積 DESC 的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="31cd1-113">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="31cd1-114">UINT64 大小</span><span class="sxs-lookup"><span data-stu-id="31cd1-114">UINT64 size</span></span>

<span data-ttu-id="31cd1-115">[**D3D12 \_堆積 \_ 屬性**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) 屬性</span><span class="sxs-lookup"><span data-stu-id="31cd1-115">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="31cd1-116"> (opt) UINT64 對齊 = 0</span><span class="sxs-lookup"><span data-stu-id="31cd1-116">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="31cd1-117"> (opt) [**D3D12 \_ 堆積 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) 標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無</span><span class="sxs-lookup"><span data-stu-id="31cd1-117">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="31cd1-118">**CD3DX12 \_ 堆積 \_ DESC (UINT64 大小，D3D12 \_ 堆積 \_ 類型類型，UINT64 對齊 = 0，D3D12 \_ 堆積 \_ 旗標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="31cd1-118">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_TYPE type, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="31cd1-119">建立 CD3DX12 堆積 DESC 的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="31cd1-119">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="31cd1-120">UINT64 大小</span><span class="sxs-lookup"><span data-stu-id="31cd1-120">UINT64 size</span></span>

<span data-ttu-id="31cd1-121">[**D3D12 \_堆積 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) 類型</span><span class="sxs-lookup"><span data-stu-id="31cd1-121">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="31cd1-122"> (opt) UINT64 對齊 = 0</span><span class="sxs-lookup"><span data-stu-id="31cd1-122">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="31cd1-123"> (opt) [**D3D12 \_ 堆積 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) 標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無</span><span class="sxs-lookup"><span data-stu-id="31cd1-123">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="31cd1-124">**CD3DX12 \_ 堆積 \_ DESC (UINT64 大小、D3D12 \_ CPU \_ 頁面 \_ 屬性 cpuPageProperty、D3D12 \_ 記憶體 \_ 集區 MEMORYPOOLPREFERENCE、UINT64 對齊 = 0、D3D12 \_ 堆積 \_ 旗標 = D3D12 \_ 堆積旗標 \_ \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="31cd1-124">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="31cd1-125">建立 CD3DX12 堆積 DESC 的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="31cd1-125">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="31cd1-126">UINT64 大小</span><span class="sxs-lookup"><span data-stu-id="31cd1-126">UINT64 size</span></span>

<span data-ttu-id="31cd1-127">[**D3D12 \_CPU \_ 頁面 \_ 屬性**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="31cd1-127">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="31cd1-128">[**D3D12 \_記憶體 \_ 集**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) 區 memoryPoolPreference</span><span class="sxs-lookup"><span data-stu-id="31cd1-128">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="31cd1-129"> (opt) UINT64 對齊 = 0</span><span class="sxs-lookup"><span data-stu-id="31cd1-129">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="31cd1-130"> (opt) [**D3D12 \_ 堆積 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) 標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無</span><span class="sxs-lookup"><span data-stu-id="31cd1-130">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="31cd1-131">**CD3DX12 \_ 堆積 \_ DESC (const D3D12 \_ 資源 \_ 分配 \_ 資訊& resAllocInfo，D3D12 \_ 堆積 \_ 屬性屬性，D3D12 \_ 堆積 \_ 旗標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="31cd1-131">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_PROPERTIES properties, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="31cd1-132">建立 CD3DX12 堆積 DESC 的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="31cd1-132">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="31cd1-133">[**D3D12 \_資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="31cd1-133">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="31cd1-134">[**D3D12 \_堆積 \_ 屬性**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) 屬性</span><span class="sxs-lookup"><span data-stu-id="31cd1-134">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="31cd1-135"> (opt) [**D3D12 \_ 堆積 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) 標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無</span><span class="sxs-lookup"><span data-stu-id="31cd1-135">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="31cd1-136">**CD3DX12 \_ 堆積 \_ DESC (const D3D12 \_ 資源 \_ 分配 \_ 資訊& resAllocInfo、D3D12 \_ 堆積 \_ 類型類型、D3D12 \_ 堆積 \_ 旗標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="31cd1-136">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_TYPE type, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="31cd1-137">建立 CD3DX12 堆積 DESC 的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="31cd1-137">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="31cd1-138">[**D3D12 \_資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="31cd1-138">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="31cd1-139">[**D3D12 \_堆積 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) 類型</span><span class="sxs-lookup"><span data-stu-id="31cd1-139">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="31cd1-140"> (opt) [**D3D12 \_ 堆積 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) 標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無</span><span class="sxs-lookup"><span data-stu-id="31cd1-140">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="31cd1-141">**CD3DX12 \_ 堆積 \_ DESC (const D3D12 \_ 資源 \_ 分配 \_ 資訊& resAllocInfo、D3D12 \_ CPU \_ 頁面 \_ 屬性 CPUPAGEPROPERTY、D3D12 \_ 記憶體 \_ 集區 memoryPoolPreference、D3D12 \_ 堆積 \_ 旗標 = D3D12 \_ 堆積旗標 \_ \_ 無)**</span><span class="sxs-lookup"><span data-stu-id="31cd1-141">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="31cd1-142">建立 CD3DX12 堆積 DESC 的新實例 \_ \_ ，並初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="31cd1-142">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="31cd1-143">[**D3D12 \_資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="31cd1-143">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="31cd1-144">[**D3D12 \_CPU \_ 頁面 \_ 屬性**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="31cd1-144">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="31cd1-145">[**D3D12 \_記憶體 \_ 集**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) 區 memoryPoolPreference</span><span class="sxs-lookup"><span data-stu-id="31cd1-145">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="31cd1-146"> (opt) [**D3D12 \_ 堆積 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) 標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無</span><span class="sxs-lookup"><span data-stu-id="31cd1-146">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="31cd1-147">**運算子 const D3D12 \_ 堆積 \_ DESC& () const**</span><span class="sxs-lookup"><span data-stu-id="31cd1-147">**operator const D3D12\_HEAP\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="31cd1-148">針對 CD3DX12 \_ 堆積 DESC 結構類型定義 & 的傳址運算子 \_ 。</span><span class="sxs-lookup"><span data-stu-id="31cd1-148">Defines the & pass-by-reference operator for the CD3DX12\_HEAP\_DESC structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31cd1-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="31cd1-149">Requirements</span></span>



| <span data-ttu-id="31cd1-150">需求</span><span class="sxs-lookup"><span data-stu-id="31cd1-150">Requirement</span></span> | <span data-ttu-id="31cd1-151">值</span><span class="sxs-lookup"><span data-stu-id="31cd1-151">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="31cd1-152">標頭</span><span class="sxs-lookup"><span data-stu-id="31cd1-152">Header</span></span><br/> | <dl> <span data-ttu-id="31cd1-153"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="31cd1-153"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31cd1-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31cd1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31cd1-155">**D3D12 \_ 堆積 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="31cd1-155">**D3D12\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[<span data-ttu-id="31cd1-156">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="31cd1-156">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





