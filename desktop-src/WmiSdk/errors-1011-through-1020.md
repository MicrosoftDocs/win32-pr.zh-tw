---
description: 描述 WMI SNMP 提供者錯誤1011到1020。
ms.assetid: 5151a110-1532-48cc-832a-2cee21853b6b
ms.tgt_platform: multiple
title: 錯誤1011到1020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a73f90ce0fc161604d87672fb5b33f9708aa945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027233"
---
# <a name="errors-1011-through-1020"></a><span data-ttu-id="08042-103">錯誤1011到1020</span><span class="sxs-lookup"><span data-stu-id="08042-103">Errors 1011 through 1020</span></span>

<span data-ttu-id="08042-104">描述 WMI SNMP 提供者錯誤1011到1020。</span><span class="sxs-lookup"><span data-stu-id="08042-104">Describes WMI SNMP provider errors 1011 through 1020.</span></span>

[<span data-ttu-id="08042-105">嚴重錯誤1011</span><span class="sxs-lookup"><span data-stu-id="08042-105">Fatal Error 1011</span></span>](#fatal-error-1011)

[<span data-ttu-id="08042-106">嚴重錯誤1012</span><span class="sxs-lookup"><span data-stu-id="08042-106">Fatal Error 1012</span></span>](#fatal-error-1012)

[<span data-ttu-id="08042-107">嚴重錯誤1013</span><span class="sxs-lookup"><span data-stu-id="08042-107">Fatal Error 1013</span></span>](#fatal-error-1013)

[<span data-ttu-id="08042-108">警告1014</span><span class="sxs-lookup"><span data-stu-id="08042-108">Warning 1014</span></span>](#warning-1014)

[<span data-ttu-id="08042-109">嚴重錯誤1015</span><span class="sxs-lookup"><span data-stu-id="08042-109">Fatal Error 1015</span></span>](#fatal-error-1015)

[<span data-ttu-id="08042-110">嚴重錯誤1016</span><span class="sxs-lookup"><span data-stu-id="08042-110">Fatal Error 1016</span></span>](#fatal-error-1016)

[<span data-ttu-id="08042-111">嚴重錯誤1018</span><span class="sxs-lookup"><span data-stu-id="08042-111">Fatal Error 1018</span></span>](#fatal-error-1018)

[<span data-ttu-id="08042-112">嚴重錯誤1020</span><span class="sxs-lookup"><span data-stu-id="08042-112">Fatal Error 1020</span></span>](#fatal-error-1020)

## <a name="fatal-error-1011"></a><span data-ttu-id="08042-113">嚴重錯誤1011</span><span class="sxs-lookup"><span data-stu-id="08042-113">Fatal Error 1011</span></span>

<dl> <dt>

<span data-ttu-id="08042-114"><span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011、嚴重>： " <fileName> ： <行 \#> SEQUENCE 成員的語法， <identifier> <identifier> 與物件類型的語法子句不同」**</span><span class="sxs-lookup"><span data-stu-id="08042-114"><span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011, Fatal>: "<fileName>:<line\#> the SYNTAX of member <identifier> of SEQUENCE, <identifier>, differs from the SYNTAX clause of the OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="08042-115">**物件類型** 宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="08042-115">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="08042-116">序列的專案必須與物件類型定義的語法子句中的型別相同。</span><span class="sxs-lookup"><span data-stu-id="08042-116">An element of a SEQUENCE must be same as the type in the SYNTAX clause of the OBJECT-TYPE definition.</span></span> <span data-ttu-id="08042-117"><行 \#> 參數是物件類型定義的語法子句的行。</span><span class="sxs-lookup"><span data-stu-id="08042-117">The <line\#> parameter is the line of the SYNTAX clause of the OBJECT-TYPE definition.</span></span>

<span data-ttu-id="08042-118">這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。</span><span class="sxs-lookup"><span data-stu-id="08042-118">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1012"></a><span data-ttu-id="08042-119">嚴重錯誤1012</span><span class="sxs-lookup"><span data-stu-id="08042-119">Fatal Error 1012</span></span>

<dl> <dt>

<span data-ttu-id="08042-120"><span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012、嚴重>： " <fileName> ： <行 \#> 索引或增強子句僅適用于 SEQUENCE 物件類型"**</span><span class="sxs-lookup"><span data-stu-id="08042-120"><span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012, Fatal>: "<fileName>:<line\#> An INDEX or AUGMENTS clause is required only for SEQUENCE OBJECT-TYPES"**</span></span>
</dt> <dd>

<span data-ttu-id="08042-121">**物件類型** 宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="08042-121">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="08042-122">索引子句必須只存在於其語法解析為序列類型的物件類型定義中。</span><span class="sxs-lookup"><span data-stu-id="08042-122">An INDEX clause must only be present in an OBJECT-TYPE definition whose SYNTAX resolves to a SEQUENCE type.</span></span>

<span data-ttu-id="08042-123">編譯 SNMPv1 或 SNMPv2C MIB 時，會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="08042-123">This error can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

</dd> </dl>

## <a name="fatal-error-1013"></a><span data-ttu-id="08042-124">嚴重錯誤1013</span><span class="sxs-lookup"><span data-stu-id="08042-124">Fatal Error 1013</span></span>

<dl> <dt>

<span data-ttu-id="08042-125"><span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013，嚴重>：「 <fileName><行 \#>： <identifier> 應解析為序列類型」**</span><span class="sxs-lookup"><span data-stu-id="08042-125"><span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013, Fatal>: "<fileName><line\#>: <identifier> should resolve to a SEQUENCE type"**</span></span>
</dt> <dd>

<span data-ttu-id="08042-126">**物件類型** 宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="08042-126">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="08042-127">「序列」結構中使用的型別必須解析為序列型別。</span><span class="sxs-lookup"><span data-stu-id="08042-127">A type used in the "SEQUENCE OF" construct must resolve to a SEQUENCE type.</span></span>

<span data-ttu-id="08042-128">這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。</span><span class="sxs-lookup"><span data-stu-id="08042-128">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="warning-1014"></a><span data-ttu-id="08042-129">警告1014</span><span class="sxs-lookup"><span data-stu-id="08042-129">Warning 1014</span></span>

<dl> <dt>

<span data-ttu-id="08042-130"><span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014，警告>： " <fileName> ： <行 \#>： oid 中不建議是值0的子識別碼"**</span><span class="sxs-lookup"><span data-stu-id="08042-130"><span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, Warning>: "<fileName>:<line\#>: Sub-identifier of value 0 not recommended in OIDs"**</span></span>
</dt> <dd>

<span data-ttu-id="08042-131">**物件類型** 宏調用模組語義警告。</span><span class="sxs-lookup"><span data-stu-id="08042-131">**OBJECT-TYPE** macro invocation module semantic warning.</span></span> <span data-ttu-id="08042-132">建議網際網路標準 MIB 中的物件在其物件識別碼中使用零的子識別碼。</span><span class="sxs-lookup"><span data-stu-id="08042-132">It is recommended that no object in an Internet Standard MIB use a sub-identifier of zero in its OBJECT IDENTIFIER.</span></span>

<span data-ttu-id="08042-133">此警告可能會在 SNMPv1 或 SNMPv2C 中發生。</span><span class="sxs-lookup"><span data-stu-id="08042-133">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1015"></a><span data-ttu-id="08042-134">嚴重錯誤1015</span><span class="sxs-lookup"><span data-stu-id="08042-134">Fatal Error 1015</span></span>

<dl> <dt>

<span data-ttu-id="08042-135"><span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015，嚴重>： " <fileName> ： <行 \#>： <identifier> 來自模組 <identifier> 和 <identifier> 模組的 OBJECT-TYPEs <identifier> 都會指派相同的 OID 值」**</span><span class="sxs-lookup"><span data-stu-id="08042-135"><span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015, Fatal>: "<fileName>:<line\#>: OBJECT-TYPEs <identifier> from module <identifier> and <identifier> from module <identifier> are assigned the same OID values"**</span></span>
</dt> <dd>

<span data-ttu-id="08042-136">**物件類型** 宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="08042-136">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="08042-137">在相同或不同模組中 (兩個 **物件類型** 調用) 不得指派相同的物件識別碼值。</span><span class="sxs-lookup"><span data-stu-id="08042-137">Two **OBJECT-TYPE** invocations (in the same or different modules) must not be assigned the same Object Identifier value.</span></span>

<span data-ttu-id="08042-138">這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。</span><span class="sxs-lookup"><span data-stu-id="08042-138">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1016"></a><span data-ttu-id="08042-139">嚴重錯誤1016</span><span class="sxs-lookup"><span data-stu-id="08042-139">Fatal Error 1016</span></span>

<dl> <dt>

<span data-ttu-id="08042-140"><span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016，嚴重>： " <fileName> ： <行 \#>： DEFVAL 子句中的值不符合語法子句中的類型"**</span><span class="sxs-lookup"><span data-stu-id="08042-140"><span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016, Fatal>: "<fileName>:<line\#>: Value in the DEFVAL clause does not match the type in the SYNTAX clause"**</span></span>
</dt> <dd>

<span data-ttu-id="08042-141">**物件類型** 宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="08042-141">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="08042-142">DEFVAL 子句中的值必須是語法子句中所述之類型的值。</span><span class="sxs-lookup"><span data-stu-id="08042-142">A value in a DEFVAL clause must be a value of the type mentioned in the SYNTAX clause.</span></span>

<span data-ttu-id="08042-143">這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。</span><span class="sxs-lookup"><span data-stu-id="08042-143">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1018"></a><span data-ttu-id="08042-144">嚴重錯誤1018</span><span class="sxs-lookup"><span data-stu-id="08042-144">Fatal Error 1018</span></span>

<dl> <dt>

<span data-ttu-id="08042-145"><span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018，嚴重>： " <fileName><行 \#>： <symbol> 在 [在下列情況下的企業子句中，不會解析為 OID 值]**</span><span class="sxs-lookup"><span data-stu-id="08042-145"><span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018, Fatal>: "<fileName><line\#>: <symbol> in ENTERPRISE clause of TRAP-TYPE does not resolve to an OID value"**</span></span>
</dt> <dd>

<span data-ttu-id="08042-146">**陷阱類型** 宏調用，SNMPv1 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="08042-146">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="08042-147">在 **TRAP 類型** 宏調用的 ENTERPRISE 子句中使用的符號必須解析為物件識別碼值。</span><span class="sxs-lookup"><span data-stu-id="08042-147">The symbol used in the ENTERPRISE clause of a **TRAP-TYPE** macro invocation must resolve to an Object Identifier value.</span></span>

</dd> </dl>

## <a name="fatal-error-1020"></a><span data-ttu-id="08042-148">嚴重錯誤1020</span><span class="sxs-lookup"><span data-stu-id="08042-148">Fatal Error 1020</span></span>

<dl> <dt>

<span data-ttu-id="08042-149"><span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020，嚴重>：「 <fileName><行 \#>：指派給陷阱類型的值 <identifier> 無法解析為正整數」**</span><span class="sxs-lookup"><span data-stu-id="08042-149"><span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020, Fatal>: "<fileName><line\#>: Value assigned to TRAP-TYPE <identifier> does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="08042-150">**陷阱類型** 宏調用，SNMPv1 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="08042-150">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="08042-151">用來指定陷阱值的符號不會解析為正整數。</span><span class="sxs-lookup"><span data-stu-id="08042-151">A symbol used in specifying the trap value does not resolve to a positive integer.</span></span>

</dd> </dl>

 

 



