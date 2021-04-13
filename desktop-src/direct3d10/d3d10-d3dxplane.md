---
description: 描述平面。
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: 'D3DXPLANE 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 9949aec16e90a53e01e536255c20f442052bb98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323239"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a>D3DXPLANE 結構 (D3DX10Math .h) 

描述平面。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a>成員

<dl> <dt>

**的**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

一般平面方程式中裁剪平面的係數。 請參閱＜備註＞。

</dd> <dt>

**b**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

一般平面方程式中裁剪平面的 b 係數。 請參閱＜備註＞。

</dd> <dt>

**c**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

一般平面方程式中裁剪平面的 c 係數。 請參閱＜備註＞。

</dd> <dt>

**d**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

一般平面方程式中裁剪平面的 d 係數。 請參閱＜備註＞。

</dd> </dl>

## <a name="remarks"></a>備註

**D3DXPLANE** 結構的成員採用一般平面方程式的形式。 它們符合一般平面方程式，因此 ax + by + cz + dw = 0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
