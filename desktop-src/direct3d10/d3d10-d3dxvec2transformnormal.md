---
description: D3DXVec2TransformNormal 函式 (D3DX10Math) -依指定的矩陣轉換2D 向量標準。
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: 'D3DXVec2TransformNormal 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4c1e60f200a8812a25150c153852a63bcd18949162fee0eb136794afbc0fa671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990648"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a>D3DXVec2TransformNormal 函式 (D3DX10Math) 

依指定的矩陣轉換2D 向量標準。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

作業結果之 [**D3DXVECTOR2**](d3d10-d3dxvector2.md) 的指標。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

來源 D3DXVECTOR2 結構的指標。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

D3DXVECTOR2 結構的指標，此結構是已轉換的向量。

## <a name="remarks"></a>備註

此函式會將向量 (pV->x，pV->y，0，0) 由 pM 指向的矩陣。

如果您想要轉換一般，您傳遞給此函式的矩陣應該是您用來轉換點之矩陣反向的調換。

此函式的傳回值與不悅參數中所傳回的值相同。 如此一來， **D3DXVec2TransformNormal** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
