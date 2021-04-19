---
title: 'CD3DX12_TILED_RESOURCE_COORDINATE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 並排顯示的 \_ \_ 資源 \_ 座標結構。
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- CD3DX12_TILED_RESOURCE_COORDINATE 結構
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281afeab8d1172e9cae749512612129dd001161b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993859"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a>CD3DX12 並排顯示的 \_ \_ 資源 \_ 座標結構

協助程式結構，可讓您輕鬆地初始化 D3D12 並排顯示的 [**\_ \_ 資源 \_ 座標**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 並排顯示的 \_ \_ 資源 \_ 座標 ()**
</dt> <dd>

建立新的、未初始化的實例，其為 CD3DX12 並排顯示的 \_ \_ 資源 \_ 座標。

</dd> <dt>

**明確 CD3DX12 的並排 \_ \_ 資源 \_ 座標 (const D3D12 並排顯示 \_ \_ 資源 \_ 座標 &o)**
</dt> <dd>

建立 CD3DX12 平並排資源座標的新實例 \_ \_ \_ ，並以另一個 [**D3D12 並排 \_ \_ 資源 \_ 座標**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 並排顯示 \_ \_ \_ 的資源座標 (UINT x、UINT y、UINT z、uint subresource)**
</dt> <dd>

建立 CD3DX12 平並排資源座標的新實例 \_ \_ ，並 \_ 初始化下列參數：

UINT x

UINT y

UINT z

UINT subresource

</dd> <dt>

**運算子 const D3D12 並排顯示 \_ \_ 資源 \_ 座標& () const**
</dt> <dd>

針對父結構類型定義 & 的傳址運算子。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 並排顯示的 \_ \_ 資源 \_ 座標**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





