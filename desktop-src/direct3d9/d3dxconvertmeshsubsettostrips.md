---
description: 將指定的網格子集轉換成一連串的條紋。
ms.assetid: 4f005383-6a5a-4393-ac88-202e45946d3d
title: 'D3DXConvertMeshSubsetToStrips 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToStrips
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d62461c13f76eb0efce809fa1114771a5ea2fe6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000621"
---
# <a name="d3dxconvertmeshsubsettostrips-function"></a>D3DXConvertMeshSubsetToStrips 函式

將指定的網格子集轉換成一連串的條紋。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXConvertMeshSubsetToStrips(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices,
  _Out_ LPD3DXBUFFER           *ppStripLengths,
  _Out_ DWORD                  *pNumStrips
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MeshIn* \[在\]
</dt> <dd>

類型： **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

[**ID3DXBaseMesh**](id3dxbasemesh.md)介面的指標，代表要轉換成條紋的網格。

</dd> <dt>

*AttribId* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

要轉換成條紋之網格子集的屬性識別碼。

</dd> <dt>

*IBOptions* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

結合 [**D3DXMESH**](./d3dxmesh.md) 列舉中的一或多個旗標，指定建立索引緩衝區的選項。 不可為 D3DXMESH \_ 32 位。 根據 *MeshIn* 參數所指定之網格的索引緩衝區格式，將會使用32位或16位索引來建立索引緩衝區。

</dd> <dt>

*ppIndexBuffer* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

[**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)介面的指標，代表包含該帶的索引緩衝區。

</dd> <dt>

*pNumIndices* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

在 *ppIndexBuffer* 參數中傳回之緩衝區中的索引數目。

</dd> <dt>

*ppStripLengths* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

緩衝區，其中包含一個 DWORD 的陣列，每個區域會指定該區域內的三角形數目。

</dd> <dt>

*pNumStrips* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

索引緩衝區中的個別條紋數目和對應的帶長度陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

在執行此函式之前，請呼叫 [**Optimize**](id3dxmesh--optimize.md) 或 [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)，並 \_ 設定 D3DXMESHOPT ATTRSORT 旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
