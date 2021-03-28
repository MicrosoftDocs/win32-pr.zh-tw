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
# <a name="getdateformatwrapw-function"></a><span data-ttu-id="04945-103">GetDateFormatWrapW 函式</span><span class="sxs-lookup"><span data-stu-id="04945-103">GetDateFormatWrapW function</span></span>

<span data-ttu-id="04945-104">\[**GetDateFormatWrapW** 可用於 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="04945-104">\[**GetDateFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="04945-105">在後續版本中將無法使用。</span><span class="sxs-lookup"><span data-stu-id="04945-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="04945-106">您應該在其位置使用 [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) 。\]</span><span class="sxs-lookup"><span data-stu-id="04945-106">You should use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in its place.\]</span></span>

<span data-ttu-id="04945-107">將日期格式化為指定地區設定的日期字串。</span><span class="sxs-lookup"><span data-stu-id="04945-107">Formats a date as a date string for a specified locale.</span></span> <span data-ttu-id="04945-108">函數會將指定的日期或本機系統日期格式化。</span><span class="sxs-lookup"><span data-stu-id="04945-108">The function formats either a specified date or the local system date.</span></span>

> [!Note]  
> <span data-ttu-id="04945-109">**GetDateFormatWrapW** 是 **GetDateFormatW** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="04945-109">**GetDateFormatWrapW** is a wrapper for the **GetDateFormatW** function.</span></span> <span data-ttu-id="04945-110">如需進一步的使用注意事項，請參閱 [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) 頁面。</span><span class="sxs-lookup"><span data-stu-id="04945-110">See the [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="04945-111">語法</span><span class="sxs-lookup"><span data-stu-id="04945-111">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="04945-112">參數</span><span class="sxs-lookup"><span data-stu-id="04945-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04945-113">*地區* \[ 設定在\]</span><span class="sxs-lookup"><span data-stu-id="04945-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04945-114">類型： **LCID**</span><span class="sxs-lookup"><span data-stu-id="04945-114">Type: **LCID**</span></span>

<span data-ttu-id="04945-115">要格式化日期字串的地區設定。</span><span class="sxs-lookup"><span data-stu-id="04945-115">The locale for which the date string is to be formatted.</span></span> <span data-ttu-id="04945-116">如果 *pwzFormat* 為 **Null**，則函式會根據此地區設定的日期格式來格式化字串。</span><span class="sxs-lookup"><span data-stu-id="04945-116">If *pwzFormat* is **NULL**, the function formats the string according to the date format for this locale.</span></span> <span data-ttu-id="04945-117">如果 *pwzFormat* 不是 **Null**，此函式只會針對格式圖片字串中未指定的資訊使用地區設定 (例如，地區設定的日期和月份名稱) 。</span><span class="sxs-lookup"><span data-stu-id="04945-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's day and month names).</span></span>

<span data-ttu-id="04945-118">此參數可以是 [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) 宏所建立的地區設定識別碼，或下列其中一個預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="04945-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="04945-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**地區設定 \_ 系統 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="04945-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="04945-120">預設系統地區設定。</span><span class="sxs-lookup"><span data-stu-id="04945-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="04945-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**地區設定 \_ 使用者 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="04945-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="04945-122">預設使用者地區設定。</span><span class="sxs-lookup"><span data-stu-id="04945-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="04945-123">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04945-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04945-124">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="04945-124">Type: **DWORD**</span></span>

<span data-ttu-id="04945-125">指定各種函數選項。</span><span class="sxs-lookup"><span data-stu-id="04945-125">Specifies various function options.</span></span> <span data-ttu-id="04945-126">如果 *pwzFormat* 不是 **Null**，則此參數必須為零。</span><span class="sxs-lookup"><span data-stu-id="04945-126">If *pwzFormat* is not **NULL**, this parameter must be zero.</span></span> <span data-ttu-id="04945-127">如果 *pwzFormat* 為 **Null**，您可以指定下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="04945-127">If *pwzFormat* is **NULL**, you can specify a combination of the following values.</span></span> <span data-ttu-id="04945-128">如果您未指定 DATE \_ YEARMONTH、date \_ >SHORTDATE 或 date \_ >longdate，而且 *pwzFormat* 為 **Null**，則 \_ 會使用 date >shortdate 作為預設值。</span><span class="sxs-lookup"><span data-stu-id="04945-128">If you do not specify either DATE\_YEARMONTH, DATE\_SHORTDATE, or DATE\_LONGDATE, and *pwzFormat* is **NULL**, then DATE\_SHORTDATE is used as the default.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="04945-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**地區設定 \_ NOUSEROVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="04945-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="04945-130">如果設定，則函式會針對指定的地區設定使用系統預設日期格式來格式化字串。</span><span class="sxs-lookup"><span data-stu-id="04945-130">If set, the function formats the string using the system default date format for the specified locale.</span></span> <span data-ttu-id="04945-131">如果未設定，則函式會使用任何使用者覆寫來將字串格式化為地區設定的預設日期格式。</span><span class="sxs-lookup"><span data-stu-id="04945-131">If not set, the function formats the string using any user overrides to the locale's default date format.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="04945-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**地區設定 \_ 使用 \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="04945-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="04945-133">使用系統 ANSI 字碼頁進行字串轉譯，而不是地區設定的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="04945-133">Uses the system ANSI code page for string translation instead of the locale's code page.</span></span>

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span data-ttu-id="04945-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**日期 \_ >SHORTDATE**</span><span class="sxs-lookup"><span data-stu-id="04945-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**DATE\_SHORTDATE**</span></span>


</dt> <dd>

<span data-ttu-id="04945-135">使用簡短日期格式。</span><span class="sxs-lookup"><span data-stu-id="04945-135">Uses the short date format.</span></span> <span data-ttu-id="04945-136">此值不能與 DATE \_ >longdate 或 date YEARMONTH 搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="04945-136">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span data-ttu-id="04945-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**日期 \_ >LONGDATE**</span><span class="sxs-lookup"><span data-stu-id="04945-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**DATE\_LONGDATE**</span></span>


</dt> <dd>

<span data-ttu-id="04945-138">使用完整日期格式。</span><span class="sxs-lookup"><span data-stu-id="04945-138">Uses the long date format.</span></span> <span data-ttu-id="04945-139">此值不能與 DATE \_ >shortdate 或 date YEARMONTH 搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="04945-139">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span data-ttu-id="04945-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**日期 \_ YEARMONTH**</span><span class="sxs-lookup"><span data-stu-id="04945-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**DATE\_YEARMONTH**</span></span>


</dt> <dd>

<span data-ttu-id="04945-141">使用 year/month 格式。</span><span class="sxs-lookup"><span data-stu-id="04945-141">Uses the year/month format.</span></span> <span data-ttu-id="04945-142">此值不能與 DATE \_ >shortdate 或 date >longdate 搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="04945-142">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span>

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span data-ttu-id="04945-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**日期 \_ 使用 \_ ALT 行事 \_ 曆**</span><span class="sxs-lookup"><span data-stu-id="04945-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**DATE\_USE\_ALT\_CALENDAR**</span></span>


</dt> <dd>

<span data-ttu-id="04945-144">使用替代的行事曆（如果有的話）來格式化日期字串。</span><span class="sxs-lookup"><span data-stu-id="04945-144">Uses the alternate calendar, if one exists, to format the date string.</span></span> <span data-ttu-id="04945-145">如果設定此旗標，此函式會使用該替代行事曆的預設格式，而不是使用任何使用者覆寫。</span><span class="sxs-lookup"><span data-stu-id="04945-145">If this flag is set, the function uses the default format for that alternate calendar, rather than using any user overrides.</span></span> <span data-ttu-id="04945-146">只有當指定的替代行事曆沒有預設格式時，才會使用使用者覆寫。</span><span class="sxs-lookup"><span data-stu-id="04945-146">The user overrides will be used only in the event that there is no default format for the specified alternate calendar.</span></span>

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span data-ttu-id="04945-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**日期 \_ LTRREADING**</span><span class="sxs-lookup"><span data-stu-id="04945-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**DATE\_LTRREADING**</span></span>


</dt> <dd>

<span data-ttu-id="04945-148">新增從左至右閱讀配置的標記。</span><span class="sxs-lookup"><span data-stu-id="04945-148">Adds marks for left-to-right reading layout.</span></span> <span data-ttu-id="04945-149">此值無法與日期 RTLREADING 搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="04945-149">This value cannot be used with DATE\_RTLREADING.</span></span>

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span data-ttu-id="04945-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**日期 \_ RTLREADING**</span><span class="sxs-lookup"><span data-stu-id="04945-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**DATE\_RTLREADING**</span></span>


</dt> <dd>

<span data-ttu-id="04945-151">新增由右至左閱讀配置的標記。</span><span class="sxs-lookup"><span data-stu-id="04945-151">Adds marks for right-to-left reading layout.</span></span> <span data-ttu-id="04945-152">此值無法與日期 LTRREADING 搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="04945-152">This value cannot be used with DATE\_LTRREADING.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="04945-153">*lpDate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04945-153">*lpDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04945-154">類型： \**Const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="04945-154">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="04945-155">[_ *SYSTEMTIME* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)結構的指標，其中包含要格式化的日期資訊。</span><span class="sxs-lookup"><span data-stu-id="04945-155">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date information to be formatted.</span></span> <span data-ttu-id="04945-156">如果此指標為 **Null**，則函式會使用目前的本機系統日期。</span><span class="sxs-lookup"><span data-stu-id="04945-156">If this pointer is **NULL**, the function uses the current local system date.</span></span>

</dd> <dt>

<span data-ttu-id="04945-157">*pwzFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04945-157">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04945-158">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="04945-158">Type: **LPCWSTR**</span></span>

<span data-ttu-id="04945-159">用來形成日期字串的格式圖片指標。</span><span class="sxs-lookup"><span data-stu-id="04945-159">A pointer to a format picture to use to form the date string.</span></span> <span data-ttu-id="04945-160">如果 *pwzFormat* 為 **Null**，則函式會使用指定地區設定的日期格式。</span><span class="sxs-lookup"><span data-stu-id="04945-160">If *pwzFormat* is **NULL**, the function uses the date format of the specified locale.</span></span> <span data-ttu-id="04945-161">如需詳細資訊，請參閱 [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) 。</span><span class="sxs-lookup"><span data-stu-id="04945-161">See [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="04945-162">*pwzDateStr* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="04945-162">*pwzDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04945-163">類型： **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="04945-163">Type: **LPWSTR**</span></span>

<span data-ttu-id="04945-164">接收格式化日期字串之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="04945-164">A pointer to a buffer that receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="04945-165">*cchDate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04945-165">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04945-166">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="04945-166">Type: **int**</span></span>

<span data-ttu-id="04945-167">指定 *pwzDateStr* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="04945-167">Specifies the size, in characters, of the *pwzDateStr* buffer.</span></span> <span data-ttu-id="04945-168">如果 *cchDate* 為零，則函數會傳回保留格式化日期字串所需的字元數，而且不會使用 *pwzDateStr* 所指向的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="04945-168">If *cchDate* is zero, the function returns the number of characters required to hold the formatted date string, and the buffer pointed to by *pwzDateStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04945-169">傳回值</span><span class="sxs-lookup"><span data-stu-id="04945-169">Return value</span></span>

<span data-ttu-id="04945-170">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="04945-170">Type: **int**</span></span>

<span data-ttu-id="04945-171">如果函式成功，則傳回值是寫入 *pwzDateStr* 所指向之緩衝區的字元數。</span><span class="sxs-lookup"><span data-stu-id="04945-171">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzDateStr*.</span></span> <span data-ttu-id="04945-172">如果 *cchDate* 參數為零，則傳回值為保留格式化日期字串所需的字元數。</span><span class="sxs-lookup"><span data-stu-id="04945-172">If the *cchDate* parameter is zero, the return value is the number of characters required to hold the formatted date string.</span></span> <span data-ttu-id="04945-173">計數包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="04945-173">The count includes the terminating null character.</span></span>

<span data-ttu-id="04945-174">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="04945-174">If the function fails, the return value is zero.</span></span> <span data-ttu-id="04945-175">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="04945-175">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="04945-176">**GetLastError** 可能會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="04945-176">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="04945-177">**\_緩衝區不足的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="04945-177">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="04945-178">**錯誤 \_ 不正確 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="04945-178">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="04945-179">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="04945-179">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="04945-180">備註</span><span class="sxs-lookup"><span data-stu-id="04945-180">Remarks</span></span>

<span data-ttu-id="04945-181">**GetDateFormatWrapW** 能讓您在 Windows XP 之前的作業系統中使用 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="04945-181">**GetDateFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="04945-182">慣用的方法是使用 [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。</span><span class="sxs-lookup"><span data-stu-id="04945-182">The preferred method is to use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="04945-183">您必須使用序數311，直接從 Shlwapi.dll 呼叫 **GetDateFormatWrapW** 。</span><span class="sxs-lookup"><span data-stu-id="04945-183">**GetDateFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 311.</span></span>

## <a name="requirements"></a><span data-ttu-id="04945-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="04945-184">Requirements</span></span>



| <span data-ttu-id="04945-185">需求</span><span class="sxs-lookup"><span data-stu-id="04945-185">Requirement</span></span> | <span data-ttu-id="04945-186">值</span><span class="sxs-lookup"><span data-stu-id="04945-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04945-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04945-187">Minimum supported client</span></span><br/> | <span data-ttu-id="04945-188">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04945-188">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04945-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04945-189">Minimum supported server</span></span><br/> | <span data-ttu-id="04945-190">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04945-190">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="04945-191">DLL</span><span class="sxs-lookup"><span data-stu-id="04945-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04945-192"><dt>Shlwapi.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="04945-192"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04945-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04945-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04945-194">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="04945-194">**GetDateFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 
