---
description: 下列函式會與字元集一起使用。
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Unicode 和字元集函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd26edd8931b1a63887816ca07698d779bd0d4d3decceb3b53faf5d499605612
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811709"
---
# <a name="unicode-and-character-set-functions"></a>Unicode 和字元集函數

下列函式會與字元集一起使用。



| 函式                                                       | 描述                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**GetTextCharset**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | 針對目前在指定的裝置內容中選取的字型抓取字元集識別碼。         |
| [**GetTextCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | 抓取目前在指定的裝置內容中，所選字型字元集的相關資訊。 |
| [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | 判斷指定的字元是否為 system default Windows ANSI 字碼頁 (CP ACP) 的前導位元組 \_ 。           |
| [**IsDBCSLeadByteEx**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | 判斷指定的字元是否可能是前導位元組。                                                       |
| [**IsTextUnicode**](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | 判斷緩衝區是否可能包含 Unicode 文字的格式。                                                   |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | 將字元字串地圖為 UTF-16 (寬字元) 字串。                                                          |
| [**TranslateCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | 轉譯字元集資訊，並將目的結構的所有成員設定為適當的值。           |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | 地圖 UTF-16 (寬字元) 字串新增至新的字元字串。                                                      |
| [**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))                       | 請勿使用。                                                                                                           |
| [**NlsDllCodePageTranslation**](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | 請勿使用。                                                                                                           |
| [**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))                       | 請勿使用。                                                                                                           |



 

 

 
