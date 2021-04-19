---
title: 'CD3DX12_SUBRESOURCE_TILING 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ SUBRESOURCE \_ 平鋪結構。
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- CD3DX12_SUBRESOURCE_TILING 結構
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07677c8a8367f58016a0236cf0b5558b852bef01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992296"
---
# <a name="cd3dx12_subresource_tiling-structure"></a>CD3DX12 \_ SUBRESOURCE \_ 平鋪結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ SUBRESOURCE \_ 平鋪**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ SUBRESOURCE \_ () 平並排**
</dt> <dd>

建立新的、未初始化的 CD3DX12 \_ SUBRESOURCE \_ 平鋪實例。

</dd> <dt>

**明確的 CD3DX12 SUBRESOURCE 並排顯示 \_ \_ (const D3D12 \_ SUBRESOURCE \_ 平鋪 &o)**
</dt> <dd>

建立 CD3DX12 \_ SUBRESOURCE 平鋪的新實例 \_ ，並以另一個 [**D3D12 \_ SUBRESOURCE \_ 平鋪**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ (UINT WIDTHINTILES、uint16 HEIGHTINTILES、uint16 DEPTHINTILES、UINT startTileIndexInOverallResource)**
</dt> <dd>

建立 CD3DX12 \_ SUBRESOURCE 平鋪的新實例 \_ ，並初始化下列參數：

UINT widthInTiles

UINT16 heightInTiles

UINT16 depthInTiles

UINT startTileIndexInOverallResource

</dd> <dt>

**運算子 const D3D12 \_ SUBRESOURCE \_& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ SUBRESOURCE \_ 平鋪**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





