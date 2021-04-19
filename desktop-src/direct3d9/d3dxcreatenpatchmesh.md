---
description: 從三角形網格建立 N 修補程式網格。
ms.assetid: f565ed0b-72fc-4184-b423-f68b0acfafb0
title: 'D3DXCreateNPatchMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateNPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ab73d1254700808bbd56b7b46f7781b27b188b7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985910"
---
# <a name="d3dxcreatenpatchmesh-function"></a>D3DXCreateNPatchMesh 函式

從三角形網格建立 N 修補程式網格。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateNPatchMesh(
  _In_    LPD3DXMESH      pMeshSysMem,
  _Inout_ LPD3DXPATCHMESH *pPatchMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMeshSysMem* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

代表三角形網格物件之 [**ID3DXMesh**](id3dxmesh.md) 介面指標的位址。

</dd> <dt>

*pPatchMesh* \[in、out\]
</dt> <dd>

類型： **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

[**ID3DXPatchMesh**](id3dxpatchmesh.md)介面指標的位址，表示所建立的 patch 網狀物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




