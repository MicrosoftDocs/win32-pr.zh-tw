---
description: 從編譯的著色器建立紋理著色器物件。
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: 'D3DXCreateTextureShader 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c32715f1b939d30acb53b1cbe07e081d43d21823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322939"
---
# <a name="d3dxcreatetextureshader-function"></a>D3DXCreateTextureShader 函式

從編譯的著色器建立紋理著色器物件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFunction* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

函數 DWORD 資料流程的指標。

</dd> <dt>

*ppTextureShader* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***

傳回 [**ID3DXTextureShader**](id3dxtextureshader.md) 物件，這個物件可以用來 Cti 使用 [**D3DXFillTextureTX**](d3dxfilltexturetx.md) 函式填滿材質的內容。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器函式](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
