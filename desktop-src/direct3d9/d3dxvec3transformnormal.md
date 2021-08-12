---
description: D3DXVec3TransformNormal 函式 (D3dx9math) -由指定的矩陣轉換一般的3D 向量。
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: 'D3DXVec3TransformNormal 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62c70524fd1b729473c09c0ff0cb6b1c764e356069a29eb40e9cf52dfa434127
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297681"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a>D3DXVec3TransformNormal 函式 (D3dx9math) 

依指定的矩陣轉換一般的3D 向量。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是已轉換的向量。

## <a name="remarks"></a>備註

此函式會將向量 (*pv*->x， *pv*->y， *pv*>z，0) 由 *pM* 指向的矩陣。

如果您想要轉換一般，您傳遞給此函式的矩陣應該是您用來轉換點之矩陣反向的調換。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXVec3TransformNormal** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




