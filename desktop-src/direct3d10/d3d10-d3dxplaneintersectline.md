---
description: 尋找平面和直線之間的交集。
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: 'D3DXPlaneIntersectLine 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00d25fcba9e5884cec10da96964ad0f5daa9ed14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992744"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a>D3DXPlaneIntersectLine 函式 (D3DX10Math) 

尋找平面和直線之間的交集。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)的指標，識別指定之平面和線條之間的交集。

</dd> <dt>

*pP* \[在\]
</dt> <dd>

Type： **Const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

來源 [**D3DXPLANE**](d3d10-d3dxplane.md)的指標。

</dd> <dt>

*pV1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

來源 D3DXVECTOR3 結構的指標，定義行起始點。

</dd> <dt>

*pV2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

來源 D3DXVECTOR3 結構的指標，定義線條結束點。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

D3DXVECTOR3 結構的指標，此結構是指定之平面和線條之間的交集。

## <a name="remarks"></a>備註

如果直線與平面平行，則會傳回 **Null** 。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXPlaneIntersectLine 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
