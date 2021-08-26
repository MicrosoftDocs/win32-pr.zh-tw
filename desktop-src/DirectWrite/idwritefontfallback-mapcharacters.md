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
ms.openlocfilehash: 99f18932121d44f61d67c8124faa2d26638035bdcff473ad26c4222ceea9a85b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048788"
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

類型： **[ **IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\***

文字來源執行會保存文字和地區設定。

</dd> <dt>

*textPosition* 
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

類型： **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\***

要使用的預設字型集合。

</dd> <dt>

*baseFamilyName* \[在中，選擇性\]
</dt> <dd>

Type： **const wchar \_ t \***

基底字型的系列名稱。 如果您傳遞 null，則不會對該系列進行任何比對。

</dd> <dt>

*baseWeight* 
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

類型： **UINT32 \***

對應至對應字型的文字長度。 如果文字長度不是) 零，則這一律會小於或等於文字長度，並大於零 (，讓呼叫端前進至少一個字元。

</dd> <dt>

*mappedFont* \[擴展\]
</dt> <dd>

類型： **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

應該用來呈現文字的第一個 *mappedLength* 字元的字型。 如果傳回 Null，這表示沒有字型可以轉譯文字，而 *mappedLength* 是要跳過的字元數 (以遺漏的圖像) 呈現。

</dd> <dt>

*調整規模* \[擴展\]
</dt> <dd>

類型： **FLOAT \***

縮放比例，以將所傳回字型的 em 大小乘以。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                 |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

