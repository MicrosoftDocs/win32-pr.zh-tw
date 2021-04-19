---
description: 將網格儲存至 x 檔案。
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: 'D3DXSaveMeshToX 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 504e7ad69b83c67dad52ebbf0f6d1eef8639a9fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976703"
---
# <a name="d3dxsavemeshtox-function"></a>D3DXSaveMeshToX 函式

將網格儲存至 x 檔案。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFilename* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

指定檔案名之字串的指標。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，字串資料類型會解析為 LPCSTR。 請參閱＜備註＞。

</dd> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

[**ID3DXMesh**](id3dxmesh.md)介面的指標，代表要儲存至 x.x 檔案的網格。

</dd> <dt>

*pAdjacency* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

指標，指向每個臉部的三個 Dword 陣列，為網格中的每個臉部指定三個相鄰專案。 這個參數可以是 **Null**。

</dd> <dt>

*pMaterials* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATERIAL**](d3dxmaterial.md) \***

[**D3DXMATERIAL**](d3dxmaterial.md)結構陣列的指標，其中包含要儲存在. x 檔案中的材質資訊。

</dd> <dt>

*pEffectInstances* \[在\]
</dt> <dd>

Type： **Const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

效果實例陣列的指標，網格中的每個屬性群組都有一個。 這個參數可以是 **Null**。 效果實例是用來初始化效果之狀態資訊的特定實例。 如需詳細資訊，請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。

</dd> <dt>

*NumMaterials* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

*PMaterials* 陣列中的 [**D3DXMATERIAL**](d3dxmaterial.md)結構數目。

</dd> <dt>

*格式* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

儲存. x 檔案時，檔案格式和儲存選項的組合。 請參閱 [D3DX X 檔案常數](dx9-graphics-reference-d3dx-x-file-constants.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXSaveMeshToXW。 否則，函式呼叫會解析為 D3DXSaveMeshToXA，因為正在使用 ANSI 字串。

預設檔案格式為 binary;但是，如果同時將檔案指定為二進位檔和文字檔，則會將它儲存為文字檔。 無論檔案格式為何，您也可以使用壓縮格式來減少檔案大小。

以下是如何使用此函數的一般程式碼範例。


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 
