---
description: D3DXVec3Project 函式 (D3dx9math) -從物件空間將3D 向量投射到螢幕空間。
ms.assetid: b012771d-052f-4bf9-b39c-387d8a63fa59
title: 'D3DXVec3Project 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1bb0d7b962dd4595ec9246c036d4ff9e459e062f366b6e62f46cce1a5a3ebab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803810"
---
# <a name="d3dxvec3project-function-d3dx9mathh"></a>D3DXVec3Project 函式 (D3dx9math) 

將物件空間中的3D 向量投射到螢幕空間。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
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

*pViewport* \[在\]
</dt> <dd>

Type： **Const [**D3DVIEWPORT9**](d3dviewport9.md) \***

[**D3DVIEWPORT9**](d3dviewport9.md)結構的指標，表示區。

</dd> <dt>

*pProjection* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，表示投射矩陣。

</dd> <dt>

*pView* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，代表視圖矩陣。

</dd> <dt>

*pWorld* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，代表世界矩陣。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是從物件空間到螢幕空間投射的向量。

## <a name="remarks"></a>備註

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXVec3Project** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Unproject**](d3dxvec3unproject.md)
</dt> </dl>

 

 




