---
description: 說明在存取控制專案中使用的字串。
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: ACE 字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed8f9aad8696bd3d3c251170f2ff79ea493ce57
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644180"
---
# <a name="ace-strings"></a><span data-ttu-id="23a3c-103">ACE 字串</span><span class="sxs-lookup"><span data-stu-id="23a3c-103">ACE Strings</span></span>

<span data-ttu-id="23a3c-104">[安全描述項定義語言](security-descriptor-definition-language.md) (SDDL) 在 [*安全描述項*](/windows/desktop/SecGloss/s-gly)字串的 DACL 和 SACL 元件中使用 ACE 字串。</span><span class="sxs-lookup"><span data-stu-id="23a3c-104">The [security descriptor definition language](security-descriptor-definition-language.md) (SDDL) uses ACE strings in the DACL and SACL components of a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string.</span></span>

<span data-ttu-id="23a3c-105">如 [安全描述項字串格式](security-descriptor-string-format.md) 範例所示，安全描述項字串中的每個 ACE 都會以括弧括住。</span><span class="sxs-lookup"><span data-stu-id="23a3c-105">As shown in the [Security Descriptor String Format](security-descriptor-string-format.md) examples, each ACE in a security descriptor string is enclosed in parentheses.</span></span> <span data-ttu-id="23a3c-106">ACE 的欄位會以下列順序排列，並以分號分隔 (; ) 。</span><span class="sxs-lookup"><span data-stu-id="23a3c-106">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="23a3c-107">條件式 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) 的格式與其他 ace 類型 (ace) 不同。</span><span class="sxs-lookup"><span data-stu-id="23a3c-107">There is a different format for conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) than other ACE types.</span></span> <span data-ttu-id="23a3c-108">針對條件式 Ace，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)。</span><span class="sxs-lookup"><span data-stu-id="23a3c-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a><span data-ttu-id="23a3c-109">欄位</span><span class="sxs-lookup"><span data-stu-id="23a3c-109">Fields</span></span>

<dl> <dt>

<span data-ttu-id="23a3c-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**ace \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="23a3c-110"><span id="ace_type"></span><span id="ACE_TYPE"></span>**ace\_type**</span></span>
</dt> <dd>

<span data-ttu-id="23a3c-111">字串，指出 [**ACE \_ 標頭**](/windows/desktop/api/Winnt/ns-winnt-ace_header)結構之 **AceType** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="23a3c-111">A string that indicates the value of the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="23a3c-112">ACE 類型字串可以是在 Sddl 中定義的下列其中一個字串。</span><span class="sxs-lookup"><span data-stu-id="23a3c-112">The ACE type string can be one of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="23a3c-113">ACE 類型字串</span><span class="sxs-lookup"><span data-stu-id="23a3c-113">ACE type string</span></span> | <span data-ttu-id="23a3c-114">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="23a3c-114">Constant in Sddl.h</span></span>                      | <span data-ttu-id="23a3c-115">AceType 值</span><span class="sxs-lookup"><span data-stu-id="23a3c-115">AceType value</span></span>                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23a3c-116">"A"</span><span class="sxs-lookup"><span data-stu-id="23a3c-116">"A"</span></span>             | <span data-ttu-id="23a3c-117">\_允許 SDDL 存取 \_</span><span class="sxs-lookup"><span data-stu-id="23a3c-117">SDDL\_ACCESS\_ALLOWED</span></span>                   | <span data-ttu-id="23a3c-118">存取 \_ 允許的 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="23a3c-118">ACCESS\_ALLOWED\_ACE\_TYPE</span></span>                                                                                                                                         |
| <span data-ttu-id="23a3c-119">"D"</span><span class="sxs-lookup"><span data-stu-id="23a3c-119">"D"</span></span>             | <span data-ttu-id="23a3c-120">SDDL \_ \_ 拒絕存取</span><span class="sxs-lookup"><span data-stu-id="23a3c-120">SDDL\_ACCESS\_DENIED</span></span>                    | <span data-ttu-id="23a3c-121">\_拒絕存取 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="23a3c-121">ACCESS\_DENIED\_ACE\_TYPE</span></span>                                                                                                                                          |
| <span data-ttu-id="23a3c-122">OA</span><span class="sxs-lookup"><span data-stu-id="23a3c-122">"OA"</span></span>            | <span data-ttu-id="23a3c-123">\_允許 SDDL 物件 \_ 存取 \_</span><span class="sxs-lookup"><span data-stu-id="23a3c-123">SDDL\_OBJECT\_ACCESS\_ALLOWED</span></span>           | <span data-ttu-id="23a3c-124">存取 \_ 允許的 \_ 物件 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="23a3c-124">ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                 |
| <span data-ttu-id="23a3c-125">OD</span><span class="sxs-lookup"><span data-stu-id="23a3c-125">"OD"</span></span>            | <span data-ttu-id="23a3c-126">SDDL \_ 物件 \_ \_ 拒絕存取</span><span class="sxs-lookup"><span data-stu-id="23a3c-126">SDDL\_OBJECT\_ACCESS\_DENIED</span></span>            | <span data-ttu-id="23a3c-127">\_拒絕存取 \_ 物件 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="23a3c-127">ACCESS\_DENIED\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                  |
| <span data-ttu-id="23a3c-128">澳大利亞</span><span class="sxs-lookup"><span data-stu-id="23a3c-128">"AU"</span></span>            | <span data-ttu-id="23a3c-129">SDDL \_ 審核</span><span class="sxs-lookup"><span data-stu-id="23a3c-129">SDDL\_AUDIT</span></span>                             | <span data-ttu-id="23a3c-130">系統 \_ 審核 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="23a3c-130">SYSTEM\_AUDIT\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="23a3c-131">"AL"</span><span class="sxs-lookup"><span data-stu-id="23a3c-131">"AL"</span></span>            | <span data-ttu-id="23a3c-132">SDDL \_ 警示</span><span class="sxs-lookup"><span data-stu-id="23a3c-132">SDDL\_ALARM</span></span>                             | <span data-ttu-id="23a3c-133">系統 \_ 警示 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="23a3c-133">SYSTEM\_ALARM\_ACE\_TYPE</span></span>                                                                                                                                           |
| <span data-ttu-id="23a3c-134">/OU</span><span class="sxs-lookup"><span data-stu-id="23a3c-134">"OU"</span></span>            | <span data-ttu-id="23a3c-135">SDDL \_ 物件 \_ AUDIT</span><span class="sxs-lookup"><span data-stu-id="23a3c-135">SDDL\_OBJECT\_AUDIT</span></span>                     | <span data-ttu-id="23a3c-136">SYSTEM \_ AUDIT \_ OBJECT \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="23a3c-136">SYSTEM\_AUDIT\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="23a3c-137">歐</span><span class="sxs-lookup"><span data-stu-id="23a3c-137">"OL"</span></span>            | <span data-ttu-id="23a3c-138">SDDL \_ 物件 \_ 警示</span><span class="sxs-lookup"><span data-stu-id="23a3c-138">SDDL\_OBJECT\_ALARM</span></span>                     | <span data-ttu-id="23a3c-139">系統 \_ 警報 \_ 物件 \_ ACE \_ 類型</span><span class="sxs-lookup"><span data-stu-id="23a3c-139">SYSTEM\_ALARM\_OBJECT\_ACE\_TYPE</span></span>                                                                                                                                   |
| <span data-ttu-id="23a3c-140">ML</span><span class="sxs-lookup"><span data-stu-id="23a3c-140">"ML"</span></span>            | <span data-ttu-id="23a3c-141">SDDL \_ 強制 \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="23a3c-141">SDDL\_MANDATORY\_LABEL</span></span>                  | <span data-ttu-id="23a3c-142">系統 \_ 強制 \_ 標籤 \_ ACE \_ 類型 **Windows Server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-142">SYSTEM\_MANDATORY\_LABEL\_ACE\_TYPE **Windows Server 2003:** Not available.</span></span>                                                                                        |
| <span data-ttu-id="23a3c-143">XA</span><span class="sxs-lookup"><span data-stu-id="23a3c-143">"XA"</span></span>            | <span data-ttu-id="23a3c-144">\_允許 SDDL 回呼 \_ 存取 \_</span><span class="sxs-lookup"><span data-stu-id="23a3c-144">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span>         | <span data-ttu-id="23a3c-145">存取 \_ 允許 \_ \_ 的回呼 ACE \_ 類型 **Windows Server 2008、windows Vista 和 windows server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-145">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span>                                                |
| <span data-ttu-id="23a3c-146">XD</span><span class="sxs-lookup"><span data-stu-id="23a3c-146">"XD"</span></span>            | <span data-ttu-id="23a3c-147">SDDL \_ 回呼 \_ \_ 拒絕存取</span><span class="sxs-lookup"><span data-stu-id="23a3c-147">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span>          | <span data-ttu-id="23a3c-148">\_拒絕存取 \_ 回呼 \_ ACE \_ 類型 **Windows Server 2008、Windows Vista 和 windows server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-148">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE **Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span>                                                 |
| <span data-ttu-id="23a3c-149">RA</span><span class="sxs-lookup"><span data-stu-id="23a3c-149">"RA"</span></span>            | <span data-ttu-id="23a3c-150">SDDL \_ 資源 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="23a3c-150">SDDL\_RESOURCE\_ATTRIBUTE</span></span>               | <span data-ttu-id="23a3c-151">系統 \_ 資源 \_ 屬性 \_ ACE \_ 類型 **： Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 windows Server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-151">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/> |
| <span data-ttu-id="23a3c-152">SP-1</span><span class="sxs-lookup"><span data-stu-id="23a3c-152">"SP"</span></span>            | <span data-ttu-id="23a3c-153">SDDL \_ 範圍 \_ 原則 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="23a3c-153">SDDL\_SCOPED\_POLICY\_ID</span></span>                | <span data-ttu-id="23a3c-154">系統 \_ 範圍 \_ 原則 \_ 識別碼 \_ ACE \_ 類型 **： Windows server 2008 R2、windows 7、windows Server 2008、windows Vista 和 windows Server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-154">SYSTEM\_SCOPED\_POLICY\_ID\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>  |
| <span data-ttu-id="23a3c-155">XU</span><span class="sxs-lookup"><span data-stu-id="23a3c-155">"XU"</span></span>            | <span data-ttu-id="23a3c-156">SDDL \_ 回呼 \_ 審核</span><span class="sxs-lookup"><span data-stu-id="23a3c-156">SDDL\_CALLBACK\_AUDIT</span></span>                   | <span data-ttu-id="23a3c-157">系統 \_ AUDIT \_ 回呼 \_ ACE \_ 類型 **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 windows Server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-157">SYSTEM\_AUDIT\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>     |
| <span data-ttu-id="23a3c-158">ZA</span><span class="sxs-lookup"><span data-stu-id="23a3c-158">"ZA"</span></span>            | <span data-ttu-id="23a3c-159">\_允許 SDDL 回呼 \_ 物件 \_ 存取 \_</span><span class="sxs-lookup"><span data-stu-id="23a3c-159">SDDL\_CALLBACK\_OBJECT\_ACCESS\_ALLOWED</span></span> | <span data-ttu-id="23a3c-160">存取 \_ 允許 \_ \_ 的回呼 ACE \_ 類型 **Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 windows Server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-160">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span><br/>   |
| <span data-ttu-id="23a3c-161">TL</span><span class="sxs-lookup"><span data-stu-id="23a3c-161">"TL"</span></span>            | <span data-ttu-id="23a3c-162">SDDL \_ 進程 \_ 信任 \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="23a3c-162">SDDL\_PROCESS\_TRUST\_LABEL</span></span>             | <span data-ttu-id="23a3c-163">系統 \_ 進程 \_ 信任 \_ 標籤 \_ ACE \_ 類型 **Windows Server 2012、Windows 8、windows server 2008 R2、windows 7、windows Server 2008、windows Vista 和 Windows server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-163">SYSTEM\_PROCESS\_TRUST\_LABEL\_ACE\_TYPE **Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span> |
| <span data-ttu-id="23a3c-164">奧蘭多</span><span class="sxs-lookup"><span data-stu-id="23a3c-164">"FL"</span></span>            | <span data-ttu-id="23a3c-165">SDDL \_ 存取 \_ 篩選</span><span class="sxs-lookup"><span data-stu-id="23a3c-165">SDDL\_ACCESS\_FILTER</span></span>                    | <span data-ttu-id="23a3c-166">系統 \_ 存取 \_ 篩選 \_ ACE \_ 類型 **Windows Server 2016、Windows 10 版1607、Windows 10 1511 版、Windows 10 版本1507、windows server 2012 R2、Windows 8.1、windows Server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008、windows Vista 和 windows server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-166">SYSTEM\_ACCESS\_FILTER\_ACE\_TYPE **Windows Server 2016, Windows 10 Version 1607, Windows 10 Version 1511, Windows 10 Version 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span> |
 

> [!Note]  
> <span data-ttu-id="23a3c-167">如果 **ace \_ 類型** 為 access \_ 允許 \_ \_ 的物件 ace \_ 類型， **而且物件 \_ guid** 或 **繼承 \_ 物件 \_ guid** 都未指定 [**guid**](/windows/win32/api/guiddef/ns-guiddef-guid) ，則 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 會將 **ace \_ 類型** 轉換成存取允許的 \_ \_ ace \_ 類型。</span><span class="sxs-lookup"><span data-stu-id="23a3c-167">If **ace\_type** is ACCESS\_ALLOWED\_OBJECT\_ACE\_TYPE and neither **object\_guid** nor **inherit\_object\_guid** has a [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) specified, then [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converts **ace\_type** to ACCESS\_ALLOWED\_ACE\_TYPE.</span></span>

 

</dd> <dt>

<span data-ttu-id="23a3c-168"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ace \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="23a3c-168"><span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ace\_flags**</span></span>
</dt> <dd>

<span data-ttu-id="23a3c-169">字串，指出 [**ACE \_ 標頭**](/windows/desktop/api/Winnt/ns-winnt-ace_header)結構之 **AceFlags** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="23a3c-169">A string that indicates the value of the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="23a3c-170">ACE 旗標字串可以是以 Sddl. h 定義的下列字串的串連。</span><span class="sxs-lookup"><span data-stu-id="23a3c-170">The ACE flags string can be a concatenation of the following strings defined in Sddl.h.</span></span>



| <span data-ttu-id="23a3c-171">ACE 旗標字串</span><span class="sxs-lookup"><span data-stu-id="23a3c-171">ACE flags string</span></span> | <span data-ttu-id="23a3c-172">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="23a3c-172">Constant in Sddl.h</span></span>       | <span data-ttu-id="23a3c-173">AceFlag 值</span><span class="sxs-lookup"><span data-stu-id="23a3c-173">AceFlag value</span></span>                 |
|------------------|--------------------------|-------------------------------|
| <span data-ttu-id="23a3c-174">CI</span><span class="sxs-lookup"><span data-stu-id="23a3c-174">"CI"</span></span>             | <span data-ttu-id="23a3c-175">SDDL \_ 容器 \_ 繼承</span><span class="sxs-lookup"><span data-stu-id="23a3c-175">SDDL\_CONTAINER\_INHERIT</span></span> | <span data-ttu-id="23a3c-176">容器 \_ 繼承 \_ ACE</span><span class="sxs-lookup"><span data-stu-id="23a3c-176">CONTAINER\_INHERIT\_ACE</span></span>       |
| <span data-ttu-id="23a3c-177">OI</span><span class="sxs-lookup"><span data-stu-id="23a3c-177">"OI"</span></span>             | <span data-ttu-id="23a3c-178">SDDL \_ 物件 \_ 繼承</span><span class="sxs-lookup"><span data-stu-id="23a3c-178">SDDL\_OBJECT\_INHERIT</span></span>    | <span data-ttu-id="23a3c-179">OBJECT \_ INHERIT \_ ACE</span><span class="sxs-lookup"><span data-stu-id="23a3c-179">OBJECT\_INHERIT\_ACE</span></span>          |
| <span data-ttu-id="23a3c-180">NP-IN</span><span class="sxs-lookup"><span data-stu-id="23a3c-180">"NP"</span></span>             | <span data-ttu-id="23a3c-181">SDDL \_ 沒有 \_ 傳播</span><span class="sxs-lookup"><span data-stu-id="23a3c-181">SDDL\_NO\_PROPAGATE</span></span>      | <span data-ttu-id="23a3c-182">沒有 \_ 傳播 \_ 繼承 \_ ACE</span><span class="sxs-lookup"><span data-stu-id="23a3c-182">NO\_PROPAGATE\_INHERIT\_ACE</span></span>   |
| <span data-ttu-id="23a3c-183">IO</span><span class="sxs-lookup"><span data-stu-id="23a3c-183">"IO"</span></span>             | <span data-ttu-id="23a3c-184">SDDL \_ \_ 只繼承</span><span class="sxs-lookup"><span data-stu-id="23a3c-184">SDDL\_INHERIT\_ONLY</span></span>      | <span data-ttu-id="23a3c-185">\_只繼承 \_ ACE</span><span class="sxs-lookup"><span data-stu-id="23a3c-185">INHERIT\_ONLY\_ACE</span></span>            |
| <span data-ttu-id="23a3c-186">「識別碼」</span><span class="sxs-lookup"><span data-stu-id="23a3c-186">"ID"</span></span>             | <span data-ttu-id="23a3c-187">SDDL \_ 繼承</span><span class="sxs-lookup"><span data-stu-id="23a3c-187">SDDL\_INHERITED</span></span>          | <span data-ttu-id="23a3c-188">繼承的 \_ ACE</span><span class="sxs-lookup"><span data-stu-id="23a3c-188">INHERITED\_ACE</span></span>                |
| <span data-ttu-id="23a3c-189">SA</span><span class="sxs-lookup"><span data-stu-id="23a3c-189">"SA"</span></span>             | <span data-ttu-id="23a3c-190">SDDL \_ 審核 \_ 成功</span><span class="sxs-lookup"><span data-stu-id="23a3c-190">SDDL\_AUDIT\_SUCCESS</span></span>     | <span data-ttu-id="23a3c-191">成功的 \_ 存取 \_ ACE \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="23a3c-191">SUCCESSFUL\_ACCESS\_ACE\_FLAG</span></span> |
| <span data-ttu-id="23a3c-192">FA</span><span class="sxs-lookup"><span data-stu-id="23a3c-192">"FA"</span></span>             | <span data-ttu-id="23a3c-193">SDDL \_ 審核 \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="23a3c-193">SDDL\_AUDIT\_FAILURE</span></span>     | <span data-ttu-id="23a3c-194">\_存取 \_ ACE \_ 旗標失敗</span><span class="sxs-lookup"><span data-stu-id="23a3c-194">FAILED\_ACCESS\_ACE\_FLAG</span></span>     |
| <span data-ttu-id="23a3c-195">TP</span><span class="sxs-lookup"><span data-stu-id="23a3c-195">"TP"</span></span>             | <span data-ttu-id="23a3c-196">SDDL \_ 信任 \_ 受保護的 \_ 篩選</span><span class="sxs-lookup"><span data-stu-id="23a3c-196">SDDL\_TRUST\_PROTECTED\_FILTER</span></span> | <span data-ttu-id="23a3c-197">信任 \_ PROTECTED \_ FILTER \_ ACE \_ 旗標 **Windows Server 2016、Windows 10 1607 版、Windows 10 1511 版、Windows 10 1507 版、windows server 2012 R2、Windows 8.1、windows Server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008、windows Vista 和 windows server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-197">TRUST\_PROTECTED\_FILTER\_ACE\_FLAG **Windows Server 2016, Windows 10 Version 1607, Windows 10 Version 1511, Windows 10 Version 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span> |
| <span data-ttu-id="23a3c-198">CR</span><span class="sxs-lookup"><span data-stu-id="23a3c-198">"CR"</span></span>             | <span data-ttu-id="23a3c-199">SDDL \_ 重大</span><span class="sxs-lookup"><span data-stu-id="23a3c-199">SDDL\_CRITICAL</span></span>           | <span data-ttu-id="23a3c-200">重大 \_ ACE \_ 旗標 **Windows Server 1803 版、Windows 10 版1803、Windows Server 1709 版、Windows 10 1709 版、Windows 10 版本1703、Windows Server 2016、Windows 10 版本1607、Windows 10 版本1511、Windows 10 版本1507、windows server 2012、Windows 8.1、windows server 2012、Windows 8、Windows server 2008 r2、Windows 7、windows Server 2008、Windows Vista 和 windows server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-200">CRITICAL\_ACE\_FLAG **Windows Server Version 1803, Windows 10 Version 1803, Windows Server Version 1709, Windows 10 Version 1709, Windows 10 Version 1703, Windows Server 2016, Windows 10 Version 1607, Windows 10 Version 1511, Windows 10 Version 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span> |
 

</dd> <dt>

<span data-ttu-id="23a3c-201"><span id="rights"></span><span id="RIGHTS"></span>**權利**</span><span class="sxs-lookup"><span data-stu-id="23a3c-201"><span id="rights"></span><span id="RIGHTS"></span>**rights**</span></span>
</dt> <dd>

<span data-ttu-id="23a3c-202">表示由 ACE 所控制之 [存取權限](access-rights-and-access-masks.md) 的字串。</span><span class="sxs-lookup"><span data-stu-id="23a3c-202">A string that indicates the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span> <span data-ttu-id="23a3c-203">這個字串可以是存取權限的十六進位字串標記法（例如 "0x7800003F"），也可以是下列字串的串連。</span><span class="sxs-lookup"><span data-stu-id="23a3c-203">This string can be a hexadecimal string representation of the access rights, such as "0x7800003F", or it can be a concatenation of the following strings.</span></span>



### <a name="generic-access-rights"></a><span data-ttu-id="23a3c-204">一般存取權限</span><span class="sxs-lookup"><span data-stu-id="23a3c-204">Generic access rights</span></span>

| <span data-ttu-id="23a3c-205">存取權限字串</span><span class="sxs-lookup"><span data-stu-id="23a3c-205">Access rights string</span></span> | <span data-ttu-id="23a3c-206">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="23a3c-206">Constant in Sddl.h</span></span> | <span data-ttu-id="23a3c-207">存取權限值</span><span class="sxs-lookup"><span data-stu-id="23a3c-207">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="23a3c-208">正式</span><span class="sxs-lookup"><span data-stu-id="23a3c-208">"GA"</span></span>                 | <span data-ttu-id="23a3c-209">SDDL \_ 泛型 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="23a3c-209">SDDL\_GENERIC\_ALL</span></span> | <span data-ttu-id="23a3c-210">一般 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="23a3c-210">GENERIC\_ALL</span></span>       |
| <span data-ttu-id="23a3c-211">GR</span><span class="sxs-lookup"><span data-stu-id="23a3c-211">"GR"</span></span>                 | <span data-ttu-id="23a3c-212">SDDL \_ 一般 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="23a3c-212">SDDL\_GENERIC\_READ</span></span> | <span data-ttu-id="23a3c-213">一般 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="23a3c-213">GENERIC\_READ</span></span>     |
| <span data-ttu-id="23a3c-214">GW</span><span class="sxs-lookup"><span data-stu-id="23a3c-214">"GW"</span></span>                 | <span data-ttu-id="23a3c-215">SDDL \_ 一般 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="23a3c-215">SDDL\_GENERIC\_WRITE</span></span> | <span data-ttu-id="23a3c-216">一般 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="23a3c-216">GENERIC\_WRITE</span></span> |
| <span data-ttu-id="23a3c-217">GX</span><span class="sxs-lookup"><span data-stu-id="23a3c-217">"GX"</span></span>                 | <span data-ttu-id="23a3c-218">SDDL \_ 泛型 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="23a3c-218">SDDL\_GENERIC\_EXECUTE</span></span> | <span data-ttu-id="23a3c-219">一般 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="23a3c-219">GENERIC\_EXECUTE</span></span> |


### <a name="standard-access-rights"></a><span data-ttu-id="23a3c-220">標準存取權限</span><span class="sxs-lookup"><span data-stu-id="23a3c-220">Standard access rights</span></span>

| <span data-ttu-id="23a3c-221">存取權限字串</span><span class="sxs-lookup"><span data-stu-id="23a3c-221">Access rights string</span></span> | <span data-ttu-id="23a3c-222">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="23a3c-222">Constant in Sddl.h</span></span> | <span data-ttu-id="23a3c-223">存取權限值</span><span class="sxs-lookup"><span data-stu-id="23a3c-223">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="23a3c-224">RC</span><span class="sxs-lookup"><span data-stu-id="23a3c-224">"RC"</span></span>                 | <span data-ttu-id="23a3c-225">SDDL \_ 讀取 \_ 控制</span><span class="sxs-lookup"><span data-stu-id="23a3c-225">SDDL\_READ\_CONTROL</span></span> | <span data-ttu-id="23a3c-226">讀取 \_ 控制</span><span class="sxs-lookup"><span data-stu-id="23a3c-226">READ\_CONTROL</span></span>      |
| <span data-ttu-id="23a3c-227">SD</span><span class="sxs-lookup"><span data-stu-id="23a3c-227">"SD"</span></span>                 | <span data-ttu-id="23a3c-228">SDDL \_ 標準 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="23a3c-228">SDDL\_STANDARD\_DELETE</span></span> | <span data-ttu-id="23a3c-229">刪除</span><span class="sxs-lookup"><span data-stu-id="23a3c-229">DELETE</span></span>          |
| <span data-ttu-id="23a3c-230">WD</span><span class="sxs-lookup"><span data-stu-id="23a3c-230">"WD"</span></span>                 | <span data-ttu-id="23a3c-231">SDDL \_ 寫入 \_ DAC</span><span class="sxs-lookup"><span data-stu-id="23a3c-231">SDDL\_WRITE\_DAC</span></span> | <span data-ttu-id="23a3c-232">寫入 \_ DAC</span><span class="sxs-lookup"><span data-stu-id="23a3c-232">WRITE\_DAC</span></span>            |
| <span data-ttu-id="23a3c-233">WO</span><span class="sxs-lookup"><span data-stu-id="23a3c-233">"WO"</span></span>                 | <span data-ttu-id="23a3c-234">SDDL \_ 寫入 \_ 擁有者</span><span class="sxs-lookup"><span data-stu-id="23a3c-234">SDDL\_WRITE\_OWNER</span></span> | <span data-ttu-id="23a3c-235">寫入 \_ 擁有者</span><span class="sxs-lookup"><span data-stu-id="23a3c-235">WRITE\_OWNER</span></span>        |

### <a name="directory-service-object-access-rights"></a><span data-ttu-id="23a3c-236">目錄服務物件存取權限</span><span class="sxs-lookup"><span data-stu-id="23a3c-236">Directory service object access rights</span></span>

| <span data-ttu-id="23a3c-237">存取權限字串</span><span class="sxs-lookup"><span data-stu-id="23a3c-237">Access rights string</span></span> | <span data-ttu-id="23a3c-238">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="23a3c-238">Constant in Sddl.h</span></span> | <span data-ttu-id="23a3c-239">存取權限值</span><span class="sxs-lookup"><span data-stu-id="23a3c-239">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="23a3c-240">開頭</span><span class="sxs-lookup"><span data-stu-id="23a3c-240">"RP"</span></span>                 | <span data-ttu-id="23a3c-241">SDDL \_ 讀取 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="23a3c-241">SDDL\_READ\_PROPERTY</span></span> | <span data-ttu-id="23a3c-242">ADS \_ 正確的 \_ DS \_ 讀取 \_</span><span class="sxs-lookup"><span data-stu-id="23a3c-242">ADS\_RIGHT\_DS\_READ\_PROP</span></span> |
| <span data-ttu-id="23a3c-243">WP</span><span class="sxs-lookup"><span data-stu-id="23a3c-243">"WP"</span></span>                 | <span data-ttu-id="23a3c-244">SDDL \_ 寫入 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="23a3c-244">SDDL\_WRITE\_PROPERTY</span></span> | <span data-ttu-id="23a3c-245">ADS \_ 正確的 \_ DS \_ 寫入 \_</span><span class="sxs-lookup"><span data-stu-id="23a3c-245">ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="23a3c-246">CC</span><span class="sxs-lookup"><span data-stu-id="23a3c-246">"CC"</span></span>                 | <span data-ttu-id="23a3c-247">SDDL \_ 建立 \_ 子系</span><span class="sxs-lookup"><span data-stu-id="23a3c-247">SDDL\_CREATE\_CHILD</span></span> | <span data-ttu-id="23a3c-248">ADS \_ RIGHT \_ DS \_ 建立 \_ 子系</span><span class="sxs-lookup"><span data-stu-id="23a3c-248">ADS\_RIGHT\_DS\_CREATE\_CHILD</span></span> |
| <span data-ttu-id="23a3c-249">電源</span><span class="sxs-lookup"><span data-stu-id="23a3c-249">"DC"</span></span>                 | <span data-ttu-id="23a3c-250">SDDL \_ 刪除 \_ 子系</span><span class="sxs-lookup"><span data-stu-id="23a3c-250">SDDL\_DELETE\_CHILD</span></span> | <span data-ttu-id="23a3c-251">ADS \_ 正確的 \_ DS \_ 刪除 \_ 子系</span><span class="sxs-lookup"><span data-stu-id="23a3c-251">ADS\_RIGHT\_DS\_DELETE\_CHILD</span></span> |
| <span data-ttu-id="23a3c-252">小寫</span><span class="sxs-lookup"><span data-stu-id="23a3c-252">"LC"</span></span>                 | <span data-ttu-id="23a3c-253">SDDL \_ 清單 \_ 子系</span><span class="sxs-lookup"><span data-stu-id="23a3c-253">SDDL\_LIST\_CHILDREN</span></span> | <span data-ttu-id="23a3c-254">ADS \_ RIGHT \_ ACTRL \_ DS \_ 清單</span><span class="sxs-lookup"><span data-stu-id="23a3c-254">ADS\_RIGHT\_ACTRL\_DS\_LIST</span></span> |
| <span data-ttu-id="23a3c-255">接線</span><span class="sxs-lookup"><span data-stu-id="23a3c-255">"SW"</span></span>                 | <span data-ttu-id="23a3c-256">SDDL \_ 自我 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="23a3c-256">SDDL\_SELF\_WRITE</span></span>    | <span data-ttu-id="23a3c-257">ADS \_ 適合 \_ DS \_ 自助</span><span class="sxs-lookup"><span data-stu-id="23a3c-257">ADS\_RIGHT\_DS\_SELF</span></span> |
| <span data-ttu-id="23a3c-258">高低</span><span class="sxs-lookup"><span data-stu-id="23a3c-258">"LO"</span></span>                  | <span data-ttu-id="23a3c-259">SDDL \_ 清單 \_ 物件</span><span class="sxs-lookup"><span data-stu-id="23a3c-259">SDDL\_LIST\_OBJECT</span></span> | <span data-ttu-id="23a3c-260">ADS \_ 正確的 \_ DS \_ 清單 \_ 物件</span><span class="sxs-lookup"><span data-stu-id="23a3c-260">ADS\_RIGHT\_DS\_LIST\_OBJECT</span></span> |
| <span data-ttu-id="23a3c-261">診斷</span><span class="sxs-lookup"><span data-stu-id="23a3c-261">"DT"</span></span>                 | <span data-ttu-id="23a3c-262">SDDL \_ 刪除 \_ 樹狀目錄</span><span class="sxs-lookup"><span data-stu-id="23a3c-262">SDDL\_DELETE\_TREE</span></span> | <span data-ttu-id="23a3c-263">ADS \_ 正確的 \_ DS \_ 刪除 \_ 樹狀結構</span><span class="sxs-lookup"><span data-stu-id="23a3c-263">ADS\_RIGHT\_DS\_DELETE\_TREE</span></span> |
| <span data-ttu-id="23a3c-264">CR</span><span class="sxs-lookup"><span data-stu-id="23a3c-264">"CR"</span></span>                  | <span data-ttu-id="23a3c-265">SDDL \_ 控制項 \_ 存取</span><span class="sxs-lookup"><span data-stu-id="23a3c-265">SDDL\_CONTROL\_ACCESS</span></span> | <span data-ttu-id="23a3c-266">ADS \_ 正確的 \_ DS \_ 控制 \_ 存取</span><span class="sxs-lookup"><span data-stu-id="23a3c-266">ADS\_RIGHT\_DS\_CONTROL\_ACCESS</span></span> |

### <a name="file-access-rights"></a><span data-ttu-id="23a3c-267">檔案存取權限</span><span class="sxs-lookup"><span data-stu-id="23a3c-267">File access rights</span></span>

| <span data-ttu-id="23a3c-268">存取權限字串</span><span class="sxs-lookup"><span data-stu-id="23a3c-268">Access rights string</span></span> | <span data-ttu-id="23a3c-269">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="23a3c-269">Constant in Sddl.h</span></span> | <span data-ttu-id="23a3c-270">存取權限值</span><span class="sxs-lookup"><span data-stu-id="23a3c-270">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="23a3c-271">FA</span><span class="sxs-lookup"><span data-stu-id="23a3c-271">"FA"</span></span>                 | <span data-ttu-id="23a3c-272">SDDL \_ 檔案 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="23a3c-272">SDDL\_FILE\_ALL</span></span>    | <span data-ttu-id="23a3c-273">檔案 \_ 所有 \_ 存取</span><span class="sxs-lookup"><span data-stu-id="23a3c-273">FILE\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="23a3c-274">法國</span><span class="sxs-lookup"><span data-stu-id="23a3c-274">"FR"</span></span>                 | <span data-ttu-id="23a3c-275">SDDL \_ 檔案 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="23a3c-275">SDDL\_FILE\_READ</span></span>   | <span data-ttu-id="23a3c-276">檔案 \_ 一般 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="23a3c-276">FILE\_GENERIC\_READ</span></span> |
| <span data-ttu-id="23a3c-277">FW</span><span class="sxs-lookup"><span data-stu-id="23a3c-277">"FW"</span></span>                 | <span data-ttu-id="23a3c-278">SDDL \_ 檔案 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="23a3c-278">SDDL\_FILE\_WRITE</span></span>  | <span data-ttu-id="23a3c-279">檔案 \_ 一般 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="23a3c-279">FILE\_GENERIC\_WRITE</span></span> |
| <span data-ttu-id="23a3c-280">FX</span><span class="sxs-lookup"><span data-stu-id="23a3c-280">"FX"</span></span>                 | <span data-ttu-id="23a3c-281">SDDL \_ 檔案 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="23a3c-281">SDDL\_FILE\_EXECUTE</span></span> | <span data-ttu-id="23a3c-282">FILE \_ GENERIC \_ EXECUTE</span><span class="sxs-lookup"><span data-stu-id="23a3c-282">FILE\_GENERIC\_EXECUTE</span></span> |


### <a name="registry-key-access-rights"></a><span data-ttu-id="23a3c-283">登錄機碼存取權限</span><span class="sxs-lookup"><span data-stu-id="23a3c-283">Registry key access rights</span></span>

| <span data-ttu-id="23a3c-284">存取權限字串</span><span class="sxs-lookup"><span data-stu-id="23a3c-284">Access rights string</span></span> | <span data-ttu-id="23a3c-285">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="23a3c-285">Constant in Sddl.h</span></span> | <span data-ttu-id="23a3c-286">存取權限值</span><span class="sxs-lookup"><span data-stu-id="23a3c-286">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="23a3c-287">KA</span><span class="sxs-lookup"><span data-stu-id="23a3c-287">"KA"</span></span>                 | <span data-ttu-id="23a3c-288">SDDL \_ 金鑰 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="23a3c-288">SDDL\_KEY\_ALL</span></span>     | <span data-ttu-id="23a3c-289">金鑰 \_ 所有 \_ 存取權</span><span class="sxs-lookup"><span data-stu-id="23a3c-289">KEY\_ALL\_ACCESS</span></span>   |
| <span data-ttu-id="23a3c-290">南韓</span><span class="sxs-lookup"><span data-stu-id="23a3c-290">"KR"</span></span>                 | <span data-ttu-id="23a3c-291">SDDL \_ 金鑰 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="23a3c-291">SDDL\_KEY\_READ</span></span>    | <span data-ttu-id="23a3c-292">金鑰 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="23a3c-292">KEY\_READ</span></span>          |
| <span data-ttu-id="23a3c-293">知識</span><span class="sxs-lookup"><span data-stu-id="23a3c-293">"KW"</span></span>                 | <span data-ttu-id="23a3c-294">SDDL \_ 金鑰 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="23a3c-294">SDDL\_KEY\_WRITE</span></span>   | <span data-ttu-id="23a3c-295">金鑰 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="23a3c-295">KEY\_WRITE</span></span>         |
| <span data-ttu-id="23a3c-296">"KX"</span><span class="sxs-lookup"><span data-stu-id="23a3c-296">"KX"</span></span>                 | <span data-ttu-id="23a3c-297">SDDL \_ 金鑰 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="23a3c-297">SDDL\_KEY\_EXECUTE</span></span> | <span data-ttu-id="23a3c-298">金鑰 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="23a3c-298">KEY\_EXECUTE</span></span>       |

### <a name="mandatory-label-rights"></a><span data-ttu-id="23a3c-299">強制標籤許可權</span><span class="sxs-lookup"><span data-stu-id="23a3c-299">Mandatory label rights</span></span>

| <span data-ttu-id="23a3c-300">存取權限字串</span><span class="sxs-lookup"><span data-stu-id="23a3c-300">Access rights string</span></span> | <span data-ttu-id="23a3c-301">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="23a3c-301">Constant in Sddl.h</span></span> | <span data-ttu-id="23a3c-302">存取權限值</span><span class="sxs-lookup"><span data-stu-id="23a3c-302">Access right value</span></span> |
|----------------------|--------------------|--------------------|
| <span data-ttu-id="23a3c-303">NR</span><span class="sxs-lookup"><span data-stu-id="23a3c-303">"NR"</span></span>                 | <span data-ttu-id="23a3c-304">SDDL \_ 沒有 \_ 讀取 \_</span><span class="sxs-lookup"><span data-stu-id="23a3c-304">SDDL\_NO\_READ\_UP</span></span> | <span data-ttu-id="23a3c-305">系統 \_ 強制 \_ 卷 \_ 標 \_ 否 \_ 讀取 **windows Server 2008、windows Vista 和 windows server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-305">SYSTEM\_MANDATORY\_LABEL\_NO\_READ\_UP **Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span> |
| <span data-ttu-id="23a3c-306">NW</span><span class="sxs-lookup"><span data-stu-id="23a3c-306">"NW"</span></span>                 | <span data-ttu-id="23a3c-307">SDDL \_ 沒有 \_ 寫入 \_</span><span class="sxs-lookup"><span data-stu-id="23a3c-307">SDDL\_NO\_WRITE\_UP</span></span> | <span data-ttu-id="23a3c-308">系統 \_ 強制 \_ 卷 \_ 標 \_ \_ ：無法撰寫 **windows Server 2008、windows Vista 和 windows server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-308">SYSTEM\_MANDATORY\_LABEL\_NO\_WRITE\_UP **Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span> |
| <span data-ttu-id="23a3c-309">NX</span><span class="sxs-lookup"><span data-stu-id="23a3c-309">"NX"</span></span>                 | <span data-ttu-id="23a3c-310">SDDL \_ 沒有 \_ 執行 \_</span><span class="sxs-lookup"><span data-stu-id="23a3c-310">SDDL\_NO\_EXECUTE\_UP</span></span> | <span data-ttu-id="23a3c-311">系統 \_ 強制 \_ 卷 \_ 標 \_ \_ ：不執行 **windows Server 2008、windows Vista 和 windows server 2003：** 無法使用。</span><span class="sxs-lookup"><span data-stu-id="23a3c-311">SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP **Windows Server 2008, Windows Vista and Windows Server 2003:** Not available.</span></span> |
</dd> <dt>

<span data-ttu-id="23a3c-312"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**物件 \_ guid**</span><span class="sxs-lookup"><span data-stu-id="23a3c-312"><span id="object_guid"></span><span id="OBJECT_GUID"></span>**object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="23a3c-313">GUID 的字串標記法，指出物件特定 ACE 結構的 **ObjectType** 成員值，例如 [**存取 \_ 允許的 \_ 物件 \_ ace**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace)。</span><span class="sxs-lookup"><span data-stu-id="23a3c-313">A string representation of a GUID that indicates the value of the **ObjectType** member of an object-specific ACE structure, such as [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace).</span></span> <span data-ttu-id="23a3c-314">GUID 字串會使用 [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) 函數所傳回的格式。</span><span class="sxs-lookup"><span data-stu-id="23a3c-314">The GUID string uses the format returned by the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) function.</span></span>

<span data-ttu-id="23a3c-315">下表列出一些常用的物件 Guid。</span><span class="sxs-lookup"><span data-stu-id="23a3c-315">The following table lists some commonly used object GUIDs.</span></span>



| <span data-ttu-id="23a3c-316">許可權和 GUID</span><span class="sxs-lookup"><span data-stu-id="23a3c-316">Rights and GUID</span></span>                         | <span data-ttu-id="23a3c-317">權限</span><span class="sxs-lookup"><span data-stu-id="23a3c-317">Permission</span></span>      |
|-----------------------------------------|-----------------|
| <span data-ttu-id="23a3c-318">CR; ab721a53-1e2f-11d0-9819-00aa0040529b</span><span class="sxs-lookup"><span data-stu-id="23a3c-318">CR;ab721a53-1e2f-11d0-9819-00aa0040529b</span></span> | <span data-ttu-id="23a3c-319">變更密碼</span><span class="sxs-lookup"><span data-stu-id="23a3c-319">Change password</span></span> |
| <span data-ttu-id="23a3c-320">CR; 00299570-246d-11d0-a768-00aa006e0529</span><span class="sxs-lookup"><span data-stu-id="23a3c-320">CR;00299570-246d-11d0-a768-00aa006e0529</span></span> | <span data-ttu-id="23a3c-321">重設密碼</span><span class="sxs-lookup"><span data-stu-id="23a3c-321">Reset password</span></span>  |



 

</dd> <dt>

<span data-ttu-id="23a3c-322"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**繼承 \_ 物件 \_ guid**</span><span class="sxs-lookup"><span data-stu-id="23a3c-322"><span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**inherit\_object\_guid**</span></span>
</dt> <dd>

<span data-ttu-id="23a3c-323">GUID 的字串表示，指出物件特定 ACE 結構的 **InheritedObjectType** 成員值。</span><span class="sxs-lookup"><span data-stu-id="23a3c-323">A string representation of a GUID that indicates the value of the **InheritedObjectType** member of an object-specific ACE structure.</span></span> <span data-ttu-id="23a3c-324">GUID 字串使用 [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) 格式。</span><span class="sxs-lookup"><span data-stu-id="23a3c-324">The GUID string uses the [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) format.</span></span>

</dd> <dt>

<span data-ttu-id="23a3c-325"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**帳戶 \_ sid**</span><span class="sxs-lookup"><span data-stu-id="23a3c-325"><span id="account_sid"></span><span id="ACCOUNT_SID"></span>**account\_sid**</span></span>
</dt> <dd>

<span data-ttu-id="23a3c-326">識別 ACE[信任者](trustees.md)的[SID 字串](sid-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="23a3c-326">[SID string](sid-strings.md) that identifies the [trustee](trustees.md) of the ACE.</span></span>

</dd> <dt>

<span data-ttu-id="23a3c-327"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**資源 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="23a3c-327"><span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**resource\_attribute**</span></span>
</dt> <dd>

<span data-ttu-id="23a3c-328">\[選擇性 \] ：資源 \_ 屬性僅適用于資源 ace，而且是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="23a3c-328">\[OPTIONAL\] The resource\_attribute is only for resource ACEs and is optional.</span></span> <span data-ttu-id="23a3c-329">指出資料類型的字串。</span><span class="sxs-lookup"><span data-stu-id="23a3c-329">A string that indicates the data type.</span></span> <span data-ttu-id="23a3c-330">資源屬性 ace 資料類型可以是在 Sddl 中定義的下列其中一種資料類型。</span><span class="sxs-lookup"><span data-stu-id="23a3c-330">The resource attribute ace data type can be one of the following data types defined in Sddl.h.</span></span>

<span data-ttu-id="23a3c-331">\#在資源屬性中，"" 符號與 "0" 同義。</span><span class="sxs-lookup"><span data-stu-id="23a3c-331">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="23a3c-332">例如，D:AI (XA; OICI; FA;;;WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \#) ) 相當於並解釋為 D:AI (XA; OICI; FA;;;WD; (OctetStringType = = \# 01020300) ) 。</span><span class="sxs-lookup"><span data-stu-id="23a3c-332">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

<span data-ttu-id="23a3c-333">**Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista 和 Windows Server 2003：** 無法使用資源屬性。</span><span class="sxs-lookup"><span data-stu-id="23a3c-333">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:** Resource attributes are not available.</span></span>



| <span data-ttu-id="23a3c-334">資源屬性 ace 資料類型字串</span><span class="sxs-lookup"><span data-stu-id="23a3c-334">Resource attribute ace data type string</span></span> | <span data-ttu-id="23a3c-335">Sddl 中的常數</span><span class="sxs-lookup"><span data-stu-id="23a3c-335">Constant in Sddl.h</span></span> | <span data-ttu-id="23a3c-336">資料類型</span><span class="sxs-lookup"><span data-stu-id="23a3c-336">Data type</span></span>        |
|-----------------------------------------|--------------------|------------------|
| <span data-ttu-id="23a3c-337">TI</span><span class="sxs-lookup"><span data-stu-id="23a3c-337">"TI"</span></span>                                    | <span data-ttu-id="23a3c-338">SDDL \_ INT</span><span class="sxs-lookup"><span data-stu-id="23a3c-338">SDDL\_INT</span></span>          | <span data-ttu-id="23a3c-339">帶正負號的整數</span><span class="sxs-lookup"><span data-stu-id="23a3c-339">Signed integer</span></span>   |
| <span data-ttu-id="23a3c-340">TU</span><span class="sxs-lookup"><span data-stu-id="23a3c-340">"TU"</span></span>                                    | <span data-ttu-id="23a3c-341">SDDL \_ UINT</span><span class="sxs-lookup"><span data-stu-id="23a3c-341">SDDL\_UINT</span></span>         | <span data-ttu-id="23a3c-342">不帶正負號的整數</span><span class="sxs-lookup"><span data-stu-id="23a3c-342">Unsigned integer</span></span> |
| <span data-ttu-id="23a3c-343">有毒</span><span class="sxs-lookup"><span data-stu-id="23a3c-343">"TS"</span></span>                                    | <span data-ttu-id="23a3c-344">SDDL \_ WSTRING</span><span class="sxs-lookup"><span data-stu-id="23a3c-344">SDDL\_WSTRING</span></span>      | <span data-ttu-id="23a3c-345">寬字元串</span><span class="sxs-lookup"><span data-stu-id="23a3c-345">Wide string</span></span>      |
| <span data-ttu-id="23a3c-346">T</span><span class="sxs-lookup"><span data-stu-id="23a3c-346">"TD"</span></span>                                    | <span data-ttu-id="23a3c-347">SDDL \_ SID</span><span class="sxs-lookup"><span data-stu-id="23a3c-347">SDDL\_SID</span></span>          | <span data-ttu-id="23a3c-348">SID</span><span class="sxs-lookup"><span data-stu-id="23a3c-348">SID</span></span>              |
| <span data-ttu-id="23a3c-349">TX</span><span class="sxs-lookup"><span data-stu-id="23a3c-349">"TX"</span></span>                                    | <span data-ttu-id="23a3c-350">SDDL \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="23a3c-350">SDDL\_BLOB</span></span>         | <span data-ttu-id="23a3c-351">八位字串</span><span class="sxs-lookup"><span data-stu-id="23a3c-351">Octet string</span></span>     |
| <span data-ttu-id="23a3c-352">TB</span><span class="sxs-lookup"><span data-stu-id="23a3c-352">"TB"</span></span>                                    | <span data-ttu-id="23a3c-353">SDDL \_ 布林值</span><span class="sxs-lookup"><span data-stu-id="23a3c-353">SDDL\_BOOLEAN</span></span>      | <span data-ttu-id="23a3c-354">Boolean</span><span class="sxs-lookup"><span data-stu-id="23a3c-354">Boolean</span></span>          |



 

</dd> </dl>

<span data-ttu-id="23a3c-355">下列範例顯示存取允許之 ACE 的 ACE 字串。</span><span class="sxs-lookup"><span data-stu-id="23a3c-355">The following example shows an ACE string for an access-allowed ACE.</span></span> <span data-ttu-id="23a3c-356">它不是物件特定的 ACE，因此它在 **物件 \_ guid** 中沒有任何資訊，而且會 **繼承 \_ 物件 \_ guid** 欄位。</span><span class="sxs-lookup"><span data-stu-id="23a3c-356">It is not an object-specific ACE, so it has no information in the **object\_guid** and **inherit\_object\_guid** fields.</span></span> <span data-ttu-id="23a3c-357">**Ace \_ 旗標** 欄位也是空的，這表示沒有設定任何 ace 旗標。</span><span class="sxs-lookup"><span data-stu-id="23a3c-357">The **ace\_flags** field is also empty, which indicates that none of the ACE flags are set.</span></span>


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



<span data-ttu-id="23a3c-358">以上顯示的 ACE 字串會描述下列 ACE 資訊。</span><span class="sxs-lookup"><span data-stu-id="23a3c-358">The ACE string shown above describes the following ACE information.</span></span>


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



<span data-ttu-id="23a3c-359">下列範例顯示使用 Windows 的資源宣告分類的檔案，以及將密碼設定為高度商務衝擊的結構化查詢語言 (SQL)  (SQL) 。</span><span class="sxs-lookup"><span data-stu-id="23a3c-359">The following example shows a file classified with resource claims for Windows and Structured Query Language (SQL) with Secrecy set to High Business Impact.</span></span>


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



<span data-ttu-id="23a3c-360">以上顯示的 ACE 字串會描述下列 ACE 資訊。</span><span class="sxs-lookup"><span data-stu-id="23a3c-360">The ACE string shown above describes the following ACE information.</span></span>


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



<span data-ttu-id="23a3c-361">如需詳細資訊，請參閱 [安全描述項字串格式](security-descriptor-string-format.md) 和 [SID 字串](sid-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="23a3c-361">For more information, see [Security Descriptor String Format](security-descriptor-string-format.md) and [SID Strings](sid-strings.md).</span></span> <span data-ttu-id="23a3c-362">針對條件式 Ace，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)。</span><span class="sxs-lookup"><span data-stu-id="23a3c-362">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23a3c-363">相關主題</span><span class="sxs-lookup"><span data-stu-id="23a3c-363">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="23a3c-364">[\[DTYP \] ：安全描述項描述語言](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="23a3c-364">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

