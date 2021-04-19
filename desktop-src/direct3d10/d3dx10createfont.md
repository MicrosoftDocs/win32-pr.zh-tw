---
description: 建立裝置和字型的字型物件。請注意，我們建議您不要使用這個函式，而是使用 DirectWrite 和 DirectXTK library SpriteFont 類別。
ms.assetid: a0dd02f1-c512-46d3-9e83-a785ac3ad7ee
title: 'D3DX10CreateFont 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFont
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6e5966e50c9c997085d35854868a2a7dd0455c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975685"
---
# <a name="d3dx10createfont-function"></a>D3DX10CreateFont 函式

建立裝置和字型的字型物件。

> [!Note]  
> 我們建議您不要使用這個函式，而是使用 [DirectWrite](../directwrite/direct-write-portal.md) 和 [DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 **SpriteFont** 類別。

 

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10CreateFont(
  _In_  ID3D10Device *pDevice,
  _In_  INT          Height,
  _In_  UINT         Width,
  _In_  UINT         Weight,
  _In_  UINT         MipLevels,
  _In_  BOOL         Italic,
  _In_  UINT         CharSet,
  _In_  UINT         OutputPrecision,
  _In_  UINT         Quality,
  _In_  UINT         PitchAndFamily,
  _In_  LPCTSTR      pFaceName,
  _Out_ LPD3DX10FONT *ppFont
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

ID3D10Device 介面的指標，與字型物件相關聯的裝置。

</dd> <dt>

*高度* \[在\]
</dt> <dd>

類型： **[ **INT**](../winprog/windows-data-types.md)**

邏輯單元中字元的高度。

</dd> <dt>

*寬度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

邏輯單元中字元的寬度。

</dd> <dt>

*權數* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

字型權數。 其中一個範例是粗體。

</dd> <dt>

*MipLevels* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

Mipmap 層級的數目。

</dd> <dt>

*斜體* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

若為斜體字型，則為 True，否則為 false。

</dd> <dt>

*字元集* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

字型的字元集。

</dd> <dt>

*OutputPrecision* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

指定 Windows 應該如何嘗試符合所需的字型大小和特性與實際字型。 \_ \_ 例如，只使用 OUT TT \_ PRECIS，以確保一律取得 TrueType 字型。

</dd> <dt>

*品質* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

指定 Windows 如何以真實字型符合所需的字型。 它只適用于點陣字型，不應該影響 TrueType 字型。

</dd> <dt>

*PitchAndFamily* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

音調和系列索引。

</dd> <dt>

*pFaceName* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

包含字樣名稱的字串。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，資料型別會解析為 LPCSTR。 請參閱＜備註＞。

</dd> <dt>

*ppFont* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DX10FONT**](id3dx10font.md)\***

傳回 ID3DX10Font 介面的指標，表示所建立的字型物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為 S \_ OK。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXCreateFontW。 否則，函式呼叫會解析為 D3DXCreateFontA，因為正在使用 ANSI 字串。

如果您需要有關字型參數的詳細資訊，請參閱 [邏輯字型](/previous-versions//ms533985(v=vs.85))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
