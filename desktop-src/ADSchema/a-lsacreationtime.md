---
title: LSA-建立時間屬性
description: LSA-建立時間屬性是用來支援 Windows NT 4.0 網域的複寫。
ms.assetid: a5446cbf-aa35-4ea6-a2e0-9d0ea58edaf1
ms.tgt_platform: multiple
keywords:
- LSA-建立時間屬性 AD 架構
- lSACreationTime 屬性 AD 架構
topic_type:
- apiref
api_name:
- LSA-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f32092e7d71d02807f4700d381da0ce099ccaf7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385342"
---
# <a name="lsa-creation-time-attribute"></a><span data-ttu-id="50070-105">LSA-建立時間屬性</span><span class="sxs-lookup"><span data-stu-id="50070-105">LSA-Creation-Time attribute</span></span>

<span data-ttu-id="50070-106">**LSA-建立時間** 屬性是用來支援 Windows NT 4.0 網域的複寫。</span><span class="sxs-lookup"><span data-stu-id="50070-106">The **LSA-Creation-Time** attribute is used to support replication to Windows NT 4.0 domains.</span></span>



| <span data-ttu-id="50070-107">進入</span><span class="sxs-lookup"><span data-stu-id="50070-107">Entry</span></span> | <span data-ttu-id="50070-108">值</span><span class="sxs-lookup"><span data-stu-id="50070-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="50070-109">CN</span><span class="sxs-lookup"><span data-stu-id="50070-109">CN</span></span>                | <span data-ttu-id="50070-110">LSA-建立時間</span><span class="sxs-lookup"><span data-stu-id="50070-110">LSA-Creation-Time</span></span>                    |
| <span data-ttu-id="50070-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="50070-111">Ldap-Display-Name</span></span> | <span data-ttu-id="50070-112">lSACreationTime</span><span class="sxs-lookup"><span data-stu-id="50070-112">lSACreationTime</span></span>                      |
| <span data-ttu-id="50070-113">大小</span><span class="sxs-lookup"><span data-stu-id="50070-113">Size</span></span>              | <span data-ttu-id="50070-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="50070-114">8 bytes</span></span>                              |
| <span data-ttu-id="50070-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="50070-115">Update Privilege</span></span>  | <span data-ttu-id="50070-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="50070-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="50070-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="50070-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="50070-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="50070-118">Attribute-Id</span></span>      | <span data-ttu-id="50070-119">1.2.840.113556.1.4.66</span><span class="sxs-lookup"><span data-stu-id="50070-119">1.2.840.113556.1.4.66</span></span>                |
| <span data-ttu-id="50070-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="50070-120">System-Id-Guid</span></span>    | <span data-ttu-id="50070-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="50070-121">bf9679ad-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="50070-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="50070-122">Syntax</span></span>            | [<span data-ttu-id="50070-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="50070-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="50070-124">實作</span><span class="sxs-lookup"><span data-stu-id="50070-124">Implementations</span></span>

-   [<span data-ttu-id="50070-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="50070-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="50070-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="50070-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="50070-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="50070-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="50070-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="50070-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="50070-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="50070-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="50070-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="50070-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="50070-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="50070-131">Windows 2000 Server</span></span>



| <span data-ttu-id="50070-132">進入</span><span class="sxs-lookup"><span data-stu-id="50070-132">Entry</span></span> | <span data-ttu-id="50070-133">值</span><span class="sxs-lookup"><span data-stu-id="50070-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="50070-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50070-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="50070-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50070-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="50070-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="50070-136">System-Only</span></span>            | <span data-ttu-id="50070-137">否</span><span class="sxs-lookup"><span data-stu-id="50070-137">False</span></span>                                        |
| <span data-ttu-id="50070-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50070-138">Is-Single-Valued</span></span>       | <span data-ttu-id="50070-139">對</span><span class="sxs-lookup"><span data-stu-id="50070-139">True</span></span>                                         |
| <span data-ttu-id="50070-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50070-140">Is Indexed</span></span>             | <span data-ttu-id="50070-141">否</span><span class="sxs-lookup"><span data-stu-id="50070-141">False</span></span>                                        |
| <span data-ttu-id="50070-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50070-142">In Global Catalog</span></span>      | <span data-ttu-id="50070-143">否</span><span class="sxs-lookup"><span data-stu-id="50070-143">False</span></span>                                        |
| <span data-ttu-id="50070-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50070-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="50070-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50070-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="50070-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50070-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="50070-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50070-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="50070-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50070-148">Search-Flags</span></span>           | <span data-ttu-id="50070-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50070-149">0x00000000</span></span>                                   |
| <span data-ttu-id="50070-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50070-150">System-Flags</span></span>           | <span data-ttu-id="50070-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50070-151">0x00000010</span></span>                                   |
| <span data-ttu-id="50070-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50070-152">Classes used in</span></span>        | [<span data-ttu-id="50070-153">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="50070-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="50070-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="50070-154">Windows Server 2003</span></span>



| <span data-ttu-id="50070-155">進入</span><span class="sxs-lookup"><span data-stu-id="50070-155">Entry</span></span> | <span data-ttu-id="50070-156">值</span><span class="sxs-lookup"><span data-stu-id="50070-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="50070-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50070-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="50070-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50070-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="50070-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="50070-159">System-Only</span></span>            | <span data-ttu-id="50070-160">否</span><span class="sxs-lookup"><span data-stu-id="50070-160">False</span></span>                                        |
| <span data-ttu-id="50070-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50070-161">Is-Single-Valued</span></span>       | <span data-ttu-id="50070-162">對</span><span class="sxs-lookup"><span data-stu-id="50070-162">True</span></span>                                         |
| <span data-ttu-id="50070-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50070-163">Is Indexed</span></span>             | <span data-ttu-id="50070-164">否</span><span class="sxs-lookup"><span data-stu-id="50070-164">False</span></span>                                        |
| <span data-ttu-id="50070-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50070-165">In Global Catalog</span></span>      | <span data-ttu-id="50070-166">否</span><span class="sxs-lookup"><span data-stu-id="50070-166">False</span></span>                                        |
| <span data-ttu-id="50070-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50070-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="50070-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50070-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="50070-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50070-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="50070-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50070-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="50070-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50070-171">Search-Flags</span></span>           | <span data-ttu-id="50070-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50070-172">0x00000000</span></span>                                   |
| <span data-ttu-id="50070-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50070-173">System-Flags</span></span>           | <span data-ttu-id="50070-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50070-174">0x00000010</span></span>                                   |
| <span data-ttu-id="50070-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50070-175">Classes used in</span></span>        | [<span data-ttu-id="50070-176">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="50070-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="50070-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="50070-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="50070-178">進入</span><span class="sxs-lookup"><span data-stu-id="50070-178">Entry</span></span> | <span data-ttu-id="50070-179">值</span><span class="sxs-lookup"><span data-stu-id="50070-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="50070-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50070-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="50070-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50070-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="50070-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="50070-182">System-Only</span></span>            | <span data-ttu-id="50070-183">否</span><span class="sxs-lookup"><span data-stu-id="50070-183">False</span></span>                                        |
| <span data-ttu-id="50070-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50070-184">Is-Single-Valued</span></span>       | <span data-ttu-id="50070-185">對</span><span class="sxs-lookup"><span data-stu-id="50070-185">True</span></span>                                         |
| <span data-ttu-id="50070-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50070-186">Is Indexed</span></span>             | <span data-ttu-id="50070-187">否</span><span class="sxs-lookup"><span data-stu-id="50070-187">False</span></span>                                        |
| <span data-ttu-id="50070-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50070-188">In Global Catalog</span></span>      | <span data-ttu-id="50070-189">否</span><span class="sxs-lookup"><span data-stu-id="50070-189">False</span></span>                                        |
| <span data-ttu-id="50070-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50070-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="50070-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50070-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="50070-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50070-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="50070-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50070-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="50070-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50070-194">Search-Flags</span></span>           | <span data-ttu-id="50070-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50070-195">0x00000000</span></span>                                   |
| <span data-ttu-id="50070-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50070-196">System-Flags</span></span>           | <span data-ttu-id="50070-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50070-197">0x00000010</span></span>                                   |
| <span data-ttu-id="50070-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50070-198">Classes used in</span></span>        | [<span data-ttu-id="50070-199">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="50070-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="50070-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50070-200">Windows Server 2008</span></span>



| <span data-ttu-id="50070-201">進入</span><span class="sxs-lookup"><span data-stu-id="50070-201">Entry</span></span> | <span data-ttu-id="50070-202">值</span><span class="sxs-lookup"><span data-stu-id="50070-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="50070-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50070-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="50070-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50070-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="50070-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="50070-205">System-Only</span></span>            | <span data-ttu-id="50070-206">否</span><span class="sxs-lookup"><span data-stu-id="50070-206">False</span></span>                                        |
| <span data-ttu-id="50070-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50070-207">Is-Single-Valued</span></span>       | <span data-ttu-id="50070-208">對</span><span class="sxs-lookup"><span data-stu-id="50070-208">True</span></span>                                         |
| <span data-ttu-id="50070-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50070-209">Is Indexed</span></span>             | <span data-ttu-id="50070-210">否</span><span class="sxs-lookup"><span data-stu-id="50070-210">False</span></span>                                        |
| <span data-ttu-id="50070-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50070-211">In Global Catalog</span></span>      | <span data-ttu-id="50070-212">否</span><span class="sxs-lookup"><span data-stu-id="50070-212">False</span></span>                                        |
| <span data-ttu-id="50070-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50070-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="50070-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50070-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="50070-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50070-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="50070-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50070-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="50070-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50070-217">Search-Flags</span></span>           | <span data-ttu-id="50070-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50070-218">0x00000000</span></span>                                   |
| <span data-ttu-id="50070-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50070-219">System-Flags</span></span>           | <span data-ttu-id="50070-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50070-220">0x00000010</span></span>                                   |
| <span data-ttu-id="50070-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50070-221">Classes used in</span></span>        | [<span data-ttu-id="50070-222">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="50070-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="50070-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50070-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="50070-224">進入</span><span class="sxs-lookup"><span data-stu-id="50070-224">Entry</span></span> | <span data-ttu-id="50070-225">值</span><span class="sxs-lookup"><span data-stu-id="50070-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="50070-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50070-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="50070-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50070-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="50070-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="50070-228">System-Only</span></span>            | <span data-ttu-id="50070-229">否</span><span class="sxs-lookup"><span data-stu-id="50070-229">False</span></span>                                        |
| <span data-ttu-id="50070-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50070-230">Is-Single-Valued</span></span>       | <span data-ttu-id="50070-231">對</span><span class="sxs-lookup"><span data-stu-id="50070-231">True</span></span>                                         |
| <span data-ttu-id="50070-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50070-232">Is Indexed</span></span>             | <span data-ttu-id="50070-233">否</span><span class="sxs-lookup"><span data-stu-id="50070-233">False</span></span>                                        |
| <span data-ttu-id="50070-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50070-234">In Global Catalog</span></span>      | <span data-ttu-id="50070-235">否</span><span class="sxs-lookup"><span data-stu-id="50070-235">False</span></span>                                        |
| <span data-ttu-id="50070-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50070-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="50070-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50070-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="50070-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50070-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="50070-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50070-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="50070-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50070-240">Search-Flags</span></span>           | <span data-ttu-id="50070-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50070-241">0x00000000</span></span>                                   |
| <span data-ttu-id="50070-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50070-242">System-Flags</span></span>           | <span data-ttu-id="50070-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50070-243">0x00000010</span></span>                                   |
| <span data-ttu-id="50070-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50070-244">Classes used in</span></span>        | [<span data-ttu-id="50070-245">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="50070-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="50070-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50070-246">Windows Server 2012</span></span>



| <span data-ttu-id="50070-247">進入</span><span class="sxs-lookup"><span data-stu-id="50070-247">Entry</span></span> | <span data-ttu-id="50070-248">值</span><span class="sxs-lookup"><span data-stu-id="50070-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="50070-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="50070-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="50070-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="50070-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="50070-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="50070-251">System-Only</span></span>            | <span data-ttu-id="50070-252">否</span><span class="sxs-lookup"><span data-stu-id="50070-252">False</span></span>                                        |
| <span data-ttu-id="50070-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="50070-253">Is-Single-Valued</span></span>       | <span data-ttu-id="50070-254">對</span><span class="sxs-lookup"><span data-stu-id="50070-254">True</span></span>                                         |
| <span data-ttu-id="50070-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="50070-255">Is Indexed</span></span>             | <span data-ttu-id="50070-256">否</span><span class="sxs-lookup"><span data-stu-id="50070-256">False</span></span>                                        |
| <span data-ttu-id="50070-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="50070-257">In Global Catalog</span></span>      | <span data-ttu-id="50070-258">否</span><span class="sxs-lookup"><span data-stu-id="50070-258">False</span></span>                                        |
| <span data-ttu-id="50070-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="50070-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="50070-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="50070-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="50070-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="50070-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="50070-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="50070-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="50070-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="50070-263">Search-Flags</span></span>           | <span data-ttu-id="50070-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="50070-264">0x00000000</span></span>                                   |
| <span data-ttu-id="50070-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="50070-265">System-Flags</span></span>           | <span data-ttu-id="50070-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="50070-266">0x00000010</span></span>                                   |
| <span data-ttu-id="50070-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="50070-267">Classes used in</span></span>        | [<span data-ttu-id="50070-268">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="50070-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





