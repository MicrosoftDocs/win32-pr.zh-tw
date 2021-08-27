---
description: 描述 WMI SNMP 提供者錯誤1041到1050。
ms.assetid: e7e70fb3-12c6-40b1-91a4-c550e8210c09
ms.tgt_platform: multiple
title: 錯誤1041到1050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b1a245f8e4da4556dd05a9827255ca2e7f168ab
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879857"
---
# <a name="errors-1041-through-1050"></a>錯誤1041到1050

描述 WMI SNMP 提供者錯誤1041到1050。

[嚴重錯誤1041](#fatal-error-1041)

[嚴重錯誤1042](#fatal-error-1042)

[警告1043](#warning-1043)

[嚴重錯誤1044](#fatal-error-1044)

[警告1045](#warning-1045)

[警告1046](#warning-1046)

[警告1047](#warning-1047)

[警告1048](#warning-1048)

[嚴重錯誤1049](#fatal-error-1049)

## <a name="fatal-error-1041"></a>嚴重錯誤1041

<dl> <dt>

<span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041、嚴重>：「 &lt; 檔案名 &gt;<行 \#>： &lt; &gt; 範圍規格中的識別碼識別碼無法解析為整數值」**
</dt> <dd>

範圍或大小規格中的模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。 大小規格中使用的符號必須解析為八位字串或不透明。 用於指定範圍的任何值都必須是整數。

</dd> </dl>

## <a name="fatal-error-1042"></a>嚴重錯誤1042

<dl> <dt>

<span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042、嚴重>：「 &lt; 檔案名 &gt;<行 \#>：範圍規格的上限小於下限」**
</dt> <dd>

範圍或大小規格中的模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。 大小規格中使用的符號必須解析為八位字串或不透明。 範圍或大小規格的下限不得大於上限。

</dd> </dl>

## <a name="warning-1043"></a>警告1043

<dl> <dt>

<span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043，警告>： " &lt; 檔案名 &gt; ： <行 \#>：具有語法" SEQUENCE "的物件類型，則應該有存取子句「無法存取」**
</dt> <dd>

**物件類型** 宏調用模組語義警告。 資料表或概念資料列 (序列的或序列物件類型，分別) 必須是「不可存取」。

此警告可能會在 SNMPv1 或 SNMPv2C 中發生。

</dd> </dl>

## <a name="fatal-error-1044"></a>嚴重錯誤1044

<dl> <dt>

<span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044、嚴重>：「 &lt; 檔案名 &gt;<行 \#>：重新定義符號 &lt; 識別碼 &gt; 」**
</dt> <dd>

模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。 重新定義物件描述項、宏調用和 asn.1 類型會導致錯誤。

</dd> </dl>

## <a name="warning-1045"></a>警告1045

<dl> <dt>

<span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045，警告>： " &lt; fileName &gt;<lineReference to 標準符號 &lt; symbolName &gt; 假設是針對定義如 moduleName 中的 &lt; 定義 &gt; 。如果您想要參考目前模組中的定義，請使用 "module. symbol" 標記法。**
</dt> <dd>

模組語義警告，特定于 SNMPv1 或 SNMPv2C。 編譯器已知的符號已重新定義，並且被參考。 編譯器會假設符號的標準定義。 因此，若要使用標準符號的重新定義，您必須使用 "Module. Symbol" 標記法。

</dd> </dl>

## <a name="warning-1046"></a>警告1046

<dl> <dt>

<span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046，警告>： " &lt; 檔案名 &gt;<行 \#>： &lt; &gt; 未定義符號。假設標準定義**
</dt> <dd>

模組語義警告，特定于 SNMPv1 或 SNMPv2C。 編譯器已知的符號不可重新定義或使用，但不會匯入。

</dd> </dl>

## <a name="warning-1047"></a>警告1047

<dl> <dt>

<span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047，警告>： " &lt; 檔案名 &gt;<行 \#>： &lt; &gt; 定義但未參考的類型定義符號"**
</dt> <dd>

模組語義警告，特定于 SNMPv1 或 SNMPv2C。 所有值指派和類型定義都必須在某處參考。

</dd> </dl>

## <a name="warning-1048"></a>警告1048

<dl> <dt>

<span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048，警告>： " &lt; 檔案名 &gt;<行 \#>： &lt; &gt; 定義但未參考的值定義符號"**
</dt> <dd>

模組語義警告，特定于 SNMPv1 或 SNMPv2C。 所有值指派和類型定義都必須在某處參考。

</dd> </dl>

## <a name="fatal-error-1049"></a>嚴重錯誤1049

<dl> <dt>

<span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049、嚴重>： " &lt; fileName &gt; ： <line \#>： DEFVAL 子句不能用於具有語法 NETWORKADDRESS.CACHE.TTL 的物件類型"**
</dt> <dd>

**物件類型** 宏調用 SNMPv1 特定模組語意錯誤。 此物件類型的語法子句解析為 Networkaddress.cache.ttl 時，不允許 DEFVAL 子句。

</dd> </dl>

 

 



