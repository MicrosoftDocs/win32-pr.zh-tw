---
description: 下列資訊訊息說明編譯器操作。
ms.assetid: 838e598d-871d-4015-a372-4d94cacf8048
ms.tgt_platform: multiple
title: 一般資訊訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0997fad497299c7598fc1130edace49c20d7bb76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318940"
---
# <a name="general-information-messages"></a><span data-ttu-id="31ff2-103">一般資訊訊息</span><span class="sxs-lookup"><span data-stu-id="31ff2-103">General Information Messages</span></span>

<span data-ttu-id="31ff2-104">下列資訊訊息說明編譯器操作。</span><span class="sxs-lookup"><span data-stu-id="31ff2-104">The following information messages describe the compiler operation.</span></span>

<dl> <dt>

<span data-ttu-id="31ff2-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir：版本 <版本 \#> MIB 定義，其編譯來源為 <file name>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: Version <version \#> MIB definitions compiled from <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-106">這則訊息會出現在每個檔案編譯的開頭。</span><span class="sxs-lookup"><span data-stu-id="31ff2-106">This message appears at the beginning of every file compilation.</span></span> <span data-ttu-id="31ff2-107">這表示該檔案可能已由使用者在命令列上明確指定，或由編譯器從登錄包含目錄或命令列上所述的 include 目錄中提取。</span><span class="sxs-lookup"><span data-stu-id="31ff2-107">It means the file may have been explicitly specified on the command line by the user, or it may have been pulled in by the compiler from the registry include directories or the include directories mentioned on the command line.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir：語法檢查失敗于 <file name>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Syntax check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-109">此訊息前面的特定錯誤訊息會提供語法錯誤的性質。</span><span class="sxs-lookup"><span data-stu-id="31ff2-109">The specific error messages that precede this message give the nature of the syntax errors.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir：語義檢查失敗于 <file name>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Semantic check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-111">此訊息前面的特定錯誤訊息會提供語意錯誤的性質。</span><span class="sxs-lookup"><span data-stu-id="31ff2-111">The specific error messages that precede this message give the nature of the semantic errors.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir：無法載入 <file name> 至 smir**</span><span class="sxs-lookup"><span data-stu-id="31ff2-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: Could not load <file name> into the smir**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-113">模組上的語法或語義檢查失敗，或 SMIR 互動未完成。</span><span class="sxs-lookup"><span data-stu-id="31ff2-113">Syntax or semantic check failed on the module, or SMIR interaction was not complete.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir：語法檢查成功于 <file name>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Syntax check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="31ff2-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir：語義檢查成功于 <file name>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Semantic check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="31ff2-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir： <file name> 已成功載入至 smir**</span><span class="sxs-lookup"><span data-stu-id="31ff2-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: Loaded <file name> successfully into the smir**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="31ff2-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir：無法解析中的一或多個符號 <module name>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: Could not resolve one or more symbols in <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-118">找不到對應至指定模組中一或多個匯入符號的模組，或無法編譯。</span><span class="sxs-lookup"><span data-stu-id="31ff2-118">The modules corresponding to one or more of the imported symbols in the specified module were not found or could not be compiled.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir：無法連接到 SMIR**</span><span class="sxs-lookup"><span data-stu-id="31ff2-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: Could not connect to the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-120">請確認 Smir.dll 存在、已使用 regsvr32 命令註冊，而且 Windows Management Instrumentation (WMI) 伺服器已啟動且正在執行。</span><span class="sxs-lookup"><span data-stu-id="31ff2-120">Ensure that Smir.dll exists, has been registered using the regsvr32 command, and that the Windows Management Instrumentation (WMI) server is up and running.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir： SMIR： <模組清單中的模組，每一行 1>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: Modules in the SMIR: <list of modules, 1 on each line>**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-122">這是 **/l** 參數的輸出。</span><span class="sxs-lookup"><span data-stu-id="31ff2-122">This is the output of the **/l** switch.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir 無法列出 SMIR 中的模組**</span><span class="sxs-lookup"><span data-stu-id="31ff2-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir Could not list the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-124">這表示因為沒有 SMIR 連接，所以 **/l** 參數失敗。</span><span class="sxs-lookup"><span data-stu-id="31ff2-124">This indicates a failure of the **/l** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir：已成功刪除模組 <module name>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: Deleted module <module name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-126">**/D** 參數成功。</span><span class="sxs-lookup"><span data-stu-id="31ff2-126">The **/d** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir：無法刪除模組 <module name>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: Could not delete module <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-128">這表示因為沒有任何 SMIR 連接，所以無法使用 **/d** 參數。</span><span class="sxs-lookup"><span data-stu-id="31ff2-128">This indicates a failure of the **/d** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir：已刪除 SMIR 中的所有模組**</span><span class="sxs-lookup"><span data-stu-id="31ff2-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Deleted all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-130">**/P** 參數成功。</span><span class="sxs-lookup"><span data-stu-id="31ff2-130">The **/p** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir：無法刪除 SMIR 中的所有模組**</span><span class="sxs-lookup"><span data-stu-id="31ff2-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Could not delete all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-132">**/P** 參數失敗，因為沒有 SMIR 連接。</span><span class="sxs-lookup"><span data-stu-id="31ff2-132">The **/p** switch failed because there is no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir：模組不 <module name> 存在於 SMIR 中**</span><span class="sxs-lookup"><span data-stu-id="31ff2-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: Module <module name> does not exist in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-134">**/D** 參數失敗，因為指定的模組不在 SMIR 中。</span><span class="sxs-lookup"><span data-stu-id="31ff2-134">The **/d** switch failed because the specified module is not in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir：已成功產生 MOF**</span><span class="sxs-lookup"><span data-stu-id="31ff2-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: Generated MOF successfully**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-136">**/G** 或 **/gc** 參數的工作成功。</span><span class="sxs-lookup"><span data-stu-id="31ff2-136">The **/g** or **/gc** switch worked successfully.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir：無法產生 MOF**</span><span class="sxs-lookup"><span data-stu-id="31ff2-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: Could not generate MOF**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-138">**/G** 或 **/gc** 參數未順利運作，因為沒有 SMIR 連接。</span><span class="sxs-lookup"><span data-stu-id="31ff2-138">The **/g** or **/gc** switch did not work successfully due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir：模組的名稱： <module name>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: Name of the module: <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-140">這是成功的 **/n** 參數輸出。</span><span class="sxs-lookup"><span data-stu-id="31ff2-140">This is the successful output of the **/n** switch.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir：無法成功剖析 <file name>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: Could not parse <file name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-142">這表示 **/n** 或 **/ni** 參數的失敗，因為指定的檔案不是有效的 MIB 檔案。</span><span class="sxs-lookup"><span data-stu-id="31ff2-142">This indicates failure of the **/n** or **/ni** switch because the specified file is not a valid MIB file.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir：已成功處理的檔案 <number>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: Processed <number> files successfully**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-144">這會指定使用 **/r** 或 **/auto** 參數時，已成功剖析的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="31ff2-144">This specifies the number of files that were successfully parsed when the **/r** or the **/auto** switch were used.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir：模組的輸入中重複的檔案 <module name> 。只 <file name> 會編譯檔案**</span><span class="sxs-lookup"><span data-stu-id="31ff2-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: Repeated files in the input for module <module name>. Only the file <file name> will be compiled**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-146">使用者已在命令列上明確指定一個以上的檔案，而且這些檔案中有兩個以上的檔案具有相同的 MIB 模組。</span><span class="sxs-lookup"><span data-stu-id="31ff2-146">The user has explicitly specified more than one file on the command line, and two or more of these files have the same MIB module.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir：已將目錄新增 <directory name> 至登錄**</span><span class="sxs-lookup"><span data-stu-id="31ff2-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Added directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-148">**/Pa** 參數成功。</span><span class="sxs-lookup"><span data-stu-id="31ff2-148">Success of the **/pa** switch.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir：無法將目錄新增 <directory name> 至登錄**</span><span class="sxs-lookup"><span data-stu-id="31ff2-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Could not add directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-150">**/Pa** 參數失敗，只有在登錄 API 失敗時才會發生。</span><span class="sxs-lookup"><span data-stu-id="31ff2-150">Failure of the **/pa** switch, which happens only if the registry API fails.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir：已從登錄中刪除目錄 <directory name>**</span><span class="sxs-lookup"><span data-stu-id="31ff2-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Deleted directory <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-152">**/Pd** 參數成功。</span><span class="sxs-lookup"><span data-stu-id="31ff2-152">Success of the **/pd** switch.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir：無法從登錄 <directory name> 中刪除**</span><span class="sxs-lookup"><span data-stu-id="31ff2-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Could not delete <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-154">**/Pd** 切換失敗。</span><span class="sxs-lookup"><span data-stu-id="31ff2-154">Failure of the **/pd** switch.</span></span> <span data-ttu-id="31ff2-155">指定的目錄不存在於登錄中的目錄清單中。</span><span class="sxs-lookup"><span data-stu-id="31ff2-155">The specified directory does not exist in the list of directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="31ff2-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir： <file name> 不是有效的 mib 檔案**</span><span class="sxs-lookup"><span data-stu-id="31ff2-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> is not a valid mib file**</span></span>
</dt> <dd>

<span data-ttu-id="31ff2-157">在命令列上指定了一個以上的檔案，其中一個檔案不是有效的 MIB 檔案。</span><span class="sxs-lookup"><span data-stu-id="31ff2-157">More than one file has been specified on the command line, one of which is not a valid MIB file.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="31ff2-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="31ff2-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31ff2-159">設定 WMI SNMP 環境</span><span class="sxs-lookup"><span data-stu-id="31ff2-159">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



