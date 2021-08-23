---
description: 請注意，我們建議您不要使用此舊版函式，而是使用 D3DDisassemble API。 這個函式--將已編譯的著色器反組解碼為包含元件指令和註冊指派的文字字串--不存在。
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: 'D3DX10DisassembleShader 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: bd69b6dc2cede96e6ca07983195d202cfd248633f44a13fe1967393c446ca329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753218"
---
# <a name="d3dx10disassembleshader-function"></a>D3DX10DisassembleShader 函式

> [!Note]  
> 我們建議您不要使用此舊版函式，而是使用 [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API。

 

這個函式--將已編譯的著色器反組解碼為包含元件指令和註冊指派的文字字串--不存在。 相反地，請使用 [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect)。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pShader* \[在\]
</dt> <dd>

類型： **const void \***

[**已編譯之著色器**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout)的指標。

</dd> <dt>

*BytecodeLength* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**

PShader 的大小。

</dd> <dt>

*EnableColorCode* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

在輸出中包含 HTML 標籤，以將結果色彩編碼。

</dd> <dt>

*pComments* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

著色器頂端的批註字串，可識別著色器的常數和變數。

</dd> <dt>

*ppDisassembly* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

緩衝區的位址 (參閱 [**ID3D10Blob 介面**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) ，其中包含已拆解的著色器。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

這項傳回的文字包含一個標頭，其中包含用來產生此物件的 HLSL 編譯器版本、描述著色器所使用之常數緩衝區記憶體配置的批註、輸入和輸出簽章，以及資源系結點。

以下是將已編譯的著色器分解的範例。 此範例假設您從已編譯的著色器開始 (顯示為 *pVSBuf* ，您可以在 [HLSLWithoutFX10 範例](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)) 中看到。


```
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleShader( (UINT*) pVSBuf->GetBufferPointer(), 
        pVSBuf->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "shader.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Core。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
