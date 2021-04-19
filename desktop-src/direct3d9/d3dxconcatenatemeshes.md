---
description: 將網格群組串連成一個常見的網格。 這個方法可以選擇性地將矩陣轉換套用到每個輸入網格及其材質座標。
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: 'D3DXConcatenateMeshes 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b96fe47a3d818c382b35a93708ac51b60e891841
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981842"
---
# <a name="d3dxconcatenatemeshes-function"></a>D3DXConcatenateMeshes 函式

將網格群組串連成一個常見的網格。 這個方法可以選擇性地將矩陣轉換套用到每個輸入網格及其材質座標。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppMeshes* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

輸入網格指標的陣列 (參閱 [**ID3DXMesh**](id3dxmesh.md)) 。 陣列中的元素數目是 NumMeshes。

</dd> <dt>

*NumMeshes* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要串連的輸入網格數目。

</dd> <dt>

*選項* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

網狀建立選項;這是一或多個 [**D3DXMESH**](./d3dxmesh.md) 旗標的組合。 網格建立選項相當於 [**D3DXCreateMesh**](d3dxcreatemesh.md)所需的 options 參數。

</dd> <dt>

*pGeomXForms* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

幾何轉換的選擇性陣列。 陣列中的元素數目為 NumMeshes;每個元素都是轉換矩陣 (請參閱 [**D3DXMATRIX**](d3dxmatrix.md)) 。 可能是 **Null**。

</dd> <dt>

*pTextureXForms* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

紋理轉換的選擇性陣列。 陣列中的元素數目為 NumMeshes;每個元素都是轉換矩陣 (請參閱 [**D3DXMATRIX**](d3dxmatrix.md)) 。 這個參數可以是 **Null**。

</dd> <dt>

*pDecl* \[在\]
</dt> <dd>

Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

頂點宣告的選擇性指標 (查看 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)) 。 這個參數可以是 **Null**。

</dd> <dt>

*pD3DDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

用來建立新網格之 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 裝置的指標。

</dd> <dt>

*ppMeshOut* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

所建立之網狀 (的指標位址，請參閱 [**ID3DXMesh**](id3dxmesh.md)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為 S \_ OK。 如果函式失敗，則傳回值可以是下列其中一個： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

如果在選項網格建立參數中未提供任何 [頂點](vertex-declaration.md) 宣告，方法會產生 submeshes 之所有頂點宣告的聯集，並在必要時升階通道和類型。 方法將會從輸入網格的屬性工作表建立屬性資料表。 為確保建立屬性工作表，請呼叫 [**Optimize**](id3dxmesh--optimize.md) With 旗標設定為 D3DXMESHOPT \_ COMPACT and D3DXMESHOPT \_ ATTRSORT (參閱 [**D3DXMESHOPT**](./d3dxmeshopt.md)) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
