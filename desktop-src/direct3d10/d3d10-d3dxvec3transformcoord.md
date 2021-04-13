---
description: 依指定的矩陣轉換3D 向量，將結果投射回 w = 1。
ms.assetid: e138fdc0-6999-45ab-8bcf-54f53bd9b1bf
title: 'D3DXVec3TransformCoord 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: a8fc7c7a00133e036921eabaa145dca01a12f042
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322964"
---
# <a name="d3dxvec3transformcoord-function-d3dx10mathh"></a>D3DXVec3TransformCoord 函式 (D3DX10Math) 

依指定的矩陣轉換3D 向量，將結果投射回 w = 1。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

來源 D3DXVECTOR3 結構的指標。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

D3DXVECTOR3 結構的指標，此結構是已轉換的向量。

## <a name="remarks"></a>備註

此函式會將向量、pV (x、y、z、1) ，由矩陣 pM 轉換，然後將結果投射回 w = 1。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXVec3TransformCoord 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
