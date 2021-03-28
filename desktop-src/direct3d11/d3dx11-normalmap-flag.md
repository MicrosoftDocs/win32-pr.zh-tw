---
title: 'D3DX11_NORMALMAP_FLAG 列舉 (D3DX11tex .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 一般對應選項。 您可以使用位 OR 運算來合併任何數目的旗標。
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- D3DX11_NORMALMAP_FLAG 列舉 Direct3D 11
- LPD3DX11_NORMALMAP_FLAG 列舉指標 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196444"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a>D3DX11 \_ NORMALMAP \_ 旗標列舉

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

一般對應選項。 您可以使用位 OR 運算來合併任何數目的旗標。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11 \_ NORMALMAP \_ 鏡像 \_ U**
</dt> <dd>

指出 U 軸上材質邊緣的圖元應鏡像，而非 wraped。

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ NORMALMAP \_ 鏡像 \_ V**
</dt> <dd>

指出 V 軸上材質邊緣的圖元應鏡像，而非 wraped。

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11 \_ NORMALMAP \_ 鏡像**
</dt> <dd>

與 D3DX11 \_ NORMALMAP \_ 鏡像 \_ U \| D3DX11 \_ NORMALMAP \_ 鏡像 V 相同 \_ 。

</dd> <dt>

<span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ NORMALMAP \_ INVERTSIGN**
</dt> <dd>

反轉每個標準的方向。

</dd> <dt>

<span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11 \_ NORMALMAP \_ COMPUTE \_ 遮蔽**
</dt> <dd>

計算每個圖元的遮蔽詞彙，然後將其編碼成 Alpha。 Alpha 為1表示圖元不會以任何方式隱藏，而 Alpha 為0表示圖元完全隱藏。

</dd> </dl>

## <a name="remarks"></a>備註

[**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md)會使用這些旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX11tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





