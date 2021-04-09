---
description: 在預先計算 radiance 傳輸中使用有效率的光線追蹤 (PRT) 模擬，以判斷光線是否與網格相交。 通常用來判斷指定的點是否在陰影中。
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'ID3DXPRTEngine：： ShadowRayIntersects 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 701aa4c89ee6a9d657721d872565c9b2056bb435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035373"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a>ID3DXPRTEngine：： ShadowRayIntersects 方法

在預先計算 radiance 傳輸中使用有效率的光線追蹤 (PRT) 模擬，以判斷光線是否與網格相交。 通常用來判斷指定的點是否在陰影中。

## <a name="syntax"></a>語法


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
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

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

如果光線與目前的網格相交，則傳回 **TRUE** ;否則，會傳回 **FALSE**。

## <a name="remarks"></a>備註

使用 [**ID3DXPRTEngine：： SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) 來設定與光線相交的最小和最大距離。

這個方法的執行速度比 [**ID3DXPRTEngine：： ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)更快。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
