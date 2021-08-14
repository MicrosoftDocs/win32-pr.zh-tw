---
description: 定義頂點著色器的取樣器紋理類型。
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: 'D3DSAMPLER_TEXTURE_TYPE 列舉 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 5b1755f97ad39a5924367747199cf21c1c46a209a8202cc6b38ef22c73e8ccec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408222"
---
# <a name="d3dsampler_texture_type-enumeration"></a>D3DSAMPLER \_ 紋理 \_ 類型列舉

定義頂點著色器的取樣器紋理類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ 不明**
</dt> <dd>

未初始化的值。 這個元素的值是 0 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT。

</dd> <dt>

<span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2d**
</dt> <dd>

宣告2D 材質。 此元素的值為 2 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT。

</dd> <dt>

<span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**D3DSTT \_ CUBE**
</dt> <dd>

宣告 cube 紋理。 此元素的值為 3 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT。

</dd> <dt>

<span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**D3DSTT \_ 磁片區**
</dt> <dd>

宣告磁片區材質。 此元素的值為 4 &lt; &lt; D3DSP \_ TEXTURETYPE \_ SHIFT。

</dd> <dt>

<span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




