---
description: 描述 WMI SNMP 提供者錯誤231到240。
ms.assetid: edb3dabb-6a65-4285-97d3-f7025d3bb5da
ms.tgt_platform: multiple
title: 錯誤231到240
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d053cac57eec9d0055dec56bbfab8304ad3f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194705"
---
# <a name="errors-231-through-240"></a>錯誤231到240

描述 WMI SNMP 提供者錯誤231到240。

[嚴重錯誤232](#fatal-error-232)

[嚴重錯誤233](#fatal-error-233)

[嚴重錯誤234](#fatal-error-234)

[嚴重錯誤236](#fatal-error-236)

## <a name="fatal-error-232"></a>嚴重錯誤232

<dl> <dt>

<span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232、嚴重>： " <fileName> ： <行 \#>： SNMPV1 smi-s 物件的調用-不允許的類型"**
</dt> <dd>

模組語法錯誤。 您已在 MIB 中使用 SNMPv1 特定的 **物件類型** 調用，但指定了 **/v2c** 參數，這需要嚴格符合 SNMPv2C 語法。

</dd> </dl>

## <a name="fatal-error-233"></a>嚴重錯誤233

<dl> <dt>

<span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233、嚴重>： " <fileName> ： <行 \#>： SNMPV1 smi-s 陷阱的調用-不允許的類型"**
</dt> <dd>

模組語法錯誤。 您已在 MIB 中使用 SNMPv1 特定的 **陷阱類型** 調用，但指定了 **/v2c** 參數，這需要嚴格符合 SNMPv2C 語法。

</dd> </dl>

## <a name="fatal-error-234"></a>嚴重錯誤234

<dl> <dt>

<span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234，嚴重>： " <fileName> ： <行 \#>：模組-身分識別調用只允許緊接在 IMPORTS 區段"**
</dt> <dd>

模組語法錯誤。 **模組識別** 調用已錯置。

</dd> </dl>

## <a name="fatal-error-236"></a>嚴重錯誤236

<dl> <dt>

<span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236、嚴重>： " <fileName> ： <行 \#>：數位不符合編譯器所使用的32位標記法」**
</dt> <dd>

值指派中的模組語法錯誤。 有一個 MIB 值指派錯誤，其中整數值很大，因此需要超過32個位才能代表它。

</dd> </dl>

 

 



