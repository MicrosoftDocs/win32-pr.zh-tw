---
description: 描述 WMI SNMP 提供者錯誤1051到1060。
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: 錯誤1051到1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170eddf3126a40f929aa36899259b731fa244941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978280"
---
# <a name="errors-1051-through-1060"></a><span data-ttu-id="eb2c3-103">錯誤1051到1060</span><span class="sxs-lookup"><span data-stu-id="eb2c3-103">Errors 1051 through 1060</span></span>

<span data-ttu-id="eb2c3-104">描述 WMI SNMP 提供者錯誤1051到1060。</span><span class="sxs-lookup"><span data-stu-id="eb2c3-104">Describes WMI SNMP provider errors 1051 through 1060.</span></span>

[<span data-ttu-id="eb2c3-105">嚴重錯誤1051</span><span class="sxs-lookup"><span data-stu-id="eb2c3-105">Fatal Error 1051</span></span>](#fatal-error-1051)

[<span data-ttu-id="eb2c3-106">嚴重錯誤1054</span><span class="sxs-lookup"><span data-stu-id="eb2c3-106">Fatal Error 1054</span></span>](#fatal-error-1054)

[<span data-ttu-id="eb2c3-107">嚴重錯誤1055</span><span class="sxs-lookup"><span data-stu-id="eb2c3-107">Fatal Error 1055</span></span>](#fatal-error-1055)

## <a name="fatal-error-1051"></a><span data-ttu-id="eb2c3-108">嚴重錯誤1051</span><span class="sxs-lookup"><span data-stu-id="eb2c3-108">Fatal Error 1051</span></span>

<dl> <dt>

<span data-ttu-id="eb2c3-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051、嚴重>： " <fileName> ： <行 \#>：不明確參考符號 <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="eb2c3-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Fatal>: "<fileName>:<line\#>: Ambiguous reference to symbol <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="eb2c3-110">IMPORTS 區段模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="eb2c3-110">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="eb2c3-111">對應到網際網路標準 MIB 中物件的每個物件描述項都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="eb2c3-111">Each object descriptor corresponding to an object in an Internet Standard MIB must be unique.</span></span> <span data-ttu-id="eb2c3-112">因為 enterprise Mib 可以有通用的物件描述項，所以必須使用標記法 "module."，在 MIB 模組中明確地使用從兩個模組匯入的這類描述項。</span><span class="sxs-lookup"><span data-stu-id="eb2c3-112">Since enterprise MIBs can have common object descriptors, such descriptors imported from two modules must be used unambiguously in the MIB module by using the notation "module.descriptor."</span></span>

</dd> </dl>

## <a name="fatal-error-1054"></a><span data-ttu-id="eb2c3-113">嚴重錯誤1054</span><span class="sxs-lookup"><span data-stu-id="eb2c3-113">Fatal Error 1054</span></span>

<dl> <dt>

<span data-ttu-id="eb2c3-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054，嚴重>： " <fileName> ： <行 \#>： <identifier> in INDEX 子句無法解析為其中一個允許的類型"**</span><span class="sxs-lookup"><span data-stu-id="eb2c3-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, Fatal>: "<fileName>:<line\#>: <identifier> in INDEX clause does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="eb2c3-115">**物件類型** 宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb2c3-115">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="eb2c3-116">INDEX 子句中的物件類型，或在 INDEX 子句中指定的任何類型，都必須解析成純量類型，也就是非序列或非序列的型別。</span><span class="sxs-lookup"><span data-stu-id="eb2c3-116">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span> <span data-ttu-id="eb2c3-117">INDEX 子句中指定的任何類型也必須解析為其中一種。</span><span class="sxs-lookup"><span data-stu-id="eb2c3-117">Any type specified in the INDEX clause must also resolve to one of these.</span></span>

<span data-ttu-id="eb2c3-118">這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。</span><span class="sxs-lookup"><span data-stu-id="eb2c3-118">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1055"></a><span data-ttu-id="eb2c3-119">嚴重錯誤1055</span><span class="sxs-lookup"><span data-stu-id="eb2c3-119">Fatal Error 1055</span></span>

<dl> <dt>

<span data-ttu-id="eb2c3-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055，嚴重>： " <fileName> ： <行 \#>： INDEX 物件類型的語法 <identifier> 不會解析為其中一個允許的類型"**</span><span class="sxs-lookup"><span data-stu-id="eb2c3-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, Fatal>:"<fileName>:<line\#>: SYNTAX of INDEX OBJECT-TYPE <identifier>, does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="eb2c3-121">**物件類型** 宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb2c3-121">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="eb2c3-122">INDEX 子句中的物件類型，或在 INDEX 子句中指定的任何類型，都必須解析成純量類型，也就是非序列或非序列的型別。</span><span class="sxs-lookup"><span data-stu-id="eb2c3-122">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span>

<span data-ttu-id="eb2c3-123">這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。</span><span class="sxs-lookup"><span data-stu-id="eb2c3-123">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



