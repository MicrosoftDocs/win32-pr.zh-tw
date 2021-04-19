---
description: 調整色彩的對比值。
ms.assetid: be49c9c7-b625-4cbc-bd63-1d5766ae2dbb
title: 'D3DXColorAdjustContrast 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6765f442b6a2550ba262073f61c876e3b3ae1fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986524"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx9mathh"></a>D3DXColorAdjustContrast 函式 (D3dx9math) 

調整色彩的對比值。

## <a name="syntax"></a>語法


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     c
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

*c* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

對比值。 此參數會以線性方式在50% 的灰色與彩色電腦之間進行插補。 C 的值沒有限制。 如果此參數為零，則傳回的色彩會是50% 灰色。 如果這個參數是1，則傳回的色彩會是原始色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***

此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，此結構是對比調整的結果。

## <a name="remarks"></a>備註

輸入 Alpha 通道會複製（未經修改）至輸出 Alpha 通道。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，此函式就可以用來做為另一個函式的參數。

此函式會將 [**D3DXCOLOR**](d3dxcolor.md) 結構的紅色、綠色和藍色色彩元件，插入50% 的灰色和指定的對比值之間，如下列範例所示。


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



如果 c 大於0且小於1，則會減少對比。 如果 c 大於1，則會增加對比。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorAdjustSaturation**](d3dxcoloradjustsaturation.md)
</dt> </dl>

 

 
