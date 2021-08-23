---
description: D3DXVec2TransformCoord 函式 (D3DX10Math) -依指定的矩陣轉換2D 向量，然後將結果投射回 w = 1。
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: 'D3DXVec2TransformCoord 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 67cdde2ba057f41d8a1929e6f641b22d05919b698fee61fd8351deb64b27f5ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990678"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a>D3DXVec2TransformCoord 函式 (D3DX10Math) 

依指定的矩陣轉換2D 向量，將結果投射回 w = 1。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

作業結果之 [**D3DXVECTOR2**](d3d10-d3dxvector2.md) 的指標。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

來源 D3DXVECTOR2 結構的指標。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

D3DXVECTOR2 結構的指標，此結構是已轉換的向量。

## <a name="remarks"></a>備註

此函式會將向量、pV (x、y、0、1) ，由矩陣 pM 轉換，然後將結果投射回 w = 1。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXVec2TransformCoord 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
