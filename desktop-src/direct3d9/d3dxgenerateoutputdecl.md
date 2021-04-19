---
description: 從輸入宣告產生輸出頂點宣告。 輸出宣告適用于網格鑲嵌函數。
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: 'D3DXGenerateOutputDecl 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGenerateOutputDecl
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3fed752e74df3afa812c228a174503e20c6adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989195"
---
# <a name="d3dxgenerateoutputdecl-function"></a>D3DXGenerateOutputDecl 函式

從輸入宣告產生輸出頂點宣告。 輸出宣告適用于網格鑲嵌函數。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pOutput* \[擴展\]
</dt> <dd>

類型： **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***

輸出頂點宣告的指標。 請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。

</dd> <dt>

*pInput* \[在\]
</dt> <dd>

Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

輸入頂點宣告的指標。 請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




