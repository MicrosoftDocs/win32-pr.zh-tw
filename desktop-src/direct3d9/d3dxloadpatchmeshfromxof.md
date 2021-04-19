---
description: 從 ID3DXFileData 物件載入 patch 網狀。
ms.assetid: 8054e33e-6bf8-4a56-9f66-30600732c84f
title: 'D3DXLoadPatchMeshFromXof 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPatchMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa2e75e34927d0bb3c68445b994ee0911adb08f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981249"
---
# <a name="d3dxloadpatchmeshfromxof-function"></a>D3DXLoadPatchMeshFromXof 函式

從 [**ID3DXFileData**](id3dxfiledata.md) 物件載入 patch 網狀。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXLoadPatchMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ PDWORD            pNumMaterials,
  _Out_ LPD3DXPATCHMESH   *ppMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pxofMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

[**ID3DXFileData**](id3dxfiledata.md)介面的指標，代表要載入的檔案資料物件。

</dd> <dt>

*選項* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [**D3DXMESH**](./d3dxmesh.md) 旗標的組合，指定網格的建立選項。

</dd> <dt>

*pD3DDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

用來建立網格之裝置的指標。

</dd> <dt>

*ppMaterials* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

網格中包含的材質陣列。 每個材質都會以 [**ID3DXBuffer**](id3dxbuffer.md) 介面編制索引。

</dd> <dt>

*ppEffectInstances* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

包含效果實例陣列的緩衝區指標，傳回網格中每個屬性群組一個。 效果實例是用來初始化效果之狀態資訊的特定實例。 請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。 如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。

</dd> <dt>

*pNumMaterials* \[擴展\]
</dt> <dd>

類型： **PDWORD**

包含網格中材質數目的指標。

</dd> <dt>

*ppMesh* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

[**ID3DXPatchMesh**](id3dxpatchmesh.md)介面指標的位址，表示已載入的網格。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

對於不包含效果實例資訊的網格檔，將會從. x 檔案中的材質資訊產生預設效果實例。 預設效果實例會有預設值，這些值會對應至 [**D3DMATERIAL9**](d3dmaterial9.md) 結構的成員。

預設紋理名稱也會填入，但會以不同的方式處理。 名稱會是 Texture0@Name ，它會以名稱為 "Texture0" 的 "" 名稱對應至效果變數，並具有稱為 "name" 的注釋。 這會包含材質的字串檔案名。

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

 

 
