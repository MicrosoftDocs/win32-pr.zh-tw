---
description: WsdCodeGen 有兩個函式：產生設定檔，以及產生 WSDAPI 用戶端和主機應用程式的原始程式碼。
ms.assetid: 75f5071c-040b-4e65-a80e-e1fea63535b0
title: WsdCodeGen 命令列語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7db3afe9b13286833f8563c0cacb41919d77bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848607"
---
# <a name="wsdcodegen-command-line-syntax"></a><span data-ttu-id="59253-103">WsdCodeGen 命令列語法</span><span class="sxs-lookup"><span data-stu-id="59253-103">WsdCodeGen Command Line Syntax</span></span>

<span data-ttu-id="59253-104">WsdCodeGen 有兩個函式：產生設定檔，以及產生 WSDAPI 用戶端和主機應用程式的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="59253-104">WsdCodeGen has two functions: generating configuration files and generating source code for WSDAPI client and host applications.</span></span> <span data-ttu-id="59253-105">本主題提供用來執行每項工作的命令列語法。</span><span class="sxs-lookup"><span data-stu-id="59253-105">This topic gives the command line syntax used to perform each task.</span></span>

## <a name="generating-a-configuration-file"></a><span data-ttu-id="59253-106">產生設定檔</span><span class="sxs-lookup"><span data-stu-id="59253-106">Generating a Configuration File</span></span>

### <a name="syntax"></a><span data-ttu-id="59253-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="59253-107">Syntax</span></span>

<span data-ttu-id="59253-108">**WSDCODEGEN.EXE** **/generateconfig：**{**client** \| **host** \| **all**} **\[ /outputfile：**_ConfigFileName_ *_\]_* *WSDLFileNameList*</span><span class="sxs-lookup"><span data-stu-id="59253-108">**WSDCODEGEN.EXE** **/generateconfig:**{**client**\|**host**\|**all**} **\[/outputfile:**_ConfigFileName_*_\]_* *WSDLFileNameList*</span></span>

### <a name="parameters"></a><span data-ttu-id="59253-109">參數</span><span class="sxs-lookup"><span data-stu-id="59253-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59253-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig： {client \| host \| all}**</span><span class="sxs-lookup"><span data-stu-id="59253-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig:{client \| host \| all}**</span></span>
</dt> <dd>

<span data-ttu-id="59253-111">輸出設定檔將產生的程式碼類型。</span><span class="sxs-lookup"><span data-stu-id="59253-111">The type of code that the output configuration file will generate.</span></span> <span data-ttu-id="59253-112">**/generateconfig：用戶端** 用來產生用來產生用戶端程式代碼的設定檔， **/generateconfig：主機** 可用來產生用來產生主機程式碼的設定檔，而 **/generateconfig： all** 用來產生設定檔，以產生用戶端和主機程式碼。</span><span class="sxs-lookup"><span data-stu-id="59253-112">**/generateconfig:client** is used to generate a configuration file for generating client code, **/generateconfig:host** is used to generate a configuration file for generating host code, and **/generateconfig:all** is used to generate a configuration file for generating both client and host code.</span></span>

</dd> <dt>

<span data-ttu-id="59253-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/outputfile：**_ConfigFileName_</span><span class="sxs-lookup"><span data-stu-id="59253-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/outputfile:**_ConfigFileName_</span></span>
</dt> <dd>

<span data-ttu-id="59253-114">這個選擇性參數是用來指定輸出設定檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="59253-114">This optional parameter is used to specify the file name of the output configuration file.</span></span> <span data-ttu-id="59253-115">如果排除此參數，則會 codegen.config 輸出設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="59253-115">If this parameter is excluded, the name of the output configuration file is codegen.config.</span></span>

</dd> <dt>

<span data-ttu-id="59253-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span><span class="sxs-lookup"><span data-stu-id="59253-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span></span>
</dt> <dd>

<span data-ttu-id="59253-117">在設定檔中包含 Pnp-x 範本。</span><span class="sxs-lookup"><span data-stu-id="59253-117">Include a PnP-X template in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="59253-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*</span><span class="sxs-lookup"><span data-stu-id="59253-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*</span></span>
</dt> <dd>

<span data-ttu-id="59253-119">以空格分隔的 WSDL 檔案清單， (s) 要由 WsdCodeGen 處理。</span><span class="sxs-lookup"><span data-stu-id="59253-119">A space-delimited list of the WSDL file(s) to be processed by WsdCodeGen.</span></span>

</dd> </dl>

## <a name="generating-source-code"></a><span data-ttu-id="59253-120">產生原始程式碼</span><span class="sxs-lookup"><span data-stu-id="59253-120">Generating Source Code</span></span>

### <a name="syntax"></a><span data-ttu-id="59253-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="59253-121">Syntax</span></span>

<span data-ttu-id="59253-122">**WSDCODEGEN.EXE** **/generatecode** **\[ /download \]** **\[ /gbc \]** **\[ outputroot：**_path_ *_\]_* **\[ /writeaccess：**_command_ *_\]_* *ConfigFileName*</span><span class="sxs-lookup"><span data-stu-id="59253-122">**WSDCODEGEN.EXE** **/generatecode** **\[/download\]** **\[/gbc\]** **\[outputroot:**_path_*_\]_* **\[/writeaccess:**_command_*_\]_* *ConfigFileName*</span></span>

### <a name="parameters"></a><span data-ttu-id="59253-123">參數</span><span class="sxs-lookup"><span data-stu-id="59253-123">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59253-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span><span class="sxs-lookup"><span data-stu-id="59253-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span></span>
</dt> <dd>

<span data-ttu-id="59253-125">指示 WsdCodeGen 產生原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="59253-125">Directs WsdCodeGen to generate source code.</span></span> <span data-ttu-id="59253-126">如果未指定任何模式，這就是預設模式。</span><span class="sxs-lookup"><span data-stu-id="59253-126">This is the default mode if no mode is specified.</span></span>

</dd> <dt>

<span data-ttu-id="59253-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/download**</span><span class="sxs-lookup"><span data-stu-id="59253-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/download**</span></span>
</dt> <dd>

<span data-ttu-id="59253-128">下載設定檔所參考的匯入檔。</span><span class="sxs-lookup"><span data-stu-id="59253-128">Downloads imported documents referenced by the configuration file.</span></span> <span data-ttu-id="59253-129">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="59253-129">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="59253-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span><span class="sxs-lookup"><span data-stu-id="59253-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span></span>
</dt> <dd>

<span data-ttu-id="59253-131">將批註新增至表示產生程式碼的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="59253-131">Adds comments to the source code that indicates the code was generated.</span></span> <span data-ttu-id="59253-132">這些批註前面會加上「產生者」片語。</span><span class="sxs-lookup"><span data-stu-id="59253-132">These comments are prefixed with the phrase "Generated by".</span></span> <span data-ttu-id="59253-133">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="59253-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="59253-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot：**_path_</span><span class="sxs-lookup"><span data-stu-id="59253-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_path_</span></span>
</dt> <dd>

<span data-ttu-id="59253-135">所產生檔案的輸出位置。</span><span class="sxs-lookup"><span data-stu-id="59253-135">The output location for generated files.</span></span> <span data-ttu-id="59253-136">*路徑* 可以是絕對或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="59253-136">*path* can be an absolute or relative path.</span></span> <span data-ttu-id="59253-137">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="59253-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="59253-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess：**_命令_</span><span class="sxs-lookup"><span data-stu-id="59253-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess:**_command_</span></span>
</dt> <dd>

<span data-ttu-id="59253-139">指示 WsdCodeGen 在修改磁片上的任何現有檔案之前，執行指定的命令。</span><span class="sxs-lookup"><span data-stu-id="59253-139">Directs WsdCodeGen to execute the specified command before it modifies any existing files on disk.</span></span> <span data-ttu-id="59253-140">與磁片上相同的輸出檔案不會收到此命令，也不會寫入這些檔案。</span><span class="sxs-lookup"><span data-stu-id="59253-140">Output files that are identical to those on disk will not receive this command, nor will they be written to.</span></span> <span data-ttu-id="59253-141">如果命令包含序列 " {0} "，此序列將會取代為要修改的檔案名。</span><span class="sxs-lookup"><span data-stu-id="59253-141">If the command contains the sequence "{0}", this sequence will be replaced with the filename of the file to be modified.</span></span> <span data-ttu-id="59253-142">如果沒有，則會將檔案名附加至命令。</span><span class="sxs-lookup"><span data-stu-id="59253-142">If not, the filename will be appended to the command.</span></span>

<span data-ttu-id="59253-143">範例：</span><span class="sxs-lookup"><span data-stu-id="59253-143">Examples:</span></span>

<span data-ttu-id="59253-144">**/writeaccess： "attrib-r"**</span><span class="sxs-lookup"><span data-stu-id="59253-144">**/writeaccess:"attrib -r"**</span></span>

<span data-ttu-id="59253-145">**/writeaccess： "attrib-r {0} "**</span><span class="sxs-lookup"><span data-stu-id="59253-145">**/writeaccess:"attrib -r {0}"**</span></span>

<span data-ttu-id="59253-146">**/writeaccess： "copy {0} ... \\備份 \\ 」**</span><span class="sxs-lookup"><span data-stu-id="59253-146">**/writeaccess:"copy {0} ..\\backup\\"**</span></span>

</dd> <dt>

<span data-ttu-id="59253-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*ConfigFileName*</span><span class="sxs-lookup"><span data-stu-id="59253-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*ConfigFileName*</span></span>
</dt> <dd>

<span data-ttu-id="59253-148">產生程式碼之前要處理的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="59253-148">The name of the configuration file to process before generating code.</span></span>

</dd> </dl>

## <a name="formatting-legend"></a><span data-ttu-id="59253-149">格式圖例</span><span class="sxs-lookup"><span data-stu-id="59253-149">Formatting Legend</span></span>



| <span data-ttu-id="59253-150">格式</span><span class="sxs-lookup"><span data-stu-id="59253-150">Format</span></span>                                                                    | <span data-ttu-id="59253-151">意義</span><span class="sxs-lookup"><span data-stu-id="59253-151">Meaning</span></span>                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="59253-152">*斜體*</span><span class="sxs-lookup"><span data-stu-id="59253-152">*Italic*</span></span>                                                                  | <span data-ttu-id="59253-153">使用者必須提供的資訊</span><span class="sxs-lookup"><span data-stu-id="59253-153">Information that the user must provide</span></span>                  |
| <span data-ttu-id="59253-154">**粗體字**</span><span class="sxs-lookup"><span data-stu-id="59253-154">**Bold**</span></span>                                                                  | <span data-ttu-id="59253-155">使用者必須依照顯示的方式鍵入的元素</span><span class="sxs-lookup"><span data-stu-id="59253-155">Elements that the user must type exactly as shown</span></span>       |
| <span data-ttu-id="59253-156">介於括弧之間 (\[ \]) </span><span class="sxs-lookup"><span data-stu-id="59253-156">Between brackets (\[\])</span></span>                                                   | <span data-ttu-id="59253-157">選擇性項目</span><span class="sxs-lookup"><span data-stu-id="59253-157">Optional items</span></span>                                          |
| <span data-ttu-id="59253-158">介於大括弧 ({}) ; 以管道 () 分隔的選項 \| 。</span><span class="sxs-lookup"><span data-stu-id="59253-158">Between braces ({}); choices separated by pipe (\|).</span></span> <span data-ttu-id="59253-159">範例： {偶數 \| 奇數}</span><span class="sxs-lookup"><span data-stu-id="59253-159">Example: {even\|odd}</span></span> | <span data-ttu-id="59253-160">使用者必須從中選擇一項的選項集</span><span class="sxs-lookup"><span data-stu-id="59253-160">Set of choices from which the user must choose only one</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="59253-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="59253-161">Requirements</span></span>



| <span data-ttu-id="59253-162">需求</span><span class="sxs-lookup"><span data-stu-id="59253-162">Requirement</span></span> | <span data-ttu-id="59253-163">值</span><span class="sxs-lookup"><span data-stu-id="59253-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59253-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59253-164">Minimum supported client</span></span><br/> | <span data-ttu-id="59253-165">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59253-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59253-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59253-166">Minimum supported server</span></span><br/> | <span data-ttu-id="59253-167">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59253-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59253-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59253-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59253-169">WsdCodeGen 設定檔</span><span class="sxs-lookup"><span data-stu-id="59253-169">WsdCodeGen Configuration File</span></span>](wsdcodegen-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="59253-170">使用 WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="59253-170">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 




