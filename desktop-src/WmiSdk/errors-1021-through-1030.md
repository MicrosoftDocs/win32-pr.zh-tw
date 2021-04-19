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
# <a name="errors-1021-through-1030"></a><span data-ttu-id="68346-103">錯誤1021到1030</span><span class="sxs-lookup"><span data-stu-id="68346-103">Errors 1021 through 1030</span></span>

<span data-ttu-id="68346-104">描述 WMI SNMP 提供者錯誤1021到1033。</span><span class="sxs-lookup"><span data-stu-id="68346-104">Describes WMI SNMP provider errors 1021 through 1033.</span></span>

[<span data-ttu-id="68346-105">嚴重錯誤1021</span><span class="sxs-lookup"><span data-stu-id="68346-105">Fatal Error 1021</span></span>](#fatal-error-1021)

[<span data-ttu-id="68346-106">嚴重錯誤1022</span><span class="sxs-lookup"><span data-stu-id="68346-106">Fatal Error 1022</span></span>](#fatal-error-1022)

[<span data-ttu-id="68346-107">嚴重錯誤1023</span><span class="sxs-lookup"><span data-stu-id="68346-107">Fatal Error 1023</span></span>](#fatal-error-1023)

[<span data-ttu-id="68346-108">嚴重錯誤1024</span><span class="sxs-lookup"><span data-stu-id="68346-108">Fatal Error 1024</span></span>](#fatal-error-1024)

[<span data-ttu-id="68346-109">嚴重錯誤1025</span><span class="sxs-lookup"><span data-stu-id="68346-109">Fatal Error 1025</span></span>](#fatal-error-1025)

[<span data-ttu-id="68346-110">嚴重錯誤1026</span><span class="sxs-lookup"><span data-stu-id="68346-110">Fatal Error 1026</span></span>](#fatal-error-1026)

[<span data-ttu-id="68346-111">警告1027</span><span class="sxs-lookup"><span data-stu-id="68346-111">Warning 1027</span></span>](#warning-1027)

[<span data-ttu-id="68346-112">嚴重錯誤1028</span><span class="sxs-lookup"><span data-stu-id="68346-112">Fatal Error 1028</span></span>](#fatal-error-1028)

[<span data-ttu-id="68346-113">嚴重錯誤1029</span><span class="sxs-lookup"><span data-stu-id="68346-113">Fatal Error 1029</span></span>](#fatal-error-1029)

[<span data-ttu-id="68346-114">嚴重錯誤1030</span><span class="sxs-lookup"><span data-stu-id="68346-114">Fatal Error 1030</span></span>](#fatal-error-1030)

## <a name="fatal-error-1021"></a><span data-ttu-id="68346-115">嚴重錯誤1021</span><span class="sxs-lookup"><span data-stu-id="68346-115">Fatal Error 1021</span></span>

<dl> <dt>

<span data-ttu-id="68346-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021，嚴重>： " <fileName><行 \#>： <identifier> TRAP 類型之 VARIABLES 子句中的識別碼無法解析為純量物件類型"**</span><span class="sxs-lookup"><span data-stu-id="68346-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021, Fatal>: "<fileName><line\#>: Identifier <identifier> in the VARIABLES clause of TRAP-TYPE does not resolve to a scalar OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="68346-117">**陷阱類型** 宏調用，SNMPv1 特定模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="68346-117">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="68346-118">在 **TRAP 類型** 宏調用的 variables 子句中使用的變數清單中的每個專案，都必須解析成純量物件類型實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="68346-118">Each item in the list of variables used in the VARIABLES clause of a **TRAP-TYPE** macro invocation must resolve to the name of a scalar OBJECT-TYPE instance.</span></span>

</dd> </dl>

## <a name="fatal-error-1022"></a><span data-ttu-id="68346-119">嚴重錯誤1022</span><span class="sxs-lookup"><span data-stu-id="68346-119">Fatal Error 1022</span></span>

<dl> <dt>

<span data-ttu-id="68346-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022、嚴重>：「 <fileName><行 \#>：值未解析為類型」 <type>**</span><span class="sxs-lookup"><span data-stu-id="68346-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022, Fatal>: "<fileName><line\#>: Value does not resolve to type <type>"**</span></span>
</dt> <dd>

<span data-ttu-id="68346-121">值指派模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。</span><span class="sxs-lookup"><span data-stu-id="68346-121">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="68346-122">整數的 RHS 值、 **Null**、八進位字串或物件識別碼值指派的類型錯誤。</span><span class="sxs-lookup"><span data-stu-id="68346-122">The value on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment is of the wrong type.</span></span>

</dd> </dl>

## <a name="fatal-error-1023"></a><span data-ttu-id="68346-123">嚴重錯誤1023</span><span class="sxs-lookup"><span data-stu-id="68346-123">Fatal Error 1023</span></span>

<dl> <dt>

<span data-ttu-id="68346-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023、嚴重>：「 <fileName><行 \#>：識別碼 <identifier> 無法解析為類型」 <identifier>**</span><span class="sxs-lookup"><span data-stu-id="68346-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to the type <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="68346-125">值指派模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。</span><span class="sxs-lookup"><span data-stu-id="68346-125">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="68346-126">RHS 整數、 **Null**、八進位字串或物件識別碼值指派的符號 (值參考) 不會解析為正確的類型。</span><span class="sxs-lookup"><span data-stu-id="68346-126">A symbol (value reference) on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment does not resolve to the right type.</span></span>

</dd> </dl>

## <a name="fatal-error-1024"></a><span data-ttu-id="68346-127">嚴重錯誤1024</span><span class="sxs-lookup"><span data-stu-id="68346-127">Fatal Error 1024</span></span>

<dl> <dt>

<span data-ttu-id="68346-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024、嚴重>：「 <fileName><行 \#>： OID 值定義中的負整數」**</span><span class="sxs-lookup"><span data-stu-id="68346-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024, Fatal>: "<fileName><line\#>: Negative integer in OID value definition"**</span></span>
</dt> <dd>

<span data-ttu-id="68346-129">值指派模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。</span><span class="sxs-lookup"><span data-stu-id="68346-129">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="68346-130">OID 元件清單中的所有值都必須為非負數 (最好是正數) 整數。</span><span class="sxs-lookup"><span data-stu-id="68346-130">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1025"></a><span data-ttu-id="68346-131">嚴重錯誤1025</span><span class="sxs-lookup"><span data-stu-id="68346-131">Fatal Error 1025</span></span>

<dl> <dt>

<span data-ttu-id="68346-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025，嚴重>：「 <identifier> OID 值中的識別碼無法解析為正整數」**</span><span class="sxs-lookup"><span data-stu-id="68346-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025, Fatal>: "Identifier <identifier> in OID value does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="68346-133">值指派模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。</span><span class="sxs-lookup"><span data-stu-id="68346-133">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="68346-134">OID 元件清單中的所有值都必須為非負數 (最好是正數) 整數。</span><span class="sxs-lookup"><span data-stu-id="68346-134">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1026"></a><span data-ttu-id="68346-135">嚴重錯誤1026</span><span class="sxs-lookup"><span data-stu-id="68346-135">Fatal Error 1026</span></span>

<dl> <dt>

<span data-ttu-id="68346-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026、嚴重>：「 <fileName><行 \#>： <identifier> oid 值中的識別碼都不會解析為 oid 值也不會解析為正整數」**</span><span class="sxs-lookup"><span data-stu-id="68346-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026, Fatal>: "<fileName><line\#>: Identifier <identifier> in OID value neither resolves to an OID value nor a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="68346-137">值指派模組語意錯誤，不是 SNMPv1 或 SNMPv2C 所特有。</span><span class="sxs-lookup"><span data-stu-id="68346-137">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="68346-138">OID 值中使用的第一個元件必須解析為 OID 值或整數。</span><span class="sxs-lookup"><span data-stu-id="68346-138">The first component used in an OID value must resolve to an OID value or an INTEGER.</span></span>

</dd> </dl>

## <a name="warning-1027"></a><span data-ttu-id="68346-139">警告1027</span><span class="sxs-lookup"><span data-stu-id="68346-139">Warning 1027</span></span>

<dl> <dt>

<span data-ttu-id="68346-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027，警告>：「 <fileName><行 \#>：未使用匯入的符號」 <identifier>**</span><span class="sxs-lookup"><span data-stu-id="68346-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, Warning>: "<fileName><line\#>: Imported symbol <identifier> unused"**</span></span>
</dt> <dd>

<span data-ttu-id="68346-141">匯入區段模組語義警告，特定于 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="68346-141">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="68346-142">針對每個未使用的匯入符號發出警告。</span><span class="sxs-lookup"><span data-stu-id="68346-142">A warning is issued for every unused imported symbol.</span></span>

</dd> </dl>

## <a name="fatal-error-1028"></a><span data-ttu-id="68346-143">嚴重錯誤1028</span><span class="sxs-lookup"><span data-stu-id="68346-143">Fatal Error 1028</span></span>

<dl> <dt>

<span data-ttu-id="68346-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028、嚴重>：「模組 <identifier> 未匯入匯入區段」**</span><span class="sxs-lookup"><span data-stu-id="68346-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028, Fatal>: "Module <identifier> not imported in the IMPORTS section"**</span></span>
</dt> <dd>

<span data-ttu-id="68346-145">IMPORTS 區段模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="68346-145">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="68346-146">用於參考符號的模組名稱，必須出現在 IMPORTS 子句中，或為目前模組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68346-146">A module name used in referencing a symbol must either be present in the IMPORTS clause, or be the name of the current module.</span></span>

</dd> </dl>

## <a name="fatal-error-1029"></a><span data-ttu-id="68346-147">嚴重錯誤1029</span><span class="sxs-lookup"><span data-stu-id="68346-147">Fatal Error 1029</span></span>

<dl> <dt>

<span data-ttu-id="68346-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029、嚴重>：「 <fileName><行 \#>：無法匯入目前的模組」 <identifier>**</span><span class="sxs-lookup"><span data-stu-id="68346-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029, Fatal>: "<fileName><line\#>: Current module <identifier> cannot be imported"**</span></span>
</dt> <dd>

<span data-ttu-id="68346-149">IMPORTS 區段模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="68346-149">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="68346-150">目前模組的名稱也是匯入清單中的數位。</span><span class="sxs-lookup"><span data-stu-id="68346-150">The name of the current module also figures in the IMPORTS list.</span></span>

</dd> </dl>

## <a name="fatal-error-1030"></a><span data-ttu-id="68346-151">嚴重錯誤1030</span><span class="sxs-lookup"><span data-stu-id="68346-151">Fatal Error 1030</span></span>

<dl> <dt>

<span data-ttu-id="68346-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030、嚴重>：「 <fileName><行 \#>： <identifier> 未從模組匯入 <identifier> 符號」**</span><span class="sxs-lookup"><span data-stu-id="68346-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030, Fatal>:"<fileName><line\#>: Symbol <identifier> not imported from Module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="68346-153">IMPORTS 區段模組語意錯誤，特定于 SNMPv1 或 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="68346-153">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="68346-154">您已使用 "Module. Symbol" 標記法，但尚未從 [匯入] 區段中的指定模組匯入符號。</span><span class="sxs-lookup"><span data-stu-id="68346-154">You have used the "Module.Symbol" notation, but the symbol has not been imported from the specified module in the IMPORTS section.</span></span>

</dd> </dl>

 

 



