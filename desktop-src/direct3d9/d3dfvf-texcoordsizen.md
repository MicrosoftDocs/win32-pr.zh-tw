---
description: 會建立用來識別 FVF 描述內材質座標格式的位模式。 您可以使用 OR 運算子，將這些宏的結果結合在 FVF 描述內。
ms.assetid: c3076d7c-7935-40ee-b513-7ff6551a535f
title: 'D3DFVF_TEXCOORDSIZEN (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFVF_TEXCOORDSIZEN
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f5a39827f94f0415d6235797489f6e18c5fb515a5e5c36c0f26153b7ba8303ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988908"
---
# <a name="d3dfvf_texcoordsizen"></a>D3DFVF \_ TEXCOORDSIZEN

會建立用來識別 FVF 描述內材質座標格式的位模式。 您可以使用 OR 運算子，將這些宏的結果結合在 FVF 描述內。

``` syntax
#define D3DFVF_TEXCOORDSIZEN(CoordIndex) 
#define D3DFVF_TEXCOORDSIZE1(CoordIndex) (D3DFVF_TEXTUREFORMAT1 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE2(CoordIndex) (D3DFVF_TEXTUREFORMAT2) 
#define D3DFVF_TEXCOORDSIZE3(CoordIndex) (D3DFVF_TEXTUREFORMAT3 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE4(CoordIndex) (D3DFVF_TEXTUREFORMAT4 << (CoordIndex*2 + 16))
```

## <a name="parameters"></a>參數



| 參數                                                                                                    | 描述                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>CoordIndex<br/> | 值，這個值會識別材質座標大小 (1-、2-、3或 4Dimensional) 套用的材質座標集合。 <br/> |



 

## <a name="remarks"></a>備註

**D3DFVF \_ TEXCOORDSIZEN** 宏會使用下列常數。


```C++
#define D3DFVF_TEXTUREFORMAT1 3 // one floating point value
#define D3DFVF_TEXTUREFORMAT2 0 // two floating point values
#define D3DFVF_TEXTUREFORMAT3 1 // three floating point values
#define D3DFVF_TEXTUREFORMAT4 2 // four floating point values
```



下列 FVF 描述會識別具有位置的頂點格式;一般;擴散和反射色彩;以及兩組材質座標。 第一組紋理座標包含單一元素，而第二組則包含兩個元素：


```C++
DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE |
              D3DFVF_SPECULAR | D3DFVF_TEX2 |
              D3DFVF_TEXCOORDSIZE1(0) |  // Uses 1D texture coordinates for
                                         // texture coordinate set 1 (index 0).
              D3DFVF_TEXCOORDSIZE2(1);   // And 2D texture coordinates for 
                                         // texture coordinate set 2 (index 1).
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DFVF](d3dfvf.md)
</dt> </dl>

 

 




