---
title: 字串
description: 本節討論字串函數。
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- 資源，字串
- 字串
- 字串函數 (string functions)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3231006de2dfe6ed611b58e5b511819a40c21e8b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103683557"
---
# <a name="strings"></a><span data-ttu-id="354bd-106">字串</span><span class="sxs-lookup"><span data-stu-id="354bd-106">Strings</span></span>

<span data-ttu-id="354bd-107">本節說明字串函式，並說明如何在您的應用程式中使用這些函數。</span><span class="sxs-lookup"><span data-stu-id="354bd-107">This section describes the string functions and explains how to use them in your applications.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="354bd-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="354bd-108">In This Section</span></span>



| <span data-ttu-id="354bd-109">Name</span><span class="sxs-lookup"><span data-stu-id="354bd-109">Name</span></span>                                     | <span data-ttu-id="354bd-110">描述</span><span class="sxs-lookup"><span data-stu-id="354bd-110">Description</span></span>                                             |
|------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="354bd-111">關於字串</span><span class="sxs-lookup"><span data-stu-id="354bd-111">About Strings</span></span>](about-strings.md)       | <span data-ttu-id="354bd-112">討論字串函數。</span><span class="sxs-lookup"><span data-stu-id="354bd-112">Discusses the string functions.</span></span><br/>              |
| [<span data-ttu-id="354bd-113">關於 >strsafe.h。h</span><span class="sxs-lookup"><span data-stu-id="354bd-113">About Strsafe.h</span></span>](strsafe-ovw.md)       | <span data-ttu-id="354bd-114">討論 >strsafe.h 中的字串函數。</span><span class="sxs-lookup"><span data-stu-id="354bd-114">Discusses the string functions in Strsafe.h.</span></span><br/> |
| [<span data-ttu-id="354bd-115">字串參考</span><span class="sxs-lookup"><span data-stu-id="354bd-115">String Reference</span></span>](string-reference.md) | <span data-ttu-id="354bd-116">包含 API 參考。</span><span class="sxs-lookup"><span data-stu-id="354bd-116">Contains the API reference.</span></span><br/>                  |



 

### <a name="string-functions"></a><span data-ttu-id="354bd-117">字串函式</span><span class="sxs-lookup"><span data-stu-id="354bd-117">String Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="354bd-118">Name</span><span class="sxs-lookup"><span data-stu-id="354bd-118">Name</span></span></th>
<th><span data-ttu-id="354bd-119">描述</span><span class="sxs-lookup"><span data-stu-id="354bd-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="354bd-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></span></span></td>
<td><span data-ttu-id="354bd-121">將字元字串或單一字元轉換成小寫。</span><span class="sxs-lookup"><span data-stu-id="354bd-121">Converts a character string or a single character to lowercase.</span></span> <span data-ttu-id="354bd-122">如果運算元是字元字串，則函式會就地轉換字元。</span><span class="sxs-lookup"><span data-stu-id="354bd-122">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></span></span></td>
<td><span data-ttu-id="354bd-124">將緩衝區中的大寫字元轉換成小寫字元。</span><span class="sxs-lookup"><span data-stu-id="354bd-124">Converts uppercase characters in a buffer to lowercase characters.</span></span> <span data-ttu-id="354bd-125">函數會就地轉換字元。</span><span class="sxs-lookup"><span data-stu-id="354bd-125">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></span></span></td>
<td><span data-ttu-id="354bd-127">抓取字串中下一個字元的指標。</span><span class="sxs-lookup"><span data-stu-id="354bd-127">Retrieves a pointer to the next character in a string.</span></span> <span data-ttu-id="354bd-128">此函數可以處理由單一或多位元組字元組成的字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-128">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></span></span></td>
<td><span data-ttu-id="354bd-130">抓取字串中下一個字元的指標。</span><span class="sxs-lookup"><span data-stu-id="354bd-130">Retrieves the pointer to the next character in a string.</span></span> <span data-ttu-id="354bd-131">此函數可以處理由單一或多位元組字元組成的字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-131">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></span></span></td>
<td><span data-ttu-id="354bd-133">抓取字串中上一個字元的指標。</span><span class="sxs-lookup"><span data-stu-id="354bd-133">Retrieves a pointer to the preceding character in a string.</span></span> <span data-ttu-id="354bd-134">此函數可以處理由單一或多位元組字元組成的字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-134">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></span></span></td>
<td><span data-ttu-id="354bd-136">抓取字串中上一個字元的指標。</span><span class="sxs-lookup"><span data-stu-id="354bd-136">Retrieves the pointer to the preceding character in a string.</span></span> <span data-ttu-id="354bd-137">此函數可以處理由單一或多位元組字元組成的字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-137">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></span></span></td>
<td><span data-ttu-id="354bd-139">將字串轉譯成 OEM 定義的字元集。</span><span class="sxs-lookup"><span data-stu-id="354bd-139">Translates a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></span></span></td>
<td><span data-ttu-id="354bd-141">將字串中指定的字元數轉譯成 OEM 定義的字元集。</span><span class="sxs-lookup"><span data-stu-id="354bd-141">Translates a specified number of characters in a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></span></span></td>
<td><span data-ttu-id="354bd-143">將字元字串或單一字元轉換成大寫。</span><span class="sxs-lookup"><span data-stu-id="354bd-143">Converts a character string or a single character to uppercase.</span></span> <span data-ttu-id="354bd-144">如果運算元是字元字串，則函式會就地轉換字元。</span><span class="sxs-lookup"><span data-stu-id="354bd-144">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></span></span></td>
<td><span data-ttu-id="354bd-146">將緩衝區中的小寫字元轉換成大寫字元。</span><span class="sxs-lookup"><span data-stu-id="354bd-146">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="354bd-147">函數會就地轉換字元。</span><span class="sxs-lookup"><span data-stu-id="354bd-147">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span></span></td>
<td><span data-ttu-id="354bd-149">使用指定的地區設定，比較兩個字元字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-149">Compares two character strings, using the specified locale.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="354bd-150">若要與 Unicode 相容，請使用 <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> 或 unicode 版本的 <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="354bd-150">For compatibility with Unicode, use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> or the Unicode version of <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></span></span></td>
<td><span data-ttu-id="354bd-152">使用指定的地區設定，比較兩個 Unicode (寬字元) 字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-152">Compares two Unicode (wide character) strings, using the specified locale.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></span></span></td>
<td><span data-ttu-id="354bd-154">將一個字串對應至另一個字串，並執行指定的轉換選項。</span><span class="sxs-lookup"><span data-stu-id="354bd-154">Maps one string to another, performing a specified transformation option.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></span></span></td>
<td><span data-ttu-id="354bd-156">抓取指定之來源字串中字元的字元類型資訊。</span><span class="sxs-lookup"><span data-stu-id="354bd-156">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="354bd-157">針對字串中的每個字元，函數會在輸出陣列的對應16位元素中設定一或多個位。</span><span class="sxs-lookup"><span data-stu-id="354bd-157">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="354bd-158">每個位都會識別指定的字元類型，例如字元是字母、數位，或兩者都不是。</span><span class="sxs-lookup"><span data-stu-id="354bd-158">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></span></span></td>
<td><span data-ttu-id="354bd-160">抓取指定之來源字串中字元的字元類型資訊。</span><span class="sxs-lookup"><span data-stu-id="354bd-160">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="354bd-161">針對字串中的每個字元，函數會在輸出陣列的對應16位元素中設定一或多個位。</span><span class="sxs-lookup"><span data-stu-id="354bd-161">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="354bd-162">每個位都會識別指定的字元類型，例如字元是字母、數位，或兩者都不是。</span><span class="sxs-lookup"><span data-stu-id="354bd-162">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span> <br/> <span data-ttu-id="354bd-163">不同于其 close 的<a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a>和<a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>， <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GETSTRINGTYPEEX</strong></a>會透過使用<strong> # define UNICODE</strong>參數來展現標準行為。</span><span class="sxs-lookup"><span data-stu-id="354bd-163">Unlike its close relatives <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> exhibits standard behavior through the use of the <strong>#define UNICODE</strong> switch.</span></span> <span data-ttu-id="354bd-164">這是建議的函式。</span><span class="sxs-lookup"><span data-stu-id="354bd-164">It is the recommended function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></span></span></td>
<td><span data-ttu-id="354bd-166">抓取指定之來源字串中字元的字元類型資訊。</span><span class="sxs-lookup"><span data-stu-id="354bd-166">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="354bd-167">針對字串中的每個字元，函數會在輸出陣列的對應16位元素中設定一或多個位。</span><span class="sxs-lookup"><span data-stu-id="354bd-167">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="354bd-168">每個位都會識別指定的字元類型，例如字元是字母、數位，或兩者都不是。</span><span class="sxs-lookup"><span data-stu-id="354bd-168">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></span></span></td>
<td><span data-ttu-id="354bd-170">判斷字元是否為字母字元。</span><span class="sxs-lookup"><span data-stu-id="354bd-170">Determines whether a character is an alphabetical character.</span></span> <span data-ttu-id="354bd-171">這項決定是根據使用者在安裝期間或透過主控台所選取之語言的語法。</span><span class="sxs-lookup"><span data-stu-id="354bd-171">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></span></span></td>
<td><span data-ttu-id="354bd-173">判斷字元是否為字母或數位字元。</span><span class="sxs-lookup"><span data-stu-id="354bd-173">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="354bd-174">這項決定是根據使用者在安裝期間或透過主控台所選取之語言的語法。</span><span class="sxs-lookup"><span data-stu-id="354bd-174">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></span></span></td>
<td><span data-ttu-id="354bd-176">判斷字元是否為小寫。</span><span class="sxs-lookup"><span data-stu-id="354bd-176">Determines whether a character is lowercase.</span></span> <span data-ttu-id="354bd-177">這項決定是根據使用者在安裝期間或透過主控台所選取之語言的語法。</span><span class="sxs-lookup"><span data-stu-id="354bd-177">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></span></span></td>
<td><span data-ttu-id="354bd-179">判斷字元是否為大寫。</span><span class="sxs-lookup"><span data-stu-id="354bd-179">Determines whether a character is uppercase.</span></span> <span data-ttu-id="354bd-180">這項決定是根據使用者在安裝期間或透過主控台所選取之語言的語法。</span><span class="sxs-lookup"><span data-stu-id="354bd-180">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>Loadstring 時</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a></span></span></td>
<td><span data-ttu-id="354bd-182">從與指定模組相關聯的可執行檔載入字串資源、將字串複製到緩衝區，並附加終止的 Null 字元。</span><span class="sxs-lookup"><span data-stu-id="354bd-182">Loads a string resource from the executable file associated with a specified module, copies the string into a buffer, and appends a terminating NULL character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></span></span></td>
<td><span data-ttu-id="354bd-184">將一個字串附加至另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-184">Appends one string to another.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></span></span></td>
<td><span data-ttu-id="354bd-186">比較兩個字元字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-186">Compares two character strings.</span></span> <span data-ttu-id="354bd-187">比較會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="354bd-187">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></span></span></td>
<td><span data-ttu-id="354bd-189">比較兩個字元字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-189">Compares two character strings.</span></span> <span data-ttu-id="354bd-190">這項比較不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="354bd-190">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></span></span></td>
<td><span data-ttu-id="354bd-192">將字串複製到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="354bd-192">Copies a string to a buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></span></span></td>
<td><span data-ttu-id="354bd-194">從來源字串將指定的字元數複製到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="354bd-194">Copies a specified number of characters from a source string into a buffer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span></span></td>
<td><span data-ttu-id="354bd-196">判斷指定之字串的長度 (不包括終止的 null 字元) 。</span><span class="sxs-lookup"><span data-stu-id="354bd-196">Determines the length of the specified string (not including the terminating null character).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></span></span></td>
<td><span data-ttu-id="354bd-198">將 OEM 定義字元集中的字串轉譯為 ANSI 或寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-198">Translates a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></span></span></td>
<td><span data-ttu-id="354bd-200">將字串中指定的字元數從 OEM 定義的字元集轉譯為 ANSI 或寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-200">Translates a specified number of characters in a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="354bd-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span></span></td>
<td><span data-ttu-id="354bd-202">將格式化資料寫入至指定的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="354bd-202">Writes formatted data to the specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="354bd-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="354bd-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></span></span></td>
<td><span data-ttu-id="354bd-204">使用引數清單的指標，將格式化資料寫入指定的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="354bd-204">Writes formatted data to the specified buffer using a pointer to a list of arguments.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="strsafe-functions"></a><span data-ttu-id="354bd-205">>strsafe.h 函式</span><span class="sxs-lookup"><span data-stu-id="354bd-205">Strsafe Functions</span></span>



| <span data-ttu-id="354bd-206">Name</span><span class="sxs-lookup"><span data-stu-id="354bd-206">Name</span></span>                                             | <span data-ttu-id="354bd-207">描述</span><span class="sxs-lookup"><span data-stu-id="354bd-207">Description</span></span>                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="354bd-208">**StringCbCat**</span><span class="sxs-lookup"><span data-stu-id="354bd-208">**StringCbCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | <span data-ttu-id="354bd-209">將一個字串串連至另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-209">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="354bd-210">**StringCbCatEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-210">**StringCbCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | <span data-ttu-id="354bd-211">將一個字串串連至另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-211">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="354bd-212">**StringCbCatN**</span><span class="sxs-lookup"><span data-stu-id="354bd-212">**StringCbCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | <span data-ttu-id="354bd-213">將指定的位元組數從一個字串串連到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-213">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="354bd-214">**StringCbCatNEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-214">**StringCbCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | <span data-ttu-id="354bd-215">將指定的位元組數從一個字串串連到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-215">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="354bd-216">**StringCbCopy**</span><span class="sxs-lookup"><span data-stu-id="354bd-216">**StringCbCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | <span data-ttu-id="354bd-217">將一個字串複製到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-217">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="354bd-218">**StringCbCopyEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-218">**StringCbCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | <span data-ttu-id="354bd-219">將一個字串複製到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-219">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="354bd-220">**StringCbCopyN**</span><span class="sxs-lookup"><span data-stu-id="354bd-220">**StringCbCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | <span data-ttu-id="354bd-221">將指定的位元組數目從某個字串複製到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-221">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="354bd-222">**StringCbCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-222">**StringCbCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | <span data-ttu-id="354bd-223">將指定的位元組數目從某個字串複製到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-223">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="354bd-224">**StringCbGets**</span><span class="sxs-lookup"><span data-stu-id="354bd-224">**StringCbGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | <span data-ttu-id="354bd-225">從 stdin 取得一行文字，最多可包含分行符號 ( ' \\ n ' ) 。</span><span class="sxs-lookup"><span data-stu-id="354bd-225">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="354bd-226">**StringCbGetsEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-226">**StringCbGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | <span data-ttu-id="354bd-227">從 stdin 取得一行文字，最多可包含分行符號 ( ' \\ n ' ) 。</span><span class="sxs-lookup"><span data-stu-id="354bd-227">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="354bd-228">**StringCbLength**</span><span class="sxs-lookup"><span data-stu-id="354bd-228">**StringCbLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | <span data-ttu-id="354bd-229">判斷字串是否超過指定的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="354bd-229">Determines whether a string exceeds the specified length, in bytes.</span></span><br/>                   |
| [<span data-ttu-id="354bd-230">**StringCbPrintf**</span><span class="sxs-lookup"><span data-stu-id="354bd-230">**StringCbPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | <span data-ttu-id="354bd-231">將格式化資料寫入指定的字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-231">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="354bd-232">**StringCbPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-232">**StringCbPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | <span data-ttu-id="354bd-233">將格式化資料寫入指定的字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-233">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="354bd-234">**StringCbVPrintf**</span><span class="sxs-lookup"><span data-stu-id="354bd-234">**StringCbVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | <span data-ttu-id="354bd-235">使用引數清單的指標，將格式化資料寫入指定的字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-235">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="354bd-236">**StringCbVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-236">**StringCbVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | <span data-ttu-id="354bd-237">使用引數清單的指標，將格式化資料寫入指定的字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-237">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="354bd-238">**StringCchCat**</span><span class="sxs-lookup"><span data-stu-id="354bd-238">**StringCchCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | <span data-ttu-id="354bd-239">將一個字串串連至另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-239">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="354bd-240">**StringCchCatEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-240">**StringCchCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | <span data-ttu-id="354bd-241">將一個字串串連至另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-241">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="354bd-242">**StringCchCatN**</span><span class="sxs-lookup"><span data-stu-id="354bd-242">**StringCchCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | <span data-ttu-id="354bd-243">將指定的字元數從一個字串串連到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-243">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="354bd-244">**StringCchCatNEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-244">**StringCchCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | <span data-ttu-id="354bd-245">將指定的字元數從一個字串串連到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-245">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="354bd-246">**StringCchCopy**</span><span class="sxs-lookup"><span data-stu-id="354bd-246">**StringCchCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | <span data-ttu-id="354bd-247">將一個字串複製到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-247">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="354bd-248">**StringCchCopyEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-248">**StringCchCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | <span data-ttu-id="354bd-249">將一個字串複製到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-249">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="354bd-250">**StringCchCopyN**</span><span class="sxs-lookup"><span data-stu-id="354bd-250">**StringCchCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | <span data-ttu-id="354bd-251">將指定的字元數從某個字串複製到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-251">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="354bd-252">**StringCchCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-252">**StringCchCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | <span data-ttu-id="354bd-253">將指定的字元數從某個字串複製到另一個字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-253">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="354bd-254">**StringCchGets**</span><span class="sxs-lookup"><span data-stu-id="354bd-254">**StringCchGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | <span data-ttu-id="354bd-255">從 stdin 取得一行文字，最多可包含分行符號 ( ' \\ n ' ) 。</span><span class="sxs-lookup"><span data-stu-id="354bd-255">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="354bd-256">**StringCchGetsEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-256">**StringCchGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | <span data-ttu-id="354bd-257">從 stdin 取得一行文字，最多可包含分行符號 ( ' \\ n ' ) 。</span><span class="sxs-lookup"><span data-stu-id="354bd-257">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="354bd-258">**StringCchLength**</span><span class="sxs-lookup"><span data-stu-id="354bd-258">**StringCchLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | <span data-ttu-id="354bd-259">判斷字串是否超過指定的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="354bd-259">Determines whether a string exceeds the specified length, in characters.</span></span><br/>              |
| [<span data-ttu-id="354bd-260">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="354bd-260">**StringCchPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | <span data-ttu-id="354bd-261">將格式化資料寫入指定的字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-261">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="354bd-262">**StringCchPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-262">**StringCchPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | <span data-ttu-id="354bd-263">將格式化資料寫入指定的字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-263">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="354bd-264">**StringCchVPrintf**</span><span class="sxs-lookup"><span data-stu-id="354bd-264">**StringCchVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | <span data-ttu-id="354bd-265">使用引數清單的指標，將格式化資料寫入指定的字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-265">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="354bd-266">**StringCchVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="354bd-266">**StringCchVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | <span data-ttu-id="354bd-267">使用引數清單的指標，將格式化資料寫入指定的字串。</span><span class="sxs-lookup"><span data-stu-id="354bd-267">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |



 

 

