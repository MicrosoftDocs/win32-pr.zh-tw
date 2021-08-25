---
description: D3DXMatrixMultiplyTranspose 函式 (D3DX10Math) -計算兩個矩陣的轉換乘積。
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: 'D3DXMatrixMultiplyTranspose 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 55bf8dc8eaed13c6bfdc4a8cedacd02b9c5cc5aa11ca0d3e494ed194c8cc9245
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858778"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a>D3DXMatrixMultiplyTranspose 函式 (D3DX10Math) 

計算兩個矩陣的轉換乘積。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pM1* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

來源 D3DXMATRIX 結構的指標 (左手邊) 。

</dd> <dt>

*pM2* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

指向來源 D3DXMATRIX 結構 (右手邊) 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

D3DXMATRIX 結構的指標，這是兩個矩陣的乘積。

## <a name="remarks"></a>備註

結果會是兩個轉換矩陣的乘積，Out = T (M1 \* M2) 。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXMatrixMultiplyTranspose 函式就可以用來做為另一個函式的參數。

此函數有助於將矩陣設定為頂點和圖元著色器的常數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
