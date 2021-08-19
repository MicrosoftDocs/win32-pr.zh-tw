---
description: D3DXPLANE 結構 (D3dx9math) -描述平面。
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: 'D3DXPLANE 結構 (D3dx9math .h) '
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
- d3dx9math.h
ms.openlocfilehash: 5fa7e7155cdcf5c5dc1996dee1dcf02d0190e4bb91b4c319231e2f03168722c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095456"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a>D3DXPLANE 結構 (D3dx9math .h) 

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

**D3DXPLANE** 結構的成員採用一般平面方程式的形式。 它們符合一般平面 **方程式，** 因此 x + **b** y + **c** z + **d** w = 0。

C + + 程式設計人員可以利用執行多載的函式和指派、一元和二元 (（包括相等) 運算子的 [**D3DXPLANE 延伸**](d3dxplane-extensions.md) 模組）來利用運算子多載和類型轉換。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
