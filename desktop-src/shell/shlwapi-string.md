---
description: 本節說明 Windows Shell 字串處理函數。 本檔中所述的程式設計項目是由 Shlwapi.dll 匯出，並定義于 Shlwapi 和 Shlwapi 中。
title: Shell 字串處理函式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c2e47785db10ba7dc4bbe54e78e3a06be1b152a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945080"
---
# <a name="shell-string-handling-functions"></a><span data-ttu-id="010ac-104">Shell 字串處理函式</span><span class="sxs-lookup"><span data-stu-id="010ac-104">Shell String Handling Functions</span></span>

<span data-ttu-id="010ac-105">本節說明 Windows Shell 字串處理函數。</span><span class="sxs-lookup"><span data-stu-id="010ac-105">This section describes the Windows Shell string handling functions.</span></span> <span data-ttu-id="010ac-106">本檔中所述的程式設計項目是由 Shlwapi.dll 匯出，並定義于 Shlwapi 和 Shlwapi 中。</span><span class="sxs-lookup"><span data-stu-id="010ac-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="010ac-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="010ac-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="010ac-108">主題</span><span class="sxs-lookup"><span data-stu-id="010ac-108">Topic</span></span></th>
<th><span data-ttu-id="010ac-109">描述</span><span class="sxs-lookup"><span data-stu-id="010ac-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="010ac-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-111">在兩個字元之間執行比較。</span><span class="sxs-lookup"><span data-stu-id="010ac-111">Performs a comparison between two characters.</span></span> <span data-ttu-id="010ac-112">這項比較不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-112">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-114">在指定語言喜好設定時，捕獲與網站搭配使用的字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-114">Retrieves a string used with websites when specifying language preferences.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-116">針對兩個當地語系化字串開頭的指定字元數，執行區分大小寫的比較。</span><span class="sxs-lookup"><span data-stu-id="010ac-116">Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-118">從兩個當地語系化字串的開頭，執行指定字元數的不區分大小寫比較。</span><span class="sxs-lookup"><span data-stu-id="010ac-118">Performs a case-insensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-120">比較兩個當地語系化字串開頭的指定字元數。</span><span class="sxs-lookup"><span data-stu-id="010ac-120">Compares a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-122">判斷字元是否代表空格。</span><span class="sxs-lookup"><span data-stu-id="010ac-122">Determines whether a character represents a space.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-124">當指定的文字資源以間接字串的形式提供，而該資源的 (開頭為 ' @ ' 符號的字串) 時，會將指定的文字資源解壓縮。</span><span class="sxs-lookup"><span data-stu-id="010ac-124">Extracts a specified text resource when given that resource in the form of an indirect string (a string that begins with the '@' symbol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-126">在新配置的記憶體中建立字串的複本。</span><span class="sxs-lookup"><span data-stu-id="010ac-126">Makes a copy of a string in newly allocated memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-128">將一個字串附加至另一個字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-128">Appends one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="010ac-129">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="010ac-129">Do not use.</span></span> <span data-ttu-id="010ac-130">請參閱備註以取得替代功能。</span><span class="sxs-lookup"><span data-stu-id="010ac-130">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-132">將字元從某個字串複製並附加至另一個字串的結尾。</span><span class="sxs-lookup"><span data-stu-id="010ac-132">Copies and appends characters from one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="010ac-133">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="010ac-133">Do not use.</span></span> <span data-ttu-id="010ac-134">請參閱備註以取得替代功能。</span><span class="sxs-lookup"><span data-stu-id="010ac-134">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-136">串連兩個 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-136">Concatenates two Unicode strings.</span></span> <span data-ttu-id="010ac-137">當需要重複串連至相同緩衝區時使用。</span><span class="sxs-lookup"><span data-stu-id="010ac-137">Used when repeated concatenations to the same buffer are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-139">搜尋字串中第一次出現符合指定字元的字元。</span><span class="sxs-lookup"><span data-stu-id="010ac-139">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="010ac-140">比較會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-140">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-142">搜尋字串中第一次出現符合指定字元的字元。</span><span class="sxs-lookup"><span data-stu-id="010ac-142">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="010ac-143">這項比較不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-143">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-145">搜尋字串中第一次出現的指定字元。</span><span class="sxs-lookup"><span data-stu-id="010ac-145">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="010ac-146">這項比較不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-146">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-148">搜尋字串中第一次出現的指定字元。</span><span class="sxs-lookup"><span data-stu-id="010ac-148">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="010ac-149">比較會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-149">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-151">比較兩個字串，以判斷它們是否相同。</span><span class="sxs-lookup"><span data-stu-id="010ac-151">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="010ac-152">比較會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-152">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-154">使用 C 執行時間 (ASCII) 定序規則來比較字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-154">Compares strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="010ac-155">比較會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-155">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-157">比較兩個字串，以判斷它們是否相同。</span><span class="sxs-lookup"><span data-stu-id="010ac-157">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="010ac-158">這項比較不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-158">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-160">使用 C 執行時間 (ASCII) 定序規則比較兩個字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-160">Compares two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="010ac-161">這項比較不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-161">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-163">比較兩個 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-163">Compares two Unicode strings.</span></span> <span data-ttu-id="010ac-164">字串中的數位會被視為數位內容，而不是文字。</span><span class="sxs-lookup"><span data-stu-id="010ac-164">Digits in the strings are considered as numerical content rather than text.</span></span> <span data-ttu-id="010ac-165">這項測試不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-165">This test is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-167">比較兩個字串開頭的指定字元數，以判斷它們是否相同。</span><span class="sxs-lookup"><span data-stu-id="010ac-167">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="010ac-168">比較會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-168">The comparison is case-sensitive.</span></span> <span data-ttu-id="010ac-169"><strong>StrNCmp</strong>宏的名稱只與此函數不同。</span><span class="sxs-lookup"><span data-stu-id="010ac-169">The <strong>StrNCmp</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-171">使用 C 執行時間 (ASCII) 定序規則，比較兩個字串開頭的指定字元數。</span><span class="sxs-lookup"><span data-stu-id="010ac-171">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="010ac-172">比較會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-172">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-174">比較兩個字串開頭的指定字元數，以判斷它們是否相同。</span><span class="sxs-lookup"><span data-stu-id="010ac-174">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="010ac-175">這項比較不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-175">The comparison is not case-sensitive.</span></span> <span data-ttu-id="010ac-176"><strong>StrNCmpI</strong>宏的名稱只與此函數不同。</span><span class="sxs-lookup"><span data-stu-id="010ac-176">The <strong>StrNCmpI</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-178">使用 C 執行時間 (ASCII) 定序規則，比較兩個字串開頭的指定字元數。</span><span class="sxs-lookup"><span data-stu-id="010ac-178">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="010ac-179">這項比較不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-179">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-181">將一個字串複製到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-181">Copies one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="010ac-182">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="010ac-182">Do not use.</span></span> <span data-ttu-id="010ac-183">請參閱備註以取得替代功能。</span><span class="sxs-lookup"><span data-stu-id="010ac-183">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-185">將指定的字元數從一個字串的開頭複製到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-185">Copies a specified number of characters from the beginning of one string to another.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="010ac-186">請勿使用此函數或 <strong>StrNCpy</strong> 宏。</span><span class="sxs-lookup"><span data-stu-id="010ac-186">Do not use this function or the <strong>StrNCpy</strong> macro.</span></span> <span data-ttu-id="010ac-187">請參閱備註以取得替代功能。</span><span class="sxs-lookup"><span data-stu-id="010ac-187">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-189">搜尋字串中是否有任何一組字元的第一次出現。</span><span class="sxs-lookup"><span data-stu-id="010ac-189">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="010ac-190">搜尋方法會區分大小寫，且終止的 <strong>Null</strong> 字元會包含在搜尋模式比對中。</span><span class="sxs-lookup"><span data-stu-id="010ac-190">The search method is case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-192">搜尋字串中是否有任何一組字元的第一次出現。</span><span class="sxs-lookup"><span data-stu-id="010ac-192">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="010ac-193">搜尋方法不區分大小寫，且終止的 <strong>Null</strong> 字元會包含在搜尋模式比對中。</span><span class="sxs-lookup"><span data-stu-id="010ac-193">The search method is not case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-195">複製字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-195">Duplicates a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-197">根據大小，將數值轉換為表示以位元組為單位的大小值（以位元組為單位，kb、mb 或 gb）表示的數位值。</span><span class="sxs-lookup"><span data-stu-id="010ac-197">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-199">根據大小，將數值轉換為表示以位元組為單位的大小值（以位元組為單位，kb、mb 或 gb）表示的數位值。</span><span class="sxs-lookup"><span data-stu-id="010ac-199">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="010ac-200">與一個參數類型中的 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> 不同。</span><span class="sxs-lookup"><span data-stu-id="010ac-200">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-202">根據大小，將數值轉換為表示位元組、kb、mb 或 gb 數位的字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-202">Converts a numeric value into a string that represents the number in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="010ac-203">藉由提供選項以四捨五入至最接近的顯示數位，或捨棄 undisplayed 數位，來擴充 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="010ac-203">Extends <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> by offering the option to round to the nearest displayed digit or to discard undisplayed digits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-205">根據大小，將數值轉換為表示以位元組為單位的大小值（以位元組為單位，kb、mb 或 gb）表示的數位值。</span><span class="sxs-lookup"><span data-stu-id="010ac-205">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="010ac-206">與一個參數類型中的 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> 不同。</span><span class="sxs-lookup"><span data-stu-id="010ac-206">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-208">將數值轉換成字串，表示以 kb 為單位的大小值（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="010ac-208">Converts a numeric value into a string that represents the number expressed as a size value in kilobytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-210">將時間間隔（以毫秒為單位）轉換成字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-210">Converts a time interval, specified in milliseconds, to a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-212">比較兩個字串開頭的指定字元數，以判斷它們是否相等。</span><span class="sxs-lookup"><span data-stu-id="010ac-212">Compares a specified number of characters from the beginning of two strings to determine if they are equal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-214">將一個字串開頭的指定字元數附加至另一個字串的結尾。</span><span class="sxs-lookup"><span data-stu-id="010ac-214">Appends a specified number of characters from the beginning of one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="010ac-215">請勿使用此函數或 <strong>StrCatN</strong> 宏。</span><span class="sxs-lookup"><span data-stu-id="010ac-215">Do not use this function or the <strong>StrCatN</strong> macro.</span></span> <span data-ttu-id="010ac-216">請參閱備註以取得替代功能。</span><span class="sxs-lookup"><span data-stu-id="010ac-216">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-218">在字串中搜尋指定緩衝區所包含的第一次出現的字元。</span><span class="sxs-lookup"><span data-stu-id="010ac-218">Searches a string for the first occurrence of a character contained in a specified buffer.</span></span> <span data-ttu-id="010ac-219">此搜尋不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="010ac-219">This search does not include the terminating null character.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-221">在字串中搜尋指定字元的最後一個出現位置。</span><span class="sxs-lookup"><span data-stu-id="010ac-221">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="010ac-222">比較會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-222">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-224">在字串中搜尋指定字元的最後一個出現位置。</span><span class="sxs-lookup"><span data-stu-id="010ac-224">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="010ac-225">這項比較不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-225">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-227">接受包含或指向字串之<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder：： GetDisplayNameOf</strong></a>所傳回的<a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a>結構，並以<a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>形式傳回該字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-227">Accepts a <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> that contains or points to a string, and returns that string as a <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-229">將<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder：： GetDisplayNameOf</strong></a>傳回的<a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a>結構轉換成字串，並將結果放在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="010ac-229">Converts an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-231">採用<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder：： GetDisplayNameOf</strong></a>傳回的<a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a>結構，並將指標傳回至包含顯示名稱的配置字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-231">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> and returns a pointer to an allocated string containing the display name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-232"><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-232"><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-233">採用<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder：： GetDisplayNameOf</strong></a>傳回的<a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a>結構，將它轉換成字串，並將結果放在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="010ac-233">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a>, converts it to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-235">搜尋字串中所指定子字串的最後一個出現專案。</span><span class="sxs-lookup"><span data-stu-id="010ac-235">Searches for the last occurrence of a specified substring within a string.</span></span> <span data-ttu-id="010ac-236">這項比較不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-236">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-238">取得字串內子字串的長度，該字串包含指定緩衝區中包含的所有字元。</span><span class="sxs-lookup"><span data-stu-id="010ac-238">Obtains the length of a substring within a string that consists entirely of characters contained in a specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-240">在字串中尋找第一個出現的子字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-240">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="010ac-241">比較會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-241">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-243">在字串中尋找第一個出現的子字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-243">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="010ac-244">這項比較不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="010ac-244">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-246">將表示十進位值的字串轉換成整數。</span><span class="sxs-lookup"><span data-stu-id="010ac-246">Converts a string that represents a decimal value to an integer.</span></span> <span data-ttu-id="010ac-247"><strong>StrToLong</strong>宏與此函數相同。</span><span class="sxs-lookup"><span data-stu-id="010ac-247">The <strong>StrToLong</strong> macro is identical to this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-249">將表示十進位或十六進位值的字串轉換成64位整數。</span><span class="sxs-lookup"><span data-stu-id="010ac-249">Converts a string representing a decimal or hexadecimal value to a 64-bit integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-251">將表示十進位或十六進位數位的字串轉換成整數。</span><span class="sxs-lookup"><span data-stu-id="010ac-251">Converts a string representing a decimal or hexadecimal number to an integer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-253">從字串中移除指定的開頭和結尾字元。</span><span class="sxs-lookup"><span data-stu-id="010ac-253">Removes specified leading and trailing characters from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="010ac-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-255">接受可變長度的引數清單，並傳回引數的值做為 <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>樣式的格式化字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-255">Takes a variable-length argument list and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="010ac-256">請勿使用此函數。</span><span class="sxs-lookup"><span data-stu-id="010ac-256">Do not use this function.</span></span> <span data-ttu-id="010ac-257">請參閱備註以取得替代功能。</span><span class="sxs-lookup"><span data-stu-id="010ac-257">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="010ac-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="010ac-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="010ac-259">接受引數清單，並傳回引數的值做為 <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>樣式的格式化字串。</span><span class="sxs-lookup"><span data-stu-id="010ac-259">Takes a list of arguments and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="010ac-260">請勿使用此函數。</span><span class="sxs-lookup"><span data-stu-id="010ac-260">Do not use this function.</span></span> <span data-ttu-id="010ac-261">請參閱備註以取得替代功能。</span><span class="sxs-lookup"><span data-stu-id="010ac-261">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
