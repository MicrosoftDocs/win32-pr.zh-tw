---
description: D3DXMatrixTranspose 函式 (D3DX10Math) -傳回矩陣的矩陣轉型。
ms.assetid: 934b17cc-39c4-425c-839b-69e080f0efd7
title: 'D3DXMatrixTranspose 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e20fd8a29ba3f9adec7134a011f8f470c60f7011
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108856"
---
# <a name="d3dxmatrixtranspose-function-d3dx10mathh"></a>D3DXMatrixTranspose 函式 (D3DX10Math) 

傳回矩陣的矩陣變換。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
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

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

來源 D3DXMATRIX 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

D3DXMATRIX 結構的指標，此結構是矩陣的矩陣變換。

## <a name="remarks"></a>備註

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXMatrixTranspose 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
