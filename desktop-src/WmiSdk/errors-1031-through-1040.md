---
description: 描述 WMI SNMP 提供者錯誤1031到1040。
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: 錯誤1031到1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5986ba80a55d2d8f3d4a87b0587331765aa38d67
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886872"
---
# <a name="errors-1031-through-1040"></a>錯誤1031到1040

描述 WMI SNMP 提供者錯誤1031到1040。

[警告1031](#warning-1031)

[嚴重錯誤1032](#fatal-error-1032)

[嚴重錯誤1033](#fatal-error-1033)

[警告1034](#warning-1034)

[警告1036](#warning-1036)

[嚴重錯誤1037](#fatal-error-1037)

[嚴重錯誤1038](#fatal-error-1038)

[嚴重錯誤1039](#fatal-error-1039)

[嚴重錯誤1040](#fatal-error-1040)

## <a name="warning-1031"></a>警告1031

<dl> <dt>

<span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031，警告>： " &lt; 檔案名 &gt; ： <行 \#>： &lt; &gt; 應從模組識別碼匯入標準符號 &lt; 識別碼 &gt; 。假設標準定義。」**
</dt> <dd>

匯入區段模組語義警告，特定于 SNMPv1 或 SNMPv2C。 如果編譯器已知的 SNMP 識別碼是在 IMPORTS 區段中，則匯入它的模組必須是其中一個標準模組。

某些常用的匯入是編譯器部分的「假設知道」。 編譯器不需要存取其他資訊模組來解決這些問題。

下表說明內建的 SNMPv1 和 SNMPv2C 匯入。

</dd> </dl>

**內建 SNMPv1 匯入**



| 匯入類別 | 模組      | 執行個體                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| ASN. 1 值  | RFC1155-SMI-S | 網際網路、目錄、管理、實驗性、私用、企業 |
|              | RFC1213-MIB | MIB-II 和 IP、介面、傳輸                             |
| ASN. 1 類型   | RFC1155-SMI-S | Networkaddress.cache.ttl、IpAddress、Counter、量測計、TimeTicks、不透明        |
|              | RFC1213-MIB | DisplayString、PhysAddress                                          |
| ASN. 1 宏  | RFC-1212    | 物件類型                                                         |
|              | RFC-1215    | TRAP 類型                                                           |



 

**內建 SNMPv2C 匯入**



| 匯入類別       | 模組      | 執行個體                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASN. 1 值        | SNMPv2-SMI-S  | org、dod、Internet、directory、管理、mib 2、傳輸、實驗性、私用、企業、安全性、snmpv2、snmpDomains、snmpProxys、snmpModules                                                           |
|                    | SNMPv2-TM   | rfc1157Proxy                                                                                                                                                                                                   |
| 物件識別    | SNMPv2-SMI-S  | zeroDotZero                                                                                                                                                                                                    |
|                    | SNMPv2-TM   | snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain                                                                                                                     |
| ASN. 1 類型         | SNMPv2-SMI-S  | Integer32、IpAddress、Counter32、TimeTicks、不透明、Counter64、Unsigned32、Gauge32                                                                                                                             |
| ASN. 1 宏        | SNMPv2-SMI-S  | 模組-身分識別，物件-身分識別，物件類型，通知類型                                                                                                                                               |
|                    | SNMPv2-會議 | 物件群組、通知群組、模組相容性、代理程式功能                                                                                                                                        |
|                    | SNMPv2-TC   | 文字慣例                                                                                                                                                                                             |
| 文字慣例 | SNMPv2-TC   | DisplayString、PhysAddress、MacAddress、TruthValue、TestAndIncr、AutonomousType、InstancePointer、VariablePointer、RowPointer、RowStatus、TimeStamp、TimeInterval、>formatting.dateandtime.custom、StorageType、Tdomain、Taddress |
|                    | SNMPv2-TM   | SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a>嚴重錯誤1032

<dl> <dt>

<span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032，嚴重>： " &lt; 檔案名 &gt;<行 \#>： &lt; &gt; 列舉中的值重複值"**
</dt> <dd>

列舉中的模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。 不得有任何重複的值。 <行 \#> 參數是名稱/值的週期位置。

</dd> </dl>

## <a name="fatal-error-1033"></a>嚴重錯誤1033

<dl> <dt>

<span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033，嚴重>： " &lt; 檔案名 &gt;<行 \#>： &lt; &gt; 列舉中的重複名稱識別碼"**
</dt> <dd>

列舉中的模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。 不得有任何重複的名稱。 <行 \#> 參數是名稱/值的週期位置。

</dd> </dl>

## <a name="warning-1034"></a>警告1034

<dl> <dt>

<span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034，警告>： " &lt; 檔案名 &gt;<行 \#>：列舉中不允許有0值）**
</dt> <dd>

列舉中的模組語義警告，特定于 SNMPv1 或 SNMPv2C。 建議您不要在列舉中使用指名的值零。

</dd> </dl>

## <a name="warning-1036"></a>警告1036

<dl> <dt>

<span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036，警告> " &lt; fileName &gt;<行 \#>：列舉中的值無法解析為正整數"**
</dt> <dd>

列舉中的模組語義警告，特定于 SNMPv1 或 SNMPv2C。 列舉中不允許負數值。

</dd> </dl>

## <a name="fatal-error-1037"></a>嚴重錯誤1037

<dl> <dt>

<span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037、嚴重>：「 &lt; 檔案名 &gt;<行 \#>：識別碼 &lt; 識別碼 &gt; 無法解析為八位字串或不透明的類型」**
</dt> <dd>

錯誤規格中的模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。 大小規格中使用的符號必須解析為八位字串或不透明。

</dd> </dl>

## <a name="fatal-error-1038"></a>嚴重錯誤1038

<dl> <dt>

<span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038、嚴重>：「 &lt; 檔案名 &gt;<行 \#>：識別碼 &lt; 識別碼 &gt; 無法解析整數或量測計類型」**
</dt> <dd>

範圍規格中的模組語意錯誤。 這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。

在 SNMPv1 中，範圍規格中使用的符號必須解析為整數或量測計。

在 SNMPv2C 中，範圍規格中使用的符號必須解析為整數、Gauge32、Integer32 或 Unsigned32。

</dd> </dl>

## <a name="fatal-error-1039"></a>嚴重錯誤1039

<dl> <dt>

<span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039、嚴重>： &lt; 檔案名 &gt;<行 \#>：大小規格中使用的負數值 "**
</dt> <dd>

錯誤規格中的模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。 用來指定大小的任何值都必須為非負數。

</dd> </dl>

## <a name="fatal-error-1040"></a>嚴重錯誤1040

<dl> <dt>

<span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040，嚴重>： " &lt; 檔案名 &gt;<行 \#>： &lt; &gt; 大小規格中的識別碼識別碼無法解析為非負整數值"**
</dt> <dd>

範圍或大小規格中的模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。 在大小規格中用來指定值的任何符號都會解析為非負數值。

</dd> </dl>

 

 



