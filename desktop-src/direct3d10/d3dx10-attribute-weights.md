---
description: D3DX10_ATTRIBUTE_WEIGHTS 結構-指定網格權數屬性。
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: 'D3DX10_ATTRIBUTE_WEIGHTS 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 1ef80db70d0562b000aa527afe17da43eee0eed5d6498e5da5b3d1ad964f5f87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282778"
---
# <a name="d3dx10_attribute_weights-structure"></a>D3DX10 \_ 屬性 \_ 加權結構

指定網狀加權屬性。

## <a name="syntax"></a>語法


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
```



## <a name="members"></a>成員

<dl> <dt>

**位置**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

位置。

</dd> <dt>

**界限**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Blend 權數。

</dd> <dt>

**Normal**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

一般。

</dd> <dt>

**擴散**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

擴散光源值。

</dd> <dt>

**反射**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

反射光源值。

</dd> <dt>

**Texcoord**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

八個材質座標。

</dd> <dt>

**正切值**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

切線。

</dd> <dt>

**Binormal**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormal.

</dd> </dl>

## <a name="remarks"></a>備註

此結構描述當您計算折迭邊緣之間的相對成本時，簡化作業將如何考慮頂點資料。 例如，如果一般欄位為0.0，則在計算折迭的錯誤時，簡化作業將會忽略頂點一般元件。 但是，如果一般欄位是1.0，簡化作業將會使用頂點一般元件。 如果正常欄位是2.0，請將錯誤的數量加倍;如果正常欄位是4.0，則會有四個錯誤數目，依此類推。

LPD3DX \_ 屬性權數 \_ 型別定義為 D3DX 屬性權數結構的指標 \_ \_ 。


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
