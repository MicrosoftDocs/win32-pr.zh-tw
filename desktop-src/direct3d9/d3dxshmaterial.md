---
description: 球形調和 (SH) 預先計算 radiance transfer (PRT) 材質特性。
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: 'D3DXSHMATERIAL 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 4bfbf00c7d8654ad851ca8c691c9f028c09648219dbe76bb4ef07fe3b830e4d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849718"
---
# <a name="d3dxshmaterial-structure"></a>D3DXSHMATERIAL 結構

球形調和 (SH) 預先計算 radiance transfer (PRT) 材質特性。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a>成員

<dl> <dt>

**擴散**
</dt> <dd>

類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

介面的擴散 >albedo。 如果物件是鏡像，則會忽略此值。

</dd> <dt>

**bMirror**
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

必須設定為 **FALSE**。

</dd> <dt>

**bSubSurf**
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

設定為 **TRUE** 以啟用地下散佈;任何地下散佈的物件都不能是鏡像。

</dd> <dt>

**RelativeIndexOfRefraction**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

折射的相對索引是折射的兩個絕對索引之間的比率。 折射的索引是發生角度的正弦與折射角度正弦的比率。

</dd> <dt>

**吸收**
</dt> <dd>

類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

吸收係數是磁片區轉譯方程式的參數，可用來將參與媒體中的輕量傳播模型。

</dd> <dt>

**ReducedScattering**
</dt> <dd>

類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

減少的散佈係數是磁片區轉譯方程式的參數，可用來在參與的媒體中建立燈光傳播的模型。

</dd> </dl>

## <a name="remarks"></a>備註

非光譜場景會使用材質中的紅色色板，而非亮度值。

如需 PRT 的詳細資訊，請參閱：

-   Jensen，Henrik Wann，et al.exe. Siggraph 訴訟：地下 Light Transport 的實際模型，2001。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
