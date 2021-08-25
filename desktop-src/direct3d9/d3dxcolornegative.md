---
description: 建立色彩值的負值色彩值。
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: 'D3DXColorNegative 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c046702b81ce60f2e50817cb98c04686d9a35e964a141d88fd70dd05654e3067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069328"
---
# <a name="d3dxcolornegative-function"></a>D3DXColorNegative 函式

建立色彩值的負值色彩值。

## <a name="syntax"></a>語法


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
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

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***

此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，此結構是色彩值的負色彩值。

## <a name="remarks"></a>備註

輸入 Alpha 通道會複製（未經修改）至輸出 Alpha 通道。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來， **D3DXColorNegative** 函式就可以用來做為另一個函式的參數。

此函式會藉由從 [**D3DXCOLOR**](d3dxcolor.md) 結構的色彩元件減去1.0 來傳回負的色彩值，如下列範例所示。


```
pOut->r = 1.0f - pC->r;
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

[**D3DXColorLerp**](d3dxcolorlerp.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 




