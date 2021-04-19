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
# <a name="cd3dx12_heap_desc-structure"></a>CD3DX12 \_ 堆積 \_ DESC 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 堆積 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) 結構。

## <a name="syntax"></a>語法


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



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 堆積 \_ DESC ()**
</dt> <dd>

建立 CD3DX12 堆積 DESC 的新、未初始化的 \_ 實例 \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ 堆積 \_ desc (const D3D12 \_ 堆積 \_ desc &o)**
</dt> <dd>

建立 CD3DX12 堆積 desc 的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ 堆積 \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 堆積 \_ DESC (UINT64 大小，D3D12 \_ 堆積 \_ 屬性屬性，UINT64 對齊 = 0，D3D12 \_ 堆積 \_ 旗標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無)**
</dt> <dd>

建立 CD3DX12 堆積 DESC 的新實例 \_ \_ ，並初始化下列參數：

UINT64 大小

[**D3D12 \_堆積 \_ 屬性**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) 屬性

 (opt) UINT64 對齊 = 0

 (opt) [**D3D12 \_ 堆積 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) 標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無

</dd> <dt>

**CD3DX12 \_ 堆積 \_ DESC (UINT64 大小，D3D12 \_ 堆積 \_ 類型類型，UINT64 對齊 = 0，D3D12 \_ 堆積 \_ 旗標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無)**
</dt> <dd>

建立 CD3DX12 堆積 DESC 的新實例 \_ \_ ，並初始化下列參數：

UINT64 大小

[**D3D12 \_堆積 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) 類型

 (opt) UINT64 對齊 = 0

 (opt) [**D3D12 \_ 堆積 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) 標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無

</dd> <dt>

**CD3DX12 \_ 堆積 \_ DESC (UINT64 大小、D3D12 \_ CPU \_ 頁面 \_ 屬性 cpuPageProperty、D3D12 \_ 記憶體 \_ 集區 MEMORYPOOLPREFERENCE、UINT64 對齊 = 0、D3D12 \_ 堆積 \_ 旗標 = D3D12 \_ 堆積旗標 \_ \_ 無)**
</dt> <dd>

建立 CD3DX12 堆積 DESC 的新實例 \_ \_ ，並初始化下列參數：

UINT64 大小

[**D3D12 \_CPU \_ 頁面 \_ 屬性**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_記憶體 \_ 集**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) 區 memoryPoolPreference

 (opt) UINT64 對齊 = 0

 (opt) [**D3D12 \_ 堆積 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) 標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無

</dd> <dt>

**CD3DX12 \_ 堆積 \_ DESC (const D3D12 \_ 資源 \_ 分配 \_ 資訊& resAllocInfo，D3D12 \_ 堆積 \_ 屬性屬性，D3D12 \_ 堆積 \_ 旗標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無)**
</dt> <dd>

建立 CD3DX12 堆積 DESC 的新實例 \_ \_ ，並初始化下列參數：

[**D3D12 \_資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_堆積 \_ 屬性**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) 屬性

 (opt) [**D3D12 \_ 堆積 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) 標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無

</dd> <dt>

**CD3DX12 \_ 堆積 \_ DESC (const D3D12 \_ 資源 \_ 分配 \_ 資訊& resAllocInfo、D3D12 \_ 堆積 \_ 類型類型、D3D12 \_ 堆積 \_ 旗標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無)**
</dt> <dd>

建立 CD3DX12 堆積 DESC 的新實例 \_ \_ ，並初始化下列參數：

[**D3D12 \_資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_堆積 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) 類型

 (opt) [**D3D12 \_ 堆積 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) 標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無

</dd> <dt>

**CD3DX12 \_ 堆積 \_ DESC (const D3D12 \_ 資源 \_ 分配 \_ 資訊& resAllocInfo、D3D12 \_ CPU \_ 頁面 \_ 屬性 CPUPAGEPROPERTY、D3D12 \_ 記憶體 \_ 集區 memoryPoolPreference、D3D12 \_ 堆積 \_ 旗標 = D3D12 \_ 堆積旗標 \_ \_ 無)**
</dt> <dd>

建立 CD3DX12 堆積 DESC 的新實例 \_ \_ ，並初始化下列參數：

[**D3D12 \_資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_CPU \_ 頁面 \_ 屬性**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_記憶體 \_ 集**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) 區 memoryPoolPreference

 (opt) [**D3D12 \_ 堆積 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) 標旗標 = D3D12 \_ 堆積 \_ 旗標 \_ 無

</dd> <dt>

**運算子 const D3D12 \_ 堆積 \_ DESC& () const**
</dt> <dd>

針對 CD3DX12 \_ 堆積 DESC 結構類型定義 & 的傳址運算子 \_ 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 堆積 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





