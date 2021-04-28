---
description: D3DXIntersectTri 函數 (D3DX10math) -計算光線和三角形的交集。
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: 'D3DXIntersectTri 函式 (D3DX10math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectTri
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c8bf502cca48701a7d71a083e515f9988cafe303
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113236"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a>D3DXIntersectTri 函式 (D3DX10math) 

計算光線和三角形的交集。

## <a name="syntax"></a>語法


```C++
BOOL D3DXIntersectTri(
  _In_  const D3DXVECTOR3 *p0,
  _In_  const D3DXVECTOR3 *p1,
  _In_  const D3DXVECTOR3 *p2,
  _In_  const D3DXVECTOR3 *pRayPos,
  _In_  const D3DXVECTOR3 *pRayDir,
  _Out_       FLOAT       *pU,
  _Out_       FLOAT       *pV,
  _Out_       FLOAT       *pDist
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*p0* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，描述第一個三角形頂點的位置。

</dd> <dt>

*p1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，描述第二個三角形頂點的位置。

</dd> <dt>

*p2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，描述第三個三角形頂點的位置。

</dd> <dt>

*pRayPos* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，指定光線開始的時間點。

</dd> <dt>

*pRayDir* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，指定光線的方向。

</dd> <dt>

*pU* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

Barycentric 點擊座標、U。

</dd> <dt>

*pV* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

Barycentric 點擊座標，V。

</dd> <dt>

*pDist* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

光線交集參數距離。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

如果光線與三角形的區域相交，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="remarks"></a>備註

平面 V1V2V3 中的任何點都可由 barycentric 座標 (U，V) 表示。 參數 U 會控制要將多少 V2 加權至結果中，而參數 V 控制要將多少 V3 加權到結果中。 最後， \[ 1 (U + V) 的值會 \] 控制 V1 在結果中的加權量。

Barycentric 座標是一種一般座標形式。 在此內容中，使用 barycentric 座標代表座標系統中的變更。 笛卡兒座標的 true 是 barycentric 座標的 true。

Barycentric 座標會根據三角形的頂點定義三角形內的點。 如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
