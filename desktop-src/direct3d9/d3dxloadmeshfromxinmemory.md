---
description: 從記憶體載入網格。
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: 'D3DXLoadMeshFromXInMemory 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 66b07a88a938b09217a2fee2b9eed272233edc75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982207"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a>D3DXLoadMeshFromXInMemory 函式

從記憶體載入網格。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*記憶體* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

包含網格資料之記憶體緩衝區的指標。

</dd> <dt>

*SizeOfMemory* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

檔案在記憶體中的大小（以位元組為單位）。

</dd> <dt>

*選項* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

結合 [**D3DXMESH**](./d3dxmesh.md) 列舉中的一或多個旗標，指定網格的建立選項。

</dd> <dt>

*pD3DDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與網格相關聯的裝置物件。

</dd> <dt>

*ppAdjacency* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。 當方法傳回時，此參數會填入三個 Dword 的陣列，每個臉部會針對網格中的每個臉部指定三個相鄰專案。

</dd> <dt>

*ppMaterials* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。 當此方法傳回時，此參數會填入 [**D3DXMATERIAL**](d3dxmaterial.md) 結構的陣列，其中包含儲存在 DirectX 檔案中的資訊。

</dd> <dt>

*ppEffectInstances* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

包含效果實例陣列的緩衝區指標，傳回網格中每個屬性群組一個。 效果實例是用來初始化效果之狀態資訊的特定實例。 請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。 如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。

</dd> <dt>

*pNumMaterials* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

當方法傳回時，為 *ppMaterials* 陣列中 [**D3DXMATERIAL**](d3dxmaterial.md)結構數目的指標。

</dd> <dt>

*ppMesh* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示已載入的網格。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

檔案中的所有網格都將折迭成一個輸出網格。 如果檔案包含框架階層，則所有轉換都會套用至網格。

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

 

 
