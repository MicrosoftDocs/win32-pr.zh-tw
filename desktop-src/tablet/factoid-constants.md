---
description: 定義常數位符串值，藉由提供內容相關資訊給辨識器，來增加辨識的精確度。
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: " (Msinkaut 的) 的模擬模擬常數"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1353a4989ddfb5af3865788c0fa7fdc2d377f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511724"
---
# <a name="factoid-constants"></a><span data-ttu-id="cfafe-103">模擬常數</span><span class="sxs-lookup"><span data-stu-id="cfafe-103">Factoid Constants</span></span>

<span data-ttu-id="cfafe-104">定義常數位符串值，藉由提供內容相關資訊給辨識器，來增加辨識的精確度。</span><span class="sxs-lookup"><span data-stu-id="cfafe-104">Defines constant string values that are used to increase recognition accuracy by providing contextual information to the recognizer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="cfafe-105">Name</span><span class="sxs-lookup"><span data-stu-id="cfafe-105">Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="cfafe-106">描述</span><span class="sxs-lookup"><span data-stu-id="cfafe-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl> <span data-ttu-id="cfafe-107"><dt><strong>FACTOID_NONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-107"><dt><strong>FACTOID_NONE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-108">停用所有其他 factoids 和字典。</span><span class="sxs-lookup"><span data-stu-id="cfafe-108">Disables all other factoids and dictionaries.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl> <span data-ttu-id="cfafe-109"><dt><strong>FACTOID_DEFAULT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-109"><dt> <strong>FACTOID_DEFAULT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-110">西方語言的 factoids 預設設定包括系統字典、使用者字典、各種標點符號，以及 Web 和數位的模擬。</span><span class="sxs-lookup"><span data-stu-id="cfafe-110">The Default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the Web and Number factoid.</span></span> <span data-ttu-id="cfafe-111">東亞語言的 factoids 預設設定包含辨識器支援的所有字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-111">The Default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl> <span data-ttu-id="cfafe-112"><dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-112"><dt> <strong>FACTOID_SYSTEMDICTIONARY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-113">指出辨識器僅使用系統字典。</span><span class="sxs-lookup"><span data-stu-id="cfafe-113">Indicates to a recognizer to use the system dictionary only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl> <span data-ttu-id="cfafe-114"><dt><strong>FACTOID_WORDLIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-114"><dt> <strong>FACTOID_WORDLIST</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-115">指示辨識器使用以程式設計方式定義的單字清單。</span><span class="sxs-lookup"><span data-stu-id="cfafe-115">Indicates to a recognizer to use a programmatically-defined list of words.</span></span> <span data-ttu-id="cfafe-116">單字清單是由<a href="inkrecognizercontext-class.md"><strong>InkRecognizerCoNtext</strong></a>物件的 [<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>單詞表</strong></a>] 屬性所定義。</span><span class="sxs-lookup"><span data-stu-id="cfafe-116">The list of words is defined by the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList</strong></a> property of a <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cfafe-117">如果將字串加入至字組清單，也會隱含地加入其大寫版本。</span><span class="sxs-lookup"><span data-stu-id="cfafe-117">If a string is added to a word list, its capitalized versions are also implicitly added.</span></span> <span data-ttu-id="cfafe-118">比方說，加入 hello 時，會 &quot; &quot; 隱含地加入 &quot; hello &quot; 和 &quot; hello &quot; 。</span><span class="sxs-lookup"><span data-stu-id="cfafe-118">For instance, adding &quot;hello&quot; implicitly adds &quot;Hello&quot; and &quot;HELLO&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl> <span data-ttu-id="cfafe-119"><dt><strong>FACTOID_EMAIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-119"><dt> <strong>FACTOID_EMAIL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-120">指示辨識器尋找電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="cfafe-120">Indicates to a recognizer to look for an email address.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cfafe-121">&quot; someone@example.com 此模擬程式必須使用完整的電子郵件地址（例如 &quot; ）。</span><span class="sxs-lookup"><span data-stu-id="cfafe-121">A fully qualified email address, such as &quot;someone@example.com&quot;, must be used for this factoid.</span></span> <span data-ttu-id="cfafe-122">無法辨識獨立的別名，例如 &quot; 他人 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="cfafe-122">A lone alias, such as &quot;someone&quot;, is not recognized.</span></span>
</blockquote>
<br/>
<pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl> <span data-ttu-id="cfafe-123"><dt><strong>FACTOID_WEB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-123"><dt><strong>FACTOID_WEB</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-124">指示辨識器尋找網址。</span><span class="sxs-lookup"><span data-stu-id="cfafe-124">Indicates to a recognizer to look for a Web address.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl> <span data-ttu-id="cfafe-125"><dt><strong>FACTOID_ONECHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-125"><dt> <strong>FACTOID_ONECHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-126">指示辨識器尋找單一字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-126">Indicates to a recognizer to look for a single character.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cfafe-127">此模擬程式會尋找任何隔離的 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-127">This factoid looks for any isolated ANSI character.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl> <span data-ttu-id="cfafe-128"><dt><strong>FACTOID_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-128"><dt> <strong>FACTOID_NUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-129">指示辨識器尋找數位。</span><span class="sxs-lookup"><span data-stu-id="cfafe-129">Indicates to a recognizer to look for a number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cfafe-130">數值包含分隔符號、小數、序數和其他常用的數位記號。</span><span class="sxs-lookup"><span data-stu-id="cfafe-130">Numeric values include separators, decimals, ordinals and other commonly used numeric symbols.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl> <span data-ttu-id="cfafe-131"><dt><strong>FACTOID_DIGIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-131"><dt> <strong>FACTOID_DIGIT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-132">指出辨識器要尋找單一位數（0到9）。</span><span class="sxs-lookup"><span data-stu-id="cfafe-132">Indicates to a recognizer to look for a single digit, 0 through 9.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl> <span data-ttu-id="cfafe-133"><dt><strong>FACTOID_NUMBERSIMPLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-133"><dt> <strong>FACTOID_NUMBERSIMPLE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-134">提供簡單的數值內容給辨識器。</span><span class="sxs-lookup"><span data-stu-id="cfafe-134">Provides a simple numeric context to a recognizer.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cfafe-135">此版本的 Tablet PC SDK 不支援此模擬。</span><span class="sxs-lookup"><span data-stu-id="cfafe-135">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl> <span data-ttu-id="cfafe-136"><dt><strong>FACTOID_CURRENCY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-136"><dt> <strong>FACTOID_CURRENCY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-137">指示辨識器尋找表示貨幣值的字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-137">Indicates to a recognizer to look for characters that denote a currency value.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl> <span data-ttu-id="cfafe-138"><dt><strong>FACTOID_POSTALCODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-138"><dt> <strong>FACTOID_POSTALCODE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-139">指示辨識器尋找郵遞區號。</span><span class="sxs-lookup"><span data-stu-id="cfafe-139">Indicates to a recognizer to look for postal codes.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>98112</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl> <span data-ttu-id="cfafe-140"><dt><strong>FACTOID_PERCENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-140"><dt> <strong>FACTOID_PERCENT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-141">指示辨識器尋找百分比。</span><span class="sxs-lookup"><span data-stu-id="cfafe-141">Indicates to a recognizer to look for percentages.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>87%</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl> <span data-ttu-id="cfafe-142"><dt><strong>FACTOID_DATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-142"><dt> <strong>FACTOID_DATE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-143">指示辨識器尋找表示日期的字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-143">Indicates to a recognizer to look for characters that denote a date.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>10/30/2001, &#39;01, 31/12, 12/99, 1999-2000</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl> <span data-ttu-id="cfafe-144"><dt><strong>FACTOID_TIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-144"><dt> <strong>FACTOID_TIME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-145">指示辨識器尋找表示時間的字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-145">Indicates to a recognizer to look for characters that denote a time.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl> <span data-ttu-id="cfafe-146"><dt><strong>FACTOID_TELEPHONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-146"><dt> <strong>FACTOID_TELEPHONE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-147">指出辨識器尋找代表電話號碼的字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-147">Indicates to a recognizer to look for characters that denote a telephone number.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl> <span data-ttu-id="cfafe-148"><dt><strong>FACTOID_FILENAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-148"><dt> <strong>FACTOID_FILENAME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-149">指示辨識器尋找表示檔案名的字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-149">Indicates to a recognizer to look for characters that denote a file name.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl> <span data-ttu-id="cfafe-150"><dt><strong>FACTOID_UPPERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-150"><dt> <strong>FACTOID_UPPERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-151">指出辨識器要尋找單一大寫字元： A 到 Z。</span><span class="sxs-lookup"><span data-stu-id="cfafe-151">Indicates to a recognizer to look for a single uppercase character: A through Z.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl> <span data-ttu-id="cfafe-152"><dt><strong>FACTOID_LOWERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-152"><dt> <strong>FACTOID_LOWERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-153">指出辨識器要尋找單一小寫字元： A 到 Z。</span><span class="sxs-lookup"><span data-stu-id="cfafe-153">Indicates to a recognizer to look for a single lowercase character: A through Z.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cfafe-154">此版本的 Tablet PC SDK 不支援此模擬。</span><span class="sxs-lookup"><span data-stu-id="cfafe-154">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl> <span data-ttu-id="cfafe-155"><dt><strong>FACTOID_PUNCCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-155"><dt> <strong>FACTOID_PUNCCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-156">指示辨識器尋找標點符號字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-156">Indicates to a recognizer to look for punctuation characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cfafe-157">此版本的 Tablet PC SDK 不支援此模擬。</span><span class="sxs-lookup"><span data-stu-id="cfafe-157">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl> <span data-ttu-id="cfafe-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-159">指示辨識器尋找常用的日文漢字、片假名和平假名字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-159">Indicates to a recognizer to look for commonly used Kanji, Katakana, and Hiragana characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl> <span data-ttu-id="cfafe-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-161">指出辨識器尋找常用的簡體中文字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-161">Indicates to a recognizer to look for commonly used Simplified Chinese characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl> <span data-ttu-id="cfafe-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-163">指出辨識器會尋找常用的繁體中文字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-163">Indicates to a recognizer to look for commonly used Traditional Chinese characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl> <span data-ttu-id="cfafe-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-165">指示辨識器尋找常用的韓文字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-165">Indicates to a recognizer to look for commonly used Korean characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl> <span data-ttu-id="cfafe-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-167">指出辨識器只尋找平假名字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-167">Indicates to a recognizer to look for Hiragana characters only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl> <span data-ttu-id="cfafe-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-169">指出辨識器只尋找片假名字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-169">Indicates to a recognizer to look for Katakana characters only.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl> <span data-ttu-id="cfafe-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-171">指示辨識器尋找常用的中文字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-171">Indicates to a recognizer to look for commonly used kanji characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl> <span data-ttu-id="cfafe-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-173">指出辨識器尋找很少使用的中文字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-173">Indicates to a recognizer to look for rarely used kanji characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cfafe-174">此版本的 Tablet PC SDK 不支援此模擬。</span><span class="sxs-lookup"><span data-stu-id="cfafe-174">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl> <span data-ttu-id="cfafe-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-176">指示辨識器尋找注音字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-176">Indicates to a recognizer to look for Bopomofo characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl> <span data-ttu-id="cfafe-177"><dt><strong>FACTOID_JAMO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-177"><dt><strong>FACTOID_JAMO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-178">指示辨識器尋找韓文相容性拼音字母字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-178">Indicates to a recognizer to look for Hangul compatibility Jamo characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl> <span data-ttu-id="cfafe-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-180">指示辨識器尋找常用的韓文字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-180">Indicates to a recognizer to look for commonly used Hangul characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl> <span data-ttu-id="cfafe-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="cfafe-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="cfafe-182">指出辨識器尋找很少使用的韓文字元。</span><span class="sxs-lookup"><span data-stu-id="cfafe-182">Indicates to a recognizer to look for rarely used Hangul characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cfafe-183">此版本的 Tablet PC SDK 不支援此模擬。</span><span class="sxs-lookup"><span data-stu-id="cfafe-183">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="cfafe-184">備註</span><span class="sxs-lookup"><span data-stu-id="cfafe-184">Remarks</span></span>

<span data-ttu-id="cfafe-185">在 c + + 中，您可以在 Msinkaut .h 標頭檔中存取這些常數， <systemdrive> \\ 如果您將 SDK 安裝在預設位置，該檔案位於： Program Files \\ Microsoft TABLET PC Platform SDK \\ Include 目錄。</span><span class="sxs-lookup"><span data-stu-id="cfafe-185">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="cfafe-186">這些常數都是 WCHARs，而不是 Bstr。</span><span class="sxs-lookup"><span data-stu-id="cfafe-186">These constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="cfafe-187">必須先將它們轉換成 Bstr，才能做為物件方法的參數使用。</span><span class="sxs-lookup"><span data-stu-id="cfafe-187">They must be converted into BSTRs before use as parameters to object methods.</span></span> <span data-ttu-id="cfafe-188">如需 BSTR 資料類型的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="cfafe-188">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="cfafe-189">若為拉丁腳本的辨識器，則會針對回溯相容性提供此類別中定義的 factoids。</span><span class="sxs-lookup"><span data-stu-id="cfafe-189">For recognizers of Latin script, the factoids defined in this class are provided for backward compatibility only.</span></span> <span data-ttu-id="cfafe-190">針對新的開發，建議您使用 [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) 函數中定義的值。</span><span class="sxs-lookup"><span data-stu-id="cfafe-190">For new development, you are encouraged to use the values defined in the [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) function.</span></span> <span data-ttu-id="cfafe-191">如需詳細資訊，請參閱 [使用內容改善精確度](using-context-to-improve-accuracy.md)。</span><span class="sxs-lookup"><span data-stu-id="cfafe-191">For details, see [Using Context to Improve Accuracy](using-context-to-improve-accuracy.md).</span></span>

 

<span data-ttu-id="cfafe-192">您可以使用這些識別碼來指定辨識期間應使用的模擬。</span><span class="sxs-lookup"><span data-stu-id="cfafe-192">Use these identifiers to specify which factoid should be used during recognition.</span></span>

<span data-ttu-id="cfafe-193">下列 factoids 組合僅支援西方語言。</span><span class="sxs-lookup"><span data-stu-id="cfafe-193">The following combinations of factoids are supported for western languages only.</span></span> <span data-ttu-id="cfafe-194">這些都沒有不同的定義，但可以接受使用 factoids 之物件的「 [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) 」屬性的字串常值輸入。</span><span class="sxs-lookup"><span data-stu-id="cfafe-194">These do not have separate definitions, but are acceptable string literal inputs to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of objects that use factoids.</span></span> <span data-ttu-id="cfafe-195">這些模擬型字串常數允許輸入符合運算式中的任何 factoids。</span><span class="sxs-lookup"><span data-stu-id="cfafe-195">These factoid string constants allow the input to match any of the factoids in the expression.</span></span>



| <span data-ttu-id="cfafe-196">合併</span><span class="sxs-lookup"><span data-stu-id="cfafe-196">Combination</span></span>               | <span data-ttu-id="cfafe-197">定義</span><span class="sxs-lookup"><span data-stu-id="cfafe-197">Definition</span></span>                                                |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="cfafe-198">"WEB \| 單詞表"</span><span class="sxs-lookup"><span data-stu-id="cfafe-198">"WEB\|WORDLIST"</span></span>           | <span data-ttu-id="cfafe-199">Web 模擬或字組清單。</span><span class="sxs-lookup"><span data-stu-id="cfafe-199">The Web factoid or the word list.</span></span>                         |
| <span data-ttu-id="cfafe-200">"EMAIL \| 單詞表"</span><span class="sxs-lookup"><span data-stu-id="cfafe-200">"EMAIL\|WORDLIST"</span></span>         | <span data-ttu-id="cfafe-201">電子郵件的智慧標籤或字組清單。</span><span class="sxs-lookup"><span data-stu-id="cfafe-201">The Email factoid or the word list.</span></span>                       |
| <span data-ttu-id="cfafe-202">"FILENAME \| WEB \| 單詞表"</span><span class="sxs-lookup"><span data-stu-id="cfafe-202">"FILENAME\|WEB\|WORDLIST"</span></span> | <span data-ttu-id="cfafe-203">檔案名模擬或 Web 模擬或字組清單。</span><span class="sxs-lookup"><span data-stu-id="cfafe-203">The Filename factoid or the Web factoid or the word list.</span></span> |



 

<span data-ttu-id="cfafe-204">如果您使用 [InkEdit](inkedit-control-reference.md) 控制項，則可以將模擬程式設定為控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="cfafe-204">If you are using the [InkEdit](inkedit-control-reference.md) control, the factoid can be set as a property of the control.</span></span>

<span data-ttu-id="cfafe-205">如果您使用 Tablet PC 平臺 Api，您可以在 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md)物件上設定 [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)程式屬性。</span><span class="sxs-lookup"><span data-stu-id="cfafe-205">If you are using the Tablet PC Platform APIs, you can set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on an [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

<span data-ttu-id="cfafe-206">或者，您可以使用實際的「模擬」字串常數來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="cfafe-206">Alternatively, you can set this property with the actual factoid string constant.</span></span>

> [!Note]  
> <span data-ttu-id="cfafe-207">模擬型字串常數會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cfafe-207">Factoid string constants are case sensitive.</span></span> <span data-ttu-id="cfafe-208">如需 factoids 及其使用方式的詳細資訊，請參閱使用內容 [改善精確度](using-context-to-improve-accuracy.md)。</span><span class="sxs-lookup"><span data-stu-id="cfafe-208">For more information about factoids and how to use them, see Using Context to [Improve Accuracy](using-context-to-improve-accuracy.md).</span></span> <span data-ttu-id="cfafe-209">若要判斷是否有特定語言的模擬程式，請參閱 [第1版所支援的 Factoids](supported-factoids-from-version-1.md)。</span><span class="sxs-lookup"><span data-stu-id="cfafe-209">To determine whether a factoid is available in a specific language, see [Supported Factoids from Version 1](supported-factoids-from-version-1.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cfafe-210">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfafe-210">Requirements</span></span>



| <span data-ttu-id="cfafe-211">需求</span><span class="sxs-lookup"><span data-stu-id="cfafe-211">Requirement</span></span> | <span data-ttu-id="cfafe-212">值</span><span class="sxs-lookup"><span data-stu-id="cfafe-212">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfafe-213">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfafe-213">Minimum supported client</span></span><br/> | <span data-ttu-id="cfafe-214">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfafe-214">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cfafe-215">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfafe-215">Minimum supported server</span></span><br/> | <span data-ttu-id="cfafe-216">都不支援</span><span class="sxs-lookup"><span data-stu-id="cfafe-216">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="cfafe-217">標頭</span><span class="sxs-lookup"><span data-stu-id="cfafe-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfafe-218"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="cfafe-218"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfafe-219">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfafe-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="cfafe-220">[**模擬屬性 \[ InkRecognizeCoNtext 類別\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="cfafe-220">[**Factoid Property \[InkRecognizeContext Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="cfafe-221">[**模擬屬性 \[ PenInputPanel 類別\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="cfafe-221">[**Factoid Property \[PenInputPanel Class\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="cfafe-222">[**模擬的屬性 \[ InkEdit 控制項\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="cfafe-222">[**Factoid Property \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span></span>
</dt> <dt>

[<span data-ttu-id="cfafe-223">使用內容改善精確度</span><span class="sxs-lookup"><span data-stu-id="cfafe-223">Using Context to Improve Accuracy</span></span>](using-context-to-improve-accuracy.md)
</dt> <dt>

[<span data-ttu-id="cfafe-224">從版本1支援的 Factoids</span><span class="sxs-lookup"><span data-stu-id="cfafe-224">Supported Factoids from Version 1</span></span>](supported-factoids-from-version-1.md)
</dt> </dl>

 

