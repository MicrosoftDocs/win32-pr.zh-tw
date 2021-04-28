---
description: D3DXVec2Transform 函式 (D3dx9math) -依指定的矩陣轉換2D 向量。
ms.assetid: ccde9e34-2d99-4112-a8ed-3820d018b547
title: 'D3DXVec2Transform 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b9b0f5ae0e3fda05cd8bdd92ee73b826f81b970
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097946"
---
# <a name="d3dxvec2transform-function-d3dx9mathh"></a>D3DXVec2Transform 函式 (D3dx9math) 

依指定的矩陣轉換2D 向量。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***

[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***

[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是已轉換的向量。

## <a name="remarks"></a>備註

此函式會將向量 *pV* (x、y、0、1) 由矩陣 *pM* 進行轉換。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXVec2Transform** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2TransformCoord**](d3dxvec2transformcoord.md)
</dt> <dt>

[**D3DXVec2TransformNormal**](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




