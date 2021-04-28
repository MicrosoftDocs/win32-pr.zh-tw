---
description: ID3DXBaseMesh：： GenerateAdjacency 方法-產生網格邊緣的清單，以及共用每個邊緣的臉部清單。
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: 'ID3DXBaseMesh：： GenerateAdjacency 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 783ed7ad61337e606793b9b467e4b17fddd7ecd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115456"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a>ID3DXBaseMesh：： GenerateAdjacency 方法

產生網格邊緣清單以及共用每個邊緣的臉部清單。

## <a name="syntax"></a>語法


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Epsilon* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

指定在位置中差異小於 epsilon 的頂點應視為重合。

</dd> <dt>

*pAdjacency* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

要填入相鄰臉部索引的每個臉部陣列的指標。 此陣列中的位元組數目必須至少為 3 \* [**ID3DXBaseMesh：： GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

在應用程式產生網格的相鄰資訊之後，可以將網格資料優化，以提升繪製效能。

相鄰緩衝區中的專案順序是由索引緩衝區中的頂點索引順序所決定。 連續的三角形0一律對應至角落0和1的索引之間的邊緣。 連續的三角形1一律對應至角落1和2的索引之間的邊緣，連續的三角形2則對應至角落2與0的索引之間的邊緣。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXMesh：： Optimize**](id3dxmesh--optimize.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
