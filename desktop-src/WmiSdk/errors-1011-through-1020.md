---
description: 描述 WMI SNMP 提供者錯誤1011到1020。
ms.assetid: 5151a110-1532-48cc-832a-2cee21853b6b
ms.tgt_platform: multiple
title: 錯誤1011到1020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960c646e600f57a9ce98230b12a89424ec9c61dc94c4fdc5360fb6ceaeda24d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374498"
---
# <a name="errors-1011-through-1020"></a>錯誤1011到1020

描述 WMI SNMP 提供者錯誤1011到1020。

[嚴重錯誤1011](#fatal-error-1011)

[嚴重錯誤1012](#fatal-error-1012)

[嚴重錯誤1013](#fatal-error-1013)

[警告1014](#warning-1014)

[嚴重錯誤1015](#fatal-error-1015)

[嚴重錯誤1016](#fatal-error-1016)

[嚴重錯誤1018](#fatal-error-1018)

[嚴重錯誤1020](#fatal-error-1020)

## <a name="fatal-error-1011"></a>嚴重錯誤1011

<dl> <dt>

<span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011、嚴重>： " <fileName> ： <行 \#> SEQUENCE 成員的語法， <identifier> <identifier> 與物件類型的語法子句不同」**
</dt> <dd>

**物件類型** 宏調用模組語意錯誤。 序列的專案必須與物件類型定義的語法子句中的型別相同。 <行 \#> 參數是物件類型定義的語法子句的行。

這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。

</dd> </dl>

## <a name="fatal-error-1012"></a>嚴重錯誤1012

<dl> <dt>

<span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012、嚴重>： " <fileName> ： <行 \#> 索引或增強子句僅適用于 SEQUENCE 物件類型"**
</dt> <dd>

**物件類型** 宏調用模組語意錯誤。 索引子句必須只存在於其語法解析為序列類型的物件類型定義中。

編譯 SNMPv1 或 SNMPv2C MIB 時，會發生此錯誤。

</dd> </dl>

## <a name="fatal-error-1013"></a>嚴重錯誤1013

<dl> <dt>

<span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013，嚴重>：「 <fileName><行 \#>： <identifier> 應解析為序列類型」**
</dt> <dd>

**物件類型** 宏調用模組語意錯誤。 「序列」結構中使用的型別必須解析為序列型別。

這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。

</dd> </dl>

## <a name="warning-1014"></a>警告1014

<dl> <dt>

<span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014，警告>： " <fileName> ： <行 \#>： oid 中不建議是值0的子識別碼"**
</dt> <dd>

**物件類型** 宏調用模組語義警告。 建議網際網路標準 MIB 中的物件在其物件識別碼中使用零的子識別碼。

此警告可能會在 SNMPv1 或 SNMPv2C 中發生。

</dd> </dl>

## <a name="fatal-error-1015"></a>嚴重錯誤1015

<dl> <dt>

<span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015，嚴重>： " <fileName> ： <行 \#>： <identifier> 來自模組 <identifier> 和 <identifier> 模組的 OBJECT-TYPEs <identifier> 都會指派相同的 OID 值」**
</dt> <dd>

**物件類型** 宏調用模組語意錯誤。 在相同或不同模組中 (兩個 **物件類型** 調用) 不得指派相同的物件識別碼值。

這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。

</dd> </dl>

## <a name="fatal-error-1016"></a>嚴重錯誤1016

<dl> <dt>

<span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016，嚴重>： " <fileName> ： <行 \#>： DEFVAL 子句中的值不符合語法子句中的類型"**
</dt> <dd>

**物件類型** 宏調用模組語意錯誤。 DEFVAL 子句中的值必須是語法子句中所述之類型的值。

這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。

</dd> </dl>

## <a name="fatal-error-1018"></a>嚴重錯誤1018

<dl> <dt>

<span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018，嚴重>： " <fileName><行 \#>： <symbol> 在 [在下列情況下的企業子句中，不會解析為 OID 值]**
</dt> <dd>

**陷阱類型** 宏調用，SNMPv1 特定模組語意錯誤。 在 **TRAP 類型** 宏調用的 ENTERPRISE 子句中使用的符號必須解析為物件識別碼值。

</dd> </dl>

## <a name="fatal-error-1020"></a>嚴重錯誤1020

<dl> <dt>

<span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020，嚴重>：「 <fileName><行 \#>：指派給陷阱類型的值 <identifier> 無法解析為正整數」**
</dt> <dd>

**陷阱類型** 宏調用，SNMPv1 特定模組語意錯誤。 用來指定陷阱值的符號不會解析為正整數。

</dd> </dl>

 

 



