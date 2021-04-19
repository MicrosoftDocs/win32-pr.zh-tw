---
description: 列出目前定義的 ACE 類型。
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: 'ACE (Winnt. h) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d06b3457e4df6aea38d3e35acf4f7aaa4e2f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982375"
---
# <a name="ace"></a><span data-ttu-id="fc9c3-103">Ace</span><span class="sxs-lookup"><span data-stu-id="fc9c3-103">ACE</span></span>

<span data-ttu-id="fc9c3-104">**ACE** 是 [*存取控制清單*](/windows/desktop/SecGloss/a-gly)中 (ACL) 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)。</span><span class="sxs-lookup"><span data-stu-id="fc9c3-104">An **ACE** is an [*access control entry*](/windows/desktop/SecGloss/a-gly) in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span>

<span data-ttu-id="fc9c3-105">下表列出目前定義的 **ACE** 類型。</span><span class="sxs-lookup"><span data-stu-id="fc9c3-105">The following table lists the currently defined **ACE** types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc9c3-106">ACE 類型</span><span class="sxs-lookup"><span data-stu-id="fc9c3-106">ACE type</span></span></th>
<th><span data-ttu-id="fc9c3-107">結構</span><span class="sxs-lookup"><span data-stu-id="fc9c3-107">Structure</span></span></th>
<th><span data-ttu-id="fc9c3-108">ACL 類型</span><span class="sxs-lookup"><span data-stu-id="fc9c3-108">ACL type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fc9c3-109">允許存取</span><span class="sxs-lookup"><span data-stu-id="fc9c3-109">Access allowed</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-110"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-110"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-111">酌情</span><span class="sxs-lookup"><span data-stu-id="fc9c3-111">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="fc9c3-112">允許存取</span><span class="sxs-lookup"><span data-stu-id="fc9c3-112">Access allowed</span></span></li>
<li><span data-ttu-id="fc9c3-113">允許在存取檢查期間回呼</span><span class="sxs-lookup"><span data-stu-id="fc9c3-113">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-114"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-114"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-115">酌情</span><span class="sxs-lookup"><span data-stu-id="fc9c3-115">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fc9c3-116">允許存取</span><span class="sxs-lookup"><span data-stu-id="fc9c3-116">Access allowed</span></span></li>
<li><span data-ttu-id="fc9c3-117">物件特定</span><span class="sxs-lookup"><span data-stu-id="fc9c3-117">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-118"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-118"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-119">酌情</span><span class="sxs-lookup"><span data-stu-id="fc9c3-119">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="fc9c3-120">允許存取</span><span class="sxs-lookup"><span data-stu-id="fc9c3-120">Access allowed</span></span></li>
<li><span data-ttu-id="fc9c3-121">物件特定</span><span class="sxs-lookup"><span data-stu-id="fc9c3-121">Object specific</span></span></li>
<li><span data-ttu-id="fc9c3-122">允許在存取檢查期間回呼</span><span class="sxs-lookup"><span data-stu-id="fc9c3-122">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-123"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-123"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-124">酌情</span><span class="sxs-lookup"><span data-stu-id="fc9c3-124">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fc9c3-125">拒絕存取</span><span class="sxs-lookup"><span data-stu-id="fc9c3-125">Access denied</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-126"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-126"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-127">酌情</span><span class="sxs-lookup"><span data-stu-id="fc9c3-127">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="fc9c3-128">拒絕存取</span><span class="sxs-lookup"><span data-stu-id="fc9c3-128">Access denied</span></span></li>
<li><span data-ttu-id="fc9c3-129">允許在存取檢查期間回呼</span><span class="sxs-lookup"><span data-stu-id="fc9c3-129">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-130"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-130"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-131">酌情</span><span class="sxs-lookup"><span data-stu-id="fc9c3-131">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fc9c3-132">拒絕存取</span><span class="sxs-lookup"><span data-stu-id="fc9c3-132">Access denied</span></span></li>
<li><span data-ttu-id="fc9c3-133">物件特定</span><span class="sxs-lookup"><span data-stu-id="fc9c3-133">Object specific</span></span></li>
<li><span data-ttu-id="fc9c3-134">允許在存取檢查期間回呼</span><span class="sxs-lookup"><span data-stu-id="fc9c3-134">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-135"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-135"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-136">酌情</span><span class="sxs-lookup"><span data-stu-id="fc9c3-136">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="fc9c3-137">拒絕存取</span><span class="sxs-lookup"><span data-stu-id="fc9c3-137">Access denied</span></span></li>
<li><span data-ttu-id="fc9c3-138">物件特定</span><span class="sxs-lookup"><span data-stu-id="fc9c3-138">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-139"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-139"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-140">酌情</span><span class="sxs-lookup"><span data-stu-id="fc9c3-140">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fc9c3-141">系統警示</span><span class="sxs-lookup"><span data-stu-id="fc9c3-141">System alarm</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-142"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-142"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-143">系統</span><span class="sxs-lookup"><span data-stu-id="fc9c3-143">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="fc9c3-144">系統警示</span><span class="sxs-lookup"><span data-stu-id="fc9c3-144">System alarm</span></span></li>
<li><span data-ttu-id="fc9c3-145">允許在存取檢查期間回呼</span><span class="sxs-lookup"><span data-stu-id="fc9c3-145">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-146"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-146"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-147">系統</span><span class="sxs-lookup"><span data-stu-id="fc9c3-147">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fc9c3-148">系統警示</span><span class="sxs-lookup"><span data-stu-id="fc9c3-148">System alarm</span></span></li>
<li><span data-ttu-id="fc9c3-149">物件特定</span><span class="sxs-lookup"><span data-stu-id="fc9c3-149">Object specific</span></span></li>
<li><span data-ttu-id="fc9c3-150">允許在存取檢查期間回呼</span><span class="sxs-lookup"><span data-stu-id="fc9c3-150">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-151"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-151"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-152">系統</span><span class="sxs-lookup"><span data-stu-id="fc9c3-152">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="fc9c3-153">系統警示</span><span class="sxs-lookup"><span data-stu-id="fc9c3-153">System alarm</span></span></li>
<li><span data-ttu-id="fc9c3-154">物件特定</span><span class="sxs-lookup"><span data-stu-id="fc9c3-154">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-155"><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-155"><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-156">系統</span><span class="sxs-lookup"><span data-stu-id="fc9c3-156">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fc9c3-157">系統審核</span><span class="sxs-lookup"><span data-stu-id="fc9c3-157">System audit</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-158"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-158"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-159">系統</span><span class="sxs-lookup"><span data-stu-id="fc9c3-159">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="fc9c3-160">系統審核</span><span class="sxs-lookup"><span data-stu-id="fc9c3-160">System audit</span></span></li>
<li><span data-ttu-id="fc9c3-161">允許在存取檢查期間回呼</span><span class="sxs-lookup"><span data-stu-id="fc9c3-161">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-162"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-162"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-163">系統</span><span class="sxs-lookup"><span data-stu-id="fc9c3-163">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fc9c3-164">系統審核</span><span class="sxs-lookup"><span data-stu-id="fc9c3-164">System audit</span></span></li>
<li><span data-ttu-id="fc9c3-165">物件特定</span><span class="sxs-lookup"><span data-stu-id="fc9c3-165">Object specific</span></span></li>
<li><span data-ttu-id="fc9c3-166">允許在存取檢查期間回呼</span><span class="sxs-lookup"><span data-stu-id="fc9c3-166">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-167"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-167"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-168">系統</span><span class="sxs-lookup"><span data-stu-id="fc9c3-168">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="fc9c3-169">系統審核</span><span class="sxs-lookup"><span data-stu-id="fc9c3-169">System audit</span></span></li>
<li><span data-ttu-id="fc9c3-170">物件特定</span><span class="sxs-lookup"><span data-stu-id="fc9c3-170">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="fc9c3-171"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc9c3-171"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="fc9c3-172">系統</span><span class="sxs-lookup"><span data-stu-id="fc9c3-172">System</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fc9c3-173">目前不支援系統警示和物件特定的系統警示 Ace。</span><span class="sxs-lookup"><span data-stu-id="fc9c3-173">System-alarm and object-specific system-alarm ACEs are not currently supported.</span></span>

> [!Note]  
> <span data-ttu-id="fc9c3-174">每個 ACE 的開頭都是 [**ace \_ 標頭**](/windows/desktop/api/Winnt/ns-winnt-ace_header) 結構。</span><span class="sxs-lookup"><span data-stu-id="fc9c3-174">Each ACE starts with an [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="fc9c3-175">標頭之後的資料格式會根據標頭中指定的 ACE 類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="fc9c3-175">The format of the data following the header varies according to the ACE type specified in the header.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fc9c3-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc9c3-176">Requirements</span></span>



| <span data-ttu-id="fc9c3-177">需求</span><span class="sxs-lookup"><span data-stu-id="fc9c3-177">Requirement</span></span> | <span data-ttu-id="fc9c3-178">值</span><span class="sxs-lookup"><span data-stu-id="fc9c3-178">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc9c3-179">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc9c3-179">Minimum supported client</span></span><br/> | <span data-ttu-id="fc9c3-180">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc9c3-180">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="fc9c3-181">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc9c3-181">Minimum supported server</span></span><br/> | <span data-ttu-id="fc9c3-182">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc9c3-182">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="fc9c3-183">標頭</span><span class="sxs-lookup"><span data-stu-id="fc9c3-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc9c3-184"><dt>Winnt (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fc9c3-184"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc9c3-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc9c3-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc9c3-186">**AddAce**</span><span class="sxs-lookup"><span data-stu-id="fc9c3-186">**AddAce**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[<span data-ttu-id="fc9c3-187">**存取 \_ 允許的 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="fc9c3-187">**ACCESS\_ALLOWED\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[<span data-ttu-id="fc9c3-188">**\_拒絕存取 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="fc9c3-188">**ACCESS\_DENIED\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[<span data-ttu-id="fc9c3-189">**Acl**</span><span class="sxs-lookup"><span data-stu-id="fc9c3-189">**ACL**</span></span>](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[<span data-ttu-id="fc9c3-190">**系統 \_ 警報 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="fc9c3-190">**SYSTEM\_ALARM\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[<span data-ttu-id="fc9c3-191">**系統 \_ AUDIT \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="fc9c3-191">**SYSTEM\_AUDIT\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

