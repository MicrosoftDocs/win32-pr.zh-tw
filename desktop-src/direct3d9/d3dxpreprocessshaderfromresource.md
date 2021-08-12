---
description: 在不執行編譯的情況下，預處理著色器資源。 這會解析所有的 \# 定義和 \# 包含，提供適用于後續編譯的獨立著色器。
ms.assetid: a00c2db9-d7ba-48ab-80e3-dc20774e1b1e
title: 'D3DXPreprocessShaderFromResource 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 235b1146cd589d09d4718f938f15e7250fdb57993295d48eaa94290abe1cd52f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298516"
---
# <a name="d3dxpreprocessshaderfromresource-function"></a>D3DXPreprocessShaderFromResource 函式

在不執行編譯的情況下，預處理著色器資源。 這會解析所有的 \# 定義和 \# 包含，提供適用于後續編譯的獨立著色器。

> [!Note]  
> 我們建議您不要使用此舊版函式，而是使用 [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API。

 

## <a name="syntax"></a>語法


```C++
HRESULT D3DXPreprocessShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCSTR        pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSrcModule* \[在\]
</dt> <dd>

類型： **[ **HMODULE**](../winprog/windows-data-types.md)**

保存著色器資源之模組的控制碼。 如果這個值為 **Null**，則會使用目前的模組。

</dd> <dt>

*pSrcResource* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

代表模組中資源名稱的字串。

</dd> <dt>

*pDefines* \[在\]
</dt> <dd>

Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***

[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列。 這個值可以是 **Null**。

</dd> <dt>

*pInclude* \[在\]
</dt> <dd>

類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。 如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。

</dd> <dt>

*ppShaderText* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

傳回包含單一大型字串的緩衝區，代表產生的格式化權杖資料流程。

</dd> <dt>

*ppErrorMsgs* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

傳回緩衝區，其中包含在編譯期間遇到的錯誤和警告清單。 這些是偵錯工具在偵測模式中執行時所顯示的相同訊息。 這個值可以是 **Null**。

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
</dt> <dt>

[**D3DXPreprocessShaderFromFile**](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[**D3DXPreprocessShader**](d3dxpreprocessshader.md)
</dt> </dl>

 

 
