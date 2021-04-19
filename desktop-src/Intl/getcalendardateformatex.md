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
# <a name="getcalendardateformatex-function"></a><span data-ttu-id="6917b-103">GetCalendarDateFormatEx 函式</span><span class="sxs-lookup"><span data-stu-id="6917b-103">GetCalendarDateFormatEx function</span></span>

<span data-ttu-id="6917b-104">已取代。</span><span class="sxs-lookup"><span data-stu-id="6917b-104">Deprecated.</span></span> <span data-ttu-id="6917b-105">使用指定的日期和行事曆，抓取指定地區設定的正確格式化日期字串。</span><span class="sxs-lookup"><span data-stu-id="6917b-105">Retrieves a properly formatted date string for the specified locale using the specified date and calendar.</span></span> <span data-ttu-id="6917b-106">使用者可以指定簡短日期格式、完整日期格式、年月格式，或自訂格式模式。</span><span class="sxs-lookup"><span data-stu-id="6917b-106">The user can specify the short date format, the long date format, the year month format, or a custom format pattern.</span></span>

> [!Note]  
> <span data-ttu-id="6917b-107">此函式可以取出版本之間變更的資料，例如，由於自訂地區設定。</span><span class="sxs-lookup"><span data-stu-id="6917b-107">This function can retrieve data that changes between releases, for example, due to a custom locale.</span></span> <span data-ttu-id="6917b-108">如果您的應用程式必須保存或傳輸資料，請參閱 [使用永久性地區設定資料](using-persistent-locale-data.md)。</span><span class="sxs-lookup"><span data-stu-id="6917b-108">If your application must persist or transmit data, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6917b-109">語法</span><span class="sxs-lookup"><span data-stu-id="6917b-109">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="6917b-110">參數</span><span class="sxs-lookup"><span data-stu-id="6917b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6917b-111">*lpszLocale* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6917b-111">*lpszLocale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6917b-112">地區設定名稱的指標，或下列其中一個預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="6917b-112">Pointer to a locale name, or one of the following predefined values.</span></span>

-   [<span data-ttu-id="6917b-113">地區設定 \_ 名稱不 \_ 變</span><span class="sxs-lookup"><span data-stu-id="6917b-113">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="6917b-114">地區設定 \_ 名稱 \_ 系統 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="6917b-114">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="6917b-115">地區設定 \_ 名稱 \_ 使用者 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="6917b-115">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="6917b-116">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6917b-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6917b-117">指定日期格式選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="6917b-117">Flags specifying date format options.</span></span> <span data-ttu-id="6917b-118">如果 *lpFormat* 未設定為 **Null**，則此參數必須設定為0。</span><span class="sxs-lookup"><span data-stu-id="6917b-118">If *lpFormat* is not set to **NULL**, this parameter must be set to 0.</span></span> <span data-ttu-id="6917b-119">如果 *lpFormat* 設定為 **Null**，則應用程式可以指定下列值和 [地區設定 \_ NOUSEROVERRIDE](locale-nouseroverride.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="6917b-119">If *lpFormat* is set to **NULL**, the application can specify a combination of the following values and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md).</span></span>



| <span data-ttu-id="6917b-120">值</span><span class="sxs-lookup"><span data-stu-id="6917b-120">Value</span></span>                                                                                                                                                               | <span data-ttu-id="6917b-121">意義</span><span class="sxs-lookup"><span data-stu-id="6917b-121">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <span data-ttu-id="6917b-122"><dt>**日期 \_ >SHORTDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="6917b-122"><dt>**DATE\_SHORTDATE**</dt></span></span> </dl>    | <span data-ttu-id="6917b-123">使用簡短日期格式。</span><span class="sxs-lookup"><span data-stu-id="6917b-123">Use the short date format.</span></span> <span data-ttu-id="6917b-124">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="6917b-124">This is the default.</span></span> <span data-ttu-id="6917b-125">此值不能與 DATE \_ >longdate 或 date YEARMONTH 搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6917b-125">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span> <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <span data-ttu-id="6917b-126"><dt>**日期 \_ >LONGDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="6917b-126"><dt>**DATE\_LONGDATE**</dt></span></span> </dl>       | <span data-ttu-id="6917b-127">使用完整日期格式。</span><span class="sxs-lookup"><span data-stu-id="6917b-127">Use the long date format.</span></span> <span data-ttu-id="6917b-128">此值不能與 DATE \_ >shortdate 或 date YEARMONTH 搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6917b-128">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span> <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <span data-ttu-id="6917b-129"><dt>**日期 \_ YEARMONTH**</dt></span><span class="sxs-lookup"><span data-stu-id="6917b-129"><dt>**DATE\_YEARMONTH**</dt></span></span> </dl>    | <span data-ttu-id="6917b-130">使用 year/month 格式。</span><span class="sxs-lookup"><span data-stu-id="6917b-130">Use the year/month format.</span></span> <span data-ttu-id="6917b-131">此值不能與 DATE \_ >shortdate 或 date >longdate 搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6917b-131">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span><br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <span data-ttu-id="6917b-132"><dt>**日期 \_ LTRREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="6917b-132"><dt>**DATE\_LTRREADING**</dt></span></span> </dl> | <span data-ttu-id="6917b-133">將標記新增至由左至右閱讀的版面配置。</span><span class="sxs-lookup"><span data-stu-id="6917b-133">Add marks for left-to-right reading layout.</span></span> <span data-ttu-id="6917b-134">此值無法與日期 RTLREADING 搭配使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6917b-134">This value cannot be used with DATE\_RTLREADING.</span></span><br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <span data-ttu-id="6917b-135"><dt>**日期 \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="6917b-135"><dt>**DATE\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="6917b-136">新增由右至左閱讀配置的標記。</span><span class="sxs-lookup"><span data-stu-id="6917b-136">Add marks for right-to-left reading layout.</span></span> <span data-ttu-id="6917b-137">此值無法與日期 LTRREADING 搭配使用 \_</span><span class="sxs-lookup"><span data-stu-id="6917b-137">This value cannot be used with DATE\_LTRREADING</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="6917b-138">*lpCalDateTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6917b-138">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6917b-139">[**CALDATETIME**](caldatetime.md)結構的指標，其中包含要格式化的日期和行事曆資訊。</span><span class="sxs-lookup"><span data-stu-id="6917b-139">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to format.</span></span>

</dd> <dt>

<span data-ttu-id="6917b-140">*lpFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6917b-140">*lpFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6917b-141">用來形成日期字串之格式圖片字串的指標。</span><span class="sxs-lookup"><span data-stu-id="6917b-141">Pointer to a format picture string that is used to form the date string.</span></span> <span data-ttu-id="6917b-142">格式圖片字串的可能值會在 [Day、Month、Year 和 Era 格式的圖片](day--month--year--and-era-format-pictures.md)中定義。</span><span class="sxs-lookup"><span data-stu-id="6917b-142">Possible values for the format picture string are defined in [Day, Month, Year, and Era Format Pictures](day--month--year--and-era-format-pictures.md).</span></span>

<span data-ttu-id="6917b-143">格式圖片字串必須以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="6917b-143">The format picture string must be null-terminated.</span></span> <span data-ttu-id="6917b-144">此函數只會針對未在格式圖片字串中指定的資訊使用地區設定，例如地區設定的日期和月份名稱。</span><span class="sxs-lookup"><span data-stu-id="6917b-144">The function uses the locale only for information not specified in the format picture string, for example, the day and month names for the locale.</span></span> <span data-ttu-id="6917b-145">如果函式是使用指定地區設定的日期格式，則應用程式會將此參數設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="6917b-145">The application sets this parameter to **NULL** if the function is to use the date format of the specified locale.</span></span>

</dd> <dt>

<span data-ttu-id="6917b-146">*lpDateStr* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6917b-146">*lpDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6917b-147">緩衝區的指標，此函式會接收格式化的日期字串。</span><span class="sxs-lookup"><span data-stu-id="6917b-147">Pointer to a buffer in which this function receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="6917b-148">*cchDate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6917b-148">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6917b-149">*LpDateStr* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="6917b-149">Size, in characters, of the *lpDateStr* buffer.</span></span> <span data-ttu-id="6917b-150">或者，應用程式可以將此參數設定為0。</span><span class="sxs-lookup"><span data-stu-id="6917b-150">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="6917b-151">在此情況下，函數會傳回保留格式化日期字串所需的字元數，而且不會使用 *lpDateStr* 參數。</span><span class="sxs-lookup"><span data-stu-id="6917b-151">In this case, the function returns the number of characters required to hold the formatted date string, and the *lpDateStr* parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6917b-152">傳回值</span><span class="sxs-lookup"><span data-stu-id="6917b-152">Return value</span></span>

<span data-ttu-id="6917b-153">如果成功，則傳回寫入 *lpDateStr* 緩衝區的字元數。</span><span class="sxs-lookup"><span data-stu-id="6917b-153">Returns the number of characters written to the *lpDateStr* buffer if successful.</span></span> <span data-ttu-id="6917b-154">如果 *cchDate* 參數設定為0，則函式會傳回保留格式化日期字串所需的字元數，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="6917b-154">If the *cchDate* parameter is set to 0, the function returns the number of characters required to hold the formatted date string, including the terminating null character.</span></span>

<span data-ttu-id="6917b-155">如果不成功，則此函式會傳回0。</span><span class="sxs-lookup"><span data-stu-id="6917b-155">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="6917b-156">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="6917b-156">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="6917b-157">錯誤 \_ 日期 \_ 超出 \_ \_ 範圍。</span><span class="sxs-lookup"><span data-stu-id="6917b-157">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="6917b-158">指定的日期超出範圍。</span><span class="sxs-lookup"><span data-stu-id="6917b-158">The specified date was out of range.</span></span>
-   <span data-ttu-id="6917b-159">\_緩衝區不足 \_ 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6917b-159">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="6917b-160">提供的緩衝區大小不夠大，或未正確設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6917b-160">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="6917b-161">錯誤 \_ 無效 \_ 的旗標。</span><span class="sxs-lookup"><span data-stu-id="6917b-161">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="6917b-162">為旗標提供的值無效。</span><span class="sxs-lookup"><span data-stu-id="6917b-162">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="6917b-163">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="6917b-163">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="6917b-164">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="6917b-164">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="6917b-165">備註</span><span class="sxs-lookup"><span data-stu-id="6917b-165">Remarks</span></span>

<span data-ttu-id="6917b-166">此函數所支援的最早日期是1601年1月1日。</span><span class="sxs-lookup"><span data-stu-id="6917b-166">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="6917b-167">此函數沒有相關聯的標頭檔或程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="6917b-167">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="6917b-168">應用程式可以使用 DLL 名稱 (Kernel32.dll) 來呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="6917b-168">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="6917b-169">然後，您可以使用該模組控制碼和此函式的名稱來呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，以取得函數位址。</span><span class="sxs-lookup"><span data-stu-id="6917b-169">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="6917b-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="6917b-170">Requirements</span></span>



| <span data-ttu-id="6917b-171">需求</span><span class="sxs-lookup"><span data-stu-id="6917b-171">Requirement</span></span> | <span data-ttu-id="6917b-172">值</span><span class="sxs-lookup"><span data-stu-id="6917b-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6917b-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6917b-173">Minimum supported client</span></span><br/> | <span data-ttu-id="6917b-174">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6917b-174">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6917b-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6917b-175">Minimum supported server</span></span><br/> | <span data-ttu-id="6917b-176">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6917b-176">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6917b-177">DLL</span><span class="sxs-lookup"><span data-stu-id="6917b-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6917b-178"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6917b-178"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6917b-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6917b-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6917b-180">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="6917b-180">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="6917b-181">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="6917b-181">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="6917b-182">日、月、年和年代格式的圖片</span><span class="sxs-lookup"><span data-stu-id="6917b-182">Day, Month, Year, and Era Format Pictures</span></span>](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[<span data-ttu-id="6917b-183">NLS：以名稱為基礎的 Api 範例</span><span class="sxs-lookup"><span data-stu-id="6917b-183">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> <dt>

[<span data-ttu-id="6917b-184">**EnumDateFormatsExEx**</span><span class="sxs-lookup"><span data-stu-id="6917b-184">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[<span data-ttu-id="6917b-185">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="6917b-185">**GetDateFormat**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[<span data-ttu-id="6917b-186">**GetDateFormatEx**</span><span class="sxs-lookup"><span data-stu-id="6917b-186">**GetDateFormatEx**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[<span data-ttu-id="6917b-187">**CALDATETIME**</span><span class="sxs-lookup"><span data-stu-id="6917b-187">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 
