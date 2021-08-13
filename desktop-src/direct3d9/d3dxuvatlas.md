---
description: 定義在將材質調整為曲線表面時，執行測式距離計算的選項。 使用此旗標可在計算紋理塔時，選擇高品質與快速計算。
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: 'D3DXU加值稅LAS 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 1edcf2b1cbe2363f805bee1f5eb67f5558702ea9e163a865e1a6c51d6f5ed6ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523834"
---
# <a name="d3dxuvatlas-enumeration"></a>D3DXU加值稅LAS 列舉

定義在將材質調整為曲線表面時，執行測式距離計算的選項。 使用此旗標可在計算紋理塔時，選擇高品質與快速計算。

## <a name="syntax"></a>Syntax


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXU加值稅LAS \_ 預設值**
</dt> <dd>

具有超過25k 臉部的網格將會套用 fast geodasic 距離方法，而小於25k 臉部的網格會改為套用較高品質的地線距離方法。

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXU加值稅LAS \_ 地線 \_ FAST**
</dt> <dd>

使用近似值來改善圖表速度，代價是新增的延展或更多圖表是網格的輸出。

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXU加值稅LAS \_ 地線 \_ 品質**
</dt> <dd>

提供更高品質的圖表，但需要的時間和記憶體比快得多。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




