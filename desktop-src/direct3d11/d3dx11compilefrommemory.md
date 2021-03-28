---
title: 'D3DX11CompileFromMemory 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 Fxc.exe 命令列編譯器，或使用其中一個 HLSL 編譯 Api （例如 D3DCompile API），以離線方式編譯。 編譯已載入記憶體中的著色器或效果。
ms.assetid: 3396560f-f411-4c66-9f22-03c0050c74b0
keywords:
- D3DX11CompileFromMemory 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e10590c3db458a23bf4d52b6507146884630087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974616"
---
# <a name="d3dx11compilefrommemory-function"></a>D3DX11CompileFromMemory 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

> [!Note]  
> 我們建議您不要使用這個函式，而是使用 Fxc.exe 命令列編譯器，或使用其中一個 HLSL 編譯 Api （例如 [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API），以離線方式編譯。

 

編譯已載入記憶體中的著色器或效果。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrcData* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

記憶體中著色器的指標。

</dd> <dt>

*SrcDataLen* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**

記憶體中的著色器大小。

</dd> <dt>

*pFileName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

包含著色器程式碼的檔案名。

</dd> <dt>

*pDefines* \[在\]
</dt> <dd>

Type： **Const [**D3D10 \_ 著色器 \_ 宏**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

選擇性。 巨集定義陣列的指標 (參閱 [**D3D10 \_ 著色器 \_ 宏**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) 。 陣列中的最後一個結構作為結束字元，且必須將所有成員設定為0。 如果未使用，請將 *pDefines* 設定為 **Null**。

</dd> <dt>

*pInclude* \[在\]
</dt> <dd>

類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

選擇性。 處理 include 檔之介面的指標。 若將此 **值** 設定為 Null，將會導致編譯錯誤（如果著色器包含） \# 。

</dd> <dt>

*pFunctionName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

著色器開始執行的著色器輸入點函式名稱。 當您編譯效果時， **D3DX11CompileFromMemory** 會忽略 *pFunctionName*;建議您將 *pFunctionName* 設定為 **null** ，因為如果所呼叫的函式不會使用它，則將指標參數設定為 **null** ，是很好的程式設計作法。

</dd> <dt>

*pProfile* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

指定著色器模型的字串。可以是著色器模型2、著色器模型3、著色器模型4或著色器模型5中的任何設定檔。 設定檔也可以是適用于效果類型 (例如 fx \_ 4 \_ 1) 。

</dd> <dt>

*Flags1* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

著色器 [**編譯旗標**](/windows/desktop/direct3dhlsl/d3dcompile-constants)。

</dd> <dt>

*Flags2* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

效果 [**編譯旗標**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)。 當您編譯著色器而非效果檔案時， **D3DX11CompileFromMemory** 會忽略 *Flags2*;我們建議您將 *Flags2* 設定為零，因為如果所呼叫的函式不會使用它，則將指標參數設定為零是很好的程式設計作法。

</dd> <dt>

*pPump* \[在\]
</dt> <dd>

類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

執行緒抽取介面的指標 (查看 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)) 。 使用 **Null** 來指定此函式必須等到完成後才會傳回。

</dd> <dt>

*ppShader* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

記憶體的指標，其中包含已編譯的著色器，以及任何內嵌的 debug 和符號表資訊。

</dd> <dt>

*ppErrorMsgs* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

記憶體的指標，其中包含在編譯期間發生的錯誤和警告清單。 這些錯誤和警告與偵錯工具的偵錯工具輸出完全相同。

</dd> <dt>

*pHResult* \[擴展\]
</dt> <dd>

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

傳回值的指標。 可能是 **Null**。 如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

如果您將 \_ **null** 提供給 *pPump* 參數，則 D3DX11CompileFromMemory 會傳回 E INVALIDARG，如果您將非 **null** 提供給 *pHResult* 參數。 如需這種情況的詳細資訊，請參閱備註。

## <a name="remarks"></a>備註

如需 **D3DX11CompileFromMemory** 的詳細資訊，請參閱 [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile)。

如果您也提供 **null** 給 *pPump* 參數，則必須將 **null** 提供給 *pHResult* 參數。 否則，您接著無法使用 **D3DX11CompileFromMemory** 在 *ppShader* 參數指向的記憶體中傳回的已編譯著色器程式碼來建立著色器。 若要從編譯的著色器程式碼建立著色器，請呼叫下列其中一個 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 介面方法：

-   [**CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [**CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**CreatePixelShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

此外，如果您在提供 **null** 給 *pPump* 時，將非 **Null** 值提供給 *pHResult* ， **D3DX11CompileFromMemory** 就會傳回 E \_ INVALIDARG 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11async。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

