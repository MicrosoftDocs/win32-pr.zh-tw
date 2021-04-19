---
description: 建立將幾何壓平合併成平面的矩陣。
ms.assetid: 8f283ff9-c879-476c-8057-f4fe77a7a9e7
title: 'D3DXMatrixShadow 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6bf1639adb7364536cce5c0dead9ef58ae10bea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982009"
---
# <a name="d3dxmatrixshadow-function-d3dx9mathh"></a>D3DXMatrixShadow 函式 (D3dx9math) 

建立將幾何壓平合併成平面的矩陣。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pLight* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***

[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，描述光源的位置。

</dd> <dt>

*pPlane* \[在\]
</dt> <dd>

Type： **Const [**D3DXPLANE**](d3dxplane.md) \***

來源 [**D3DXPLANE**](d3dxplane.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

將幾何壓平合併成平面的 [**D3DXMATRIX**](d3dxmatrix.md) 結構指標。

## <a name="remarks"></a>備註

**D3DXMatrixShadow** 函式會將幾何簡維化為平面，就像從燈光轉換陰影一樣。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXMatrixShadow** 函式就可以用來做為另一個函式的參數。

此函數會使用下列公式來計算傳回的矩陣。


```
P = normalize(Plane);
L = Light;
d = -dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



如果光線的 w 元件為0，從原點到燈光的光線代表方向光線。 如果是1，則光線是點燈。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




