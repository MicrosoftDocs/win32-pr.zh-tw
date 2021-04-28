---
description: D3DXPlaneFromPointNormal 函式 (D3DX10Math) -從點和一般結構來建立平面。
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: 'D3DXPlaneFromPointNormal 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 519ce82a8d5a8c6adaf22b69047a8d365bd777ac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108836"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a>D3DXPlaneFromPointNormal 函式 (D3DX10Math) 

從點和一般結構來建立平面。

## <a name="syntax"></a>語法


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

作業結果之 [**D3DXPLANE**](d3d10-d3dxplane.md) 的指標。

</dd> <dt>

*pPoint* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)的指標，定義用來建立平面的點。

</dd> <dt>

*pNormal* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

D3DXVECTOR3 結構的指標，定義用來建立平面的一般。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

從點和標準所建立的 D3DXPLANE 結構指標。

## <a name="remarks"></a>備註

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXPlaneFromPointNormal 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
