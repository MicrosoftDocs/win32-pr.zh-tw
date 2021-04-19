---
description: 使用宣告子建立網格物件。
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: 'D3DXCreateMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cfb56fe5c52d2726dff0877522b6f72f70437552
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001482"
---
# <a name="d3dxcreatemesh-function"></a>D3DXCreateMesh 函式

使用宣告子建立網格物件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateMesh(
  _In_        DWORD               NumFaces,
  _In_        DWORD               NumVertices,
  _In_        DWORD               Options,
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _In_        LPDIRECT3DDEVICE9   pD3DDevice,
  _Out_       LPD3DXMESH          *ppMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NumFaces* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

網格的臉部數目。 此數位的有效範圍大於0，而一個小於最大 DWORD (通常是 65534) ，因為會保留最後一個索引。

</dd> <dt>

*NumVertices* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

網格的頂點數目。 此參數必須大於0。

</dd> <dt>

*選項* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

[**D3DXMESH**](./d3dxmesh.md)列舉中的一或多個旗標組合，指定網格的選項。

</dd> <dt>

*pDeclaration* \[在\]
</dt> <dd>

Type： **Const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，描述傳回之網格的頂點格式。 此參數必須直接對應至彈性頂點格式， (FVF) 。

</dd> <dt>

*pD3DDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，也就是要與網格相關聯的裝置物件。

</dd> <dt>

*ppMesh* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示所建立的網格物件。

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
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
