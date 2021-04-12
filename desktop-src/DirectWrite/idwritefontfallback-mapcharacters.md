---
title: IDWriteFontFallback MapCharacters 方法
description: 決定用來呈現文字開頭範圍的適當字型。
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- MapCharacters 方法直接寫入
- MapCharacters 方法 Direct Write，IDWriteFontFallback 介面
- IDWriteFontFallback 介面 Direct Write，MapCharacters 方法
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317311"
---
# <a name="idwritefontfallbackmapcharacters-method"></a>IDWriteFontFallback：： MapCharacters 方法

決定用來呈現文字開頭範圍的適當字型。

## <a name="syntax"></a>語法


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*source* 
</dt> <dd>

類型： **[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _

文字來源執行會保存文字和地區設定。

</dd> <dt>

_textPosition * 
</dt> <dd>

類型： **UINT32**

要分析的開始位置。

</dd> <dt>

*textLength* 
</dt> <dd>

類型： **UINT32**

要分析的文字長度。

</dd> <dt>

*baseFontCollection* \[在中，選擇性\]
</dt> <dd>

類型： **[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _

要使用的預設字型集合。

</dd> <dt>

_baseFamilyName * \[ in，選擇性\]
</dt> <dd>

類型： **const wchar \_ t \** _

基底字型的系列名稱。 如果您傳遞 null，則不會對該系列進行任何比對。

</dd> <dt>

_baseWeight * 
</dt> <dd>

類型： **[ **DWRITE \_ 字型 \_ 粗細**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**

所需的權數。

</dd> <dt>

*baseStyle* 
</dt> <dd>

類型： **[ **DWRITE \_ 字型 \_ 樣式**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**

所需的樣式。

</dd> <dt>

*baseStretch* 
</dt> <dd>

類型： **[ **DWRITE \_ 字型 \_ 延展**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**

所需的 stretch。

</dd> <dt>

*mappedLength* \[擴展\]
</dt> <dd>

類型： **UINT32 \** _

對應至對應字型的文字長度。 如果文字長度不是) 零，則這一律會小於或等於文字長度，並大於零 (，讓呼叫端前進至少一個字元。

</dd> <dt>

_mappedFont * \[ out\]
</dt> <dd>

類型： **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

應該用來呈現文字的第一個 *mappedLength* 字元的字型。 如果傳回 Null，這表示沒有字型可以轉譯文字，而 *mappedLength* 是要跳過的字元數 (以遺漏的圖像) 呈現。

</dd> <dt>

*調整規模* \[擴展\]
</dt> <dd>

類型： **FLOAT \** _

縮放比例，以將所傳回字型的 em 大小乘以。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                 |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

