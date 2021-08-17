---
description: 取得矩形 patch 的大小。
ms.assetid: d25373ef-789d-4515-83da-7049f040c9a4
title: 'D3DXRectPatchSize 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRectPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 51b00ab5ffcd0fa88d3523412c0f340404bbdd782bed6f3f01e1b5f7ee1ca91b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460118"
---
# <a name="d3dxrectpatchsize-function"></a>D3DXRectPatchSize 函式

取得矩形 patch 的大小。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXRectPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pwdVertices
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pfNumSegs* \[在\]
</dt> <dd>

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

要 tessellate 的每個邊緣區段數目。

</dd> <dt>

*pdwTriangles* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

DWORD 的指標，其中包含修補程式中的三角形數目。

</dd> <dt>

*pwdVertices* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

DWORD 的指標，其中包含修補程式中的頂點數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
