---
description: 決定兩個3D 向量的交叉乘積。
ms.assetid: c9623f35-c8fc-4fbe-87b6-0e5bb8ebd5e8
title: 'D3DXVec3Cross 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3fdf2a5d3c3771056f169900df519d90a183798d6f5c60df0904444dbce5fd9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122572"
---
# <a name="d3dxvec3cross-function"></a>D3DXVec3Cross 函式

決定兩個3D 向量的交叉乘積。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR3* D3DXVec3Cross(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pV1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。

</dd> <dt>

*pV2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，這是兩個3d 向量的交叉乘積。

## <a name="remarks"></a>備註

此函數會使用下列程式碼來決定交叉乘積。


```
D3DXVECTOR3 v;
    
v.x = pV1->y * pV2->z - pV1->z * pV2->y;
v.y = pV1->z * pV2->x - pV1->x * pV2->z;
v.z = pV1->x * pV2->y - pV1->y * pV2->x;
    
*pOut = v;
```



此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXVec3Cross** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Dot**](d3dxvec3dot.md)
</dt> </dl>

 

 




