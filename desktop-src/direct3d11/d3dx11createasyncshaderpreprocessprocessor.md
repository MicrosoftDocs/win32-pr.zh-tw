---
title: 'D3DX11CreateAsyncShaderPreprocessProcessor 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。 以非同步方式建立著色器的資料處理器。
ms.assetid: a7e9754b-acc1-49d0-bd8e-b116bc3c7e3a
keywords:
- D3DX11CreateAsyncShaderPreprocessProcessor 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderPreprocessProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e58b267f186e5fd0104b10e9f9423f407aaf13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946180"
---
# <a name="d3dx11createasyncshaderpreprocessprocessor-function"></a>D3DX11CreateAsyncShaderPreprocessProcessor 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。

 

以非同步方式建立著色器的資料處理器。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFileName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

包含著色器檔案名的字串。

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

*ppShaderText* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

緩衝區指標的位址，其中包含著色器的 ASCII 文字。

</dd> <dt>

*ppErrorBuffer* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

包含編譯錯誤之緩衝區的指標位址。

</dd> <dt>

*ppDataProcessor* \[擴展\]
</dt> <dd>

類型： **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX11DataProcessor 介面**](id3dx11dataprocessor.md)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。

針對 Windows Store 應用程式， (的 DirectX 範例，例如 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。

針對 Win32 傳統型應用程式，您可以使用 [並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) 來執行類似于 Windows 執行階段非同步程式設計模型的內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11async。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

