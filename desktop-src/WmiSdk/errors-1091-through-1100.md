---
description: 描述 WMI SNMP 提供者錯誤1091到1100。
ms.assetid: 9b7db4fc-8ae8-46f7-a40f-e4401a335c5d
ms.tgt_platform: multiple
title: 錯誤1091到1100
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc57b8eb628de86b4a7d737bacec13bc2fdeadfb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880088"
---
# <a name="errors-1091-through-1100"></a>錯誤1091到1100

描述 WMI SNMP 提供者錯誤1091到1100。

[警告1091](#warning-1091)

[嚴重錯誤1092](#fatal-error-1092)

[嚴重錯誤1093](#fatal-error-1093)

[嚴重錯誤1094](#fatal-error-1094)

[嚴重錯誤1095](#fatal-error-1095)

[嚴重錯誤1097](#fatal-error-1097)

[嚴重錯誤1098](#fatal-error-1098)

[嚴重錯誤1099](#fatal-error-1099)

## <a name="warning-1091"></a>警告1091

<dl> <dt>

<span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091，警告>：「 &lt; 檔案名 &gt; ： <行 \#> 隱含子句不能用於固定大小的物件」**
</dt> <dd>

**物件類型** 宏調用 SNMPv2C 特定模組語義警告。 只有在索引子句中具有可變長度語法的物件（例如物件識別碼或可變長度的八位字串）時，才會出現隱含關鍵字。

</dd> </dl>

## <a name="fatal-error-1092"></a>嚴重錯誤1092

<dl> <dt>

<span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092，嚴重>： " &lt; fileName &gt; ： <行 \#> 不允許有零長度物件的隱含子句"**
</dt> <dd>

**物件類型** 宏調用 SNMPv2C 特定模組語意錯誤。 如果物件的長度為零，則不能在可變長度的物件上使用隱含的子句。

</dd> </dl>

## <a name="fatal-error-1093"></a>嚴重錯誤1093

<dl> <dt>

<span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093。嚴重>： " &lt; 檔案名 &gt;<行 \#>：只能根據 V1 smi-s 來列舉類型" INTEGER "**
</dt> <dd>

類型指派，SNMPv1 特定模組語意錯誤。 SNMPv1 MIB 列舉只能使用整數類型。

</dd> </dl>

## <a name="fatal-error-1094"></a>嚴重錯誤1094

<dl> <dt>

<span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094。嚴重>： " &lt; 檔案名 &gt;<行 \#>：列舉中使用的類型不會解析為其中一個允許的類型"**
</dt> <dd>

類型指派，SNMPv2C 特定模組語意錯誤。 列舉中使用的型別必須是整數或對等的型別，或是另一個列舉。

</dd> </dl>

## <a name="fatal-error-1095"></a>嚴重錯誤1095

<dl> <dt>

<span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095。嚴重>： " &lt; 檔案名 &gt;<行 \#>：列舉成員不是父列舉的成員"**
</dt> <dd>

類型指派，SNMPv2C 特定模組語意錯誤。 如果使用另一個列舉，其一組專案必須是父列舉專案集合的子集。

</dd> </dl>

## <a name="fatal-error-1097"></a>嚴重錯誤1097

<dl> <dt>

<span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097、嚴重>：「 &lt; 檔案名 &gt;<行 \#>：識別碼 &lt; 名稱 &gt; 無法解析為整數值」**
</dt> <dd>

類型指派，SNMPv2C 特定模組語意錯誤。 位類型中的值必須是整數值。

</dd> </dl>

## <a name="fatal-error-1098"></a>嚴重錯誤1098

<dl> <dt>

<span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098，嚴重>： " &lt; 檔案名 &gt;<行 \#>： &lt; &gt; 位結構中的重複值值"**
</dt> <dd>

類型指派，SNMPv2C 特定模組語意錯誤。 BITS 結構中不能有重複的名稱和值。 <行 \#> 參數是名稱/值的週期位置。

</dd> </dl>

## <a name="fatal-error-1099"></a>嚴重錯誤1099

<dl> <dt>

<span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099，嚴重>： " &lt; 檔案名 &gt;<行 \#>： &lt; &gt; 位結構中的重複名稱識別碼"**
</dt> <dd>

類型指派，SNMPv2C 特定模組語意錯誤。 BITS 結構中不能有重複的名稱和值。 <行 \#> 參數是名稱/值的週期位置。

</dd> </dl>

 

 



