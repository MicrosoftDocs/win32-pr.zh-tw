---
description: D3DXPlaneTransform 函式 (D3DX10Math) -依矩陣轉換平面。 輸入矩陣是實際轉換的反向變換。
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: 'D3DXPlaneTransform 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9b1d16ba2a29d42614c388a6207503ad32dd5e0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108786"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a>D3DXPlaneTransform 函式 (D3DX10Math) 

依矩陣轉換平面。 輸入矩陣是實際轉換的反向變換。

## <a name="syntax"></a>語法


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

[**D3DXPLANE**](d3d10-d3dxplane.md)的指標，其中包含所產生的已轉換平面。 請參閱範例。

</dd> <dt>

*pP* \[在\]
</dt> <dd>

Type： **Const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

輸入 D3DXPLANE 結構的指標，其中包含將轉換的平面。 在呼叫此函式之前，必須先正規化向量 (a，b，c) 來描述平面。 請參閱範例。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標，其中包含轉換值。 此矩陣必須包含轉換值的反向變換。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

D3DXPLANE 結構的指標，代表已轉換的平面。 這是在不悅參數中傳回的相同值，因此可以使用此函式作為其他函式的參數。

## <a name="remarks"></a>備註

### <a name="examples"></a>範例

此範例會套用非統一比例來轉換平面。


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
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

 

 
