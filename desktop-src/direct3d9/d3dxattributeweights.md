---
description: D3DXATTRIBUTEWEIGHTS 結構-指定網格權數屬性。
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: 'D3DXATTRIBUTEWEIGHTS 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fa40476bdd1f65dddf0f78b57cfca2b20ac7bd8186eaf78546ddda9b3fa8771a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096593"
---
# <a name="d3dxattributeweights-structure"></a>D3DXATTRIBUTEWEIGHTS 結構

指定網狀加權屬性。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
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

LPD3DXATTRIBUTEWEIGHTS 型別定義為 **D3DXATTRIBUTEWEIGHTS** 結構的指標。


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 
