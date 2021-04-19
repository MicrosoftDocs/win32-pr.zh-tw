---
description: 描述 WMI SNMP 提供者錯誤1021到1033。
ms.assetid: fc638d0f-20f4-46d0-a36a-c3898415f35c
ms.tgt_platform: multiple
title: 錯誤1021到1030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8bce9c7c4d70250fa63ad0100cf93c8d5b26984
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978894"
---
# <a name="errors-1021-through-1030"></a>錯誤1021到1030

描述 WMI SNMP 提供者錯誤1021到1033。

[嚴重錯誤1021](#fatal-error-1021)

[嚴重錯誤1022](#fatal-error-1022)

[嚴重錯誤1023](#fatal-error-1023)

[嚴重錯誤1024](#fatal-error-1024)

[嚴重錯誤1025](#fatal-error-1025)

[嚴重錯誤1026](#fatal-error-1026)

[警告1027](#warning-1027)

[嚴重錯誤1028](#fatal-error-1028)

[嚴重錯誤1029](#fatal-error-1029)

[嚴重錯誤1030](#fatal-error-1030)

## <a name="fatal-error-1021"></a>嚴重錯誤1021

<dl> <dt>

<span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021，嚴重>： " <fileName><行 \#>： <identifier> TRAP 類型之 VARIABLES 子句中的識別碼無法解析為純量物件類型"**
</dt> <dd>

**陷阱類型** 宏調用，SNMPv1 特定模組語意錯誤。 在 **TRAP 類型** 宏調用的 variables 子句中使用的變數清單中的每個專案，都必須解析成純量物件類型實例的名稱。

</dd> </dl>

## <a name="fatal-error-1022"></a>嚴重錯誤1022

<dl> <dt>

<span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022、嚴重>：「 <fileName><行 \#>：值未解析為類型」 <type>**
</dt> <dd>

值指派模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。 整數的 RHS 值、 **Null**、八進位字串或物件識別碼值指派的類型錯誤。

</dd> </dl>

## <a name="fatal-error-1023"></a>嚴重錯誤1023

<dl> <dt>

<span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023、嚴重>：「 <fileName><行 \#>：識別碼 <identifier> 無法解析為類型」 <identifier>**
</dt> <dd>

值指派模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。 RHS 整數、 **Null**、八進位字串或物件識別碼值指派的符號 (值參考) 不會解析為正確的類型。

</dd> </dl>

## <a name="fatal-error-1024"></a>嚴重錯誤1024

<dl> <dt>

<span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024、嚴重>：「 <fileName><行 \#>： OID 值定義中的負整數」**
</dt> <dd>

值指派模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。 OID 元件清單中的所有值都必須為非負數 (最好是正數) 整數。

</dd> </dl>

## <a name="fatal-error-1025"></a>嚴重錯誤1025

<dl> <dt>

<span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025，嚴重>：「 <identifier> OID 值中的識別碼無法解析為正整數」**
</dt> <dd>

值指派模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。 OID 元件清單中的所有值都必須為非負數 (最好是正數) 整數。

</dd> </dl>

## <a name="fatal-error-1026"></a>嚴重錯誤1026

<dl> <dt>

<span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026、嚴重>：「 <fileName><行 \#>： <identifier> oid 值中的識別碼都不會解析為 oid 值也不會解析為正整數」**
</dt> <dd>

值指派模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。 OID 值中使用的第一個元件必須解析為 OID 值或整數。

</dd> </dl>

## <a name="warning-1027"></a>警告1027

<dl> <dt>

<span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027，警告>：「 <fileName><行 \#>：未使用匯入的符號」 <identifier>**
</dt> <dd>

匯入區段模組語義警告，特定于 SNMPv1 或 SNMPv2C。 針對每個未使用的匯入符號發出警告。

</dd> </dl>

## <a name="fatal-error-1028"></a>嚴重錯誤1028

<dl> <dt>

<span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028、嚴重>：「模組 <identifier> 未匯入匯入區段」**
</dt> <dd>

IMPORTS 區段模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。 用於參考符號的模組名稱，必須出現在 IMPORTS 子句中，或為目前模組的名稱。

</dd> </dl>

## <a name="fatal-error-1029"></a>嚴重錯誤1029

<dl> <dt>

<span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029、嚴重>：「 <fileName><行 \#>：無法匯入目前的模組」 <identifier>**
</dt> <dd>

IMPORTS 區段模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。 目前模組的名稱也是匯入清單中的數位。

</dd> </dl>

## <a name="fatal-error-1030"></a>嚴重錯誤1030

<dl> <dt>

<span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030、嚴重>：「 <fileName><行 \#>： <identifier> 未從模組匯入 <identifier> 符號」**
</dt> <dd>

IMPORTS 區段模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。 您已使用 "Module. Symbol" 標記法，但尚未從 [匯入] 區段中的指定模組匯入符號。

</dd> </dl>

 

 



