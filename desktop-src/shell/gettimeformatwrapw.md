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
# <a name="gettimeformatwrapw-function"></a><span data-ttu-id="cdf17-103">GetTimeFormatWrapW 函式</span><span class="sxs-lookup"><span data-stu-id="cdf17-103">GetTimeFormatWrapW function</span></span>

<span data-ttu-id="cdf17-104">\[**GetTimeFormatWrapW** 可用於 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="cdf17-104">\[**GetTimeFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="cdf17-105">在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="cdf17-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="cdf17-106">您應該在其位置使用 [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) 。\]</span><span class="sxs-lookup"><span data-stu-id="cdf17-106">You should use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in its place.\]</span></span>

<span data-ttu-id="cdf17-107">將時間格式化為指定地區設定的時間字串。</span><span class="sxs-lookup"><span data-stu-id="cdf17-107">Formats time as a time string for a specified locale.</span></span> <span data-ttu-id="cdf17-108">函數會格式化指定的時間或本機系統時間。</span><span class="sxs-lookup"><span data-stu-id="cdf17-108">The function formats either a specified time or the local system time.</span></span>

> [!Note]  
> <span data-ttu-id="cdf17-109">**GetTimeFormatWrapW** 是 **GetTimeFormatW** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="cdf17-109">**GetTimeFormatWrapW** is a wrapper for the **GetTimeFormatW** function.</span></span> <span data-ttu-id="cdf17-110">如需進一步的使用注意事項，請參閱 [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) 頁面。</span><span class="sxs-lookup"><span data-stu-id="cdf17-110">See the [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cdf17-111">語法</span><span class="sxs-lookup"><span data-stu-id="cdf17-111">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="cdf17-112">參數</span><span class="sxs-lookup"><span data-stu-id="cdf17-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdf17-113">*地區* \[ 設定在\]</span><span class="sxs-lookup"><span data-stu-id="cdf17-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf17-114">類型： **LCID**</span><span class="sxs-lookup"><span data-stu-id="cdf17-114">Type: **LCID**</span></span>

<span data-ttu-id="cdf17-115">指定要格式化時間字串的地區設定。</span><span class="sxs-lookup"><span data-stu-id="cdf17-115">Specifies the locale for which the time string is to be formatted.</span></span> <span data-ttu-id="cdf17-116">如果 *pwzFormat* 為 **Null**，則函式會根據此地區設定的時間格式來格式化字串。</span><span class="sxs-lookup"><span data-stu-id="cdf17-116">If *pwzFormat* is **NULL**, the function formats the string according to the time format for this locale.</span></span> <span data-ttu-id="cdf17-117">如果 *pwzFormat* 不是 **Null**，此函式只會針對格式圖片字串中未指定的資訊使用地區設定 (例如，地區設定的時間標記) 。</span><span class="sxs-lookup"><span data-stu-id="cdf17-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's time markers).</span></span>

<span data-ttu-id="cdf17-118">此參數可以是 [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) 宏所建立的地區設定識別碼，或下列其中一個預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="cdf17-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="cdf17-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**地區設定 \_ 系統 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="cdf17-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="cdf17-120">預設系統地區設定。</span><span class="sxs-lookup"><span data-stu-id="cdf17-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="cdf17-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**地區設定 \_ 使用者 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="cdf17-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="cdf17-122">預設使用者地區設定。</span><span class="sxs-lookup"><span data-stu-id="cdf17-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cdf17-123">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdf17-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf17-124">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cdf17-124">Type: **DWORD**</span></span>

<span data-ttu-id="cdf17-125">指定各種函數選項。</span><span class="sxs-lookup"><span data-stu-id="cdf17-125">Specifies various function options.</span></span> <span data-ttu-id="cdf17-126">您可以指定下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="cdf17-126">You can specify a combination of the following values.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="cdf17-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**地區設定 \_ NOUSEROVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="cdf17-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="cdf17-128">如果設定，函數會針對指定的地區設定使用系統預設時間格式來格式化字串。</span><span class="sxs-lookup"><span data-stu-id="cdf17-128">If set, the function formats the string using the system default time format for the specified locale.</span></span> <span data-ttu-id="cdf17-129">如果未設定，則函式會使用任何使用者覆寫來將字串格式化為地區設定的預設時間格式。</span><span class="sxs-lookup"><span data-stu-id="cdf17-129">If not set, the function formats the string using any user overrides to the locale's default time format.</span></span> <span data-ttu-id="cdf17-130">只有當 *pwzFormat* 為 **Null** 時，才能設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="cdf17-130">This flag can only be set if *pwzFormat* is **NULL**.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="cdf17-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**地區設定 \_ 使用 \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="cdf17-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="cdf17-132">使用系統 ANSI 字碼頁進行字串轉譯，而不是地區設定字碼頁。</span><span class="sxs-lookup"><span data-stu-id="cdf17-132">Uses the system ANSI code page for string translation instead of the locale code page.</span></span>

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span data-ttu-id="cdf17-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**時間 \_ NOMINUTESORSECONDS**</span><span class="sxs-lookup"><span data-stu-id="cdf17-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**TIME\_NOMINUTESORSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="cdf17-134">不會使用分鐘或秒數。</span><span class="sxs-lookup"><span data-stu-id="cdf17-134">Does not use minutes or seconds.</span></span>

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span data-ttu-id="cdf17-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**時間 \_ NOSECONDS**</span><span class="sxs-lookup"><span data-stu-id="cdf17-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TIME\_NOSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="cdf17-136">不會使用秒數。</span><span class="sxs-lookup"><span data-stu-id="cdf17-136">Does not use seconds.</span></span>

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span data-ttu-id="cdf17-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**時間 \_ NOTIMEMARKER**</span><span class="sxs-lookup"><span data-stu-id="cdf17-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**TIME\_NOTIMEMARKER**</span></span>


</dt> <dd>

<span data-ttu-id="cdf17-138">不使用時間標記。</span><span class="sxs-lookup"><span data-stu-id="cdf17-138">Does not use a time marker.</span></span>

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span data-ttu-id="cdf17-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**時間 \_ FORCE24HOURFORMAT**</span><span class="sxs-lookup"><span data-stu-id="cdf17-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**TIME\_FORCE24HOURFORMAT**</span></span>


</dt> <dd>

<span data-ttu-id="cdf17-140">一律使用24小時的時間格式。</span><span class="sxs-lookup"><span data-stu-id="cdf17-140">Always uses a 24-hour time format.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cdf17-141">*lpTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdf17-141">*lpTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf17-142">類型： \**Const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="cdf17-142">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="cdf17-143">[_ *SYSTEMTIME* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)結構的指標，其中包含要格式化的時間資訊。</span><span class="sxs-lookup"><span data-stu-id="cdf17-143">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the time information to be formatted.</span></span> <span data-ttu-id="cdf17-144">如果此指標為 **Null**，則函式會使用目前的本機系統時間。</span><span class="sxs-lookup"><span data-stu-id="cdf17-144">If this pointer is **NULL**, the function uses the current local system time.</span></span>

</dd> <dt>

<span data-ttu-id="cdf17-145">*pwzFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdf17-145">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf17-146">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="cdf17-146">Type: **LPCWSTR**</span></span>

<span data-ttu-id="cdf17-147">用來形成時間字串的格式指標。</span><span class="sxs-lookup"><span data-stu-id="cdf17-147">A pointer to a format to use to form the time string.</span></span> <span data-ttu-id="cdf17-148">如果 *pwzFormat* 為 **Null**，則函式會使用指定地區設定的時間格式。</span><span class="sxs-lookup"><span data-stu-id="cdf17-148">If *pwzFormat* is **NULL**, the function uses the time format of the specified locale.</span></span> <span data-ttu-id="cdf17-149">如需詳細資訊，請參閱 [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) 。</span><span class="sxs-lookup"><span data-stu-id="cdf17-149">See [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="cdf17-150">*pwzTimeStr* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cdf17-150">*pwzTimeStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf17-151">類型： **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="cdf17-151">Type: **LPWSTR**</span></span>

<span data-ttu-id="cdf17-152">接收格式化時間字串的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="cdf17-152">A pointer to a buffer that receives the formatted time string.</span></span>

</dd> <dt>

<span data-ttu-id="cdf17-153">*cchTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdf17-153">*cchTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf17-154">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="cdf17-154">Type: **int**</span></span>

<span data-ttu-id="cdf17-155">*PwzTimeStr* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="cdf17-155">The size, in characters, of the *pwzTimeStr* buffer.</span></span> <span data-ttu-id="cdf17-156">如果 *cchTime* 為零，則函數會傳回保留格式化時間字串所需的字元數，而且不會使用 *pwzTimeStr* 所指向的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cdf17-156">If *cchTime* is zero, the function returns the number of characters required to hold the formatted time string, and the buffer pointed to by *pwzTimeStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdf17-157">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdf17-157">Return value</span></span>

<span data-ttu-id="cdf17-158">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="cdf17-158">Type: **int**</span></span>

<span data-ttu-id="cdf17-159">如果函式成功，則傳回值是寫入 *pwzTimeStr* 所指向之緩衝區的字元數。</span><span class="sxs-lookup"><span data-stu-id="cdf17-159">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzTimeStr*.</span></span> <span data-ttu-id="cdf17-160">如果 *cchTime* 參數為零，則傳回值為保留格式化時間字串所需的字元數。</span><span class="sxs-lookup"><span data-stu-id="cdf17-160">If the *cchTime* parameter is zero, the return value is the number of characters required to hold the formatted time string.</span></span> <span data-ttu-id="cdf17-161">計數包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="cdf17-161">The count includes the terminating null character.</span></span>

<span data-ttu-id="cdf17-162">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="cdf17-162">If the function fails, the return value is zero.</span></span> <span data-ttu-id="cdf17-163">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="cdf17-163">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="cdf17-164">**GetLastError** 可能會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cdf17-164">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="cdf17-165">**\_緩衝區不足的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="cdf17-165">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="cdf17-166">**錯誤 \_ 不正確 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="cdf17-166">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="cdf17-167">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="cdf17-167">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cdf17-168">備註</span><span class="sxs-lookup"><span data-stu-id="cdf17-168">Remarks</span></span>

<span data-ttu-id="cdf17-169">**GetTimeFormatWrapW** 能讓您在 Windows XP 之前的作業系統中使用 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="cdf17-169">**GetTimeFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="cdf17-170">慣用的方法是使用 [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。</span><span class="sxs-lookup"><span data-stu-id="cdf17-170">The preferred method is to use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="cdf17-171">您必須使用序數310，直接從 Shlwapi.dll 呼叫 **GetTimeFormatWrapW** 。</span><span class="sxs-lookup"><span data-stu-id="cdf17-171">**GetTimeFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 310.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdf17-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdf17-172">Requirements</span></span>



| <span data-ttu-id="cdf17-173">需求</span><span class="sxs-lookup"><span data-stu-id="cdf17-173">Requirement</span></span> | <span data-ttu-id="cdf17-174">值</span><span class="sxs-lookup"><span data-stu-id="cdf17-174">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf17-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cdf17-175">Minimum supported client</span></span><br/> | <span data-ttu-id="cdf17-176">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdf17-176">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cdf17-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cdf17-177">Minimum supported server</span></span><br/> | <span data-ttu-id="cdf17-178">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cdf17-178">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cdf17-179">DLL</span><span class="sxs-lookup"><span data-stu-id="cdf17-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdf17-180"><dt>Shlwapi.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="cdf17-180"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdf17-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdf17-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf17-182">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="cdf17-182">**GetTimeFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
