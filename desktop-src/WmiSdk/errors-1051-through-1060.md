---
description: 描述 WMI SNMP 提供者錯誤1051到1060。
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: 錯誤1051到1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e75d2fda06b7761fd7e14de936ef7b38fbb18df46dd2597509bc7c1e1502023
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464078"
---
# <a name="errors-1051-through-1060"></a>錯誤1051到1060

描述 WMI SNMP 提供者錯誤1051到1060。

[嚴重錯誤1051](#fatal-error-1051)

[嚴重錯誤1054](#fatal-error-1054)

[嚴重錯誤1055](#fatal-error-1055)

## <a name="fatal-error-1051"></a>嚴重錯誤1051

<dl> <dt>

<span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051、嚴重>： " <fileName> ： <行 \#>：不明確參考符號 <identifier> "**
</dt> <dd>

IMPORTS 區段模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。 對應到網際網路標準 MIB 中物件的每個物件描述項都必須是唯一的。 因為 enterprise Mib 可以有通用的物件描述項，所以必須使用標記法 "module."，在 MIB 模組中明確地使用從兩個模組匯入的這類描述項。

</dd> </dl>

## <a name="fatal-error-1054"></a>嚴重錯誤1054

<dl> <dt>

<span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054，嚴重>： " <fileName> ： <行 \#>： <identifier> in INDEX 子句無法解析為其中一個允許的類型"**
</dt> <dd>

**物件類型** 宏調用模組語意錯誤。 INDEX 子句中的物件類型，或在 INDEX 子句中指定的任何類型，都必須解析成純量類型，也就是非序列或非序列的型別。 INDEX 子句中指定的任何類型也必須解析為其中一種。

這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。

</dd> </dl>

## <a name="fatal-error-1055"></a>嚴重錯誤1055

<dl> <dt>

<span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055，嚴重>： " <fileName> ： <行 \#>： INDEX 物件類型的語法 <identifier> 不會解析為其中一個允許的類型"**
</dt> <dd>

**物件類型** 宏調用模組語意錯誤。 INDEX 子句中的物件類型，或在 INDEX 子句中指定的任何類型，都必須解析成純量類型，也就是非序列或非序列的型別。

這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。

</dd> </dl>

 

 



