---
description: 描述 WMI SNMP 提供者錯誤1031到1040。
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: 錯誤1031到1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34079c2cbdb8e50aef04e8c364ba99abee760fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985013"
---
# <a name="errors-1031-through-1040"></a><span data-ttu-id="9895e-103">錯誤1031到1040</span><span class="sxs-lookup"><span data-stu-id="9895e-103">Errors 1031 through 1040</span></span>

<span data-ttu-id="9895e-104">描述 WMI SNMP 提供者錯誤1031到1040。</span><span class="sxs-lookup"><span data-stu-id="9895e-104">Describes WMI SNMP provider errors 1031 through 1040.</span></span>

[<span data-ttu-id="9895e-105">警告1031</span><span class="sxs-lookup"><span data-stu-id="9895e-105">Warning 1031</span></span>](#warning-1031)

[<span data-ttu-id="9895e-106">嚴重錯誤1032</span><span class="sxs-lookup"><span data-stu-id="9895e-106">Fatal Error 1032</span></span>](#fatal-error-1032)

[<span data-ttu-id="9895e-107">嚴重錯誤1033</span><span class="sxs-lookup"><span data-stu-id="9895e-107">Fatal Error 1033</span></span>](#fatal-error-1033)

[<span data-ttu-id="9895e-108">警告1034</span><span class="sxs-lookup"><span data-stu-id="9895e-108">Warning 1034</span></span>](#warning-1034)

[<span data-ttu-id="9895e-109">警告1036</span><span class="sxs-lookup"><span data-stu-id="9895e-109">Warning 1036</span></span>](#warning-1036)

[<span data-ttu-id="9895e-110">嚴重錯誤1037</span><span class="sxs-lookup"><span data-stu-id="9895e-110">Fatal Error 1037</span></span>](#fatal-error-1037)

[<span data-ttu-id="9895e-111">嚴重錯誤1038</span><span class="sxs-lookup"><span data-stu-id="9895e-111">Fatal Error 1038</span></span>](#fatal-error-1038)

[<span data-ttu-id="9895e-112">嚴重錯誤1039</span><span class="sxs-lookup"><span data-stu-id="9895e-112">Fatal Error 1039</span></span>](#fatal-error-1039)

[<span data-ttu-id="9895e-113">嚴重錯誤1040</span><span class="sxs-lookup"><span data-stu-id="9895e-113">Fatal Error 1040</span></span>](#fatal-error-1040)

## <a name="warning-1031"></a><span data-ttu-id="9895e-114">警告1031</span><span class="sxs-lookup"><span data-stu-id="9895e-114">Warning 1031</span></span>

<dl> <dt>

<span data-ttu-id="9895e-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031，警告>： " <fileName> ： <行 \#>： <identifier> 應從模組匯入標準符號 <identifier> 。假設標準定義。」**</span><span class="sxs-lookup"><span data-stu-id="9895e-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, Warning>: "<fileName>:<line\#>: Standard symbol <identifier> should be imported from module <identifier>. Assuming the standard definition."**</span></span>
</dt> <dd>

<span data-ttu-id="9895e-116">匯入區段模組語義警告，特定于 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="9895e-116">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9895e-117">如果編譯器已知的 SNMP 識別碼是在 IMPORTS 區段中，則匯入它的模組必須是其中一個標準模組。</span><span class="sxs-lookup"><span data-stu-id="9895e-117">If an SNMP identifier known to the compiler is in the IMPORTS section, then the module from which it is imported must be one of the standard modules.</span></span>

<span data-ttu-id="9895e-118">某些常用的匯入是編譯器部分的「假設知道」。</span><span class="sxs-lookup"><span data-stu-id="9895e-118">Certain commonly used IMPORTS are "assumed knowledge" on the part of the compiler.</span></span> <span data-ttu-id="9895e-119">編譯器不需要存取其他資訊模組來解決這些問題。</span><span class="sxs-lookup"><span data-stu-id="9895e-119">It is unnecessary for the compiler to require access to other information modules to resolve these.</span></span>

<span data-ttu-id="9895e-120">下表說明內建的 SNMPv1 和 SNMPv2C 匯入。</span><span class="sxs-lookup"><span data-stu-id="9895e-120">The built-in SNMPv1 and SNMPv2C IMPORTS are described in the following tables.</span></span>

</dd> </dl>

<span data-ttu-id="9895e-121">**內建 SNMPv1 匯入**</span><span class="sxs-lookup"><span data-stu-id="9895e-121">**Built-in SNMPv1 IMPORTS**</span></span>



| <span data-ttu-id="9895e-122">匯入類別</span><span class="sxs-lookup"><span data-stu-id="9895e-122">Import Class</span></span> | <span data-ttu-id="9895e-123">模組</span><span class="sxs-lookup"><span data-stu-id="9895e-123">Module</span></span>      | <span data-ttu-id="9895e-124">執行個體</span><span class="sxs-lookup"><span data-stu-id="9895e-124">Instances</span></span>                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| <span data-ttu-id="9895e-125">ASN. 1 值</span><span class="sxs-lookup"><span data-stu-id="9895e-125">ASN.1 Value</span></span>  | <span data-ttu-id="9895e-126">RFC1155-SMI-S</span><span class="sxs-lookup"><span data-stu-id="9895e-126">RFC1155-SMI</span></span> | <span data-ttu-id="9895e-127">網際網路、目錄、管理、實驗性、私用、企業</span><span class="sxs-lookup"><span data-stu-id="9895e-127">Internet, directory, management, experimental, private, enterprises</span></span> |
|              | <span data-ttu-id="9895e-128">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="9895e-128">RFC1213-MIB</span></span> | <span data-ttu-id="9895e-129">MIB-II 和 IP、介面、傳輸</span><span class="sxs-lookup"><span data-stu-id="9895e-129">MIB-II and IP, interfaces, transmission</span></span>                             |
| <span data-ttu-id="9895e-130">ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="9895e-130">ASN.1 Type</span></span>   | <span data-ttu-id="9895e-131">RFC1155-SMI-S</span><span class="sxs-lookup"><span data-stu-id="9895e-131">RFC1155-SMI</span></span> | <span data-ttu-id="9895e-132">Networkaddress.cache.ttl、IpAddress、Counter、量測計、TimeTicks、不透明</span><span class="sxs-lookup"><span data-stu-id="9895e-132">NetworkAddress, IpAddress, Counter, Gauge, TimeTicks, Opaque</span></span>        |
|              | <span data-ttu-id="9895e-133">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="9895e-133">RFC1213-MIB</span></span> | <span data-ttu-id="9895e-134">DisplayString、PhysAddress</span><span class="sxs-lookup"><span data-stu-id="9895e-134">DisplayString, PhysAddress</span></span>                                          |
| <span data-ttu-id="9895e-135">ASN. 1 宏</span><span class="sxs-lookup"><span data-stu-id="9895e-135">ASN.1 Macro</span></span>  | <span data-ttu-id="9895e-136">RFC-1212</span><span class="sxs-lookup"><span data-stu-id="9895e-136">RFC-1212</span></span>    | <span data-ttu-id="9895e-137">物件類型</span><span class="sxs-lookup"><span data-stu-id="9895e-137">OBJECT-TYPE</span></span>                                                         |
|              | <span data-ttu-id="9895e-138">RFC-1215</span><span class="sxs-lookup"><span data-stu-id="9895e-138">RFC-1215</span></span>    | <span data-ttu-id="9895e-139">TRAP 類型</span><span class="sxs-lookup"><span data-stu-id="9895e-139">TRAP-TYPE</span></span>                                                           |



 

<span data-ttu-id="9895e-140">**內建 SNMPv2C 匯入**</span><span class="sxs-lookup"><span data-stu-id="9895e-140">**Built-in SNMPv2C IMPORTS**</span></span>



| <span data-ttu-id="9895e-141">匯入類別</span><span class="sxs-lookup"><span data-stu-id="9895e-141">Import Class</span></span>       | <span data-ttu-id="9895e-142">模組</span><span class="sxs-lookup"><span data-stu-id="9895e-142">Module</span></span>      | <span data-ttu-id="9895e-143">執行個體</span><span class="sxs-lookup"><span data-stu-id="9895e-143">Instances</span></span>                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9895e-144">ASN. 1 值</span><span class="sxs-lookup"><span data-stu-id="9895e-144">ASN.1 Value</span></span>        | <span data-ttu-id="9895e-145">SNMPv2-SMI-S</span><span class="sxs-lookup"><span data-stu-id="9895e-145">SNMPv2-SMI</span></span>  | <span data-ttu-id="9895e-146">org、dod、Internet、directory、管理、mib 2、傳輸、實驗性、私用、企業、安全性、snmpv2、snmpDomains、snmpProxys、snmpModules</span><span class="sxs-lookup"><span data-stu-id="9895e-146">org, dod, Internet, directory, mgmt, mib-2, transmission, experimental, private, enterprises, security, snmpv2, snmpDomains, snmpProxys, snmpModules</span></span>                                                           |
|                    | <span data-ttu-id="9895e-147">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="9895e-147">SNMPv2-TM</span></span>   | <span data-ttu-id="9895e-148">rfc1157Proxy</span><span class="sxs-lookup"><span data-stu-id="9895e-148">rfc1157Proxy</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="9895e-149">物件識別</span><span class="sxs-lookup"><span data-stu-id="9895e-149">Object Identity</span></span>    | <span data-ttu-id="9895e-150">SNMPv2-SMI-S</span><span class="sxs-lookup"><span data-stu-id="9895e-150">SNMPv2-SMI</span></span>  | <span data-ttu-id="9895e-151">zeroDotZero</span><span class="sxs-lookup"><span data-stu-id="9895e-151">zeroDotZero</span></span>                                                                                                                                                                                                    |
|                    | <span data-ttu-id="9895e-152">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="9895e-152">SNMPv2-TM</span></span>   | <span data-ttu-id="9895e-153">snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain</span><span class="sxs-lookup"><span data-stu-id="9895e-153">snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain</span></span>                                                                                                                     |
| <span data-ttu-id="9895e-154">ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="9895e-154">ASN.1 Type</span></span>         | <span data-ttu-id="9895e-155">SNMPv2-SMI-S</span><span class="sxs-lookup"><span data-stu-id="9895e-155">SNMPv2-SMI</span></span>  | <span data-ttu-id="9895e-156">Integer32、IpAddress、Counter32、TimeTicks、不透明、Counter64、Unsigned32、Gauge32</span><span class="sxs-lookup"><span data-stu-id="9895e-156">Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32</span></span>                                                                                                                             |
| <span data-ttu-id="9895e-157">ASN. 1 宏</span><span class="sxs-lookup"><span data-stu-id="9895e-157">ASN.1 Macro</span></span>        | <span data-ttu-id="9895e-158">SNMPv2-SMI-S</span><span class="sxs-lookup"><span data-stu-id="9895e-158">SNMPv2-SMI</span></span>  | <span data-ttu-id="9895e-159">模組-身分識別，物件-身分識別，物件類型，通知類型</span><span class="sxs-lookup"><span data-stu-id="9895e-159">MODULE-IDENTITY, OBJECT-IDENTITY, OBJECT-TYPE, NOTIFICATION-TYPE</span></span>                                                                                                                                               |
|                    | <span data-ttu-id="9895e-160">SNMPv2-會議</span><span class="sxs-lookup"><span data-stu-id="9895e-160">SNMPv2-CONF</span></span> | <span data-ttu-id="9895e-161">物件群組、通知群組、模組相容性、代理程式功能</span><span class="sxs-lookup"><span data-stu-id="9895e-161">OBJECT-GROUP, NOTIFICATION-GROUP, MODULE-COMPLIANCE, AGENT-CAPABILITIES</span></span>                                                                                                                                        |
|                    | <span data-ttu-id="9895e-162">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="9895e-162">SNMPv2-TC</span></span>   | <span data-ttu-id="9895e-163">文字慣例</span><span class="sxs-lookup"><span data-stu-id="9895e-163">TEXTUAL-CONVENTION</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="9895e-164">文字慣例</span><span class="sxs-lookup"><span data-stu-id="9895e-164">Textual Convention</span></span> | <span data-ttu-id="9895e-165">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="9895e-165">SNMPv2-TC</span></span>   | <span data-ttu-id="9895e-166">DisplayString、PhysAddress、MacAddress、TruthValue、TestAndIncr、AutonomousType、InstancePointer、VariablePointer、RowPointer、RowStatus、TimeStamp、TimeInterval、>formatting.dateandtime.custom、StorageType、Tdomain、Taddress</span><span class="sxs-lookup"><span data-stu-id="9895e-166">DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain, Taddress</span></span> |
|                    | <span data-ttu-id="9895e-167">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="9895e-167">SNMPv2-TM</span></span>   | <span data-ttu-id="9895e-168">SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="9895e-168">SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress</span></span>                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a><span data-ttu-id="9895e-169">嚴重錯誤1032</span><span class="sxs-lookup"><span data-stu-id="9895e-169">Fatal Error 1032</span></span>

<dl> <dt>

<span data-ttu-id="9895e-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032、嚴重>：「 <fileName><行 \#>： <value> 列舉中的重複值」**</span><span class="sxs-lookup"><span data-stu-id="9895e-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, Fatal>: "<fileName><line\#>: Duplicate value <value> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="9895e-171">列舉中的模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。</span><span class="sxs-lookup"><span data-stu-id="9895e-171">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9895e-172">不得有任何重複的值。</span><span class="sxs-lookup"><span data-stu-id="9895e-172">There must not be any duplicate values.</span></span> <span data-ttu-id="9895e-173"><行 \#> 參數是名稱/值的週期位置。</span><span class="sxs-lookup"><span data-stu-id="9895e-173">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="fatal-error-1033"></a><span data-ttu-id="9895e-174">嚴重錯誤1033</span><span class="sxs-lookup"><span data-stu-id="9895e-174">Fatal Error 1033</span></span>

<dl> <dt>

<span data-ttu-id="9895e-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033、嚴重>：「 <fileName><行 \#>： <identifier> 列舉中的重複名稱」**</span><span class="sxs-lookup"><span data-stu-id="9895e-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, Fatal>: "<fileName><line\#>: Duplicate name <identifier> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="9895e-176">列舉中的模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。</span><span class="sxs-lookup"><span data-stu-id="9895e-176">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9895e-177">不得有任何重複的名稱。</span><span class="sxs-lookup"><span data-stu-id="9895e-177">There must not be any duplicate names.</span></span> <span data-ttu-id="9895e-178"><行 \#> 參數是名稱/值的週期位置。</span><span class="sxs-lookup"><span data-stu-id="9895e-178">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="warning-1034"></a><span data-ttu-id="9895e-179">警告1034</span><span class="sxs-lookup"><span data-stu-id="9895e-179">Warning 1034</span></span>

<dl> <dt>

<span data-ttu-id="9895e-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034，警告>：「 <fileName><行 \#>：列舉中不允許有0值」**</span><span class="sxs-lookup"><span data-stu-id="9895e-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Warning>: "<fileName><line\#>: A value of 0 disallowed in an enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="9895e-181">列舉中的模組語義警告，特定于 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="9895e-181">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9895e-182">建議您不要在列舉中使用指名的值零。</span><span class="sxs-lookup"><span data-stu-id="9895e-182">It is recommended that a named value of zero not be used in an enumeration.</span></span>

</dd> </dl>

## <a name="warning-1036"></a><span data-ttu-id="9895e-183">警告1036</span><span class="sxs-lookup"><span data-stu-id="9895e-183">Warning 1036</span></span>

<dl> <dt>

<span data-ttu-id="9895e-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036，警告> 「 <fileName><行 \#>：列舉中的值無法解析為正整數」**</span><span class="sxs-lookup"><span data-stu-id="9895e-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, Warning> "<fileName><line\#>: Value in enumeration does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="9895e-185">列舉中的模組語義警告，特定于 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="9895e-185">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9895e-186">列舉中不允許負數值。</span><span class="sxs-lookup"><span data-stu-id="9895e-186">A negative value is not allowed in an enumeration.</span></span>

</dd> </dl>

## <a name="fatal-error-1037"></a><span data-ttu-id="9895e-187">嚴重錯誤1037</span><span class="sxs-lookup"><span data-stu-id="9895e-187">Fatal Error 1037</span></span>

<dl> <dt>

<span data-ttu-id="9895e-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037、嚴重>：「 <fileName><行 \#>：識別碼 <identifier> 無法解析為八位字串或不透明的類型」**</span><span class="sxs-lookup"><span data-stu-id="9895e-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to OCTET STRING or Opaque types"**</span></span>
</dt> <dd>

<span data-ttu-id="9895e-189">錯誤規格中的模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="9895e-189">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9895e-190">大小規格中使用的符號必須解析為八位字串或不透明。</span><span class="sxs-lookup"><span data-stu-id="9895e-190">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span>

</dd> </dl>

## <a name="fatal-error-1038"></a><span data-ttu-id="9895e-191">嚴重錯誤1038</span><span class="sxs-lookup"><span data-stu-id="9895e-191">Fatal Error 1038</span></span>

<dl> <dt>

<span data-ttu-id="9895e-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038、嚴重>：「 <fileName><行 \#>：識別碼 <identifier> 無法解析整數或量測計類型」**</span><span class="sxs-lookup"><span data-stu-id="9895e-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve an INTEGER or Gauge type"**</span></span>
</dt> <dd>

<span data-ttu-id="9895e-193">範圍規格中的模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="9895e-193">Module semantic error in range specification.</span></span> <span data-ttu-id="9895e-194">這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。</span><span class="sxs-lookup"><span data-stu-id="9895e-194">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

<span data-ttu-id="9895e-195">在 SNMPv1 中，範圍規格中使用的符號必須解析為整數或量測計。</span><span class="sxs-lookup"><span data-stu-id="9895e-195">In SNMPv1, the symbol used in a Range specification must resolve to INTEGER or Gauge.</span></span>

<span data-ttu-id="9895e-196">在 SNMPv2C 中，範圍規格中使用的符號必須解析為整數、Gauge32、Integer32 或 Unsigned32。</span><span class="sxs-lookup"><span data-stu-id="9895e-196">In SNMPv2C, the symbol used in a Range specification must resolve to INTEGER, Gauge32, Integer32, or Unsigned32.</span></span>

</dd> </dl>

## <a name="fatal-error-1039"></a><span data-ttu-id="9895e-197">嚴重錯誤1039</span><span class="sxs-lookup"><span data-stu-id="9895e-197">Fatal Error 1039</span></span>

<dl> <dt>

<span data-ttu-id="9895e-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039、嚴重>： <fileName><行 \#>：大小規格中使用的負數值 "**</span><span class="sxs-lookup"><span data-stu-id="9895e-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, Fatal>:<fileName><line\#>: Negative value used in SIZE specification"**</span></span>
</dt> <dd>

<span data-ttu-id="9895e-199">錯誤規格中的模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="9895e-199">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9895e-200">用來指定大小的任何值都必須為非負數。</span><span class="sxs-lookup"><span data-stu-id="9895e-200">Any value used in specifying the SIZE must be non-negative.</span></span>

</dd> </dl>

## <a name="fatal-error-1040"></a><span data-ttu-id="9895e-201">嚴重錯誤1040</span><span class="sxs-lookup"><span data-stu-id="9895e-201">Fatal Error 1040</span></span>

<dl> <dt>

<span data-ttu-id="9895e-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040，嚴重>：「 <fileName><行 \#>： <identifier> 大小規格中的識別碼無法解析為非負整數值」**</span><span class="sxs-lookup"><span data-stu-id="9895e-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, Fatal>: "<fileName><line\#>: Identifier <identifier> in SIZE specification does not resolve to a non-negative integral value"**</span></span>
</dt> <dd>

<span data-ttu-id="9895e-203">範圍或大小規格中的模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="9895e-203">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9895e-204">在大小規格中用來指定值的任何符號都會解析為非負數值。</span><span class="sxs-lookup"><span data-stu-id="9895e-204">Any symbol used in specifying a value in a SIZE specification resolves to a non-negative value.</span></span>

</dd> </dl>

 

 



