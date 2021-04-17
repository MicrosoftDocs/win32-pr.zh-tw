---
title: Nt-Pwd-歷程記錄屬性
description: Windows NT 單向格式的使用者密碼歷程記錄 (OWF) 。 Windows 2000 使用 Windows NT OWF。
ms.assetid: 7c6a0fe2-561e-43a2-af46-7505e7e13288
ms.tgt_platform: multiple
keywords:
- Nt-Pwd-歷程記錄屬性 AD 架構
- ntPwdHistory 屬性 AD 架構
topic_type:
- apiref
api_name:
- Nt-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41ed3196109d13d4fb6cfae7e23be7ffdfb8c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509678"
---
# <a name="nt-pwd-history-attribute"></a><span data-ttu-id="f0ebf-106">Nt-Pwd-歷程記錄屬性</span><span class="sxs-lookup"><span data-stu-id="f0ebf-106">Nt-Pwd-History attribute</span></span>

<span data-ttu-id="f0ebf-107">Windows NT 單向格式的使用者密碼歷程記錄 (OWF) 。</span><span class="sxs-lookup"><span data-stu-id="f0ebf-107">The password history of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="f0ebf-108">Windows 2000 使用 Windows NT OWF。</span><span class="sxs-lookup"><span data-stu-id="f0ebf-108">Windows 2000 uses the Windows NT OWF.</span></span>



| <span data-ttu-id="f0ebf-109">進入</span><span class="sxs-lookup"><span data-stu-id="f0ebf-109">Entry</span></span> | <span data-ttu-id="f0ebf-110">值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f0ebf-111">CN</span><span class="sxs-lookup"><span data-stu-id="f0ebf-111">CN</span></span>                | <span data-ttu-id="f0ebf-112">Nt-Pwd-歷程記錄</span><span class="sxs-lookup"><span data-stu-id="f0ebf-112">Nt-Pwd-History</span></span>                                        |
| <span data-ttu-id="f0ebf-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f0ebf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f0ebf-114">ntPwdHistory</span><span class="sxs-lookup"><span data-stu-id="f0ebf-114">ntPwdHistory</span></span>                                          |
| <span data-ttu-id="f0ebf-115">大小</span><span class="sxs-lookup"><span data-stu-id="f0ebf-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f0ebf-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f0ebf-116">Update Privilege</span></span>  | <span data-ttu-id="f0ebf-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="f0ebf-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="f0ebf-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f0ebf-118">Update Frequency</span></span>  | <span data-ttu-id="f0ebf-119">每次使用者變更密碼時。</span><span class="sxs-lookup"><span data-stu-id="f0ebf-119">Each time the user changes passwords.</span></span>                 |
| <span data-ttu-id="f0ebf-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f0ebf-120">Attribute-Id</span></span>      | <span data-ttu-id="f0ebf-121">1.2.840.113556.1.4.94</span><span class="sxs-lookup"><span data-stu-id="f0ebf-121">1.2.840.113556.1.4.94</span></span>                                 |
| <span data-ttu-id="f0ebf-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f0ebf-122">System-Id-Guid</span></span>    | <span data-ttu-id="f0ebf-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f0ebf-123">bf9679e2-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="f0ebf-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0ebf-124">Syntax</span></span>            | [<span data-ttu-id="f0ebf-125">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-125">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f0ebf-126">實作</span><span class="sxs-lookup"><span data-stu-id="f0ebf-126">Implementations</span></span>

-   [<span data-ttu-id="f0ebf-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f0ebf-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f0ebf-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f0ebf-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f0ebf-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f0ebf-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f0ebf-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f0ebf-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f0ebf-134">Windows 2000 Server</span></span>



| <span data-ttu-id="f0ebf-135">進入</span><span class="sxs-lookup"><span data-stu-id="f0ebf-135">Entry</span></span> | <span data-ttu-id="f0ebf-136">值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0ebf-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ebf-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0ebf-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ebf-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0ebf-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ebf-139">System-Only</span></span>            | <span data-ttu-id="f0ebf-140">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-140">False</span></span>                             |
| <span data-ttu-id="f0ebf-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ebf-142">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-142">False</span></span>                             |
| <span data-ttu-id="f0ebf-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ebf-143">Is Indexed</span></span>             | <span data-ttu-id="f0ebf-144">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-144">False</span></span>                             |
| <span data-ttu-id="f0ebf-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ebf-145">In Global Catalog</span></span>      | <span data-ttu-id="f0ebf-146">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-146">False</span></span>                             |
| <span data-ttu-id="f0ebf-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ebf-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ebf-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ebf-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0ebf-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ebf-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f0ebf-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ebf-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f0ebf-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-151">Search-Flags</span></span>           | <span data-ttu-id="f0ebf-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ebf-152">0x00000000</span></span>                        |
| <span data-ttu-id="f0ebf-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-153">System-Flags</span></span>           | <span data-ttu-id="f0ebf-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ebf-154">0x00000010</span></span>                        |
| <span data-ttu-id="f0ebf-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ebf-155">Classes used in</span></span>        | [<span data-ttu-id="f0ebf-156">**User**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f0ebf-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0ebf-157">Windows Server 2003</span></span>



| <span data-ttu-id="f0ebf-158">進入</span><span class="sxs-lookup"><span data-stu-id="f0ebf-158">Entry</span></span> | <span data-ttu-id="f0ebf-159">值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0ebf-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ebf-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0ebf-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ebf-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0ebf-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ebf-162">System-Only</span></span>            | <span data-ttu-id="f0ebf-163">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-163">False</span></span>                             |
| <span data-ttu-id="f0ebf-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ebf-165">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-165">False</span></span>                             |
| <span data-ttu-id="f0ebf-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ebf-166">Is Indexed</span></span>             | <span data-ttu-id="f0ebf-167">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-167">False</span></span>                             |
| <span data-ttu-id="f0ebf-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ebf-168">In Global Catalog</span></span>      | <span data-ttu-id="f0ebf-169">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-169">False</span></span>                             |
| <span data-ttu-id="f0ebf-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ebf-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ebf-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ebf-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0ebf-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ebf-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f0ebf-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ebf-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f0ebf-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-174">Search-Flags</span></span>           | <span data-ttu-id="f0ebf-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ebf-175">0x00000000</span></span>                        |
| <span data-ttu-id="f0ebf-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-176">System-Flags</span></span>           | <span data-ttu-id="f0ebf-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ebf-177">0x00000010</span></span>                        |
| <span data-ttu-id="f0ebf-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ebf-178">Classes used in</span></span>        | [<span data-ttu-id="f0ebf-179">**User**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f0ebf-180">亞當</span><span class="sxs-lookup"><span data-stu-id="f0ebf-180">ADAM</span></span>



| <span data-ttu-id="f0ebf-181">進入</span><span class="sxs-lookup"><span data-stu-id="f0ebf-181">Entry</span></span> | <span data-ttu-id="f0ebf-182">值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f0ebf-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ebf-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f0ebf-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ebf-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="f0ebf-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ebf-185">System-Only</span></span>            | <span data-ttu-id="f0ebf-186">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-186">False</span></span>                                                             |
| <span data-ttu-id="f0ebf-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ebf-188">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-188">False</span></span>                                                             |
| <span data-ttu-id="f0ebf-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ebf-189">Is Indexed</span></span>             | <span data-ttu-id="f0ebf-190">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-190">False</span></span>                                                             |
| <span data-ttu-id="f0ebf-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ebf-191">In Global Catalog</span></span>      | <span data-ttu-id="f0ebf-192">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-192">False</span></span>                                                             |
| <span data-ttu-id="f0ebf-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ebf-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ebf-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ebf-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="f0ebf-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ebf-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="f0ebf-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ebf-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="f0ebf-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-197">Search-Flags</span></span>           | <span data-ttu-id="f0ebf-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ebf-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="f0ebf-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-199">System-Flags</span></span>           | <span data-ttu-id="f0ebf-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ebf-200">0x00000010</span></span>                                                        |
| <span data-ttu-id="f0ebf-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ebf-201">Classes used in</span></span>        | [<span data-ttu-id="f0ebf-202">**ms DS 可系結-物件**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f0ebf-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f0ebf-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f0ebf-204">進入</span><span class="sxs-lookup"><span data-stu-id="f0ebf-204">Entry</span></span> | <span data-ttu-id="f0ebf-205">值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0ebf-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ebf-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0ebf-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ebf-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0ebf-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ebf-208">System-Only</span></span>            | <span data-ttu-id="f0ebf-209">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-209">False</span></span>                             |
| <span data-ttu-id="f0ebf-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-210">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ebf-211">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-211">False</span></span>                             |
| <span data-ttu-id="f0ebf-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ebf-212">Is Indexed</span></span>             | <span data-ttu-id="f0ebf-213">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-213">False</span></span>                             |
| <span data-ttu-id="f0ebf-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ebf-214">In Global Catalog</span></span>      | <span data-ttu-id="f0ebf-215">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-215">False</span></span>                             |
| <span data-ttu-id="f0ebf-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ebf-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ebf-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ebf-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0ebf-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ebf-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f0ebf-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ebf-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f0ebf-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-220">Search-Flags</span></span>           | <span data-ttu-id="f0ebf-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ebf-221">0x00000000</span></span>                        |
| <span data-ttu-id="f0ebf-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-222">System-Flags</span></span>           | <span data-ttu-id="f0ebf-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ebf-223">0x00000010</span></span>                        |
| <span data-ttu-id="f0ebf-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ebf-224">Classes used in</span></span>        | [<span data-ttu-id="f0ebf-225">**User**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f0ebf-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0ebf-226">Windows Server 2008</span></span>



| <span data-ttu-id="f0ebf-227">進入</span><span class="sxs-lookup"><span data-stu-id="f0ebf-227">Entry</span></span> | <span data-ttu-id="f0ebf-228">值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0ebf-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ebf-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0ebf-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ebf-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0ebf-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ebf-231">System-Only</span></span>            | <span data-ttu-id="f0ebf-232">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-232">False</span></span>                             |
| <span data-ttu-id="f0ebf-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-233">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ebf-234">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-234">False</span></span>                             |
| <span data-ttu-id="f0ebf-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ebf-235">Is Indexed</span></span>             | <span data-ttu-id="f0ebf-236">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-236">False</span></span>                             |
| <span data-ttu-id="f0ebf-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ebf-237">In Global Catalog</span></span>      | <span data-ttu-id="f0ebf-238">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-238">False</span></span>                             |
| <span data-ttu-id="f0ebf-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ebf-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ebf-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ebf-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0ebf-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ebf-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f0ebf-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ebf-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f0ebf-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-243">Search-Flags</span></span>           | <span data-ttu-id="f0ebf-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ebf-244">0x00000000</span></span>                        |
| <span data-ttu-id="f0ebf-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-245">System-Flags</span></span>           | <span data-ttu-id="f0ebf-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ebf-246">0x00000010</span></span>                        |
| <span data-ttu-id="f0ebf-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ebf-247">Classes used in</span></span>        | [<span data-ttu-id="f0ebf-248">**User**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f0ebf-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0ebf-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f0ebf-250">進入</span><span class="sxs-lookup"><span data-stu-id="f0ebf-250">Entry</span></span> | <span data-ttu-id="f0ebf-251">值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0ebf-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ebf-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0ebf-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ebf-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0ebf-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ebf-254">System-Only</span></span>            | <span data-ttu-id="f0ebf-255">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-255">False</span></span>                             |
| <span data-ttu-id="f0ebf-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-256">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ebf-257">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-257">False</span></span>                             |
| <span data-ttu-id="f0ebf-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ebf-258">Is Indexed</span></span>             | <span data-ttu-id="f0ebf-259">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-259">False</span></span>                             |
| <span data-ttu-id="f0ebf-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ebf-260">In Global Catalog</span></span>      | <span data-ttu-id="f0ebf-261">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-261">False</span></span>                             |
| <span data-ttu-id="f0ebf-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ebf-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ebf-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ebf-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0ebf-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ebf-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f0ebf-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ebf-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f0ebf-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-266">Search-Flags</span></span>           | <span data-ttu-id="f0ebf-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ebf-267">0x00000000</span></span>                        |
| <span data-ttu-id="f0ebf-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-268">System-Flags</span></span>           | <span data-ttu-id="f0ebf-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ebf-269">0x00000010</span></span>                        |
| <span data-ttu-id="f0ebf-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ebf-270">Classes used in</span></span>        | [<span data-ttu-id="f0ebf-271">**User**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f0ebf-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0ebf-272">Windows Server 2012</span></span>



| <span data-ttu-id="f0ebf-273">進入</span><span class="sxs-lookup"><span data-stu-id="f0ebf-273">Entry</span></span> | <span data-ttu-id="f0ebf-274">值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0ebf-275">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ebf-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0ebf-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ebf-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0ebf-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ebf-277">System-Only</span></span>            | <span data-ttu-id="f0ebf-278">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-278">False</span></span>                             |
| <span data-ttu-id="f0ebf-279">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ebf-279">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ebf-280">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-280">False</span></span>                             |
| <span data-ttu-id="f0ebf-281">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ebf-281">Is Indexed</span></span>             | <span data-ttu-id="f0ebf-282">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-282">False</span></span>                             |
| <span data-ttu-id="f0ebf-283">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ebf-283">In Global Catalog</span></span>      | <span data-ttu-id="f0ebf-284">否</span><span class="sxs-lookup"><span data-stu-id="f0ebf-284">False</span></span>                             |
| <span data-ttu-id="f0ebf-285">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ebf-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ebf-286">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ebf-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0ebf-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ebf-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f0ebf-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ebf-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f0ebf-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-289">Search-Flags</span></span>           | <span data-ttu-id="f0ebf-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ebf-290">0x00000000</span></span>                        |
| <span data-ttu-id="f0ebf-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ebf-291">System-Flags</span></span>           | <span data-ttu-id="f0ebf-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ebf-292">0x00000010</span></span>                        |
| <span data-ttu-id="f0ebf-293">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ebf-293">Classes used in</span></span>        | [<span data-ttu-id="f0ebf-294">**User**</span><span class="sxs-lookup"><span data-stu-id="f0ebf-294">**User**</span></span>](c-user.md)<br/> |



 

 





