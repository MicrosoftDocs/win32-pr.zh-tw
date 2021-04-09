---
description: 驗證 patch 網狀，以傳回退化頂點和修補程式的數目。
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: 'D3DXValidPatchMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87d7fbe15c78a8b768d845e6a23cc084b69f3e02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946079"
---
# <a name="d3dxvalidpatchmesh-function"></a>D3DXValidPatchMesh 函式

驗證 patch 網狀，以傳回退化頂點和修補程式的數目。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMeshIn* \[在\]
</dt> <dd>

類型： **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**

[**ID3DXPatchMesh**](id3dxpatchmesh.md)介面的指標，代表要測試的修補程式網格。

</dd> <dt>

*pNumDegenerateVertices* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

傳回修補程式網格中的退化頂點數目。

</dd> <dt>

*pNumDegeneratePatches* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

傳回修補程式網格中的退化修補程式數目。

</dd> <dt>

*ppErrorsAndWarnings* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

傳回包含錯誤和警告字串的緩衝區指標，以說明在修補程式網格中找到的問題。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

這個方法會檢查是否有不正確索引來驗證網格。 您可以從偵錯工具輸出取得錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
