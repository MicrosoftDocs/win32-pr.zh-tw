---
description: 描述 WMI SNMP 提供者錯誤211到220。
ms.assetid: beaa644d-51b3-4a57-8853-0b37f69f615a
ms.tgt_platform: multiple
title: 錯誤211到220
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25dbf8cb8f27d4c58a1505176eca218b8d947d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694931"
---
# <a name="errors-211-through-220"></a><span data-ttu-id="faf99-103">錯誤211到220</span><span class="sxs-lookup"><span data-stu-id="faf99-103">Errors 211 through 220</span></span>

<span data-ttu-id="faf99-104">描述 WMI SNMP 提供者錯誤211到220。</span><span class="sxs-lookup"><span data-stu-id="faf99-104">Describes WMI SNMP provider errors 211 through 220.</span></span>

[<span data-ttu-id="faf99-105">資訊訊息211</span><span class="sxs-lookup"><span data-stu-id="faf99-105">Information Message 211</span></span>](#information-message-211)

[<span data-ttu-id="faf99-106">嚴重錯誤212</span><span class="sxs-lookup"><span data-stu-id="faf99-106">Fatal Error 212</span></span>](#fatal-error-212)

[<span data-ttu-id="faf99-107">嚴重錯誤213</span><span class="sxs-lookup"><span data-stu-id="faf99-107">Fatal Error 213</span></span>](#fatal-error-213)

[<span data-ttu-id="faf99-108">嚴重錯誤214</span><span class="sxs-lookup"><span data-stu-id="faf99-108">Fatal Error 214</span></span>](#fatal-error-214)

[<span data-ttu-id="faf99-109">嚴重錯誤215</span><span class="sxs-lookup"><span data-stu-id="faf99-109">Fatal Error 215</span></span>](#fatal-error-215)

[<span data-ttu-id="faf99-110">嚴重錯誤216</span><span class="sxs-lookup"><span data-stu-id="faf99-110">Fatal Error 216</span></span>](#fatal-error-216)

[<span data-ttu-id="faf99-111">嚴重錯誤217</span><span class="sxs-lookup"><span data-stu-id="faf99-111">Fatal Error 217</span></span>](#fatal-error-217)

[<span data-ttu-id="faf99-112">嚴重錯誤218</span><span class="sxs-lookup"><span data-stu-id="faf99-112">Fatal Error 218</span></span>](#fatal-error-218)

[<span data-ttu-id="faf99-113">嚴重錯誤219</span><span class="sxs-lookup"><span data-stu-id="faf99-113">Fatal Error 219</span></span>](#fatal-error-219)

[<span data-ttu-id="faf99-114">嚴重錯誤220</span><span class="sxs-lookup"><span data-stu-id="faf99-114">Fatal Error 220</span></span>](#fatal-error-220)

## <a name="information-message-211"></a><span data-ttu-id="faf99-115">資訊訊息211</span><span class="sxs-lookup"><span data-stu-id="faf99-115">Information Message 211</span></span>

<dl> <dt>

<span data-ttu-id="faf99-116"><span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211，資訊>：「略過 <identifier> 陷阱類型」**</span><span class="sxs-lookup"><span data-stu-id="faf99-116"><span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211, Information>: "Skipping TRAP-TYPE <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="faf99-117">陷阱型別定義中的任何錯誤都會產生此訊息。</span><span class="sxs-lookup"><span data-stu-id="faf99-117">Any errors in the TRAP-TYPE definition generate this message.</span></span>

</dd> </dl>

## <a name="fatal-error-212"></a><span data-ttu-id="faf99-118">嚴重錯誤212</span><span class="sxs-lookup"><span data-stu-id="faf99-118">Fatal Error 212</span></span>

<dl> <dt>

<span data-ttu-id="faf99-119"><span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212，嚴重>： " <fileName> ： <行 \#>：順序定義中發生語法錯誤。上次讀取的權杖是 <token> "**</span><span class="sxs-lookup"><span data-stu-id="faf99-119"><span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212, Fatal>: "<fileName>:<line\#>: Syntax Error in SEQUENCE definition. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="faf99-120">類型指派中的模組語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="faf99-120">Module syntax error in type assignment.</span></span> <span data-ttu-id="faf99-121">順序結構的左右大括弧之間有錯誤，這是在 MIB 類型指派中的語法錯誤數量。</span><span class="sxs-lookup"><span data-stu-id="faf99-121">There is an error between the left and right braces of a SEQUENCE construct, which amounts to a syntax error in a MIB type assignment.</span></span>

</dd> </dl>

## <a name="fatal-error-213"></a><span data-ttu-id="faf99-122">嚴重錯誤213</span><span class="sxs-lookup"><span data-stu-id="faf99-122">Fatal Error 213</span></span>

<dl> <dt>

<span data-ttu-id="faf99-123"><span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213，嚴重>： " <fileName> ： <行 \#>：物件識別碼值中有語法錯誤。上次讀取的權杖是 <token> "**</span><span class="sxs-lookup"><span data-stu-id="faf99-123"><span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213, Fatal>: "<fileName>:<line\#>: Syntax Error in Object Identifier value. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="faf99-124">值指派中的模組語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="faf99-124">Module syntax error in value assignment.</span></span> <span data-ttu-id="faf99-125">物件識別碼值的左括弧和右大括弧之間有錯誤。</span><span class="sxs-lookup"><span data-stu-id="faf99-125">There is an error between the left and right braces of an object identifier value.</span></span>

</dd> </dl>

## <a name="fatal-error-214"></a><span data-ttu-id="faf99-126">嚴重錯誤214</span><span class="sxs-lookup"><span data-stu-id="faf99-126">Fatal Error 214</span></span>

<dl> <dt>

<span data-ttu-id="faf99-127"><span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214、嚴重>： " <fileName> ： <行 \#>： IMPORTS 符號清單中的語法錯誤。上次讀取的權杖是 <token> "**</span><span class="sxs-lookup"><span data-stu-id="faf99-127"><span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214, Fatal>: "<fileName>:<line\#>: Syntax Error in the list of symbols in IMPORTS. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="faf99-128">IMPORTS 區段中的模組語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="faf99-128">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-215"></a><span data-ttu-id="faf99-129">嚴重錯誤215</span><span class="sxs-lookup"><span data-stu-id="faf99-129">Fatal Error 215</span></span>

<dl> <dt>

<span data-ttu-id="faf99-130"><span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215，嚴重>： " <fileName> ： <行 \#>：匯入 (缺少模組名稱？ ) 中的語法錯誤。上次讀取的權杖是 <token> "**</span><span class="sxs-lookup"><span data-stu-id="faf99-130"><span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215, Fatal>: "<fileName>:<line\#>: Syntax Error in IMPORTS (missing module name?). Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="faf99-131">IMPORTS 區段中的模組語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="faf99-131">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-216"></a><span data-ttu-id="faf99-132">嚴重錯誤216</span><span class="sxs-lookup"><span data-stu-id="faf99-132">Fatal Error 216</span></span>

<dl> <dt>

<span data-ttu-id="faf99-133"><span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216，嚴重>： " <fileName> ： <行 \#>： IMPORTS 區段中發生語法錯誤。上次讀取的權杖是 <token> "**</span><span class="sxs-lookup"><span data-stu-id="faf99-133"><span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216, Fatal>: "<fileName>:<line\#>: Syntax Error in the IMPORTS section. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="faf99-134">IMPORTS 區段中的模組語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="faf99-134">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-217"></a><span data-ttu-id="faf99-135">嚴重錯誤217</span><span class="sxs-lookup"><span data-stu-id="faf99-135">Fatal Error 217</span></span>

<dl> <dt>

<span data-ttu-id="faf99-136"><span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217、嚴重>： " <fileName> ： <行 \#>：整數列舉中有語法錯誤。上次讀取的權杖是 <token> "**</span><span class="sxs-lookup"><span data-stu-id="faf99-136"><span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217, Fatal>: "<fileName>:<line\#>: Syntax error in INTEGER Enumeration. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="faf99-137">MIB 列舉定義的左右大括弧之間的任何模組語法錯誤都會產生此訊息。</span><span class="sxs-lookup"><span data-stu-id="faf99-137">Any module syntax error between the left and right braces of a MIB enumeration definition generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-218"></a><span data-ttu-id="faf99-138">嚴重錯誤218</span><span class="sxs-lookup"><span data-stu-id="faf99-138">Fatal Error 218</span></span>

<dl> <dt>

<span data-ttu-id="faf99-139"><span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218，嚴重>： " <fileName> ： <行 \#>：子類型規格中有語法錯誤。上次讀取的權杖是 <token> "**</span><span class="sxs-lookup"><span data-stu-id="faf99-139"><span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218, Fatal>: "<fileName>:<line\#>: Syntax Error in sub-type specification. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="faf99-140">子類型規格中的括弧之間的任何模組語法錯誤都會產生此訊息。</span><span class="sxs-lookup"><span data-stu-id="faf99-140">Any module syntax error between the parentheses in a sub-type specification generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-219"></a><span data-ttu-id="faf99-141">嚴重錯誤219</span><span class="sxs-lookup"><span data-stu-id="faf99-141">Fatal Error 219</span></span>

<dl> <dt>

<span data-ttu-id="faf99-142"><span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219，嚴重>： " <fileName> ： <行 \#>：大小規格中有語法錯誤。上次讀取的權杖是 <token> "**</span><span class="sxs-lookup"><span data-stu-id="faf99-142"><span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219, Fatal>:"<fileName>:<line\#>: Syntax Error in the SIZE specification. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="faf99-143">左右括弧之間的 SIZE 子句中的任何模組語法錯誤都會產生此訊息。</span><span class="sxs-lookup"><span data-stu-id="faf99-143">Any module syntax error in the SIZE clause between the left and right parentheses generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-220"></a><span data-ttu-id="faf99-144">嚴重錯誤220</span><span class="sxs-lookup"><span data-stu-id="faf99-144">Fatal Error 220</span></span>

<dl> <dt>

<span data-ttu-id="faf99-145"><span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220、嚴重>： " <fileName> ： <行 \#>：不允許 SNMPV2SMI 的物件類型調用"**</span><span class="sxs-lookup"><span data-stu-id="faf99-145"><span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220, Fatal>:"<fileName>:<line\#>: OBJECT-TYPE invocation of SNMPv2SMI not allowed"**</span></span>
</dt> <dd>

<span data-ttu-id="faf99-146">模組語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="faf99-146">Module syntax error.</span></span> <span data-ttu-id="faf99-147">您已在 MIB 中使用 SNMPv2C 特定的 **物件類型** 調用，但指定了 **/v1** 參數，這需要嚴格符合 SNMPv1 語法。</span><span class="sxs-lookup"><span data-stu-id="faf99-147">You have used the SNMPv2C-specific **OBJECT-TYPE** invocation in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

 

 



