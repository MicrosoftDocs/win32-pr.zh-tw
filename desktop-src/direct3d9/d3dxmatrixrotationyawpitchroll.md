---
description: 建立具有指定之偏擺、音調和變換的矩陣。
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: 'D3DXMatrixRotationYawPitchRoll 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2a8d6a531592ce49342dae0d0ecd6b3ace995bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196183"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a>D3DXMatrixRotationYawPitchRoll 函式 (D3dx9math) 

建立具有指定之偏擺、音調和變換的矩陣。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*偏擺* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

偏擺圍繞 y 軸，以弧度為單位。

</dd> <dt>

*推銷* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

X 軸的間距，以弧度為單位。

</dd> <dt>

*滾動* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

以弧度為單位，圍繞 Z 軸。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，該結構具有指定的偏擺、音調和滾動。

## <a name="remarks"></a>備註

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXMatrixRotationYawPitchRoll** 函式就可以用來做為另一個函式的參數。

轉換順序會優先擲出，然後再偏擺。 相對於物件的本機座標軸，這相當於圍繞 Z 軸的旋轉，後面接著圍繞 X 軸旋轉，後面接著旋轉 y 軸（如下圖所示）。

![捲軸、音調和偏擺的圖例，作為三個軸的旋轉](images/pitchyawroll.png)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**D3DXMatrixRotationQuaternion**](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)
</dt> <dt>

[**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)
</dt> <dt>

[**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
