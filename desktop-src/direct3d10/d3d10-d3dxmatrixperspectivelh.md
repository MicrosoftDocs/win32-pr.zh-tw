---
description: D3DXMatrixPerspectiveLH 函式 (D3DX10Math) -建立左手式的透視圖投影矩陣
ms.assetid: 5fd8da67-ff12-42fa-b915-b50fa2680b32
title: 'D3DXMatrixPerspectiveLH 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ea9b91fe926ecbab34fa65fd6c21f852501b6d515acaf8b9aaa5b8971a27c37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304502"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx10mathh"></a>D3DXMatrixPerspectiveLH 函式 (D3DX10Math) 

建立左手向的透視圖投影矩陣

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*w* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

接近 view 平面的視圖音量寬度。

</dd> <dt>

*h* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

接近 view 平面的視圖音量高度。

</dd> <dt>

*zn* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

接近視圖平面的 Z 值。

</dd> <dt>

*zf* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

最遠的視圖平面的 Z 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

D3DXMATRIX 結構的指標，此結構是左手向的透視圖投影矩陣。

## <a name="remarks"></a>備註

D3DXMatrixPerspectiveLH 函數的所有參數都是相機空間中的距離。 參數描述視圖磁片區的維度。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXMatrixPerspectiveLH 函式就可以用來做為另一個函式的參數。

此函數會使用下列公式來計算傳回的矩陣。


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
