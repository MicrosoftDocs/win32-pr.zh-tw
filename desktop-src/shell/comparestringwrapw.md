---
description: 使用指定的地區設定，比較兩個 Unicode 字元字串。
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: CompareStringWrapW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 0731182f5c01ad56db722972628d2cbe39373835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972064"
---
# <a name="comparestringwrapw-function"></a><span data-ttu-id="544b0-103">CompareStringWrapW 函式</span><span class="sxs-lookup"><span data-stu-id="544b0-103">CompareStringWrapW function</span></span>

<span data-ttu-id="544b0-104">\[**CompareStringWrapW** 可用於 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="544b0-104">\[**CompareStringWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="544b0-105">在後續版本中將無法使用。</span><span class="sxs-lookup"><span data-stu-id="544b0-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="544b0-106">您應該在其位置使用 [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 。\]</span><span class="sxs-lookup"><span data-stu-id="544b0-106">You should use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in its place.\]</span></span>

<span data-ttu-id="544b0-107">使用指定的地區設定，比較兩個 Unicode 字元字串。</span><span class="sxs-lookup"><span data-stu-id="544b0-107">Compares two Unicode character strings, using a specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="544b0-108">**CompareStringWrapW** 是 **CompareStringW** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="544b0-108">**CompareStringWrapW** is a wrapper for the **CompareStringW** function.</span></span> <span data-ttu-id="544b0-109">如需進一步的使用注意事項，請參閱 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 頁面。</span><span class="sxs-lookup"><span data-stu-id="544b0-109">See the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="544b0-110">語法</span><span class="sxs-lookup"><span data-stu-id="544b0-110">Syntax</span></span>


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a><span data-ttu-id="544b0-111">參數</span><span class="sxs-lookup"><span data-stu-id="544b0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="544b0-112">*地區* \[ 設定在\]</span><span class="sxs-lookup"><span data-stu-id="544b0-112">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="544b0-113">類型： **LCID**</span><span class="sxs-lookup"><span data-stu-id="544b0-113">Type: **LCID**</span></span>

<span data-ttu-id="544b0-114">用於比較的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="544b0-114">A locale identifier used for the comparison.</span></span> <span data-ttu-id="544b0-115">這個參數可以是下列其中一個預先定義的地區設定識別碼，或 [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) 宏所建立的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="544b0-115">This parameter can be one of the following predefined locale identifiers or a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="544b0-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**地區設定 \_ 系統 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="544b0-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="544b0-117">系統的預設地區設定。</span><span class="sxs-lookup"><span data-stu-id="544b0-117">The system's default locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="544b0-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**地區設定 \_ 使用者 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="544b0-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="544b0-119">目前使用者的預設地區設定。</span><span class="sxs-lookup"><span data-stu-id="544b0-119">The current user's default locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="544b0-120">*dwCmpFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="544b0-120">*dwCmpFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="544b0-121">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="544b0-121">Type: **DWORD**</span></span>

<span data-ttu-id="544b0-122">旗標，指出函數如何比較兩個字串。</span><span class="sxs-lookup"><span data-stu-id="544b0-122">The flags that indicate how the function compares the two strings.</span></span> <span data-ttu-id="544b0-123">依預設，不會設定這些旗標。</span><span class="sxs-lookup"><span data-stu-id="544b0-123">By default, these flags are not set.</span></span> <span data-ttu-id="544b0-124">設定為零以取得預設行為或下列值的任何組合。</span><span class="sxs-lookup"><span data-stu-id="544b0-124">Set to zero to get the default behavior or to any combination of the following values.</span></span>

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span data-ttu-id="544b0-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**標準 \_ IGNORECASE**</span><span class="sxs-lookup"><span data-stu-id="544b0-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**NORM\_IGNORECASE**</span></span>


</dt> <dd>

<span data-ttu-id="544b0-126">忽略大小寫。</span><span class="sxs-lookup"><span data-stu-id="544b0-126">Ignore case.</span></span>

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span data-ttu-id="544b0-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**標準 \_ IGNOREKANATYPE**</span><span class="sxs-lookup"><span data-stu-id="544b0-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**NORM\_IGNOREKANATYPE**</span></span>


</dt> <dd>

<span data-ttu-id="544b0-128">請勿區分平假名和片假名字元。</span><span class="sxs-lookup"><span data-stu-id="544b0-128">Do not differentiate between Hiragana and Katakana characters.</span></span> <span data-ttu-id="544b0-129">對應的平假名和片假名字元比較為相等。</span><span class="sxs-lookup"><span data-stu-id="544b0-129">Corresponding Hiragana and Katakana characters compare as equal.</span></span>

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span data-ttu-id="544b0-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**標準 \_ IGNORENONSPACE**</span><span class="sxs-lookup"><span data-stu-id="544b0-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**NORM\_IGNORENONSPACE**</span></span>


</dt> <dd>

<span data-ttu-id="544b0-131">忽略非空白字元。</span><span class="sxs-lookup"><span data-stu-id="544b0-131">Ignore nonspacing characters.</span></span>

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span data-ttu-id="544b0-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**標準 \_ IGNORESYMBOLS**</span><span class="sxs-lookup"><span data-stu-id="544b0-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**NORM\_IGNORESYMBOLS**</span></span>


</dt> <dd>

<span data-ttu-id="544b0-133">忽略符號。</span><span class="sxs-lookup"><span data-stu-id="544b0-133">Ignore symbols.</span></span>

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span data-ttu-id="544b0-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**標準 \_ IGNOREWIDTH**</span><span class="sxs-lookup"><span data-stu-id="544b0-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**NORM\_IGNOREWIDTH**</span></span>


</dt> <dd>

<span data-ttu-id="544b0-135">請勿區分單一位元組字元和與雙位元組字元相同的字元。</span><span class="sxs-lookup"><span data-stu-id="544b0-135">Do not differentiate between a single-byte character and the same character as a double-byte character.</span></span>

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span data-ttu-id="544b0-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**排序 \_ STRINGSORT**</span><span class="sxs-lookup"><span data-stu-id="544b0-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**SORT\_STRINGSORT**</span></span>


</dt> <dd>

<span data-ttu-id="544b0-137">將標點符號視為與符號相同。</span><span class="sxs-lookup"><span data-stu-id="544b0-137">Treat punctuation the same as symbols.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="544b0-138">*lpString1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="544b0-138">*lpString1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="544b0-139">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="544b0-139">Type: **LPCWSTR**</span></span>

<span data-ttu-id="544b0-140">要比較之第一個 Unicode 字串的指標。</span><span class="sxs-lookup"><span data-stu-id="544b0-140">A pointer to the first Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="544b0-141">*cchCount1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="544b0-141">*cchCount1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="544b0-142">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="544b0-142">Type: **int**</span></span>

<span data-ttu-id="544b0-143">*LpString1* 參數所指向之字串中的字元數。</span><span class="sxs-lookup"><span data-stu-id="544b0-143">The number of characters in the string pointed to by the *lpString1* parameter.</span></span> <span data-ttu-id="544b0-144">此計數不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="544b0-144">The count does not include the terminating null character.</span></span> <span data-ttu-id="544b0-145">如果此參數為負值，則會假設字串是以 null 終止，且會自動計算長度。</span><span class="sxs-lookup"><span data-stu-id="544b0-145">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="544b0-146">*lpString2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="544b0-146">*lpString2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="544b0-147">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="544b0-147">Type: **LPCWSTR**</span></span>

<span data-ttu-id="544b0-148">要比較之第二個 Unicode 字串的指標。</span><span class="sxs-lookup"><span data-stu-id="544b0-148">A pointer to the second Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="544b0-149">*cchCount2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="544b0-149">*cchCount2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="544b0-150">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="544b0-150">Type: **int**</span></span>

<span data-ttu-id="544b0-151">*LpString2* 參數所指向之字串中的字元數。</span><span class="sxs-lookup"><span data-stu-id="544b0-151">The number of characters in the string pointed to by the *lpString2* parameter.</span></span> <span data-ttu-id="544b0-152">此計數不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="544b0-152">The count does not include the terminating null character.</span></span> <span data-ttu-id="544b0-153">如果此參數為負值，則會假設字串是以 null 終止，且會自動計算長度。</span><span class="sxs-lookup"><span data-stu-id="544b0-153">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="544b0-154">傳回值</span><span class="sxs-lookup"><span data-stu-id="544b0-154">Return value</span></span>

<span data-ttu-id="544b0-155">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="544b0-155">Type: **int**</span></span>

<span data-ttu-id="544b0-156">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="544b0-156">If the function fails, the return value is zero.</span></span> <span data-ttu-id="544b0-157">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="544b0-157">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="544b0-158">**GetLastError** 可能會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="544b0-158">**GetLastError** may return one of the following error codes.</span></span>

-   <span data-ttu-id="544b0-159">錯誤 \_ 不正確 \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="544b0-159">ERROR\_INVALID\_FLAGS</span></span>
-   <span data-ttu-id="544b0-160">錯誤 \_ 不正確 \_ 參數</span><span class="sxs-lookup"><span data-stu-id="544b0-160">ERROR\_INVALID\_PARAMETER</span></span>

<span data-ttu-id="544b0-161">如果函式成功，則傳回值是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="544b0-161">If the function succeeds, the return value is one of the following values.</span></span> 

| <span data-ttu-id="544b0-162">需求</span><span class="sxs-lookup"><span data-stu-id="544b0-162">Requirement</span></span> | <span data-ttu-id="544b0-163">值</span><span class="sxs-lookup"><span data-stu-id="544b0-163">Value</span></span> |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="544b0-164">CSTR \_ 小於 \_</span><span class="sxs-lookup"><span data-stu-id="544b0-164">CSTR\_LESS\_THAN</span></span>    | <span data-ttu-id="544b0-165">*LpString1* 參數所指向的字串，在詞法值中小於 *lpString2* 參數所指向的字串。</span><span class="sxs-lookup"><span data-stu-id="544b0-165">The string pointed to by the *lpString1* parameter is less in lexical value than the string pointed to by the *lpString2* parameter.</span></span> |
| <span data-ttu-id="544b0-166">CSTR \_ 等於</span><span class="sxs-lookup"><span data-stu-id="544b0-166">CSTR\_EQUAL</span></span>         | <span data-ttu-id="544b0-167">*LpString1* 所指向的字串在詞法值中等於 *lpString2* 所指向的字串。</span><span class="sxs-lookup"><span data-stu-id="544b0-167">The string pointed to by *lpString1* is equal in lexical value to the string pointed to by *lpString2*.</span></span>                              |
| <span data-ttu-id="544b0-168">CSTR \_ 大於 \_</span><span class="sxs-lookup"><span data-stu-id="544b0-168">CSTR\_GREATER\_THAN</span></span> | <span data-ttu-id="544b0-169">*LpString1* 所指向的字串在詞法值中大於 *lpString2* 所指向的字串</span><span class="sxs-lookup"><span data-stu-id="544b0-169">The string pointed to by *lpString1* is greater in lexical value than the string pointed to by *lpString2*</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="544b0-170">備註</span><span class="sxs-lookup"><span data-stu-id="544b0-170">Remarks</span></span>

<span data-ttu-id="544b0-171">**安全性警告：** 使用此函式不正確，可能會危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="544b0-171">**Security Warning:** Using this function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="544b0-172">未正確比較的字串可能會產生不正確輸入。</span><span class="sxs-lookup"><span data-stu-id="544b0-172">Strings that are not compared correctly can produce invalid input.</span></span> <span data-ttu-id="544b0-173">測試字串以確保它們在使用之前都有效，並提供錯誤處理常式。</span><span class="sxs-lookup"><span data-stu-id="544b0-173">Test strings to make sure they are valid before using them and provide error handlers.</span></span> <span data-ttu-id="544b0-174">如需詳細資訊，請參閱 [安全性考慮：國際功能](../intl/security-considerations--international-features.md)</span><span class="sxs-lookup"><span data-stu-id="544b0-174">For more information, see [Security Considerations: International Features](../intl/security-considerations--international-features.md)</span></span>

<span data-ttu-id="544b0-175">慣用的方法是使用 [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。</span><span class="sxs-lookup"><span data-stu-id="544b0-175">The preferred method is to use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="544b0-176">您必須使用序數45，直接從 Shlwapi.dll 呼叫 **CompareStringWrapW** 。</span><span class="sxs-lookup"><span data-stu-id="544b0-176">**CompareStringWrapW** must be called directly from Shlwapi.dll, using ordinal 45.</span></span>

## <a name="requirements"></a><span data-ttu-id="544b0-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="544b0-177">Requirements</span></span>



| <span data-ttu-id="544b0-178">需求</span><span class="sxs-lookup"><span data-stu-id="544b0-178">Requirement</span></span> | <span data-ttu-id="544b0-179">值</span><span class="sxs-lookup"><span data-stu-id="544b0-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="544b0-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="544b0-180">Minimum supported client</span></span><br/> | <span data-ttu-id="544b0-181">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="544b0-181">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="544b0-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="544b0-182">Minimum supported server</span></span><br/> | <span data-ttu-id="544b0-183">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="544b0-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="544b0-184">標頭</span><span class="sxs-lookup"><span data-stu-id="544b0-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="544b0-185"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="544b0-185"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="544b0-186">DLL</span><span class="sxs-lookup"><span data-stu-id="544b0-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="544b0-187"><dt>Shlwapi.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="544b0-187"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="544b0-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="544b0-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="544b0-189">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="544b0-189">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
