---
description: 根據以 z 為基礎的調適型鑲嵌準則，執行適應性鑲嵌。
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'ID3DXPatchMesh：： TessellateAdaptive 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4cc6c6b7ff7b0cdb99e56386df49529f26c9166
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992332"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a>ID3DXPatchMesh：： TessellateAdaptive 方法

根據以 z 為基礎的調適型鑲嵌準則，執行適應性鑲嵌。

## <a name="syntax"></a>語法


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTrans* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***

指定以頂點表示的4D 向量，以取得每個頂點的自我調整鑲嵌量。 每個邊緣都會鑲嵌至它所連接的兩個頂點的鑲嵌層平均值。

</dd> <dt>

*dwMaxTessLevel* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

適應性鑲嵌的最大限制。 這是在現有頂點之間引進的頂點數目。 這個整數值的範圍可以從1到32（含）。

</dd> <dt>

*dwMinTessLevel* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

適應性鑲嵌的最小限制。 這是在現有頂點之間引進的頂點數目。 這個整數值的範圍可以從1到32（含）。

</dd> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

產生的鑲嵌網格。 請參閱 [**ID3DXMesh**](id3dxmesh.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

如果已使用 [**ID3DXPatchMesh：： Optimize**](id3dxpatchmesh--optimize.md)將修補程式網格優化，此函式將會更有效率地執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
