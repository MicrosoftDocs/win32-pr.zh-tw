---
description: SNMP 編譯器會以命令列模式以單一可執行檔的形式執行。
ms.assetid: 0e85fe84-dacb-4720-8242-ffa0046780f3
ms.tgt_platform: multiple
title: smi2smir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e1d757293b5ee128f2ce1bc2bd5ec8479d9b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195051"
---
# <a name="smi2smir"></a><span data-ttu-id="3a8d3-103">smi2smir</span><span class="sxs-lookup"><span data-stu-id="3a8d3-103">smi2smir</span></span>

<span data-ttu-id="3a8d3-104">SNMP 編譯器會以命令列模式以單一可執行檔的形式執行。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-104">The SNMP compiler runs as a single executable file in the command-line mode.</span></span> <span data-ttu-id="3a8d3-105">編譯器會接受一個 SNMP 資訊模組作為輸入，並接受解析外部參考所需的任何其他模組。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-105">The compiler accepts one SNMP information module as input, and accepts any additional modules necessary to resolve external references.</span></span> <span data-ttu-id="3a8d3-106">使用下列其中一個命令列語法範例。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-106">Use one of the following command-line syntax examples.</span></span>

<span data-ttu-id="3a8d3-107">如需有關如何使用這個編譯器的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-107">For more information about when this compiler is used, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a><span data-ttu-id="3a8d3-108">交換器</span><span class="sxs-lookup"><span data-stu-id="3a8d3-108">Switches</span></span>

<dl> <span data-ttu-id="3a8d3-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3a8d3-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> </span></span><dd>

<span data-ttu-id="3a8d3-110">編譯器接受下列診斷引數。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-110">The compiler accepts the following diagnostic arguments.</span></span>

<dl> <dt>

<span data-ttu-id="3a8d3-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<**_診斷層級_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3a8d3-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<**_diagnostic-level_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-112">要顯示的診斷類型。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-112">Type of diagnostics to display.</span></span> <span data-ttu-id="3a8d3-113">預設值為 2。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-113">The default is 2.</span></span>

<span data-ttu-id="3a8d3-114">以下是可以設定的診斷層級值清單：</span><span class="sxs-lookup"><span data-stu-id="3a8d3-114">The following is a list of the diagnostic level values that can be set:</span></span>

-   <span data-ttu-id="3a8d3-115">0 = 無訊息</span><span class="sxs-lookup"><span data-stu-id="3a8d3-115">0 = Silent</span></span>
-   <span data-ttu-id="3a8d3-116">1 = 嚴重</span><span class="sxs-lookup"><span data-stu-id="3a8d3-116">1 = Fatal</span></span>
-   <span data-ttu-id="3a8d3-117">2 = 嚴重和警告</span><span class="sxs-lookup"><span data-stu-id="3a8d3-117">2 = Fatal and warning</span></span>
-   <span data-ttu-id="3a8d3-118">3 = 嚴重、警告和資訊訊息</span><span class="sxs-lookup"><span data-stu-id="3a8d3-118">3 = Fatal, warning, and information messages</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<**_計數_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3a8d3-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<**_count_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-120">要顯示的最大嚴重訊息和警告訊息數目; *計數* 必須是正整數整數。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-120">Maximum number of fatal and warning messages to display; *count* must be a positive decimal integer.</span></span> <span data-ttu-id="3a8d3-121">如果未指定 **/c** ，可以回報的錯誤數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-121">If **/c** is not specified, there is no limit to the number of errors that can be reported.</span></span>

<span data-ttu-id="3a8d3-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3a8d3-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> </span></span><dd>

<span data-ttu-id="3a8d3-123">編譯器接受下列版本引數。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-123">The compiler accepts the following version arguments.</span></span>

<dl> <dt>

<span data-ttu-id="3a8d3-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-125">指定嚴格符合 SNMPv1 SMI-S。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-125">Specifies strict conformance to the SNMPv1 SMI.</span></span> <span data-ttu-id="3a8d3-126">如果編譯器偵測到非 SNMPv1 語句，則會報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-126">The compiler reports an error if it detects non-SNMPv1 statements.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-128">指定對 SNMPv2 SMI-S 的嚴格一致性。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-128">Specifies strict conformance to the SNMPv2 SMI.</span></span> <span data-ttu-id="3a8d3-129">如果編譯器偵測到非 SNMPv2 語句，則會報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-129">The compiler reports an error if it detects non-SNMPv2 statements.</span></span>

<span data-ttu-id="3a8d3-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3a8d3-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span></span><dd>

<span data-ttu-id="3a8d3-131">編譯器接受下列命令引數。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-131">The compiler accepts the following command arguments.</span></span>

<dl> <dt>

<span data-ttu-id="3a8d3-132"><span id="_d"></span><span id="_D"></span>**/d**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-132"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-133">從 SMIR 中刪除指定的模組。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-133">Deletes the specified module from the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-134"><span id="_p"></span><span id="_P"></span>**/p**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-134"><span id="_p"></span><span id="_P"></span>**/p**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-135">刪除 SMIR 中的所有模組。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-135">Deletes all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-136"><span id="_l"></span><span id="_L"></span>**/l**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-136"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-137">列出 SMIR 中的所有模組。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-137">Lists all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-139">在模組上執行本機語法檢查。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-139">Performs a local syntax check on the module.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ec** **\[<**_CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="3a8d3-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ec** **\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-141">在模組上執行本機和外部檢查。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-141">Performs local and external checks on the module.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <**_CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="3a8d3-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**/a\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-143">執行本機和外部檢查，並將模組載入至 SMIR。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-143">Performs local and external checks and loads the module into the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /sa <**_CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="3a8d3-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**/sa\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-145">與 **/a** 相同，但以無訊息方式運作。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-145">Same as **/a**, but works silently.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <**_CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="3a8d3-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**/g\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-147">產生 SMIR 的 mof 檔案，您稍後可以使用 MOF 編譯器將它載入至 WMI。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-147">Generates a SMIR .mof file that you can later load into WMI using the MOF compiler.</span></span> <span data-ttu-id="3a8d3-148">SNMP 類別提供者用來將類別動態提供給一或多個命名空間。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-148">Used by the SNMP class provider to provide classes dynamically to one or more namespaces.</span></span> <span data-ttu-id="3a8d3-149">當您不知道受管理的 SNMP 裝置支援哪些 Mib 時，請使用此選項。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-149">Use this option when you do not know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="3a8d3-150">SNMP 類別提供者會在執行時間檢查裝置是否有此 MIB，並以動態方式將類別提供給命名空間。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-150">The SNMP class provider checks the device at runtime for the presence of this MIB and supplies the classes dynamically to the namespace.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /gc <**_CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="3a8d3-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**/gc\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-152">產生靜態的 mof 檔案，該檔案可稍後載入至 WMI 作為特定命名空間的靜態類別。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-152">Generates a static .mof file that can be loaded later into WMI as static classes for a particular namespace.</span></span> <span data-ttu-id="3a8d3-153">當您知道受管理的 SNMP 裝置支援哪些 Mib 時，請使用此選項。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-153">Use this option when you know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="3a8d3-154">您可以藉由將命令的輸出導向至指定的檔案，來定義要產生的 mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-154">You can define the .mof file to be generated by directing the output of your command to a specified file.</span></span> <span data-ttu-id="3a8d3-155">請勿使用 with **/ext/o**。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-155">Do not use with **/ext/o**.</span></span>

<span data-ttu-id="3a8d3-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3a8d3-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> </span></span><dd>

<span data-ttu-id="3a8d3-157">編譯器接受下列命令修飾詞。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-157">The compiler accepts the following command modifiers.</span></span>

<dl> <dt>

<span data-ttu-id="3a8d3-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<**_目錄_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3a8d3-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<**_directory_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-159">指定要搜尋的相依 MIB 模組目錄。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-159">Specifies a directory to be searched for dependent MIB modules.</span></span> <span data-ttu-id="3a8d3-160">使用搭配 **/a**、 **/ec**、 **/g**、 **/gc** 和 **/sa**。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-160">Use with **/a**, **/ec**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="3a8d3-161">**/I** 選項可以出現在命令中多次;系統會依命令中指定的順序來搜尋目錄。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-161">The **/i** option can appear multiple times in the command; directories are searched in the order specified in the command.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-162"><span id="_ch"></span><span id="_CH"></span>**/ch**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-162"><span id="_ch"></span><span id="_CH"></span>**/ch**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-163">產生 MOF 檔案標頭中的內容資訊，例如日期、時間、主機或使用者。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-163">Generates context information, such as the date, time, host, or user, in the MOF file header.</span></span> <span data-ttu-id="3a8d3-164">搭配 **/g** 和 **/gc** 使用。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-164">Use with **/g** and **/gc**.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-165"><span id="_t"></span><span id="_T"></span>**一起**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-165"><span id="_t"></span><span id="_T"></span>**/t**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-166">產生 [SnmpNotification](snmpnotification.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-166">Generates [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="3a8d3-167">搭配 **/a**、 **/g** 和 **/sa** 使用。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-167">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-168"><span id="_ext"></span><span id="_EXT"></span>**/ext**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-168"><span id="_ext"></span><span id="_EXT"></span>**/ext**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-169">產生 [SnmpExtendedNotification](snmpextendednotification.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-169">Generates [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="3a8d3-170">搭配 **/a**、 **/g** 和 **/sa** 使用。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-170">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-172">只產生 [SnmpNotification](snmpnotification.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-172">Generates only [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="3a8d3-173">搭配 **/a**、 **/g** 和 **/sa** 使用。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-173">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-175">只產生 [SnmpExtendedNotification](snmpextendednotification.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-175">Generates only [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="3a8d3-176">搭配 **/a**、 **/g** 和 **/sa** 使用。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-176">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-177"><span id="_s"></span><span id="_S"></span>**/s**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-177"><span id="_s"></span><span id="_S"></span>**/s**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-178">不會對應 DESCRIPTION 子句的文字。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-178">Does not map the text of the DESCRIPTION clause.</span></span> <span data-ttu-id="3a8d3-179">使用 **/a**、 **/g**、 **/gc** 和 **/sa**。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-179">Use with **/a**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="3a8d3-180">當您想要將儲存體需求降至最低時，請使用此選項。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-180">Use this option when you want to minimize storage requirements.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-181"><span id="_auto"></span><span id="_AUTO"></span>**/auto**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-181"><span id="_auto"></span><span id="_AUTO"></span>**/auto**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-182">在完成 <*CommandArg*> 切換之前重建 MIB 查閱資料表。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-182">Rebuilds the MIB lookup table before completing the <*CommandArg*> switch.</span></span> <span data-ttu-id="3a8d3-183">使用 **/a**、 **/ec**、 **/g** 和 **/gc**。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-183">Use with **/a**, **/ec**, **/g**, and **/gc**.</span></span>

<span data-ttu-id="3a8d3-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3a8d3-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> </span></span><dd>

<span data-ttu-id="3a8d3-185">編譯器接受下列登錄引數。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-185">The compiler accepts the following registry arguments.</span></span>

<dl> <dt>

<span data-ttu-id="3a8d3-186"><span id="_pa"></span><span id="_PA"></span>**/pa**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-186"><span id="_pa"></span><span id="_PA"></span>**/pa**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-187">將指定的目錄新增至登錄。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-187">Adds the specified directory to the registry.</span></span> <span data-ttu-id="3a8d3-188">預設值是目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-188">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-189"><span id="_pd"></span><span id="_PD"></span>**/pd**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-189"><span id="_pd"></span><span id="_PD"></span>**/pd**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-190">從登錄中刪除指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-190">Deletes the specified directory from the registry.</span></span> <span data-ttu-id="3a8d3-191">預設值是目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-191">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-192"><span id="_pl"></span><span id="_PL"></span>**/pl**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-192"><span id="_pl"></span><span id="_PL"></span>**/pl**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-193">列出登錄中的 MIB 查閱目錄。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-193">Lists the MIB lookup directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-194"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-194"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-195">重建整個 MIB 查閱資料表。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-195">Rebuilds the entire MIB lookup table.</span></span>

<span data-ttu-id="3a8d3-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3a8d3-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> </span></span><dd>

<span data-ttu-id="3a8d3-197">編譯器接受下列模組資訊引數。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-197">The compiler accepts the following module information arguments.</span></span>

<dl> <dt>

<span data-ttu-id="3a8d3-198"><span id="_n"></span><span id="_N"></span>**n**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-198"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-199">傳回指定模組的 ASN. 1 名稱。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-199">Returns the ASN.1 name of the specified module.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-201">傳回輸入模組所參考之所有匯入模組的 asn.1 名稱。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-201">Returns the ASN.1 names of all import modules referred to by the input module.</span></span>

<span data-ttu-id="3a8d3-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3a8d3-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> </span></span><dd>

<span data-ttu-id="3a8d3-203">編譯器接受下列說明引數。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-203">The compiler accepts the following help arguments.</span></span>

<dl> <dt>

<span data-ttu-id="3a8d3-204"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-204"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-205">顯示 SNMP 編譯器語法的說明。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-205">Displays help on the SNMP compiler syntax.</span></span>

</dd> <dt>

<span data-ttu-id="3a8d3-206"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="3a8d3-206"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="3a8d3-207">顯示 SNMP 編譯器語法的說明。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-207">Displays help on the SNMP compiler syntax.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a8d3-208">備註</span><span class="sxs-lookup"><span data-stu-id="3a8d3-208">Remarks</span></span>

<span data-ttu-id="3a8d3-209">SNMP 資訊模組是以抽象語法標記法 (一)  (asn.1 的子集撰寫) 編譯器會執行下列功能：</span><span class="sxs-lookup"><span data-stu-id="3a8d3-209">SNMP information modules are written in a subset of the Abstract Syntax Notation One (ASN.1) The compiler performs the following functions:</span></span>

-   <span data-ttu-id="3a8d3-210">從 SNMP 資訊模組載入資料。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-210">Loads the data from the SNMP information module.</span></span>
-   <span data-ttu-id="3a8d3-211">在資訊模組上執行檢查操作。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-211">Performs checking operations on the information module.</span></span> <span data-ttu-id="3a8d3-212">例如，它會檢查本機語法，並且針對附屬模組中的資訊檢查外部參考。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-212">For example, it checks the local syntax and it checks external references against information in the subsidiary modules.</span></span>
-   <span data-ttu-id="3a8d3-213">從 SMIR 移除之前載入的所有資料，或從一個資訊模組移除載入的資料。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-213">Removes all previously loaded data from the SMIR, or removes data loaded from one information module.</span></span>
-   <span data-ttu-id="3a8d3-214">傳回指定檔案的 asn.1 模組名稱，或傳回指定檔案中所有匯入模組的 asn.1 模組名稱。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-214">Returns the ASN.1 module name of a specified file or returns the ASN.1 module names of all imported modules in a specified file.</span></span>
-   <span data-ttu-id="3a8d3-215">傳回 SMIR 中目前載入的所有 SNMP 資訊模組的 ASN.1 模組名稱。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-215">Returns the ASN.1 module names of all SNMP information modules currently loaded in the SMIR.</span></span>
-   <span data-ttu-id="3a8d3-216">會自動解決匯入的模組，而不需要使用者手動指定所需的模組。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-216">Performs automatic resolution of imported modules rather than requiring users to specify the required modules manually.</span></span>
-   <span data-ttu-id="3a8d3-217">執行不會產生任何輸出的無訊息載入模式，但是可以在安裝作業期間，用來將資料載入 SMIR。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-217">Performs a silent-loading mode of operation that does not generate any output, but can be used to load data into the SMIR during an installation operation.</span></span>
-   <span data-ttu-id="3a8d3-218">將 SNMP 資訊模組中的資料輸出到 SMIR 中。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-218">Outputs the data from the SNMP information module into the SMIR.</span></span>
-   <span data-ttu-id="3a8d3-219">（選擇性）建立靜態或 SMIR MOF 檔案，其中包含資訊模組的輸出。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-219">Optionally creates a static or SMIR MOF file containing the output from the information module.</span></span>

    <span data-ttu-id="3a8d3-220">如有必要，您可以將靜態的 mof 檔案載入至 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-220">If necessary, you can load the static .mof file into a WMI namespace.</span></span> <span data-ttu-id="3a8d3-221">SMIR mof 檔案包含類別應該位於其中的 SNMP 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-221">A SMIR .mof file contains the name of the SNMP namespace in which the classes should reside.</span></span>

## <a name="examples"></a><span data-ttu-id="3a8d3-222">範例</span><span class="sxs-lookup"><span data-stu-id="3a8d3-222">Examples</span></span>

<span data-ttu-id="3a8d3-223">下列範例會將 pra mof 檔案定義為 pra 的輸出。</span><span class="sxs-lookup"><span data-stu-id="3a8d3-223">The following example defines the pra.mof file to be the output from the pra.mib file.</span></span>

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a><span data-ttu-id="3a8d3-224">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a8d3-224">Requirements</span></span>



| <span data-ttu-id="3a8d3-225">需求</span><span class="sxs-lookup"><span data-stu-id="3a8d3-225">Requirement</span></span> | <span data-ttu-id="3a8d3-226">值</span><span class="sxs-lookup"><span data-stu-id="3a8d3-226">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3a8d3-227">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a8d3-227">Minimum supported client</span></span><br/> | <span data-ttu-id="3a8d3-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a8d3-228">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3a8d3-229">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a8d3-229">Minimum supported server</span></span><br/> | <span data-ttu-id="3a8d3-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a8d3-230">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a8d3-231">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a8d3-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a8d3-232">SNMP 編譯器錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="3a8d3-232">SNMP Compiler Error Messages</span></span>](snmp-compiler-error-messages.md)
</dt> <dt>

[<span data-ttu-id="3a8d3-233">設定 WMI SNMP 環境</span><span class="sxs-lookup"><span data-stu-id="3a8d3-233">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[<span data-ttu-id="3a8d3-234">存取 SNMP 裝置</span><span class="sxs-lookup"><span data-stu-id="3a8d3-234">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 




