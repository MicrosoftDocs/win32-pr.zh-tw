---
description: 在預先計算 radiance 傳輸中使用有效率的光線追蹤 (PRT) 模擬，以判斷光線是否與網格相交。
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'ID3DXPRTEngine：： ClosestRayIntersects 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2620140337807891efa739da4540e3895394f63bcc494396c13e7c15d0c1b29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729784"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a>ID3DXPRTEngine：： ClosestRayIntersects 方法

在預先計算 radiance 傳輸中使用有效率的光線追蹤 (PRT) 模擬，以判斷光線是否與網格相交。 如果找到交集，方法會傳回最接近之網格臉部的索引，以及交集點的 barycentric 座標。

## <a name="syntax"></a>語法


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRayPos* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線開始的時間點。

</dd> <dt>

*pRayDir* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線的正規化方向。

</dd> <dt>

*pFaceIndex* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

目前網格臉部的索引指標，該指標是由指定光線第一個叫用的，根據目前網格前方的所有封鎖程式網格臉部堆疊。

</dd> <dt>

*pU* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

指標，指向三角形的頂點 0 barycentric 點擊座標 U。

</dd> <dt>

*pV* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

指標，指向三角形的頂點1的 barycentric 點擊座標（V）。

</dd> <dt>

*pDist* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

沿著光線相交點距離的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

如果光線與目前的網格相交，則傳回 **TRUE** ;否則，會傳回 **FALSE**。

## <a name="remarks"></a>備註

使用 [**ID3DXPRTEngine：： SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) 來設定與光線相交的最小和最大距離。

三角形的第三個頂點 (頂點 2) 的 barycentric 座標是 1 ( U + V ) 。

這個方法的執行速度比 [**ID3DXPRTEngine：： ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)慢。 如果不需要交集點的位置，請使用 **ID3DXPRTEngine：： ShadowRayIntersects** 。

Barycentric 座標會根據三角形的頂點定義三角形內的點。 如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
