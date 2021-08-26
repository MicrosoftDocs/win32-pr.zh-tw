---
description: D3DXVec3ProjectArray 函式 (D3DX10Math) -投射陣列 (x、y、z、0) 從物件空間到螢幕空間。
ms.assetid: 33f0f65a-c027-4a31-83a7-f5f6b2a2f72f
title: 'D3DXVec3ProjectArray 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 660d48219c3d93e9b3188926dd6f5bc2ddf9db45a9310b3bf8716cb2e960e895
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989618"
---
# <a name="d3dxvec3projectarray-function-d3dx10mathh"></a>D3DXVec3ProjectArray 函式 (D3DX10Math) 

投射陣列 (x、y、z、0) 從物件空間到螢幕空間。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_          UINT           OutStride,
  _In_    const D3DXVECTOR3    *pV,
  _In_          UINT           VStride,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld,
  _In_          UINT           n
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。

</dd> <dt>

*OutStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

輸出資料流程中向量之間的 Stride。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

來源 D3DXVECTOR3 結構的指標。

</dd> <dt>

*VStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

輸入資料流程中向量之間的 Stride。

</dd> <dt>

*pViewport* \[在\]
</dt> <dd>

Type： **Const [**D3D10 \_ 視口**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***

[**D3D10 \_ 區**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)的指標，表示區。

</dd> <dt>

*pProjection* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，表示投射矩陣。

</dd> <dt>

*pView* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

D3DXMATRIX 結構的指標，代表視圖矩陣。

</dd> <dt>

*pWorld* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

D3DXMATRIX 結構的指標，代表世界矩陣。

</dd> <dt>

*n* \[ in\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

陣列中的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

D3DXVECTOR3 結構的指標，此結構是從物件空間投射到螢幕空間的陣列。

## <a name="remarks"></a>備註

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXVec3ProjectArray 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
