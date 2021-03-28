---
description: 將日期格式化為指定地區設定的日期字串。
ms.assetid: e45f6d1c-2890-44f6-8406-022c99c59e02
title: GetDateFormatWrapW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDateFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9c369584fd15a27d5e684452b2277104b5b1da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192692"
---
# <a name="getdateformatwrapw-function"></a>GetDateFormatWrapW 函式

\[**GetDateFormatWrapW** 可用於 Windows XP。 在後續版本中將無法使用。 您應該在其位置使用 [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) 。\]

將日期格式化為指定地區設定的日期字串。 函數會將指定的日期或本機系統日期格式化。

> [!Note]  
> **GetDateFormatWrapW** 是 **GetDateFormatW** 函數的包裝函式。 如需進一步的使用注意事項，請參閱 [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) 頁面。

 

## <a name="syntax"></a>語法


```C++
int GetDateFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpDate,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzDateStr,
  _In_        int        cchDate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*地區* \[ 設定在\]
</dt> <dd>

類型： **LCID**

要格式化日期字串的地區設定。 如果 *pwzFormat* 為 **Null**，則函式會根據此地區設定的日期格式來格式化字串。 如果 *pwzFormat* 不是 **Null**，此函式只會針對格式圖片字串中未指定的資訊使用地區設定 (例如，地區設定的日期和月份名稱) 。

此參數可以是 [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) 宏所建立的地區設定識別碼，或下列其中一個預先定義的值。

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**地區設定 \_ 系統 \_ 預設值**


</dt> <dd>

預設系統地區設定。

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**地區設定 \_ 使用者 \_ 預設值**


</dt> <dd>

預設使用者地區設定。

</dd> </dl> </dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

類型： **DWORD**

指定各種函數選項。 如果 *pwzFormat* 不是 **Null**，則此參數必須為零。 如果 *pwzFormat* 為 **Null**，您可以指定下列值的組合。 如果您未指定 DATE \_ YEARMONTH、date \_ >SHORTDATE 或 date \_ >longdate，而且 *pwzFormat* 為 **Null**，則 \_ 會使用 date >shortdate 作為預設值。

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**地區設定 \_ NOUSEROVERRIDE**


</dt> <dd>

如果設定，則函式會針對指定的地區設定使用系統預設日期格式來格式化字串。 如果未設定，則函式會使用任何使用者覆寫來將字串格式化為地區設定的預設日期格式。

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**地區設定 \_ 使用 \_ CP \_ ACP**


</dt> <dd>

使用系統 ANSI 字碼頁進行字串轉譯，而不是地區設定的字碼頁。

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**日期 \_ >SHORTDATE**


</dt> <dd>

使用簡短日期格式。 此值不能與 DATE \_ >longdate 或 date YEARMONTH 搭配使用 \_ 。

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**日期 \_ >LONGDATE**


</dt> <dd>

使用完整日期格式。 此值不能與 DATE \_ >shortdate 或 date YEARMONTH 搭配使用 \_ 。

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**日期 \_ YEARMONTH**


</dt> <dd>

使用 year/month 格式。 此值不能與 DATE \_ >shortdate 或 date >longdate 搭配使用 \_ 。

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**日期 \_ 使用 \_ ALT 行事 \_ 曆**


</dt> <dd>

使用替代的行事曆（如果有的話）來格式化日期字串。 如果設定此旗標，此函式會使用該替代行事曆的預設格式，而不是使用任何使用者覆寫。 只有當指定的替代行事曆沒有預設格式時，才會使用使用者覆寫。

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**日期 \_ LTRREADING**


</dt> <dd>

新增從左至右閱讀配置的標記。 此值無法與日期 RTLREADING 搭配使用 \_ 。

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**日期 \_ RTLREADING**


</dt> <dd>

新增由右至左閱讀配置的標記。 此值無法與日期 LTRREADING 搭配使用 \_ 。

</dd> </dl> </dd> <dt>

*lpDate* \[在\]
</dt> <dd>

類型： **Const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _

[_ *SYSTEMTIME* *](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)結構的指標，其中包含要格式化的日期資訊。 如果此指標為 **Null**，則函式會使用目前的本機系統日期。

</dd> <dt>

*pwzFormat* \[在\]
</dt> <dd>

類型： **LPCWSTR**

用來形成日期字串的格式圖片指標。 如果 *pwzFormat* 為 **Null**，則函式會使用指定地區設定的日期格式。 如需詳細資訊，請參閱 [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) 。

</dd> <dt>

*pwzDateStr* \[擴展\]
</dt> <dd>

類型： **LPWSTR**

接收格式化日期字串之緩衝區的指標。

</dd> <dt>

*cchDate* \[在\]
</dt> <dd>

類型： **int**

指定 *pwzDateStr* 緩衝區的大小（以字元為單位）。 如果 *cchDate* 為零，則函數會傳回保留格式化日期字串所需的字元數，而且不會使用 *pwzDateStr* 所指向的緩衝區。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **int**

如果函式成功，則傳回值是寫入 *pwzDateStr* 所指向之緩衝區的字元數。 如果 *cchDate* 參數為零，則傳回值為保留格式化日期字串所需的字元數。 計數包含終止的 null 字元。

如果此函式失敗，則傳回值為零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。 **GetLastError** 可能會傳回下列其中一個錯誤碼。

<dl> <dt>

**\_緩衝區不足的錯誤 \_**
</dt> <dt>

**錯誤 \_ 不正確 \_ 旗標**
</dt> <dt>

**錯誤 \_ 不正確 \_ 參數**
</dt> </dl>

## <a name="remarks"></a>備註

**GetDateFormatWrapW** 能讓您在 Windows XP 之前的作業系統中使用 Unicode 字串。 慣用的方法是使用 [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。

您必須使用序數311，直接從 Shlwapi.dll 呼叫 **GetDateFormatWrapW** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 
