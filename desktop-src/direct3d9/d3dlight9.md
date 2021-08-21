---
description: 定義一組光源屬性。
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: 'D3DLIGHT9 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e38cd5b6cfaba4822ddecf121aa2b03c86e2a3a899e464df18bfa473322f41f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804835"
---
# <a name="d3dlight9-structure"></a>D3DLIGHT9 結構

定義一組光源屬性。

## <a name="syntax"></a>語法


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a>成員

<dl> <dt>

**類型**
</dt> <dd>

類型： **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**

</dd> <dd>

燈光來源的類型。 這個值是 [**D3DLIGHTTYPE**](./d3dlighttype.md) 列舉型別的其中一個成員。

</dd> <dt>

**擴散**
</dt> <dd>

類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

光線發出的擴散色彩。 此成員是 [**D3DCOLORVALUE**](d3dcolorvalue.md) 結構。

</dd> <dt>

**反射**
</dt> <dd>

類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

光線發出的反射色彩。 此成員是 [**D3DCOLORVALUE**](d3dcolorvalue.md) 結構。

</dd> <dt>

**環境**
</dt> <dd>

類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

光線發出的環境色彩。 此成員是 [**D3DCOLORVALUE**](d3dcolorvalue.md) 結構。

</dd> <dt>

**位置**
</dt> <dd>

類型： **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

光線在世界空間中的位置，由 [**D3DVECTOR**](d3dvector.md) 結構指定。 這個成員沒有方向性光源的意義，而且在這種情況下會被忽略。

</dd> <dt>

[方向]
</dt> <dd>

類型： **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

光線指向世界空間的方向，由 [**D3DVECTOR**](d3dvector.md) 結構指定。 這個成員只有方向和聚光燈的意義。 此向量不需要正規化，但長度應為非零長度。

</dd> <dt>

**範圍**
</dt> <dd>

類型： **float**

</dd> <dd>

光沒有任何作用的距離。 這個成員允許的最大值是 FLT MAX 的平方根 \_ 。 此成員不會影響方向性光源。

</dd> <dt>

**衰減**
</dt> <dd>

類型： **float**

</dd> <dd>

專注的內部錐形之間的照明減少 (Theta) 和外部錐形的外緣 (Phi) 指定的角度。

對光源的衰減效果很微妙。 此外，藉由塑造衰減曲線，會造成較小的效能負面影響。 基於這些理由，大部分的開發人員都會將此值設定為1.0。

</dd> <dt>

**Attenuation0**
</dt> <dd>

類型： **float**

</dd> <dd>

指定光線濃度如何隨著距離變更的值。 方向光線會忽略衰減值。 此成員代表衰減常數。 如需衰減的詳細資訊，請參閱 [ (Direct3D 9) 的淺色屬性 ](light-properties.md)。 此成員的有效值範圍從0.0 到無限大。 若為非方向光源，則所有三個衰減值都不應同時設定為0.0。

</dd> <dt>

**Attenuation1**
</dt> <dd>

類型： **float**

</dd> <dd>

指定光線濃度如何隨著距離變更的值。 方向光線會忽略衰減值。 此成員代表衰減常數。 如需衰減的詳細資訊，請參閱 [ (Direct3D 9) 的淺色屬性 ](light-properties.md)。 此成員的有效值範圍從0.0 到無限大。 若為非方向光源，則所有三個衰減值都不應同時設定為0.0。

</dd> <dt>

**Attenuation2**
</dt> <dd>

類型： **float**

</dd> <dd>

指定光線濃度如何隨著距離變更的值。 方向光線會忽略衰減值。 此成員代表衰減常數。 如需衰減的詳細資訊，請參閱 [ (Direct3D 9) 的淺色屬性 ](light-properties.md)。 此成員的有效值範圍從0.0 到無限大。 若為非方向光源，則所有三個衰減值都不應同時設定為0.0。

</dd> <dt>

**Θ**
</dt> <dd>

類型： **float**

</dd> <dd>

焦點的內部錐形角度（以弧度為單位），也就是完全發亮的聚焦錐形。 這個值必須介於0到 Phi 指定的值之間。

</dd> <dt>

**披**
</dt> <dd>

類型： **float**

</dd> <dd>

角度，以弧度為單位，定義焦點外部錐形的外緣。 焦點以外的點不會發亮。 這個值必須介於0和 pi 之間。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[**SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
