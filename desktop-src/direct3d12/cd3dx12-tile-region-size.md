---
title: 'CD3DX12_TILE_REGION_SIZE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 圖格 \_ 區域 \_ 大小結構。
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- CD3DX12_TILE_REGION_SIZE 結構
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998997"
---
# <a name="cd3dx12_tile_region_size-structure"></a>CD3DX12 \_ 圖格 \_ 區域 \_ 大小結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 圖格 \_ 區域 \_ 大小**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 圖格 \_ 區域 \_ 大小 ()**
</dt> <dd>

建立 CD3DX12 圖格區域大小的新、未初始化的實例 \_ \_ \_ 。

</dd> <dt>

**明確的 CD3DX12 \_ 圖格 \_ 區域 \_ 大小 (const D3D12 \_ 磚 \_ 區域 \_ 大小 &o)**
</dt> <dd>

建立 CD3DX12 \_ 圖 \_ 格區域大小的新實例 \_ ，並以另一個 [**D3D12 \_ 磚 \_ 區域 \_ 大小**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 圖格 \_ 區域 \_ 大小 (UINT NumTiles、BOOL useBox、UINT width、UINT16 height、uint16 depth)**
</dt> <dd>

建立 CD3DX12 圖格區域大小的新實例 \_ \_ ，並 \_ 初始化下列參數：

UINT numTiles

BOOL useBox

UINT 寬度

UINT16 高度

UINT16 深度

</dd> <dt>

**運算子 const D3D12 \_ 圖格 \_ 區域 \_ 大小& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 圖格 \_ 區域 \_ 大小**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





