---
description: 建立自訂的左手向透視圖投影矩陣。
ms.assetid: de2732dd-a4f2-47bc-9509-de16f1ca85c2
title: 'D3DXMatrixPerspectiveOffCenterLH 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15743af16be84587fd8dc03e845ffcd8bd8dbc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974835"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx9mathh"></a>D3DXMatrixPerspectiveOffCenterLH 函式 (D3dx9math) 

建立自訂的左手向透視圖投影矩陣。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
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

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*l* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

視圖音量的最小 x 值。

</dd> <dt>

*r* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

視圖音量的最大 x 值。

</dd> <dt>

*b* \[ in\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

視圖音量的最小 y 值。

</dd> <dt>

 \[ 中的 t\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

視圖音量的最大 y 值。

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

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是自訂、左方的透視圖投影矩陣。

## <a name="remarks"></a>備註

**D3DXMatrixPerspectiveOffCenterLH** 函數的所有參數都是相機空間中的距離。 參數描述視圖磁片區的維度。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXMatrixPerspectiveOffCenterLH** 函式就可以用來做為另一個函式的參數。

此函數會使用下列公式來計算傳回的矩陣。


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)
</dt> </dl>

 

 
