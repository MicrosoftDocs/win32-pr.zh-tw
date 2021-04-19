---
description: 調整色彩的飽和度值。
ms.assetid: 1f66c3b4-2f02-4993-80c6-c484180c2459
title: 'D3DXColorAdjustSaturation 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d9a801a8355c1a9399f9864f9b1753bbecc17b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992329"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx9mathh"></a>D3DXColorAdjustSaturation 函式 (D3dx9math) 

調整色彩的飽和度值。

## <a name="syntax"></a>語法


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***

[**D3DXCOLOR**](d3dxcolor.md)結構的指標，該結構為運算的結果。

</dd> <dt>

*電腦* \[在\]
</dt> <dd>

Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***

來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。

</dd> <dt>

 \[ 中的 s\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

飽和度值。 此參數會在轉換成灰階的色彩和原始色彩（pC）之間以線性方式進行插補。 的值沒有限制。 如果 s 為0，則傳回的色彩為灰階色彩。 如果 s 是1，則傳回的色彩會是原始色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***

此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，此結構是飽和度調整的結果。

## <a name="remarks"></a>備註

輸入 Alpha 通道會複製（未經修改）至輸出 Alpha 通道。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，此函式就可以用來做為另一個函式的參數。

此函式會在 unsaturated 色彩和色彩之間，插入 [**D3DXCOLOR**](d3dxcolor.md) 結構的紅色、綠色和藍色色彩元件，如下列範例所示。


```
    // Approximate values for each component's contribution to luminance.
    // Based upon the NTSC standard described in ITU-R Recommendation BT.709.
    FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;
    
    pOut->r = grey + s * (pC->r - grey);
```



如果 s 大於0且小於1，則會減少飽和度。 如果 s 大於1，則會增加飽和度。

灰階色彩的計算方式如下：


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorAdjustContrast**](d3dxcoloradjustcontrast.md)
</dt> </dl>

 

 
