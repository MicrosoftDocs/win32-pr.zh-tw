---
description: 建立轉換矩陣。 Null 引數會被視為身分識別轉換。
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: 'D3DXMatrixTransformation 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2174329e01e3e624ef27608ca56b33181b770db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035330"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a>D3DXMatrixTransformation 函式 (D3dx9math) 

建立轉換矩陣。 **Null** 引數會被視為身分識別轉換。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pScalingCenter* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，可識別縮放中心點。 如果這個引數是 **Null**，則會將身分識別 M <sub>sc</sub> 矩陣套用至備註中的公式。

</dd> <dt>

*pScalingRotation* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

指定縮放旋轉之 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。 如果這個引數是 **Null**，則會將身分識別 M <sub>sr</sub> 矩陣套用至備註中的公式。

</dd> <dt>

*pScaling* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，也就是縮放向量。 如果這個引數是 **Null**，則會將身分識別 Ms 矩陣套用至備註中的公式。

</dd> <dt>

*pRotationCenter* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，也就是識別旋轉中心的點。 如果此引數為 **Null**，則會將身分識別 M <sub>rc</sub> 矩陣套用至備註中的公式。

</dd> <dt>

*pRotation* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

指定旋轉之 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。 如果這個引數是 **Null**，則會將身分識別 M <sub>r</sub> 矩陣套用至備註中的公式。

</dd> <dt>

*pTranslation* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，表示轉譯。 如果此引數為 **Null**，則會將身分識別 Mt 矩陣套用至備註中的公式。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是轉換矩陣。

## <a name="remarks"></a>備註

此函式會使用下列公式來計算轉換矩陣，並以由左至右順序評估矩陣串連：

M<sub>out</sub> = (m<sub>sc</sub>) ⁻¹ \* (M<sub>sr</sub>) ⁻¹ \* Ms \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>) ⁻¹ \* m<sub>r</sub> \* m<sub>rc</sub> \* Mt

其中：

M <sub>out</sub> = 輸出矩陣 (*不悅*) 

M <sub>sc</sub> = 縮放中心矩陣 (*pScalingCenter*) 

M <sub>sr</sub> = 調整旋轉矩陣 (*pScalingRotation*) 

Ms = 調整矩陣 (*pScaling*) 

M <sub>rc</sub> = 旋轉矩陣的中心 (*pRotationCenter*) 

M <sub>r</sub> = 旋轉矩陣 (*pRotation*) 

Mt = 轉譯矩陣 (*pTranslation*) 

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXMatrixTransformation** 函式就可以用來做為另一個函式的參數。

若是2D 轉換，請使用 [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[轉換 (Direct3D 9) ](transforms.md)
</dt> </dl>

 

 




