---
description: 描述 WMI SNMP 提供者錯誤1091到1100。
ms.assetid: 9b7db4fc-8ae8-46f7-a40f-e4401a335c5d
ms.tgt_platform: multiple
title: 錯誤1091到1100
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf582a3df41fbc7c329f5a993555a2d76145ded0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986626"
---
# <a name="errors-1091-through-1100"></a><span data-ttu-id="68e69-103">錯誤1091到1100</span><span class="sxs-lookup"><span data-stu-id="68e69-103">Errors 1091 through 1100</span></span>

<span data-ttu-id="68e69-104">描述 WMI SNMP 提供者錯誤1091到1100。</span><span class="sxs-lookup"><span data-stu-id="68e69-104">Describes WMI SNMP provider errors 1091 through 1100.</span></span>

[<span data-ttu-id="68e69-105">警告1091</span><span class="sxs-lookup"><span data-stu-id="68e69-105">Warning 1091</span></span>](#warning-1091)

[<span data-ttu-id="68e69-106">嚴重錯誤1092</span><span class="sxs-lookup"><span data-stu-id="68e69-106">Fatal Error 1092</span></span>](#fatal-error-1092)

[<span data-ttu-id="68e69-107">嚴重錯誤1093</span><span class="sxs-lookup"><span data-stu-id="68e69-107">Fatal Error 1093</span></span>](#fatal-error-1093)

[<span data-ttu-id="68e69-108">嚴重錯誤1094</span><span class="sxs-lookup"><span data-stu-id="68e69-108">Fatal Error 1094</span></span>](#fatal-error-1094)

[<span data-ttu-id="68e69-109">嚴重錯誤1095</span><span class="sxs-lookup"><span data-stu-id="68e69-109">Fatal Error 1095</span></span>](#fatal-error-1095)

[<span data-ttu-id="68e69-110">嚴重錯誤1097</span><span class="sxs-lookup"><span data-stu-id="68e69-110">Fatal Error 1097</span></span>](#fatal-error-1097)

[<span data-ttu-id="68e69-111">嚴重錯誤1098</span><span class="sxs-lookup"><span data-stu-id="68e69-111">Fatal Error 1098</span></span>](#fatal-error-1098)

[<span data-ttu-id="68e69-112">嚴重錯誤1099</span><span class="sxs-lookup"><span data-stu-id="68e69-112">Fatal Error 1099</span></span>](#fatal-error-1099)

## <a name="warning-1091"></a><span data-ttu-id="68e69-113">警告1091</span><span class="sxs-lookup"><span data-stu-id="68e69-113">Warning 1091</span></span>

<dl> <dt>

<span data-ttu-id="68e69-114"><span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091，警告>： " <fileName> ： \# 不允許固定大小物件使用 <行> 默示子句」**</span><span class="sxs-lookup"><span data-stu-id="68e69-114"><span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, Warning>: "<fileName>:<line\#> IMPLIED clause is not allowed for fixed size objects"**</span></span>
</dt> <dd>

<span data-ttu-id="68e69-115">**物件類型** 宏調用 SNMPv2C 特定模組語義警告。</span><span class="sxs-lookup"><span data-stu-id="68e69-115">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic warning.</span></span> <span data-ttu-id="68e69-116">只有在索引子句中具有可變長度語法的物件（例如物件識別碼或可變長度的八位字串）時，才會出現隱含關鍵字。</span><span class="sxs-lookup"><span data-stu-id="68e69-116">The IMPLIED keyword can only be present for an object having a variable-length syntax, such as an OBJECT IDENTIFIER or variable-length OCTET STRING, in the INDEX clause.</span></span>

</dd> </dl>

## <a name="fatal-error-1092"></a><span data-ttu-id="68e69-117">嚴重錯誤1092</span><span class="sxs-lookup"><span data-stu-id="68e69-117">Fatal Error 1092</span></span>

<dl> <dt>

<span data-ttu-id="68e69-118"><span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092、嚴重>： " <fileName> ： \# 不允許有零長度物件的 <行> 默示子句」**</span><span class="sxs-lookup"><span data-stu-id="68e69-118"><span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092, Fatal>: "<fileName>:<line\#> IMPLIED clause not allowed for potentially zero-length objects"**</span></span>
</dt> <dd>

<span data-ttu-id="68e69-119">**物件類型** 宏調用 SNMPv2C 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="68e69-119">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="68e69-120">如果物件的長度為零，則不能在可變長度的物件上使用隱含的子句。</span><span class="sxs-lookup"><span data-stu-id="68e69-120">The IMPLIED clause cannot be used on a variable-length object if that object can have a zero length.</span></span>

</dd> </dl>

## <a name="fatal-error-1093"></a><span data-ttu-id="68e69-121">嚴重錯誤1093</span><span class="sxs-lookup"><span data-stu-id="68e69-121">Fatal Error 1093</span></span>

<dl> <dt>

<span data-ttu-id="68e69-122"><span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093。嚴重>：「 <fileName><行 \#>：只能根據 V1 smi-s 來列舉類型 "INTEGER"**</span><span class="sxs-lookup"><span data-stu-id="68e69-122"><span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093. Fatal>: "<fileName><line\#>: Only the type "INTEGER" can be enumerated according to the V1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="68e69-123">類型指派，SNMPv1 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="68e69-123">Type assignment, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="68e69-124">SNMPv1 MIB 列舉只能使用整數類型。</span><span class="sxs-lookup"><span data-stu-id="68e69-124">An SNMPv1 MIB enumeration can use only the type INTEGER.</span></span>

</dd> </dl>

## <a name="fatal-error-1094"></a><span data-ttu-id="68e69-125">嚴重錯誤1094</span><span class="sxs-lookup"><span data-stu-id="68e69-125">Fatal Error 1094</span></span>

<dl> <dt>

<span data-ttu-id="68e69-126"><span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094。嚴重>：「 <fileName><行 \#>：列舉中使用的類型不會解析為其中一個允許的類型」**</span><span class="sxs-lookup"><span data-stu-id="68e69-126"><span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094. Fatal>: "<fileName><line\#>: The type used in the enumeration does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="68e69-127">類型指派，SNMPv2C 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="68e69-127">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="68e69-128">列舉中使用的型別必須是整數或對等的型別，或是另一個列舉。</span><span class="sxs-lookup"><span data-stu-id="68e69-128">The type used in an enumeration must be INTEGER or an equivalent type, or another enumeration.</span></span>

</dd> </dl>

## <a name="fatal-error-1095"></a><span data-ttu-id="68e69-129">嚴重錯誤1095</span><span class="sxs-lookup"><span data-stu-id="68e69-129">Fatal Error 1095</span></span>

<dl> <dt>

<span data-ttu-id="68e69-130"><span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095。嚴重>：「 <fileName><行 \#>：列舉成員不是父列舉的成員」**</span><span class="sxs-lookup"><span data-stu-id="68e69-130"><span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095. Fatal>: "<fileName><line\#>: Enumeration member is not a member of the parent enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="68e69-131">類型指派，SNMPv2C 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="68e69-131">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="68e69-132">如果使用另一個列舉，其一組專案必須是父列舉專案集合的子集。</span><span class="sxs-lookup"><span data-stu-id="68e69-132">If another enumeration is used, its set of items must be a subset of the parent enumeration's set of items.</span></span>

</dd> </dl>

## <a name="fatal-error-1097"></a><span data-ttu-id="68e69-133">嚴重錯誤1097</span><span class="sxs-lookup"><span data-stu-id="68e69-133">Fatal Error 1097</span></span>

<dl> <dt>

<span data-ttu-id="68e69-134"><span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097、嚴重>：「 <fileName><行 \#>：識別碼 <name> 無法解析為整數值」**</span><span class="sxs-lookup"><span data-stu-id="68e69-134"><span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097, Fatal>: "<fileName><line\#>: identifier <name> does not resolve to an integer value"**</span></span>
</dt> <dd>

<span data-ttu-id="68e69-135">類型指派，SNMPv2C 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="68e69-135">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="68e69-136">位類型中的值必須是整數值。</span><span class="sxs-lookup"><span data-stu-id="68e69-136">The values in the BITS type must be integer values.</span></span>

</dd> </dl>

## <a name="fatal-error-1098"></a><span data-ttu-id="68e69-137">嚴重錯誤1098</span><span class="sxs-lookup"><span data-stu-id="68e69-137">Fatal Error 1098</span></span>

<dl> <dt>

<span data-ttu-id="68e69-138"><span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098、嚴重>：「 <fileName><行 \#>： <value> 位結構中的重複值」**</span><span class="sxs-lookup"><span data-stu-id="68e69-138"><span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098, Fatal>: "<fileName><line\#>: Duplicate value <value> in BITS construct"**</span></span>
</dt> <dd>

<span data-ttu-id="68e69-139">類型指派，SNMPv2C 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="68e69-139">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="68e69-140">BITS 結構中不能有重複的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="68e69-140">There must be no duplicate names and values in a BITS construct.</span></span> <span data-ttu-id="68e69-141"><行 \#> 參數是名稱/值的週期位置。</span><span class="sxs-lookup"><span data-stu-id="68e69-141">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="fatal-error-1099"></a><span data-ttu-id="68e69-142">嚴重錯誤1099</span><span class="sxs-lookup"><span data-stu-id="68e69-142">Fatal Error 1099</span></span>

<dl> <dt>

<span data-ttu-id="68e69-143"><span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099、嚴重>：「 <fileName><行 \#>： <identifier> 位結構中的重複名稱」**</span><span class="sxs-lookup"><span data-stu-id="68e69-143"><span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099, Fatal>: "<fileName><line\#>: Duplicate name <identifier> in BITS construct"**</span></span>
</dt> <dd>

<span data-ttu-id="68e69-144">類型指派，SNMPv2C 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="68e69-144">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="68e69-145">BITS 結構中不能有重複的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="68e69-145">There must be no duplicate names and values in a BITS construct.</span></span> <span data-ttu-id="68e69-146"><行 \#> 參數是名稱/值的週期位置。</span><span class="sxs-lookup"><span data-stu-id="68e69-146">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

 

 



