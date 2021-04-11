---
description: 將格式化的文字載入視訊記憶體，以改善轉譯至裝置的效率。 這個方法支援 ANSI 和 Unicode 字串。
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: 'ID3DX10Font：:P reloadText 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7294fb7e86b3532960a34a15e1118dc33f748f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196277"
---
# <a name="id3dx10fontpreloadtext-method"></a>ID3DX10Font：:P reloadText 方法

將格式化的文字載入視訊記憶體，以改善轉譯至裝置的效率。 這個方法支援 ANSI 和 Unicode 字串。

## <a name="syntax"></a>語法


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pString* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

要載入視訊記憶體的字元字串指標。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR;否則，資料型別會解析為 LPCSTR。 請參閱＜備註＞。

</dd> <dt>

*計數* \[在\]
</dt> <dd>

類型： **[ **INT**](../winprog/windows-data-types.md)**

文字字串中的字元數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 PreloadTextW。 否則，函式呼叫會解析為 PreloadTextA，因為正在使用 ANSI 字串。

這個方法會產生包含代表輸入文字之字元的材質。 圖像會繪製成一系列的三角形。

系統不會將文字轉譯至裝置;ID3DX10Font：仍然必須呼叫:D rawText，才能呈現文字。 不過，藉由將文字預先載入視訊記憶體，ID3DX10Font：:D rawText 將會使用明顯較少的 CPU 資源。

這個方法會在內部使用 GDI 函數 [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85))將字元轉換成字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
