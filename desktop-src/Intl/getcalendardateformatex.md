---
description: 已取代。
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: GetCalendarDateFormatEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarDateFormatEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: b0130bf62c742d0565b1c98c138ac8c71ddf7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975129"
---
# <a name="getcalendardateformatex-function"></a>GetCalendarDateFormatEx 函式

已取代。 使用指定的日期和行事曆，抓取指定地區設定的正確格式化日期字串。 使用者可以指定簡短日期格式、完整日期格式、年月格式，或自訂格式模式。

> [!Note]  
> 此函式可以取出版本之間變更的資料，例如，由於自訂地區設定。 如果您的應用程式必須保存或傳輸資料，請參閱 [使用永久性地區設定資料](using-persistent-locale-data.md)。

 

## <a name="syntax"></a>語法


```C++
BOOL GetCalendarDateFormatEx(
  _In_        LPCWSTR       lpszLocale,
  _In_        DWORD         dwFlags,
  _In_  const LPCALDATETIME lpCalDateTime,
  _In_        LPCWSTR       lpFormat,
  _Out_       LPWSTR        lpDateStr,
  _In_        int           cchDate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszLocale* \[在\]
</dt> <dd>

地區設定名稱的指標，或下列其中一個預先定義的值。

-   [地區設定 \_ 名稱不 \_ 變](locale-name-constants.md)
-   [地區設定 \_ 名稱 \_ 系統 \_ 預設值](locale-name-constants.md)
-   [地區設定 \_ 名稱 \_ 使用者 \_ 預設值](locale-name-constants.md)

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

指定日期格式選項的旗標。 如果 *lpFormat* 未設定為 **Null**，則此參數必須設定為0。 如果 *lpFormat* 設定為 **Null**，則應用程式可以指定下列值和 [地區設定 \_ NOUSEROVERRIDE](locale-nouseroverride.md)的組合。



| 值                                                                                                                                                               | 意義                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <dt>**日期 \_ >SHORTDATE**</dt> </dl>    | 使用簡短日期格式。 此為預設值。 此值不能與 DATE \_ >longdate 或 date YEARMONTH 搭配使用 \_ 。 <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <dt>**日期 \_ >LONGDATE**</dt> </dl>       | 使用完整日期格式。 此值不能與 DATE \_ >shortdate 或 date YEARMONTH 搭配使用 \_ 。 <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <dt>**日期 \_ YEARMONTH**</dt> </dl>    | 使用 year/month 格式。 此值不能與 DATE \_ >shortdate 或 date >longdate 搭配使用 \_ 。<br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <dt>**日期 \_ LTRREADING**</dt> </dl> | 將標記新增至由左至右閱讀的版面配置。 此值無法與日期 RTLREADING 搭配使用 \_ 。<br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <dt>**日期 \_ RTLREADING**</dt> </dl> | 新增由右至左閱讀配置的標記。 此值無法與日期 LTRREADING 搭配使用 \_<br/>                        |



 

</dd> <dt>

*lpCalDateTime* \[在\]
</dt> <dd>

[**CALDATETIME**](caldatetime.md)結構的指標，其中包含要格式化的日期和行事曆資訊。

</dd> <dt>

*lpFormat* \[在\]
</dt> <dd>

用來形成日期字串之格式圖片字串的指標。 格式圖片字串的可能值會在 [Day、Month、Year 和 Era 格式的圖片](day--month--year--and-era-format-pictures.md)中定義。

格式圖片字串必須以 null 結束。 此函數只會針對未在格式圖片字串中指定的資訊使用地區設定，例如地區設定的日期和月份名稱。 如果函式是使用指定地區設定的日期格式，則應用程式會將此參數設定為 **Null** 。

</dd> <dt>

*lpDateStr* \[擴展\]
</dt> <dd>

緩衝區的指標，此函式會接收格式化的日期字串。

</dd> <dt>

*cchDate* \[在\]
</dt> <dd>

*LpDateStr* 緩衝區的大小（以字元為單位）。 或者，應用程式可以將此參數設定為0。 在此情況下，函數會傳回保留格式化日期字串所需的字元數，而且不會使用 *lpDateStr* 參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回寫入 *lpDateStr* 緩衝區的字元數。 如果 *cchDate* 參數設定為0，則函式會傳回保留格式化日期字串所需的字元數，包括結束的 null 字元。

如果不成功，則此函式會傳回0。 若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：

-   錯誤 \_ 日期 \_ 超出 \_ \_ 範圍。 指定的日期超出範圍。
-   \_緩衝區不足 \_ 的錯誤。 提供的緩衝區大小不夠大，或未正確設定為 **Null**。
-   錯誤 \_ 無效 \_ 的旗標。 為旗標提供的值無效。
-   錯誤 \_ 無效 \_ 的參數。 任何參數值都無效。

## <a name="remarks"></a>備註

此函數所支援的最早日期是1601年1月1日。

此函數沒有相關聯的標頭檔或程式庫檔案。 應用程式可以使用 DLL 名稱 (Kernel32.dll) 來呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。 然後，您可以使用該模組控制碼和此函式的名稱來呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，以取得函數位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[國家語言支援](national-language-support.md)
</dt> <dt>

[國家語言支援功能](national-language-support-functions.md)
</dt> <dt>

[日、月、年和年代格式的圖片](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[NLS：以名稱為基礎的 Api 範例](nls--name-based-apis-sample.md)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 
