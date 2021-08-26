---
description: D3DXMatrixInverse 函數 (D3DX10Math) -計算矩陣的反向。
ms.assetid: 928a201b-814d-41cc-bfab-d2f8a12addeb
title: 'D3DXMatrixInverse 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixInverse
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c69b66ab081588a14942f7b14aeb8a0b2e64b90df5ece0bd55cc4ea6b0f9550e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895627"
---
# <a name="d3dxmatrixinverse-function-d3dx10mathh"></a>D3DXMatrixInverse 函式 (D3DX10Math) 

計算矩陣的反向。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pDeterminant* \[in、out\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

包含矩陣行列式的 FLOAT 值指標。 如果不需要行列式，請將此參數設定為 **Null**。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

來源 D3DXMATRIX 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

D3DXMATRIX 結構的指標，此結構是矩陣的反向。 如果矩陣反轉失敗，則會傳回 **Null** 。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXMatrixInverse 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
