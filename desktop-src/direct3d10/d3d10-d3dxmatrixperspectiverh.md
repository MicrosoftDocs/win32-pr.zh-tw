---
description: 建置右手透視投影矩陣。
ms.assetid: 324c8a21-24ef-4b3a-aac1-a753e26076d4
title: 'D3DXMatrixPerspectiveRH 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eb1c2b4b876fb2dda842912d2f18f845a3167406
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975704"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx10mathh"></a>D3DXMatrixPerspectiveRH 函式 (D3DX10Math) 

建置右手透視投影矩陣。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
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

D3DXMATRIX 結構的指標，此結構是右手向的透視圖投影矩陣。

## <a name="remarks"></a>備註

D3DXMatrixPerspectiveRH 函數的所有參數都是相機空間中的距離。 參數描述視圖磁片區的維度。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXMatrixPerspectiveRH 函式就可以用來做為另一個函式的參數。

此函數會使用下列公式來計算傳回的矩陣。


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
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

 

 
