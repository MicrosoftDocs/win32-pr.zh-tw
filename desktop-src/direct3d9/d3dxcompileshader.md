---
description: D3DXCompileShader 函式-編譯著色器檔。
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: 'D3DXCompileShader 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6441e000422c113521803924d7c1fc746cd2c96591463d33677425a49f7edfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988688"
---
# <a name="d3dxcompileshader-function"></a>D3DXCompileShader 函式

編譯著色器檔。

> [!Note]  
> 我們建議您不要使用此舊版函式，而是使用 Fxc.exe 命令列編譯器或使用 [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API，以離線方式編譯。

 

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCompileShader(
  _In_        LPCSTR              pSrcData,
  _In_        UINT                srcDataLen,
  _In_  const D3DXMACRO           *pDefines,
  _In_        LPD3DXINCLUDE       pInclude,
  _In_        LPCSTR              pFunctionName,
  _In_        LPCSTR              pProfile,
  _In_        DWORD               Flags,
  _Out_       LPD3DXBUFFER        *ppShader,
  _Out_       LPD3DXBUFFER        *ppErrorMsgs,
  _Out_       LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrcData* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

包含著色器之字串的指標。

</dd> <dt>

*srcDataLen* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

資料的長度（以位元組為單位）。

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

*pFunctionName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

字串的指標，該字串包含執行開始之著色器進入點函式的名稱。

</dd> <dt>

*pProfile* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

著色器設定檔的指標，此設定檔可決定著色器指令集。 如需可用的配置檔案清單，請參閱 [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) 或 [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) 。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

不同旗標所識別的編譯選項。 Direct3D 10 HLSL 編譯器現在是預設值。 如需詳細資料，請參閱 [D3DXSHADER 旗標](d3dxshader-flags.md) 。

</dd> <dt>

*ppShader* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

傳回包含已建立之著色器的緩衝區。 這個緩衝區包含已編譯的著色器程式碼，以及任何內嵌的 debug 和 symbol 資料表資訊。

</dd> <dt>

*ppErrorMsgs* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

傳回緩衝區，其中包含在編譯期間遇到的錯誤和警告清單。 這些是偵錯工具在偵測模式中執行時所顯示的相同訊息。 這個值可以是 **Null**。

</dd> <dt>

*ppConstantTable* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

傳回 [**ID3DXConstantTable**](id3dxconstanttable.md) 介面，這個介面可以用來存取著色器常數。 這個值可以是 **Null**。 如果您將應用程式編譯為大型位址感知 (也就是說，您可以使用/LARGEADDRESSAWARE 連結器選項來處理大於 2 GB 的位址) ，您無法使用此參數，而且必須將它設定為 **Null**。 相反地，您必須使用 [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) 函式來取出內嵌于著色器中的著色器常數資料表。 在這個 **D3DXGetShaderConstantTableEx** 呼叫中，您必須將 **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** 旗標傳遞給 *Flags* 參數，以指定最多可存取 4 GB 的虛擬位址空間。

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

[**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
