---
description: D3DXSphereBoundProbe 函式 (D3DX9Mesh) -決定光線是否與球體周框方塊的音量相交。
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: 'D3DXSphereBoundProbe 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85dbd46233176d65e7e7abbf0eb266c81868ceba7e67e3257bf902d1775d6a90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731151"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a>D3DXSphereBoundProbe 函式 (D3DX9Mesh) 

判斷光線是否與球體周框方塊的音量相交。

## <a name="syntax"></a>語法


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCenter* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定球體的中心座標。

</dd> <dt>

*Radius* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

球體的半徑。

</dd> <dt>

*pRayPosition* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線的原點座標。

</dd> <dt>

*pRayDirection* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線的方向。 此向量不應該是 (0、0、0) 但不需要標準化。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

如果光線與球體周框方塊的音量相交，則會傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="remarks"></a>備註

**D3DXSphereBoundProbe** 會決定光線是否與球體周框方塊的音量相交，而不只是球體的表面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
