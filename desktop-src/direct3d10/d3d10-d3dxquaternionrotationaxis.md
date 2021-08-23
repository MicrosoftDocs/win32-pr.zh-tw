---
description: D3DXQuaternionRotationAxis 函式 (D3DX10Math) -圍繞任意軸旋轉四元數。
ms.assetid: 9673ef89-458f-4a25-960e-8f03179e78ba
title: 'D3DXQuaternionRotationAxis 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1ab148eee572e5c0f2ad2965b91c869ce490f5b35d8a78644090165b33ac19a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991048"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx10mathh"></a>D3DXQuaternionRotationAxis 函式 (D3DX10Math) 

旋轉有關任意軸的四元數。

## <a name="syntax"></a>語法


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

識別要用來旋轉四元數之軸的 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 指標。

</dd> <dt>

*角度* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

旋轉的角度，以弧度為單位。 沿著旋轉軸向原點方向看時，角度是順時針方向測量。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

圍繞指定軸旋轉之 D3DXQUATERNION 結構的指標。

## <a name="remarks"></a>備註

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXQuaternionRotationAxis 函式就可以用來做為另一個函式的參數。

針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
