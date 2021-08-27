---
description: D3DXPlaneTransformArray 函式 (D3DX10Math) -依據矩陣轉換平面陣列。 描述每個平面的向量必須正規化。
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: 'D3DXPlaneTransformArray 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 04cda233d777f05dec44b4fc93537cc33b0369d14d95c104773f0f33ef03498d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070038"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a>D3DXPlaneTransformArray 函式 (D3DX10Math) 

依據矩陣轉換平面的陣列。 描述每個平面的向量必須正規化。

## <a name="syntax"></a>語法


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

[**D3DXPLANE**](d3d10-d3dxplane.md)結構的指標，其中包含所產生的已轉換平面。 請參閱範例。

</dd> <dt>

*OutStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

每個轉換平面的 stride。

</dd> <dt>

*pP* \[在\]
</dt> <dd>

Type： **Const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

輸入 D3DXPLANE 結構的指標，其中包含要轉換之平面的陣列。 在呼叫此函式之前，必須先正規化向量 (a，b，c) 來描述平面。 請參閱範例。

</dd> <dt>

*PStride* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

每個未轉換平面的 stride。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標，其中包含轉換值的反向變換。

</dd> <dt>

*n* \[ in\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要轉換的平面數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

D3DXPLANE 結構的指標，代表已轉換的平面。 這是在不悅參數中傳回的相同值，因此可以使用此函式作為其他函式的參數。

## <a name="remarks"></a>備註

此範例會藉由套用非統一比例來轉換一個平面。


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



依 ax +、+ cz + dw = 0 描述的平面。 第一個平面是以 (a、b、c、d) = (0、1、1、0) 來建立，而這是 y + z = 0 所描述的平面。 調整之後，新的平面會包含 (a、b、c、d) = (0、0.353 f、0.235 f、0) ，以顯示 0.353 y + 0.235 z = 0 所要描述的新平面。

參數 pM 包含轉換矩陣的反向變換。 這個方法需要反向變換，如此一來，已轉換之平面的一般向量也可以正確轉換。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
