---
description: 提供指定之地區設定的腳本清單。
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: 'DownlevelGetLocaleScripts 函式 (Idndl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: f636ab426cd4d50878df93e3e30d69de54d60ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194550"
---
# <a name="downlevelgetlocalescripts-function"></a><span data-ttu-id="8001c-103">DownlevelGetLocaleScripts 函式</span><span class="sxs-lookup"><span data-stu-id="8001c-103">DownlevelGetLocaleScripts function</span></span>

<span data-ttu-id="8001c-104">提供指定之地區設定的腳本清單。</span><span class="sxs-lookup"><span data-stu-id="8001c-104">Provides a list of scripts for the specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="8001c-105">只有在 Windows Vista 之前的作業系統上執行的應用程式，才會使用此函式。</span><span class="sxs-lookup"><span data-stu-id="8001c-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="8001c-106">其用途需要下載套件。</span><span class="sxs-lookup"><span data-stu-id="8001c-106">Its use requires the download package.</span></span> <span data-ttu-id="8001c-107">只有在 Windows Vista 和更新版本上執行的應用程式，應該呼叫 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ，並將 *LCType* 設定為 [地區設定 \_ SSCRIPTS](locale-sscripts.md)。</span><span class="sxs-lookup"><span data-stu-id="8001c-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SSCRIPTS](locale-sscripts.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8001c-108">語法</span><span class="sxs-lookup"><span data-stu-id="8001c-108">Syntax</span></span>


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="8001c-109">參數</span><span class="sxs-lookup"><span data-stu-id="8001c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8001c-110">*lpLocaleName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8001c-110">*lpLocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8001c-111">以 null 結束之地區設定 [名稱](locale-names.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="8001c-111">Pointer to a null-terminated [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="8001c-112">*lpScripts* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8001c-112">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8001c-113">緩衝區的指標，此函式會使用 [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html)中使用的4個字元標記法，來抓取表示腳本清單的以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="8001c-113">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="8001c-114">每個腳本名稱都是由四個拉丁字元所組成，而且名稱會依字母順序抓取。</span><span class="sxs-lookup"><span data-stu-id="8001c-114">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="8001c-115">其中每個專案（包括最後一個）後面都會加上分號。</span><span class="sxs-lookup"><span data-stu-id="8001c-115">Each of them, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="8001c-116">或者，如果 *cchScripts* 設為0，則此參數可以包含 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8001c-116">Alternatively, this parameter can contain **NULL** if *cchScripts* is set to 0.</span></span> <span data-ttu-id="8001c-117">在此情況下，函數會傳回腳本緩衝區所需的大小。</span><span class="sxs-lookup"><span data-stu-id="8001c-117">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8001c-118">*cchScripts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8001c-118">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8001c-119">*LpScripts* 所指出的腳本緩衝區大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="8001c-119">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="8001c-120">或者，應用程式可以將此參數設定為0。</span><span class="sxs-lookup"><span data-stu-id="8001c-120">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="8001c-121">在此情況下，此函式會在 *lpScripts* 中抓取 **Null** ，並傳回腳本緩衝區所需的大小。</span><span class="sxs-lookup"><span data-stu-id="8001c-121">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8001c-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="8001c-122">Return value</span></span>

<span data-ttu-id="8001c-123">傳回腳本緩衝區中取出的字元數，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="8001c-123">Returns the number of characters retrieved in the script buffer, including the terminating null character.</span></span> <span data-ttu-id="8001c-124">如果函式成功，且 *cchScripts* 的值為0，則傳回值為腳本緩衝區所需的大小（以字元為單位，包括結束的 null 字元）。</span><span class="sxs-lookup"><span data-stu-id="8001c-124">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span>

<span data-ttu-id="8001c-125">如果不成功，則此函式會傳回0。</span><span class="sxs-lookup"><span data-stu-id="8001c-125">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="8001c-126">若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="8001c-126">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="8001c-127">錯誤 \_ BADDB。</span><span class="sxs-lookup"><span data-stu-id="8001c-127">ERROR\_BADDB.</span></span> <span data-ttu-id="8001c-128">函數無法存取資料。</span><span class="sxs-lookup"><span data-stu-id="8001c-128">The function could not access the data.</span></span> <span data-ttu-id="8001c-129">通常不會發生這種情況，通常表示安裝不良、磁片問題或類似。</span><span class="sxs-lookup"><span data-stu-id="8001c-129">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="8001c-130">\_緩衝區不足 \_ 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8001c-130">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="8001c-131">提供的緩衝區大小不夠大，或未正確設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8001c-131">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="8001c-132">錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="8001c-132">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="8001c-133">任何參數值都無效。</span><span class="sxs-lookup"><span data-stu-id="8001c-133">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="8001c-134">備註</span><span class="sxs-lookup"><span data-stu-id="8001c-134">Remarks</span></span>

<span data-ttu-id="8001c-135">這項功能可作為策略的一部分，以降低與國際化功能變數名稱相關的安全性問題 [ (IDNs) ](handling-internationalized-domain-names--idns.md)。</span><span class="sxs-lookup"><span data-stu-id="8001c-135">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="8001c-136">以下是此函式之輸入和輸出的一些範例，假設有足夠的緩衝區大小：</span><span class="sxs-lookup"><span data-stu-id="8001c-136">Here are some examples of inputs and outputs for this function, assuming a sufficient buffer size:</span></span>



| <span data-ttu-id="8001c-137">Locale</span><span class="sxs-lookup"><span data-stu-id="8001c-137">Locale</span></span>                  | <span data-ttu-id="8001c-138">*lpLocaleName*</span><span class="sxs-lookup"><span data-stu-id="8001c-138">*lpLocaleName*</span></span> | <span data-ttu-id="8001c-139">*lpScripts*</span><span class="sxs-lookup"><span data-stu-id="8001c-139">*lpScripts*</span></span>     |
|-------------------------|----------------|-----------------|
| <span data-ttu-id="8001c-140">英文 (美國)</span><span class="sxs-lookup"><span data-stu-id="8001c-140">English (United States)</span></span> | <span data-ttu-id="8001c-141">zh-TW</span><span class="sxs-lookup"><span data-stu-id="8001c-141">en-US</span></span>          | <span data-ttu-id="8001c-142">Latn;</span><span class="sxs-lookup"><span data-stu-id="8001c-142">Latn;</span></span>           |
| <span data-ttu-id="8001c-143">印度文 (印度)</span><span class="sxs-lookup"><span data-stu-id="8001c-143">Hindi (India)</span></span>           | <span data-ttu-id="8001c-144">hi-IN</span><span class="sxs-lookup"><span data-stu-id="8001c-144">hi-IN</span></span>          | <span data-ttu-id="8001c-145">Deva;</span><span class="sxs-lookup"><span data-stu-id="8001c-145">Deva;</span></span>           |
| <span data-ttu-id="8001c-146">日文 (日本)</span><span class="sxs-lookup"><span data-stu-id="8001c-146">Japanese (Japan)</span></span>        | <span data-ttu-id="8001c-147">ja-JP</span><span class="sxs-lookup"><span data-stu-id="8001c-147">ja-JP</span></span>          | <span data-ttu-id="8001c-148">Hani;Hira;區分</span><span class="sxs-lookup"><span data-stu-id="8001c-148">Hani;Hira;Kana;</span></span> |



 

<span data-ttu-id="8001c-149">此清單不包含拉丁腳本，除非它是用於地區設定之書寫系統的必要部分。</span><span class="sxs-lookup"><span data-stu-id="8001c-149">The list does not contain the Latin script unless it is an essential part of the writing system used for a locale.</span></span> <span data-ttu-id="8001c-150">但是，拉丁字元通常用於不是原生的地區設定內容中，而不是外部業務名稱。</span><span class="sxs-lookup"><span data-stu-id="8001c-150">However, Latin characters are often used in the context of locales for which they are not native, as for a foreign business name.</span></span> <span data-ttu-id="8001c-151">在上述範例中，針對印度文的印度文，唯一抓取的腳本是「Deva」 (適用于梵文) ，不過拉丁字元也可以出現在印度文文字中。</span><span class="sxs-lookup"><span data-stu-id="8001c-151">In the example above for Hindi in India, the only script retrieved is "Deva" (for Devanagari), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="8001c-152">[**DownlevelVerifyScripts**](downlevelverifyscripts.md)函式具有特殊旗標，可解決該情況。</span><span class="sxs-lookup"><span data-stu-id="8001c-152">The [**DownlevelVerifyScripts**](downlevelverifyscripts.md) function has a special flag to address that case.</span></span>

<span data-ttu-id="8001c-153">必要的標頭檔和 DLL 是「 [Microsoft 國際化功能變數名稱 (IDN) 緩和 api](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) 」下載的一部分，可從 [MSDN 下載中心](https://www.microsoft.com/?ref=go)取得。</span><span class="sxs-lookup"><span data-stu-id="8001c-153">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="8001c-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="8001c-154">Requirements</span></span>



| <span data-ttu-id="8001c-155">需求</span><span class="sxs-lookup"><span data-stu-id="8001c-155">Requirement</span></span> | <span data-ttu-id="8001c-156">值</span><span class="sxs-lookup"><span data-stu-id="8001c-156">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8001c-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8001c-157">Minimum supported client</span></span><br/> | <span data-ttu-id="8001c-158">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8001c-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="8001c-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8001c-159">Minimum supported server</span></span><br/> | <span data-ttu-id="8001c-160">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8001c-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="8001c-161">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8001c-161">Redistributable</span></span><br/>          | <span data-ttu-id="8001c-162">Microsoft 國際化功能變數名稱 (IDN) Windows XP (SP2 或更新版本) 、Windows Server 2003 (SP1 或更新版本) 或 Windows Vista 上的緩和 Api</span><span class="sxs-lookup"><span data-stu-id="8001c-162">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="8001c-163">標頭</span><span class="sxs-lookup"><span data-stu-id="8001c-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="8001c-164"><dt>Idndl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8001c-164"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="8001c-165">DLL</span><span class="sxs-lookup"><span data-stu-id="8001c-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8001c-166"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8001c-166"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="8001c-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8001c-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8001c-168">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="8001c-168">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="8001c-169">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="8001c-169">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="8001c-170">處理國際化功能變數名稱 (IDNs) </span><span class="sxs-lookup"><span data-stu-id="8001c-170">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="8001c-171">**DownlevelGetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="8001c-171">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="8001c-172">**DownlevelVerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="8001c-172">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="8001c-173">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="8001c-173">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
