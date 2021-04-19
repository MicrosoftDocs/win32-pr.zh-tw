---
description: 這些旗標是用來控制 D3DX10ComputeNormalMap 產生一般對應的方式。 這些旗標的任意數目可能會以任何組合方式組合。
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: 'D3DX10_NORMALMAP_FLAG 列舉 (D3DX10Tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985532"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a>D3DX10 \_ NORMALMAP \_ 旗標列舉

這些旗標是用來控制 [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) 產生一般對應的方式。 這些旗標的任意數目可能會以任何組合方式組合。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10 \_ NORMALMAP \_ 鏡像 \_ U**
</dt> <dd>

指出 U 軸上材質邊緣的圖元應鏡像，而非 wraped。

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10 \_ NORMALMAP \_ 鏡像 \_ V**
</dt> <dd>

指出 V 軸上材質邊緣的圖元應鏡像，而非 wraped。

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3DX10 \_ NORMALMAP \_ 鏡像**
</dt> <dd>

與 D3DX10 \_ NORMALMAP \_ 鏡像 \_ U \| D3DX10 \_ NORMALMAP \_ 鏡像 V 相同 \_ 。

</dd> <dt>

<span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10 \_ NORMALMAP \_ INVERTSIGN**
</dt> <dd>

反轉每個標準的方向。

</dd> <dt>

<span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10 \_ NORMALMAP \_ COMPUTE \_ 遮蔽**
</dt> <dd>

計算每個圖元的遮蔽詞彙，然後將其編碼成 Alpha。 Alpha 為1表示圖元不會以任何方式隱藏，而 Alpha 為0表示圖元完全隱藏。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




