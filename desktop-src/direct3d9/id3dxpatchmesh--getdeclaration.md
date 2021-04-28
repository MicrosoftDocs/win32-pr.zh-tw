---
description: ID3DXPatchMesh：： GetDeclaration 方法-取得頂點宣告。
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: 'ID3DXPatchMesh：： GetDeclaration 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0fde070b1b013e651c84ffea7098eb8225aed8f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093296"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a>ID3DXPatchMesh：： GetDeclaration 方法

取得頂點宣告。

## <a name="syntax"></a>語法


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDeclaration* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**

描述網格頂點頂點格式的 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 元素陣列。 此宣告子陣列的維度是 [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md)。 頂點元素陣列的結尾是 [**D3DDECL \_ END**](d3ddecl-end.md) 宏。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

專案的陣列包含結束宣告的 [**D3DDECL \_ 結束**](d3ddecl-end.md) 宏。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
