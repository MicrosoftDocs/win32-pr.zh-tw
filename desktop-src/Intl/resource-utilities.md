---
description: 本主題說明用來建立 MUI 應用程式的兩個公用程式。
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: 資源公用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550cf283779a57bc5ca35f88d336646b061c3f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944850"
---
# <a name="resource-utilities"></a><span data-ttu-id="b154c-103">資源公用程式</span><span class="sxs-lookup"><span data-stu-id="b154c-103">Resource Utilities</span></span>

<span data-ttu-id="b154c-104">本主題說明用來建立 MUI 應用程式的兩個公用程式。</span><span class="sxs-lookup"><span data-stu-id="b154c-104">This topic describes two utilities used to build MUI applications.</span></span> <span data-ttu-id="b154c-105">雖然 MUIRCT 是一種 MUI 專屬的工具，但 MUI 也利用標準的 Windows RC 編譯器公用程式。</span><span class="sxs-lookup"><span data-stu-id="b154c-105">While MUIRCT is a MUI-specific tool, MUI also makes use of the standard Windows RC Compiler utility.</span></span> <span data-ttu-id="b154c-106">[當地語系化資源和建立應用程式](localizing-resources-and-building-the-application.md)時，會提供使用這些公用程式的指示。</span><span class="sxs-lookup"><span data-stu-id="b154c-106">Instructions for using these utilities are provided in [Localizing Resources and Building the Application](localizing-resources-and-building-the-application.md).</span></span>

## <a name="muirct-utility"></a><span data-ttu-id="b154c-107">MUIRCT 公用程式</span><span class="sxs-lookup"><span data-stu-id="b154c-107">MUIRCT Utility</span></span>

<span data-ttu-id="b154c-108">MUIRCT (Muirct.exe) 是一種命令列公用程式，可將標準可執行檔分割成 LN 檔和特定語言的 (，也就是可當地語系化的) 資源檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-108">MUIRCT (Muirct.exe) is a command line utility for splitting a standard executable file into an LN file and language-specific (that is, localizable) resource files.</span></span> <span data-ttu-id="b154c-109">每個產生的檔案都包含檔案關聯的資源配置資料。</span><span class="sxs-lookup"><span data-stu-id="b154c-109">Each of the resulting files contains resource configuration data for file association.</span></span> <span data-ttu-id="b154c-110">MUIRCT 包含在 Windows Vista 的 Microsoft Windows SDK 中。</span><span class="sxs-lookup"><span data-stu-id="b154c-110">MUIRCT is included in the Microsoft Windows SDK for Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="b154c-111">從 Windows Vista 開始，Win32 資源載入器會更新以從特定語言的檔案和 LN 檔案載入資源。</span><span class="sxs-lookup"><span data-stu-id="b154c-111">Starting with Windows Vista, the Win32 resource loader is updated to load resources from language-specific files as well as from LN files.</span></span>

 

### <a name="muirct-usages"></a><span data-ttu-id="b154c-112">MUIRCT 使用方式</span><span class="sxs-lookup"><span data-stu-id="b154c-112">MUIRCT Usages</span></span>

1.  <span data-ttu-id="b154c-113">根據 rc 設定檔將二進位檔分割成主要二進位檔和 mui 檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b154c-113">Split binary into main binary and mui file based on rc\_config file.</span></span>

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  <span data-ttu-id="b154c-114">從總和檢查碼檔案中解壓縮總和檢查碼 \_ ，然後將它插入輸出檔中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b154c-114">Extract checksum from checksum\_file and insert it in output\_file.</span></span>

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  <span data-ttu-id="b154c-115">根據總和檢查碼檔案計算總和檢查碼 \_ ，並將它插入輸出檔中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b154c-115">Calculate checksum based on checksum\_file and insert it in output\_file.</span></span>

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  <span data-ttu-id="b154c-116">從輸入檔傾印資源設定資料內容 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b154c-116">Dump resource configuration data contents from input\_file.</span></span>

    `Muirct -d input_file`

### <a name="muirct-syntax"></a><span data-ttu-id="b154c-117">MUIRCT 語法</span><span class="sxs-lookup"><span data-stu-id="b154c-117">MUIRCT Syntax</span></span>

<span data-ttu-id="b154c-118">MUIRCT 可以從命令列參數和（或）使用-q 參數指定的資源設定檔中取得方向。</span><span class="sxs-lookup"><span data-stu-id="b154c-118">MUIRCT can take direction from command line switches and/or from a resource configuration file, specified using the -q switch.</span></span>


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



<span data-ttu-id="b154c-119">**參數和引數**</span><span class="sxs-lookup"><span data-stu-id="b154c-119">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b154c-120">-h |-？</span><span class="sxs-lookup"><span data-stu-id="b154c-120">-h|-?</span></span></td>
<td><span data-ttu-id="b154c-121">顯示說明畫面。</span><span class="sxs-lookup"><span data-stu-id="b154c-121">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b154c-122">-c</span><span class="sxs-lookup"><span data-stu-id="b154c-122">-c</span></span></td>
<td><span data-ttu-id="b154c-123">指定要從中解壓縮或計算資源總和檢查碼的輸入 checksum_file。</span><span class="sxs-lookup"><span data-stu-id="b154c-123">Specifies the input checksum_file from which to extract or calculate the resource checksum.</span></span> <span data-ttu-id="b154c-124">Checksum_file 必須是包含可當地語系化資源的 Win32 二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="b154c-124">Checksum_file must be a Win32 binary file containing localizable resources.</span></span> <span data-ttu-id="b154c-125">如果 checksum_file 包含多個語言的資源，則必須使用-b 參數來指定應使用的是哪一個，否則 MUIRCT 會失敗。</span><span class="sxs-lookup"><span data-stu-id="b154c-125">If checksum_file contains resources for more than one language, the -b switch must be used to specify which of these should be used otherwise MUIRCT fails.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b154c-126">-b</span><span class="sxs-lookup"><span data-stu-id="b154c-126">-b</span></span></td>
<td><span data-ttu-id="b154c-127">指定當以-c 指定的 checksum_file 包含多種語言的資源時，所要使用的語言。</span><span class="sxs-lookup"><span data-stu-id="b154c-127">Specifies the language to be used when the checksum_file specified with -c contains resources in multiple languages.</span></span> <span data-ttu-id="b154c-128">這個參數只能搭配-c 參數使用。</span><span class="sxs-lookup"><span data-stu-id="b154c-128">This switch can only be used in conjunction with the -c switch.</span></span> <span data-ttu-id="b154c-129">語言識別項可以是十進位或十六進位格式。</span><span class="sxs-lookup"><span data-stu-id="b154c-129">The language identifier can be in decimal or hexadecimal format.</span></span> <span data-ttu-id="b154c-130">如果 checksum_file 包含多種語言的資源，但未指定-b，或在 checksum_file 中找不到-b 參數所指定的語言，則 MUIRCT 會失敗。</span><span class="sxs-lookup"><span data-stu-id="b154c-130">MUIRCT fails if the checksum_file contains resources in multiple language and the -b is not specified or if the language specified by the -b switch cannot be found in the checksum_file.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b154c-131">-g</span><span class="sxs-lookup"><span data-stu-id="b154c-131">-g</span></span></td>
<td><span data-ttu-id="b154c-132">在 LN 檔案的資源設定資料區段中，指定要包含為最終回溯語言的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="b154c-132">Specifies the language ID to be included as the ultimate fallback language in the resource configuration data section of the LN file.</span></span> <span data-ttu-id="b154c-133">如果資源載入器無法從執行緒慣用 UI 語言載入要求的 mui 檔，它會使用最終的回溯語言做為最後一次嘗試。</span><span class="sxs-lookup"><span data-stu-id="b154c-133">If the resource loader fails to load a requested .mui file from the thread preferred UI languages, it uses the ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="b154c-134">LangID 值可以指定為十進位或十六進位格式。</span><span class="sxs-lookup"><span data-stu-id="b154c-134">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="b154c-135">例如，英文 (美國) 可由-g 0x409 或-g 1033 指定。</span><span class="sxs-lookup"><span data-stu-id="b154c-135">For example English (United States) can be specified by -g 0x409 or -g 1033.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b154c-136">-Q</span><span class="sxs-lookup"><span data-stu-id="b154c-136">-q</span></span></td>
<td><span data-ttu-id="b154c-137">指定根據 rc_config 檔案配置，將 source_file 分割成 output_LN_file 和 output_MUI_file。</span><span class="sxs-lookup"><span data-stu-id="b154c-137">Specifies that the source_file is to be split into the output_LN_file and the output_MUI_file according to the rc_config file layout.</span></span> <span data-ttu-id="b154c-138">Rc_config 檔案是一種 XML 格式的檔案，可指定要將哪些資源解壓縮至 mui 檔案，而且會保留在 LN 檔案中。</span><span class="sxs-lookup"><span data-stu-id="b154c-138">The rc_config file is an XML formatted file that specifies which resources will be extracted to the .mui file and which will be left in the LN file.</span></span> <span data-ttu-id="b154c-139">Rc_config 可以指定 output_LN_file 和 output_MUI_file 之間的資源類型和個別命名專案的散發。</span><span class="sxs-lookup"><span data-stu-id="b154c-139">The rc_config can specify the distribution of resource types and individual named items between the output_LN_file and output_MUI_file.</span></span> <span data-ttu-id="b154c-140">Source_file 必須是包含單一語言之資源的 Win32 二進位檔，否則 MUIRCT 會失敗。</span><span class="sxs-lookup"><span data-stu-id="b154c-140">The source_file must be a Win32 binary that contains resources in a single language otherwise MUIRCT fails.</span></span> <span data-ttu-id="b154c-141">如果檔案是中性語言，則 MUIRCT 不會分割該檔案，而是以檔案中的語言識別項值0表示。</span><span class="sxs-lookup"><span data-stu-id="b154c-141">MUIRCT does not split the file if it is language neutral which is indicated by having only language ID value 0 in the file.</span></span> <span data-ttu-id="b154c-142">Output_LN_file 和 output_mui_file 是要分割 source_file 的中性語言和 mui 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="b154c-142">The output_LN_file and output_mui_file are the names of the language neutral and .mui file into which the source_file is split.</span></span> <span data-ttu-id="b154c-143">這些檔案名是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="b154c-143">These file names are optional.</span></span> <span data-ttu-id="b154c-144">如果未指定，MUIRCT 會將副檔名 ln 和 mui 附加至 source_file。</span><span class="sxs-lookup"><span data-stu-id="b154c-144">If they are not specified, MUIRCT appends the extensions .ln and .mui to source_file.</span></span> <span data-ttu-id="b154c-145">一般來說，您應該 &quot; 先移除 ln &quot; 副檔名，再部署檔案。</span><span class="sxs-lookup"><span data-stu-id="b154c-145">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span> <span data-ttu-id="b154c-146">MUIRCT 會根據 source_file 名稱和檔案版本來計算總和檢查碼，然後將結果插入每個輸出檔案的資源設定區段，以建立 output_LN_file 和 output_MUI_file 的關聯。</span><span class="sxs-lookup"><span data-stu-id="b154c-146">MUIRCT associates the output_LN_file and output_MUI_file by calculating a checksum based on the source_file name and file version and inserting the result into the resource configuration section of each output file.</span></span> <span data-ttu-id="b154c-147">與-c 參數搭配使用時，-q 參數優先。</span><span class="sxs-lookup"><span data-stu-id="b154c-147">When used in conjunction with the -c switch, the -q switch takes precedence.</span></span> <span data-ttu-id="b154c-148">如果以-q 參數提供的 rc_config 檔案包含總和檢查碼 MUIRCT，則會忽略-c 參數，並將值的總和檢查碼值從 rc_config 檔案插入到 LN 和 mui 檔案。</span><span class="sxs-lookup"><span data-stu-id="b154c-148">If the rc_config file supplied with the -q switch contains a checksum MUIRCT ignores the -c switch and inserts the checksum value from the value, rc_config file into the LN and.mui files.</span></span> <span data-ttu-id="b154c-149">如果在 rc_config 中找不到總和檢查碼值，MUIRCT 會根據-c 參數的行為來計算資源總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="b154c-149">If no checksum value is found in the rc_config, MUIRCT calculates the resource checksum based on the behavior of the -c switch.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b154c-150">-v</span><span class="sxs-lookup"><span data-stu-id="b154c-150">-v</span></span></td>
<td><span data-ttu-id="b154c-151">指定記錄的資訊層級。</span><span class="sxs-lookup"><span data-stu-id="b154c-151">Specifies the level of verboseness for logging.</span></span> <span data-ttu-id="b154c-152">指定1以列印所有基本錯誤訊息和作業結果。</span><span class="sxs-lookup"><span data-stu-id="b154c-152">Specify 1 to print all basic error messages and operation results.</span></span> <span data-ttu-id="b154c-153">指定2，也可以包含包含在 mui 檔和 LN 檔案中的資源資訊 (類型、名稱、語言識別項) 。</span><span class="sxs-lookup"><span data-stu-id="b154c-153">Specify 2 to also include the resource information (type, name, language identifier) included in the .mui file and LN file.</span></span> <span data-ttu-id="b154c-154">預設值為-v 1</span><span class="sxs-lookup"><span data-stu-id="b154c-154">The default is -v 1</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b154c-155">-X</span><span class="sxs-lookup"><span data-stu-id="b154c-155">-x</span></span></td>
<td><span data-ttu-id="b154c-156">指定 MUIRCT 將所有資源類型新增至 mui 檔案的資源區段中的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="b154c-156">Specifies the language ID with which MUIRCT marks all resource types added to the resource section of the .mui file.</span></span> <span data-ttu-id="b154c-157">LangID 值可以指定為十進位或十六進位格式。</span><span class="sxs-lookup"><span data-stu-id="b154c-157">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="b154c-158">例如，英文 (美國) 可由-x 0x409 或-x 1033 指定。</span><span class="sxs-lookup"><span data-stu-id="b154c-158">For example English (United States) can be specified by -x 0x409 or -x 1033.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b154c-159">-E</span><span class="sxs-lookup"><span data-stu-id="b154c-159">-e</span></span></td>
<td><span data-ttu-id="b154c-160">解壓縮隨附于-c 參數的 checksum_file 中的資源總和檢查碼，並將它插入指定的 output_file。</span><span class="sxs-lookup"><span data-stu-id="b154c-160">Extracts the resource checksum contained in the checksum_file provided with the -c switch and inserts it in the specified output_file.</span></span> <span data-ttu-id="b154c-161">當指定-e 時，MUIRCT 會忽略-c 參數以外的所有參數。</span><span class="sxs-lookup"><span data-stu-id="b154c-161">When -e is specified, MUIRCT ignores all switches other than the -c switch.</span></span> <span data-ttu-id="b154c-162">在此情況下，checksum_file 必須是 Win32 二進位檔案，其中包含具有總和檢查碼值的資源設定資料區段。</span><span class="sxs-lookup"><span data-stu-id="b154c-162">In this case the checksum_file must be a Win32 binary file that contains a resource configuration data section with a checksum value.</span></span> <span data-ttu-id="b154c-163">Output_file 必須是現有的 LN 檔或 mui 檔案。</span><span class="sxs-lookup"><span data-stu-id="b154c-163">The output_file must be an existing LN file or .mui file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b154c-164">-Z</span><span class="sxs-lookup"><span data-stu-id="b154c-164">-z</span></span></td>
<td><span data-ttu-id="b154c-165">計算並插入指定輸出檔中的資源總和檢查碼資料。</span><span class="sxs-lookup"><span data-stu-id="b154c-165">Calculates and inserts resource checksum data in the specified output file.</span></span> <span data-ttu-id="b154c-166">MUIRCT 會對-c 參數所提供的輸入和選擇性的-b 參數進行基礎總和檢查碼計算。</span><span class="sxs-lookup"><span data-stu-id="b154c-166">MUIRCT bases checksum calculation on the input provided with the -c switch, and the optional -b switch.</span></span> <span data-ttu-id="b154c-167">如果您指定不存在之-z 參數的輸出檔，MUIRCT 會結束併發生失敗。</span><span class="sxs-lookup"><span data-stu-id="b154c-167">If you specify an output file for the -z switch that does not exist, MUIRCT exits with a failure.</span></span><br/> <span data-ttu-id="b154c-168">範例：根據 Notepad.exe 中的可當地語系化資源來計算總和檢查碼，並將總和檢查碼插入輸出檔 Notepad2.exe。</span><span class="sxs-lookup"><span data-stu-id="b154c-168">Example: Calculates the checksum based on localizable resources in Notepad.exe and inserts the checksum into the output file Notepad2.exe.</span></span><br/> <code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b154c-169">-f</span><span class="sxs-lookup"><span data-stu-id="b154c-169">-f</span></span></td>
<td><span data-ttu-id="b154c-170">建立具有版本資源的 mui 檔案，此檔案是唯一可當地語系化的資源。</span><span class="sxs-lookup"><span data-stu-id="b154c-170">Enables creating a .mui file with the version resource being the only localizable resource.</span></span> <span data-ttu-id="b154c-171">根據預設，MUIRCT 不允許這種情況。</span><span class="sxs-lookup"><span data-stu-id="b154c-171">By default, MUIRCT does not allow this.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b154c-172">-d</span><span class="sxs-lookup"><span data-stu-id="b154c-172">-d</span></span></td>
<td><span data-ttu-id="b154c-173">在原始檔中尋找並顯示內嵌資源設定資料。</span><span class="sxs-lookup"><span data-stu-id="b154c-173">Locates and displays embedded resource configuration data in the source file.</span></span> <span data-ttu-id="b154c-174">當您指定這個參數時，MUIRCT 會忽略所有其他的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="b154c-174">When you specify this switch, MUIRCT ignores all other command line options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b154c-175">-M</span><span class="sxs-lookup"><span data-stu-id="b154c-175">-m</span></span></td>
<td><span data-ttu-id="b154c-176">指定計算與 output_LN_file 和 output_MUI_file 相關聯的總和檢查碼時，所要使用的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="b154c-176">Specifies the version number to use when calculating the checksum for associating the output_LN_file and output_MUI_file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b154c-177">source_filename</span><span class="sxs-lookup"><span data-stu-id="b154c-177">source_filename</span></span></td>
<td><span data-ttu-id="b154c-178">當地語系化二進位原始程式檔的名稱;無法使用萬用字元。</span><span class="sxs-lookup"><span data-stu-id="b154c-178">Name of the localized binary source file; wildcards cannot be used.</span></span> <span data-ttu-id="b154c-179">這個檔案只能包含一種語言的資源。</span><span class="sxs-lookup"><span data-stu-id="b154c-179">This file can only contain resources in one language.</span></span> <span data-ttu-id="b154c-180">如果檔案中有多種語言的資源，除非使用-b 參數，否則 MUIRCT 會失敗。</span><span class="sxs-lookup"><span data-stu-id="b154c-180">If there are resources in multiple languages in the file, MUIRCT fails, unless the -b switch is used.</span></span> <span data-ttu-id="b154c-181">如果檔案包含的資源具有僅具有0值的語言識別項，則 MUIRCT 不會分割檔案，因為語言識別項為0表示中立的語言。</span><span class="sxs-lookup"><span data-stu-id="b154c-181">If the file contains resources with language identifiers having value 0 only, MUIRCT does not split the file because a language identifier of 0 indicates a neutral language.</span></span><br/> <span data-ttu-id="b154c-182">若是-d 參數，source_filename 是 LN 檔或特定語言的資源檔，MUIRCT 會顯示資源設定資料。</span><span class="sxs-lookup"><span data-stu-id="b154c-182">For the -d switch, source_filename is either an LN file or a language-specific resource file for which MUIRCT is to display resource configuration data.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b154c-183">language_neutral_filename</span><span class="sxs-lookup"><span data-stu-id="b154c-183">language_neutral_filename</span></span></td>
<td><span data-ttu-id="b154c-184">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b154c-184">Optional.</span></span> <span data-ttu-id="b154c-185">LN 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="b154c-185">Name of LN file.</span></span> <span data-ttu-id="b154c-186">如果您未指定此檔案的名稱，MUIRCT 會將第二個副檔名附加至 &quot; &quot; 來原始檔案名，以做為非語言相關的檔案名。</span><span class="sxs-lookup"><span data-stu-id="b154c-186">If you do not specify the name of this file, MUIRCT appends a second extension &quot;.ln&quot; to the source file name to use as the language-neutral file name.</span></span> <span data-ttu-id="b154c-187">一般來說，您應該 &quot; 先移除 ln &quot; 副檔名，再部署檔案。</span><span class="sxs-lookup"><span data-stu-id="b154c-187">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b154c-188">LN 檔案不能包含字串或功能表。</span><span class="sxs-lookup"><span data-stu-id="b154c-188">The LN file should not contain strings or menus.</span></span> <span data-ttu-id="b154c-189">您應手動移除它們。</span><span class="sxs-lookup"><span data-stu-id="b154c-189">You should remove them manually.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b154c-190">mui_filename</span><span class="sxs-lookup"><span data-stu-id="b154c-190">mui_filename</span></span></td>
<td><span data-ttu-id="b154c-191">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b154c-191">Optional.</span></span> <span data-ttu-id="b154c-192">特定語言的資源檔名稱。</span><span class="sxs-lookup"><span data-stu-id="b154c-192">Name of language-specific resource file.</span></span> <span data-ttu-id="b154c-193">如果您未指定名稱，MUIRCT 會將第二個副檔名附加至 &quot; &quot; 來原始檔案名，以作為檔案名。一般來說，MUIRCT 會建立特定語言的資源檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-193">If you do not specify a name, MUIRCT appends a second extension &quot;.mui&quot; to the source file name to use as the file name.Normally, MUIRCT creates a language-specific resource file.</span></span> <span data-ttu-id="b154c-194">但是，如果有下列任何一種情況，則不會建立資源檔：</span><span class="sxs-lookup"><span data-stu-id="b154c-194">However, it does not create a resource file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="b154c-195">原始二進位檔案中沒有可當地語系化的資源。</span><span class="sxs-lookup"><span data-stu-id="b154c-195">No localizable resources are in the original binary file.</span></span></li>
<li><span data-ttu-id="b154c-196">在原始二進位檔案中唯一找到的資來源語言是中立的語言。</span><span class="sxs-lookup"><span data-stu-id="b154c-196">The only resource language found in the original binary file is the neutral language.</span></span></li>
<li><span data-ttu-id="b154c-197">原始的二進位檔案具有多個語言的資源，而不會計算中性語言。</span><span class="sxs-lookup"><span data-stu-id="b154c-197">The original binary file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="b154c-198">如果二進位檔案包含兩種語言的資源，而其中一個是中性語言，則公用程式會將檔案視為單一語言，並在有可當地語系化的資源時建立特定語言的資源檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-198">If the binary file contains resources for two languages, and one of them is the neutral language, the utility considers the file to be monolingual and creates a language-specific resource file if there are localizable resources.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="muirct-language-output"></a><span data-ttu-id="b154c-199">MUIRCT 語言輸出</span><span class="sxs-lookup"><span data-stu-id="b154c-199">MUIRCT Language Output</span></span>

<span data-ttu-id="b154c-200">MUIRCT 會根據下列順序（從最高優先順序到最低），選擇要插入 LN 檔案資源設定資料的 "UltimateFallbackLanguage" 屬性值：</span><span class="sxs-lookup"><span data-stu-id="b154c-200">MUIRCT chooses the "UltimateFallbackLanguage" attribute value to insert in the LN file resource configuration data based on the following order, from highest priority to lowest:</span></span>

1.  <span data-ttu-id="b154c-201">來源資源設定檔中的 "UltimateFallbackLanguage" 屬性（如果其中一個是以輸入形式傳遞）。</span><span class="sxs-lookup"><span data-stu-id="b154c-201">"UltimateFallbackLanguage" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="b154c-202">使用-g 參數指定的語言。</span><span class="sxs-lookup"><span data-stu-id="b154c-202">The language specified with the -g switch.</span></span>
3.  <span data-ttu-id="b154c-203">輸入檔語言。</span><span class="sxs-lookup"><span data-stu-id="b154c-203">Input file language.</span></span>

<span data-ttu-id="b154c-204">MUIRCT 會根據下列順序挑選 "language" 屬性值，以在 mui 檔案資源設定資料中插入：</span><span class="sxs-lookup"><span data-stu-id="b154c-204">MUIRCT picks the "language" attribute value to insert in the .mui file resource configuration data based on the following order:</span></span>

1.  <span data-ttu-id="b154c-205">來源資源設定檔中的 "language" 屬性（如果其中一個是以輸入形式傳遞）。</span><span class="sxs-lookup"><span data-stu-id="b154c-205">"language" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="b154c-206">-X 參數所指定的語言 (強制語言) 。</span><span class="sxs-lookup"><span data-stu-id="b154c-206">The language specified by the -x switch (force language).</span></span>
3.  <span data-ttu-id="b154c-207">輸入檔語言。</span><span class="sxs-lookup"><span data-stu-id="b154c-207">Input file language.</span></span>

### <a name="muirct-checksum-handling"></a><span data-ttu-id="b154c-208">MUIRCT 總和檢查碼處理</span><span class="sxs-lookup"><span data-stu-id="b154c-208">MUIRCT Checksum Handling</span></span>

<span data-ttu-id="b154c-209">除非您透過資源設定檔指定總和檢查碼，否則作業系統通常會計算檔案中特定語言資源的總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="b154c-209">The operating system normally calculates the checksum over the language-specific resources in a file unless you specify the checksum through a resource configuration file.</span></span> <span data-ttu-id="b154c-210">只要 LN 檔和所有相關聯的語言特定資源檔的總和檢查碼相同，且 LN 和語言相依的資源設定中的 language 屬性相符，資源載入器就可以成功載入資源。</span><span class="sxs-lookup"><span data-stu-id="b154c-210">As long as the checksum is the same for the LN file and all associated language-specific resource files, and the language attribute in the resource configuration in the LN and language dependent match, the resource loader can successfully load resources.</span></span>

<span data-ttu-id="b154c-211">MUIRCT 支援數個在資源設定資料中放置適當總和檢查碼的方法：</span><span class="sxs-lookup"><span data-stu-id="b154c-211">MUIRCT supports several methods for placing appropriate checksums in the resource configuration data:</span></span>

1.  <span data-ttu-id="b154c-212">為每個語言建立可執行檔，其中包含程式碼和資源。</span><span class="sxs-lookup"><span data-stu-id="b154c-212">Build an executable for each language, containing both code and resources.</span></span> <span data-ttu-id="b154c-213">之後，請使用 MUIRCT 將每個檔案分割成 LN 檔和特定語言的資源檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-213">After this, use MUIRCT to split each of these files into an LN file and a language-specific resource file.</span></span> <span data-ttu-id="b154c-214">MUIRCT 會多次執行，以產生每個語言的資源檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-214">MUIRCT runs multiple times, once to generate a resource file for each language.</span></span> <span data-ttu-id="b154c-215">您可以透過下列方式執行組建：</span><span class="sxs-lookup"><span data-stu-id="b154c-215">You can perform the build in the following ways:</span></span>
    1.  <span data-ttu-id="b154c-216">使用-q 參數來指定資源設定檔中的總和檢查碼值。</span><span class="sxs-lookup"><span data-stu-id="b154c-216">Use the -q switch to specify a checksum value in the resource configuration file.</span></span> <span data-ttu-id="b154c-217">MUIRCT 會將此值放在產生的所有 LN 檔和特定語言的資源檔中。</span><span class="sxs-lookup"><span data-stu-id="b154c-217">MUIRCT places this value in all the LN files and language-specific resource files produced.</span></span> <span data-ttu-id="b154c-218">您必須採用策略來選擇此值，如本主題稍後所述。</span><span class="sxs-lookup"><span data-stu-id="b154c-218">You need to adopt a strategy for choosing this value, as described later in this topic.</span></span>
    2.  <span data-ttu-id="b154c-219">使用-c 參數 (，並選擇性地使用-b 參數) 選擇具有 MUIRCT 從中解壓縮總和檢查碼之資源的單一語言。</span><span class="sxs-lookup"><span data-stu-id="b154c-219">Use the -c switch (and, optionally, the -b switch) to choose a single language having resources from which MUIRCT extracts the checksum.</span></span>
    3.  <span data-ttu-id="b154c-220">使用-z 參數來選擇具有資源的單一語言，MUIRCT 一律從中解壓縮總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="b154c-220">Use the -z switch to choose a single language having resources from which MUIRCT always extracts the checksum.</span></span> <span data-ttu-id="b154c-221">使用其他方法建立檔案之後，請套用此總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="b154c-221">Apply this checksum after the files have been built using other methods.</span></span>
2.  <span data-ttu-id="b154c-222">建立可執行檔，其中包含單一語言的程式碼和資源。</span><span class="sxs-lookup"><span data-stu-id="b154c-222">Build an executable containing both code and resources for a single language.</span></span> <span data-ttu-id="b154c-223">之後，請使用 MUIRCT 來分割 LN 檔和特定語言資源檔之間的資源。</span><span class="sxs-lookup"><span data-stu-id="b154c-223">After this, use MUIRCT to split the resources between the LN file and the language-specific resource file.</span></span> <span data-ttu-id="b154c-224">最後，使用二進位當地語系化工具來修改每個語言產生的資源檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-224">Finally, use a binary localization tool to modify the resulting resource file for each language.</span></span>

<span data-ttu-id="b154c-225">總和檢查碼處理最常見的慣例是以英文 (美國) 資源作為總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="b154c-225">The most common convention for checksum handling is to base the checksum on the English (United States) resources.</span></span> <span data-ttu-id="b154c-226">您可以自由採用不同的慣例，只要每個 LN 檔案都是一致的。</span><span class="sxs-lookup"><span data-stu-id="b154c-226">You are free to adopt a different convention, as long as it is consistent for each LN file.</span></span> <span data-ttu-id="b154c-227">例如，軟體發展企業完全可以接受軟體發展企業將其總和檢查碼以法文 (法國) 資源為基礎，而非英文 (美國) 資源，只要所有的應用程式都有法文 (法國) 的資源，就會以總和檢查碼作為基礎。</span><span class="sxs-lookup"><span data-stu-id="b154c-227">For example, it is perfectly acceptable for a software development enterprise to base its checksums in the software it builds on French (France) resources instead of English (United States) resources, as long as all the applications have French (France) resources on which to base the checksums.</span></span> <span data-ttu-id="b154c-228">您也可以使用資源設定檔，將任意十六進位值（最多16個十六進位數位）指派為總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="b154c-228">It is also acceptable to use the resource configuration file to assign an arbitrary hexadecimal value of up to 16 hexadecimal digits as a checksum.</span></span> <span data-ttu-id="b154c-229">最後一個策略會防止 MUIRCT 的-z、-c 和-b 參數有效使用。</span><span class="sxs-lookup"><span data-stu-id="b154c-229">This last strategy precludes the effective use of the -z, -c, and -b switches of MUIRCT.</span></span> <span data-ttu-id="b154c-230">它需要採用使用 [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) 或其他工具來產生總和檢查碼值的方法。</span><span class="sxs-lookup"><span data-stu-id="b154c-230">It requires adoption of a method using either [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) or some other tool to generate checksum values.</span></span> <span data-ttu-id="b154c-231">此策略也會要求您設定原則，以決定何時要在新增可當地語系化的資源時修改該值。</span><span class="sxs-lookup"><span data-stu-id="b154c-231">This strategy also requires you to set up a policy for determining when to modify the value when adding new localizable resources.</span></span>

<span data-ttu-id="b154c-232">若要將英文 (美國) 總和檢查碼套用至所有檔案，您可以使用上述任何一種總和檢查碼處理方法。</span><span class="sxs-lookup"><span data-stu-id="b154c-232">To apply the English (United States) checksum to all files, you can use any of the checksum handling methods described above.</span></span> <span data-ttu-id="b154c-233">例如，您可以針對英文 (的美國) 產生 LN 檔案和特定語言的資源檔，然後使用 MUIRCT-d 參數來取得產生的總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="b154c-233">For example, you can generate the LN file and language-specific resource file for English (United States), then use the MUIRCT -d switch to obtain the resulting checksum.</span></span> <span data-ttu-id="b154c-234">您可以將此總和檢查碼複製到資源設定檔中，並搭配使用-q 參數與 MUIRCT，將總和檢查碼套用至所有其他檔案。</span><span class="sxs-lookup"><span data-stu-id="b154c-234">You can copy this checksum into your resource configuration file and use the -q switch with MUIRCT to apply the checksum to all other files.</span></span>

### <a name="use-of-a-resource-configuration-file-with-muirct"></a><span data-ttu-id="b154c-235">使用資源設定檔搭配 MUIRCT</span><span class="sxs-lookup"><span data-stu-id="b154c-235">Use of a Resource Configuration File with MUIRCT</span></span>

<span data-ttu-id="b154c-236">使用 MUIRCT 時，您可以指定資源設定資料。</span><span class="sxs-lookup"><span data-stu-id="b154c-236">You can specify resource configuration data when using MUIRCT.</span></span> <span data-ttu-id="b154c-237">無論您是否明確提供資源設定檔，每個特定語言的資源檔都有資源設定資料，如同任何含有相關聯資源檔的 LN 檔案一樣。</span><span class="sxs-lookup"><span data-stu-id="b154c-237">Whether or not you explicitly supply a resource configuration file, every language-specific resource file has resource configuration data, as does any LN file with an associated resource file.</span></span> <span data-ttu-id="b154c-238">例如：</span><span class="sxs-lookup"><span data-stu-id="b154c-238">For example:</span></span>

-   <span data-ttu-id="b154c-239">如果您使用-q 參數來指定資源設定檔，但您的輸入來源檔案中沒有可當地語系化的資源，則不會產生特定語言的資源檔，而產生的 LN 檔案不會包含資源設定資料。</span><span class="sxs-lookup"><span data-stu-id="b154c-239">If you use the -q switch to specify a resource configuration file, but there are no localizable resources in your input source file, no language-specific resource file is generated and the resulting LN file does not contain resource configuration data.</span></span> <span data-ttu-id="b154c-240">此外，如果輸入來源檔案有多語系資源，則 MUIRCT 不會將檔案分割。</span><span class="sxs-lookup"><span data-stu-id="b154c-240">Also, if the input source file has multilingual resources, then MUIRCT won't split the file.</span></span>

> [!Note]  
> <span data-ttu-id="b154c-241">目前，當資源設定檔的 neutralResources 元素未包含 resourceType 元素，而且 localizedResources 元素包含字串和功能表時，MUIRCT 的行為不一致。</span><span class="sxs-lookup"><span data-stu-id="b154c-241">Currently the behavior of MUIRCT is inconsistent when the neutralResources element of the resource configuration file contains no resourceType elements and the localizedResources element contains strings and menus, for example.</span></span> <span data-ttu-id="b154c-242">在這種情況下，MUIRCT 會分割資源，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b154c-242">In such a case, MUIRCT splits the resources as follows:</span></span>
>
> -   <span data-ttu-id="b154c-243">原始二進位檔 (中的所有資源（包括字串和功能表) ，加上 MUI 資源）都會放置在 LN 檔案中。</span><span class="sxs-lookup"><span data-stu-id="b154c-243">All resources in the original binary (including strings and menus), plus the MUI resources, are placed in the LN file.</span></span>
> -   <span data-ttu-id="b154c-244">字串、功能表和 MUI 資源會放在適當的語言特定資源檔中。</span><span class="sxs-lookup"><span data-stu-id="b154c-244">Strings, menus, and MUI resources are placed in the appropriate language-specific resource file.</span></span>

 

### <a name="examples-for-using-muirct"></a><span data-ttu-id="b154c-245">使用 MUIRCT 的範例</span><span class="sxs-lookup"><span data-stu-id="b154c-245">Examples for Using MUIRCT</span></span>

<span data-ttu-id="b154c-246">**標準使用量範例**</span><span class="sxs-lookup"><span data-stu-id="b154c-246">**Examples of Standard Usage**</span></span>


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



<span data-ttu-id="b154c-247">**使用-d 參數輸出 LN 檔案的範例**</span><span class="sxs-lookup"><span data-stu-id="b154c-247">**Example of LN File Output Using -d Switch**</span></span>

<span data-ttu-id="b154c-248">以下範例是使用-d 參數搭配 MUIRCT，從 LN 檔案 Shell32.dll 的資源設定資料輸出：</span><span class="sxs-lookup"><span data-stu-id="b154c-248">Here is an example of the resource configuration data output from an LN file, Shell32.dll, using the -d switch with MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



<span data-ttu-id="b154c-249">**使用-d 參數 Language-Specific 資源檔輸出的範例**</span><span class="sxs-lookup"><span data-stu-id="b154c-249">**Example of Language-Specific Resource File Output Using -d Switch**</span></span>

<span data-ttu-id="b154c-250">以下範例是使用 MUIRCT 的-d 參數，從 mui 檔案（Shell32.dll mui）的資源設定資料輸出：</span><span class="sxs-lookup"><span data-stu-id="b154c-250">Here is an example of the resource configuration data output from a .mui file, Shell32.dll.mui, using the -d switch for MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a><span data-ttu-id="b154c-251">RC 編譯器公用程式</span><span class="sxs-lookup"><span data-stu-id="b154c-251">RC Compiler Utility</span></span>

<span data-ttu-id="b154c-252">RC 編譯器 (Rc.exe) 是一種命令列公用程式，可將資源定義腳本檔案（ ( .rc) 延伸模組）編譯為 ( 的資源檔) .res 延伸。</span><span class="sxs-lookup"><span data-stu-id="b154c-252">RC Compiler (Rc.exe) is a command line utility for compiling a resource definition script file (.rc extension) into resource files (.res extension).</span></span> <span data-ttu-id="b154c-253">RC 編譯器包含在 Windows SDK 中。</span><span class="sxs-lookup"><span data-stu-id="b154c-253">RC Compiler is included in the Windows SDK.</span></span> <span data-ttu-id="b154c-254">本檔僅說明如何搭配使用 RC 編譯器與資源載入器的 MUI 相關功能。</span><span class="sxs-lookup"><span data-stu-id="b154c-254">This document only explains the use of RC Compiler with MUI-related capabilities of the resource loader.</span></span> <span data-ttu-id="b154c-255">如需編譯器的完整資訊，請參閱 [關於資源檔](../menurc/about-resource-files.md)。</span><span class="sxs-lookup"><span data-stu-id="b154c-255">For complete information about the compiler, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="b154c-256">RC 編譯器可讓您從一組來源、LN 檔和個別的特定語言資源檔建立。</span><span class="sxs-lookup"><span data-stu-id="b154c-256">RC Compiler allows you to build, from a single set of sources, an LN file and a separate language-specific resource file.</span></span> <span data-ttu-id="b154c-257">針對 MUIRCT，檔案會與資源設定資料相關聯。</span><span class="sxs-lookup"><span data-stu-id="b154c-257">As for MUIRCT, the files are associated by resource configuration data.</span></span>

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a><span data-ttu-id="b154c-258">用於 MUI 資源的 RC 編譯器語法</span><span class="sxs-lookup"><span data-stu-id="b154c-258">RC Compiler Syntax as Used for MUI Resources</span></span>

<span data-ttu-id="b154c-259">RC 編譯器參數在 [使用 rc](../menurc/using-rc-the-rc-command-line-.md)中有詳細的定義。</span><span class="sxs-lookup"><span data-stu-id="b154c-259">RC Compiler switches are defined in detail in [Using RC](../menurc/using-rc-the-rc-command-line-.md).</span></span> <span data-ttu-id="b154c-260">本節只會定義用來建立 MUI 資源的參數。</span><span class="sxs-lookup"><span data-stu-id="b154c-260">This section only defines the switches used to build MUI resources.</span></span> <span data-ttu-id="b154c-261">請記住，每個參數都不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b154c-261">Remember that each switch is case-insensitive.</span></span> <span data-ttu-id="b154c-262">除非另有指示，否則資源類型會假設為非語言相關。</span><span class="sxs-lookup"><span data-stu-id="b154c-262">Resource types are assumed to be language-neutral unless otherwise indicated.</span></span>


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



<span data-ttu-id="b154c-263">**參數和引數**</span><span class="sxs-lookup"><span data-stu-id="b154c-263">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b154c-264">-h |-？</span><span class="sxs-lookup"><span data-stu-id="b154c-264">-h|-?</span></span></td>
<td><span data-ttu-id="b154c-265">顯示說明畫面。</span><span class="sxs-lookup"><span data-stu-id="b154c-265">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b154c-266">-fm</span><span class="sxs-lookup"><span data-stu-id="b154c-266">-fm</span></span></td>
<td><span data-ttu-id="b154c-267">針對特定語言的資源使用指定的資源檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-267">Uses the specified resource file for language-specific resources.</span></span> <span data-ttu-id="b154c-268">資源編譯器通常會建立特定語言的資源檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-268">Normally the resource compiler creates a language-specific resource file.</span></span> <span data-ttu-id="b154c-269">但是，如果有下列任何一種情況，則不會建立檔案：</span><span class="sxs-lookup"><span data-stu-id="b154c-269">However, it does not create the file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="b154c-270">.Rc 檔中沒有可當地語系化的資源。</span><span class="sxs-lookup"><span data-stu-id="b154c-270">There are no localizable resources in the .rc file.</span></span></li>
<li><span data-ttu-id="b154c-271">.Rc 檔中唯一找到的資來源語言是中性語言。</span><span class="sxs-lookup"><span data-stu-id="b154c-271">The only resource language found in the .rc file is the neutral language.</span></span></li>
<li><span data-ttu-id="b154c-272">.Rc 檔案有多個語言的資源，不會計算中性語言。</span><span class="sxs-lookup"><span data-stu-id="b154c-272">The .rc file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="b154c-273">如果 .rc 檔包含兩種語言的資源，其中一個是中性語言，則編譯器會將檔案視為單一語言。</span><span class="sxs-lookup"><span data-stu-id="b154c-273">If the .rc file contains resources for two languages, and one of them is the neutral language, the compiler considers the file to be monolingual.</span></span> <span data-ttu-id="b154c-274">如果有任何可當地語系化的資源，編譯器會建立特定語言的資源檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-274">If there are any localizable resources, the compiler creates a language-specific resource file.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b154c-275">-Q</span><span class="sxs-lookup"><span data-stu-id="b154c-275">-q</span></span></td>
<td><span data-ttu-id="b154c-276">使用指定的資源設定檔來取得要放在特定語言資源檔和 LN 檔案中的資源類型。</span><span class="sxs-lookup"><span data-stu-id="b154c-276">Uses the specified resource configuration file to obtain the resource types to place in the language-specific resource file and the LN file.</span></span> <span data-ttu-id="b154c-277">如需詳細資訊，請參閱 <a href="preparing-a-resource-configuration-file.md">準備資源設定檔</a>。</span><span class="sxs-lookup"><span data-stu-id="b154c-277">For more information, see <a href="preparing-a-resource-configuration-file.md">Preparing a Resource Configuration File</a>.</span></span> <span data-ttu-id="b154c-278">除了此參數之外，您還可以使用-j 和-k 參數，但最好是使用資源設定檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-278">As an alternative to this switch, you can use the -j and -k switches, but it is preferred to use a resource configuration file.</span></span> <br/> <span data-ttu-id="b154c-279">藉由搭配使用-q 參數與資源設定檔，您可以執行以專案為基礎的分割，並提供最後會在 LN 和語言特定資源檔中使用二進位資源設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="b154c-279">By using the -q switch with a resource configuration file, you can implement an item-based split and provide attributes that will end up with the binary resource configuration in the LN and language-specific resource file.</span></span> <span data-ttu-id="b154c-280">使用-j 和-k 參數無法進行分割。</span><span class="sxs-lookup"><span data-stu-id="b154c-280">This split is not possible using the -j and -k switches.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b154c-281">如果您將資源和版本資訊儲存在不同的資源設定檔中，RC 編譯器分割進程就無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b154c-281">The RC Compiler split process does not work properly if you store resources and version information in different resource configuration files.</span></span> <span data-ttu-id="b154c-282">在此情況下，RC 編譯器不會分割版本資訊。</span><span class="sxs-lookup"><span data-stu-id="b154c-282">In this case, RC Compiler does not split the version information.</span></span> <span data-ttu-id="b154c-283">因此，連結特定語言的資源檔時，會發生連結器錯誤，因為該檔案沒有版本資源。</span><span class="sxs-lookup"><span data-stu-id="b154c-283">Therefore a linker error occurs during linking of the language-specific resource file because the file does not have version resources.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b154c-284">-g</span><span class="sxs-lookup"><span data-stu-id="b154c-284">-g</span></span></td>
<td><span data-ttu-id="b154c-285">指定十六進位的最終回溯 <a href="language-identifiers.md">語言</a> 識別碼。</span><span class="sxs-lookup"><span data-stu-id="b154c-285">Specifies the ultimate <a href="language-identifiers.md">fallback language</a> identifier in hexadecimal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b154c-286">-g1</span><span class="sxs-lookup"><span data-stu-id="b154c-286">-g1</span></span></td>
<td><span data-ttu-id="b154c-287">即使版本資源是唯一可當地語系化的內容，也會建立 MUI 檔案。</span><span class="sxs-lookup"><span data-stu-id="b154c-287">Creates a MUI .res file even if the VERSION resource is the only localizable content.</span></span> <span data-ttu-id="b154c-288">根據預設，如果版本是唯一可當地語系化的資源，RC 編譯器就不會產生 .res 檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-288">By default, RC Compiler does not produce a .res file if VERSION is the only localizable resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b154c-289">-g2</span><span class="sxs-lookup"><span data-stu-id="b154c-289">-g2</span></span></td>
<td><span data-ttu-id="b154c-290">指定在計算總和檢查碼時要使用的自訂版本號碼。</span><span class="sxs-lookup"><span data-stu-id="b154c-290">Specifies the custom version number to use when calculating the checksum.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b154c-291">mui_res_name</span><span class="sxs-lookup"><span data-stu-id="b154c-291">mui_res_name</span></span></td>
<td><span data-ttu-id="b154c-292">特定語言資源的資源檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-292">Resource file for language-specific resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b154c-293">rc_config_file_name</span><span class="sxs-lookup"><span data-stu-id="b154c-293">rc_config_file_name</span></span></td>
<td><span data-ttu-id="b154c-294">資源設定檔案。</span><span class="sxs-lookup"><span data-stu-id="b154c-294">Resource configuration file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b154c-295">langid</span><span class="sxs-lookup"><span data-stu-id="b154c-295">langid</span></span></td>
<td><span data-ttu-id="b154c-296">語言識別項。</span><span class="sxs-lookup"><span data-stu-id="b154c-296">Language identifier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b154c-297">version</span><span class="sxs-lookup"><span data-stu-id="b154c-297">version</span></span></td>
<td><span data-ttu-id="b154c-298">自訂版本號碼，格式為 &quot; 6.2.0.0 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="b154c-298">Custom version number, in a format such as &quot;6.2.0.0&quot;.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a><span data-ttu-id="b154c-299">使用 RC 編譯器建立 MUI 資源的範例</span><span class="sxs-lookup"><span data-stu-id="b154c-299">Example for Using RC Compiler to Build MUI Resources</span></span>

<span data-ttu-id="b154c-300">為了說明使用 MUI 資源的 RC 編譯器操作，讓我們檢查下列命令列，以取得資源檔 Myfile.txt .rc：</span><span class="sxs-lookup"><span data-stu-id="b154c-300">To illustrate RC Compiler operation with MUI resources, let's examine the following command line, for the resource file Myfile.rc:</span></span>


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



<span data-ttu-id="b154c-301">此命令列會導致 RC 編譯器執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="b154c-301">This command line causes RC Compiler to do the following:</span></span>

-   <span data-ttu-id="b154c-302">根據 .rc 檔的名稱，建立預設為 Myfile.txt 的語言專屬資源檔 Myfile.txt \_ .res 和非語言相關資源檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-302">Create the language-specific resource file Myfile\_res.res and a language-neutral resource file that defaults to Myfile.res, based on the name of the .rc file.</span></span>
-   <span data-ttu-id="b154c-303">將 2 (專案 5 6 7 8 9 10 11 12) 、4、5、6、9、11、16、23、240、1024我 \_ 的類型資源類型新增至特定語言的 .res 檔案（如果它們位於 .rc 檔中）。</span><span class="sxs-lookup"><span data-stu-id="b154c-303">Add the 2 (item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY\_TYPE resource types to the language-specific .res file if they are in the .rc file.</span></span>
-   <span data-ttu-id="b154c-304">將資源類型16（以及資源檔中所述的任何其他資源類型）新增至語言中性 .res 檔和語言特定 .res 檔。</span><span class="sxs-lookup"><span data-stu-id="b154c-304">Add resource type 16, along with any other resource types described in the resource file to the language-neutral .res file and to the language-specific .res file.</span></span> <span data-ttu-id="b154c-305">請注意，在此範例中，會在兩個位置加入資源類型16。</span><span class="sxs-lookup"><span data-stu-id="b154c-305">Note that, in this example, resource type 16 is being added in two places.</span></span>
-   <span data-ttu-id="b154c-306">選擇 "UltimateFallbackLanguage" 屬性值，根據下列準則（從最高優先順序到最低順序）來插入 LN 檔案資源設定資料：</span><span class="sxs-lookup"><span data-stu-id="b154c-306">Choose the "UltimateFallbackLanguage" attribute value to insert into the LN file resource configuration data based on the following criteria, ordered from highest priority to lowest:</span></span>
    -   <span data-ttu-id="b154c-307">資源設定檔中的 "UltimateFallbackLanguage" 屬性（如果其中一個是以輸入形式傳遞）。</span><span class="sxs-lookup"><span data-stu-id="b154c-307">"UltimateFallbackLanguage" attribute in the resource configuration file if one is passed in as input.</span></span>
    -   <span data-ttu-id="b154c-308">要根據 RC 編譯器語言順序插入資源設定資料的語言屬性值， (非語言相關和特定語言的資源檔語言) 。</span><span class="sxs-lookup"><span data-stu-id="b154c-308">Language attribute value to insert in the resource configuration data based on the RC Compiler language order (language-neutral and language-specific resource file language).</span></span> <span data-ttu-id="b154c-309">考慮事項包括 .rc 檔中的語言、-gl 參數的語言值，以及英文 (美國) 的識別碼0x0409。</span><span class="sxs-lookup"><span data-stu-id="b154c-309">Considerations include language in the .rc file, language value of the -gl switch, and identifier 0x0409 for English (United States).</span></span>

## <a name="remarks"></a><span data-ttu-id="b154c-310">備註</span><span class="sxs-lookup"><span data-stu-id="b154c-310">Remarks</span></span>

<span data-ttu-id="b154c-311">如果您在 neutralResources 元素中包含任何圖示 (3) 、對話方塊 (5) 、字串 (6) 或版本 (16) 資源類型，則您必須在資源設定檔的 localizedResources 元素中複製該專案。</span><span class="sxs-lookup"><span data-stu-id="b154c-311">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element in the resource configuration file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b154c-312">相關主題</span><span class="sxs-lookup"><span data-stu-id="b154c-312">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b154c-313">多語系消費者介面參考</span><span class="sxs-lookup"><span data-stu-id="b154c-313">Multilingual User Interface Reference</span></span>](multilingual-user-interface-reference.md)
</dt> <dt>

[<span data-ttu-id="b154c-314">MUI 資源管理</span><span class="sxs-lookup"><span data-stu-id="b154c-314">MUI Resource Management</span></span>](mui-resource-management.md)
</dt> <dt>

[<span data-ttu-id="b154c-315">當地語系化資源和建立應用程式</span><span class="sxs-lookup"><span data-stu-id="b154c-315">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
