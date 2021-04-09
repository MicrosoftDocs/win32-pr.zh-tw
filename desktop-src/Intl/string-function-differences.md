---
description: 本主題說明用來處理 Unicode 和字元集資訊的字串函數之間的差異。 這些函式都有 Unicode 和 Windows 字碼頁的實作為支援 Unicode 和 Windows 字碼頁參數。
ms.assetid: 52a15957-b44b-49ba-b915-e5c8e003a7e6
title: 字串函數差異
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c940aa8be1603f7958fb1993cc521ca7b1ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943848"
---
# <a name="string-function-differences"></a><span data-ttu-id="3d3c5-104">字串函數差異</span><span class="sxs-lookup"><span data-stu-id="3d3c5-104">String Function Differences</span></span>

<span data-ttu-id="3d3c5-105">本主題說明用來處理 Unicode 和字元集資訊的字串函數之間的差異。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-105">This topic describes differences among string functions used in handling Unicode and character set information.</span></span> <span data-ttu-id="3d3c5-106">這些函式都有 [unicode](unicode.md) 和 [windows 字碼頁](code-pages.md) 的實作為支援 unicode 和 windows 字碼頁參數。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-106">These functions have both [Unicode](unicode.md) and [Windows code page](code-pages.md) implementations to support Unicode and Windows code page parameters.</span></span>

<span data-ttu-id="3d3c5-107">下列字串函數不需要特殊批註。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-107">The following string functions do not require special comment.</span></span> <span data-ttu-id="3d3c5-108">其 Unicode 和 Windows 字碼頁的執行方式均相同。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-108">Their Unicode and Windows code page implementations work identically.</span></span>

-   [<span data-ttu-id="3d3c5-109">**CharNext**</span><span class="sxs-lookup"><span data-stu-id="3d3c5-109">**CharNext**</span></span>](/windows/win32/api/winuser/nf-winuser-charnexta)
-   [<span data-ttu-id="3d3c5-110">**CharPrev**</span><span class="sxs-lookup"><span data-stu-id="3d3c5-110">**CharPrev**</span></span>](/windows/win32/api/winuser/nf-winuser-charpreva)
-   <span data-ttu-id="3d3c5-111">[**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata)、 [ **StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)</span><span class="sxs-lookup"><span data-stu-id="3d3c5-111">[**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)</span></span>
-   <span data-ttu-id="3d3c5-112">[**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya)、 [ **StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)</span><span class="sxs-lookup"><span data-stu-id="3d3c5-112">[**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)</span></span>
-   <span data-ttu-id="3d3c5-113">[**StrCbLength**](/windows/win32/api/strsafe/nf-strsafe-stringcblengtha)、 [ **StrCchLength**](/windows/win32/api/strsafe/nf-strsafe-stringcchlengtha)</span><span class="sxs-lookup"><span data-stu-id="3d3c5-113">[**StrCbLength**](/windows/win32/api/strsafe/nf-strsafe-stringcblengtha), [**StrCchLength**](/windows/win32/api/strsafe/nf-strsafe-stringcchlengtha)</span></span>

<span data-ttu-id="3d3c5-114">其中一個字串長度函式所抓取的長度值一律以一般字元寬度為依據：適用于 Windows 字碼頁的8位、Unicode 的16位。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-114">The length value retrieved by one of the string length functions is always based on normal character width: 8 bits for Windows code pages, 16 bits for Unicode.</span></span> <span data-ttu-id="3d3c5-115">此值通常稱為「字元計數」。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-115">This value is often referred to as a "count of characters."</span></span> <span data-ttu-id="3d3c5-116">因為使用 [雙位元組字元集](double-byte-character-sets.md) 的 Windows 字碼頁 (dbcs) 有一些全形字元實際上是以兩個連續的位元組來表示，所以此詞彙完全正確。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-116">This term is strictly correct because Windows code pages that use [double-byte character sets](double-byte-character-sets.md) (DBCSs) have some full-width characters that are actually represented by two consecutive bytes.</span></span> <span data-ttu-id="3d3c5-117">Unicode 中的 [代理](surrogates-and-supplementary-characters.md) 程式會發生類似的情況。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-117">A similar situation arises for [surrogates](surrogates-and-supplementary-characters.md) in Unicode.</span></span>

<span data-ttu-id="3d3c5-118">下列字串函式會區分目前線程的地區設定，這些函數衍生自使用者在主控台中選取的語言。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-118">The following string functions are sensitive to the locale of the current thread, derived from the language the user selects in the Control Panel.</span></span> <span data-ttu-id="3d3c5-119">[**Lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)和 [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)函式不會像 ANSI namesakes 一樣執行位元組比較，例如 [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp)。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-119">The [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) and [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) functions do not perform byte comparisons like their ANSI namesakes, for example, [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp).</span></span> <span data-ttu-id="3d3c5-120">相反地，它們會根據地區設定的規則來比較字串。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-120">Instead, they compare strings according to the rules of the locale.</span></span>

-   [<span data-ttu-id="3d3c5-121">**CharLower**</span><span class="sxs-lookup"><span data-stu-id="3d3c5-121">**CharLower**</span></span>](/windows/win32/api/winuser/nf-winuser-charlowera)
-   [<span data-ttu-id="3d3c5-122">**CharLowerBuff**</span><span class="sxs-lookup"><span data-stu-id="3d3c5-122">**CharLowerBuff**</span></span>](/windows/win32/api/winuser/nf-winuser-charlowerbuffa)
-   [<span data-ttu-id="3d3c5-123">**CharUpper**</span><span class="sxs-lookup"><span data-stu-id="3d3c5-123">**CharUpper**</span></span>](/windows/win32/api/winuser/nf-winuser-charuppera)
-   [<span data-ttu-id="3d3c5-124">**CharUpperBuff**</span><span class="sxs-lookup"><span data-stu-id="3d3c5-124">**CharUpperBuff**</span></span>](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
-   [<span data-ttu-id="3d3c5-125">**lstrcmp**</span><span class="sxs-lookup"><span data-stu-id="3d3c5-125">**lstrcmp**</span></span>](/windows/win32/api/winbase/nf-winbase-lstrcmpa)
-   [<span data-ttu-id="3d3c5-126">**lstrcmpi**</span><span class="sxs-lookup"><span data-stu-id="3d3c5-126">**lstrcmpi**</span></span>](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

<span data-ttu-id="3d3c5-127">下列函式會根據所使用的版本，在 OEM 字元集和目前的 Windows 字碼頁或 Unicode 之間進行轉換：</span><span class="sxs-lookup"><span data-stu-id="3d3c5-127">The following functions convert between the OEM character set and either the current Windows code page or Unicode, depending on which version is used:</span></span>

-   [<span data-ttu-id="3d3c5-128">**CharToOem**</span><span class="sxs-lookup"><span data-stu-id="3d3c5-128">**CharToOem**</span></span>](/windows/win32/api/winuser/nf-winuser-chartooema)
-   [<span data-ttu-id="3d3c5-129">**CharToOemBuff**</span><span class="sxs-lookup"><span data-stu-id="3d3c5-129">**CharToOemBuff**</span></span>](/windows/win32/api/winuser/nf-winuser-chartooembuffa)
-   [<span data-ttu-id="3d3c5-130">**OemToCharBuff**</span><span class="sxs-lookup"><span data-stu-id="3d3c5-130">**OemToCharBuff**</span></span>](/windows/win32/api/winuser/nf-winuser-oemtocharbuffa)

<span data-ttu-id="3d3c5-131">列印函式（例如 [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa)）支援 Unicode，方法是在其格式規格中提供下列新的和變更的資料類型。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-131">The print functions, for example, [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), support Unicode by providing the following new and changed data types in their format specifications.</span></span> <span data-ttu-id="3d3c5-132">這些格式規格會影響函數解讀對應輸入參數的方式。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-132">These format specifications affect the way the functions interpret the corresponding input parameter.</span></span>



| <span data-ttu-id="3d3c5-133">格式規格</span><span class="sxs-lookup"><span data-stu-id="3d3c5-133">Format specification</span></span> | <span data-ttu-id="3d3c5-134">Windows 字碼頁版本的資料類型</span><span class="sxs-lookup"><span data-stu-id="3d3c5-134">Data type for Windows code page version</span></span> | <span data-ttu-id="3d3c5-135">Unicode 版本的資料類型</span><span class="sxs-lookup"><span data-stu-id="3d3c5-135">Data type for Unicode version</span></span> |
|----------------------|-----------------------------------------|-------------------------------|
| <span data-ttu-id="3d3c5-136">c</span><span class="sxs-lookup"><span data-stu-id="3d3c5-136">c</span></span>                    | <span data-ttu-id="3d3c5-137">CHAR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-137">CHAR</span></span>                                    | <span data-ttu-id="3d3c5-138">WCHAR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-138">WCHAR</span></span>                         |
| <span data-ttu-id="3d3c5-139">C</span><span class="sxs-lookup"><span data-stu-id="3d3c5-139">C</span></span>                    | <span data-ttu-id="3d3c5-140">WCHAR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-140">WCHAR</span></span>                                   | <span data-ttu-id="3d3c5-141">CHAR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-141">CHAR</span></span>                          |
| <span data-ttu-id="3d3c5-142">hc、hC</span><span class="sxs-lookup"><span data-stu-id="3d3c5-142">hc, hC</span></span>               | <span data-ttu-id="3d3c5-143">CHAR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-143">CHAR</span></span>                                    | <span data-ttu-id="3d3c5-144">CHAR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-144">CHAR</span></span>                          |
| <span data-ttu-id="3d3c5-145">hs、hS</span><span class="sxs-lookup"><span data-stu-id="3d3c5-145">hs, hS</span></span>               | <span data-ttu-id="3d3c5-146">LPSTR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-146">LPSTR</span></span>                                   | <span data-ttu-id="3d3c5-147">LPSTR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-147">LPSTR</span></span>                         |
| <span data-ttu-id="3d3c5-148">lc、lC</span><span class="sxs-lookup"><span data-stu-id="3d3c5-148">lc, lC</span></span>               | <span data-ttu-id="3d3c5-149">WCHAR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-149">WCHAR</span></span>                                   | <span data-ttu-id="3d3c5-150">WCHAR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-150">WCHAR</span></span>                         |
| <span data-ttu-id="3d3c5-151">ls、lS</span><span class="sxs-lookup"><span data-stu-id="3d3c5-151">ls, lS</span></span>               | <span data-ttu-id="3d3c5-152">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-152">LPWSTR</span></span>                                  | <span data-ttu-id="3d3c5-153">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-153">LPWSTR</span></span>                        |
| <span data-ttu-id="3d3c5-154">s</span><span class="sxs-lookup"><span data-stu-id="3d3c5-154">s</span></span>                    | <span data-ttu-id="3d3c5-155">LPSTR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-155">LPSTR</span></span>                                   | <span data-ttu-id="3d3c5-156">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-156">LPWSTR</span></span>                        |
| <span data-ttu-id="3d3c5-157">S</span><span class="sxs-lookup"><span data-stu-id="3d3c5-157">S</span></span>                    | <span data-ttu-id="3d3c5-158">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-158">LPWSTR</span></span>                                  | <span data-ttu-id="3d3c5-159">LPSTR</span><span class="sxs-lookup"><span data-stu-id="3d3c5-159">LPSTR</span></span>                         |



 

<span data-ttu-id="3d3c5-160">輸出文字的資料類型一律取決於函數的版本。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-160">The data type for the output text always depends on the version of the function.</span></span> <span data-ttu-id="3d3c5-161">當輸入參數的資料類型和輸出文字的資料類型不一致時，print 函式會視需要執行從 Unicode 轉換成目前的 Windows 字碼頁，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-161">When the data type of the input parameter and the data type of the output text do not agree, the print function performs a conversion from Unicode to the current Windows code page, or vice versa, as required.</span></span>

<span data-ttu-id="3d3c5-162">若是列印函式的 Unicode 版本，格式字串是 Unicode，就像輸出文字一樣。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-162">For the Unicode version of the print functions, the format string is Unicode, as is the output text.</span></span>

> [!Caution]  
> <span data-ttu-id="3d3c5-163">不佳的緩衝區處理暗喻著在涉及緩衝區溢位的許多安全性問題中。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-163">Poor buffer handling is implicated in many security issues that involve buffer overruns.</span></span> <span data-ttu-id="3d3c5-164">請參閱 [>strsafe.h 參考](../menurc/strsafe-ovw.md)。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-164">See [Strsafe.h Reference](../menurc/strsafe-ovw.md).</span></span> <span data-ttu-id="3d3c5-165">>strsafe.h 中定義的函式會在程式碼中為適當的緩衝區處理提供額外的處理。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-165">The functions defined in Strsafe.h provide additional processing for proper buffer handling in your code.</span></span> <span data-ttu-id="3d3c5-166">基於這個理由，它們的目的是要取代其內建的 C/c + + 對應專案，以及特定的 Microsoft Windows 實作為方案。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-166">For this reason, they are intended to replace their built-in C/C++ counterparts as well as specific Microsoft Windows implementations.</span></span> <span data-ttu-id="3d3c5-167">如需詳細資訊，請參閱 [安全性考慮：國際化功能](security-considerations--international-features.md)。</span><span class="sxs-lookup"><span data-stu-id="3d3c5-167">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3d3c5-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="3d3c5-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d3c5-169">Windows API 中的 Unicode</span><span class="sxs-lookup"><span data-stu-id="3d3c5-169">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
