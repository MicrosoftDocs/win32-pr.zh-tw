---
description: 本主題說明如何在您的應用程式中 (IDNs) 來使用國際化功能變數名稱。
ms.assetid: e0ca356e-f8c1-4845-ae1e-ce2ae8987515
title: '處理國際化功能變數名稱 (IDNs) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95e853f0ea3f62fc3e5ee848431417cc031eaa5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193691"
---
# <a name="handling-internationalized-domain-names-idns"></a><span data-ttu-id="fb6bb-103">處理國際化功能變數名稱 (IDNs) </span><span class="sxs-lookup"><span data-stu-id="fb6bb-103">Handling Internationalized Domain Names (IDNs)</span></span>

<span data-ttu-id="fb6bb-104">本主題說明如何在您的應用程式中 (IDNs) 來使用國際化功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-104">This topic describes how you can work with internationalized domain names (IDNs) in your applications.</span></span> <span data-ttu-id="fb6bb-105">IDNs 是由網路工作群組 [RFC 3490 所指定：在應用程式中將功能變數名稱國際化 (IDNA) ](http://www.faqs.org/rfcs/rfc3490.html)。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-105">IDNs are specified by Network Working Group [RFC 3490: Internationalizing Domain Names in Applications (IDNA)](http://www.faqs.org/rfcs/rfc3490.html).</span></span> <span data-ttu-id="fb6bb-106">在此草稿標準之前，IDNs 限制為不含變音符號的拉丁字元。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-106">Prior to this draft standard, IDNs were limited to Latin characters without diacritics.</span></span> <span data-ttu-id="fb6bb-107">IDNA 可讓 IDNs 包含含有發音符號的拉丁字元，以及來自非拉丁腳本的字元，例如斯拉夫文、阿拉伯文和中文。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-107">IDNA allows IDNs to include Latin characters with diacritics, along with characters from non-Latin scripts, such as Cyrillic, Arabic, and Chinese.</span></span> <span data-ttu-id="fb6bb-108">標準也會建立將 IDNs 對應至僅限 ASCII 功能變數名稱的規則。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-108">The standard also establishes rules for mapping IDNs to ASCII-only domain names.</span></span> <span data-ttu-id="fb6bb-109">因此，IDNA 問題可以在用戶端上處理，而不需要任何功能變數名稱伺服器 (DNS) 變更。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-109">Thus, IDNA issues can be handled on the client side, without requiring any domain name server (DNS) changes.</span></span>

> [!Caution]  
> <span data-ttu-id="fb6bb-110">RFC 3490 引進了許多與使用 IDNs 相關的安全性問題。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-110">RFC 3490 introduces a number of security issues related to the use of IDNs.</span></span> <span data-ttu-id="fb6bb-111">如需詳細資訊，請參閱安全性考慮的相關章節 [：國際功能](security-considerations--international-features.md)。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-111">For more information see the related section of [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="fb6bb-112">IDNA 目前是以 Unicode 3.2 為基礎。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-112">IDNA is currently based on Unicode 3.2.</span></span>

 

## <a name="nls-api-functions-for-handling-idns"></a><span data-ttu-id="fb6bb-113">處理 IDNs 的 NLS API 函式</span><span class="sxs-lookup"><span data-stu-id="fb6bb-113">NLS API Functions for Handling IDNs</span></span>

<span data-ttu-id="fb6bb-114">NLS 包含下列轉換函式，可讓您的應用程式用來將 IDN 轉換成不同的標記法。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-114">NLS includes the following conversion functions that your application can use to convert an IDN to different representations.</span></span> <span data-ttu-id="fb6bb-115">如需使用這些函數的範例，請參閱 [NLS：國際化功能變數名稱 (IDN) 轉換範例](nls--internationalized-domain-name--idn--conversion-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-115">For an example of the use of these functions, see [NLS: Internationalized Domain Name (IDN) Conversion Sample](nls--internationalized-domain-name--idn--conversion-sample.md).</span></span>

-   <span data-ttu-id="fb6bb-116">[**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii)。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-116">[**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii).</span></span> <span data-ttu-id="fb6bb-117">將 IDN 轉換成 Punycode。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-117">Converts an IDN to Punycode.</span></span>
-   <span data-ttu-id="fb6bb-118">[**IdnToNameprepUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntonameprepunicode)。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-118">[**IdnToNameprepUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntonameprepunicode).</span></span> <span data-ttu-id="fb6bb-119">執行將 IDN 轉換成 ASCII 名稱的 NamePrep 部分。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-119">Performs the NamePrep portion of the conversion of an IDN to an ASCII name.</span></span> <span data-ttu-id="fb6bb-120">此函數會建立字串的標準 Unicode 標記法。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-120">This function creates a canonical Unicode representation of a string.</span></span>
-   <span data-ttu-id="fb6bb-121">[**IdnToUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntounicode)。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-121">[**IdnToUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntounicode).</span></span> <span data-ttu-id="fb6bb-122">將 Punycode 字串轉換為一般 UTF-16 字串。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-122">Converts a Punycode string to a normal UTF-16 string.</span></span>

<span data-ttu-id="fb6bb-123">NLS 也會定義數個 API 函式，可用來減輕一些 IDN 技術所呈現的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-123">NLS also defines several API functions that can be used to mitigate some of the security risks presented by the IDN technology.</span></span> <span data-ttu-id="fb6bb-124">在 Windows Vista 和更新版本上，下列函式是用來驗證指定的 IDN 中的字元是否完全取自與特定地區設定或地區設定相關聯的腳本。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-124">On Windows Vista and later, the following functions are used to verify that the characters in a given IDN are drawn entirely from the scripts associated with a particular locale or locales.</span></span> <span data-ttu-id="fb6bb-125">如需使用這些函數的範例，請參閱 [NLS：國際化功能變數名稱 (IDN) 緩和範例](nls--internationalized-domain-name--idn--mitigation-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-125">For an example of the use of these functions, see [NLS: Internationalized Domain Name (IDN) Mitigation Sample](nls--internationalized-domain-name--idn--mitigation-sample.md).</span></span>

-   <span data-ttu-id="fb6bb-126">[**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-126">[**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span></span> <span data-ttu-id="fb6bb-127">提供特定字串中所使用的腳本清單。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-127">Provides a list of scripts used in a particular string.</span></span>
-   <span data-ttu-id="fb6bb-128">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)、 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-128">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa), [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex).</span></span> <span data-ttu-id="fb6bb-129">取出地區設定資訊。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-129">Retrieve locale information.</span></span> <span data-ttu-id="fb6bb-130">使用 *LCType* 設定為 [LOCALE \_ SSCRIPTS](locale-sscripts.md) 的函式，可提供一般用於特定地區設定的腳本清單。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-130">Using the functions with *LCType* set to [LOCALE\_SSCRIPTS](locale-sscripts.md) provides a list of scripts normally used for a particular locale.</span></span>
-   <span data-ttu-id="fb6bb-131">[**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-131">[**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span></span> <span data-ttu-id="fb6bb-132">比較腳本清單。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-132">Compares lists of scripts.</span></span> <span data-ttu-id="fb6bb-133">若要針對多個地區設定進行驗證，應用程式可以對 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 或 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 和 [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)進行多個呼叫。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-133">To verify against multiple locales, the application can make multiple calls to [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) and [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span></span>

<span data-ttu-id="fb6bb-134">針對在 Windows XP 與 Windows Server 2003 上執行的應用程式， [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)、 [**DownlevelGetStringScripts**](downlevelgetstringscripts.md)和 [**DownlevelVerifyScripts**](downlevelverifyscripts.md) 等函式對上述的函式扮演類似的角色，以降低安全性風險。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-134">For applications that run on Windows XP and Windows Server 2003, the functions [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md), [**DownlevelGetStringScripts**](downlevelgetstringscripts.md), and [**DownlevelVerifyScripts**](downlevelverifyscripts.md) play a similar role to the functions listed above in mitigating security risk.</span></span> <span data-ttu-id="fb6bb-135">[MSDN 下載中心](https://www.microsoft.com/?ref=go)提供「 [Microsoft 國際化功能變數名稱 (IDN) 緩和 api](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) 」下載。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-135">The ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download is available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="handle-unicode-strings"></a><span data-ttu-id="fb6bb-136">處理 Unicode 字串</span><span class="sxs-lookup"><span data-stu-id="fb6bb-136">Handle Unicode Strings</span></span>

<span data-ttu-id="fb6bb-137">IDNA 支援將 Unicode 字串轉換成合法的主機名稱標籤，但包含某些禁止字元的字串除外，例如控制字元、私用區域的字元 (PUA) 和 like。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-137">IDNA supports the transformation of Unicode strings into legitimate host name labels, with the exception of strings containing certain prohibited characters, such as control characters, characters from the private use area (PUA), and the like.</span></span> <span data-ttu-id="fb6bb-138">您的應用程式可以使用 IDN \_ use \_ STD3 \_ ASCII 規則旗標搭配 \_ 數個 NLS 轉換函式，來強制函式在遇到字母、數位或連字號-減號 (-) 字元以外的 ascii 字元，或者字串開頭或結尾為連字號-減號字元時失敗。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-138">Your application can use the IDN\_USE\_STD3\_ASCII\_RULES flag with several NLS conversion functions to force the functions to fail if they encounter ASCII characters other than letters, numbers, or the hyphen-minus (-) character, or if a string begins or ends with the hyphen-minus character.</span></span> <span data-ttu-id="fb6bb-139">這些字元一律禁止在功能變數名稱中使用，並在草稿標準中保持禁止。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-139">These characters have always been prohibited from use in domain names, and remain prohibited in the draft standard.</span></span>

## <a name="handle-unassigned-code-points"></a><span data-ttu-id="fb6bb-140">處理未指派的程式碼點</span><span class="sxs-lookup"><span data-stu-id="fb6bb-140">Handle Unassigned Code Points</span></span>

<span data-ttu-id="fb6bb-141">IDNs 不能包含未指派的程式碼點。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-141">IDNs cannot contain unassigned code points.</span></span> <span data-ttu-id="fb6bb-142">因此，未與 Unicode 3.2 ( 「指派」 ) 字元相關聯的程式碼點也不會定義 IDN 對應，即使在某些轉換函式中，[IDN \_ 允許 \_ 未指派] 旗標可讓它們對應至 Punycode 也一樣。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-142">Therefore, code points that are not associated with a character ("assigned") as of Unicode 3.2 do not have defined IDN mappings, even though the IDN\_ALLOW\_UNASSIGNED flag in certain conversion functions allows them to be mapped to Punycode.</span></span> <span data-ttu-id="fb6bb-143">您可以在 [RFC 3454](http://www.faqs.org/rfcs/rfc3454.html)中尋找未指派的程式碼點清單。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-143">You can find a list of unassigned code points in [RFC 3454](http://www.faqs.org/rfcs/rfc3454.html).</span></span>

> [!Caution]  
> <span data-ttu-id="fb6bb-144">如果您的應用程式將未指派的程式碼點編碼為 Punycode，則產生的功能變數名稱應該是不合法的。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-144">If your application encodes unassigned code points as Punycode, the resulting domain names should be illegal.</span></span> <span data-ttu-id="fb6bb-145">如果較新版本的 IDNA 讓這些名稱合法，或如果應用程式篩選掉不合法的字元來嘗試建立合法的功能變數名稱，安全性可能會受到危害。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-145">Security can be compromised if a later version of IDNA makes these names legal or if the application filters out the illegal characters to try to create a legal domain name.</span></span>

 

<span data-ttu-id="fb6bb-146">通訊協定識別碼和命名實體中使用的預存字串中不允許未指派的程式碼點，例如數位憑證和 DNS 功能變數名稱部分中的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-146">Unassigned code points are not allowed in the stored strings used in protocol identifiers and named entities, such as names in digital certificates and DNS domain name parts.</span></span> <span data-ttu-id="fb6bb-147">不過，查詢字串中允許使用程式碼點，例如，用來比對預存識別碼的使用者輸入的數位憑證授權單位單位和 DNS 查閱名稱。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-147">However, the code points are allowed in query strings, for example, user-entered names for digital certificate authorities and DNS lookups, which are used to match against stored identifiers.</span></span>

> [!Caution]  
> <span data-ttu-id="fb6bb-148">雖然查詢字串可以使用未指派的程式碼點，但您不應該在應用程式中使用它們。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-148">Although query strings can use unassigned code points, you should not use them in your applications.</span></span> <span data-ttu-id="fb6bb-149">即使是使用者提供的查詢字串，也會帶來「詐騙」攻擊的風險。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-149">Even a user-supplied query string presents a risk of a "spoofing" attack.</span></span> <span data-ttu-id="fb6bb-150">在這種類型的攻擊中，不道德的主機網站會將使用者從想要存取的網站，重設為另一個可能提供機密資訊給協力廠商的網站。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-150">In this type of attack, the unscrupulous host site reroutes users from the site they intend to access to another site that might provide sensitive information to a third party.</span></span> <span data-ttu-id="fb6bb-151">例如，從內送電子郵件複製字串，可能會出現與在瀏覽器中按一下連結相同的風險。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-151">For example, copying a string from an incoming e-mail can present the same risks as clicking on a link in a browser.</span></span>

 

## <a name="convert-domain-names-to-ascii-names"></a><span data-ttu-id="fb6bb-152">將功能變數名稱轉換成 ASCII 名稱</span><span class="sxs-lookup"><span data-stu-id="fb6bb-152">Convert Domain Names to ASCII Names</span></span>

<span data-ttu-id="fb6bb-153">您的應用程式可以使用 [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii) 函數和某些緩和函式，將 IDNs 轉換為 ASCII。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-153">Your application can use the [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii) function and certain mitigation functions to convert IDNs to ASCII.</span></span>

> [!Caution]  
> <span data-ttu-id="fb6bb-154">因為具有非常不同之二進位表示的字串可以與相同的比較，所以此函式可能會引發特定的安全性考慮。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-154">Because strings with very different binary representations can compare as identical, this function can raise certain security concerns.</span></span> <span data-ttu-id="fb6bb-155">如需詳細資訊，請參閱安全性考慮中的比較函數討論 [：國際化功能](security-considerations--international-features.md)。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-155">For more information, see the discussion of comparison functions in [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="examples"></a><span data-ttu-id="fb6bb-156">範例</span><span class="sxs-lookup"><span data-stu-id="fb6bb-156">Examples</span></span>

<span data-ttu-id="fb6bb-157">[NLS：國際化功能變數名稱 (idn) 轉換範例](nls--internationalized-domain-name--idn--conversion-sample.md) 示範如何使用 idn 轉換函數。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-157">[NLS: Internationalized Domain Name (IDN) Conversion Sample](nls--internationalized-domain-name--idn--conversion-sample.md) demonstrates the use of the IDN conversion functions.</span></span> <span data-ttu-id="fb6bb-158">[NLS：國際化功能變數名稱 (IDN) 緩和範例](nls--internationalized-domain-name--idn--mitigation-sample.md) 示範如何使用 idn 緩和功能。</span><span class="sxs-lookup"><span data-stu-id="fb6bb-158">[NLS: Internationalized Domain Name (IDN) Mitigation Sample](nls--internationalized-domain-name--idn--mitigation-sample.md) demonstrates the use of the IDN mitigation functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb6bb-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="fb6bb-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb6bb-160">使用國家語言支援</span><span class="sxs-lookup"><span data-stu-id="fb6bb-160">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="fb6bb-161">安全性考慮：國際功能</span><span class="sxs-lookup"><span data-stu-id="fb6bb-161">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> </dl>

 

 



