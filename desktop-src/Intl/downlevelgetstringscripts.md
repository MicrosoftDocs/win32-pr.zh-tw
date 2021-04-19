---
description: 提供指定之 Unicode 字串中所使用的腳本清單。
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: 'DownlevelGetStringScripts 函式 (Idndl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: bc5a9fdaf3beb9e1c401943f923fa48bd9d4b44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975260"
---
# <a name="downlevelgetstringscripts-function"></a><span data-ttu-id="b6f2a-103">DownlevelGetStringScripts 函式</span><span class="sxs-lookup"><span data-stu-id="b6f2a-103">DownlevelGetStringScripts function</span></span>

<span data-ttu-id="b6f2a-104">提供指定之 Unicode 字串中所使用的腳本清單。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-104">Provides a list of scripts used in the specified Unicode string.</span></span>

> [!Note]  
> <span data-ttu-id="b6f2a-105">只有在 Windows Vista 之前的作業系統上執行的應用程式，才會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="b6f2a-106">其用途需要下載套件。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-106">Its use requires the download package.</span></span> <span data-ttu-id="b6f2a-107">只在 Windows Vista 和更新版本上執行的應用程式應該呼叫 [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-107">Applications that only run on Windows Vista and later should call [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b6f2a-108">語法</span><span class="sxs-lookup"><span data-stu-id="b6f2a-108">Syntax</span></span>


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="b6f2a-109">參數</span><span class="sxs-lookup"><span data-stu-id="b6f2a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6f2a-110">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6f2a-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6f2a-111">指定腳本抓取選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-111">Flags specifying options for script retrieval.</span></span>



| <span data-ttu-id="b6f2a-112">值</span><span class="sxs-lookup"><span data-stu-id="b6f2a-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="b6f2a-113">意義</span><span class="sxs-lookup"><span data-stu-id="b6f2a-113">Meaning</span></span>                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <span data-ttu-id="b6f2a-114"><dt>**GSS \_ 允許 \_ 繼承 \_ 通用**</dt></span><span class="sxs-lookup"><span data-stu-id="b6f2a-114"><dt>**GSS\_ALLOW\_INHERITED\_COMMON**</dt></span></span> </dl> | <span data-ttu-id="b6f2a-115">取出 "Qaii" (繼承) 和 "Zyyy" (通用) 腳本資訊。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-115">Retrieve "Qaii" (INHERITED) and "Zyyy" (COMMON) script information.</span></span> <span data-ttu-id="b6f2a-116">此值不會影響未指派字元的處理。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-116">This value does not affect the processing of unassigned characters.</span></span> <span data-ttu-id="b6f2a-117">輸入字串中的這些字元一律會導致「Zzzz」 (未指派的腳本) 出現在腳本字串中。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-117">These characters in the input string always cause a "Zzzz" (UNASSIGNED script) to appear in the script string.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="b6f2a-118">根據預設，此函式會忽略輸入 Unicode 字串中的任何繼承或一般字元。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-118">By default, this function ignores any inherited or common characters in the input Unicode string.</span></span> <span data-ttu-id="b6f2a-119">如果 \_ \_ \_ 未設定 [GSS 允許繼承的一般]，即使輸入字串包含這類字元，腳本字串中都不會出現 "Qaii" 或 "Zyyy"。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-119">If GSS\_ALLOW\_INHERITED\_COMMON is not set, neither "Qaii" nor "Zyyy" will appear in the script string, even if the input string contains such characters.</span></span> <span data-ttu-id="b6f2a-120">如果 \_ 已設定 [GSS 允許 \_ 繼承 \_ 一般]，而且輸入字串包含繼承和/或通用字元，則腳本字串中會出現 "Qaii" 和/或 "Zyyy"。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-120">If GSS\_ALLOW\_INHERITED\_COMMON is set, and if the input string contains inherited and/or common characters, "Qaii" and/or "Zyyy" appear in the script string.</span></span> <span data-ttu-id="b6f2a-121">請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-121">See the Remarks section.</span></span>

 

</dd> <dt>

<span data-ttu-id="b6f2a-122">*lpString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6f2a-122">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6f2a-123">要分析的 Unicode 字串指標。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-123">Pointer to the Unicode string to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="b6f2a-124">*cchString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6f2a-124">*cchString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6f2a-125">*LpString* 所表示之 Unicode 字串的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-125">Size, in characters, of the Unicode string indicated by *lpString*.</span></span> <span data-ttu-id="b6f2a-126">如果字串是以 null 終止，則應用程式會將此參數設定為-1。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-126">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="b6f2a-127">如果應用程式將此參數設定為0，則函式會 \\ 在 *lpScripts* 中 )  (L "0" 的 null Unicode 字串，並傳回1。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-127">If the application sets this parameter to 0, the function retrieves a null Unicode string (L"\\0") in *lpScripts* and returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="b6f2a-128">*lpScripts* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b6f2a-128">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6f2a-129">緩衝區的指標，此函式會使用 [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html)中使用的4個字元標記法，來抓取表示腳本清單的以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-129">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="b6f2a-130">每個腳本名稱都是由四個拉丁字元所組成，而且名稱會依字母順序抓取。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-130">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="b6f2a-131">每個名稱（包括最後一個）後面都會加上分號。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-131">Each name, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="b6f2a-132">或者，如果 *cchScripts* 設為0，則此參數可以包含 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-132">Alternatively, this parameter can contain **NULL** if *cchScripts* set to 0.</span></span> <span data-ttu-id="b6f2a-133">在此情況下，函數會傳回腳本緩衝區所需的大小。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-133">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b6f2a-134">*cchScripts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6f2a-134">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6f2a-135">*LpScripts* 所指出的腳本緩衝區大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-135">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="b6f2a-136">或者，應用程式可以將此參數設定為0。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-136">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="b6f2a-137">在此情況下，此函式會在 *lpScripts* 中抓取 **Null** ，並傳回腳本緩衝區所需的大小。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-137">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6f2a-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6f2a-138">Return value</span></span>

<span data-ttu-id="b6f2a-139">如果成功且 *cchScripts* 設為非零值，則傳回在輸出緩衝區中取出的字元數，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-139">Returns the number of characters retrieved in the output buffer, including a terminating null character, if successful and *cchScripts* is set to a nonzero value.</span></span> <span data-ttu-id="b6f2a-140">此函式會傳回1，表示找不到任何腳本，例如，當輸入字串只包含通用或繼承字元，而且 \_ \_ 未設定 GSS 允許繼承 \_ 的一般時。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-140">The function returns 1 to indicate that no script has been found, for example, when the input string only contains COMMON or INHERITED characters and GSS\_ALLOW\_INHERITED\_COMMON is not set.</span></span> <span data-ttu-id="b6f2a-141">假設每個找到的腳本會將五個字元加 (四個字元 + 分隔符號) ，簡單的數學運算會提供 (傳回 \_ 碼 1) /5 的腳本計數。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-141">Given that each found script adds five characters (four characters + delimiter), a simple mathematical operation provides the script count as (return\_code - 1) / 5.</span></span>

<span data-ttu-id="b6f2a-142">如果函式成功，且 *cchScripts* 的值為0，則傳回值為腳本緩衝區所需的大小（以字元為單位，包括結束的 null 字元）。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-142">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span> <span data-ttu-id="b6f2a-143">腳本計數如上所述。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-143">The script count is as described above.</span></span>

<span data-ttu-id="b6f2a-144">如果不成功，函數會傳回0。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-144">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="b6f2a-145">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="b6f2a-145">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="b6f2a-146">錯誤 \_ BADDB。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-146">ERROR\_BADDB.</span></span> <span data-ttu-id="b6f2a-147">函數無法存取資料。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-147">The function could not access the data.</span></span> <span data-ttu-id="b6f2a-148">通常不會發生這種情況，通常表示安裝不良、磁片問題或類似。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-148">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="b6f2a-149">\_緩衝區不足 \_ 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-149">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="b6f2a-150">提供的緩衝區大小不夠大，或未正確設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-150">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="b6f2a-151">錯誤 \_ 無效 \_ 的旗標。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-151">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="b6f2a-152">為旗標提供的值無效。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-152">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="b6f2a-153">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-153">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="b6f2a-154">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-154">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6f2a-155">備註</span><span class="sxs-lookup"><span data-stu-id="b6f2a-155">Remarks</span></span>

<span data-ttu-id="b6f2a-156">這項功能可作為策略的一部分，以降低與國際化功能變數名稱相關的安全性問題 [ (IDNs) ](handling-internationalized-domain-names--idns.md)。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-156">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="b6f2a-157">腳本判斷是以中 Unicode 協會所發行的腳本值為基礎 <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> ，不同之處在于未指派的字元具有值 "Zzzz" (未指派) ，而不是 "Zyyy" (一般) 。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-157">The script determination is based on the script values published by the Unicode Consortium in <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt>, except that the unassigned characters have the value "Zzzz" (UNASSIGNED) instead of "Zyyy" (COMMON).</span></span>

<span data-ttu-id="b6f2a-158">以下是此函式行為的一些範例：</span><span class="sxs-lookup"><span data-stu-id="b6f2a-158">Here are some examples of the behavior of this function:</span></span>



<span data-ttu-id="b6f2a-159">輸入字串</span><span class="sxs-lookup"><span data-stu-id="b6f2a-159">Input string</span></span>

<span data-ttu-id="b6f2a-160">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b6f2a-160">*dwFlags*</span></span>

<span data-ttu-id="b6f2a-161">*lpScripts*</span><span class="sxs-lookup"><span data-stu-id="b6f2a-161">*lpScripts*</span></span>

<span data-ttu-id="b6f2a-162">指令碼</span><span class="sxs-lookup"><span data-stu-id="b6f2a-162">Scripts</span></span>

<span data-ttu-id="b6f2a-163">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b6f2a-163">Microsoft.com</span></span>

<span data-ttu-id="b6f2a-164">0</span><span class="sxs-lookup"><span data-stu-id="b6f2a-164">0</span></span>

<span data-ttu-id="b6f2a-165">Latn;</span><span class="sxs-lookup"><span data-stu-id="b6f2a-165">Latn;</span></span>

<span data-ttu-id="b6f2a-166">拉丁文</span><span class="sxs-lookup"><span data-stu-id="b6f2a-166">Latin</span></span>

<span data-ttu-id="b6f2a-167">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b6f2a-167">Microsoft.com</span></span>

<span data-ttu-id="b6f2a-168">GSS \_ 允許 \_ 繼承 \_ 通用</span><span class="sxs-lookup"><span data-stu-id="b6f2a-168">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="b6f2a-169">Latn;Zyyy;</span><span class="sxs-lookup"><span data-stu-id="b6f2a-169">Latn;Zyyy;</span></span>

<span data-ttu-id="b6f2a-170">拉丁 + 通用</span><span class="sxs-lookup"><span data-stu-id="b6f2a-170">Latin + Common</span></span>

<span data-ttu-id="b6f2a-171">$ {ROWSPAN2} $Ni ño $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6f2a-171">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="b6f2a-172">004E 0069 0241 006F</span><span class="sxs-lookup"><span data-stu-id="b6f2a-172">004E 0069 0241 006F</span></span>

<span data-ttu-id="b6f2a-173">$ {ROWSPAN2} $GSS \_ 允許 \_ 繼承的 \_ 通用 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6f2a-173">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="b6f2a-174">$ {ROWSPAN2} $Latn; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6f2a-174">${ROWSPAN2}$Latn;${REMOVE}$</span></span>  

<span data-ttu-id="b6f2a-175">$ {ROWSPAN2} $Latin $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6f2a-175">${ROWSPAN2}$Latin${REMOVE}$</span></span>  

<span data-ttu-id="b6f2a-176">使用具有波狀符號的拉丁小寫字母 N</span><span class="sxs-lookup"><span data-stu-id="b6f2a-176">Uses LATIN SMALL LETTER N WITH TILDE</span></span>

<span data-ttu-id="b6f2a-177">$ {ROWSPAN2} $Ni ño $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6f2a-177">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="b6f2a-178">004E 0069 006E 0303 006F</span><span class="sxs-lookup"><span data-stu-id="b6f2a-178">004E 0069 006E 0303 006F</span></span>

<span data-ttu-id="b6f2a-179">$ {ROWSPAN2} $GSS \_ 允許 \_ 繼承的 \_ 通用 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6f2a-179">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="b6f2a-180">$ {ROWSPAN2} $Latn;Qaii; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6f2a-180">${ROWSPAN2}$Latn;Qaii;${REMOVE}$</span></span>  

<span data-ttu-id="b6f2a-181">$ {ROWSPAN2} $Latin + 繼承 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6f2a-181">${ROWSPAN2}$Latin + Inherited${REMOVE}$</span></span>  

<span data-ttu-id="b6f2a-182">使用組合波狀符號</span><span class="sxs-lookup"><span data-stu-id="b6f2a-182">Uses COMBINING TILDE</span></span>

<span data-ttu-id="b6f2a-183">$ {ROWSPAN2} $Sp ооf $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6f2a-183">${ROWSPAN2}$Spооf${REMOVE}$</span></span>  

<span data-ttu-id="b6f2a-184">0053 0070 043e 043e 0066</span><span class="sxs-lookup"><span data-stu-id="b6f2a-184">0053 0070 043e 043e 0066</span></span>

<span data-ttu-id="b6f2a-185">$ {ROWSPAN2} $ 0 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6f2a-185">${ROWSPAN2}$0${REMOVE}$</span></span>  

<span data-ttu-id="b6f2a-186">$ {ROWSPAN2} $Latn;Cyrl; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6f2a-186">${ROWSPAN2}$Latn;Cyrl;${REMOVE}$</span></span>  

<span data-ttu-id="b6f2a-187">$ {ROWSPAN2} $Latin + 斯拉夫 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b6f2a-187">${ROWSPAN2}$Latin + Cyrillic${REMOVE}$</span></span>  

<span data-ttu-id="b6f2a-188">使用斯拉夫小寫字母 O</span><span class="sxs-lookup"><span data-stu-id="b6f2a-188">Uses CYRILLIC SMALL LETTER O</span></span>

<span data-ttu-id="b6f2a-189"></span><span class="sxs-lookup"><span data-stu-id="b6f2a-189"></span></span>

<span data-ttu-id="b6f2a-190">U + f000</span><span class="sxs-lookup"><span data-stu-id="b6f2a-190">U+f000</span></span>

<span data-ttu-id="b6f2a-191">0</span><span class="sxs-lookup"><span data-stu-id="b6f2a-191">0</span></span>

<span data-ttu-id="b6f2a-192">Zzzz</span><span class="sxs-lookup"><span data-stu-id="b6f2a-192">Zzzz;</span></span>

<span data-ttu-id="b6f2a-193">未指定</span><span class="sxs-lookup"><span data-stu-id="b6f2a-193">Unassigned</span></span>

<span data-ttu-id="b6f2a-194"></span><span class="sxs-lookup"><span data-stu-id="b6f2a-194"></span></span>

<span data-ttu-id="b6f2a-195">U + f000</span><span class="sxs-lookup"><span data-stu-id="b6f2a-195">U+f000</span></span>

<span data-ttu-id="b6f2a-196">GSS \_ 允許 \_ 繼承 \_ 通用</span><span class="sxs-lookup"><span data-stu-id="b6f2a-196">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="b6f2a-197">Zzzz</span><span class="sxs-lookup"><span data-stu-id="b6f2a-197">Zzzz;</span></span>

<span data-ttu-id="b6f2a-198">未指定</span><span class="sxs-lookup"><span data-stu-id="b6f2a-198">Unassigned</span></span>



 

<span data-ttu-id="b6f2a-199">必要的標頭檔和 DLL 是「 [Microsoft 國際化功能變數名稱 (IDN) 緩和 api](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) 」下載的一部分，可從 [MSDN 下載中心](https://www.microsoft.com/?ref=go)取得。</span><span class="sxs-lookup"><span data-stu-id="b6f2a-199">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6f2a-200">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6f2a-200">Requirements</span></span>



| <span data-ttu-id="b6f2a-201">需求</span><span class="sxs-lookup"><span data-stu-id="b6f2a-201">Requirement</span></span> | <span data-ttu-id="b6f2a-202">值</span><span class="sxs-lookup"><span data-stu-id="b6f2a-202">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f2a-203">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6f2a-203">Minimum supported client</span></span><br/> | <span data-ttu-id="b6f2a-204">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6f2a-204">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="b6f2a-205">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6f2a-205">Minimum supported server</span></span><br/> | <span data-ttu-id="b6f2a-206">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6f2a-206">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="b6f2a-207">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b6f2a-207">Redistributable</span></span><br/>          | <span data-ttu-id="b6f2a-208">Microsoft 國際化功能變數名稱 (IDN) Windows XP (SP2 或更新版本) 、Windows Server 2003 (SP1 或更新版本) 或 Windows Vista 上的緩和 Api</span><span class="sxs-lookup"><span data-stu-id="b6f2a-208">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="b6f2a-209">標頭</span><span class="sxs-lookup"><span data-stu-id="b6f2a-209">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6f2a-210"><dt>Idndl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6f2a-210"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="b6f2a-211">DLL</span><span class="sxs-lookup"><span data-stu-id="b6f2a-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6f2a-212"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6f2a-212"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="b6f2a-213">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6f2a-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6f2a-214">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="b6f2a-214">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="b6f2a-215">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="b6f2a-215">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="b6f2a-216">處理國際化功能變數名稱 (IDNs) </span><span class="sxs-lookup"><span data-stu-id="b6f2a-216">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="b6f2a-217">**DownlevelGetLocaleScripts**</span><span class="sxs-lookup"><span data-stu-id="b6f2a-217">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="b6f2a-218">**DownlevelVerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="b6f2a-218">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="b6f2a-219">**GetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="b6f2a-219">**GetStringScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 
