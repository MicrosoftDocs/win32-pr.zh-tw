---
description: 指定材質屬性。
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: 'D3DMATERIAL9 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386473"
---
# <a name="d3dmaterial9-structure"></a>D3DMATERIAL9 結構

指定材質屬性。

## <a name="syntax"></a>語法


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a>成員

<dl> <dt>

**擴散**
</dt> <dd>

類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

值，指定材質的擴散色彩。 請參閱 [**D3DCOLORVALUE**](d3dcolorvalue.md)。

</dd> <dt>

**環境**
</dt> <dd>

類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

值，指定材質的環境色彩。 請參閱 [**D3DCOLORVALUE**](d3dcolorvalue.md)。

</dd> <dt>

**反射**
</dt> <dd>

類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

值，指定材質的反射色彩。 請參閱 [**D3DCOLORVALUE**](d3dcolorvalue.md)。

</dd> <dt>

**放射**
</dt> <dd>

類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

值，指定材質的放射色彩。 請參閱 [**D3DCOLORVALUE**](d3dcolorvalue.md)。

</dd> <dt>

**電源**
</dt> <dd>

類型： **float**

</dd> <dd>

指定反射醒目顯示清晰度的浮點值。 值愈高，反白顯示的愈銳利。

</dd> </dl>

## <a name="remarks"></a>備註

若要關閉高光，請 \_ 使用 [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)將 D3DRS SPECULARENABLE 設定為 **FALSE**。 這是最快的選項，因為系統不會計算任何高光。

如需使用燈光引擎計算反射光源的詳細資訊，請參閱 [ (Direct3D 9) 的反射光源 ](specular-lighting.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DDevice9::GetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
