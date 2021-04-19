---
description: 比較兩個腳本的列舉清單。
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: 'DownlevelVerifyScripts 函式 (Idndl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 62e029576d53109e3c57faf4ec913472f8aea65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980000"
---
# <a name="downlevelverifyscripts-function"></a><span data-ttu-id="4ec22-103">DownlevelVerifyScripts 函式</span><span class="sxs-lookup"><span data-stu-id="4ec22-103">DownlevelVerifyScripts function</span></span>

<span data-ttu-id="4ec22-104">比較兩個腳本的列舉清單。</span><span class="sxs-lookup"><span data-stu-id="4ec22-104">Compares two enumerated lists of scripts.</span></span>

> [!Note]  
> <span data-ttu-id="4ec22-105">只有在 Windows Vista 之前的作業系統上執行的應用程式，才會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="4ec22-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="4ec22-106">其用途需要下載套件。</span><span class="sxs-lookup"><span data-stu-id="4ec22-106">Its use requires the download package.</span></span> <span data-ttu-id="4ec22-107">只在 Windows Vista 和更新版本上執行的應用程式應該呼叫 [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)。</span><span class="sxs-lookup"><span data-stu-id="4ec22-107">Applications that only run on Windows Vista and later should call [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4ec22-108">語法</span><span class="sxs-lookup"><span data-stu-id="4ec22-108">Syntax</span></span>


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a><span data-ttu-id="4ec22-109">參數</span><span class="sxs-lookup"><span data-stu-id="4ec22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ec22-110">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ec22-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec22-111">指定腳本驗證選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="4ec22-111">Flags specifying script verification options.</span></span>



| <span data-ttu-id="4ec22-112">值</span><span class="sxs-lookup"><span data-stu-id="4ec22-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="4ec22-113">意義</span><span class="sxs-lookup"><span data-stu-id="4ec22-113">Meaning</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <span data-ttu-id="4ec22-114"><dt>**VS \_ 允許 \_ 拉丁**</dt></span><span class="sxs-lookup"><span data-stu-id="4ec22-114"><dt>**VS\_ALLOW\_LATIN**</dt></span></span> </dl> | <span data-ttu-id="4ec22-115">在測試清單中允許 "Latn" (拉丁腳本) ，即使它不在地區設定清單中也一樣。</span><span class="sxs-lookup"><span data-stu-id="4ec22-115">Allow "Latn" (Latin script) in the test list, even if it is not in the locale list.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4ec22-116">*lpLocaleScripts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ec22-116">*lpLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec22-117">地區設定清單的指標，也就是指定地區設定的腳本列舉清單。</span><span class="sxs-lookup"><span data-stu-id="4ec22-117">Pointer to the locale list, the enumerated list of scripts for a given locale.</span></span> <span data-ttu-id="4ec22-118">這份清單通常會藉由呼叫 [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)來填入。</span><span class="sxs-lookup"><span data-stu-id="4ec22-118">This list is typically populated by calling [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ec22-119">*cchLocaleScripts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ec22-119">*cchLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec22-120">*LpLocaleScripts* 所表示之字串的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4ec22-120">Size, in characters, of the string indicated by *lpLocaleScripts*.</span></span> <span data-ttu-id="4ec22-121">如果字串是以 null 終止，則應用程式會將此參數設定為-1。</span><span class="sxs-lookup"><span data-stu-id="4ec22-121">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="4ec22-122">如果此參數設定為0，則函數會失敗。</span><span class="sxs-lookup"><span data-stu-id="4ec22-122">If this parameter is set to 0, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="4ec22-123">*lpTestScripts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ec22-123">*lpTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec22-124">測試清單的指標，也就是腳本的第二個列舉清單。</span><span class="sxs-lookup"><span data-stu-id="4ec22-124">Pointer to the test list, a second enumerated list of scripts.</span></span> <span data-ttu-id="4ec22-125">這份清單通常會藉由呼叫 [**DownlevelGetStringScripts**](downlevelgetstringscripts.md)來填入。</span><span class="sxs-lookup"><span data-stu-id="4ec22-125">This list is typically populated by calling [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ec22-126">*cchTestScripts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ec22-126">*cchTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec22-127">*LpTestScripts* 所表示之字串的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4ec22-127">Size, in characters, of the string indicated by *lpTestScripts*.</span></span> <span data-ttu-id="4ec22-128">如果字串是以 null 終止，則應用程式會將此參數設定為-1。</span><span class="sxs-lookup"><span data-stu-id="4ec22-128">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="4ec22-129">如果此參數設定為0，則函數會失敗。</span><span class="sxs-lookup"><span data-stu-id="4ec22-129">If this parameter is set to 0, the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ec22-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ec22-130">Return value</span></span>

<span data-ttu-id="4ec22-131">如果測試清單不是空白，而且清單中的所有專案也包含在地區設定清單中，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="4ec22-131">Returns **TRUE** if the test list is non-empty and all items in the list are also included in the locale list.</span></span> <span data-ttu-id="4ec22-132">否則，函數會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="4ec22-132">Otherwise, the function returns **FALSE**.</span></span>

<span data-ttu-id="4ec22-133">如果傳回值為 **FALSE** ，則表示測試清單包含不在地區設定清單中的專案，或可能表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4ec22-133">A return value of **FALSE** can indicate that the test list contains an item that is not in the locale list, or it can indicate an error.</span></span> <span data-ttu-id="4ec22-134">若要區分這兩種情況，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="4ec22-134">To distinguish between these two cases, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="4ec22-135">如果 **DownlevelVerifyScripts** 成功判斷出測試清單中的專案不在地區設定清單中，則 **GETLASTERROR** 會傳回錯誤 \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="4ec22-135">If **DownlevelVerifyScripts** has successfully determined that there is an item in the test list that is not in the locale list, **GetLastError** returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="4ec22-136">否則， **GetLastError** 可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="4ec22-136">Otherwise, **GetLastError** can return one of the following error codes:</span></span>

-   <span data-ttu-id="4ec22-137">錯誤 \_ 無效 \_ 的旗標。</span><span class="sxs-lookup"><span data-stu-id="4ec22-137">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="4ec22-138">為旗標提供的值無效。</span><span class="sxs-lookup"><span data-stu-id="4ec22-138">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="4ec22-139">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="4ec22-139">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="4ec22-140">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="4ec22-140">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ec22-141">備註</span><span class="sxs-lookup"><span data-stu-id="4ec22-141">Remarks</span></span>

<span data-ttu-id="4ec22-142">此函數會比較字串，例如 "Latn;Cyrl; "，其中包含一連串4個字元的腳本名稱，每個腳本名稱後面加上分號。</span><span class="sxs-lookup"><span data-stu-id="4ec22-142">This function compares strings, such as "Latn;Cyrl;", that consist of a series of 4-character script names, with each script name followed by a semicolon.</span></span> <span data-ttu-id="4ec22-143">此外，它也有特殊的案例，因為拉丁腳本通常用於不是原生的語言和地區設定。</span><span class="sxs-lookup"><span data-stu-id="4ec22-143">It also has a special case to account for the fact that the Latin script is often used in languages and locales for which it is not native.</span></span>

<span data-ttu-id="4ec22-144">這項功能可作為策略的一部分，以降低與國際化功能變數名稱相關的安全性問題 [ (IDNs) ](handling-internationalized-domain-names--idns.md)。</span><span class="sxs-lookup"><span data-stu-id="4ec22-144">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="4ec22-145">以下是此函式的傳回範例，以及在各種案例中對 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 的後續呼叫。</span><span class="sxs-lookup"><span data-stu-id="4ec22-145">The following are examples of the return of this function and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in various scenarios.</span></span> <span data-ttu-id="4ec22-146">最後兩個範例分別說明測試清單缺少結束分號 (格式錯誤的字串) 和測試清單空白的案例。</span><span class="sxs-lookup"><span data-stu-id="4ec22-146">The last two examples illustrate, respectively, a case in which the test list lacks a terminating semicolon (malformed string) and a case in which the test list is empty.</span></span>



| <span data-ttu-id="4ec22-147">"Locale" 字串</span><span class="sxs-lookup"><span data-stu-id="4ec22-147">"Locale" string</span></span> | <span data-ttu-id="4ec22-148">"Test" 字串</span><span class="sxs-lookup"><span data-stu-id="4ec22-148">"Test" string</span></span> | <span data-ttu-id="4ec22-149">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="4ec22-149">*dwFlags*</span></span>        | <span data-ttu-id="4ec22-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ec22-150">Return value</span></span> | <span data-ttu-id="4ec22-151">GetLastError return</span><span class="sxs-lookup"><span data-stu-id="4ec22-151">GetLastError return</span></span>       |
|-----------------|---------------|------------------|--------------|---------------------------|
| <span data-ttu-id="4ec22-152">Hani;Hira;區分</span><span class="sxs-lookup"><span data-stu-id="4ec22-152">Hani;Hira;Kana;</span></span> | <span data-ttu-id="4ec22-153">Hani;</span><span class="sxs-lookup"><span data-stu-id="4ec22-153">Hani;</span></span>         | <span data-ttu-id="4ec22-154">N/A</span><span class="sxs-lookup"><span data-stu-id="4ec22-154">N/A</span></span>              | <span data-ttu-id="4ec22-155">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="4ec22-155">**TRUE**</span></span>     | <span data-ttu-id="4ec22-156">N/A</span><span class="sxs-lookup"><span data-stu-id="4ec22-156">N/A</span></span>                       |
| <span data-ttu-id="4ec22-157">Hani;Hira;區分</span><span class="sxs-lookup"><span data-stu-id="4ec22-157">Hani;Hira;Kana;</span></span> | <span data-ttu-id="4ec22-158">Hani;Latn;</span><span class="sxs-lookup"><span data-stu-id="4ec22-158">Hani;Latn;</span></span>    | <span data-ttu-id="4ec22-159">0</span><span class="sxs-lookup"><span data-stu-id="4ec22-159">0</span></span>                | <span data-ttu-id="4ec22-160">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="4ec22-160">**FALSE**</span></span>    | <span data-ttu-id="4ec22-161">錯誤 \_ 成功</span><span class="sxs-lookup"><span data-stu-id="4ec22-161">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="4ec22-162">Hani;Hira;區分</span><span class="sxs-lookup"><span data-stu-id="4ec22-162">Hani;Hira;Kana;</span></span> | <span data-ttu-id="4ec22-163">Hani;Latn;</span><span class="sxs-lookup"><span data-stu-id="4ec22-163">Hani;Latn;</span></span>    | <span data-ttu-id="4ec22-164">VS \_ 允許 \_ 拉丁</span><span class="sxs-lookup"><span data-stu-id="4ec22-164">VS\_ALLOW\_LATIN</span></span> | <span data-ttu-id="4ec22-165">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="4ec22-165">**TRUE**</span></span>     | <span data-ttu-id="4ec22-166">N/A</span><span class="sxs-lookup"><span data-stu-id="4ec22-166">N/A</span></span>                       |
| <span data-ttu-id="4ec22-167">Hani;Hira;區分</span><span class="sxs-lookup"><span data-stu-id="4ec22-167">Hani;Hira;Kana;</span></span> | <span data-ttu-id="4ec22-168">Cyrl;</span><span class="sxs-lookup"><span data-stu-id="4ec22-168">Cyrl;</span></span>         | <span data-ttu-id="4ec22-169">N/A</span><span class="sxs-lookup"><span data-stu-id="4ec22-169">N/A</span></span>              | <span data-ttu-id="4ec22-170">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="4ec22-170">**FALSE**</span></span>    | <span data-ttu-id="4ec22-171">錯誤 \_ 成功</span><span class="sxs-lookup"><span data-stu-id="4ec22-171">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="4ec22-172">Hani;Hira;區分</span><span class="sxs-lookup"><span data-stu-id="4ec22-172">Hani;Hira;Kana;</span></span> | <span data-ttu-id="4ec22-173">Cyrl;</span><span class="sxs-lookup"><span data-stu-id="4ec22-173">Cyrl;</span></span>         | <span data-ttu-id="4ec22-174">N/A</span><span class="sxs-lookup"><span data-stu-id="4ec22-174">N/A</span></span>              | <span data-ttu-id="4ec22-175">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="4ec22-175">**FALSE**</span></span>    | <span data-ttu-id="4ec22-176">錯誤 \_ 不正確 \_ 參數</span><span class="sxs-lookup"><span data-stu-id="4ec22-176">ERROR\_INVALID\_PARAMETER</span></span> |
| <span data-ttu-id="4ec22-177">Hani;Hira;區分</span><span class="sxs-lookup"><span data-stu-id="4ec22-177">Hani;Hira;Kana;</span></span> |               | <span data-ttu-id="4ec22-178">N/A</span><span class="sxs-lookup"><span data-stu-id="4ec22-178">N/A</span></span>              | <span data-ttu-id="4ec22-179">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="4ec22-179">**FALSE**</span></span>    | <span data-ttu-id="4ec22-180">錯誤 \_ 成功</span><span class="sxs-lookup"><span data-stu-id="4ec22-180">ERROR\_SUCCESS</span></span>            |



 

<span data-ttu-id="4ec22-181">必要的標頭檔和 DLL 是「 [Microsoft 國際化功能變數名稱 (IDN) 緩和 api](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) 」下載的一部分，可從 [MSDN 下載中心](https://www.microsoft.com/?ref=go)取得。</span><span class="sxs-lookup"><span data-stu-id="4ec22-181">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ec22-182">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ec22-182">Requirements</span></span>



| <span data-ttu-id="4ec22-183">需求</span><span class="sxs-lookup"><span data-stu-id="4ec22-183">Requirement</span></span> | <span data-ttu-id="4ec22-184">值</span><span class="sxs-lookup"><span data-stu-id="4ec22-184">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec22-185">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ec22-185">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec22-186">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ec22-186">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                  |
| <span data-ttu-id="4ec22-187">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ec22-187">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec22-188">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ec22-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                         |
| <span data-ttu-id="4ec22-189">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4ec22-189">Redistributable</span></span><br/>          | <span data-ttu-id="4ec22-190">Microsoft 國際化功能變數名稱 (IDN) 緩和 Api 于 windows XP SP2、Windows Server 2003 SP1、orWindows Vista</span><span class="sxs-lookup"><span data-stu-id="4ec22-190">Microsoft Internationalized Domain Name (IDN) Mitigation APIs onWindows XP with SP2,Windows Server 2003 with SP1, orWindows Vista</span></span><br/> |
| <span data-ttu-id="4ec22-191">標頭</span><span class="sxs-lookup"><span data-stu-id="4ec22-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ec22-192"><dt>Idndl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ec22-192"><dt>Idndl.h</dt></span></span> </dl>                                                           |
| <span data-ttu-id="4ec22-193">DLL</span><span class="sxs-lookup"><span data-stu-id="4ec22-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ec22-194"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ec22-194"><dt>Idndl.dll</dt></span></span> </dl>                                                         |



## <a name="see-also"></a><span data-ttu-id="4ec22-195">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ec22-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec22-196">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="4ec22-196">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="4ec22-197">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="4ec22-197">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="4ec22-198">處理國際化功能變數名稱 (IDNs) </span><span class="sxs-lookup"><span data-stu-id="4ec22-198">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="4ec22-199">**DownlevelGetLocaleScripts**</span><span class="sxs-lookup"><span data-stu-id="4ec22-199">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="4ec22-200">**DownlevelGetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="4ec22-200">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="4ec22-201">**VerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="4ec22-201">**VerifyScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
