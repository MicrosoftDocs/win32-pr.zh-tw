---
description: 在 xy 平面中建立2D 仿射轉換矩陣。 Null 引數會被視為身分識別轉換。
ms.assetid: 335de919-ae4d-405d-b6bb-ca6bdc2d568a
title: 'D3DXMatrixAffineTransformation2D 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6edd0658eb80ec53d19b6c136a672cb78a2087b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993875"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx9mathh"></a>D3DXMatrixAffineTransformation2D 函式 (D3dx9math) 

在 xy 平面中建立2D 仿射轉換矩陣。 **Null** 引數會被視為身分識別轉換。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_          FLOAT       Scaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*調整* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

調整係數。

</dd> <dt>

*pRotationCenter* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，也就是識別旋轉中心的點。 如果此引數為 **Null**，則會將身分識別 M <sub>rc</sub> 矩陣套用至備註中的公式。

</dd> <dt>

*旋轉* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

旋轉的角度。

</dd> <dt>

*pTranslation* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，表示轉譯。 如果此引數為 **Null**，則會將身分識別 Mt 矩陣套用至備註中的公式。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是仿射轉換矩陣。

## <a name="remarks"></a>備註

此函式會使用下列公式來計算仿射轉換矩陣，並以由左至右順序評估矩陣串連：

M<sub>out</sub> = Ms \* (M<sub>rc</sub>) ⁻¹ \* m<sub>r</sub> \* m<sub>rc</sub> \* Mt

其中：

M <sub>out</sub> = 輸出矩陣 (*不悅*) 

Ms = 調整矩陣 (*調整*) 

M <sub>rc</sub> = 旋轉矩陣的中心 (*pRotationCenter*) 

M <sub>r</sub> = 旋轉矩陣 (*旋轉*) 

Mt = 轉譯矩陣 (*pTranslation*) 

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來， **D3DXMatrixAffineTransformation2D** 函式就可以用來做為另一個函式的參數。

若為3D 仿射轉換，請使用 [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md)
</dt> <dt>

[轉換 (Direct3D 9) ](transforms.md)
</dt> </dl>

 

 
