---
description: 根據鑲嵌式層級執行統一鑲嵌。
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: 'ID3DXPatchMesh：： Tessellate 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b94b79a9decd2f44fa1675e257a2401e2ae8f7a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106979886"
---
# <a name="id3dxpatchmeshtessellate-method"></a>ID3DXPatchMesh：： Tessellate 方法

根據鑲嵌式層級執行統一鑲嵌。

## <a name="syntax"></a>語法


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fTessLevel* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

鑲嵌式層級。 這是在現有頂點之間引進的頂點數目。 此浮點數參數的範圍為 0 < fTessLevel <= 32。

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

 

 
