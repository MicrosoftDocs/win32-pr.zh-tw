---
description: D3DXQuaternionToAxisAngle 函數 (D3DX10Math) -計算四元數的軸和旋轉角度。
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: 'D3DXQuaternionToAxisAngle 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 51f704aa839ff210b3c2de57767cb32ec609232f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108696"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a>D3DXQuaternionToAxisAngle 函式 (D3DX10Math) 

計算四元數的軸和旋轉角度。

## <a name="syntax"></a>語法


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pQ* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

來源 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)的指標。

</dd> <dt>

*pAxis* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

此函式會傳回 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標，以識別四元數的旋轉軸。

</dd> <dt>

*pAngle* \[in、out\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

此函式會傳回浮點值的指標，此值會識別四元數的旋轉角度（以弧度為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

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

 

 
