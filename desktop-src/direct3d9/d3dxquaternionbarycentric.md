---
description: 傳回 barycentric 座標中的四元數。
ms.assetid: 8fcd2e16-1bf1-4e18-afc9-17c92f2bbac5
title: 'D3DXQuaternionBaryCentric 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionBaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 002d235ab9957784c19b5e5a699dd87dfed74d4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981824"
---
# <a name="d3dxquaternionbarycentric-function-d3dx9mathh"></a>D3DXQuaternionBaryCentric 函式 (D3dx9math) 

傳回 barycentric 座標中的四元數。

## <a name="syntax"></a>語法


```C++
D3DXQUATERNION* D3DXQuaternionBaryCentric(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_    const D3DXQUATERNION *pQ3,
  _In_          FLOAT          f,
  _In_          FLOAT          g
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pQ1* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。

</dd> <dt>

*pQ2* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。

</dd> <dt>

*pQ3* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。

</dd> <dt>

*f* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

加權係數。 請參閱＜備註＞。

</dd> <dt>

*g* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

加權係數。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Barycentric 座標中 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。

## <a name="remarks"></a>備註

為了計算 barycentric 座標， **D3DXQuaternionBaryCentric** 函式會執行下列一連串的球面線性插補作業：


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXQuaternionBaryCentric** 函式就可以用來做為另一個函式的參數。

針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。

Barycentric 座標會根據三角形的頂點定義三角形內的點。 如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
