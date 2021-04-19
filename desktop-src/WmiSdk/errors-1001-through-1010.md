---
description: 描述 WMI SNMP 提供者錯誤1001到1010。
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: 錯誤1001到1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa10b83c660d617bdbf37b6f119e824bbba60616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983680"
---
# <a name="errors-1001-through-1010"></a><span data-ttu-id="e3c5d-103">錯誤1001到1010</span><span class="sxs-lookup"><span data-stu-id="e3c5d-103">Errors 1001 through 1010</span></span>

<span data-ttu-id="e3c5d-104">描述 WMI SNMP 提供者錯誤1001到1010。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-104">Describes WMI SNMP provider errors 1001 through 1010.</span></span>

[<span data-ttu-id="e3c5d-105">嚴重錯誤1001</span><span class="sxs-lookup"><span data-stu-id="e3c5d-105">Fatal Error 1001</span></span>](#fatal-error-1001)

[<span data-ttu-id="e3c5d-106">嚴重錯誤1002</span><span class="sxs-lookup"><span data-stu-id="e3c5d-106">Fatal Error 1002</span></span>](#fatal-error-1002)

[<span data-ttu-id="e3c5d-107">嚴重錯誤1003</span><span class="sxs-lookup"><span data-stu-id="e3c5d-107">Fatal Error 1003</span></span>](#fatal-error-1003)

[<span data-ttu-id="e3c5d-108">警告1004</span><span class="sxs-lookup"><span data-stu-id="e3c5d-108">Warning 1004</span></span>](#warning-1004)

[<span data-ttu-id="e3c5d-109">警告1005</span><span class="sxs-lookup"><span data-stu-id="e3c5d-109">Warning 1005</span></span>](#warning-1005)

[<span data-ttu-id="e3c5d-110">嚴重錯誤1006</span><span class="sxs-lookup"><span data-stu-id="e3c5d-110">Fatal Error 1006</span></span>](#fatal-error-1006)

[<span data-ttu-id="e3c5d-111">嚴重錯誤1008</span><span class="sxs-lookup"><span data-stu-id="e3c5d-111">Fatal Error 1008</span></span>](#fatal-error-1008)

## <a name="fatal-error-1001"></a><span data-ttu-id="e3c5d-112">嚴重錯誤1001</span><span class="sxs-lookup"><span data-stu-id="e3c5d-112">Fatal Error 1001</span></span>

<dl> <dt>

<span data-ttu-id="e3c5d-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001，嚴重>： " <fileName> ： <行 \#>：物件類型的語法子句無法解析為允許的類型"</span><span class="sxs-lookup"><span data-stu-id="e3c5d-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, Fatal>: "<fileName>:<line\#>: SYNTAX clause of OBJECT-TYPE does not resolve to allowed types"</span></span>
</dt> <dd>

<span data-ttu-id="e3c5d-114">物件類型宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-114">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="e3c5d-115">物件類型宏的語法子句必須解析為類型或子類型，使用 SNMPv1 或 SNMPv2C SMI-S 允許的大小或範圍規格來形成。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-115">The SYNTAX clause of the OBJECT-TYPE macro must resolve to a type or subtype, formed by using the SIZE or range specification that the SNMPv1 or SNMPv2C SMI allows.</span></span> <span data-ttu-id="e3c5d-116">如果不是這種情況，則會報告嚴重錯誤1001。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-116">If this is not the case, fatal error 1001 is reported.</span></span>

<span data-ttu-id="e3c5d-117">編譯 SNMPv1 或 SNMPv2C MIB 時，會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-117">This error can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

<span data-ttu-id="e3c5d-118">SNMPv1 SMI-S 允許的類型為：</span><span class="sxs-lookup"><span data-stu-id="e3c5d-118">Types allowed by the SNMPv1 SMI are:</span></span>

-   <span data-ttu-id="e3c5d-119">INTEGER</span><span class="sxs-lookup"><span data-stu-id="e3c5d-119">INTEGER</span></span>
-   <span data-ttu-id="e3c5d-120">NULL</span><span class="sxs-lookup"><span data-stu-id="e3c5d-120">NULL</span></span>
-   <span data-ttu-id="e3c5d-121">八位字串</span><span class="sxs-lookup"><span data-stu-id="e3c5d-121">OCTET STRING</span></span>
-   <span data-ttu-id="e3c5d-122">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="e3c5d-122">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="e3c5d-123">Networkaddress.cache.ttl</span><span class="sxs-lookup"><span data-stu-id="e3c5d-123">NetworkAddress</span></span>
-   <span data-ttu-id="e3c5d-124">IpAddress</span><span class="sxs-lookup"><span data-stu-id="e3c5d-124">IpAddress</span></span>
-   <span data-ttu-id="e3c5d-125">計數器</span><span class="sxs-lookup"><span data-stu-id="e3c5d-125">Counter</span></span>
-   <span data-ttu-id="e3c5d-126">量測計</span><span class="sxs-lookup"><span data-stu-id="e3c5d-126">Gauge</span></span>
-   <span data-ttu-id="e3c5d-127">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="e3c5d-127">TimeTicks</span></span>
-   <span data-ttu-id="e3c5d-128">Opaque</span><span class="sxs-lookup"><span data-stu-id="e3c5d-128">Opaque</span></span>
-   <span data-ttu-id="e3c5d-129">DisplayString</span><span class="sxs-lookup"><span data-stu-id="e3c5d-129">DisplayString</span></span>
-   <span data-ttu-id="e3c5d-130">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="e3c5d-130">PhysAddress</span></span>

<span data-ttu-id="e3c5d-131">SNMPv2C SMI-S 允許的類型為：</span><span class="sxs-lookup"><span data-stu-id="e3c5d-131">Types allowed by the SNMPv2C SMI are:</span></span>

-   <span data-ttu-id="e3c5d-132">INTEGER</span><span class="sxs-lookup"><span data-stu-id="e3c5d-132">INTEGER</span></span>
-   <span data-ttu-id="e3c5d-133">八位字串</span><span class="sxs-lookup"><span data-stu-id="e3c5d-133">OCTET STRING</span></span>
-   <span data-ttu-id="e3c5d-134">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="e3c5d-134">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="e3c5d-135">BITS</span><span class="sxs-lookup"><span data-stu-id="e3c5d-135">BITS</span></span>
-   <span data-ttu-id="e3c5d-136">Integer32</span><span class="sxs-lookup"><span data-stu-id="e3c5d-136">Integer32</span></span>
-   <span data-ttu-id="e3c5d-137">IpAddress</span><span class="sxs-lookup"><span data-stu-id="e3c5d-137">IpAddress</span></span>
-   <span data-ttu-id="e3c5d-138">Counter32</span><span class="sxs-lookup"><span data-stu-id="e3c5d-138">Counter32</span></span>
-   <span data-ttu-id="e3c5d-139">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="e3c5d-139">TimeTicks</span></span>
-   <span data-ttu-id="e3c5d-140">Opaque</span><span class="sxs-lookup"><span data-stu-id="e3c5d-140">Opaque</span></span>
-   <span data-ttu-id="e3c5d-141">Counter64</span><span class="sxs-lookup"><span data-stu-id="e3c5d-141">Counter64</span></span>
-   <span data-ttu-id="e3c5d-142">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="e3c5d-142">Unsigned32</span></span>
-   <span data-ttu-id="e3c5d-143">DisplayString</span><span class="sxs-lookup"><span data-stu-id="e3c5d-143">DisplayString</span></span>
-   <span data-ttu-id="e3c5d-144">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="e3c5d-144">PhysAddress</span></span>
-   <span data-ttu-id="e3c5d-145">MacAddress</span><span class="sxs-lookup"><span data-stu-id="e3c5d-145">MacAddress</span></span>
-   <span data-ttu-id="e3c5d-146">TruthValue</span><span class="sxs-lookup"><span data-stu-id="e3c5d-146">TruthValue</span></span>
-   <span data-ttu-id="e3c5d-147">TestAndIncr</span><span class="sxs-lookup"><span data-stu-id="e3c5d-147">TestAndIncr</span></span>
-   <span data-ttu-id="e3c5d-148">AutonomousType</span><span class="sxs-lookup"><span data-stu-id="e3c5d-148">AutonomousType</span></span>
-   <span data-ttu-id="e3c5d-149">InstancePointer</span><span class="sxs-lookup"><span data-stu-id="e3c5d-149">InstancePointer</span></span>
-   <span data-ttu-id="e3c5d-150">VariablePointer</span><span class="sxs-lookup"><span data-stu-id="e3c5d-150">VariablePointer</span></span>
-   <span data-ttu-id="e3c5d-151">RowPointer</span><span class="sxs-lookup"><span data-stu-id="e3c5d-151">RowPointer</span></span>
-   <span data-ttu-id="e3c5d-152">RowStatus</span><span class="sxs-lookup"><span data-stu-id="e3c5d-152">RowStatus</span></span>
-   <span data-ttu-id="e3c5d-153">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="e3c5d-153">TimeStamp</span></span>
-   <span data-ttu-id="e3c5d-154">TimeInterval</span><span class="sxs-lookup"><span data-stu-id="e3c5d-154">TimeInterval</span></span>
-   <span data-ttu-id="e3c5d-155">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="e3c5d-155">DateAndTime</span></span>
-   <span data-ttu-id="e3c5d-156">StorageType</span><span class="sxs-lookup"><span data-stu-id="e3c5d-156">StorageType</span></span>
-   <span data-ttu-id="e3c5d-157">Tdomain</span><span class="sxs-lookup"><span data-stu-id="e3c5d-157">Tdomain</span></span>
-   <span data-ttu-id="e3c5d-158">Taddress</span><span class="sxs-lookup"><span data-stu-id="e3c5d-158">Taddress</span></span>

</dd> </dl>

## <a name="fatal-error-1002"></a><span data-ttu-id="e3c5d-159">嚴重錯誤1002</span><span class="sxs-lookup"><span data-stu-id="e3c5d-159">Fatal Error 1002</span></span>

<dl> <dt>

<span data-ttu-id="e3c5d-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002，嚴重>： " <fileName> ： <行 \#>：不正確存取子句 <clause> "</span><span class="sxs-lookup"><span data-stu-id="e3c5d-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, Fatal>: "<fileName>:<line\#>: Invalid ACCESS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="e3c5d-161">物件類型宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-161">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="e3c5d-162">若為 SNMPv1，則物件類型宏的存取子句必須是「唯讀」、「僅限寫入」、「讀取/寫入」或「不可存取」。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-162">For SNMPv1, the ACCESS clause of the OBJECT-TYPE macro must be "read-only," "write-only," "read/write," or "not-accessible."</span></span>

<span data-ttu-id="e3c5d-163">針對 SNMPv2C，MAX 存取子句必須是「唯讀」、「讀取-建立」、「讀取/寫入」或「無法存取」。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-163">For SNMPv2C, the MAX-ACCESS clause must be "read-only," "read-create," "read/write," or "not-accessible."</span></span>

</dd> </dl>

## <a name="fatal-error-1003"></a><span data-ttu-id="e3c5d-164">嚴重錯誤1003</span><span class="sxs-lookup"><span data-stu-id="e3c5d-164">Fatal Error 1003</span></span>

<dl> <dt>

<span data-ttu-id="e3c5d-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003、嚴重>： " <fileName> ： <行 \#>：不正確 STATUS 子句 <clause> "</span><span class="sxs-lookup"><span data-stu-id="e3c5d-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, Fatal>: "<fileName>:<line\#>: Invalid STATUS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="e3c5d-166">物件類型宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-166">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="e3c5d-167">若為 SNMPv1，則物件類型宏調用的 STATUS 子句必須是「強制性」、「選擇性」、「已淘汰」或「已淘汰」。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-167">For SNMPv1, the STATUS clause of an OBJECT-TYPE macro invocation must be "mandatory," "optional," "obsolete," or "deprecated."</span></span>

<span data-ttu-id="e3c5d-168">若為 SNMPv2C，則物件類型宏調用的 STATUS 子句必須是「目前」、「已淘汰」或「過時」。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-168">For SNMPv2C, the STATUS clause of an OBJECT-TYPE macro invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="warning-1004"></a><span data-ttu-id="e3c5d-169">警告1004</span><span class="sxs-lookup"><span data-stu-id="e3c5d-169">Warning 1004</span></span>

<dl> <dt>

<span data-ttu-id="e3c5d-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004，警告>： " <fileName> ： <行 \#>：物件類型 <identifier> ，其語法解析為其中一個計數器類型時，不是以字母 '" 結尾</span><span class="sxs-lookup"><span data-stu-id="e3c5d-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, whose syntax resolves to one of the Counter types does not end with the letter 's' "</span></span>
</dt> <dd>

<span data-ttu-id="e3c5d-171">物件類型宏調用模組語義警告。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-171">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="e3c5d-172">語法計數器 (SNMPv1) 或 Counter32 和 Counter64 (SNMPv2C) 的物件識別碼必須是複數。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-172">The identifier for an object of SYNTAX Counter (SNMPv1) or Counter32 and Counter64 (SNMPv2C) must be plural.</span></span>

<span data-ttu-id="e3c5d-173">編譯 SNMPv1 或 SNMPv2C MIB 時可能會發生這個警告。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-173">This warning can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

</dd> </dl>

## <a name="warning-1005"></a><span data-ttu-id="e3c5d-174">警告1005</span><span class="sxs-lookup"><span data-stu-id="e3c5d-174">Warning 1005</span></span>

<dl> <dt>

<span data-ttu-id="e3c5d-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005，警告>： " <fileName> ： <行 \#>：具有" SEQUENCE OF "順序的物件類型，則應該有存取子句「無法存取」</span><span class="sxs-lookup"><span data-stu-id="e3c5d-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, Warning>: "<fileName>:<line\#>: OBJECT-TYPE with SYNTAX "SEQUENCE OF", should have an ACCESS clause "not-accessible"</span></span>
</dt> <dd>

<span data-ttu-id="e3c5d-176">物件類型宏調用模組語義警告。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-176">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="e3c5d-177">資料表或概念資料列 (序列的或序列物件類型，分別) 必須是「不可存取」。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-177">A table or conceptual row (SEQUENCE OF or SEQUENCE object types, respectively) must be "not-accessible."</span></span>

<span data-ttu-id="e3c5d-178">此警告可能會在 SNMPv1 或 SNMPv2C 中發生。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-178">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1006"></a><span data-ttu-id="e3c5d-179">嚴重錯誤1006</span><span class="sxs-lookup"><span data-stu-id="e3c5d-179">Fatal Error 1006</span></span>

<dl> <dt>

<span data-ttu-id="e3c5d-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006，嚴重>： " <fileName> ： <行 \#> 物件類型 <identifier> （這是語法順序）沒有索引或增強子句"</span><span class="sxs-lookup"><span data-stu-id="e3c5d-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, Fatal>: "<fileName>:<line\#> OBJECT-TYPE <identifier>, which is of SYNTAX SEQUENCE, does not have an INDEX or AUGMENTS clause"</span></span>
</dt> <dd>

<span data-ttu-id="e3c5d-181">物件類型宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-181">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="e3c5d-182">針對 SNMPv1，其語法會解析為序列類型的物件類型定義必須有 INDEX 子句。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-182">For SNMPv1, the INDEX clause must be present for an OBJECT-TYPE definition whose SYNTAX resolves to a SEQUENCE type.</span></span>

<span data-ttu-id="e3c5d-183">針對 SNMPv2C，概念資料列宣告必須有索引或增強子句。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-183">For SNMPv2C, either the INDEX or the AUGMENTS clause must be present for a conceptual row declaration.</span></span>

</dd> </dl>

## <a name="fatal-error-1008"></a><span data-ttu-id="e3c5d-184">嚴重錯誤1008</span><span class="sxs-lookup"><span data-stu-id="e3c5d-184">Fatal Error 1008</span></span>

<dl> <dt>

<span data-ttu-id="e3c5d-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008，嚴重>： " <fileName> ： <行 \#>：物件類型 <identifier> ，也就是" SEQUENCE "的語法未被參考"</span><span class="sxs-lookup"><span data-stu-id="e3c5d-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, Fatal>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, which is of SYNTAX "SEQUENCE" has not been referenced"</span></span>
</dt> <dd>

<span data-ttu-id="e3c5d-186">物件類型宏調用模組語意錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-186">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="e3c5d-187">以語法子句作為序列類型的物件類型，必須在只是一個代表資料表宣告的物件類型調用的語法子句中，也就是使用語法子句作為類型序列的物件。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-187">An OBJECT-TYPE with the SYNTAX clause as a SEQUENCE type must figure in the SYNTAX clause of exactly one OBJECT-TYPE invocation that stands for a table declaration, that is, an object with the SYNTAX clause as a SEQUENCE OF type.</span></span> <span data-ttu-id="e3c5d-188"><行 \#> 參數參考第二個點參考。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-188">The <line\#> parameter refers to the second point of reference.</span></span>

<span data-ttu-id="e3c5d-189">這項錯誤可能會發生在 SNMPv1 或 SNMPv2C 中。</span><span class="sxs-lookup"><span data-stu-id="e3c5d-189">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



