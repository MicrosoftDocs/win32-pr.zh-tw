---
description: 將網格分割成小於指定大小的網格。
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: 'D3DXSplitMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aee07e79286867ce11ce394e852fdfc01c6a1e41dc75b8c979838844b4f09d2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298250"
---
# <a name="d3dxsplitmesh-function"></a>D3DXSplitMesh 函式

將網格分割成小於指定大小的網格。

## <a name="syntax"></a>語法


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMeshIn* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

[**ID3DXMesh**](id3dxmesh.md)介面的指標，代表來源網格。

</dd> <dt>

*pAdjacencyIn* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

指標，指向每個臉部的三個 Dword 陣列，以指定要簡化網格中每個臉部的三個相鄰專案。

</dd> <dt>

*MaxSize* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md)**

所產生網格中頂點的最大數目。

</dd> <dt>

*選項* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md)**

新網格的選項旗標。

</dd> <dt>

*pMeshesOut* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

傳回的網格數目。

</dd> <dt>

*ppMeshArrayOut* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

包含新網格 [**ID3DXMesh**](id3dxmesh.md) 介面陣列的緩衝區。 如果來源網格分割成 n 個網格，則 *ppMeshArrayOut* 是 n 個 **ID3DXMesh** 指標的陣列。

</dd> <dt>

*ppAdjacencyArrayOut* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

包含相鄰陣列陣列的緩衝區， (Dword) 用於新的網格。 請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。 這是選擇性參數。

</dd> <dt>

*ppFaceRemapArrayOut* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

包含臉部重新對應陣列陣列的緩衝區， (Dword) 用於新的網格。 請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。 這是選擇性參數。

</dd> <dt>

*ppVertRemapArrayOut* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

包含新網格之頂點重新對應陣列陣列的緩衝區。 請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。 這是選擇性參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

此函式的常見用法是將具有32位索引的網格分割 (超過65535個頂點) 多個網格中，每個網格都有16位的索引。

相鄰、頂點重新對應和臉部重新對應陣列是一個 Dword，其中每個陣列包含 n 個 DWORD 指標，後面接著指標所參考的 DWORD 資料。 例如，若要取得網格2中臉部3的臉部重新對應資訊，可使用下列程式碼，假設臉部重新對應資料是在名為 *ppFaceRemapArrayOut* 的變數中傳回。


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
