---
title: Lm-Pwd-歷程記錄屬性
description: LAN Manager 使用者的密碼歷程記錄 (LM) 單向格式 (OWF) 。 LM OWF 是用於與 LAN Manager 2.x 用戶端、Windows 95 和 Windows 98 的相容性。
ms.assetid: c4cb2e74-b37d-4c76-8d21-d71bc9c19a4a
ms.tgt_platform: multiple
keywords:
- Lm-Pwd-歷程記錄屬性 AD 架構
- lmPwdHistory 屬性 AD 架構
topic_type:
- apiref
api_name:
- Lm-Pwd-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f5c73b35bb0ea2cae9d01324d82e1568485541
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845231"
---
# <a name="lm-pwd-history-attribute"></a><span data-ttu-id="7a96a-106">Lm-Pwd-歷程記錄屬性</span><span class="sxs-lookup"><span data-stu-id="7a96a-106">Lm-Pwd-History attribute</span></span>

<span data-ttu-id="7a96a-107">LAN Manager 使用者的密碼歷程記錄 (LM) 單向格式 (OWF) 。</span><span class="sxs-lookup"><span data-stu-id="7a96a-107">The password history of the user in LAN Manager (LM) one-way format (OWF).</span></span> <span data-ttu-id="7a96a-108">LM OWF 是用於與 LAN Manager 2 的相容性。*x* 用戶端、windows 95 和 windows 98。</span><span class="sxs-lookup"><span data-stu-id="7a96a-108">The LM OWF is used for compatibility with LAN Manager 2.*x* clients, Windows 95, and Windows 98.</span></span>



| <span data-ttu-id="7a96a-109">進入</span><span class="sxs-lookup"><span data-stu-id="7a96a-109">Entry</span></span> | <span data-ttu-id="7a96a-110">值</span><span class="sxs-lookup"><span data-stu-id="7a96a-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="7a96a-111">CN</span><span class="sxs-lookup"><span data-stu-id="7a96a-111">CN</span></span>                | <span data-ttu-id="7a96a-112">Lm-Pwd-歷程記錄</span><span class="sxs-lookup"><span data-stu-id="7a96a-112">Lm-Pwd-History</span></span>                                        |
| <span data-ttu-id="7a96a-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7a96a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7a96a-114">lmPwdHistory</span><span class="sxs-lookup"><span data-stu-id="7a96a-114">lmPwdHistory</span></span>                                          |
| <span data-ttu-id="7a96a-115">大小</span><span class="sxs-lookup"><span data-stu-id="7a96a-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="7a96a-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7a96a-116">Update Privilege</span></span>  | <span data-ttu-id="7a96a-117">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="7a96a-117">Domain administrator</span></span>                                  |
| <span data-ttu-id="7a96a-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7a96a-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="7a96a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7a96a-119">Attribute-Id</span></span>      | <span data-ttu-id="7a96a-120">1.2.840.113556.1.4.160</span><span class="sxs-lookup"><span data-stu-id="7a96a-120">1.2.840.113556.1.4.160</span></span>                                |
| <span data-ttu-id="7a96a-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7a96a-121">System-Id-Guid</span></span>    | <span data-ttu-id="7a96a-122">bf96799d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="7a96a-122">bf96799d-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="7a96a-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a96a-123">Syntax</span></span>            | [<span data-ttu-id="7a96a-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="7a96a-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="7a96a-125">實作</span><span class="sxs-lookup"><span data-stu-id="7a96a-125">Implementations</span></span>

-   [<span data-ttu-id="7a96a-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7a96a-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7a96a-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7a96a-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7a96a-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7a96a-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7a96a-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7a96a-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7a96a-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7a96a-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7a96a-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7a96a-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7a96a-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7a96a-132">Windows 2000 Server</span></span>



| <span data-ttu-id="7a96a-133">進入</span><span class="sxs-lookup"><span data-stu-id="7a96a-133">Entry</span></span> | <span data-ttu-id="7a96a-134">值</span><span class="sxs-lookup"><span data-stu-id="7a96a-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7a96a-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7a96a-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7a96a-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a96a-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7a96a-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a96a-137">System-Only</span></span>            | <span data-ttu-id="7a96a-138">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-138">False</span></span>                             |
| <span data-ttu-id="7a96a-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7a96a-139">Is-Single-Valued</span></span>       | <span data-ttu-id="7a96a-140">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-140">False</span></span>                             |
| <span data-ttu-id="7a96a-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7a96a-141">Is Indexed</span></span>             | <span data-ttu-id="7a96a-142">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-142">False</span></span>                             |
| <span data-ttu-id="7a96a-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7a96a-143">In Global Catalog</span></span>      | <span data-ttu-id="7a96a-144">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-144">False</span></span>                             |
| <span data-ttu-id="7a96a-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7a96a-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a96a-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7a96a-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7a96a-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a96a-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7a96a-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a96a-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7a96a-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a96a-149">Search-Flags</span></span>           | <span data-ttu-id="7a96a-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a96a-150">0x00000000</span></span>                        |
| <span data-ttu-id="7a96a-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a96a-151">System-Flags</span></span>           | <span data-ttu-id="7a96a-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a96a-152">0x00000010</span></span>                        |
| <span data-ttu-id="7a96a-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7a96a-153">Classes used in</span></span>        | [<span data-ttu-id="7a96a-154">**User**</span><span class="sxs-lookup"><span data-stu-id="7a96a-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7a96a-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7a96a-155">Windows Server 2003</span></span>



| <span data-ttu-id="7a96a-156">進入</span><span class="sxs-lookup"><span data-stu-id="7a96a-156">Entry</span></span> | <span data-ttu-id="7a96a-157">值</span><span class="sxs-lookup"><span data-stu-id="7a96a-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7a96a-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7a96a-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7a96a-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a96a-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7a96a-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a96a-160">System-Only</span></span>            | <span data-ttu-id="7a96a-161">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-161">False</span></span>                             |
| <span data-ttu-id="7a96a-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7a96a-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7a96a-163">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-163">False</span></span>                             |
| <span data-ttu-id="7a96a-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7a96a-164">Is Indexed</span></span>             | <span data-ttu-id="7a96a-165">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-165">False</span></span>                             |
| <span data-ttu-id="7a96a-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7a96a-166">In Global Catalog</span></span>      | <span data-ttu-id="7a96a-167">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-167">False</span></span>                             |
| <span data-ttu-id="7a96a-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7a96a-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a96a-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7a96a-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7a96a-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a96a-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7a96a-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a96a-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7a96a-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a96a-172">Search-Flags</span></span>           | <span data-ttu-id="7a96a-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a96a-173">0x00000000</span></span>                        |
| <span data-ttu-id="7a96a-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a96a-174">System-Flags</span></span>           | <span data-ttu-id="7a96a-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a96a-175">0x00000010</span></span>                        |
| <span data-ttu-id="7a96a-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7a96a-176">Classes used in</span></span>        | [<span data-ttu-id="7a96a-177">**User**</span><span class="sxs-lookup"><span data-stu-id="7a96a-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7a96a-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7a96a-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7a96a-179">進入</span><span class="sxs-lookup"><span data-stu-id="7a96a-179">Entry</span></span> | <span data-ttu-id="7a96a-180">值</span><span class="sxs-lookup"><span data-stu-id="7a96a-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7a96a-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7a96a-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7a96a-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a96a-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7a96a-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a96a-183">System-Only</span></span>            | <span data-ttu-id="7a96a-184">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-184">False</span></span>                             |
| <span data-ttu-id="7a96a-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7a96a-185">Is-Single-Valued</span></span>       | <span data-ttu-id="7a96a-186">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-186">False</span></span>                             |
| <span data-ttu-id="7a96a-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7a96a-187">Is Indexed</span></span>             | <span data-ttu-id="7a96a-188">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-188">False</span></span>                             |
| <span data-ttu-id="7a96a-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7a96a-189">In Global Catalog</span></span>      | <span data-ttu-id="7a96a-190">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-190">False</span></span>                             |
| <span data-ttu-id="7a96a-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7a96a-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a96a-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7a96a-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7a96a-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a96a-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7a96a-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a96a-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7a96a-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a96a-195">Search-Flags</span></span>           | <span data-ttu-id="7a96a-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a96a-196">0x00000000</span></span>                        |
| <span data-ttu-id="7a96a-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a96a-197">System-Flags</span></span>           | <span data-ttu-id="7a96a-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a96a-198">0x00000010</span></span>                        |
| <span data-ttu-id="7a96a-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7a96a-199">Classes used in</span></span>        | [<span data-ttu-id="7a96a-200">**User**</span><span class="sxs-lookup"><span data-stu-id="7a96a-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7a96a-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a96a-201">Windows Server 2008</span></span>



| <span data-ttu-id="7a96a-202">進入</span><span class="sxs-lookup"><span data-stu-id="7a96a-202">Entry</span></span> | <span data-ttu-id="7a96a-203">值</span><span class="sxs-lookup"><span data-stu-id="7a96a-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7a96a-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7a96a-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7a96a-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a96a-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7a96a-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a96a-206">System-Only</span></span>            | <span data-ttu-id="7a96a-207">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-207">False</span></span>                             |
| <span data-ttu-id="7a96a-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7a96a-208">Is-Single-Valued</span></span>       | <span data-ttu-id="7a96a-209">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-209">False</span></span>                             |
| <span data-ttu-id="7a96a-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7a96a-210">Is Indexed</span></span>             | <span data-ttu-id="7a96a-211">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-211">False</span></span>                             |
| <span data-ttu-id="7a96a-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7a96a-212">In Global Catalog</span></span>      | <span data-ttu-id="7a96a-213">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-213">False</span></span>                             |
| <span data-ttu-id="7a96a-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7a96a-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a96a-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7a96a-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7a96a-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a96a-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7a96a-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a96a-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7a96a-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a96a-218">Search-Flags</span></span>           | <span data-ttu-id="7a96a-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a96a-219">0x00000000</span></span>                        |
| <span data-ttu-id="7a96a-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a96a-220">System-Flags</span></span>           | <span data-ttu-id="7a96a-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a96a-221">0x00000010</span></span>                        |
| <span data-ttu-id="7a96a-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7a96a-222">Classes used in</span></span>        | [<span data-ttu-id="7a96a-223">**User**</span><span class="sxs-lookup"><span data-stu-id="7a96a-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7a96a-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a96a-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7a96a-225">進入</span><span class="sxs-lookup"><span data-stu-id="7a96a-225">Entry</span></span> | <span data-ttu-id="7a96a-226">值</span><span class="sxs-lookup"><span data-stu-id="7a96a-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7a96a-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7a96a-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7a96a-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a96a-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7a96a-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a96a-229">System-Only</span></span>            | <span data-ttu-id="7a96a-230">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-230">False</span></span>                             |
| <span data-ttu-id="7a96a-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7a96a-231">Is-Single-Valued</span></span>       | <span data-ttu-id="7a96a-232">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-232">False</span></span>                             |
| <span data-ttu-id="7a96a-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7a96a-233">Is Indexed</span></span>             | <span data-ttu-id="7a96a-234">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-234">False</span></span>                             |
| <span data-ttu-id="7a96a-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7a96a-235">In Global Catalog</span></span>      | <span data-ttu-id="7a96a-236">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-236">False</span></span>                             |
| <span data-ttu-id="7a96a-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7a96a-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a96a-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7a96a-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7a96a-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a96a-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7a96a-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a96a-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7a96a-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a96a-241">Search-Flags</span></span>           | <span data-ttu-id="7a96a-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a96a-242">0x00000000</span></span>                        |
| <span data-ttu-id="7a96a-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a96a-243">System-Flags</span></span>           | <span data-ttu-id="7a96a-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a96a-244">0x00000010</span></span>                        |
| <span data-ttu-id="7a96a-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7a96a-245">Classes used in</span></span>        | [<span data-ttu-id="7a96a-246">**User**</span><span class="sxs-lookup"><span data-stu-id="7a96a-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7a96a-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a96a-247">Windows Server 2012</span></span>



| <span data-ttu-id="7a96a-248">進入</span><span class="sxs-lookup"><span data-stu-id="7a96a-248">Entry</span></span> | <span data-ttu-id="7a96a-249">值</span><span class="sxs-lookup"><span data-stu-id="7a96a-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7a96a-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7a96a-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7a96a-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a96a-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7a96a-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a96a-252">System-Only</span></span>            | <span data-ttu-id="7a96a-253">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-253">False</span></span>                             |
| <span data-ttu-id="7a96a-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7a96a-254">Is-Single-Valued</span></span>       | <span data-ttu-id="7a96a-255">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-255">False</span></span>                             |
| <span data-ttu-id="7a96a-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7a96a-256">Is Indexed</span></span>             | <span data-ttu-id="7a96a-257">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-257">False</span></span>                             |
| <span data-ttu-id="7a96a-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7a96a-258">In Global Catalog</span></span>      | <span data-ttu-id="7a96a-259">否</span><span class="sxs-lookup"><span data-stu-id="7a96a-259">False</span></span>                             |
| <span data-ttu-id="7a96a-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7a96a-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a96a-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7a96a-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7a96a-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a96a-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7a96a-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a96a-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7a96a-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a96a-264">Search-Flags</span></span>           | <span data-ttu-id="7a96a-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a96a-265">0x00000000</span></span>                        |
| <span data-ttu-id="7a96a-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a96a-266">System-Flags</span></span>           | <span data-ttu-id="7a96a-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a96a-267">0x00000010</span></span>                        |
| <span data-ttu-id="7a96a-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7a96a-268">Classes used in</span></span>        | [<span data-ttu-id="7a96a-269">**User**</span><span class="sxs-lookup"><span data-stu-id="7a96a-269">**User**</span></span>](c-user.md)<br/> |



 

 





