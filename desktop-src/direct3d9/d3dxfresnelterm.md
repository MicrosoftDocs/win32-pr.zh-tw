---
description: D3DXFresnelTerm 函式 (D3dx9math) -計算 Fresnel 字詞。
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: 'D3DXFresnelTerm 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5472f9839928fd3b4c1830bc309c7f610d487864
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114476"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a>D3DXFresnelTerm 函式 (D3dx9math) 

計算 Fresnel 字詞。

## <a name="syntax"></a>語法


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CosTheta* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

值長度必須介於 0 到 1 之間。

</dd> <dt>

*RefractionIndex* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

材質的折射索引。 值必須大於1。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

此函數會傳回 unpolarized light 的 Fresnel 字詞。 CosTheta 是事件角度的余弦值。

## <a name="remarks"></a>備註

若要尋找 Fresnel 字詞 (F) ：

如果是發生的角度，B 是折射的角度，則


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



然後，使用三角函數和簡化進行擴充，您會得到：


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
