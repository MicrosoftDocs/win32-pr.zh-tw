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
# <a name="cd3dx12_heap_properties-structure"></a>CD3DX12 \_ 堆積 \_ 屬性結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 堆積 \_ 屬性**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) 結構。

## <a name="syntax"></a>語法


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



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 堆積 \_ 屬性 ()**
</dt> <dd>

建立 CD3DX12 堆積屬性的新、未初始化的 \_ 實例 \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ 堆積 \_ 屬性 (const D3D12 \_ 堆積 \_ 屬性 &o)**
</dt> <dd>

建立 CD3DX12 堆積屬性的新實例 \_ \_ ，並以另一個 [**D3D12 \_ 堆積 \_ 屬性**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 堆積 \_ 屬性 (D3D12 \_ CPU \_ 頁面 \_ 屬性 cpuPageProperty、D3D12 \_ 記憶體 \_ 集區 MEMORYPOOLPREFERENCE、UINT creationNodeMask = 1、UINT nodeMask = 1)**
</dt> <dd>

建立 CD3DX12 堆積屬性的新實例 \_ \_ ，並初始化下列參數：

[**D3D12 \_CPU \_ 頁面 \_ 屬性**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_記憶體 \_ 集**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) 區 memoryPoolPreference

 (opt) UINT creationNodeMask = 1

 (opt) UINT nodeMask = 1

</dd> <dt>

**明確的 CD3DX12 \_ 堆積 \_ 屬性 (D3D12 \_ 堆積 \_ 類型 type、uint CREATIONNODEMASK = 1、uint nodeMask = 1)**
</dt> <dd>

建立 CD3DX12 堆積屬性的新實例 \_ \_ ，並初始化下列參數：

[**D3D12 \_堆積 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) 類型

 (opt) UINT creationNodeMask = 1

 (opt) UINT nodeMask = 1

</dd> <dt>

**運算子 const D3D12 \_ 堆積 \_ 屬性& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> <dt>

**內嵌運算子 = = ( const D3D12 \_ 堆積 \_ 屬性& l，const D3D12 \_ 堆積 \_ 屬性& r )**
</dt> <dd>

\_ \_ 根據所有成員欄位的相等，測試指定的 D3D12 堆積屬性實例是否相等。

</dd> <dt>

**內嵌運算子！ = ( 常數 D3D12 \_ 堆積 \_ 屬性& l，const D3D12 \_ 堆積 \_ 屬性& r )**
</dt> <dd>

測試指定的 D3D12 \_ 堆積屬性實例是否不相等 \_ 。 採用 **operator = =** 值的反向實作為實值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 堆積 \_ 屬性**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





