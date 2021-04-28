---
description: D3DXMatrixAffineTransformation function (D3dx9math) -建立3D 仿射轉換矩陣。 Null 引數會被視為身分識別轉換。
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: 'D3DXMatrixAffineTransformation 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7329ffbffe5ffd89ed64e5386246f39699618960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094166"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a>D3DXMatrixAffineTransformation 函式 (D3dx9math) 

建立3D 仿射轉換矩陣。 **Null** 引數會被視為身分識別轉換。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
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

*調整* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

調整係數。

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

表示轉譯之 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。 如果此引數為 **Null**，則會將身分識別 Mt 矩陣套用至備註中的公式。

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

M <sub>r</sub> = 旋轉矩陣 (*pRotation*) 

Mt = 轉譯矩陣 (*pTranslation*) 

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來， **D3DXMatrixAffineTransformation** 函式就可以用來做為另一個函式的參數。

若是2D 仿射轉換，請使用 [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixTransformation**](d3dxmatrixtransformation.md)
</dt> <dt>

[轉換 (Direct3D 9) ](transforms.md)
</dt> </dl>

 

 
