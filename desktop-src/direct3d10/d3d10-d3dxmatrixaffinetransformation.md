---
description: D3DXMatrixAffineTransformation function (D3DX10Math) -建立3D 仿射轉換矩陣。 Null 引數會被視為身分識別轉換。
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: 'D3DXMatrixAffineTransformation 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5c847d537eaa79b266ef785f40806c37e2503b2b9a8a97bf99a678c7dff219de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609518"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a>D3DXMatrixAffineTransformation 函式 (D3DX10Math) 

建立3D 仿射轉換矩陣。 **Null** 引數會被視為身分識別轉換。

## <a name="syntax"></a>語法


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[在\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

作業結果之 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 的指標。

</dd> <dt>

*調整* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

調整係數。

</dd> <dt>

*pRotationCenter* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)的指標，也就是識別旋轉中心的點。 如果此引數為 **Null**，則會將身分識別 M <sub>rc</sub> 矩陣套用至備註中的公式。

</dd> <dt>

*pRotation* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

指定旋轉之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。 如果這個引數是 **Null**，則會將身分識別 M <sub>r</sub> 矩陣套用至備註中的公式。

</dd> <dt>

*pTranslation* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

表示轉譯之 D3DXVECTOR3 結構的指標。 如果此引數為 **Null**，則會將身分識別 Mt 矩陣套用至備註中的公式。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

D3DXMATRIX 結構的指標，此結構是仿射轉換矩陣。

## <a name="remarks"></a>備註

此函式會使用下列公式來計算仿射轉換矩陣，並以由左至右順序評估矩陣串連：

M<sub>out</sub> = Ms \* (M<sub>rc</sub>) -1 \* M<sub>r</sub> \* m<sub>rc</sub> \* Mt

其中：

M<sub>out</sub> = 輸出矩陣 (不悅) 

Ms = 調整矩陣 (調整) 

M<sub>rc</sub> = 旋轉矩陣的中心 (pRotationCenter) 

M<sub>r</sub> = 旋轉矩陣 (pRotation) 

Mt = 轉譯矩陣 (pTranslation) 

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXMatrixAffineTransformation 函式就可以用來做為另一個函式的參數。

若是2D 仿射轉換，請使用 D3DXMatrixAffineTransformation2D。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
