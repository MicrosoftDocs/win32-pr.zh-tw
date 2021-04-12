---
title: 修訂屬性
description: 安全描述項或其他變更的修訂層級。 僅用於 sam 伺服器和 ds ui 設定物件。
ms.assetid: 480de80f-3e76-4a62-a4a7-29a67f910a62
ms.tgt_platform: multiple
keywords:
- 修訂屬性 AD 架構
- 修訂屬性 AD 架構
topic_type:
- apiref
api_name:
- Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8948bd865db776c52ac021d296792a6f7d0720dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509580"
---
# <a name="revision-attribute"></a><span data-ttu-id="8242e-106">修訂屬性</span><span class="sxs-lookup"><span data-stu-id="8242e-106">Revision attribute</span></span>

<span data-ttu-id="8242e-107">安全描述項或其他變更的修訂層級。</span><span class="sxs-lookup"><span data-stu-id="8242e-107">The revision level for a security descriptor or other change.</span></span> <span data-ttu-id="8242e-108">僅用於 sam 伺服器和 ds ui 設定物件。</span><span class="sxs-lookup"><span data-stu-id="8242e-108">Only used in the sam-server and ds-ui-settings objects.</span></span>



| <span data-ttu-id="8242e-109">進入</span><span class="sxs-lookup"><span data-stu-id="8242e-109">Entry</span></span> | <span data-ttu-id="8242e-110">值</span><span class="sxs-lookup"><span data-stu-id="8242e-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8242e-111">CN</span><span class="sxs-lookup"><span data-stu-id="8242e-111">CN</span></span>                | <span data-ttu-id="8242e-112">修訂版</span><span class="sxs-lookup"><span data-stu-id="8242e-112">Revision</span></span>                             |
| <span data-ttu-id="8242e-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8242e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8242e-114">revision</span><span class="sxs-lookup"><span data-stu-id="8242e-114">revision</span></span>                             |
| <span data-ttu-id="8242e-115">大小</span><span class="sxs-lookup"><span data-stu-id="8242e-115">Size</span></span>              | <span data-ttu-id="8242e-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="8242e-116">4 bytes</span></span>                              |
| <span data-ttu-id="8242e-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8242e-117">Update Privilege</span></span>  | <span data-ttu-id="8242e-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="8242e-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="8242e-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8242e-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8242e-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8242e-120">Attribute-Id</span></span>      | <span data-ttu-id="8242e-121">1.2.840.113556.1.4.145</span><span class="sxs-lookup"><span data-stu-id="8242e-121">1.2.840.113556.1.4.145</span></span>               |
| <span data-ttu-id="8242e-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8242e-122">System-Id-Guid</span></span>    | <span data-ttu-id="8242e-123">bf967a21-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8242e-123">bf967a21-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="8242e-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="8242e-124">Syntax</span></span>            | [<span data-ttu-id="8242e-125">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="8242e-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="8242e-126">實作</span><span class="sxs-lookup"><span data-stu-id="8242e-126">Implementations</span></span>

-   [<span data-ttu-id="8242e-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8242e-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8242e-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8242e-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8242e-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="8242e-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8242e-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8242e-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8242e-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8242e-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8242e-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8242e-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8242e-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8242e-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8242e-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8242e-134">Windows 2000 Server</span></span>



| <span data-ttu-id="8242e-135">進入</span><span class="sxs-lookup"><span data-stu-id="8242e-135">Entry</span></span> | <span data-ttu-id="8242e-136">值</span><span class="sxs-lookup"><span data-stu-id="8242e-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8242e-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8242e-137">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="8242e-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8242e-138">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="8242e-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="8242e-139">System-Only</span></span>            | <span data-ttu-id="8242e-140">否</span><span class="sxs-lookup"><span data-stu-id="8242e-140">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8242e-141">Is-Single-Valued</span></span>       | <span data-ttu-id="8242e-142">對</span><span class="sxs-lookup"><span data-stu-id="8242e-142">True</span></span>                                                                                  |
| <span data-ttu-id="8242e-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8242e-143">Is Indexed</span></span>             | <span data-ttu-id="8242e-144">否</span><span class="sxs-lookup"><span data-stu-id="8242e-144">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8242e-145">In Global Catalog</span></span>      | <span data-ttu-id="8242e-146">否</span><span class="sxs-lookup"><span data-stu-id="8242e-146">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8242e-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="8242e-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8242e-148">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="8242e-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8242e-149">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="8242e-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8242e-150">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="8242e-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-151">Search-Flags</span></span>           | <span data-ttu-id="8242e-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8242e-152">0x00000000</span></span>                                                                            |
| <span data-ttu-id="8242e-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-153">System-Flags</span></span>           | <span data-ttu-id="8242e-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8242e-154">0x00000010</span></span>                                                                            |
| <span data-ttu-id="8242e-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8242e-155">Classes used in</span></span>        | [<span data-ttu-id="8242e-156">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="8242e-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="8242e-157">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8242e-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8242e-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8242e-158">Windows Server 2003</span></span>



| <span data-ttu-id="8242e-159">進入</span><span class="sxs-lookup"><span data-stu-id="8242e-159">Entry</span></span> | <span data-ttu-id="8242e-160">值</span><span class="sxs-lookup"><span data-stu-id="8242e-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8242e-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8242e-161">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="8242e-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8242e-162">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="8242e-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="8242e-163">System-Only</span></span>            | <span data-ttu-id="8242e-164">否</span><span class="sxs-lookup"><span data-stu-id="8242e-164">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8242e-165">Is-Single-Valued</span></span>       | <span data-ttu-id="8242e-166">對</span><span class="sxs-lookup"><span data-stu-id="8242e-166">True</span></span>                                                                                  |
| <span data-ttu-id="8242e-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8242e-167">Is Indexed</span></span>             | <span data-ttu-id="8242e-168">否</span><span class="sxs-lookup"><span data-stu-id="8242e-168">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8242e-169">In Global Catalog</span></span>      | <span data-ttu-id="8242e-170">否</span><span class="sxs-lookup"><span data-stu-id="8242e-170">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8242e-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="8242e-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8242e-172">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="8242e-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8242e-173">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="8242e-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8242e-174">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="8242e-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-175">Search-Flags</span></span>           | <span data-ttu-id="8242e-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8242e-176">0x00000000</span></span>                                                                            |
| <span data-ttu-id="8242e-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-177">System-Flags</span></span>           | <span data-ttu-id="8242e-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8242e-178">0x00000010</span></span>                                                                            |
| <span data-ttu-id="8242e-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8242e-179">Classes used in</span></span>        | [<span data-ttu-id="8242e-180">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="8242e-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="8242e-181">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8242e-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8242e-182">亞當</span><span class="sxs-lookup"><span data-stu-id="8242e-182">ADAM</span></span>



| <span data-ttu-id="8242e-183">進入</span><span class="sxs-lookup"><span data-stu-id="8242e-183">Entry</span></span> | <span data-ttu-id="8242e-184">值</span><span class="sxs-lookup"><span data-stu-id="8242e-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8242e-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8242e-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8242e-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8242e-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8242e-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8242e-187">System-Only</span></span>            | <span data-ttu-id="8242e-188">否</span><span class="sxs-lookup"><span data-stu-id="8242e-188">False</span></span>                           |
| <span data-ttu-id="8242e-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8242e-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8242e-190">對</span><span class="sxs-lookup"><span data-stu-id="8242e-190">True</span></span>                            |
| <span data-ttu-id="8242e-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8242e-191">Is Indexed</span></span>             | <span data-ttu-id="8242e-192">否</span><span class="sxs-lookup"><span data-stu-id="8242e-192">False</span></span>                           |
| <span data-ttu-id="8242e-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8242e-193">In Global Catalog</span></span>      | <span data-ttu-id="8242e-194">否</span><span class="sxs-lookup"><span data-stu-id="8242e-194">False</span></span>                           |
| <span data-ttu-id="8242e-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8242e-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8242e-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8242e-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8242e-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8242e-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8242e-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8242e-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8242e-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-199">Search-Flags</span></span>           | <span data-ttu-id="8242e-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8242e-200">0x00000000</span></span>                      |
| <span data-ttu-id="8242e-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-201">System-Flags</span></span>           | <span data-ttu-id="8242e-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8242e-202">0x00000010</span></span>                      |
| <span data-ttu-id="8242e-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8242e-203">Classes used in</span></span>        | [<span data-ttu-id="8242e-204">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8242e-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8242e-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8242e-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8242e-206">進入</span><span class="sxs-lookup"><span data-stu-id="8242e-206">Entry</span></span> | <span data-ttu-id="8242e-207">值</span><span class="sxs-lookup"><span data-stu-id="8242e-207">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8242e-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8242e-208">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="8242e-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8242e-209">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="8242e-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="8242e-210">System-Only</span></span>            | <span data-ttu-id="8242e-211">否</span><span class="sxs-lookup"><span data-stu-id="8242e-211">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8242e-212">Is-Single-Valued</span></span>       | <span data-ttu-id="8242e-213">對</span><span class="sxs-lookup"><span data-stu-id="8242e-213">True</span></span>                                                                                  |
| <span data-ttu-id="8242e-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8242e-214">Is Indexed</span></span>             | <span data-ttu-id="8242e-215">否</span><span class="sxs-lookup"><span data-stu-id="8242e-215">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8242e-216">In Global Catalog</span></span>      | <span data-ttu-id="8242e-217">否</span><span class="sxs-lookup"><span data-stu-id="8242e-217">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8242e-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="8242e-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8242e-219">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="8242e-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8242e-220">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="8242e-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8242e-221">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="8242e-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-222">Search-Flags</span></span>           | <span data-ttu-id="8242e-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8242e-223">0x00000000</span></span>                                                                            |
| <span data-ttu-id="8242e-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-224">System-Flags</span></span>           | <span data-ttu-id="8242e-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8242e-225">0x00000010</span></span>                                                                            |
| <span data-ttu-id="8242e-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8242e-226">Classes used in</span></span>        | [<span data-ttu-id="8242e-227">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="8242e-227">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="8242e-228">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8242e-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8242e-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8242e-229">Windows Server 2008</span></span>



| <span data-ttu-id="8242e-230">進入</span><span class="sxs-lookup"><span data-stu-id="8242e-230">Entry</span></span> | <span data-ttu-id="8242e-231">值</span><span class="sxs-lookup"><span data-stu-id="8242e-231">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8242e-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8242e-232">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="8242e-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8242e-233">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="8242e-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="8242e-234">System-Only</span></span>            | <span data-ttu-id="8242e-235">否</span><span class="sxs-lookup"><span data-stu-id="8242e-235">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8242e-236">Is-Single-Valued</span></span>       | <span data-ttu-id="8242e-237">對</span><span class="sxs-lookup"><span data-stu-id="8242e-237">True</span></span>                                                                                  |
| <span data-ttu-id="8242e-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8242e-238">Is Indexed</span></span>             | <span data-ttu-id="8242e-239">否</span><span class="sxs-lookup"><span data-stu-id="8242e-239">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8242e-240">In Global Catalog</span></span>      | <span data-ttu-id="8242e-241">否</span><span class="sxs-lookup"><span data-stu-id="8242e-241">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8242e-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="8242e-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8242e-243">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="8242e-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8242e-244">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="8242e-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8242e-245">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="8242e-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-246">Search-Flags</span></span>           | <span data-ttu-id="8242e-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8242e-247">0x00000000</span></span>                                                                            |
| <span data-ttu-id="8242e-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-248">System-Flags</span></span>           | <span data-ttu-id="8242e-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8242e-249">0x00000010</span></span>                                                                            |
| <span data-ttu-id="8242e-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8242e-250">Classes used in</span></span>        | [<span data-ttu-id="8242e-251">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="8242e-251">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="8242e-252">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8242e-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8242e-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8242e-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8242e-254">進入</span><span class="sxs-lookup"><span data-stu-id="8242e-254">Entry</span></span> | <span data-ttu-id="8242e-255">值</span><span class="sxs-lookup"><span data-stu-id="8242e-255">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8242e-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8242e-256">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="8242e-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8242e-257">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="8242e-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="8242e-258">System-Only</span></span>            | <span data-ttu-id="8242e-259">否</span><span class="sxs-lookup"><span data-stu-id="8242e-259">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8242e-260">Is-Single-Valued</span></span>       | <span data-ttu-id="8242e-261">對</span><span class="sxs-lookup"><span data-stu-id="8242e-261">True</span></span>                                                                                  |
| <span data-ttu-id="8242e-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8242e-262">Is Indexed</span></span>             | <span data-ttu-id="8242e-263">否</span><span class="sxs-lookup"><span data-stu-id="8242e-263">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8242e-264">In Global Catalog</span></span>      | <span data-ttu-id="8242e-265">否</span><span class="sxs-lookup"><span data-stu-id="8242e-265">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8242e-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="8242e-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8242e-267">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="8242e-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8242e-268">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="8242e-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8242e-269">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="8242e-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-270">Search-Flags</span></span>           | <span data-ttu-id="8242e-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8242e-271">0x00000000</span></span>                                                                            |
| <span data-ttu-id="8242e-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-272">System-Flags</span></span>           | <span data-ttu-id="8242e-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8242e-273">0x00000010</span></span>                                                                            |
| <span data-ttu-id="8242e-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8242e-274">Classes used in</span></span>        | [<span data-ttu-id="8242e-275">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="8242e-275">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="8242e-276">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8242e-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8242e-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8242e-277">Windows Server 2012</span></span>



| <span data-ttu-id="8242e-278">進入</span><span class="sxs-lookup"><span data-stu-id="8242e-278">Entry</span></span> | <span data-ttu-id="8242e-279">值</span><span class="sxs-lookup"><span data-stu-id="8242e-279">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8242e-280">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8242e-280">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="8242e-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8242e-281">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="8242e-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="8242e-282">System-Only</span></span>            | <span data-ttu-id="8242e-283">否</span><span class="sxs-lookup"><span data-stu-id="8242e-283">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-284">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8242e-284">Is-Single-Valued</span></span>       | <span data-ttu-id="8242e-285">對</span><span class="sxs-lookup"><span data-stu-id="8242e-285">True</span></span>                                                                                  |
| <span data-ttu-id="8242e-286">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8242e-286">Is Indexed</span></span>             | <span data-ttu-id="8242e-287">否</span><span class="sxs-lookup"><span data-stu-id="8242e-287">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-288">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8242e-288">In Global Catalog</span></span>      | <span data-ttu-id="8242e-289">否</span><span class="sxs-lookup"><span data-stu-id="8242e-289">False</span></span>                                                                                 |
| <span data-ttu-id="8242e-290">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8242e-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="8242e-291">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8242e-291">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="8242e-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8242e-292">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="8242e-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8242e-293">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="8242e-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-294">Search-Flags</span></span>           | <span data-ttu-id="8242e-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8242e-295">0x00000000</span></span>                                                                            |
| <span data-ttu-id="8242e-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8242e-296">System-Flags</span></span>           | <span data-ttu-id="8242e-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8242e-297">0x00000010</span></span>                                                                            |
| <span data-ttu-id="8242e-298">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8242e-298">Classes used in</span></span>        | [<span data-ttu-id="8242e-299">**Sam-網域-基礎**</span><span class="sxs-lookup"><span data-stu-id="8242e-299">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="8242e-300">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="8242e-300">**Top**</span></span>](c-top.md)<br/> |



 

 





