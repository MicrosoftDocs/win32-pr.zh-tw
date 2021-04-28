---
description: D3DXMatrixScaling 函式 (D3dx9math) -建立沿著 X 軸、y 軸和 Z 軸縮放的矩陣。
ms.assetid: f51baa4e-0aec-4de8-b746-24cb52f318d6
title: 'D3DXMatrixScaling 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97ccd4cc6207bb211259833d163793c3499b51a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118066"
---
# <a name="d3dxmatrixscaling-function-d3dx9mathh"></a>D3DXMatrixScaling 函式 (D3dx9math) 

建立沿著 X 軸、y 軸和 Z 軸縮放的矩陣。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*sx* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

沿著 X 軸套用的縮放係數。

</dd> <dt>

*sy* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

沿著 y 軸套用的縮放係數。

</dd> <dt>

*sz* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

沿著 Z 軸套用的縮放係數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

縮放轉換 [**D3DXMATRIX**](d3dxmatrix.md)的指標。

## <a name="remarks"></a>備註

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXMatrixScaling** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
