---
description: D3DXCOLOR 結構 (D3dx9math) -描述色彩值。
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: 'D3DXCOLOR 結構 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 58b02abc49b695169674a2579b73dc2359801a73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115926"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a>D3DXCOLOR 結構 (D3dx9math .h) 

描述色彩值。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a>成員

<dl> <dt>

**r**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

色彩的紅色元件。

</dd> <dt>

**G**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

色彩的綠色元件。

</dd> <dt>

**b**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

色彩的藍色元件。

</dd> <dt>

**的**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

色彩的 Alpha 元件。

</dd> </dl>

## <a name="remarks"></a>備註

C + + 程式設計人員可以利用 [**D3DXCOLOR 擴充**](d3dxcolor-extensions.md)功能來利用運算子多載和類型轉換，以執行多載的函式，以及指派、一元和二元 (包括相等) 運算子。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
