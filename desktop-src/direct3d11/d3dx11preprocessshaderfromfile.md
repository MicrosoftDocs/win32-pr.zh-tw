---
title: 'D3DX11PreprocessShaderFromFile 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用此函式，而是使用 D3DPreprocess API。 在不編譯的情況下，從檔案建立著色器。
ms.assetid: aab08efd-b6b0-44e5-bd68-f32c242d9e94
keywords:
- D3DX11PreprocessShaderFromFile 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00ef5c7c9a00475ead0904cbf62d6d21fd647ce0de9fe402d1499dac7ee1bd09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124663"
---
# <a name="d3dx11preprocessshaderfromfile-function"></a>D3DX11PreprocessShaderFromFile 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

> [!Note]  
> 我們建議您不要使用此函式，而是使用 [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API。

 

在不編譯的情況下，從檔案建立著色器。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFileName* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

著色器檔案名。

</dd> <dt>

*pDefines* \[在\]
</dt> <dd>

Type： **CONST D3D11 \_ 著色 \_ 器 \* 宏**

以 Null 結束的著色器宏陣列;將此設為 **Null** ，以指定無宏。

</dd> <dt>

*pInclude* \[在\]
</dt> <dd>

類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

包含介面的指標;將此設為 **Null** ，以指定沒有包含檔。

</dd> <dt>

*pPump* \[在\]
</dt> <dd>

類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

執行緒抽取介面的指標 (查看 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)) 。 使用 **Null** 來指定此函式必須等到完成後才會傳回。

</dd> <dt>

*ppShaderText* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

記憶體的指標，其中包含未編譯的著色器。

</dd> <dt>

*ppErrorMsgs* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

記憶體指標的位址，其中包含效果建立錯誤（如果有發生的話）。

</dd> <dt>

*pHResult* \[擴展\]
</dt> <dd>

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

傳回值的指標。 可能是 **Null**。 如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11async。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

