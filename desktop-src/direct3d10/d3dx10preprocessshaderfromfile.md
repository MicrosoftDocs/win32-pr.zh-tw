---
description: 請注意，我們建議您不要使用此舊版函式，而是使用 D3DPreprocess API。 在不編譯的情況下，從檔案建立著色器。
ms.assetid: 9f609aa5-5ee7-45fb-9693-69de130b6cc0
title: D3DX10PreprocessShaderFromFile 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e227ebf001e1af6beac21403d93201c758a63acf96aa5e1daa78b1c8fa506654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128352"
---
# <a name="d3dx10preprocessshaderfromfile-function"></a>D3DX10PreprocessShaderFromFile 函式

> [!Note]  
> 我們建議您不要使用此舊版函式，而是使用 [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API。

 

在不編譯的情況下，從檔案建立著色器。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFileName* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

著色器檔案名。

</dd> <dt>

*pDefines* \[在\]
</dt> <dd>

Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

著色器宏的 Null 終止陣列 (查看 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) ; 將此值設定為 **Null** 以指定無宏。

</dd> <dt>

*pInclude* \[在\]
</dt> <dd>

類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

包含介面的指標 (查看 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))) ;將此設為 **Null** ，以指定沒有包含檔。

</dd> <dt>

*pPump* \[在\]
</dt> <dd>

類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。 使用 **Null** 來指定此函式必須等到完成後才會傳回。

</dd> <dt>

*ppShaderText* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

記憶體指標 (查看包含未編譯著色器的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。

</dd> <dt>

*ppErrorMsgs* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

記憶體指標的位址 (查看包含效果建立錯誤（如果有發生）的 [**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Async。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
