---
title: 'CD3DX12_RESOURCE_ALLOCATION_INFO 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 資源 \_ 分配 \_ 資訊結構。
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- CD3DX12_RESOURCE_ALLOCATION_INFO 結構
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981245"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a>CD3DX12 \_ 資源 \_ 分配 \_ 資訊結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 資源 \_ 分配 \_ 資訊 ()**
</dt> <dd>

建立 CD3DX12 \_ 資源配置資訊的新、未初始化的 \_ 實例 \_ 。

</dd> <dt>

**明確 CD3DX12 \_ 資源 \_ 分配 \_ 資訊 (const D3D12 \_ 資源 \_ 分配 \_ 資訊& o)**
</dt> <dd>

建立 CD3DX12 \_ 資源配置資訊的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ 資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 資源 \_ 分配 \_ 資訊 (UINT64 大小，uint64 對齊)**
</dt> <dd>

建立 CD3DX12 \_ 資源配置資訊的新實例 \_ ，並 \_ 初始化下列參數：

UINT64 大小

UINT64 對齊

</dd> <dt>

**運算子 const D3D12 \_ 資源 \_ 分配 \_ 資訊& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 資源 \_ 分配 \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





