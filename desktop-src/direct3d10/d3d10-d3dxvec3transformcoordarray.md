---
description: D3DXVec3TransformCoordArray 函式 (D3DX10Math) -轉換陣列 (x、y、z、1) 指定的矩陣，然後將結果投射回 w = 1。
ms.assetid: 259a885d-89be-4fea-a579-dac3dd76878f
title: 'D3DXVec3TransformCoordArray 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoordArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 27f0187f3533b6cb7c9782ddaa0f59692a15335ebb27b86184b2b5544d44fe5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895328"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx10mathh"></a>D3DXVec3TransformCoordArray 函式 (D3DX10Math) 

將陣列 (x、y、z、1) 由指定的矩陣轉換，然後將結果投射回 w = 1。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR3* D3DXVec3TransformCoordArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。

</dd> <dt>

*OutStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

輸出資料流程中向量之間的 Stride。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

來源 D3DXVECTOR3 陣列的指標。

</dd> <dt>

*VStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

輸入資料流程中向量之間的 Stride。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。

</dd> <dt>

*n* \[ in\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

陣列中的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

D3DXVECTOR3 結構的指標，此結構是已轉換的陣列。

## <a name="remarks"></a>備註

此函式會將陣列 pV (x、y、z、1) 由矩陣 pM 轉換，然後將結果投射回 w = 1。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來， [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
