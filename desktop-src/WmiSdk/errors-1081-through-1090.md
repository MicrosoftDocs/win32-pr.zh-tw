---
description: 描述 WMI SNMP 提供者錯誤1081到1090。
ms.assetid: aa953c53-a61f-48e4-9234-acc450b9bdf1
ms.tgt_platform: multiple
title: 錯誤1081到1090
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8c707749c66c43c77021fe660eceb5aa16bbb739c930dea0c3a4084351a7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924503"
---
# <a name="errors-1081-through-1090"></a>錯誤1081到1090

描述 WMI SNMP 提供者錯誤1081到1090。

[嚴重錯誤1081](#fatal-error-1081)

[嚴重錯誤 1082](#fatal-error-1082)

[嚴重錯誤1084](#fatal-error-1084)

[警告1085](#warning-1085)

[警告1086](#warning-1086)

[嚴重錯誤1087](#fatal-error-1087)

[嚴重錯誤1089](#fatal-error-1089)

[嚴重錯誤1090](#fatal-error-1090)

## <a name="fatal-error-1081"></a>嚴重錯誤1081

<dl> <dt>

<span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081、嚴重>：「 <fileName> 行 \#>：符號 <identifier> 未出現在匯入的模組中」 <identifier>**
</dt> <dd>

交互參照中的模組語意錯誤，不是 SNMPv1 或 SNMPv2C。 從模組匯入的符號不會解析為該模組中的任何事物。 如果 MIB 中實際參考該符號，就會發生此錯誤。

</dd> </dl>

## <a name="fatal-error-1082"></a>嚴重錯誤 1082

<dl> <dt>

<span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082、嚴重>： " <fileName> ： <行 \#>：不正確 STATUS 子句 <clause> "**
</dt> <dd>

**物件身分識別** 宏調用，SNMPv2C 特定模組語意錯誤。 **物件身分識別** 調用的 STATUS 子句必須是「目前」、「已淘汰」或「過時」。

</dd> </dl>

## <a name="fatal-error-1084"></a>嚴重錯誤1084

<dl> <dt>

<span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084，嚴重>： "fileName><行 \#>： MODULE-在所有 SNMPv2 模組的 IMPORTS 區段之後所需的身分識別"**
</dt> <dd>

**模組-身分識別** 宏調用，SNMPv2C 特定模組語意錯誤。 SNMPv2C MIB 中必須至少有一個 **模組身分識別** 調用，緊接在 IMPORTS 區段之後。

</dd> </dl>

## <a name="warning-1085"></a>警告1085

<dl> <dt>

<span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085，警告>： " <fileName><行 \#>：在模組中找不到任何群組 <name> 。無法制作模組身分識別。嘗試將模組載入 SMIR 將會失敗」**
</dt> <dd>

模組語義 SNMPv1 特定的警告。 如果在模組中找不到任何物件群組，就會產生此錯誤。

</dd> </dl>

## <a name="warning-1086"></a>警告1086

<dl> <dt>

<span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086，警告>：「 <fileName><行 \#>：在模組中找不到任何群組」 <name>**
</dt> <dd>

模組語義 SNMPv1 特定的警告。 如果在模組中找不到任何物件群組，就會產生此錯誤。

</dd> </dl>

## <a name="fatal-error-1087"></a>嚴重錯誤1087

<dl> <dt>

<span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087。嚴重>： " <fileName><行 \#>： <clause> 文字慣例宏的 STATUS 子句無效"**
</dt> <dd>

類型指派，SNMPv2C 特定模組語意錯誤。 **文字慣例** 宏調用的 status 子句必須是「目前」、「已淘汰」或「過時」。

</dd> </dl>

## <a name="fatal-error-1089"></a>嚴重錯誤1089

<dl> <dt>

<span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089，嚴重>： " <fileName> ： <行 \#>： <identifier> 增強子句中的符號無法解析為數據列物件類型"**
</dt> <dd>

**物件類型** 宏調用 SNMPv2C 特定模組語意錯誤。 如果有一個增強型子句，則增強型子句中的識別碼必須解析為 table 物件類型。

</dd> </dl>

## <a name="fatal-error-1090"></a>嚴重錯誤1090

<dl> <dt>

<span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090，嚴重>： " <fileName> ： <行 \#> 隱含的子句僅適用于最後一個索引物件"**
</dt> <dd>

**物件類型** 宏調用 SNMPv2C 特定模組語意錯誤。 隱含的子句只能與 INDEX 子句中的最後一個物件相關聯。

</dd> </dl>

 

 



