---
description: 本主題包含在應用程式中使用 NLS 函式來取出時間和日期資訊，以及持續時間資料的指示。 如果您的應用程式必須保存資料，請參閱使用永久性地區設定資料。
ms.assetid: 1880ff8f-110c-4661-8b1f-afe1d8d2a38d
title: 正在抓取時間和日期資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f461f12cb1c6324892a415142c159ba570759128e61dd02b53a7cceebccc57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040408"
---
# <a name="retrieving-time-and-date-information"></a>正在抓取時間和日期資訊

本主題包含在應用程式中使用 NLS 函式來取出 [時間和日期](time-and-date.md) 資訊，以及持續時間資料的指示。 如果您的應用程式必須保存資料，請參閱 [使用永久性地區設定資料](using-persistent-locale-data.md)。

**Windows Vista 和更新版本：** 本主題所討論的函式可以從 [自訂地區](custom-locales.md)設定取得資料。 尤其是，它們可以用來自訂時間和日期格式。 例如，可能會有時間格式（例如 "hhHmm'ss ' '），並產生像是" 12H34 ' 12 ' ' "的時間字串。

## <a name="retrieve-time-information"></a>取出時間資訊

您的應用程式可以使用 [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) 和 [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) 函數，以適用于目前地區設定的任何時間取得字串。 任一個函數都會檢查有效 [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) 結構中的每個時間值，判斷它是否在適當的值範圍內，並忽略結構的日期部分。 如果有任何時間值超出正確的範圍，函數會失敗，並出現程式碼錯誤 \_ 的 \_ 參數。 此函數不會傳回錯誤格式字串的錯誤，只會形成最可能的時間字串。

> [!Note]  
> NLS 時間函數不包含毫秒做為格式化時間字串的一部分。

 

若要取得時間格式而不執行任何實際的格式設定，應用程式可以使用 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 或 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 函式，在呼叫中指定 [地區設定 \_ STIMEFORMAT](locale-stime-constants.md) 常數。

**使用時間標記**

時間標記的範例有 "AM" 和 "PM" 適用于英文 (美國) 和 "de"。 和「du」。 針對西班牙文 (墨西哥) 。 如果 \_ 在 [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) 或 [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex)的呼叫中指定了 TIME NOTIMEMARKER，此函式會移除分隔符號 (s) 在時間標記之前和之後。 如果有時間標記 \_ ，而呼叫中未設定時間 NOTIMEMARKER 旗標，則函式會根據指定的地區設定識別碼來當地語系化時間標記。

**移除分隔符號之前的分鐘數和秒數**

您的應用程式可以呼叫 [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) 或 [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) ，並 \_ 指定時間 NOMINUTESORSECONDS 或時間 \_ NOSECONDS，以移除在 [分鐘] 和/或 [秒] 元素之前的分隔符號。

**使用24小時制時間格式**

如果您的應用程式支援24小時的時間格式，則可以使用時間 FORCE24HOURFORMAT 來呼叫 [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) 或 [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) \_ 。 除非設定了 TIME \_ NOTIMEMARKER 旗標，否則函數會顯示任何現有的時間標記。

## <a name="retrieve-date-information"></a>取得日期資訊

應用程式可以使用 [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) 和 [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) 函式，以適用于目前地區設定的格式取得任何日期的字串。 任一個函數都會檢查有效 [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) 結構中的每個日期值 year、month、day 和 week，並忽略結構的時間部分。 Day name、day name、month name 和縮寫月份名稱都會根據地區設定識別碼進行當地語系化。 如果星期幾的日期不正確，則函式會使用正確的值，而且不會傳回任何錯誤。 如果有任何其他日期值超出正確的範圍，則函式會失敗，並出現程式碼錯誤的 \_ \_ 參數無效。 此函數不會傳回錯誤格式字串的錯誤，只會形成最可能的日期字串。

如果應用程式需要特定行事曆的日期格式，則應該使用 [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) 或 [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)，並傳遞適當的行事 [**曆識別碼**](calendar-identifiers.md)。 若要傳回特定行事曆的所有日期格式，應用程式可以使用 [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)、 [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)、 [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)或 [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)。

**指定替代行事曆**

應用程式可以呼叫 [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) 或 [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) ，並使用旗標日期 \_ 使用 \_ ALT 行事 \_ 曆，以使用指定之替代行事曆的預設格式。 如果替代行事曆沒有預設格式，則函式會使用使用者覆寫。

若要取得替代日曆的日期格式，應用程式可以搭配使用 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 或 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 與 [LOCALE \_ IOPTIONALCALENDAR](locale-ioptionalcalendar.md) 常數。

**指定日期類型**

如果應用程式想要使用簡短日期格式，則會 \_ 在對 [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) 或 [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)的呼叫中指定日期 >shortdate。 您可以藉由指定函式呼叫中的日期 >longdate 來取得完整日期格式 \_ 。 如果未指定任何旗標，且 *lpFormat* 設定為 **Null**，則函式會使用 DATE \_ >shortdate 作為預設值。

若要取得預設地區設定行事曆的簡短和完整日期格式，應用程式應該使用 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 或 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 函數搭配 [locale \_ SSHORTDATE](locale-sshortdate.md) 或 [locale \_ SLONGDATE](locale-slongdate.md) 常數。

**指定日期格式圖片**

應用程式可以指定 [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) 或 [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) 用來形成日期字串的日期格式圖片。 如果需要指定之地區設定的日期格式，則應用程式可以呼叫 *lpFormat* 設定為 **Null** 的函式。 如果參數未設定為 **Null**，則此函式只會針對未在格式圖片字串中指定的資訊使用地區設定，例如地區設定的日期和月份名稱。

應用程式可以用單引號括住應維持在其確切格式的任何文字。 單引號也可以當做 escape 字元使用，以允許在日期字串中顯示標記本身。 但是，必須將 escape 序列括在兩個單引號內。 例如，若要將日期顯示為 "5 ' 93"，格式字串為： "MMMM ' ' ' ' yy"。

## <a name="retrieve-duration-information"></a>取出持續時間資訊

**Windows Vista 和更新版本：**[**GetDurationFormat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat)和 [**GetDurationFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex)函數可用來取得地區設定的持續時間格式，包括自訂地區設定。 若要取得地區設定的預設持續時間格式，應用程式應該使用 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 或 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 函數搭配 [locale \_ SDURATION](locale-sduration.md) 常數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用國家語言支援](about-national-language-support.md)
</dt> <dt>

[時間與日期](time-and-date.md)
</dt> <dt>

[使用永久性地區設定資料](using-persistent-locale-data.md)
</dt> </dl>

 

 
