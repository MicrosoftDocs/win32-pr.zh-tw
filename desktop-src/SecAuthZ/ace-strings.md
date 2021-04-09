---
description: 說明在存取控制專案中使用的字串。
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: ACE 字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a35bde18a1ca3ac416faa42e3b693e26305beb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692771"
---
# <a name="ace-strings"></a><span data-ttu-id="d0101-103">ACE 字串</span><span class="sxs-lookup"><span data-stu-id="d0101-103">ACE Strings</span></span>

<span data-ttu-id="d0101-104">[安全描述項定義語言](security-descriptor-definition-language.md) (SDDL) 在 [*安全描述項*](/windows/desktop/SecGloss/s-gly)字串的 DACL 和 SACL 元件中使用 ACE 字串。</span><span class="sxs-lookup"><span data-stu-id="d0101-104">The [security descriptor definition language](security-descriptor-definition-language.md) (SDDL) uses ACE strings in the DACL and SACL components of a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string.</span></span>

<span data-ttu-id="d0101-105">如 [安全描述項字串格式](security-descriptor-string-format.md) 範例所示，安全描述項字串中的每個 ACE 都會以括弧括住。</span><span class="sxs-lookup"><span data-stu-id="d0101-105">As shown in the [Security Descriptor String Format](security-descriptor-string-format.md) examples, each ACE in a security descriptor string is enclosed in parentheses.</span></span> <span data-ttu-id="d0101-106">ACE 的欄位會以下列順序排列，並以分號分隔 (; ) 。</span><span class="sxs-lookup"><span data-stu-id="d0101-106">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="d0101-107">條件式 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) 的格式與其他 ace 類型 (ace) 不同。</span><span class="sxs-lookup"><span data-stu-id="d0101-107">There is a different format for conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) than other ACE types.</span></span> <span data-ttu-id="d0101-108">針對條件式 Ace，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)。</span><span class="sxs-lookup"><span data-stu-id="d0101-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a><span data-ttu-id="d0101-109">欄位</span><span class="sxs-lookup"><span data-stu-id="d0101-109">Fields</span></span>

<dl> <dt>

<span data-ttu-id="d0101-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**ace \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d0101-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**ace\_type**</span></span>
</dt> <dd>

<span data-ttu-id="d0101-111">字串，指出 [**ACE \_ 標頭**](/windows/desktop/api/Winnt/ns-winnt-ace_header)結構之 **AceType** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="d0101-111">A string that indicates the value of the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="d0101-112">ACE 類型字串可以是在 Sddl 中定義的下列其中一個字串。</span><span class="sxs-lookup"><span data-stu-id="d0101-112">The ACE type string can be one of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="d0101-113">ACE 類型字串</span><span class="sxs-lookup"><span data-stu-id="d0101-113">ACE type string</span></span> | <span data-ttu-id="d0101-114">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="d0101-114">Constant in Sddl.h</span></span>                      | <span data-ttu-id="d0101-115">AceType 值</span><span class="sxs-lookup"><span data-stu-id="d0101-115">AceType value</span></span>                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0101-116">"A"</span><span class="sxs-lookup"><span data-stu-id="d0101-116">"A"</span></span>             | <span data-ttu-id="d0101-117">\_允許 SDDL 存取 \_</span><span class="sxs-lookup"><span data-stu-id="d0101-117">SDDL\_ACCESS\_ALLOWED</span></span>                   | <span data-ttu-id="d0101-118">存取 \_ 允許的 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="d0101-118">ACCESS\_ALLOWED\_ACE\_TYPE</span></span>                                                                                                                                         |
| <span data-ttu-id="d0101-119">"D"</span><span class="sxs-lookup"><span data-stu-id="d0101-119">"D"</span></span>             | <span data-ttu-id="d0101-120">SDDL \_ \_ 拒絕存取</span><span class="sxs-lookup"><span data-stu-id="d0101-120">SDDL\_ACCESS\_DENIED</span></span>                    | <span data-ttu-id="d0101-121">\_拒絕存取 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="d0101-121">ACCESS\_DENIED\_ACE\_TYPE</span></span>                                                                                                                                          |
| <span data-ttu-id="d0101-122">OA</span><span class="sxs-lookup"><span data-stu-id="d0101-122">"OA"</span></span>            | <span data-ttu-id="d0101-123">\_允許 SDDL 物件 \_ 存取 \_</span><span class="sxs-lookup"><span data-stu-id="d0101-123">SDDL\_OBJECT\_ACCESS\_ALLOWED</span></span>           | <span data-ttu-id="d0101-124">存取 \_ 允許的 \_ 物件 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="d0101-124">ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                 |
| <span data-ttu-id="d0101-125">OD</span><span class="sxs-lookup"><span data-stu-id="d0101-125">"OD"</span></span>            | <span data-ttu-id="d0101-126">SDDL \_ 物件 \_ \_ 拒絕存取</span><span class="sxs-lookup"><span data-stu-id="d0101-126">SDDL\_OBJECT\_ACCESS\_DENIED</span></span>            | <span data-ttu-id="d0101-127">\_拒絕存取 \_ 物件 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="d0101-127">ACCESS\_DENIED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                  |
| <span data-ttu-id="d0101-128">澳大利亞</span><span class="sxs-lookup"><span data-stu-id="d0101-128">"AU"</span></span>            | <span data-ttu-id="d0101-129">SDDL \_ 審核</span><span class="sxs-lookup"><span data-stu-id="d0101-129">SDDL\_AUDIT</span></span>                             | <span data-ttu-id="d0101-130">系統 \_ 審核 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="d0101-130">SYSTEM\_AUDIT\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="d0101-131">"AL"</span><span class="sxs-lookup"><span data-stu-id="d0101-131">"AL"</span></span>            | <span data-ttu-id="d0101-132">SDDL \_ 警示</span><span class="sxs-lookup"><span data-stu-id="d0101-132">SDDL\_ALARM</span></span>                             | <span data-ttu-id="d0101-133">系統 \_ 警示 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="d0101-133">SYSTEM\_ALARM\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="d0101-134">/OU</span><span class="sxs-lookup"><span data-stu-id="d0101-134">"OU"</span></span>            | <span data-ttu-id="d0101-135">SDDL \_ 物件 \_ AUDIT</span><span class="sxs-lookup"><span data-stu-id="d0101-135">SDDL\_OBJECT\_AUDIT</span></span>                     | <span data-ttu-id="d0101-136">SYSTEM \_ AUDIT \_ OBJECT \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="d0101-136">SYSTEM\_AUDIT\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="d0101-137">歐</span><span class="sxs-lookup"><span data-stu-id="d0101-137">"OL"</span></span>            | <span data-ttu-id="d0101-138">SDDL \_ 物件 \_ 警示</span><span class="sxs-lookup"><span data-stu-id="d0101-138">SDDL\_OBJECT\_ALARM</span></span>                     | <span data-ttu-id="d0101-139">系統 \_ 警報 \_ 物件 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="d0101-139">SYSTEM\_ALARM\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="d0101-140">ML</span><span class="sxs-lookup"><span data-stu-id="d0101-140">"ML"</span></span>            | <span data-ttu-id="d0101-141">SDDL \_ 強制 \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="d0101-141">SDDL\_MANDATORY\_LABEL</span></span>                  | <span data-ttu-id="d0101-142">系統 \_ 強制 \_ 標籤 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="d0101-142">SYSTEM\_MANDATORY\_LABEL\_ACE\_TYPE</span></span>                                                                                                                                |
| <span data-ttu-id="d0101-143">XA</span><span class="sxs-lookup"><span data-stu-id="d0101-143">"XA"</span></span>            | <span data-ttu-id="d0101-144">\_允許 SDDL 回呼 \_ 存取 \_</span><span class="sxs-lookup"><span data-stu-id="d0101-144">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span>         | <span data-ttu-id="d0101-145">存取 \_ 允許 \_ \_ 的回呼 ACE \_ 類型 **windows Vista 和 windows Server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="d0101-145">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                           |
| <span data-ttu-id="d0101-146">XD</span><span class="sxs-lookup"><span data-stu-id="d0101-146">"XD"</span></span>            | <span data-ttu-id="d0101-147">SDDL \_ 回呼 \_ \_ 拒絕存取</span><span class="sxs-lookup"><span data-stu-id="d0101-147">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span>          | <span data-ttu-id="d0101-148">\_拒絕存取 \_ 回呼 \_ ACE \_ 類型 **Windows Vista 和 Windows Server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="d0101-148">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE **Windows Vista and Windows Server 2003:** Not available.</span></span><br/>                                                            |
| <span data-ttu-id="d0101-149">RA</span><span class="sxs-lookup"><span data-stu-id="d0101-149">"RA"</span></span>            | <span data-ttu-id="d0101-150">SDDL \_ 資源 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="d0101-150">SDDL\_RESOURCE\_ATTRIBUTE</span></span>               | <span data-ttu-id="d0101-151">系統 \_ 資源 \_ 屬性 \_ ACE \_ 類型 **： Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 windows Server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="d0101-151">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/> |
| <span data-ttu-id="d0101-152">SP-1</span><span class="sxs-lookup"><span data-stu-id="d0101-152">"SP"</span></span>            | <span data-ttu-id="d0101-153">SDDL \_ 範圍 \_ 原則 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="d0101-153">SDDL\_SCOPED\_POLICY\_ID</span></span>                | <span data-ttu-id="d0101-154">系統 \_ 範圍 \_ 原則 \_ 識別碼 \_ ACE \_ 類型 **： Windows server 2008 R2、windows 7、windows Server 2008、windows Vista 和 windows Server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="d0101-154">SYSTEM\_SCOPED\_POLICY\_ID\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>  |
| <span data-ttu-id="d0101-155">XU</span><span class="sxs-lookup"><span data-stu-id="d0101-155">"XU"</span></span>            | <span data-ttu-id="d0101-156">SDDL \_ 回呼 \_ 審核</span><span class="sxs-lookup"><span data-stu-id="d0101-156">SDDL\_CALLBACK\_AUDIT</span></span>                   | <span data-ttu-id="d0101-157">系統 \_ AUDIT \_ 回呼 \_ ACE \_ 類型 **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 windows Server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="d0101-157">SYSTEM\_AUDIT\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>     |
| <span data-ttu-id="d0101-158">ZA</span><span class="sxs-lookup"><span data-stu-id="d0101-158">"ZA"</span></span>            | <span data-ttu-id="d0101-159">\_允許 SDDL 回呼 \_ 物件 \_ 存取 \_</span><span class="sxs-lookup"><span data-stu-id="d0101-159">SDDL\_CALLBACK\_OBJECT\_ACCESS\_ALLOWED</span></span> | <span data-ttu-id="d0101-160">存取 \_ 允許 \_ \_ 的回呼 ACE \_ 類型 **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 windows Server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="d0101-160">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="d0101-161">如果 **ace \_ 類型** 為 access \_ 允許 \_ \_ 的物件 ace \_ 類型， **而且物件 \_ guid** 或 **繼承 \_ 物件 \_ guid** 都未指定 [**guid**](/windows/win32/api/guiddef/ns-guiddef-guid) ，則 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 會將 **ace \_ 類型** 轉換成存取允許的 \_ \_ ace \_ 類型。</span><span class="sxs-lookup"><span data-stu-id="d0101-161">If **ace\_type** is ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE and neither **object\_guid** nor **inherit\_object\_guid** has a [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) specified, then [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converts **ace\_type** to ACCESS\_ALLOWED\_ACE\_TYPE.</span></span>

 

</dd> <dt>

<span data-ttu-id="d0101-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ace \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="d0101-162"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ace\_flags**</span></span>
</dt> <dd>

<span data-ttu-id="d0101-163">字串，指出 [**ACE \_ 標頭**](/windows/desktop/api/Winnt/ns-winnt-ace_header)結構之 **AceFlags** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="d0101-163">A string that indicates the value of the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="d0101-164">ACE 旗標字串可以是以 Sddl. h 定義的下列字串的串連。</span><span class="sxs-lookup"><span data-stu-id="d0101-164">The ACE flags string can be a concatenation of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="d0101-165">ACE 旗標字串</span><span class="sxs-lookup"><span data-stu-id="d0101-165">ACE flags string</span></span> | <span data-ttu-id="d0101-166">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="d0101-166">Constant in Sddl.h</span></span>       | <span data-ttu-id="d0101-167">AceFlag 值</span><span class="sxs-lookup"><span data-stu-id="d0101-167">AceFlag value</span></span>                 |
|------------------|--------------------------|-------------------------------|
| <span data-ttu-id="d0101-168">CI</span><span class="sxs-lookup"><span data-stu-id="d0101-168">"CI"</span></span>             | <span data-ttu-id="d0101-169">SDDL \_ 容器 \_ 繼承</span><span class="sxs-lookup"><span data-stu-id="d0101-169">SDDL\_CONTAINER\_INHERIT</span></span> | <span data-ttu-id="d0101-170">容器 \_ 繼承 \_ ACE</span><span class="sxs-lookup"><span data-stu-id="d0101-170">CONTAINER\_INHERIT\_ACE</span></span>       |
| <span data-ttu-id="d0101-171">OI</span><span class="sxs-lookup"><span data-stu-id="d0101-171">"OI"</span></span>             | <span data-ttu-id="d0101-172">SDDL \_ 物件 \_ 繼承</span><span class="sxs-lookup"><span data-stu-id="d0101-172">SDDL\_OBJECT\_INHERIT</span></span>    | <span data-ttu-id="d0101-173">OBJECT \_ INHERIT \_ ACE</span><span class="sxs-lookup"><span data-stu-id="d0101-173">OBJECT\_INHERIT\_ACE</span></span>          |
| <span data-ttu-id="d0101-174">NP-IN</span><span class="sxs-lookup"><span data-stu-id="d0101-174">"NP"</span></span>             | <span data-ttu-id="d0101-175">SDDL \_ 沒有 \_ 傳播</span><span class="sxs-lookup"><span data-stu-id="d0101-175">SDDL\_NO\_PROPAGATE</span></span>      | <span data-ttu-id="d0101-176">沒有 \_ 傳播 \_ 繼承 \_ ACE</span><span class="sxs-lookup"><span data-stu-id="d0101-176">NO\_PROPAGATE\_INHERIT\_ACE</span></span>   |
| <span data-ttu-id="d0101-177">IO</span><span class="sxs-lookup"><span data-stu-id="d0101-177">"IO"</span></span>             | <span data-ttu-id="d0101-178">SDDL \_ \_ 只繼承</span><span class="sxs-lookup"><span data-stu-id="d0101-178">SDDL\_INHERIT\_ONLY</span></span>      | <span data-ttu-id="d0101-179">\_只繼承 \_ ACE</span><span class="sxs-lookup"><span data-stu-id="d0101-179">INHERIT\_ONLY\_ACE</span></span>            |
| <span data-ttu-id="d0101-180">「識別碼」</span><span class="sxs-lookup"><span data-stu-id="d0101-180">"ID"</span></span>             | <span data-ttu-id="d0101-181">SDDL \_ 繼承</span><span class="sxs-lookup"><span data-stu-id="d0101-181">SDDL\_INHERITED</span></span>          | <span data-ttu-id="d0101-182">繼承的 \_ ACE</span><span class="sxs-lookup"><span data-stu-id="d0101-182">INHERITED\_ACE</span></span>                |
| <span data-ttu-id="d0101-183">SA</span><span class="sxs-lookup"><span data-stu-id="d0101-183">"SA"</span></span>             | <span data-ttu-id="d0101-184">SDDL \_ 審核 \_ 成功</span><span class="sxs-lookup"><span data-stu-id="d0101-184">SDDL\_AUDIT\_SUCCESS</span></span>     | <span data-ttu-id="d0101-185">成功的 \_ 存取 \_ ACE \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="d0101-185">SUCCESSFUL\_ACCESS\_ACE\_FLAG</span></span> |
| <span data-ttu-id="d0101-186">FA</span><span class="sxs-lookup"><span data-stu-id="d0101-186">"FA"</span></span>             | <span data-ttu-id="d0101-187">SDDL \_ 審核 \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="d0101-187">SDDL\_AUDIT\_FAILURE</span></span>     | <span data-ttu-id="d0101-188">\_存取 \_ ACE \_ 旗標失敗</span><span class="sxs-lookup"><span data-stu-id="d0101-188">FAILED\_ACCESS\_ACE\_FLAG</span></span>     |



 

</dd> <dt>

<span data-ttu-id="d0101-189"><span id="rights"></span><span id="RIGHTS"></span>**權利**</span><span class="sxs-lookup"><span data-stu-id="d0101-189"><span id="rights"></span><span id="RIGHTS"></span>**rights**</span></span>
</dt> <dd>

<span data-ttu-id="d0101-190">表示由 ACE 所控制之 [存取權限](access-rights-and-access-masks.md) 的字串。</span><span class="sxs-lookup"><span data-stu-id="d0101-190">A string that indicates the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span> <span data-ttu-id="d0101-191">這個字串可以是存取權限的十六進位字串標記法（例如 "0x7800003F"），也可以是下列字串的串連。</span><span class="sxs-lookup"><span data-stu-id="d0101-191">This string can be a hexadecimal string representation of the access rights, such as "0x7800003F", or it can be a concatenation of the following strings.</span></span>



### <a name="generic-access-rights"></a><span data-ttu-id="d0101-192">一般存取權限</span><span class="sxs-lookup"><span data-stu-id="d0101-192">Generic access rights</span></span>

| <span data-ttu-id="d0101-193">存取權限字串</span><span class="sxs-lookup"><span data-stu-id="d0101-193">Access rights string</span></span> | <span data-ttu-id="d0101-194">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="d0101-194">Constant in Sddl.h</span></span> | <span data-ttu-id="d0101-195">存取權限值</span><span class="sxs-lookup"><span data-stu-id="d0101-195">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="d0101-196">正式</span><span class="sxs-lookup"><span data-stu-id="d0101-196">"GA"</span></span>                 | <span data-ttu-id="d0101-197">SDDL \_ 泛型 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="d0101-197">SDDL\_GENERIC\_ALL</span></span> | <span data-ttu-id="d0101-198">一般 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="d0101-198">GENERIC\_ALL</span></span>       |
| <span data-ttu-id="d0101-199">GR</span><span class="sxs-lookup"><span data-stu-id="d0101-199">"GR"</span></span>                 | <span data-ttu-id="d0101-200">SDDL \_ 一般 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="d0101-200">SDDL\_GENERIC\_READ</span></span> | <span data-ttu-id="d0101-201">一般 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="d0101-201">GENERIC\_READ</span></span>     |
| <span data-ttu-id="d0101-202">GW</span><span class="sxs-lookup"><span data-stu-id="d0101-202">"GW"</span></span>                 | <span data-ttu-id="d0101-203">SDDL \_ 一般 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="d0101-203">SDDL\_GENERIC\_WRITE</span></span> | <span data-ttu-id="d0101-204">一般 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="d0101-204">GENERIC\_WRITE</span></span> |
| <span data-ttu-id="d0101-205">GX</span><span class="sxs-lookup"><span data-stu-id="d0101-205">"GX"</span></span>                 | <span data-ttu-id="d0101-206">SDDL \_ 泛型 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="d0101-206">SDDL\_GENERIC\_EXECUTE</span></span> | <span data-ttu-id="d0101-207">一般 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="d0101-207">GENERIC\_EXECUTE</span></span> |


### <a name="standard-access-rights"></a><span data-ttu-id="d0101-208">標準存取權限</span><span class="sxs-lookup"><span data-stu-id="d0101-208">Standard access rights</span></span>

| <span data-ttu-id="d0101-209">存取權限字串</span><span class="sxs-lookup"><span data-stu-id="d0101-209">Access rights string</span></span> | <span data-ttu-id="d0101-210">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="d0101-210">Constant in Sddl.h</span></span> | <span data-ttu-id="d0101-211">存取權限值</span><span class="sxs-lookup"><span data-stu-id="d0101-211">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="d0101-212">RC</span><span class="sxs-lookup"><span data-stu-id="d0101-212">"RC"</span></span>                 | <span data-ttu-id="d0101-213">SDDL \_ 讀取 \_ 控制</span><span class="sxs-lookup"><span data-stu-id="d0101-213">SDDL\_READ\_CONTROL</span></span> | <span data-ttu-id="d0101-214">讀取 \_ 控制</span><span class="sxs-lookup"><span data-stu-id="d0101-214">READ\_CONTROL</span></span>      |
| <span data-ttu-id="d0101-215">SD</span><span class="sxs-lookup"><span data-stu-id="d0101-215">"SD"</span></span>                 | <span data-ttu-id="d0101-216">SDDL \_ 標準 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="d0101-216">SDDL\_STANDARD\_DELETE</span></span> | <span data-ttu-id="d0101-217">刪除</span><span class="sxs-lookup"><span data-stu-id="d0101-217">DELETE</span></span>          |
| <span data-ttu-id="d0101-218">WD</span><span class="sxs-lookup"><span data-stu-id="d0101-218">"WD"</span></span>                 | <span data-ttu-id="d0101-219">SDDL \_ 寫入 \_ DAC</span><span class="sxs-lookup"><span data-stu-id="d0101-219">SDDL\_WRITE\_DAC</span></span> | <span data-ttu-id="d0101-220">寫入 \_ DAC</span><span class="sxs-lookup"><span data-stu-id="d0101-220">WRITE\_DAC</span></span>            |
| <span data-ttu-id="d0101-221">WO</span><span class="sxs-lookup"><span data-stu-id="d0101-221">"WO"</span></span>                 | <span data-ttu-id="d0101-222">SDDL \_ 寫入 \_ 擁有者</span><span class="sxs-lookup"><span data-stu-id="d0101-222">SDDL\_WRITE\_OWNER</span></span> | <span data-ttu-id="d0101-223">寫入 \_ 擁有者</span><span class="sxs-lookup"><span data-stu-id="d0101-223">WRITE\_OWNER</span></span>        |

### <a name="directory-service-object-access-rights"></a><span data-ttu-id="d0101-224">目錄服務物件存取權限</span><span class="sxs-lookup"><span data-stu-id="d0101-224">Directory service object access rights</span></span>

| <span data-ttu-id="d0101-225">存取權限字串</span><span class="sxs-lookup"><span data-stu-id="d0101-225">Access rights string</span></span> | <span data-ttu-id="d0101-226">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="d0101-226">Constant in Sddl.h</span></span> | <span data-ttu-id="d0101-227">存取權限值</span><span class="sxs-lookup"><span data-stu-id="d0101-227">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="d0101-228">開頭</span><span class="sxs-lookup"><span data-stu-id="d0101-228">"RP"</span></span>                 | <span data-ttu-id="d0101-229">SDDL \_ 讀取 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="d0101-229">SDDL\_READ\_PROPERTY</span></span> | <span data-ttu-id="d0101-230">ADS \_ 正確的 \_ DS \_ 讀取 \_</span><span class="sxs-lookup"><span data-stu-id="d0101-230">ADS\_RIGHT\_DS\_READ\_PROP</span></span> |
| <span data-ttu-id="d0101-231">WP</span><span class="sxs-lookup"><span data-stu-id="d0101-231">"WP"</span></span>                 | <span data-ttu-id="d0101-232">SDDL \_ 寫入 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="d0101-232">SDDL\_WRITE\_PROPERTY</span></span> | <span data-ttu-id="d0101-233">ADS \_ 正確的 \_ DS \_ 寫入 \_</span><span class="sxs-lookup"><span data-stu-id="d0101-233">ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="d0101-234">CC</span><span class="sxs-lookup"><span data-stu-id="d0101-234">"CC"</span></span>                 | <span data-ttu-id="d0101-235">SDDL \_ 建立 \_ 子系</span><span class="sxs-lookup"><span data-stu-id="d0101-235">SDDL\_CREATE\_CHILD</span></span> | <span data-ttu-id="d0101-236">ADS \_ RIGHT \_ DS \_ 建立 \_ 子系</span><span class="sxs-lookup"><span data-stu-id="d0101-236">ADS\_RIGHT\_DS\_CREATE\_CHILD</span></span> |
| <span data-ttu-id="d0101-237">電源</span><span class="sxs-lookup"><span data-stu-id="d0101-237">"DC"</span></span>                 | <span data-ttu-id="d0101-238">SDDL \_ 刪除 \_ 子系</span><span class="sxs-lookup"><span data-stu-id="d0101-238">SDDL\_DELETE\_CHILD</span></span> | <span data-ttu-id="d0101-239">ADS \_ 正確的 \_ DS \_ 刪除 \_ 子系</span><span class="sxs-lookup"><span data-stu-id="d0101-239">ADS\_RIGHT\_DS\_DELETE\_CHILD</span></span> |
| <span data-ttu-id="d0101-240">小寫</span><span class="sxs-lookup"><span data-stu-id="d0101-240">"LC"</span></span>                 | <span data-ttu-id="d0101-241">SDDL \_ 清單 \_ 子系</span><span class="sxs-lookup"><span data-stu-id="d0101-241">SDDL\_LIST\_CHILDREN</span></span> | <span data-ttu-id="d0101-242">ADS \_ RIGHT \_ ACTRL \_ DS \_ 清單</span><span class="sxs-lookup"><span data-stu-id="d0101-242">ADS\_RIGHT\_ACTRL\_DS\_LIST</span></span> |
| <span data-ttu-id="d0101-243">接線</span><span class="sxs-lookup"><span data-stu-id="d0101-243">"SW"</span></span>                 | <span data-ttu-id="d0101-244">SDDL \_ 自我 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="d0101-244">SDDL\_SELF\_WRITE</span></span>    | <span data-ttu-id="d0101-245">ADS \_ 適合 \_ DS \_ 自助</span><span class="sxs-lookup"><span data-stu-id="d0101-245">ADS\_RIGHT\_DS\_SELF</span></span> |
| <span data-ttu-id="d0101-246">高低</span><span class="sxs-lookup"><span data-stu-id="d0101-246">"LO"</span></span>                  | <span data-ttu-id="d0101-247">SDDL \_ 清單 \_ 物件</span><span class="sxs-lookup"><span data-stu-id="d0101-247">SDDL\_LIST\_OBJECT</span></span> | <span data-ttu-id="d0101-248">ADS \_ 正確的 \_ DS \_ 清單 \_ 物件</span><span class="sxs-lookup"><span data-stu-id="d0101-248">ADS\_RIGHT\_DS\_LIST\_OBJECT</span></span> |
| <span data-ttu-id="d0101-249">診斷</span><span class="sxs-lookup"><span data-stu-id="d0101-249">"DT"</span></span>                 | <span data-ttu-id="d0101-250">SDDL \_ 刪除 \_ 樹狀目錄</span><span class="sxs-lookup"><span data-stu-id="d0101-250">SDDL\_DELETE\_TREE</span></span> | <span data-ttu-id="d0101-251">ADS \_ 正確的 \_ DS \_ 刪除 \_ 樹狀結構</span><span class="sxs-lookup"><span data-stu-id="d0101-251">ADS\_RIGHT\_DS\_DELETE\_TREE</span></span> |
| <span data-ttu-id="d0101-252">CR</span><span class="sxs-lookup"><span data-stu-id="d0101-252">"CR"</span></span>                  | <span data-ttu-id="d0101-253">SDDL \_ 控制項 \_ 存取</span><span class="sxs-lookup"><span data-stu-id="d0101-253">SDDL\_CONTROL\_ACCESS</span></span> | <span data-ttu-id="d0101-254">ADS \_ 正確的 \_ DS \_ 控制 \_ 存取</span><span class="sxs-lookup"><span data-stu-id="d0101-254">ADS\_RIGHT\_DS\_CONTROL\_ACCESS</span></span> |

### <a name="file-access-rights"></a><span data-ttu-id="d0101-255">檔案存取權限</span><span class="sxs-lookup"><span data-stu-id="d0101-255">File access rights</span></span>

| <span data-ttu-id="d0101-256">存取權限字串</span><span class="sxs-lookup"><span data-stu-id="d0101-256">Access rights string</span></span> | <span data-ttu-id="d0101-257">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="d0101-257">Constant in Sddl.h</span></span> | <span data-ttu-id="d0101-258">存取權限值</span><span class="sxs-lookup"><span data-stu-id="d0101-258">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="d0101-259">FA</span><span class="sxs-lookup"><span data-stu-id="d0101-259">"FA"</span></span>                 | <span data-ttu-id="d0101-260">SDDL \_ 檔案 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="d0101-260">SDDL\_FILE\_ALL</span></span>    | <span data-ttu-id="d0101-261">檔案 \_ 所有 \_ 存取</span><span class="sxs-lookup"><span data-stu-id="d0101-261">FILE\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="d0101-262">法國</span><span class="sxs-lookup"><span data-stu-id="d0101-262">"FR"</span></span>                 | <span data-ttu-id="d0101-263">SDDL \_ 檔案 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="d0101-263">SDDL\_FILE\_READ</span></span>   | <span data-ttu-id="d0101-264">檔案 \_ 一般 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="d0101-264">FILE\_GENERIC\_READ</span></span> |
| <span data-ttu-id="d0101-265">FW</span><span class="sxs-lookup"><span data-stu-id="d0101-265">"FW"</span></span>                 | <span data-ttu-id="d0101-266">SDDL \_ 檔案 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="d0101-266">SDDL\_FILE\_WRITE</span></span>  | <span data-ttu-id="d0101-267">檔案 \_ 一般 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="d0101-267">FILE\_GENERIC\_WRITE</span></span> |
| <span data-ttu-id="d0101-268">FX</span><span class="sxs-lookup"><span data-stu-id="d0101-268">"FX"</span></span>                 | <span data-ttu-id="d0101-269">SDDL \_ 檔案 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="d0101-269">SDDL\_FILE\_EXECUTE</span></span> | <span data-ttu-id="d0101-270">FILE \_ GENERIC \_ EXECUTE</span><span class="sxs-lookup"><span data-stu-id="d0101-270">FILE\_GENERIC\_EXECUTE</span></span> |


### <a name="registry-key-access-rights"></a><span data-ttu-id="d0101-271">登錄機碼存取權限</span><span class="sxs-lookup"><span data-stu-id="d0101-271">Registry key access rights</span></span>

| <span data-ttu-id="d0101-272">存取權限字串</span><span class="sxs-lookup"><span data-stu-id="d0101-272">Access rights string</span></span> | <span data-ttu-id="d0101-273">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="d0101-273">Constant in Sddl.h</span></span> | <span data-ttu-id="d0101-274">存取權限值</span><span class="sxs-lookup"><span data-stu-id="d0101-274">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="d0101-275">KA</span><span class="sxs-lookup"><span data-stu-id="d0101-275">"KA"</span></span>                 | <span data-ttu-id="d0101-276">SDDL \_ 金鑰 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="d0101-276">SDDL\_KEY\_ALL</span></span>     | <span data-ttu-id="d0101-277">金鑰 \_ 所有 \_ 存取權</span><span class="sxs-lookup"><span data-stu-id="d0101-277">KEY\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="d0101-278">南韓</span><span class="sxs-lookup"><span data-stu-id="d0101-278">"KR"</span></span>                 | <span data-ttu-id="d0101-279">SDDL \_ 金鑰 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="d0101-279">SDDL\_KEY\_READ</span></span>    | <span data-ttu-id="d0101-280">金鑰 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="d0101-280">KEY\_READ</span></span>          |
| <span data-ttu-id="d0101-281">知識</span><span class="sxs-lookup"><span data-stu-id="d0101-281">"KW"</span></span>                 | <span data-ttu-id="d0101-282">SDDL \_ 金鑰 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="d0101-282">SDDL\_KEY\_WRITE</span></span>   | <span data-ttu-id="d0101-283">金鑰 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="d0101-283">KEY\_WRITE</span></span>         |
| <span data-ttu-id="d0101-284">"KX"</span><span class="sxs-lookup"><span data-stu-id="d0101-284">"KX"</span></span>                 | <span data-ttu-id="d0101-285">SDDL \_ 金鑰 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="d0101-285">SDDL\_KEY\_EXECUTE</span></span> | <span data-ttu-id="d0101-286">金鑰 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="d0101-286">KEY\_EXECUTE</span></span>       |

### <a name="mandatory-label-rights"></a><span data-ttu-id="d0101-287">強制標籤許可權</span><span class="sxs-lookup"><span data-stu-id="d0101-287">Mandatory label rights</span></span>

| <span data-ttu-id="d0101-288">存取權限字串</span><span class="sxs-lookup"><span data-stu-id="d0101-288">Access rights string</span></span> | <span data-ttu-id="d0101-289">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="d0101-289">Constant in Sddl.h</span></span> | <span data-ttu-id="d0101-290">存取權限值</span><span class="sxs-lookup"><span data-stu-id="d0101-290">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="d0101-291">NR</span><span class="sxs-lookup"><span data-stu-id="d0101-291">"NR"</span></span>                 | <span data-ttu-id="d0101-292">SDDL \_ 沒有 \_ 讀取 \_</span><span class="sxs-lookup"><span data-stu-id="d0101-292">SDDL\_NO\_READ\_UP</span></span> | <span data-ttu-id="d0101-293">系統 \_ 強制 \_ 標籤 \_ 否 \_ 讀取 \_</span><span class="sxs-lookup"><span data-stu-id="d0101-293">SYSTEM\_MANDATORY\_LABEL\_NO\_READ\_UP</span></span> |
| <span data-ttu-id="d0101-294">NW</span><span class="sxs-lookup"><span data-stu-id="d0101-294">"NW"</span></span>                 | <span data-ttu-id="d0101-295">SDDL \_ 沒有 \_ 寫入 \_</span><span class="sxs-lookup"><span data-stu-id="d0101-295">SDDL\_NO\_WRITE\_UP</span></span> | <span data-ttu-id="d0101-296">系統 \_ 強制 \_ 標籤 \_ 沒有 \_ 寫入 \_</span><span class="sxs-lookup"><span data-stu-id="d0101-296">SYSTEM\_MANDATORY\_LABEL\_NO\_WRITE\_UP</span></span> |
| <span data-ttu-id="d0101-297">NX</span><span class="sxs-lookup"><span data-stu-id="d0101-297">"NX"</span></span>                 | <span data-ttu-id="d0101-298">SDDL \_ 沒有 \_ 執行 \_</span><span class="sxs-lookup"><span data-stu-id="d0101-298">SDDL\_NO\_EXECUTE\_UP</span></span> | <span data-ttu-id="d0101-299">系統 \_ 強制 \_ 標籤 \_ 不 \_ 執行 \_</span><span class="sxs-lookup"><span data-stu-id="d0101-299">SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP</span></span> |
</dd> <dt>

<span data-ttu-id="d0101-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**物件 \_ guid**</span><span class="sxs-lookup"><span data-stu-id="d0101-300"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="d0101-301">GUID 的字串標記法，指出物件特定 ACE 結構的 **ObjectType** 成員值，例如 [**存取 \_ 允許的 \_ 物件 \_ ace**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace)。</span><span class="sxs-lookup"><span data-stu-id="d0101-301">A string representation of a GUID that indicates the value of the **ObjectType** member of an object-specific ACE structure, such as [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span></span> <span data-ttu-id="d0101-302">GUID 字串會使用 [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) 函數所傳回的格式。</span><span class="sxs-lookup"><span data-stu-id="d0101-302">The GUID string uses the format returned by the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) function.</span></span>

<span data-ttu-id="d0101-303">下表列出一些常用的物件 Guid。</span><span class="sxs-lookup"><span data-stu-id="d0101-303">The following table lists some commonly used object GUIDs.</span></span>



| <span data-ttu-id="d0101-304">許可權和 GUID</span><span class="sxs-lookup"><span data-stu-id="d0101-304">Rights and GUID</span></span>                         | <span data-ttu-id="d0101-305">權限</span><span class="sxs-lookup"><span data-stu-id="d0101-305">Permission</span></span>      |
|-----------------------------------------|-----------------|
| <span data-ttu-id="d0101-306">CR; ab721a53-1e2f-11d0-9819-00aa0040529b</span><span class="sxs-lookup"><span data-stu-id="d0101-306">CR;ab721a53-1e2f-11d0-9819-00aa0040529b</span></span> | <span data-ttu-id="d0101-307">變更密碼</span><span class="sxs-lookup"><span data-stu-id="d0101-307">Change password</span></span> |
| <span data-ttu-id="d0101-308">CR; 00299570-246d-11d0-a768-00aa006e0529</span><span class="sxs-lookup"><span data-stu-id="d0101-308">CR;00299570-246d-11d0-a768-00aa006e0529</span></span> | <span data-ttu-id="d0101-309">重設密碼</span><span class="sxs-lookup"><span data-stu-id="d0101-309">Reset password</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d0101-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**繼承 \_ 物件 \_ guid**</span><span class="sxs-lookup"><span data-stu-id="d0101-310"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**inherit\_object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="d0101-311">GUID 的字串表示，指出物件特定 ACE 結構的 **InheritedObjectType** 成員值。</span><span class="sxs-lookup"><span data-stu-id="d0101-311">A string representation of a GUID that indicates the value of the **InheritedObjectType** member of an object-specific ACE structure.</span></span> <span data-ttu-id="d0101-312">GUID 字串使用 [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) 格式。</span><span class="sxs-lookup"><span data-stu-id="d0101-312">The GUID string uses the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) format.</span></span>

</dd> <dt>

<span data-ttu-id="d0101-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**帳戶 \_ sid**</span><span class="sxs-lookup"><span data-stu-id="d0101-313"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**account\_sid**</span></span>
</dt> <dd>

<span data-ttu-id="d0101-314">識別 ACE[信任者](trustees.md)的[SID 字串](sid-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="d0101-314">[SID string](sid-strings.md) that identifies the [trustee](trustees.md) of the ACE.</span></span>

</dd> <dt>

<span data-ttu-id="d0101-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**資源 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="d0101-315"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**resource\_attribute**</span></span>
</dt> <dd>

<span data-ttu-id="d0101-316">\[選擇性 \] ：資源 \_ 屬性僅適用于資源 ace，而且是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="d0101-316">\[OPTIONAL\] The resource\_attribute is only for resource ACEs and is optional.</span></span> <span data-ttu-id="d0101-317">指出資料類型的字串。</span><span class="sxs-lookup"><span data-stu-id="d0101-317">A string that indicates the data type.</span></span> <span data-ttu-id="d0101-318">資源屬性 ace 資料類型可以是在 Sddl 中定義的下列其中一種資料類型。</span><span class="sxs-lookup"><span data-stu-id="d0101-318">The resource attribute ace data type can be one of the following data types defined in Sddl.h.</span></span>

<span data-ttu-id="d0101-319">\#在資源屬性中，"" 符號與 "0" 同義。</span><span class="sxs-lookup"><span data-stu-id="d0101-319">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="d0101-320">例如，D:AI (XA; OICI; FA;;;WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \#) ) 相當於並解釋為 D:AI (XA; OICI; FA;;;WD; (OctetStringType = = \# 01020300) ) 。</span><span class="sxs-lookup"><span data-stu-id="d0101-320">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

<span data-ttu-id="d0101-321">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 Windows Server 2003：** 無法使用資源屬性。</span><span class="sxs-lookup"><span data-stu-id="d0101-321">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Resource attributes are not available.</span></span>



| <span data-ttu-id="d0101-322">資源屬性 ace 資料類型字串</span><span class="sxs-lookup"><span data-stu-id="d0101-322">Resource attribute ace data type string</span></span> | <span data-ttu-id="d0101-323">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="d0101-323">Constant in Sddl.h</span></span> | <span data-ttu-id="d0101-324">資料類型</span><span class="sxs-lookup"><span data-stu-id="d0101-324">Data type</span></span>        |
|-----------------------------------------|--------------------|------------------|
| <span data-ttu-id="d0101-325">TI</span><span class="sxs-lookup"><span data-stu-id="d0101-325">"TI"</span></span>                                    | <span data-ttu-id="d0101-326">SDDL \_ INT</span><span class="sxs-lookup"><span data-stu-id="d0101-326">SDDL\_INT</span></span>          | <span data-ttu-id="d0101-327">帶正負號的整數</span><span class="sxs-lookup"><span data-stu-id="d0101-327">Signed integer</span></span>   |
| <span data-ttu-id="d0101-328">TU</span><span class="sxs-lookup"><span data-stu-id="d0101-328">"TU"</span></span>                                    | <span data-ttu-id="d0101-329">SDDL \_ UINT</span><span class="sxs-lookup"><span data-stu-id="d0101-329">SDDL\_UINT</span></span>         | <span data-ttu-id="d0101-330">不帶正負號的整數</span><span class="sxs-lookup"><span data-stu-id="d0101-330">Unsigned integer</span></span> |
| <span data-ttu-id="d0101-331">有毒</span><span class="sxs-lookup"><span data-stu-id="d0101-331">"TS"</span></span>                                    | <span data-ttu-id="d0101-332">SDDL \_ WSTRING</span><span class="sxs-lookup"><span data-stu-id="d0101-332">SDDL\_WSTRING</span></span>      | <span data-ttu-id="d0101-333">寬字元串</span><span class="sxs-lookup"><span data-stu-id="d0101-333">Wide string</span></span>      |
| <span data-ttu-id="d0101-334">T</span><span class="sxs-lookup"><span data-stu-id="d0101-334">"TD"</span></span>                                    | <span data-ttu-id="d0101-335">SDDL \_ SID</span><span class="sxs-lookup"><span data-stu-id="d0101-335">SDDL\_SID</span></span>          | <span data-ttu-id="d0101-336">SID</span><span class="sxs-lookup"><span data-stu-id="d0101-336">SID</span></span>              |
| <span data-ttu-id="d0101-337">TX</span><span class="sxs-lookup"><span data-stu-id="d0101-337">"TX"</span></span>                                    | <span data-ttu-id="d0101-338">SDDL \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="d0101-338">SDDL\_BLOB</span></span>         | <span data-ttu-id="d0101-339">八位字串</span><span class="sxs-lookup"><span data-stu-id="d0101-339">Octet string</span></span>     |
| <span data-ttu-id="d0101-340">TB</span><span class="sxs-lookup"><span data-stu-id="d0101-340">"TB"</span></span>                                    | <span data-ttu-id="d0101-341">SDDL \_ 布林值</span><span class="sxs-lookup"><span data-stu-id="d0101-341">SDDL\_BOOLEAN</span></span>      | <span data-ttu-id="d0101-342">Boolean</span><span class="sxs-lookup"><span data-stu-id="d0101-342">Boolean</span></span>          |



 

</dd> </dl>

<span data-ttu-id="d0101-343">下列範例顯示存取允許之 ACE 的 ACE 字串。</span><span class="sxs-lookup"><span data-stu-id="d0101-343">The following example shows an ACE string for an access-allowed ACE.</span></span> <span data-ttu-id="d0101-344">它不是物件特定的 ACE，因此它在 **物件 \_ guid** 中沒有任何資訊，而且會 **繼承 \_ 物件 \_ guid** 欄位。</span><span class="sxs-lookup"><span data-stu-id="d0101-344">It is not an object-specific ACE, so it has no information in the **object\_guid** and **inherit\_object\_guid** fields.</span></span> <span data-ttu-id="d0101-345">**Ace \_ 旗標** 欄位也是空的，這表示沒有設定任何 ace 旗標。</span><span class="sxs-lookup"><span data-stu-id="d0101-345">The **ace\_flags** field is also empty, which indicates that none of the ACE flags are set.</span></span>


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



<span data-ttu-id="d0101-346">以上顯示的 ACE 字串會描述下列 ACE 資訊。</span><span class="sxs-lookup"><span data-stu-id="d0101-346">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



<span data-ttu-id="d0101-347">下列範例顯示使用 Windows 的資源宣告分類的檔案，以及將密碼設定為高度商務衝擊的結構化查詢語言 (SQL)  (SQL) 。</span><span class="sxs-lookup"><span data-stu-id="d0101-347">The following example shows a file classified with resource claims for Windows and Structured Query Language (SQL) with Secrecy set to High Business Impact.</span></span>


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



<span data-ttu-id="d0101-348">以上顯示的 ACE 字串會描述下列 ACE 資訊。</span><span class="sxs-lookup"><span data-stu-id="d0101-348">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



<span data-ttu-id="d0101-349">如需詳細資訊，請參閱 [安全描述項字串格式](security-descriptor-string-format.md) 和 [SID 字串](sid-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="d0101-349">For more information, see [Security Descriptor String Format](security-descriptor-string-format.md) and [SID Strings](sid-strings.md).</span></span> <span data-ttu-id="d0101-350">針對條件式 Ace，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)。</span><span class="sxs-lookup"><span data-stu-id="d0101-350">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0101-351">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0101-351">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d0101-352">[\[DTYP \] ：安全描述項描述語言](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="d0101-352">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

