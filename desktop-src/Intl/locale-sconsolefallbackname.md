---
description: 地區設定 \_ SCONSOLEFALLBACKNAME
ms.assetid: 36465a1c-085f-4f80-ad3d-5be6eaefe943
title: LOCALE_SCONSOLEFALLBACKNAME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09536167c68a4ec9156a1558960c48778019ae97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985183"
---
# <a name="locale_sconsolefallbackname"></a>地區設定 \_ SCONSOLEFALLBACKNAME

**Windows Vista 和更新版本：** 用於主控台顯示的慣用地區設定。 此字串允許的最大字元數為85，包括結束的 null 字元。

> [!Note]  
> 一般情況下，應用程式不應該直接使用地區設定 \_ SCONSOLEFALLBACKNAME 資料。 若要判斷要在主控台視窗中使用哪些語言資源，應用程式應該呼叫 [SetThreadUILanguage](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) 或 [SetThreadPreferredUILanguages](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)。 這些函式會在選擇可在主控台中辨認的語言時，使用主控台回溯資料作為一個因素，但不是唯一的行列式。 特別是，主控台只會顯示單一字碼頁的字元。 例如，希臘文 (希臘) 的 el-GR 是有效的主控台語言，但如果目前的主控台字碼頁是拉丁-1 (字碼頁 1252) 則主控台會以一系列字元找不到的符號來顯示希臘文文字。

 

如果主控台中支援對應到此地區設定的語言，則此值與 [地區設定 \_ SNAME](locale-sname.md)的值相同，也就是，地區設定本身可以用來顯示主控台。 不過，主控台無法顯示只能使用 [Uniscribe](uniscribe.md)轉譯的語言。 例如，主控台無法顯示阿拉伯文或不同的印度語言。 因此， \_ 對應于這些語言之地區設定的地區設定 SCONSOLEFALLBACKNAME 值，與地區設定 SNAME 的值不同 \_ 。

針對預先定義的地區設定，如果 fallback 值與地區設定本身的值不同，則會使用中性地區設定的值。 特定地區設定會與語言和國家/地區相關聯，而中性地區設定會與語言相關聯，但不會與任何國家/地區相關聯。 例如，ar-SA 會回復為 "en"，而不是 "en-us"。 使用中性地區設定的這項原則會針對預先定義的地區設定一致地執行，強烈建議自訂地區設定。 不過，不會強制執行此原則。 若為自訂地區設定，您的應用程式可以使用特定的地區設定，而不是使用中性地區設定做為回復。

> [!Note]  
> [呼叫「地區設定名稱](calling-the--locale-name--functions.md)」函式中所述的任何函式都不接受中性地區設定做為輸入。 因此，地區設定 \_ SCONSOLEFALLBACKNAME 資料的使用非常有限。 尤其是， [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 和 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 都不接受中性地區設定做為輸入。

 

 

 



