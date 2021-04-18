---
description: 從另一個網格建立外觀網格。
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: 'D3DXCreateSkinInfoFromBlendedMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514609"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a>D3DXCreateSkinInfoFromBlendedMesh 函式

從另一個網格建立外觀網格。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

[**ID3DXBaseMesh**](id3dxbasemesh.md)物件的指標，用來建立面板網格的網格。

</dd> <dt>

*NumBones* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

附加至 BoneId 的陣列長度。 請參閱 [**D3DXBONECOMBINATION**](d3dxbonecombination.md)。

</dd> <dt>

*pBoneCombinationTable* \[在\]
</dt> <dd>

Type： **Const [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***

骨骼組合陣列的指標。 請參閱 [**D3DXBONECOMBINATION**](d3dxbonecombination.md)。

</dd> <dt>

*ppSkinInfo* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

[**ID3DXSkinInfo**](id3dxskininfo.md)介面指標的位址，表示所建立的面板網格物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列內容： E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
