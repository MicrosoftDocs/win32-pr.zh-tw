---
description: 取得所有著色器輸出元素的語法。
ms.assetid: 1a3cdd5d-0ea7-48ae-a3f1-030e95b03a42
title: 'D3DXGetShaderOutputSemantics 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderOutputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 264db967d2959c2f6e5096e0362e9db576ba9f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514593"
---
# <a name="d3dxgetshaderoutputsemantics-function"></a>D3DXGetShaderOutputSemantics 函式

取得所有著色器輸出元素的語法。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXGetShaderOutputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFunction* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

著色器函式 DWORD 資料流程的指標。

</dd> <dt>

*pSemantics* \[在\]
</dt> <dd>

類型： **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***

[**D3DXSEMANTIC**](d3dxsemantic.md)結構陣列的指標。 此函式會使用著色器所參考之每個輸出專案的語義來填滿此陣列。 此陣列假設至少包含 MAXD3DDECLLENGTH 元素。 不過，使用 pSemantics = **Null** 呼叫 **D3DXGetShaderOutputSemantics** 會傳回 pCount 所需的元素數目。

</dd> <dt>

*pCount* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

傳回 pSemantics 中的元素數目。

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

 

 
