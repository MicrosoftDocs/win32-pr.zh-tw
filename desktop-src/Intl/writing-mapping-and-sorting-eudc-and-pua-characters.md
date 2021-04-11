---
description: 應用程式會將使用者定義的字元 (EUDCs) 和私用區域 (PUA) 字元寫入螢幕或印表機，如同使用 TextOut 和 ExtTextOut 等輸出功能。
ms.assetid: c975c70d-4231-4a69-bec2-d51d6993fdd4
title: 撰寫、對應和排序 EUDC 和 PUA 字元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c34264d956bb6a87407e249f68b2bc03fb2c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191378"
---
# <a name="writing-mapping-and-sorting-eudc-and-pua-characters"></a>撰寫、對應和排序 EUDC 和 PUA 字元

應用程式會將使用者定義的字元 (EUDCs) 和私用區域 (PUA) 字元寫入螢幕或印表機，如同使用 [TextOut](/windows/win32/api/wingdi/nf-wingdi-textouta) 和 [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta)等輸出功能。 如果已啟用 EUDC，這些函式會自動從 EUDC 或 PUA 字元字型取出字元資訊。 如需詳細資訊，請參閱 [使用者 \_ 定義和私用區域字元](end-user-defined-characters.md)。

撰寫 EUDCs 或 PUA 字元時，文字輸出函式的作業取決於目前選取的字型。 如果選取的字型是整合的 EUDC 或 PUA 字元字型，則函式會從該字型抓取字元資訊。 如果選取的字型是 [雙位元組字集](double-byte-character-sets.md) (DBCS) TrueType 字型具有相關聯的個別 EUDC 字型，此函式會從指定的 eudc 字型抓取資訊。 同樣地，如果選取的字型是具有相關聯之個別 PUA 字元字型的 [Unicode](unicode.md) TrueType 字型，則函式會從 PUA 字元字型抓取資訊。 如果選取的字型沒有相關聯的 EUDC 或 PUA 字元字型，則函式會從系統預設的 EUDC 字型抓取資訊。 如果字元不是系統預設的 EUDC 字型，或沒有系統預設的 EUDC 字型，則函式會寫入所選取字型所定義的預設字元。

應用程式可以使用 [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) 和 [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) 函式，將 EUDCs 對應至 Unicode。 **MultiByteToWideChar** 函式會將大部分的 EUDCs 對應至 Unicode PUA 中的字元。 不過，為了支援特定國家或地區標準，某些 EUDCs 可對應至非 PUA 的 Unicode 程式碼點。 如果這類對應存在，而且程式碼點沒有 Unicode 的有效非 PUA 對應， **WideCharToMultiByte** 函式就會將 PUA 中的字元對應至其 EUDC 對應項。 並非所有字碼頁都有 EUDC 範圍。 對 **WideCharToMultiByte** 的呼叫中指定的字碼頁，必須包含要發生之 eudc 範圍對應的 EUDC 程式碼範圍。 如果字碼頁未包含 EUDC 程式碼範圍，則函式會抓取 Unicode PUA 中任何字元的預設字元。

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) 和 [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) 無法保證來回對應。 換句話說，您可以從包含 EUDCs 的特定多位元組字元串開始，使用 **MultiByteToWideChar** 將字串對應至 Unicode，然後將它對應回具有 **WIDECHARTOMULTIBYTE** 的原始 DBCS，最後產生與原始字串不相同的結果。 依賴將 EUDCs 對應至 Unicode 的應用程式應該確保所有必要的字元都能在適當的字碼頁 EUDC 區域和 Unicode PUA 之間來回行程。

應用程式不應該嘗試將 EUDCs 從某個字碼頁對應到另一個字碼頁。 如果應用程式從一個字碼頁的 EUDC 開始，請使用 [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)將其對應至 Unicode，並對應至不同的 DBCS 與 [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)，則不會對結果產生任何保證。 原始字元可能對應至目的地字碼頁中的不同 EUDC，或可能對應為未定義字元。 同樣地，將 Unicode 字串對應至具有 EUDC 範圍的字碼頁，可能會產生非預期的結果。 如果 Unicode 字串包含 PUA 的程式碼點，則可能會將程式碼點對應到不代表相同字元的 EUDC。

應用程式可以使用 [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 函數的 ANSI 版本，來比較包含 EUDCS 的 DBCS 字串。 函式會在比較字元值之前，將字元有效地對應至 Unicode。 應用程式可以使用 ANSI 版本的 [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) 函式和 LCMAP 分類值，建立字串的排序索引鍵 \_ 。 此函式會將字元先對應到 Unicode。 PUA 中的所有字元都是在所有其他 Unicode 字元之後排序。 在該區域內，字元會依數位順序排序。 如果應用程式嘗試使用 [GetStringTypeA](/windows/desktop/api/Winnls/nf-winnls-getstringtypea) 函式來抓取 EUDC 的 CTYPE 資訊，則此函式會針對每個字元取得 **Null** 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Unicode 和字元集](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
