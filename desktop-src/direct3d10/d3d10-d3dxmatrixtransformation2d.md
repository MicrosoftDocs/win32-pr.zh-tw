---
description: D3DXMatrixTransformation2D 函式 (D3DX10Math) -建立代表 xy 平面轉換的2D 轉換矩陣。 Null 引數會被視為身分識別轉換。
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: 'D3DXMatrixTransformation2D 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 754e755b0ee6e03692bf7eabeb4e751284478621f47c912d399eb101adfd98e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754288"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a>D3DXMatrixTransformation2D 函式 (D3DX10Math) 

建立2D 轉換矩陣，表示 xy 平面中的轉換。 **Null** 引數會被視為身分識別轉換。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       ScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，其中包含轉換的結果。

</dd> <dt>

*pScalingCenter* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

指向 [**D3DXVECTOR2**](d3d10-d3dxvector2.md)的指標，也就是識別縮放中心的點。 如果這個引數是 **Null**，則會將身分識別 M <sub>sc</sub> 矩陣套用至備註中的公式。

</dd> <dt>

*ScalingRotation* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

縮放旋轉因數的指標。

</dd> <dt>

*pScaling* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

D3DXVECTOR2 結構的指標，也就是識別尺規的點。 如果這個引數是 **Null**，則會將身分識別 Ms 矩陣套用至備註中的公式。

</dd> <dt>

*pRotationCenter* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

D3DXVECTOR2 結構的指標，也就是識別旋轉中心的點。 如果此引數為 **Null**，則會將身分識別 M <sub>rc</sub> 矩陣套用至備註中的公式。

</dd> <dt>

*旋轉* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

旋轉的角度，以弧度為單位。

</dd> <dt>

*pTranslation* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

D3DXVECTOR2 結構的指標，識別翻譯。 如果此引數為 **Null**，則會將身分識別 Mt 矩陣套用至備註中的公式。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

D3DXMATRIX 結構的指標，其中包含轉換矩陣。

## <a name="remarks"></a>備註

此函式會使用下列公式來計算轉換矩陣，並以由左至右順序評估矩陣串連：

M<sub>out</sub> = (m<sub>sc</sub>) ⁻¹ \* (M<sub>sr</sub>) ⁻¹ \* Ms \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>) ⁻¹ \* m<sub>r</sub> \* m<sub>rc</sub> \* Mt

其中：

M<sub>out</sub> = 輸出矩陣 (不悅) 

M<sub>sc</sub> = 縮放中心矩陣 (pScalingCenter) 

M<sub>sr</sub> = 調整旋轉矩陣 (pScalingRotation) 

Ms = 調整矩陣 (pScaling) 

M<sub>rc</sub> = 旋轉矩陣的中心 (pRotationCenter) 

M<sub>r</sub> = 旋轉矩陣 (旋轉) 

Mt = 轉譯矩陣 (pTranslation) 

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXMatrixTransformation2D 函式就可以用來做為另一個函式的參數。

若為3D 轉換，請使用 [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
