---
description: 描述 WMI SNMP 提供者錯誤1081到1090。
ms.assetid: aa953c53-a61f-48e4-9234-acc450b9bdf1
ms.tgt_platform: multiple
title: 錯誤1081到1090
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a80399ef61bce644813447559a76bf9710873be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969308"
---
# <a name="errors-1081-through-1090"></a><span data-ttu-id="f4e83-103">錯誤1081到1090</span><span class="sxs-lookup"><span data-stu-id="f4e83-103">Errors 1081 through 1090</span></span>

<span data-ttu-id="f4e83-104">描述 WMI SNMP 提供者錯誤1081到1090。</span><span class="sxs-lookup"><span data-stu-id="f4e83-104">Describes WMI SNMP provider errors 1081 through 1090.</span></span>

[<span data-ttu-id="f4e83-105">嚴重錯誤1081</span><span class="sxs-lookup"><span data-stu-id="f4e83-105">Fatal Error 1081</span></span>](#fatal-error-1081)

[<span data-ttu-id="f4e83-106">嚴重錯誤 1082</span><span class="sxs-lookup"><span data-stu-id="f4e83-106">Fatal Error 1082</span></span>](#fatal-error-1082)

[<span data-ttu-id="f4e83-107">嚴重錯誤1084</span><span class="sxs-lookup"><span data-stu-id="f4e83-107">Fatal Error 1084</span></span>](#fatal-error-1084)

[<span data-ttu-id="f4e83-108">警告1085</span><span class="sxs-lookup"><span data-stu-id="f4e83-108">Warning 1085</span></span>](#warning-1085)

[<span data-ttu-id="f4e83-109">警告1086</span><span class="sxs-lookup"><span data-stu-id="f4e83-109">Warning 1086</span></span>](#warning-1086)

[<span data-ttu-id="f4e83-110">嚴重錯誤1087</span><span class="sxs-lookup"><span data-stu-id="f4e83-110">Fatal Error 1087</span></span>](#fatal-error-1087)

[<span data-ttu-id="f4e83-111">嚴重錯誤1089</span><span class="sxs-lookup"><span data-stu-id="f4e83-111">Fatal Error 1089</span></span>](#fatal-error-1089)

[<span data-ttu-id="f4e83-112">嚴重錯誤1090</span><span class="sxs-lookup"><span data-stu-id="f4e83-112">Fatal Error 1090</span></span>](#fatal-error-1090)

## <a name="fatal-error-1081"></a><span data-ttu-id="f4e83-113">嚴重錯誤1081</span><span class="sxs-lookup"><span data-stu-id="f4e83-113">Fatal Error 1081</span></span>

<dl> <dt>

<span data-ttu-id="f4e83-114"><span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081、嚴重>：「 <fileName> 行 \#>：符號 <identifier> 未出現在匯入的模組中」 <identifier>**</span><span class="sxs-lookup"><span data-stu-id="f4e83-114"><span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081, Fatal>: "<fileName>line\#>: Symbol <identifier> not present in imported module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="f4e83-115">交互參照中的模組語意錯誤，不是 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="f4e83-115">Module semantic error in cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="f4e83-116">從模組匯入的符號不會解析為該模組中的任何事物。</span><span class="sxs-lookup"><span data-stu-id="f4e83-116">A symbol imported from a module does not resolve to anything in that module.</span></span> <span data-ttu-id="f4e83-117">如果 MIB 中實際參考該符號，就會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f4e83-117">If that symbol is actually referenced in the MIB, this error occurs.</span></span>

</dd> </dl>

## <a name="fatal-error-1082"></a><span data-ttu-id="f4e83-118">嚴重錯誤 1082</span><span class="sxs-lookup"><span data-stu-id="f4e83-118">Fatal Error 1082</span></span>

<dl> <dt>

<span data-ttu-id="f4e83-119"><span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082、嚴重>： " <fileName> ： <行 \#>：不正確 STATUS 子句 <clause> "**</span><span class="sxs-lookup"><span data-stu-id="f4e83-119"><span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082, Fatal>: "<fileName>:<line\#>: Invalid STATUS clause <clause>"**</span></span>
</dt> <dd>

<span data-ttu-id="f4e83-120">**物件身分識別** 宏調用，SNMPv2C 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="f4e83-120">**OBJECT-IDENTITY** macro invocation, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="f4e83-121">**物件身分識別** 調用的 STATUS 子句必須是「目前」、「已淘汰」或「過時」。</span><span class="sxs-lookup"><span data-stu-id="f4e83-121">The STATUS clause of an **OBJECT-IDENTITY** invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="fatal-error-1084"></a><span data-ttu-id="f4e83-122">嚴重錯誤1084</span><span class="sxs-lookup"><span data-stu-id="f4e83-122">Fatal Error 1084</span></span>

<dl> <dt>

<span data-ttu-id="f4e83-123"><span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084，嚴重>： "fileName><行 \#>： MODULE-在所有 SNMPv2 模組的 IMPORTS 區段之後所需的身分識別"**</span><span class="sxs-lookup"><span data-stu-id="f4e83-123"><span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084, Fatal>: "fileName><line\#>: MODULE-IDENTITY required after the IMPORTS section for all SNMPv2 modules"**</span></span>
</dt> <dd>

<span data-ttu-id="f4e83-124">**模組-身分識別** 宏調用，SNMPv2C 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="f4e83-124">**MODULE-IDENTITY** macro invocation, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="f4e83-125">SNMPv2C MIB 中必須至少有一個 **模組身分識別** 調用，緊接在 IMPORTS 區段之後。</span><span class="sxs-lookup"><span data-stu-id="f4e83-125">There must be one and only one **MODULE-IDENTITY** invocation in an SNMPv2C MIB, immediately after the IMPORTS section.</span></span>

</dd> </dl>

## <a name="warning-1085"></a><span data-ttu-id="f4e83-126">警告1085</span><span class="sxs-lookup"><span data-stu-id="f4e83-126">Warning 1085</span></span>

<dl> <dt>

<span data-ttu-id="f4e83-127"><span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085，警告>： " <fileName><行 \#>：在模組中找不到任何群組 <name> 。無法制作模組身分識別。嘗試將模組載入 SMIR 將會失敗」**</span><span class="sxs-lookup"><span data-stu-id="f4e83-127"><span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, Warning>: "<fileName><line\#>: No groups found in module <name>. Could not fabricate MODULE-IDENTITY. Attempt to load the module into the SMIR will fail"**</span></span>
</dt> <dd>

<span data-ttu-id="f4e83-128">模組語義 SNMPv1 特定的警告。</span><span class="sxs-lookup"><span data-stu-id="f4e83-128">Module semantic SNMPv1-specific warning.</span></span> <span data-ttu-id="f4e83-129">如果在模組中找不到任何物件群組，就會產生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f4e83-129">This error is generated if no object groups are found in a module.</span></span>

</dd> </dl>

## <a name="warning-1086"></a><span data-ttu-id="f4e83-130">警告1086</span><span class="sxs-lookup"><span data-stu-id="f4e83-130">Warning 1086</span></span>

<dl> <dt>

<span data-ttu-id="f4e83-131"><span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086，警告>：「 <fileName><行 \#>：在模組中找不到任何群組」 <name>**</span><span class="sxs-lookup"><span data-stu-id="f4e83-131"><span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, Warning>: "<fileName><line\#>: No groups found in module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="f4e83-132">模組語義 SNMPv1 特定的警告。</span><span class="sxs-lookup"><span data-stu-id="f4e83-132">Module semantic SNMPv1-specific warning.</span></span> <span data-ttu-id="f4e83-133">如果在模組中找不到任何物件群組，就會產生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f4e83-133">This error is generated if no object groups are found in a module.</span></span>

</dd> </dl>

## <a name="fatal-error-1087"></a><span data-ttu-id="f4e83-134">嚴重錯誤1087</span><span class="sxs-lookup"><span data-stu-id="f4e83-134">Fatal Error 1087</span></span>

<dl> <dt>

<span data-ttu-id="f4e83-135"><span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087。嚴重>： " <fileName><行 \#>： <clause> 文字慣例宏的 STATUS 子句無效"**</span><span class="sxs-lookup"><span data-stu-id="f4e83-135"><span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087. Fatal>: "<fileName><line\#>: Invalid STATUS clause <clause> for a TEXTUAL-CONVENTION macro"**</span></span>
</dt> <dd>

<span data-ttu-id="f4e83-136">類型指派，SNMPv2C 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="f4e83-136">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="f4e83-137">**文字慣例** 宏調用的 status 子句必須是「目前」、「已淘汰」或「過時」。</span><span class="sxs-lookup"><span data-stu-id="f4e83-137">The status clause of a **TEXTUAL-CONVENTION** macro invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="fatal-error-1089"></a><span data-ttu-id="f4e83-138">嚴重錯誤1089</span><span class="sxs-lookup"><span data-stu-id="f4e83-138">Fatal Error 1089</span></span>

<dl> <dt>

<span data-ttu-id="f4e83-139"><span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089，嚴重>： " <fileName> ： <行 \#>： <identifier> 增強子句中的符號無法解析為數據列物件類型"**</span><span class="sxs-lookup"><span data-stu-id="f4e83-139"><span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089, Fatal>: "<fileName>:<line\#>: Symbol <identifier> in AUGMENTS clause does not resolve to a row OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="f4e83-140">**物件類型** 宏調用 SNMPv2C 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="f4e83-140">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="f4e83-141">如果有一個增強型子句，則增強型子句中的識別碼必須解析為 table 物件類型。</span><span class="sxs-lookup"><span data-stu-id="f4e83-141">If an AUGMENTS clause is present, then the identifier in the AUGMENTS clause must resolve to a table OBJECT-TYPE.</span></span>

</dd> </dl>

## <a name="fatal-error-1090"></a><span data-ttu-id="f4e83-142">嚴重錯誤1090</span><span class="sxs-lookup"><span data-stu-id="f4e83-142">Fatal Error 1090</span></span>

<dl> <dt>

<span data-ttu-id="f4e83-143"><span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090，嚴重>： " <fileName> ： <行 \#> 隱含的子句僅適用于最後一個索引物件"**</span><span class="sxs-lookup"><span data-stu-id="f4e83-143"><span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090, Fatal>: "<fileName>:<line\#> IMPLIED clause is useful only for the last INDEX object"**</span></span>
</dt> <dd>

<span data-ttu-id="f4e83-144">**物件類型** 宏調用 SNMPv2C 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="f4e83-144">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="f4e83-145">隱含的子句只能與 INDEX 子句中的最後一個物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="f4e83-145">The IMPLIED clause can be associated only with the last object in the INDEX clause.</span></span>

</dd> </dl>

 

 



