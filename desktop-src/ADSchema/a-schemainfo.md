---
title: Schema-Info 屬性
description: 內部二進位值，用來偵測 Dc 之間的架構變更，並在複寫任何其他 NC 之前強制執行架構 NC 複寫週期。 在架構 FSMO 被佔用時用來解析系結，並在一個以上的 DC 上進行變更。
ms.assetid: 416cef3f-211b-439d-b177-267806c6a5d2
ms.tgt_platform: multiple
keywords:
- Schema-Info 屬性 AD 架構
- schemaInfo 屬性 AD 架構
topic_type:
- apiref
api_name:
- Schema-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca55fc8ad3f53709b3819a7333e3470a1ac35cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509668"
---
# <a name="schema-info-attribute"></a><span data-ttu-id="86e3a-106">Schema-Info 屬性</span><span class="sxs-lookup"><span data-stu-id="86e3a-106">Schema-Info attribute</span></span>

<span data-ttu-id="86e3a-107">內部二進位值，用來偵測 Dc 之間的架構變更，並在複寫任何其他 NC 之前強制執行架構 NC 複寫週期。</span><span class="sxs-lookup"><span data-stu-id="86e3a-107">An internal binary value used to detect schema changes between DCs and force a schema NC replication cycle before replicating any other NC.</span></span> <span data-ttu-id="86e3a-108">在架構 FSMO 被佔用時用來解析系結，並在一個以上的 DC 上進行變更。</span><span class="sxs-lookup"><span data-stu-id="86e3a-108">Used to resolve ties when the schema FSMO is seized and a change is made on more than one DC.</span></span>



| <span data-ttu-id="86e3a-109">進入</span><span class="sxs-lookup"><span data-stu-id="86e3a-109">Entry</span></span> | <span data-ttu-id="86e3a-110">值</span><span class="sxs-lookup"><span data-stu-id="86e3a-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="86e3a-111">CN</span><span class="sxs-lookup"><span data-stu-id="86e3a-111">CN</span></span>                | <span data-ttu-id="86e3a-112">Schema-Info</span><span class="sxs-lookup"><span data-stu-id="86e3a-112">Schema-Info</span></span>                                           |
| <span data-ttu-id="86e3a-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="86e3a-113">Ldap-Display-Name</span></span> | <span data-ttu-id="86e3a-114">schemaInfo</span><span class="sxs-lookup"><span data-stu-id="86e3a-114">schemaInfo</span></span>                                            |
| <span data-ttu-id="86e3a-115">大小</span><span class="sxs-lookup"><span data-stu-id="86e3a-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="86e3a-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="86e3a-116">Update Privilege</span></span>  | <span data-ttu-id="86e3a-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="86e3a-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="86e3a-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="86e3a-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="86e3a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="86e3a-119">Attribute-Id</span></span>      | <span data-ttu-id="86e3a-120">1.2.840.113556.1.4.1358</span><span class="sxs-lookup"><span data-stu-id="86e3a-120">1.2.840.113556.1.4.1358</span></span>                               |
| <span data-ttu-id="86e3a-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="86e3a-121">System-Id-Guid</span></span>    | <span data-ttu-id="86e3a-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="86e3a-122">f9fb64ae-93b4-11d2-9945-0000f87a57d4</span></span>                  |
| <span data-ttu-id="86e3a-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="86e3a-123">Syntax</span></span>            | [<span data-ttu-id="86e3a-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="86e3a-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="86e3a-125">實作</span><span class="sxs-lookup"><span data-stu-id="86e3a-125">Implementations</span></span>

-   [<span data-ttu-id="86e3a-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="86e3a-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="86e3a-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="86e3a-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="86e3a-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="86e3a-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="86e3a-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="86e3a-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="86e3a-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="86e3a-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="86e3a-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="86e3a-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="86e3a-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="86e3a-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="86e3a-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="86e3a-133">Windows 2000 Server</span></span>



| <span data-ttu-id="86e3a-134">進入</span><span class="sxs-lookup"><span data-stu-id="86e3a-134">Entry</span></span> | <span data-ttu-id="86e3a-135">值</span><span class="sxs-lookup"><span data-stu-id="86e3a-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86e3a-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="86e3a-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e3a-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e3a-138">System-Only</span></span>            | <span data-ttu-id="86e3a-139">對</span><span class="sxs-lookup"><span data-stu-id="86e3a-139">True</span></span>                            |
| <span data-ttu-id="86e3a-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="86e3a-140">Is-Single-Valued</span></span>       | <span data-ttu-id="86e3a-141">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-141">False</span></span>                           |
| <span data-ttu-id="86e3a-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="86e3a-142">Is Indexed</span></span>             | <span data-ttu-id="86e3a-143">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-143">False</span></span>                           |
| <span data-ttu-id="86e3a-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="86e3a-144">In Global Catalog</span></span>      | <span data-ttu-id="86e3a-145">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-145">False</span></span>                           |
| <span data-ttu-id="86e3a-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="86e3a-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e3a-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="86e3a-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86e3a-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e3a-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="86e3a-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e3a-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="86e3a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-150">Search-Flags</span></span>           | <span data-ttu-id="86e3a-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e3a-151">0x00000000</span></span>                      |
| <span data-ttu-id="86e3a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-152">System-Flags</span></span>           | <span data-ttu-id="86e3a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e3a-153">0x00000010</span></span>                      |
| <span data-ttu-id="86e3a-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="86e3a-154">Classes used in</span></span>        | [<span data-ttu-id="86e3a-155">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="86e3a-155">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="86e3a-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="86e3a-156">Windows Server 2003</span></span>



| <span data-ttu-id="86e3a-157">進入</span><span class="sxs-lookup"><span data-stu-id="86e3a-157">Entry</span></span> | <span data-ttu-id="86e3a-158">值</span><span class="sxs-lookup"><span data-stu-id="86e3a-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86e3a-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="86e3a-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e3a-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e3a-161">System-Only</span></span>            | <span data-ttu-id="86e3a-162">對</span><span class="sxs-lookup"><span data-stu-id="86e3a-162">True</span></span>                            |
| <span data-ttu-id="86e3a-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="86e3a-163">Is-Single-Valued</span></span>       | <span data-ttu-id="86e3a-164">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-164">False</span></span>                           |
| <span data-ttu-id="86e3a-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="86e3a-165">Is Indexed</span></span>             | <span data-ttu-id="86e3a-166">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-166">False</span></span>                           |
| <span data-ttu-id="86e3a-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="86e3a-167">In Global Catalog</span></span>      | <span data-ttu-id="86e3a-168">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-168">False</span></span>                           |
| <span data-ttu-id="86e3a-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="86e3a-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e3a-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="86e3a-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86e3a-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e3a-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="86e3a-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e3a-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="86e3a-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-173">Search-Flags</span></span>           | <span data-ttu-id="86e3a-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e3a-174">0x00000000</span></span>                      |
| <span data-ttu-id="86e3a-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-175">System-Flags</span></span>           | <span data-ttu-id="86e3a-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e3a-176">0x00000010</span></span>                      |
| <span data-ttu-id="86e3a-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="86e3a-177">Classes used in</span></span>        | [<span data-ttu-id="86e3a-178">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="86e3a-178">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="86e3a-179">亞當</span><span class="sxs-lookup"><span data-stu-id="86e3a-179">ADAM</span></span>



| <span data-ttu-id="86e3a-180">進入</span><span class="sxs-lookup"><span data-stu-id="86e3a-180">Entry</span></span> | <span data-ttu-id="86e3a-181">值</span><span class="sxs-lookup"><span data-stu-id="86e3a-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86e3a-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="86e3a-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e3a-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e3a-184">System-Only</span></span>            | <span data-ttu-id="86e3a-185">對</span><span class="sxs-lookup"><span data-stu-id="86e3a-185">True</span></span>                            |
| <span data-ttu-id="86e3a-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="86e3a-186">Is-Single-Valued</span></span>       | <span data-ttu-id="86e3a-187">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-187">False</span></span>                           |
| <span data-ttu-id="86e3a-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="86e3a-188">Is Indexed</span></span>             | <span data-ttu-id="86e3a-189">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-189">False</span></span>                           |
| <span data-ttu-id="86e3a-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="86e3a-190">In Global Catalog</span></span>      | <span data-ttu-id="86e3a-191">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-191">False</span></span>                           |
| <span data-ttu-id="86e3a-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="86e3a-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e3a-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="86e3a-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86e3a-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e3a-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="86e3a-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e3a-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="86e3a-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-196">Search-Flags</span></span>           | <span data-ttu-id="86e3a-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e3a-197">0x00000000</span></span>                      |
| <span data-ttu-id="86e3a-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-198">System-Flags</span></span>           | <span data-ttu-id="86e3a-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e3a-199">0x00000010</span></span>                      |
| <span data-ttu-id="86e3a-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="86e3a-200">Classes used in</span></span>        | [<span data-ttu-id="86e3a-201">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="86e3a-201">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="86e3a-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="86e3a-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="86e3a-203">進入</span><span class="sxs-lookup"><span data-stu-id="86e3a-203">Entry</span></span> | <span data-ttu-id="86e3a-204">值</span><span class="sxs-lookup"><span data-stu-id="86e3a-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86e3a-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="86e3a-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e3a-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e3a-207">System-Only</span></span>            | <span data-ttu-id="86e3a-208">對</span><span class="sxs-lookup"><span data-stu-id="86e3a-208">True</span></span>                            |
| <span data-ttu-id="86e3a-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="86e3a-209">Is-Single-Valued</span></span>       | <span data-ttu-id="86e3a-210">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-210">False</span></span>                           |
| <span data-ttu-id="86e3a-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="86e3a-211">Is Indexed</span></span>             | <span data-ttu-id="86e3a-212">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-212">False</span></span>                           |
| <span data-ttu-id="86e3a-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="86e3a-213">In Global Catalog</span></span>      | <span data-ttu-id="86e3a-214">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-214">False</span></span>                           |
| <span data-ttu-id="86e3a-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="86e3a-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e3a-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="86e3a-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86e3a-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e3a-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="86e3a-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e3a-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="86e3a-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-219">Search-Flags</span></span>           | <span data-ttu-id="86e3a-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e3a-220">0x00000000</span></span>                      |
| <span data-ttu-id="86e3a-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-221">System-Flags</span></span>           | <span data-ttu-id="86e3a-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e3a-222">0x00000010</span></span>                      |
| <span data-ttu-id="86e3a-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="86e3a-223">Classes used in</span></span>        | [<span data-ttu-id="86e3a-224">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="86e3a-224">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="86e3a-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86e3a-225">Windows Server 2008</span></span>



| <span data-ttu-id="86e3a-226">進入</span><span class="sxs-lookup"><span data-stu-id="86e3a-226">Entry</span></span> | <span data-ttu-id="86e3a-227">值</span><span class="sxs-lookup"><span data-stu-id="86e3a-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86e3a-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="86e3a-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e3a-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e3a-230">System-Only</span></span>            | <span data-ttu-id="86e3a-231">對</span><span class="sxs-lookup"><span data-stu-id="86e3a-231">True</span></span>                            |
| <span data-ttu-id="86e3a-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="86e3a-232">Is-Single-Valued</span></span>       | <span data-ttu-id="86e3a-233">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-233">False</span></span>                           |
| <span data-ttu-id="86e3a-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="86e3a-234">Is Indexed</span></span>             | <span data-ttu-id="86e3a-235">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-235">False</span></span>                           |
| <span data-ttu-id="86e3a-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="86e3a-236">In Global Catalog</span></span>      | <span data-ttu-id="86e3a-237">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-237">False</span></span>                           |
| <span data-ttu-id="86e3a-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="86e3a-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e3a-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="86e3a-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86e3a-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e3a-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="86e3a-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e3a-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="86e3a-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-242">Search-Flags</span></span>           | <span data-ttu-id="86e3a-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e3a-243">0x00000000</span></span>                      |
| <span data-ttu-id="86e3a-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-244">System-Flags</span></span>           | <span data-ttu-id="86e3a-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e3a-245">0x00000010</span></span>                      |
| <span data-ttu-id="86e3a-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="86e3a-246">Classes used in</span></span>        | [<span data-ttu-id="86e3a-247">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="86e3a-247">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="86e3a-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="86e3a-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="86e3a-249">進入</span><span class="sxs-lookup"><span data-stu-id="86e3a-249">Entry</span></span> | <span data-ttu-id="86e3a-250">值</span><span class="sxs-lookup"><span data-stu-id="86e3a-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86e3a-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="86e3a-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e3a-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e3a-253">System-Only</span></span>            | <span data-ttu-id="86e3a-254">對</span><span class="sxs-lookup"><span data-stu-id="86e3a-254">True</span></span>                            |
| <span data-ttu-id="86e3a-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="86e3a-255">Is-Single-Valued</span></span>       | <span data-ttu-id="86e3a-256">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-256">False</span></span>                           |
| <span data-ttu-id="86e3a-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="86e3a-257">Is Indexed</span></span>             | <span data-ttu-id="86e3a-258">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-258">False</span></span>                           |
| <span data-ttu-id="86e3a-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="86e3a-259">In Global Catalog</span></span>      | <span data-ttu-id="86e3a-260">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-260">False</span></span>                           |
| <span data-ttu-id="86e3a-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="86e3a-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e3a-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="86e3a-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86e3a-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e3a-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="86e3a-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e3a-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="86e3a-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-265">Search-Flags</span></span>           | <span data-ttu-id="86e3a-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e3a-266">0x00000000</span></span>                      |
| <span data-ttu-id="86e3a-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-267">System-Flags</span></span>           | <span data-ttu-id="86e3a-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e3a-268">0x00000010</span></span>                      |
| <span data-ttu-id="86e3a-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="86e3a-269">Classes used in</span></span>        | [<span data-ttu-id="86e3a-270">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="86e3a-270">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="86e3a-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="86e3a-271">Windows Server 2012</span></span>



| <span data-ttu-id="86e3a-272">進入</span><span class="sxs-lookup"><span data-stu-id="86e3a-272">Entry</span></span> | <span data-ttu-id="86e3a-273">值</span><span class="sxs-lookup"><span data-stu-id="86e3a-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="86e3a-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="86e3a-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="86e3a-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="86e3a-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="86e3a-276">System-Only</span></span>            | <span data-ttu-id="86e3a-277">對</span><span class="sxs-lookup"><span data-stu-id="86e3a-277">True</span></span>                            |
| <span data-ttu-id="86e3a-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="86e3a-278">Is-Single-Valued</span></span>       | <span data-ttu-id="86e3a-279">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-279">False</span></span>                           |
| <span data-ttu-id="86e3a-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="86e3a-280">Is Indexed</span></span>             | <span data-ttu-id="86e3a-281">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-281">False</span></span>                           |
| <span data-ttu-id="86e3a-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="86e3a-282">In Global Catalog</span></span>      | <span data-ttu-id="86e3a-283">否</span><span class="sxs-lookup"><span data-stu-id="86e3a-283">False</span></span>                           |
| <span data-ttu-id="86e3a-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="86e3a-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="86e3a-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="86e3a-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="86e3a-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="86e3a-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="86e3a-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="86e3a-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="86e3a-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-288">Search-Flags</span></span>           | <span data-ttu-id="86e3a-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86e3a-289">0x00000000</span></span>                      |
| <span data-ttu-id="86e3a-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="86e3a-290">System-Flags</span></span>           | <span data-ttu-id="86e3a-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86e3a-291">0x00000010</span></span>                      |
| <span data-ttu-id="86e3a-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="86e3a-292">Classes used in</span></span>        | [<span data-ttu-id="86e3a-293">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="86e3a-293">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





