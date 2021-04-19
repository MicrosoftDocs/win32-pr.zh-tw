---
description: 描述 WMI SNMP 提供者錯誤1061到1070。
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: 錯誤1061到1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a4bf0773ade1f62eb11f0c496aea340410c4a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992441"
---
# <a name="errors-1061-through-1070"></a>錯誤1061到1070

描述 WMI SNMP 提供者錯誤1061到1070。

[嚴重錯誤1063](#fatal-error-1063)

[嚴重錯誤1064](#fatal-error-1064)

[嚴重錯誤1070](#fatal-error-1070)

## <a name="fatal-error-1063"></a>嚴重錯誤1063

<dl> <dt>

<span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063、嚴重>：「 <fileName><行 \#>：大小規格的上限小於下限」**
</dt> <dd>

錯誤規格中的模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。 大小規格中使用的符號必須解析為八位字串或不透明。 範圍或大小規格的下限不得大於上限。

</dd> </dl>

## <a name="fatal-error-1064"></a>嚴重錯誤1064

<dl> <dt>

<span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064，嚴重>： " <fileName> ： <行 \#>：順序專案 <identifier> 無法解析為物件類型"**
</dt> <dd>

類型指派模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。 順序宣告的所有個別元素都必須解析為物件類型。

</dd> </dl>

## <a name="fatal-error-1070"></a>嚴重錯誤1070

<dl> <dt>

<span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070，嚴重>：「 <fileName><行 \#>： MIB 模組 <moduleName> ，其中的符號 <symbolName> 已匯入，且不存在於輸入中」**
</dt> <dd>

交互參照中的模組語意錯誤，不是 SNMPv1 或 SNMPv2C。 如果主要模組或子公司模組的 [匯入] 區段中的其中一個模組不存在，而且實際參考此模組中的一或多個符號，就會發生這個嚴重錯誤。

</dd> </dl>

 

 



