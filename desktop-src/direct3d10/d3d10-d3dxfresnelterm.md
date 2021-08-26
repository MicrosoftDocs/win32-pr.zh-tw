---
description: D3DXFresnelTerm 函式 (D3DX10Math) -計算 Fresnel 字詞。
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: 'D3DXFresnelTerm 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 862c83fd20e7646defbbaa7b82ad43ce0a384c1dd460d182af60bf8a5b23d88e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028708"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a>D3DXFresnelTerm 函式 (D3DX10Math) 

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
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
