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
# <a name="errors-1061-through-1070"></a><span data-ttu-id="94904-103">錯誤1061到1070</span><span class="sxs-lookup"><span data-stu-id="94904-103">Errors 1061 through 1070</span></span>

<span data-ttu-id="94904-104">描述 WMI SNMP 提供者錯誤1061到1070。</span><span class="sxs-lookup"><span data-stu-id="94904-104">Describes WMI SNMP provider errors 1061 through 1070.</span></span>

[<span data-ttu-id="94904-105">嚴重錯誤1063</span><span class="sxs-lookup"><span data-stu-id="94904-105">Fatal Error 1063</span></span>](#fatal-error-1063)

[<span data-ttu-id="94904-106">嚴重錯誤1064</span><span class="sxs-lookup"><span data-stu-id="94904-106">Fatal Error 1064</span></span>](#fatal-error-1064)

[<span data-ttu-id="94904-107">嚴重錯誤1070</span><span class="sxs-lookup"><span data-stu-id="94904-107">Fatal Error 1070</span></span>](#fatal-error-1070)

## <a name="fatal-error-1063"></a><span data-ttu-id="94904-108">嚴重錯誤1063</span><span class="sxs-lookup"><span data-stu-id="94904-108">Fatal Error 1063</span></span>

<dl> <dt>

<span data-ttu-id="94904-109"><span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063、嚴重>：「 <fileName><行 \#>：大小規格的上限小於下限」**</span><span class="sxs-lookup"><span data-stu-id="94904-109"><span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, Fatal>: "<fileName><line\#>: Upper bound of SIZE specification is less than the lower bound"**</span></span>
</dt> <dd>

<span data-ttu-id="94904-110">錯誤規格中的模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="94904-110">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="94904-111">大小規格中使用的符號必須解析為八位字串或不透明。</span><span class="sxs-lookup"><span data-stu-id="94904-111">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="94904-112">範圍或大小規格的下限不得大於上限。</span><span class="sxs-lookup"><span data-stu-id="94904-112">The lower bound of a range or SIZE specification must be no greater than the upper bound.</span></span>

</dd> </dl>

## <a name="fatal-error-1064"></a><span data-ttu-id="94904-113">嚴重錯誤1064</span><span class="sxs-lookup"><span data-stu-id="94904-113">Fatal Error 1064</span></span>

<dl> <dt>

<span data-ttu-id="94904-114"><span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064，嚴重>： " <fileName> ： <行 \#>：順序專案 <identifier> 無法解析為物件類型"**</span><span class="sxs-lookup"><span data-stu-id="94904-114"><span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, Fatal>: "<fileName>:<line\#>: SEQUENCE item <identifier> does not resolve to an OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="94904-115">類型指派模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。</span><span class="sxs-lookup"><span data-stu-id="94904-115">Type assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="94904-116">順序宣告的所有個別元素都必須解析為物件類型。</span><span class="sxs-lookup"><span data-stu-id="94904-116">All of the individual elements of a SEQUENCE declaration must resolve to an OBJECT-TYPE.</span></span>

</dd> </dl>

## <a name="fatal-error-1070"></a><span data-ttu-id="94904-117">嚴重錯誤1070</span><span class="sxs-lookup"><span data-stu-id="94904-117">Fatal Error 1070</span></span>

<dl> <dt>

<span data-ttu-id="94904-118"><span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070，嚴重>：「 <fileName><行 \#>： MIB 模組 <moduleName> ，其中的符號 <symbolName> 已匯入，且不存在於輸入中」**</span><span class="sxs-lookup"><span data-stu-id="94904-118"><span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, Fatal>: "<fileName><line\#>: MIB Module <moduleName>, from which symbol <symbolName> is imported, is not present in input"**</span></span>
</dt> <dd>

<span data-ttu-id="94904-119">交互參照中的模組語意錯誤，不是 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="94904-119">Module semantic error in cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="94904-120">如果主要模組或子公司模組的 [匯入] 區段中的其中一個模組不存在，而且實際參考此模組中的一或多個符號，就會發生這個嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="94904-120">If one of the modules in the IMPORTS section of the main module or a subsidiary module does not exist and one or more symbols from this module are actually referenced, this fatal error occurs.</span></span>

</dd> </dl>

 

 



