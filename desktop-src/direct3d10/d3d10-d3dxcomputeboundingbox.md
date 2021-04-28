---
description: D3DXComputeBoundingBox 函式 (D3DX10math) -計算座標軸導向的周框方塊。
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: 'D3DXComputeBoundingBox 函式 (D3DX10math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a12e7e302fb36ffb8856e6402f110e01bb2afb2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103526"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a>D3DXComputeBoundingBox 函式 (D3DX10math) 

計算座標軸導向的周框方塊。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFirstPosition* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

第一個位置的指標。

</dd> <dt>

*NumVertices* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

頂點數目。

</dd> <dt>

*dwStride* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

頂點之間的計數或位元組數目。

</dd> <dt>

*pMin* \[擴展\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，描述周框方塊的傳回左下角。

</dd> <dt>

*pMax* \[擴展\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，描述周框方塊的右上角。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
