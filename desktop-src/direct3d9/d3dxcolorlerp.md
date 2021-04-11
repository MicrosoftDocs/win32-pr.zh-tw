---
description: 使用線性插補來建立色彩值。
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: 'D3DXColorLerp 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854011"
---
# <a name="d3dxcolorlerp-function"></a>D3DXColorLerp 函式

使用線性插補來建立色彩值。

## <a name="syntax"></a>語法


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
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

*test-pc1* \[在\]
</dt> <dd>

Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***

來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。

</dd> <dt>

*pC2* \[在\]
</dt> <dd>

Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***

來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。

</dd> <dt>

 \[ 中的 s\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

以線性方式在色彩（Test-pc1 和 pC2）之間插補的參數，會將它們視為4D 向量。 的值沒有限制。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***

此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，此結構是線性插補的結果。

## <a name="remarks"></a>備註

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來， **D3DXColorLerp** 函式就可以用來做為另一個函式的參數。

此函式會將 [**D3DXCOLOR**](d3dxcolor.md) 結構的紅色、綠色、藍色和 Alpha 元件，插補兩個色彩，如下列範例所示。


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



如果您在色彩 A 和 B 之間以線性方式插即插，而 s 為0，則產生的色彩為。如果 s 是1，則產生的色彩為色彩 B。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 
