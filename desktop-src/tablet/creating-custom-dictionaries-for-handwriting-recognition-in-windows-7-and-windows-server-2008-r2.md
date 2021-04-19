---
description: 本節說明如何建立手寫辨識的自訂字典。
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: 在 Windows 7 和 Windows Server 2008 R2 中建立手寫辨識的自訂字典
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b9b7b5a1d9dfadddd83825aea7d6f676439999
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986290"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="13ee4-103">在 Windows 7 和 Windows Server 2008 R2 中建立手寫辨識的自訂字典</span><span class="sxs-lookup"><span data-stu-id="13ee4-103">Creating Custom Dictionaries for Handwriting Recognition in Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="13ee4-104">本節說明如何建立手寫辨識的自訂字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-104">This section explains how to create a custom dictionary for handwriting recognition.</span></span>

<span data-ttu-id="13ee4-105">在 Windows 7 作業系統和 Windows Server 2008 R2 作業系統中，手寫辨識的精確度可透過使用自訂字典大幅改進。</span><span class="sxs-lookup"><span data-stu-id="13ee4-105">In the Windows 7 operating system and the Windows Server 2008 R2 operating system, the accuracy of handwriting recognition can be significantly improved through the use of custom dictionaries.</span></span> <span data-ttu-id="13ee4-106">這些字典會補充或取代用於手寫的系統字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-106">These dictionaries supplement or replace system dictionaries used for handwriting.</span></span> <span data-ttu-id="13ee4-107">手寫辨識支援是透過筆跡和手寫服務功能提供，必須透過伺服器管理員啟用。</span><span class="sxs-lookup"><span data-stu-id="13ee4-107">Support for handwriting recognition is provided through the Ink and Handwriting Services feature that needs to be enabled through Server Manager.</span></span>

> [!Note]  
> <span data-ttu-id="13ee4-108">只有在已安裝該語言的手寫辨識器時，才能針對語言安裝自訂字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-108">Custom dictionaries can be installed for a language only if the handwriting recognizer for that language is installed.</span></span>

 

<span data-ttu-id="13ee4-109">有兩個基本步驟可以設定自訂字典以進行手寫：</span><span class="sxs-lookup"><span data-stu-id="13ee4-109">There are two basic steps to setting up a custom dictionary for handwriting:</span></span>

-   <span data-ttu-id="13ee4-110">編譯字組清單。</span><span class="sxs-lookup"><span data-stu-id="13ee4-110">Compile a word list.</span></span> <span data-ttu-id="13ee4-111">編譯會建立編譯的自訂字典 ( hwrdict) 檔。</span><span class="sxs-lookup"><span data-stu-id="13ee4-111">The compilation creates a compiled custom dictionary (.hwrdict) file.</span></span>
-   <span data-ttu-id="13ee4-112">安裝已編譯的自訂字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-112">Install the compiled custom dictionary.</span></span>

## <a name="compiling-a-word-list"></a><span data-ttu-id="13ee4-113">編譯單字清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-113">Compiling a Word List</span></span>

<span data-ttu-id="13ee4-114">要編譯的單字清單必須是純文字格式，而且應該使用 Unicode 編碼儲存。</span><span class="sxs-lookup"><span data-stu-id="13ee4-114">The word list to be compiled must be in plain-text format and should be saved using a Unicode encoding.</span></span> <span data-ttu-id="13ee4-115">其他編碼將無法運作。</span><span class="sxs-lookup"><span data-stu-id="13ee4-115">Other encodings will not work.</span></span> <span data-ttu-id="13ee4-116">文字檔中的每一行都會以單一專案的形式在字典中取得。</span><span class="sxs-lookup"><span data-stu-id="13ee4-116">Each line of the text file is taken as a single entry in the dictionary.</span></span> <span data-ttu-id="13ee4-117">允許包含一或多個空格的 Multiword 單位專案。</span><span class="sxs-lookup"><span data-stu-id="13ee4-117">Multiword units entries containing one or more spaces are allowed.</span></span> <span data-ttu-id="13ee4-118">會忽略行開頭或結尾的空格。</span><span class="sxs-lookup"><span data-stu-id="13ee4-118">Spaces at the beginning or end of a line are ignored.</span></span>

<span data-ttu-id="13ee4-119">自訂字典是從命令列編譯的。</span><span class="sxs-lookup"><span data-stu-id="13ee4-119">A custom dictionary is compiled from a command line.</span></span> <span data-ttu-id="13ee4-120">若要編譯字典，請開啟命令視窗，流覽至包含單字清單的資料夾，然後使用您想要使用的命令列選項來執行 HwrComp.exe。</span><span class="sxs-lookup"><span data-stu-id="13ee4-120">To compile a dictionary, open a command window, navigate to the folder containing the word list, and then run HwrComp.exe with the command-line options you want to use.</span></span>

<span data-ttu-id="13ee4-121">下列範例顯示命令列選項的使用語法。</span><span class="sxs-lookup"><span data-stu-id="13ee4-121">The following example shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a><span data-ttu-id="13ee4-122">選項的說明</span><span class="sxs-lookup"><span data-stu-id="13ee4-122">Explanation of Options</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13ee4-123">參數</span><span class="sxs-lookup"><span data-stu-id="13ee4-123">Parameter</span></span></th>
<th><span data-ttu-id="13ee4-124">Description</span><span class="sxs-lookup"><span data-stu-id="13ee4-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="13ee4-125">-lang <localename></span><span class="sxs-lookup"><span data-stu-id="13ee4-125">-lang <localename></span></span></td>
<td><span data-ttu-id="13ee4-126">指派給已編譯自訂字典檔案的指定地區設定名稱。</span><span class="sxs-lookup"><span data-stu-id="13ee4-126">The specified locale name assigned to the compiled custom dictionary file.</span></span> <span data-ttu-id="13ee4-127">引數 <localename> 的格式為 LANGUAGE REGION。</span><span class="sxs-lookup"><span data-stu-id="13ee4-127">The argument <localename> has the form language-REGION.</span></span> <span data-ttu-id="13ee4-128">其中一個範例是 en-us，表示美國地區的英文語言。</span><span class="sxs-lookup"><span data-stu-id="13ee4-128">An example of this is en-US, which signifies the English language in the United States region.</span></span> <span data-ttu-id="13ee4-129">如需此表單的範例，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。</span><span class="sxs-lookup"><span data-stu-id="13ee4-129">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <span data-ttu-id="13ee4-130">這項功能支援下列語言的 Windows 7 和 Windows Server 2008 R2： en-us、en-us、en-us、en-us、de、de、de、fr、es、es-MX、es-AR，以及。它（IT）、nl NL、nl-a、pt-BR、pt、da-深色、sv-SE、nb-NO、nn-NO、fi、pl、CZ、ru、、ro、sr-iov、-CS、sr-iov-、CA 和 hr-HR。</span><span class="sxs-lookup"><span data-stu-id="13ee4-130">The following languages are supported for Windows 7 and Windows Server 2008 R2 by this feature: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-BE, pt-BR, pt-PT, da-DK, sv-SE, nb-NO, nn-NO, fi-FI, pl-PL, cs-CZ, ru-RU, ro-RO, sr-Latn-CS, sr-Cyrl-CS, ca-ES and hr-HR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13ee4-131">-類型 <type></span><span class="sxs-lookup"><span data-stu-id="13ee4-131">-type <type></span></span></td>
<td><span data-ttu-id="13ee4-132">選項引數 <type> 是將資源作為主要單字清單的單一字串串連 (主要) 或作為主要單字清單的補充 (次要) 後面接著套用資源的實際單字清單名稱 (例如字典或姓氏) 。</span><span class="sxs-lookup"><span data-stu-id="13ee4-132">The option argument <type> is a single-string concatenation of the resource's use as either the main word list (PRIMARY) or as a supplement to the main word list (SECONDARY) followed by the actual word list name to which the resource is applied (such as DICTIONARY or SURNAME).</span></span> <span data-ttu-id="13ee4-133">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="13ee4-133">The following are possible values:</span></span>
<ul>
<li><span data-ttu-id="13ee4-134">主要-CITYNAME-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-134">PRIMARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-135">主要-COUNTRYNAME-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-135">PRIMARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-136">主要-COUNTRYSHORTNAME-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-136">PRIMARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-137">主要字典</span><span class="sxs-lookup"><span data-stu-id="13ee4-137">PRIMARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="13ee4-138">主要-GIVENNAME-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-138">PRIMARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-139">主要-STATEORPROVINCE-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-139">PRIMARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="13ee4-140">主要-STREETNAME-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-140">PRIMARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-141">主要-姓氏-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-141">PRIMARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-142">次要-CITYNAME-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-142">SECONDARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-143">次要-COUNTRYNAME-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-143">SECONDARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-144">次要-COUNTRYSHORTNAME-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-144">SECONDARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-145">次要字典</span><span class="sxs-lookup"><span data-stu-id="13ee4-145">SECONDARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="13ee4-146">次要-EMAILSMTP-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-146">SECONDARY-EMAILSMTP-LIST</span></span></li>
<li><span data-ttu-id="13ee4-147">次要-EMAILUSERNAME-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-147">SECONDARY-EMAILUSERNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-148">次要-GIVENNAME-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-148">SECONDARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-149">次要-STATEORPROVINCE-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-149">SECONDARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="13ee4-150">次要-STREETNAME-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-150">SECONDARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-151">次要-姓氏-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-151">SECONDARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="13ee4-152">次要 URL-清單</span><span class="sxs-lookup"><span data-stu-id="13ee4-152">SECONDARY-URL-LIST</span></span></li>
</ul>
<span data-ttu-id="13ee4-153">如果類型值的開頭是前置詞主要，編譯的字典在安裝之後，將會取代該語言的系統字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-153">If a type value starts with the prefix PRIMARY, the compiled dictionary, after it is installed, will replace the system dictionary for that language.</span></span> <span data-ttu-id="13ee4-154">值的主要字典代表語言的主要系統字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-154">The value PRIMARY-DICTIONARY represents the main system dictionary for a language.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="13ee4-155">取代系統字典不會對原始的系統字典內容執行任何動作，因為取代只有在移除自訂字典後才會生效。</span><span class="sxs-lookup"><span data-stu-id="13ee4-155">Replacing a system dictionary does nothing to the original system dictionary content, as the replacement is in effect only until the custom dictionary has been removed.</span></span>
</blockquote>
<br/> <span data-ttu-id="13ee4-156">如果類型值的開頭是前置詞次要，編譯的字典將會補充系統字典，而不會取代它。</span><span class="sxs-lookup"><span data-stu-id="13ee4-156">If a type value starts with the prefix SECONDARY, the compiled dictionary will supplement the system dictionary without replacing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13ee4-157">-批註</span><span class="sxs-lookup"><span data-stu-id="13ee4-157">-comment</span></span> <comment></td>
<td><span data-ttu-id="13ee4-158">指定的批註會編譯到字典檔案中。</span><span class="sxs-lookup"><span data-stu-id="13ee4-158">The specified comment is compiled into the dictionary file.</span></span> <span data-ttu-id="13ee4-159">批註必須是單一字串，且不能超過64個字元。</span><span class="sxs-lookup"><span data-stu-id="13ee4-159">The comment must be a single string and no longer than 64 characters.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13ee4-160">-o <dictfile.hwrdict></span><span class="sxs-lookup"><span data-stu-id="13ee4-160">-o <dictfile.hwrdict></span></span></td>
<td><span data-ttu-id="13ee4-161">輸出會寫入指定的檔案名 <dictfile.hwrdict> 。</span><span class="sxs-lookup"><span data-stu-id="13ee4-161">Output is written to the file name specified by <dictfile.hwrdict>.</span></span><br/> <span data-ttu-id="13ee4-162">如果遺漏這個選項，輸出檔名稱就會衍生自原始輸入檔名稱，而輸入副檔名為 hwrdict。</span><span class="sxs-lookup"><span data-stu-id="13ee4-162">If this option is missing, the output file name is derived from the original input file name, with the input file extension replaced by .hwrdict.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a><span data-ttu-id="13ee4-163">Defaults</span><span class="sxs-lookup"><span data-stu-id="13ee4-163">Defaults</span></span>

<span data-ttu-id="13ee4-164">如果未指定任何參數，預設選項值為</span><span class="sxs-lookup"><span data-stu-id="13ee4-164">If no parameters are specified, the default option values are</span></span>

<span data-ttu-id="13ee4-165">-lang <current input language> -類型次要字典</span><span class="sxs-lookup"><span data-stu-id="13ee4-165">-lang <current input language> -type SECONDARY-DICTIONARY</span></span>

### <a name="examples"></a><span data-ttu-id="13ee4-166">範例</span><span class="sxs-lookup"><span data-stu-id="13ee4-166">Examples</span></span>

<span data-ttu-id="13ee4-167">以下會編譯輸入檔 mylist1.txt、套用預設選項值，並建立輸出檔 mylist1. hwrdict。</span><span class="sxs-lookup"><span data-stu-id="13ee4-167">The following compiles the input file mylist1.txt, applies the default option values, and creates the output file mylist1.hwrdict.</span></span>

``` syntax
hwrcomp mylist1.txt
```

<span data-ttu-id="13ee4-168">相反地，下列會將 mylist1.txt 編譯為 myrsrc1. hwrdict，但會將 "英文 (US) " (en-us) 指派為語言和次要字典做為類型。</span><span class="sxs-lookup"><span data-stu-id="13ee4-168">In contrast, the following compiles mylist1.txt into myrsrc1.hwrdict, but assigns "English (US)" (en-US) as the language and SECONDARY-DICTIONARY as the type.</span></span>

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a><span data-ttu-id="13ee4-169">安裝已編譯的自訂字典</span><span class="sxs-lookup"><span data-stu-id="13ee4-169">Installing a Compiled Custom Dictionary</span></span>

<span data-ttu-id="13ee4-170">HwrComp.exe 會建立 hwrdict 檔案，這是可供手寫辨識器使用的二進位格式。</span><span class="sxs-lookup"><span data-stu-id="13ee4-170">HwrComp.exe creates a .hwrdict file, which is in a binary format usable by a handwriting recognizer.</span></span> <span data-ttu-id="13ee4-171">此檔案可以安裝在任何執行 Windows 7 或 Windows Server 2008 R2 且支援手寫辨識的電腦上。</span><span class="sxs-lookup"><span data-stu-id="13ee4-171">This file can be installed on any computer running Windows 7 or Windows Server 2008 R2 that supports handwriting recognition.</span></span> <span data-ttu-id="13ee4-172">只針對目前的使用者或電腦上的所有使用者安裝字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-172">A dictionary is installed either for just the current user or for all users on a machine.</span></span>

<span data-ttu-id="13ee4-173">您可以使用工具 HwrReg.exe，從命令列安裝已編譯的自訂字典檔。</span><span class="sxs-lookup"><span data-stu-id="13ee4-173">A compiled custom dictionary file can be installed from the command line using the tool HwrReg.exe.</span></span> <span data-ttu-id="13ee4-174">如果您想要覆寫一些編譯成檔案或預設值的設定值，這項工具就很有用。</span><span class="sxs-lookup"><span data-stu-id="13ee4-174">This tool is useful if you wish to override some of the configuration values that either are compiled into the file or are the default values.</span></span> <span data-ttu-id="13ee4-175">有兩種方式可以執行 HwrReg.exe：在檢查/安裝模式下，以及在清單/移除模式中。</span><span class="sxs-lookup"><span data-stu-id="13ee4-175">There are two ways to run HwrReg.exe: in check/install mode and in list/remove mode.</span></span>

### <a name="running-hwrregexe-in-checkinstall-mode"></a><span data-ttu-id="13ee4-176">正在檢查/安裝模式中執行 HwrReg.exe</span><span class="sxs-lookup"><span data-stu-id="13ee4-176">Running HwrReg.exe in Check/Install Mode</span></span>

<span data-ttu-id="13ee4-177">此模式適用于尚未安裝的自訂字典檔案。</span><span class="sxs-lookup"><span data-stu-id="13ee4-177">This mode is for custom dictionary files that have not yet been installed.</span></span> <span data-ttu-id="13ee4-178">以下顯示命令列選項的使用語法。</span><span class="sxs-lookup"><span data-stu-id="13ee4-178">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a><span data-ttu-id="13ee4-179">選項的說明</span><span class="sxs-lookup"><span data-stu-id="13ee4-179">Explanation of Options</span></span>



| <span data-ttu-id="13ee4-180">參數</span><span class="sxs-lookup"><span data-stu-id="13ee4-180">Parameter</span></span>                | <span data-ttu-id="13ee4-181">Description</span><span class="sxs-lookup"><span data-stu-id="13ee4-181">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13ee4-182">-檢查</span><span class="sxs-lookup"><span data-stu-id="13ee4-182">-check</span></span>                   | <span data-ttu-id="13ee4-183">字典檔會在未安裝的情況下進行驗證。</span><span class="sxs-lookup"><span data-stu-id="13ee4-183">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="13ee4-184">檢查選項會顯示檔案的批註，以及用來安裝檔案的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="13ee4-184">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="13ee4-185">此選項適用于在執行安裝之前確認註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="13ee4-185">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="13ee4-186">如果遺漏此選項，HwrReg.exe 會安裝自訂字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-186">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span><br/>  |
|  <span data-ttu-id="13ee4-187">lang <localename></span><span class="sxs-lookup"><span data-stu-id="13ee4-187">lang <localename></span></span> | <span data-ttu-id="13ee4-188">字典檔會在未安裝的情況下進行驗證。</span><span class="sxs-lookup"><span data-stu-id="13ee4-188">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="13ee4-189">檢查選項會顯示檔案的批註，以及用來安裝檔案的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="13ee4-189">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="13ee4-190">此選項適用于在執行安裝之前確認註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="13ee4-190">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="13ee4-191">如果遺漏此選項，HwrReg.exe 會安裝自訂字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-191">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span> <br/> |
|  <span data-ttu-id="13ee4-192">範圍 {所有 \| me}</span><span class="sxs-lookup"><span data-stu-id="13ee4-192">scope {all\|me}</span></span>         | <span data-ttu-id="13ee4-193">針對所有使用者安裝自訂字典 ( 範圍所有) 或僅限目前使用者 ( 範圍我) 。</span><span class="sxs-lookup"><span data-stu-id="13ee4-193">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="13ee4-194">使用範圍安裝都需要在提高許可權的命令提示字元中執行命令。否則，將會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="13ee4-194">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="13ee4-195">如果缺少這個選項，則安裝的範圍僅限於目前的使用者。</span><span class="sxs-lookup"><span data-stu-id="13ee4-195">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                          |
|  <span data-ttu-id="13ee4-196">noprompt</span><span class="sxs-lookup"><span data-stu-id="13ee4-196">noprompt</span></span>                | <span data-ttu-id="13ee4-197">HwrReg.exe 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13ee4-197">HwrReg.exe does not prompt for confirmation.</span></span> <span data-ttu-id="13ee4-198">從腳本執行 hwrReg.exe 時，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="13ee4-198">This can be useful when running hwrReg.exe from a script.</span></span> <br/>                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="13ee4-199">下列範例會安裝適用于 language "丹麥文 (丹麥) " (da 深色) 的自訂字典 myrsrc1，其預設範圍僅限於目前的使用者。</span><span class="sxs-lookup"><span data-stu-id="13ee4-199">The following example installs the custom dictionary myrsrc1.hwrdict for language "Danish (Denmark)" (da DK), with the default scope of just the current user.</span></span>

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a><span data-ttu-id="13ee4-200">在清單/移除模式中執行 HwrReg.exe</span><span class="sxs-lookup"><span data-stu-id="13ee4-200">Running HwrReg.exe in List/Remove Mode</span></span>

<span data-ttu-id="13ee4-201">這種模式會列出或移除已安裝的自訂字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-201">This mode either lists or removes installed custom dictionaries.</span></span> <span data-ttu-id="13ee4-202">以下顯示命令列選項的使用語法。</span><span class="sxs-lookup"><span data-stu-id="13ee4-202">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a><span data-ttu-id="13ee4-203">選項的說明</span><span class="sxs-lookup"><span data-stu-id="13ee4-203">Explanation of Options</span></span>



| <span data-ttu-id="13ee4-204">參數</span><span class="sxs-lookup"><span data-stu-id="13ee4-204">Parameter</span></span>                | <span data-ttu-id="13ee4-205">Description</span><span class="sxs-lookup"><span data-stu-id="13ee4-205">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <span data-ttu-id="13ee4-206">lang <localename></span><span class="sxs-lookup"><span data-stu-id="13ee4-206">lang <localename></span></span> | <span data-ttu-id="13ee4-207">只會列出或移除為此地區設定名稱註冊的字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-207">The dictionaries registered for only this locale name are listed or removed.</span></span> <span data-ttu-id="13ee4-208">引數 <localename> 具有表單語言區域。</span><span class="sxs-lookup"><span data-stu-id="13ee4-208">The argument <localename> has the form language REGION.</span></span> <span data-ttu-id="13ee4-209">如需此表單的範例，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。</span><span class="sxs-lookup"><span data-stu-id="13ee4-209">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <br/> <span data-ttu-id="13ee4-210">如果遺漏這個選項，則會列出或移除所有語言的字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-210">If this option is missing, dictionaries for all languages are listed or removed.</span></span><br/> |
|  <span data-ttu-id="13ee4-211">範圍 {所有 \| me}</span><span class="sxs-lookup"><span data-stu-id="13ee4-211">scope {all\|me}</span></span>         | <span data-ttu-id="13ee4-212">針對所有使用者安裝自訂字典 ( 範圍所有) 或僅限目前使用者 ( 範圍我) 。</span><span class="sxs-lookup"><span data-stu-id="13ee4-212">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="13ee4-213">使用範圍安裝都需要在提高許可權的命令提示字元中執行命令。否則，將會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="13ee4-213">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="13ee4-214">如果缺少這個選項，則安裝的範圍僅限於目前的使用者。</span><span class="sxs-lookup"><span data-stu-id="13ee4-214">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                      |
|  <span data-ttu-id="13ee4-215">類型 <type></span><span class="sxs-lookup"><span data-stu-id="13ee4-215">type <type></span></span>       | <span data-ttu-id="13ee4-216">只列出或移除以指定類型註冊的字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-216">Lists or removes only dictionaries that are registered with the specified type.</span></span><br/> <span data-ttu-id="13ee4-217">如果遺漏這個選項，則會列出或移除所有的字典類型。</span><span class="sxs-lookup"><span data-stu-id="13ee4-217">If this option is missing, all dictionary types are listed or removed.</span></span> <span data-ttu-id="13ee4-218">安裝或移除另一種類型的自訂字典 (例如主要 COUNTRYNAME 清單) 可能會影響其他內容中的手寫辨識。</span><span class="sxs-lookup"><span data-stu-id="13ee4-218">Installing or removing a custom dictionary of another type (such as PRIMARY-COUNTRYNAME-LIST) may affect handwriting recognition in other contexts.</span></span> <br/>                                              |
|  <span data-ttu-id="13ee4-219">list</span><span class="sxs-lookup"><span data-stu-id="13ee4-219">list</span></span>                    | <span data-ttu-id="13ee4-220">列出所有符合其他選項的已安裝字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-220">Lists all installed dictionaries that match the other options.</span></span><br/> <span data-ttu-id="13ee4-221">如果遺漏這個選項，則必須指定 [移除] 選項。</span><span class="sxs-lookup"><span data-stu-id="13ee4-221">If this option is missing, the option  remove must be specified.</span></span><br/>                                                                                                                                                                                                                          |
|  <span data-ttu-id="13ee4-222">remove</span><span class="sxs-lookup"><span data-stu-id="13ee4-222">remove</span></span>                  | <span data-ttu-id="13ee4-223">提示移除任何符合其他選項的字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-223">Prompts for removal of any dictionary that matches the other options.</span></span><br/> <span data-ttu-id="13ee4-224">如果遺漏這個選項，則必須指定選項清單。</span><span class="sxs-lookup"><span data-stu-id="13ee4-224">If this option is missing, the option  list must be specified.</span></span><br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="13ee4-225">範例</span><span class="sxs-lookup"><span data-stu-id="13ee4-225">Examples</span></span>

<span data-ttu-id="13ee4-226">以下列出的字典具有 language "英文 (US) " (en-us) 和輸入主要字典，而且只會針對目前的使用者進行安裝。</span><span class="sxs-lookup"><span data-stu-id="13ee4-226">The following lists dictionaries that have language "English (US)" (en US) and type PRIMARY DICTIONARY and that are installed for just the current user.</span></span>

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

<span data-ttu-id="13ee4-227">同樣地，下列程式會移除符合相同準則的字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-227">Similarly, the following removes dictionaries that match the same criteria.</span></span>

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a><span data-ttu-id="13ee4-228">自訂字典的一般注意事項</span><span class="sxs-lookup"><span data-stu-id="13ee4-228">General Notes on Custom Dictionaries</span></span>

-   <span data-ttu-id="13ee4-229">如果您安裝兩個具有相同類型、語言和範圍的自訂字典，則第二個安裝將會覆寫第一個。</span><span class="sxs-lookup"><span data-stu-id="13ee4-229">If you install two custom dictionaries that have the same type, language, and scope, the second installation will overwrite the first.</span></span>
-   <span data-ttu-id="13ee4-230">如果您安裝兩個具有相同類型和語言的自訂字典，但各有不同的範圍 (一個適用于所有使用者，另一個用於目前的使用者) ，則為目前使用者安裝的字典優先，而且會忽略針對所有使用者安裝的字典。</span><span class="sxs-lookup"><span data-stu-id="13ee4-230">If you install two custom dictionaries with the same type and language, but with different scopes (one for all users, and one for the current user), the dictionary installed for the current user takes precedence, and the dictionary installed for all users is ignored.</span></span>

 

