---
title: 'CD3DX12_TILE_SHAPE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 圖格 \_ 圖形結構。
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- CD3DX12_TILE_SHAPE 結構
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998a14e1bd4898d83d049ea50bc056abaeb68544
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992295"
---
# <a name="cd3dx12_tile_shape-structure"></a>CD3DX12 \_ 圖格 \_ 圖形結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 圖格 \_ 圖形**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 圖格 \_ 圖形 ()**
</dt> <dd>

建立新的、未初始化的 CD3DX12 圖格 \_ \_ 圖形實例。

</dd> <dt>

**明確的 CD3DX12 \_ 圖格 \_ 圖形 (const D3D12 \_ 磚 \_ 圖形 &o)**
</dt> <dd>

建立 CD3DX12 \_ 圖格圖形的新實例 \_ ，並使用另一個 [**D3D12 \_ 磚 \_ 圖形**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 圖格 \_ 圖形 (uint WIDTHINTEXELS、uint HEIGHTINTEXELS、uint depthInTexels)**
</dt> <dd>

建立 CD3DX12 圖格圖形的新 \_ 實例 \_ ，並初始化下列參數：

UINT widthInTexels

UINT heightInTexels

UINT depthInTexels

</dd> <dt>

**operator const D3D12 \_ 圖格 \_ 圖形& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 圖格 \_ 圖形**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





