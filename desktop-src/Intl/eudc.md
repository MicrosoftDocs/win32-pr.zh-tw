---
description: EUDC 登錄機碼包含一或多個子機碼，其中包含的值定義與使用者定義字元相關聯的字型， (EUDCs) 用於指定的字碼頁。
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b583c7a0bfaa67684901e8d0a4a95ac5e45658
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120703"
---
# <a name="eudc"></a>EUDC

EUDC 登錄機碼包含一或多個子機碼，其中包含的值定義與使用者定義字元相關聯的字型， [ (EUDCs) ](end-user-defined-characters.md) 用於指定的字碼頁。 它具有下列登錄位置：

HKEY \_ 目前的 \_ 使用者 \\ EUDC

其格式為：

EUDC SystemDefaultEUDCFont = TrueTypeEUDCFontFileName TrueTypeFontTypeface = TrueTypeEUDCFontFileName

其中：



| 值                         | 描述                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| SystemDefaultEUDCFont    | 預先定義的名稱，用來設定系統預設字型。 除非明確指定此專案，否則不會有系統預設的 EUDC 字型。     |
| TrueTypeFontTypeface     | 與非 EUDC TrueType 字型相關聯的使用者定義名稱。                                                                              |
| TrueTypeEUDCFontFileName | 由個別的 EUDC 字型檔案的檔案名所組成的字串。 此檔案會識別要與 TrueTypeFontTypeface 相關聯的字型。 |



 

下列範例會顯示字碼頁932的 EUDC 索引鍵。


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



下列範例會將系統預設的 EUDC 字型設定為 ttf，並將個別的 EUDC 字型 Mineudc. ttf 和 Goteudc，分別與字型名稱 MS Ttf 和 MS Mt 產生關聯。


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



當與非 Unicode 程式語言相關聯的 Windows 字碼頁 (system ACP) 符合子機碼時，GDI 子系統會查看子機碼值組，以取得字元的顯示資訊。 它會先尋找符合目前字型的名稱。 如果沒有，它會檢查 SystemDefaultEUDCFont 值。 如果未定義任何值，GDI 會將字元視為未定義。

請注意，文字本身不一定要位於 Windows 字碼頁中。 例如，假設字碼頁的識別碼為1252，也就是英文的預設 Windows 字碼頁。 應用程式會將 Unicode 私用區域中的單一 Unicode 程式碼點 U + E000 傳遞 (PUA) ，以進行 [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)。 在此情況下，GDI 會查看1252底下的登錄值，以取得字元顯示內容的字型資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EUDC 登錄專案](eudc-registry-entries.md)
</dt> <dt>

[EUDCCodeRange](eudccoderange.md)
</dt> </dl>

 

 
