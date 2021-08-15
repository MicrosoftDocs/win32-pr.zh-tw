---
description: 傳回由兩個3D 向量的最小元件所組成的3D 向量。
ms.assetid: f38164a5-d016-4a8a-a7fe-d7eb0a681107
title: 'D3DXVec3Minimize 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3519d7a14c02356153ac9209437f488b14c363dc68fcf8b2225f1aef48d7f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297760"
---
# <a name="d3dxvec3minimize-function"></a>D3DXVec3Minimize 函式

傳回由兩個3D 向量的最小元件所組成的3D 向量。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR3* D3DXVec3Minimize(
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

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是由兩個向量的最小元件所組成。

## <a name="remarks"></a>備註

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXVec3Minimize** 函式就可以用來做為另一個函式的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Maximize**](d3dxvec3maximize.md)
</dt> </dl>

 

 




