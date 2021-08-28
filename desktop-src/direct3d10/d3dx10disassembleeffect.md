---
description: 請注意，我們建議您不要使用此舊版函式，而是使用 D3DDisassemble API。 此函式會將已編譯的效果反組解碼為包含元件指令和註冊指派的文字字串--已被取代。
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: 'D3DX10DisassembleEffect 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 282dcbb91013e5e8bf6def540809fa3afdb3bca40e2a2fd5250c5b3c92877af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753278"
---
# <a name="d3dx10disassembleeffect-function"></a>D3DX10DisassembleEffect 函式

> [!Note]  
> 我們建議您不要使用此舊版函式，而是使用 [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API。

 

此函式會將已編譯的效果反組解碼為包含元件指令和註冊指派的文字字串--已被取代。 相反地，請使用 [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect)。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pEffect* \[在\]
</dt> <dd>

類型： **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***

效果介面的指標 (查看 [**ID3D10Effect 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)) 。

</dd> <dt>

*EnableColorCode* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

在輸出中包含 HTML 標籤，以將結果色彩編碼。

</dd> <dt>

*ppDisassembly* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

緩衝區的位址 (查看包含拆解效果的 [**ID3D10Blob 介面**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Core。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
