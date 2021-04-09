---
description: 調整色彩的飽和度值。
ms.assetid: a7ca64b4-2198-4116-8e9f-79d6c922fd09
title: 'D3DXColorAdjustSaturation 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6cfa4dd2af6e4a4ac3772af80ba11b8189405f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946200"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx10mathh"></a>D3DXColorAdjustSaturation 函式 (D3DX10Math) 

調整色彩的飽和度值。

## <a name="syntax"></a>語法


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     s
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[在\]
</dt> <dd>

類型： **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

作業結果之 [**D3DXCOLOR**](d3d10-d3dxcolor.md) 的指標。

</dd> <dt>

*電腦* \[在\]
</dt> <dd>

Type： **Const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

來源 D3DXCOLOR 結構的指標。

</dd> <dt>

 \[ 中的 s\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

飽和度值。 此參數會在轉換成灰階的色彩和原始色彩（pC）之間以線性方式進行插補。 的值沒有限制。 如果 s 為0，則傳回的色彩為灰階色彩。 如果 s 是1，則傳回的色彩會是原始色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

此函式會傳回 D3DXCOLOR 結構的指標，此結構是飽和度調整的結果。

## <a name="remarks"></a>備註

輸入 Alpha 通道會複製（未經修改）至輸出 Alpha 通道。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，此函式就可以用來做為另一個函式的參數。

此函式會在 unsaturated 色彩和色彩之間，插入 D3DXCOLOR 結構的紅色、綠色和藍色色彩元件，如下列範例所示。


```
//Approximate values for each component's contribution to luminance.
//Based upon the NTSC standard described in ITU-R Recommendation BT.709.
FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;

pOut->r = grey + s * (pC->r - grey);
```



如果 s 大於0且小於1，則會減少飽和度。 如果 s 大於1，則會增加飽和度。

灰階色彩的計算方式如下：


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b;
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

 

 
