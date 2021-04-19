---
description: 將兩個色彩值加在一起，以建立新的色彩值。
ms.assetid: 7743392d-4676-4408-93e9-f92d4bf02411
title: 'D3DXColorAdd 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f326c9bec4802a9a94accc76b825cd1c6ea28fd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992330"
---
# <a name="d3dxcoloradd-function"></a>D3DXColorAdd 函式

將兩個色彩值加在一起，以建立新的色彩值。

## <a name="syntax"></a>語法


```C++
D3DXCOLOR* D3DXColorAdd(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
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

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***

此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，這是兩個色彩值的總和。

## <a name="remarks"></a>備註

此函式的傳回值與不悅中傳回的值相同。 如此一來， **D3DXColorAdd** 函式就可以用來做為另一個函式的參數。

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

[**D3DXColorSubtract**](d3dxcolorsubtract.md)
</dt> </dl>

 

 




