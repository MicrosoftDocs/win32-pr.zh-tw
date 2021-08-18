---
description: 定義4位元組陣列，其中包含 4 8 位的空格、a-z 或 a-z 的 ASCII 值，以識別 OpenType 腳本、語言和字型功能標記。
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: 'OPENTYPE_TAG (Usp10) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c784fa7f6243e7e5444dcbc64c690ce7184d6ace469759c19be9de87854732
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040778"
---
# <a name="opentype_tag"></a>OPENTYPE \_ 標記

定義4位元組陣列，其中包含 4 8 位的空格、a-z 或 a-z 的 ASCII 值，以識別 OpenType 腳本、語言和字型功能標記。


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a>備註

下列範例會定義 OpenType 功能標記的標記法。

-   連字功能的功能標記為 "liga"。
-   適用于羅馬尼亞文、烏爾即文和波斯文的語言標記分別為「ROM」、「URD」和「遠」。 請注意，每個標記的結尾都是空格。
-   拉丁和阿拉伯文腳本的腳本標記分別為 "latn" 和 "阿拉伯"。

如需 OpenType 功能標記和 OpenType 規格的詳細資訊，請參閱 <https://www.microsoft.com/typography/otspec/featuretags.htm> 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 可轉散發套件<br/>          | Usp10.dll 1.600 版或更高版本的于 windows 展開 x) <br/>                |
| 標頭<br/>                   | <dl> <dt>Usp10。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Uniscribe 結構](uniscribe-structures.md)
</dt> <dt>

[**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




