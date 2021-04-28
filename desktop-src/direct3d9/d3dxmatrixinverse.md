---
description: D3DXMatrixInverse 函數 (D3dx9math) -計算矩陣的反向。
ms.assetid: b8cad5c5-caa5-4426-b045-1770f8806b6b
title: 'D3DXMatrixInverse 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0109481beaea282a785564c081e498fe4c7571b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098146"
---
# <a name="d3dxmatrixinverse-function-d3dx9mathh"></a>D3DXMatrixInverse 函式 (D3dx9math) 

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

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pDeterminant* \[in、out\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

包含矩陣行列式的 FLOAT 值指標。 如果不需要行列式，請將此參數設定為 **Null**。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是矩陣的反向。 如果矩陣反轉失敗，則會傳回 **Null** 。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXMatrixInverse** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
