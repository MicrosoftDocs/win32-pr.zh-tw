---
description: 條件式存取控制專案 (ACE) 可讓您在執行存取檢查時評估存取條件。 安全描述項定義語言 (SDDL) 提供以字串格式定義條件式 Ace 的語法。
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: 條件式 Ace 的安全描述項定義語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cb6ae0588ae197c84d3b13362721cc3e98b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512004"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a><span data-ttu-id="12071-104">條件式 Ace 的安全描述項定義語言</span><span class="sxs-lookup"><span data-stu-id="12071-104">Security Descriptor Definition Language for Conditional ACEs</span></span>

<span data-ttu-id="12071-105">條件式 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ACE) 可讓您在執行存取檢查時評估存取條件。</span><span class="sxs-lookup"><span data-stu-id="12071-105">A conditional [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) allows an access condition to be evaluated when an access check is performed.</span></span> <span data-ttu-id="12071-106">安全描述項定義語言 (SDDL) 提供以字串格式定義條件式 Ace 的語法。</span><span class="sxs-lookup"><span data-stu-id="12071-106">The security descriptor definition language (SDDL) provides syntax for defining conditional ACEs in a string format.</span></span>

<span data-ttu-id="12071-107">條件式 ACE 的 SDDL 與任何 ACE 的 SDDL 相同，並將條件陳述式的語法附加到 ACE 字串的結尾。</span><span class="sxs-lookup"><span data-stu-id="12071-107">The SDDL for a conditional ACE is the same as for any ACE, with the syntax for the conditional statement appended to the end of the ACE string.</span></span> <span data-ttu-id="12071-108">如需 SDDL 的詳細資訊，請參閱 [安全描述項定義語言](security-descriptor-definition-language.md)。</span><span class="sxs-lookup"><span data-stu-id="12071-108">For information about SDDL, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

<span data-ttu-id="12071-109">\#在資源屬性中，"" 符號與 "0" 同義。</span><span class="sxs-lookup"><span data-stu-id="12071-109">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="12071-110">例如，D:AI (XA; OICI; FA;;;WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \#) ) 相當於並解釋為 D:AI (XA; OICI; FA;;;WD; (OctetStringType = = \# 01020300) ) 。</span><span class="sxs-lookup"><span data-stu-id="12071-110">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

-   [<span data-ttu-id="12071-111">條件式 ACE 字串格式</span><span class="sxs-lookup"><span data-stu-id="12071-111">Conditional ACE String Format</span></span>](#conditional-ace-string-format)
-   [<span data-ttu-id="12071-112">條件運算式</span><span class="sxs-lookup"><span data-stu-id="12071-112">Conditional Expressions</span></span>](#conditional-expressions)
-   [<span data-ttu-id="12071-113">屬性</span><span class="sxs-lookup"><span data-stu-id="12071-113">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="12071-114">運算子</span><span class="sxs-lookup"><span data-stu-id="12071-114">Operators</span></span>](#operators)
-   [<span data-ttu-id="12071-115">運算子優先順序</span><span class="sxs-lookup"><span data-stu-id="12071-115">Operator Precedence</span></span>](#operator-precedence)
-   [<span data-ttu-id="12071-116">未知的值</span><span class="sxs-lookup"><span data-stu-id="12071-116">Unknown Values</span></span>](#unknown-values)
-   [<span data-ttu-id="12071-117">條件式 ACE 評估</span><span class="sxs-lookup"><span data-stu-id="12071-117">Conditional ACE Evaluation</span></span>](#conditional-ace-evaluation)
-   [<span data-ttu-id="12071-118">範例</span><span class="sxs-lookup"><span data-stu-id="12071-118">Examples</span></span>](#examples)
-   [<span data-ttu-id="12071-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="12071-119">Related topics</span></span>](#related-topics)

## <a name="conditional-ace-string-format"></a><span data-ttu-id="12071-120">條件式 ACE 字串格式</span><span class="sxs-lookup"><span data-stu-id="12071-120">Conditional ACE String Format</span></span>

<span data-ttu-id="12071-121">[*安全描述項*](/windows/desktop/SecGloss/s-gly)字串中的每個 ACE 都會以括弧括住。</span><span class="sxs-lookup"><span data-stu-id="12071-121">Each ACE in a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string is enclosed in parentheses.</span></span> <span data-ttu-id="12071-122">ACE 的欄位會以下列順序排列，並以分號分隔 (; ) 。</span><span class="sxs-lookup"><span data-stu-id="12071-122">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

<span data-ttu-id="12071-123">\*AceType \***;**_AceFlags_*_;_*_許可權_*_;_*_ObjectGuid_*_;_*_InheritObjectGuid_*_;_*_AccountSid_*_; (_ *_ConditionalExpression_* _)_*</span><span class="sxs-lookup"><span data-stu-id="12071-123">*AceType\***;**_AceFlags_*_;_*_Rights_*_;_*_ObjectGuid_*_;_*_InheritObjectGuid_*_;_*_AccountSid_*_;(_*_ConditionalExpression_*_)_\*</span></span>

<span data-ttu-id="12071-124">這些欄位如 [ACE 字串](ace-strings.md)所述，但有下列例外狀況。</span><span class="sxs-lookup"><span data-stu-id="12071-124">The fields are as described in [ACE Strings](ace-strings.md), with the following exceptions.</span></span>

-   <span data-ttu-id="12071-125">*AceType* 欄位可以是下列其中一個字串。</span><span class="sxs-lookup"><span data-stu-id="12071-125">The *AceType* field can be one of the following strings.</span></span>

    | <span data-ttu-id="12071-126">ACE 類型字串</span><span class="sxs-lookup"><span data-stu-id="12071-126">ACE type string</span></span> | <span data-ttu-id="12071-127">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="12071-127">Constant in Sddl.h</span></span>                         | <span data-ttu-id="12071-128">AceType 值</span><span class="sxs-lookup"><span data-stu-id="12071-128">AceType value</span></span>                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | <span data-ttu-id="12071-129">XA</span><span class="sxs-lookup"><span data-stu-id="12071-129">"XA"</span></span><br/> | <span data-ttu-id="12071-130">\_允許 SDDL 回呼 \_ 存取 \_</span><span class="sxs-lookup"><span data-stu-id="12071-130">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span><br/> | <span data-ttu-id="12071-131">存取 \_ 允許的 \_ 回呼 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="12071-131">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE</span></span><br/> |
    | <span data-ttu-id="12071-132">XD</span><span class="sxs-lookup"><span data-stu-id="12071-132">"XD"</span></span><br/> | <span data-ttu-id="12071-133">SDDL \_ 回呼 \_ \_ 拒絕存取</span><span class="sxs-lookup"><span data-stu-id="12071-133">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span><br/>  | <span data-ttu-id="12071-134">\_拒絕存取 \_ 回呼 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="12071-134">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE</span></span><br/>  |

    

     

-   <span data-ttu-id="12071-135">ACE 字串包含一或多個條件運算式，並在字串結尾以括弧括住。</span><span class="sxs-lookup"><span data-stu-id="12071-135">The ACE string includes one or more conditional expressions, enclosed in parentheses at the end of the string.</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="12071-136">條件運算式</span><span class="sxs-lookup"><span data-stu-id="12071-136">Conditional Expressions</span></span>

<span data-ttu-id="12071-137">條件運算式可以包含下列任何元素。</span><span class="sxs-lookup"><span data-stu-id="12071-137">A conditional expression can include any of the following elements.</span></span>



| <span data-ttu-id="12071-138">運算式元素</span><span class="sxs-lookup"><span data-stu-id="12071-138">Expression element</span></span>                                                | <span data-ttu-id="12071-139">Description</span><span class="sxs-lookup"><span data-stu-id="12071-139">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12071-140">*AttributeName*</span><span class="sxs-lookup"><span data-stu-id="12071-140">*AttributeName*</span></span><br/>                                        | <span data-ttu-id="12071-141">測試指定的屬性是否有非零值。</span><span class="sxs-lookup"><span data-stu-id="12071-141">Tests whether the specified attribute has a nonzero value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="12071-142">**存在** *AttributeName*</span><span class="sxs-lookup"><span data-stu-id="12071-142">**exists** *AttributeName*</span></span><br/>                             | <span data-ttu-id="12071-143">測試指定的屬性是否存在於用戶端內容中。</span><span class="sxs-lookup"><span data-stu-id="12071-143">Tests whether the specified attribute exists in the client context.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="12071-144">*AttributeName* *運算子\*\*值*</span><span class="sxs-lookup"><span data-stu-id="12071-144">*AttributeName* *Operator* *Value*</span></span><br/>                     | <span data-ttu-id="12071-145">傳回指定之作業的結果。</span><span class="sxs-lookup"><span data-stu-id="12071-145">Returns the result of the specified operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="12071-146">\* ConditionalExpression \* **\|\|** _ConditionalExpression_</span><span class="sxs-lookup"><span data-stu-id="12071-146">\*ConditionalExpression\***\|\|**_ConditionalExpression_</span></span><br/> | <span data-ttu-id="12071-147">測試其中一個指定的條件運算式是否為 true。</span><span class="sxs-lookup"><span data-stu-id="12071-147">Tests whether either of the specified conditional expressions is true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="12071-148">*ConditionalExpression* \**&&\*\*\*ConditionalExpression*</span><span class="sxs-lookup"><span data-stu-id="12071-148">*ConditionalExpression* **&&** *ConditionalExpression*</span></span><br/> | <span data-ttu-id="12071-149">測試兩個指定的條件運算式是否為 true。</span><span class="sxs-lookup"><span data-stu-id="12071-149">Tests whether both of the specified conditional expressions are true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="12071-150">**！ (** _ConditionalExpression_ *_)_*</span><span class="sxs-lookup"><span data-stu-id="12071-150">**!(**_ConditionalExpression_*_)_*</span></span><br/>                     | <span data-ttu-id="12071-151">條件運算式的反向。</span><span class="sxs-lookup"><span data-stu-id="12071-151">The inverse of a conditional expression.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="12071-152">{_SidArray_*_}_* **\_ 的成員**</span><span class="sxs-lookup"><span data-stu-id="12071-152">**Member\_of{**_SidArray_*_}_*</span></span><br/>                         | <span data-ttu-id="12071-153">測試用戶端內容的 [**SID \_ 和 \_ 屬性**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)陣列是否包含 (sid) 在 *SidArray* 所指定的逗點分隔清單中的所有 [安全識別碼](security-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="12071-153">Tests whether the [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) array of the client context contains all of the [Security Identifiers](security-identifiers.md) (SIDs) in the comma-separated list specified by *SidArray*.</span></span><br/> <span data-ttu-id="12071-154">若為允許 Ace，用戶端內容 SID 必須將 **SE \_ GROUP \_ ENABLED** 屬性設定為視為相符。</span><span class="sxs-lookup"><span data-stu-id="12071-154">For Allow ACEs, a client context SID must have the **SE\_GROUP\_ENABLED** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="12071-155">若為 Deny Ace，用戶端內容 SID 必須 **\_ \_ 啟用 SE 群組** ，否則 **se 群組會使用將「 \_ \_ \_ \_ \_ 僅限拒絕** 」屬性設定為視為相符。</span><span class="sxs-lookup"><span data-stu-id="12071-155">For Deny ACEs, a client context SID must have either the **SE\_GROUP\_ENABLED** or the **SE\_GROUP\_USE\_FOR\_DENY\_ONLY** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="12071-156">*SidArray* 陣列可以包含 sid 字串 (例如 "S-1-5-6" ) 或 sid 別名 (例如 "BA"</span><span class="sxs-lookup"><span data-stu-id="12071-156">The *SidArray* array can contain either SID strings (for example, "S-1-5-6") or SID aliases (for example, "BA"</span></span><br/> |



 

## <a name="attributes"></a><span data-ttu-id="12071-157">屬性</span><span class="sxs-lookup"><span data-stu-id="12071-157">Attributes</span></span>

<span data-ttu-id="12071-158">屬性代表用戶端內容中 [**AUTHZ \_ 安全性 \_ 屬性 \_ 資訊**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) 陣列內的元素。</span><span class="sxs-lookup"><span data-stu-id="12071-158">An attribute represents an element in the [**AUTHZ\_SECURITY\_ATTRIBUTES\_INFORMATION**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) array in the client context.</span></span> <span data-ttu-id="12071-159">屬性名稱可包含任何英數位元和任何字元 "："、"/"、"." 和 " \_ "。</span><span class="sxs-lookup"><span data-stu-id="12071-159">An attribute name can contain any alphanumeric characters and any of the characters ":", "/", ".", and "\_".</span></span>

<span data-ttu-id="12071-160">屬性值可以是下列任何一種類型。</span><span class="sxs-lookup"><span data-stu-id="12071-160">An attribute value can be any of the following types.</span></span>



| <span data-ttu-id="12071-161">值類型</span><span class="sxs-lookup"><span data-stu-id="12071-161">Value type</span></span>         | <span data-ttu-id="12071-162">Description</span><span class="sxs-lookup"><span data-stu-id="12071-162">Description</span></span>                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12071-163">整數</span><span class="sxs-lookup"><span data-stu-id="12071-163">Integer</span></span><br/> | <span data-ttu-id="12071-164">十進位或十六進位標記法中的64位整數。</span><span class="sxs-lookup"><span data-stu-id="12071-164">A 64-bit integer in either decimal or hexadecimal notation.</span></span><br/>                                                                                                                              |
| <span data-ttu-id="12071-165">String</span><span class="sxs-lookup"><span data-stu-id="12071-165">String</span></span><br/>  | <span data-ttu-id="12071-166">以引號分隔的字串值。</span><span class="sxs-lookup"><span data-stu-id="12071-166">A string value delimited by quotes.</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="12071-167">SID</span><span class="sxs-lookup"><span data-stu-id="12071-167">SID</span></span><br/>     | <span data-ttu-id="12071-168">SID (S-1-1-0) 或 SID (BA) 。</span><span class="sxs-lookup"><span data-stu-id="12071-168">SID(S-1-1-0) or SID(BA).</span></span> <span data-ttu-id="12071-169">必須位於的成員 \_ 或裝置成員的 RHS 上 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="12071-169">Has to be on RHS of Member\_of or Device\_Member\_of.</span></span><br/>                                                                                                           |
| <span data-ttu-id="12071-170">BLOB</span><span class="sxs-lookup"><span data-stu-id="12071-170">BLOB</span></span><br/>    | <span data-ttu-id="12071-171">\# 後面接著十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="12071-171">\# followed by hexadecimal numbers.</span></span> <span data-ttu-id="12071-172">如果數位的長度為奇數，則 \# 會轉譯為0以使其成為偶數。</span><span class="sxs-lookup"><span data-stu-id="12071-172">If length of the numbers is odd, then the \# is translated to a 0 to make it even.</span></span> <span data-ttu-id="12071-173">此外 \# ，出現在值的其他位置時，會轉譯為0。</span><span class="sxs-lookup"><span data-stu-id="12071-173">Also an \# appearing elsewhere in the value is translated to a 0.</span></span><br/> |



 

## <a name="operators"></a><span data-ttu-id="12071-174">運算子</span><span class="sxs-lookup"><span data-stu-id="12071-174">Operators</span></span>

<span data-ttu-id="12071-175">下列運算子已定義為在條件運算式中用來測試屬性的值。</span><span class="sxs-lookup"><span data-stu-id="12071-175">The following operators are defined for use in conditional expressions to test the values of attributes.</span></span> <span data-ttu-id="12071-176">這些都是二元運算子，並以 *AttributeName* *運算子\*\*值* 形式使用。</span><span class="sxs-lookup"><span data-stu-id="12071-176">All of these are binary operators and used in the form *AttributeName* *Operator* *Value*.</span></span>



| <span data-ttu-id="12071-177">運算子</span><span class="sxs-lookup"><span data-stu-id="12071-177">Operator</span></span>            | <span data-ttu-id="12071-178">描述</span><span class="sxs-lookup"><span data-stu-id="12071-178">Description</span></span>                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | <span data-ttu-id="12071-179">傳統定義。</span><span class="sxs-lookup"><span data-stu-id="12071-179">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="12071-180">!=</span><span class="sxs-lookup"><span data-stu-id="12071-180">!=</span></span><br/>       | <span data-ttu-id="12071-181">傳統定義。</span><span class="sxs-lookup"><span data-stu-id="12071-181">Conventional definition.</span></span><br/>                                                                                      |
| <<br/>     | <span data-ttu-id="12071-182">傳統定義。</span><span class="sxs-lookup"><span data-stu-id="12071-182">Conventional definition.</span></span><br/>                                                                                      |
| <=<br/>    | <span data-ttu-id="12071-183">傳統定義。</span><span class="sxs-lookup"><span data-stu-id="12071-183">Conventional definition.</span></span><br/>                                                                                      |
| ><br/>     | <span data-ttu-id="12071-184">傳統定義。</span><span class="sxs-lookup"><span data-stu-id="12071-184">Conventional definition.</span></span><br/>                                                                                      |
| >=<br/>    | <span data-ttu-id="12071-185">傳統定義。</span><span class="sxs-lookup"><span data-stu-id="12071-185">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="12071-186">包含</span><span class="sxs-lookup"><span data-stu-id="12071-186">Contains</span></span><br/> | <span data-ttu-id="12071-187">如果指定屬性的值是指定值的超集合，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="12071-187">**TRUE** if the value of the specified attribute is a superset of the specified value; otherwise, **FALSE**.</span></span><br/>  |
| <span data-ttu-id="12071-188">任何 \_</span><span class="sxs-lookup"><span data-stu-id="12071-188">Any\_of</span></span><br/>  | <span data-ttu-id="12071-189">如果指定的值為指定屬性值的超集合，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="12071-189">**TRUE** if the specified value is a superset of the value of the specified attribute; otherwise, **FALSE**.</span></span> <br/> |



 

<span data-ttu-id="12071-190">此外，一元運算子存在、成員 \_ 和否定 (！ ) 的定義方式如條件運算式資料表中所述。</span><span class="sxs-lookup"><span data-stu-id="12071-190">In addition, the unary operators Exists, Member\_of, and negation (!) are defined as described in the Conditional Expressions table.</span></span>

<span data-ttu-id="12071-191">"Contains" 運算子前面必須加上空白字元，且 "Any of \_ " 運算子之前必須加上空白字元。</span><span class="sxs-lookup"><span data-stu-id="12071-191">The "Contains" operator must be preceded and followed by white space, and the "Any\_of" operator must be preceded by white space.</span></span>

## <a name="operator-precedence"></a><span data-ttu-id="12071-192">運算子優先順序</span><span class="sxs-lookup"><span data-stu-id="12071-192">Operator Precedence</span></span>

<span data-ttu-id="12071-193">系統會依照下列優先順序來評估運算子，而且會從左至右評估相等優先順序的作業。</span><span class="sxs-lookup"><span data-stu-id="12071-193">The operators are evaluated in the following order of precedence, with operations of equal precedence being evaluated from left to right.</span></span>

1.  <span data-ttu-id="12071-194">存在 \_ ，成員隸屬于</span><span class="sxs-lookup"><span data-stu-id="12071-194">Exists, Member\_of</span></span>
2.  <span data-ttu-id="12071-195">Contains \_ 、任何</span><span class="sxs-lookup"><span data-stu-id="12071-195">Contains, Any\_of</span></span>
3.  <span data-ttu-id="12071-196">= =、！ =、<、<=、>、>=</span><span class="sxs-lookup"><span data-stu-id="12071-196">==, !=, <, <=, >, >=</span></span>
4.  <span data-ttu-id="12071-197">!</span><span class="sxs-lookup"><span data-stu-id="12071-197">!</span></span>
5.  &&
6.  \|\|

<span data-ttu-id="12071-198">此外，條件運算式的任何部分都可以用括弧括住。</span><span class="sxs-lookup"><span data-stu-id="12071-198">In addition, any portion of a conditional expression can be enclosed in parenthesis.</span></span> <span data-ttu-id="12071-199">括弧內的運算式會先評估。</span><span class="sxs-lookup"><span data-stu-id="12071-199">Expressions within parentheses are evaluated first.</span></span>

## <a name="unknown-values"></a><span data-ttu-id="12071-200">未知的值</span><span class="sxs-lookup"><span data-stu-id="12071-200">Unknown Values</span></span>

<span data-ttu-id="12071-201">條件運算式的結果有時會傳回 **未知** 的值。</span><span class="sxs-lookup"><span data-stu-id="12071-201">The results of conditional expressions sometimes return a value of **Unknown**.</span></span> <span data-ttu-id="12071-202">例如，當指定的屬性不存在時，任何關聯式作業都會傳回 **Unknown** 。</span><span class="sxs-lookup"><span data-stu-id="12071-202">For example, any of the relational operations return **Unknown** when the specified attribute does not exist.</span></span>

<span data-ttu-id="12071-203">下表描述兩個條件運算式（ *ConditionalExpression1* 和 *ConditionalExpression2*）之間邏輯 **AND** 運算的結果。</span><span class="sxs-lookup"><span data-stu-id="12071-203">The following table describes the results for a logical **AND** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="12071-204">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="12071-204">*ConditionalExpression1*</span></span> | <span data-ttu-id="12071-205">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="12071-205">*ConditionalExpression2*</span></span> | <span data-ttu-id="12071-206">*ConditionalExpression1* \**&&\*\*\*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="12071-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|----------------------------------------------------------|
| <span data-ttu-id="12071-207">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-207">**TRUE**</span></span><br/>      | <span data-ttu-id="12071-208">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-208">**TRUE**</span></span><br/>      | <span data-ttu-id="12071-209">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-209">**TRUE**</span></span><br/>                                      |
| <span data-ttu-id="12071-210">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-210">**TRUE**</span></span><br/>      | <span data-ttu-id="12071-211">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-211">**FALSE**</span></span><br/>     | <span data-ttu-id="12071-212">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-212">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="12071-213">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-213">**TRUE**</span></span><br/>      | <span data-ttu-id="12071-214">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-214">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="12071-215">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-215">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="12071-216">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-216">**FALSE**</span></span><br/>     | <span data-ttu-id="12071-217">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-217">**TRUE**</span></span><br/>      | <span data-ttu-id="12071-218">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-218">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="12071-219">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-219">**FALSE**</span></span><br/>     | <span data-ttu-id="12071-220">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-220">**FALSE**</span></span><br/>     | <span data-ttu-id="12071-221">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-221">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="12071-222">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-222">**FALSE**</span></span><br/>     | <span data-ttu-id="12071-223">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-223">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="12071-224">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-224">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="12071-225">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-225">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="12071-226">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-226">**TRUE**</span></span><br/>      | <span data-ttu-id="12071-227">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-227">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="12071-228">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-228">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="12071-229">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-229">**FALSE**</span></span><br/>     | <span data-ttu-id="12071-230">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-230">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="12071-231">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-231">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="12071-232">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-232">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="12071-233">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-233">**UNKNOWN**</span></span><br/>                                   |



 

<span data-ttu-id="12071-234">下表描述兩個條件運算式（ *ConditionalExpression1* 和 *ConditionalExpression2*）之間的邏輯 **OR** 運算結果。</span><span class="sxs-lookup"><span data-stu-id="12071-234">The following table describes the results for a logical **OR** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="12071-235">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="12071-235">*ConditionalExpression1*</span></span> | <span data-ttu-id="12071-236">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="12071-236">*ConditionalExpression2*</span></span> | <span data-ttu-id="12071-237">*ConditionalExpression1* \*\*</span><span class="sxs-lookup"><span data-stu-id="12071-237">*ConditionalExpression1* \*\*</span></span>\|\|<span data-ttu-id="12071-238">\*\* *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="12071-238">\*\* *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|------------------------------------------------------------|
| <span data-ttu-id="12071-239">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-239">**TRUE**</span></span><br/>      | <span data-ttu-id="12071-240">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-240">**TRUE**</span></span><br/>      | <span data-ttu-id="12071-241">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-241">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="12071-242">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-242">**TRUE**</span></span><br/>      | <span data-ttu-id="12071-243">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-243">**FALSE**</span></span><br/>     | <span data-ttu-id="12071-244">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-244">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="12071-245">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-245">**TRUE**</span></span><br/>      | <span data-ttu-id="12071-246">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-246">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="12071-247">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-247">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="12071-248">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-248">**FALSE**</span></span><br/>     | <span data-ttu-id="12071-249">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-249">**TRUE**</span></span><br/>      | <span data-ttu-id="12071-250">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-250">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="12071-251">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-251">**FALSE**</span></span><br/>     | <span data-ttu-id="12071-252">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-252">**FALSE**</span></span><br/>     | <span data-ttu-id="12071-253">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-253">**FALSE**</span></span><br/>                                       |
| <span data-ttu-id="12071-254">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-254">**FALSE**</span></span><br/>     | <span data-ttu-id="12071-255">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-255">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="12071-256">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-256">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="12071-257">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-257">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="12071-258">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-258">**TRUE**</span></span><br/>      | <span data-ttu-id="12071-259">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="12071-259">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="12071-260">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-260">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="12071-261">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="12071-261">**FALSE**</span></span><br/>     | <span data-ttu-id="12071-262">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-262">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="12071-263">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-263">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="12071-264">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-264">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="12071-265">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="12071-265">**UNKNOWN**</span></span><br/>                                     |



 

<span data-ttu-id="12071-266">具有 **未知** 值的條件運算式的否定也是 **未知** 的。</span><span class="sxs-lookup"><span data-stu-id="12071-266">The negation of a conditional expression with a value of **UNKNOWN** is also **UNKNOWN**.</span></span>

## <a name="conditional-ace-evaluation"></a><span data-ttu-id="12071-267">條件式 ACE 評估</span><span class="sxs-lookup"><span data-stu-id="12071-267">Conditional ACE Evaluation</span></span>

<span data-ttu-id="12071-268">下表描述條件式 ACE 的存取檢查結果，取決於條件運算式的最後評估。</span><span class="sxs-lookup"><span data-stu-id="12071-268">The following table describes the access check result of a conditional ACE depending on the final evaluation of the conditional expression.</span></span>

| <span data-ttu-id="12071-269">ACE 類型</span><span class="sxs-lookup"><span data-stu-id="12071-269">ACE type</span></span>         | <span data-ttu-id="12071-270">true</span><span class="sxs-lookup"><span data-stu-id="12071-270">TRUE</span></span>             | <span data-ttu-id="12071-271">FALSE</span><span class="sxs-lookup"><span data-stu-id="12071-271">FALSE</span></span>                 | <span data-ttu-id="12071-272">UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="12071-272">UNKNOWN</span></span>               |
|------------------|------------------|-----------------------|-----------------------|
| <span data-ttu-id="12071-273">Allow</span><span class="sxs-lookup"><span data-stu-id="12071-273">Allow</span></span><br/> | <span data-ttu-id="12071-274">Allow</span><span class="sxs-lookup"><span data-stu-id="12071-274">Allow</span></span><br/> | <span data-ttu-id="12071-275">忽略 ACE</span><span class="sxs-lookup"><span data-stu-id="12071-275">Ignore ACE</span></span><br/> | <span data-ttu-id="12071-276">忽略 ACE</span><span class="sxs-lookup"><span data-stu-id="12071-276">Ignore ACE</span></span><br/> |
| <span data-ttu-id="12071-277">拒絕</span><span class="sxs-lookup"><span data-stu-id="12071-277">Deny</span></span><br/>  | <span data-ttu-id="12071-278">拒絕</span><span class="sxs-lookup"><span data-stu-id="12071-278">Deny</span></span><br/>  | <span data-ttu-id="12071-279">忽略 ACE</span><span class="sxs-lookup"><span data-stu-id="12071-279">Ignore ACE</span></span><br/> | <span data-ttu-id="12071-280">拒絕</span><span class="sxs-lookup"><span data-stu-id="12071-280">Deny</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="12071-281">範例</span><span class="sxs-lookup"><span data-stu-id="12071-281">Examples</span></span>

<span data-ttu-id="12071-282">下列範例顯示如何使用 SDDL 定義的條件 ACE 來表示指定的存取原則。</span><span class="sxs-lookup"><span data-stu-id="12071-282">The following examples show how the specified access policies are represented by a conditional ACE defined by using SDDL.</span></span>

<dl> <dt>

<span data-ttu-id="12071-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>政策</span><span class="sxs-lookup"><span data-stu-id="12071-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="12071-284">如果符合下列兩個條件，允許執行至所有人：</span><span class="sxs-lookup"><span data-stu-id="12071-284">Allow Execute to Everyone if both of the following conditions are met:</span></span>

-   <span data-ttu-id="12071-285">標題 = PM</span><span class="sxs-lookup"><span data-stu-id="12071-285">Title = PM</span></span>
-   <span data-ttu-id="12071-286">部門 = 財務或部門 = 銷售</span><span class="sxs-lookup"><span data-stu-id="12071-286">Division = Finance or Division = Sales</span></span>

</dd> <dt>

<span data-ttu-id="12071-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="12071-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="12071-288">D： (XA;;FX;;;S-1-1-0; (@User.Title = = "PM"  &&  (@User.Division = = "財務" \| \| @User.Division = = "Sales" ) ) ) </span><span class="sxs-lookup"><span data-stu-id="12071-288">D:(XA; ;FX;;;S-1-1-0; (@User.Title=="PM" && (@User.Division=="Finance" \|\| @User.Division ==" Sales")))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="12071-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>政策</span><span class="sxs-lookup"><span data-stu-id="12071-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="12071-290">如果任何使用者專案與檔案的專案相交，則允許執行。</span><span class="sxs-lookup"><span data-stu-id="12071-290">Allow execute if any of the user s projects intersect with the file s projects.</span></span>

</dd> <dt>

<span data-ttu-id="12071-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="12071-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="12071-292">D： (XA;;FX;;;S-1-1-0; (@User.Project 任何 \_ @Resource.Project) ) </span><span class="sxs-lookup"><span data-stu-id="12071-292">D:(XA; ;FX;;;S-1-1-0; (@User.Project Any\_of @Resource.Project))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="12071-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>政策</span><span class="sxs-lookup"><span data-stu-id="12071-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="12071-294">如果使用者使用智慧卡登入、是備份操作員，並且從已啟用 Bitlocker 的電腦進行連線，則允許讀取存取。</span><span class="sxs-lookup"><span data-stu-id="12071-294">Allow read access if the user has logged in with a smart card, is a backup operator, and is connecting from a machine with Bitlocker enabled.</span></span>

</dd> <dt>

<span data-ttu-id="12071-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="12071-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="12071-296">D： (XA;; FR;;;S-1-1-0; (成員 \_ {SID (智慧卡 \_ SID) ，SID (BO) }  && @Device.Bitlocker) ) </span><span class="sxs-lookup"><span data-stu-id="12071-296">D:(XA; ;FR;;;S-1-1-0; (Member\_of {SID(Smartcard\_SID), SID(BO)} && @Device.Bitlocker))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="12071-297">相關主題</span><span class="sxs-lookup"><span data-stu-id="12071-297">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="12071-298">[\[DTYP \] ：安全描述項描述語言](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="12071-298">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

