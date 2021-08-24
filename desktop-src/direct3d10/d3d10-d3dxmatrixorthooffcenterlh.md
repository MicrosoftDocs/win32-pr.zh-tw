---
description: D3DXMatrixOrthoOffCenterLH 函式 (D3DX10Math) -建立自訂的左手投影投射矩陣。
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: 'D3DXMatrixOrthoOffCenterLH 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4396f060d33efef454e87d8594c2b4ca29e46cbcbc08151cacaa76a7a4965735
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852848"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a>D3DXMatrixOrthoOffCenterLH 函式 (D3DX10Math) 

建立自訂、左方的正向投射矩陣。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

產生之 [**D3DXMATRIX**](d3d10-d3dxmatrix.md)的指標。

</dd> <dt>

*l* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

視圖量的最小 x 值。

</dd> <dt>

*r* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

視圖量的最大 x 值。

</dd> <dt>

*b* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

View volume 的最小 y 值。

</dd> <dt>

 \[ 中的 t\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

視圖量的最大 y 值。

</dd> <dt>

*zn* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

視圖音量的最小 z 值。

</dd> <dt>

*zf* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

視圖音量的最大 z 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

產生之 [**D3DXMATRIX**](d3d10-d3dxmatrix.md)的指標。

## <a name="remarks"></a>備註

[**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md)是 D3DXMatrixOrthoOffCenterLH 函數的特殊案例。 若要使用 D3DXMatrixOrthoOffCenterLH 建立相同的投射，請使用下列值：

l =-w/2，

r = w/2，

b =-h/2，和

t = h/2。

D3DXMatrixOrthoOffCenterLH 函數的所有參數都是相機空間中的距離。 參數描述視圖磁片區的維度。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXMatrixOrthoOffCenterLH 函式就可以用來做為另一個函式的參數。

此函數會使用下列公式來計算傳回的矩陣。


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
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

 

 
