---
description: D3DXBoxBoundProbe 函式 (D3DX10math) 決定光線是否與方塊周框方塊的音量相交。
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: 'D3DXBoxBoundProbe 函式 (D3DX10math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106978550"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a>D3DXBoxBoundProbe 函式 (D3DX10math) 

判斷光線是否與方塊周框方塊的音量相交。

## <a name="syntax"></a>語法


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMin* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)的指標，描述周框方塊的左下角。 請參閱＜備註＞。

</dd> <dt>

*pMax* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，描述周框方塊的右上角。 請參閱＜備註＞。

</dd> <dt>

*pRayPosition* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

D3DXVECTOR3 結構的指標，指定光線的原點座標。

</dd> <dt>

*pRayDirection* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

D3DXVECTOR3 結構的指標，指定光線的方向。 此向量不應該是 (0、0、0) 但不需要標準化。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

如果光線與方塊周框方塊的音量相交，則會傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="remarks"></a>備註

**D3DXBoxBoundProbe** 會決定光線是否與方塊周框方塊的音量相交，而不只是方塊的表面。

傳遞至 **D3DXBoxBoundProbe** 的值為 xmin、xmax、ymin、ymax、zmin 和 zmax。 因此，下列定義周框方塊的角落。


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



Z 方向中的周框方塊深度為 zmax-zmin，y 方向為 ymax ymin，而 x 方向為 xmax-xmin。 例如，使用下列最小和最大向量、min (-1、-1、-1) 和 max (1，1，1) ，則會以下列方式定義周框方塊。


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭  | D3DX10math。h |
| 程式庫 | D3DX10 .lib  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
