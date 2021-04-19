---
description: 描述 WMI SNMP 提供者錯誤1071到1080。
ms.assetid: c9161c96-6839-4b32-b1bd-b40af18ab314
ms.tgt_platform: multiple
title: 錯誤1071到1080
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277aa7dd69d674ebc16bc0a2b4d104c349e593a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975531"
---
# <a name="errors-1071-through-1080"></a><span data-ttu-id="5caed-103">錯誤1071到1080</span><span class="sxs-lookup"><span data-stu-id="5caed-103">Errors 1071 through 1080</span></span>

<span data-ttu-id="5caed-104">描述 WMI SNMP 提供者錯誤1071到1080。</span><span class="sxs-lookup"><span data-stu-id="5caed-104">Describes WMI SNMP provider errors 1071 through 1080.</span></span>

[<span data-ttu-id="5caed-105">警告1071</span><span class="sxs-lookup"><span data-stu-id="5caed-105">Warning 1071</span></span>](#warning-1071)

[<span data-ttu-id="5caed-106">警告1072</span><span class="sxs-lookup"><span data-stu-id="5caed-106">Warning 1072</span></span>](#warning-1072)

[<span data-ttu-id="5caed-107">嚴重錯誤1074</span><span class="sxs-lookup"><span data-stu-id="5caed-107">Fatal Error 1074</span></span>](#fatal-error-1074)

[<span data-ttu-id="5caed-108">嚴重錯誤1075</span><span class="sxs-lookup"><span data-stu-id="5caed-108">Fatal Error 1075</span></span>](#fatal-error-1075)

[<span data-ttu-id="5caed-109">嚴重錯誤1077</span><span class="sxs-lookup"><span data-stu-id="5caed-109">Fatal Error 1077</span></span>](#fatal-error-1077)

[<span data-ttu-id="5caed-110">嚴重錯誤1079</span><span class="sxs-lookup"><span data-stu-id="5caed-110">Fatal Error 1079</span></span>](#fatal-error-1079)

[<span data-ttu-id="5caed-111">警告1080</span><span class="sxs-lookup"><span data-stu-id="5caed-111">Warning 1080</span></span>](#warning-1080)

## <a name="warning-1071"></a><span data-ttu-id="5caed-112">警告1071</span><span class="sxs-lookup"><span data-stu-id="5caed-112">Warning 1071</span></span>

<dl> <dt>

<span data-ttu-id="5caed-113"><span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071，警告>：「 <fileName><行 \#>：符號 <identifier> 未出現在匯入的模組中」 <identifier>**</span><span class="sxs-lookup"><span data-stu-id="5caed-113"><span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, Warning>: "<fileName><line\#>: Symbol <identifier> not present in imported module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="5caed-114">關於交互參照的模組語義警告，不是 SNMPv1 或 SNMPv2C 的特定相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5caed-114">Module semantic warning about cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="5caed-115">從模組匯入的符號不會解析為該模組中的任何事物。</span><span class="sxs-lookup"><span data-stu-id="5caed-115">A symbol imported from a module does not resolve to anything in that module.</span></span> <span data-ttu-id="5caed-116">雖然在輸入中指定該模組，但會出現此警告。</span><span class="sxs-lookup"><span data-stu-id="5caed-116">Even though that module is specified in the input, this warning appears.</span></span>

</dd> </dl>

## <a name="warning-1072"></a><span data-ttu-id="5caed-117">警告1072</span><span class="sxs-lookup"><span data-stu-id="5caed-117">Warning 1072</span></span>

<dl> <dt>

<span data-ttu-id="5caed-118"><span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072，警告>： " <fileName> ： <行 \#> 物件類型 <name> 是模組物件類型 <name> 的子 <name> 系**</span><span class="sxs-lookup"><span data-stu-id="5caed-118"><span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, Warning>: "<fileName>:<line\#> OBJECT-TYPE <name> is a descendant of OBJECT-TYPE <name> of module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="5caed-119">**物件類型** 宏調用模組語義警告。</span><span class="sxs-lookup"><span data-stu-id="5caed-119">**OBJECT-TYPE** macro invocation module semantic warning.</span></span> <span data-ttu-id="5caed-120">純量物件不能有任何子系物件。</span><span class="sxs-lookup"><span data-stu-id="5caed-120">A scalar object cannot have any descendant objects.</span></span>

<span data-ttu-id="5caed-121">此警告可能會在 SNMPv1 或 SNMPv2C 中發生。</span><span class="sxs-lookup"><span data-stu-id="5caed-121">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1074"></a><span data-ttu-id="5caed-122">嚴重錯誤1074</span><span class="sxs-lookup"><span data-stu-id="5caed-122">Fatal Error 1074</span></span>

<dl> <dt>

<span data-ttu-id="5caed-123"><span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074，嚴重>： " <fileName> ： <行 \#> 順序 (概念資料列) 物件類型沒有 <name> 一連串的 (概念資料表) 物件類型做為其父系」**</span><span class="sxs-lookup"><span data-stu-id="5caed-123"><span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074, Fatal>: "<fileName>:<line\#> SEQUENCE (Conceptual row) OBJECT-TYPE <name> does not have a SEQUENCE OF (Conceptual table) OBJECT-TYPE as its parent"**</span></span>
</dt> <dd>

<span data-ttu-id="5caed-124">**物件類型** 宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="5caed-124">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="5caed-125">每個資料列物件都必須具有 table 物件作為其父系。</span><span class="sxs-lookup"><span data-stu-id="5caed-125">Every row object must have a table object as its parent.</span></span>

<span data-ttu-id="5caed-126">這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。</span><span class="sxs-lookup"><span data-stu-id="5caed-126">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1075"></a><span data-ttu-id="5caed-127">嚴重錯誤1075</span><span class="sxs-lookup"><span data-stu-id="5caed-127">Fatal Error 1075</span></span>

<dl> <dt>

<span data-ttu-id="5caed-128"><span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075，嚴重>： " <fileName> ： <行 \#>：物件類型 <name> 不能是 MODULE 的資料表物件類型子系， <name> <name> 除非它是在後者的序列中。**</span><span class="sxs-lookup"><span data-stu-id="5caed-128"><span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075, Fatal>:"<fileName>:<line\#>: OBJECT-TYPE <name> cannot be a child of table OBJECT-TYPE <name> of module <name> unless it is in the SEQUENCE of the latter"**</span></span>
</dt> <dd>

<span data-ttu-id="5caed-129">**物件類型** 宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="5caed-129">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="5caed-130">每個順序物件都必須與序列類型定義中所述的物件完全相同，以做為其子系。</span><span class="sxs-lookup"><span data-stu-id="5caed-130">Every SEQUENCE object must have exactly the same objects that are mentioned in the SEQUENCE type definition as its children.</span></span> <span data-ttu-id="5caed-131">同樣地，每個物件順序都必須只有一個子系。</span><span class="sxs-lookup"><span data-stu-id="5caed-131">Similarly, every SEQUENCE OF object must have exactly one child.</span></span>

<span data-ttu-id="5caed-132">這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。</span><span class="sxs-lookup"><span data-stu-id="5caed-132">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1077"></a><span data-ttu-id="5caed-133">嚴重錯誤1077</span><span class="sxs-lookup"><span data-stu-id="5caed-133">Fatal Error 1077</span></span>

<dl> <dt>

<span data-ttu-id="5caed-134"><span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077、嚴重>： " <fileName> ： <行 \#>： TABLE 物件類型的語法 <name> 不是「模組」子物件類型的語法順序 <name> <name> 」**</span><span class="sxs-lookup"><span data-stu-id="5caed-134"><span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077, Fatal>: "<fileName>:<line\#>: The syntax of table OBJECT-TYPE <name> is not the SEQUENCE OF the syntax of the child OBJECT-TYPE <name> of module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="5caed-135">**物件類型** 宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="5caed-135">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="5caed-136">Table 物件的語法子句必須是資料列物件語法的「序列」。</span><span class="sxs-lookup"><span data-stu-id="5caed-136">The syntax clause of a table object must be the "SEQUENCE OF" of the syntax of the row object.</span></span>

<span data-ttu-id="5caed-137">這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。</span><span class="sxs-lookup"><span data-stu-id="5caed-137">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1079"></a><span data-ttu-id="5caed-138">嚴重錯誤1079</span><span class="sxs-lookup"><span data-stu-id="5caed-138">Fatal Error 1079</span></span>

<dl> <dt>

<span data-ttu-id="5caed-139"><span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079，嚴重>： "檔案名>： <行 \#>：物件類型 <name> 是模組物件類型的額外子系 <name> <name>**</span><span class="sxs-lookup"><span data-stu-id="5caed-139"><span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079, Fatal>:"fileName>:<line\#>: OBJECT-TYPE <name> is an extra child of OBJECT-TYPE <name> of module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="5caed-140">**物件類型** 宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="5caed-140">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="5caed-141">每個物件序列都必須只有一個子系。</span><span class="sxs-lookup"><span data-stu-id="5caed-141">Every SEQUENCE OF object must have exactly one child.</span></span>

<span data-ttu-id="5caed-142">這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。</span><span class="sxs-lookup"><span data-stu-id="5caed-142">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="warning-1080"></a><span data-ttu-id="5caed-143">警告1080</span><span class="sxs-lookup"><span data-stu-id="5caed-143">Warning 1080</span></span>

<dl> <dt>

<span data-ttu-id="5caed-144"><span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080，警告>：「 <fileName><行 \#>： MIB 模組 <moduleName> ，其中的符號 <symbolName> 已匯入，且不存在於輸入中」**</span><span class="sxs-lookup"><span data-stu-id="5caed-144"><span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, Warning>: "<fileName><line\#>: MIB Module <moduleName>, from which symbol <symbolName> is imported, is not present in input"**</span></span>
</dt> <dd>

<span data-ttu-id="5caed-145">關於交互參照的模組語義警告，不是 SNMPv1 或 SNMPv2C 的特定相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5caed-145">Module semantic warning about cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="5caed-146">如果主要模組或子公司模組的 [匯入] 區段中的其中一個模組不存在，但未參考此模組的符號，則會出現此警告。</span><span class="sxs-lookup"><span data-stu-id="5caed-146">If one of the modules in the IMPORTS section of the main module or a subsidiary module does not exist, but symbols from this module are not referenced, this warning appears.</span></span>

</dd> </dl>

 

 



