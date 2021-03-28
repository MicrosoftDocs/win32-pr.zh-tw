---
description: 將時間格式化為指定地區設定的時間字串。
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: GetTimeFormatWrapW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTimeFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 53f1bb88c2b3a79b58f3025daec31a7b1340b642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973196"
---
# <a name="gettimeformatwrapw-function"></a>GetTimeFormatWrapW 函式

\[**GetTimeFormatWrapW** 可用於 Windows XP。 在後續版本中可能無法使用。 您應該在其位置使用 [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) 。\]

將時間格式化為指定地區設定的時間字串。 函數會格式化指定的時間或本機系統時間。

> [!Note]  
> **GetTimeFormatWrapW** 是 **GetTimeFormatW** 函數的包裝函式。 如需進一步的使用注意事項，請參閱 [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) 頁面。

 

## <a name="syntax"></a>語法


```C++
int GetTimeFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpTime,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzTimeStr,
  _In_        int        cchTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*地區* \[ 設定在\]
</dt> <dd>

類型： **LCID**

指定要格式化時間字串的地區設定。 如果 *pwzFormat* 為 **Null**，則函式會根據此地區設定的時間格式來格式化字串。 如果 *pwzFormat* 不是 **Null**，此函式只會針對格式圖片字串中未指定的資訊使用地區設定 (例如，地區設定的時間標記) 。

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

指定各種函數選項。 您可以指定下列值的組合。

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**地區設定 \_ NOUSEROVERRIDE**


</dt> <dd>

如果設定，函數會針對指定的地區設定使用系統預設時間格式來格式化字串。 如果未設定，則函式會使用任何使用者覆寫來將字串格式化為地區設定的預設時間格式。 只有當 *pwzFormat* 為 **Null** 時，才能設定這個旗標。

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**地區設定 \_ 使用 \_ CP \_ ACP**


</dt> <dd>

使用系統 ANSI 字碼頁進行字串轉譯，而不是地區設定字碼頁。

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**時間 \_ NOMINUTESORSECONDS**


</dt> <dd>

不會使用分鐘或秒數。

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**時間 \_ NOSECONDS**


</dt> <dd>

不會使用秒數。

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**時間 \_ NOTIMEMARKER**


</dt> <dd>

不使用時間標記。

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**時間 \_ FORCE24HOURFORMAT**


</dt> <dd>

一律使用24小時的時間格式。

</dd> </dl> </dd> <dt>

*lpTime* \[在\]
</dt> <dd>

類型： **Const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _

[_ *SYSTEMTIME* *](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)結構的指標，其中包含要格式化的時間資訊。 如果此指標為 **Null**，則函式會使用目前的本機系統時間。

</dd> <dt>

*pwzFormat* \[在\]
</dt> <dd>

類型： **LPCWSTR**

用來形成時間字串的格式指標。 如果 *pwzFormat* 為 **Null**，則函式會使用指定地區設定的時間格式。 如需詳細資訊，請參閱 [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) 。

</dd> <dt>

*pwzTimeStr* \[擴展\]
</dt> <dd>

類型： **LPWSTR**

接收格式化時間字串的緩衝區指標。

</dd> <dt>

*cchTime* \[在\]
</dt> <dd>

類型： **int**

*PwzTimeStr* 緩衝區的大小（以字元為單位）。 如果 *cchTime* 為零，則函數會傳回保留格式化時間字串所需的字元數，而且不會使用 *pwzTimeStr* 所指向的緩衝區。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **int**

如果函式成功，則傳回值是寫入 *pwzTimeStr* 所指向之緩衝區的字元數。 如果 *cchTime* 參數為零，則傳回值為保留格式化時間字串所需的字元數。 計數包含終止的 null 字元。

如果此函式失敗，則傳回值為零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。 **GetLastError** 可能會傳回下列其中一個錯誤碼。

<dl> <dt>

**\_緩衝區不足的錯誤 \_**
</dt> <dt>

**錯誤 \_ 不正確 \_ 旗標**
</dt> <dt>

**錯誤 \_ 不正確 \_ 參數**
</dt> </dl>

## <a name="remarks"></a>備註

**GetTimeFormatWrapW** 能讓您在 Windows XP 之前的作業系統中使用 Unicode 字串。 慣用的方法是使用 [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。

您必須使用序數310，直接從 Shlwapi.dll 呼叫 **GetTimeFormatWrapW** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
