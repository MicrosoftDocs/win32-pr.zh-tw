---
description: 定義支援的 blend 模式。
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: 'D3DBLEND 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d8d779ad714e396f9c9a82bbbc42ddd09b76e2ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946064"
---
# <a name="d3dblend-enumeration"></a>D3DBLEND 列舉

定義支援的 blend 模式。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ 零**
</dt> <dd>

Blend 因數是 (0、0、0、0) 。

</dd> <dt>

<span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ 一**
</dt> <dd>

Blend 因數是 (1，1，1，1) 。

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ SRCCOLOR**
</dt> <dd>

Blend 因數是 (Rs、Gs、Bs) 。

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND \_ INVSRCCOLOR**
</dt> <dd>

Blend 因數是 (1-Rs、1-Gs、1 Bs、1) 。

</dd> <dt>

<span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ SRCALPHA**
</dt> <dd>

Blend 因數會 (As，as 和) 。

</dd> <dt>

<span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND \_ INVSRCALPHA**
</dt> <dd>

Blend 因數是 ( 1-as，1-as，1-as，1) 。

</dd> <dt>

<span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ DESTALPHA**
</dt> <dd>

Blend 因數是<sub> (a d a d</sub> <sub>a d</sub> <sub>a d</sub> <sub>) 。</sub>

</dd> <dt>

<span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND \_ INVDESTALPHA**
</dt> <dd>

Blend 因數是 (1-A<sub>d</sub> 1<sub>-a d 1-</sub> a<sub>d</sub> 1-a<sub>d</sub>) 。

</dd> <dt>

<span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ DESTCOLOR**
</dt> <dd>

Blend 因數是 (R<sub>d</sub>、G<sub>d</sub>、B<sub>d</sub>、<sub>d</sub>) 。

</dd> <dt>

<span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ INVDESTCOLOR**
</dt> <dd>

Blend 因數是 (1-R<sub>d</sub>、1-G<sub>d</sub>、1-B<sub>d</sub>、1-A<sub>d</sub>) 。

</dd> <dt>

<span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ SRCALPHASAT**
</dt> <dd>

Blend 因數是 (f、f、f、1) ;其中 f = min (為，1-A<sub>d</sub>) 。

</dd> <dt>

<span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ BOTHSRCALPHA**
</dt> <dd>

已 **淘汰**。 從 DirectX 6 開始，您可以藉由將來源和目的地 blend 因數設定為 \_ \_ 在個別呼叫中 D3DBLEND SRCALPHA 和 D3DBLEND INVSRCALPHA 來達到相同的效果。

</dd> <dt>

<span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ BOTHINVSRCALPHA**
</dt> <dd>

已 **淘汰**。 來源 blend 因數是 (1-As，1-As，1-As，1) ，而目的地 blend 因數 (As，as，as) ;目的地 blend 選取專案會遭到覆寫。 只有 D3DRS SRCBLEND 轉譯狀態才支援這個 blend 模式 \_ 。

</dd> <dt>

<span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ BLENDFACTOR**
</dt> <dd>

框架緩衝區 blender 所使用的常數色彩混合係數。 只有 \_ 在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 **SrcBlendCaps** 或 **DestBlendCaps** 成員中設定 D3DPBLENDCAPS BLENDFACTOR 時，才支援這個 blend 模式。

</dd> <dt>

<span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND \_ INVBLENDFACTOR**
</dt> <dd>

由框架緩衝區 blender 所使用的反向常數色彩混合係數。 只有在 \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 **SrcBlendCaps** 或 **DestBlendCaps** 成員中設定 D3DPBLENDCAPS BLENDFACTOR 位時，才支援這個 blend 模式。

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**
</dt> <dd>

Blend 因數是 (PSOutColor \[ 1 \] <sub>r</sub>、PSOutColor \[ 1 \] <sub>g</sub>、PSOutColor \[ 1 \] <sub>b</sub>，而不是使用) 。 請參閱轉譯 [目標混色](#render-target-blending)。



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> 此旗標僅適用于 Direct3D 9Ex。<br/> |



 

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**
</dt> <dd>

Blend 因數是 (1-PSOutColor \[ 1 \] <sub>r</sub>、1-PSOutColor \[ 1 \] <sub>g</sub>、1-PSOutColor \[ 1 \] <sub>b</sub>，未使用) ) 。 請參閱轉譯 [目標混色](#render-target-blending)。



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> 此旗標僅適用于 Direct3D 9Ex。<br/> |



 

</dd> <dt>

<span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

在上述成員描述中，來源和目的地的 RGBA 值會以 s 和 d 注標表示。

下列轉譯狀態會使用這個列舉類型中的值：

-   D3DRS \_ DESTBLEND
-   D3DRS \_ SRCBLEND
-   D3DRS \_ DESTBLENDALPHA
-   D3DRS \_ SRCBLENDALPHA

請參閱 [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

### <a name="render-target-blending"></a>轉譯目標混色

Direct3D 9Ex 改進了文字轉譯功能。 轉譯純文字類型通常需要兩次傳遞。 為了消除第二次傳遞，可以使用圖元著色器輸出兩種色彩，我們可以呼叫 PSOutColor \[ 0 \] 和 PSOutColor \[ 1 \] 。 第一個色彩會包含標準的3個色彩元件 (RGB) 。 第二個色彩會包含3個 Alpha 元件 (第一個色彩) 的每個元件各一個元件。

這些新的混合模式僅用於第一個呈現目標上的文字轉譯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
