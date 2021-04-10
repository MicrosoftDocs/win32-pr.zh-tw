---
title: MSMQ-Sites 屬性
description: 電腦所屬的網站清單 (網站 objectGUIDs 的陣列，通常不能有一個以上的 GUID) 。
ms.assetid: 0f6cfc3a-9edb-4291-a5df-06c0f1a6add8
ms.tgt_platform: multiple
keywords:
- MSMQ-Sites 屬性 AD 架構
- mSMQSites 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Sites
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47512a20301f3b1dca96c86efe604b0eacc4a73e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935528"
---
# <a name="msmq-sites-attribute"></a><span data-ttu-id="42c2d-105">MSMQ-Sites 屬性</span><span class="sxs-lookup"><span data-stu-id="42c2d-105">MSMQ-Sites attribute</span></span>

<span data-ttu-id="42c2d-106">電腦所屬的網站清單 (網站 objectGUIDs 的陣列，通常不能有一個以上的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="42c2d-106">The list of sites that the computer belongs to (an array of the sites' objectGUIDs, usually not more than one GUID).</span></span>



| <span data-ttu-id="42c2d-107">進入</span><span class="sxs-lookup"><span data-stu-id="42c2d-107">Entry</span></span> | <span data-ttu-id="42c2d-108">值</span><span class="sxs-lookup"><span data-stu-id="42c2d-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="42c2d-109">CN</span><span class="sxs-lookup"><span data-stu-id="42c2d-109">CN</span></span>                | <span data-ttu-id="42c2d-110">MSMQ-Sites</span><span class="sxs-lookup"><span data-stu-id="42c2d-110">MSMQ-Sites</span></span>                                            |
| <span data-ttu-id="42c2d-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="42c2d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="42c2d-112">mSMQSites</span><span class="sxs-lookup"><span data-stu-id="42c2d-112">mSMQSites</span></span>                                             |
| <span data-ttu-id="42c2d-113">大小</span><span class="sxs-lookup"><span data-stu-id="42c2d-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="42c2d-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="42c2d-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="42c2d-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="42c2d-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="42c2d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="42c2d-116">Attribute-Id</span></span>      | <span data-ttu-id="42c2d-117">1.2.840.113556.1.4.927</span><span class="sxs-lookup"><span data-stu-id="42c2d-117">1.2.840.113556.1.4.927</span></span>                                |
| <span data-ttu-id="42c2d-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="42c2d-118">System-Id-Guid</span></span>    | <span data-ttu-id="42c2d-119">9a0dc32a-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="42c2d-119">9a0dc32a-c100-11d1-bbc5-0080c76670c0</span></span>                  |
| <span data-ttu-id="42c2d-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="42c2d-120">Syntax</span></span>            | [<span data-ttu-id="42c2d-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="42c2d-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="42c2d-122">實作</span><span class="sxs-lookup"><span data-stu-id="42c2d-122">Implementations</span></span>

-   [<span data-ttu-id="42c2d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="42c2d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="42c2d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="42c2d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="42c2d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="42c2d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="42c2d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="42c2d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="42c2d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="42c2d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="42c2d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="42c2d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="42c2d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="42c2d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="42c2d-130">進入</span><span class="sxs-lookup"><span data-stu-id="42c2d-130">Entry</span></span> | <span data-ttu-id="42c2d-131">值</span><span class="sxs-lookup"><span data-stu-id="42c2d-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="42c2d-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42c2d-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="42c2d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42c2d-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="42c2d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="42c2d-134">System-Only</span></span>            | <span data-ttu-id="42c2d-135">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-135">False</span></span>                                                        |
| <span data-ttu-id="42c2d-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42c2d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="42c2d-137">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-137">False</span></span>                                                        |
| <span data-ttu-id="42c2d-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42c2d-138">Is Indexed</span></span>             | <span data-ttu-id="42c2d-139">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-139">False</span></span>                                                        |
| <span data-ttu-id="42c2d-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42c2d-140">In Global Catalog</span></span>      | <span data-ttu-id="42c2d-141">對</span><span class="sxs-lookup"><span data-stu-id="42c2d-141">True</span></span>                                                         |
| <span data-ttu-id="42c2d-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42c2d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="42c2d-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42c2d-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="42c2d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42c2d-144">Range-Lower</span></span>            | <span data-ttu-id="42c2d-145">16</span><span class="sxs-lookup"><span data-stu-id="42c2d-145">16</span></span>                                                           |
| <span data-ttu-id="42c2d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42c2d-146">Range-Upper</span></span>            | <span data-ttu-id="42c2d-147">16</span><span class="sxs-lookup"><span data-stu-id="42c2d-147">16</span></span>                                                           |
| <span data-ttu-id="42c2d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42c2d-148">Search-Flags</span></span>           | <span data-ttu-id="42c2d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42c2d-149">0x00000000</span></span>                                                   |
| <span data-ttu-id="42c2d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42c2d-150">System-Flags</span></span>           | <span data-ttu-id="42c2d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42c2d-151">0x00000010</span></span>                                                   |
| <span data-ttu-id="42c2d-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42c2d-152">Classes used in</span></span>        | [<span data-ttu-id="42c2d-153">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="42c2d-153">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="42c2d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42c2d-154">Windows Server 2003</span></span>



| <span data-ttu-id="42c2d-155">進入</span><span class="sxs-lookup"><span data-stu-id="42c2d-155">Entry</span></span> | <span data-ttu-id="42c2d-156">值</span><span class="sxs-lookup"><span data-stu-id="42c2d-156">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="42c2d-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42c2d-157">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="42c2d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42c2d-158">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="42c2d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="42c2d-159">System-Only</span></span>            | <span data-ttu-id="42c2d-160">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-160">False</span></span>                                                        |
| <span data-ttu-id="42c2d-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42c2d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="42c2d-162">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-162">False</span></span>                                                        |
| <span data-ttu-id="42c2d-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42c2d-163">Is Indexed</span></span>             | <span data-ttu-id="42c2d-164">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-164">False</span></span>                                                        |
| <span data-ttu-id="42c2d-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42c2d-165">In Global Catalog</span></span>      | <span data-ttu-id="42c2d-166">對</span><span class="sxs-lookup"><span data-stu-id="42c2d-166">True</span></span>                                                         |
| <span data-ttu-id="42c2d-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42c2d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="42c2d-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42c2d-168">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="42c2d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42c2d-169">Range-Lower</span></span>            | <span data-ttu-id="42c2d-170">16</span><span class="sxs-lookup"><span data-stu-id="42c2d-170">16</span></span>                                                           |
| <span data-ttu-id="42c2d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42c2d-171">Range-Upper</span></span>            | <span data-ttu-id="42c2d-172">16</span><span class="sxs-lookup"><span data-stu-id="42c2d-172">16</span></span>                                                           |
| <span data-ttu-id="42c2d-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42c2d-173">Search-Flags</span></span>           | <span data-ttu-id="42c2d-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42c2d-174">0x00000000</span></span>                                                   |
| <span data-ttu-id="42c2d-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42c2d-175">System-Flags</span></span>           | <span data-ttu-id="42c2d-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42c2d-176">0x00000010</span></span>                                                   |
| <span data-ttu-id="42c2d-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42c2d-177">Classes used in</span></span>        | [<span data-ttu-id="42c2d-178">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="42c2d-178">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="42c2d-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="42c2d-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="42c2d-180">進入</span><span class="sxs-lookup"><span data-stu-id="42c2d-180">Entry</span></span> | <span data-ttu-id="42c2d-181">值</span><span class="sxs-lookup"><span data-stu-id="42c2d-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="42c2d-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42c2d-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="42c2d-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42c2d-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="42c2d-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="42c2d-184">System-Only</span></span>            | <span data-ttu-id="42c2d-185">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-185">False</span></span>                                                        |
| <span data-ttu-id="42c2d-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42c2d-186">Is-Single-Valued</span></span>       | <span data-ttu-id="42c2d-187">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-187">False</span></span>                                                        |
| <span data-ttu-id="42c2d-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42c2d-188">Is Indexed</span></span>             | <span data-ttu-id="42c2d-189">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-189">False</span></span>                                                        |
| <span data-ttu-id="42c2d-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42c2d-190">In Global Catalog</span></span>      | <span data-ttu-id="42c2d-191">對</span><span class="sxs-lookup"><span data-stu-id="42c2d-191">True</span></span>                                                         |
| <span data-ttu-id="42c2d-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42c2d-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="42c2d-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42c2d-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="42c2d-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42c2d-194">Range-Lower</span></span>            | <span data-ttu-id="42c2d-195">16</span><span class="sxs-lookup"><span data-stu-id="42c2d-195">16</span></span>                                                           |
| <span data-ttu-id="42c2d-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42c2d-196">Range-Upper</span></span>            | <span data-ttu-id="42c2d-197">16</span><span class="sxs-lookup"><span data-stu-id="42c2d-197">16</span></span>                                                           |
| <span data-ttu-id="42c2d-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42c2d-198">Search-Flags</span></span>           | <span data-ttu-id="42c2d-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42c2d-199">0x00000000</span></span>                                                   |
| <span data-ttu-id="42c2d-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42c2d-200">System-Flags</span></span>           | <span data-ttu-id="42c2d-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42c2d-201">0x00000010</span></span>                                                   |
| <span data-ttu-id="42c2d-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42c2d-202">Classes used in</span></span>        | [<span data-ttu-id="42c2d-203">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="42c2d-203">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="42c2d-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42c2d-204">Windows Server 2008</span></span>



| <span data-ttu-id="42c2d-205">進入</span><span class="sxs-lookup"><span data-stu-id="42c2d-205">Entry</span></span> | <span data-ttu-id="42c2d-206">值</span><span class="sxs-lookup"><span data-stu-id="42c2d-206">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="42c2d-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42c2d-207">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="42c2d-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42c2d-208">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="42c2d-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="42c2d-209">System-Only</span></span>            | <span data-ttu-id="42c2d-210">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-210">False</span></span>                                                        |
| <span data-ttu-id="42c2d-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42c2d-211">Is-Single-Valued</span></span>       | <span data-ttu-id="42c2d-212">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-212">False</span></span>                                                        |
| <span data-ttu-id="42c2d-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42c2d-213">Is Indexed</span></span>             | <span data-ttu-id="42c2d-214">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-214">False</span></span>                                                        |
| <span data-ttu-id="42c2d-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42c2d-215">In Global Catalog</span></span>      | <span data-ttu-id="42c2d-216">對</span><span class="sxs-lookup"><span data-stu-id="42c2d-216">True</span></span>                                                         |
| <span data-ttu-id="42c2d-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42c2d-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="42c2d-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42c2d-218">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="42c2d-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42c2d-219">Range-Lower</span></span>            | <span data-ttu-id="42c2d-220">16</span><span class="sxs-lookup"><span data-stu-id="42c2d-220">16</span></span>                                                           |
| <span data-ttu-id="42c2d-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42c2d-221">Range-Upper</span></span>            | <span data-ttu-id="42c2d-222">16</span><span class="sxs-lookup"><span data-stu-id="42c2d-222">16</span></span>                                                           |
| <span data-ttu-id="42c2d-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42c2d-223">Search-Flags</span></span>           | <span data-ttu-id="42c2d-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42c2d-224">0x00000000</span></span>                                                   |
| <span data-ttu-id="42c2d-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42c2d-225">System-Flags</span></span>           | <span data-ttu-id="42c2d-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42c2d-226">0x00000010</span></span>                                                   |
| <span data-ttu-id="42c2d-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42c2d-227">Classes used in</span></span>        | [<span data-ttu-id="42c2d-228">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="42c2d-228">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="42c2d-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42c2d-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="42c2d-230">進入</span><span class="sxs-lookup"><span data-stu-id="42c2d-230">Entry</span></span> | <span data-ttu-id="42c2d-231">值</span><span class="sxs-lookup"><span data-stu-id="42c2d-231">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="42c2d-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42c2d-232">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="42c2d-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42c2d-233">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="42c2d-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="42c2d-234">System-Only</span></span>            | <span data-ttu-id="42c2d-235">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-235">False</span></span>                                                        |
| <span data-ttu-id="42c2d-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42c2d-236">Is-Single-Valued</span></span>       | <span data-ttu-id="42c2d-237">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-237">False</span></span>                                                        |
| <span data-ttu-id="42c2d-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42c2d-238">Is Indexed</span></span>             | <span data-ttu-id="42c2d-239">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-239">False</span></span>                                                        |
| <span data-ttu-id="42c2d-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42c2d-240">In Global Catalog</span></span>      | <span data-ttu-id="42c2d-241">對</span><span class="sxs-lookup"><span data-stu-id="42c2d-241">True</span></span>                                                         |
| <span data-ttu-id="42c2d-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42c2d-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="42c2d-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42c2d-243">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="42c2d-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42c2d-244">Range-Lower</span></span>            | <span data-ttu-id="42c2d-245">16</span><span class="sxs-lookup"><span data-stu-id="42c2d-245">16</span></span>                                                           |
| <span data-ttu-id="42c2d-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42c2d-246">Range-Upper</span></span>            | <span data-ttu-id="42c2d-247">16</span><span class="sxs-lookup"><span data-stu-id="42c2d-247">16</span></span>                                                           |
| <span data-ttu-id="42c2d-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42c2d-248">Search-Flags</span></span>           | <span data-ttu-id="42c2d-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42c2d-249">0x00000000</span></span>                                                   |
| <span data-ttu-id="42c2d-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42c2d-250">System-Flags</span></span>           | <span data-ttu-id="42c2d-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42c2d-251">0x00000010</span></span>                                                   |
| <span data-ttu-id="42c2d-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42c2d-252">Classes used in</span></span>        | [<span data-ttu-id="42c2d-253">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="42c2d-253">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="42c2d-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42c2d-254">Windows Server 2012</span></span>



| <span data-ttu-id="42c2d-255">進入</span><span class="sxs-lookup"><span data-stu-id="42c2d-255">Entry</span></span> | <span data-ttu-id="42c2d-256">值</span><span class="sxs-lookup"><span data-stu-id="42c2d-256">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="42c2d-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="42c2d-257">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="42c2d-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42c2d-258">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="42c2d-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="42c2d-259">System-Only</span></span>            | <span data-ttu-id="42c2d-260">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-260">False</span></span>                                                        |
| <span data-ttu-id="42c2d-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="42c2d-261">Is-Single-Valued</span></span>       | <span data-ttu-id="42c2d-262">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-262">False</span></span>                                                        |
| <span data-ttu-id="42c2d-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="42c2d-263">Is Indexed</span></span>             | <span data-ttu-id="42c2d-264">否</span><span class="sxs-lookup"><span data-stu-id="42c2d-264">False</span></span>                                                        |
| <span data-ttu-id="42c2d-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="42c2d-265">In Global Catalog</span></span>      | <span data-ttu-id="42c2d-266">對</span><span class="sxs-lookup"><span data-stu-id="42c2d-266">True</span></span>                                                         |
| <span data-ttu-id="42c2d-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="42c2d-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="42c2d-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="42c2d-268">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="42c2d-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42c2d-269">Range-Lower</span></span>            | <span data-ttu-id="42c2d-270">16</span><span class="sxs-lookup"><span data-stu-id="42c2d-270">16</span></span>                                                           |
| <span data-ttu-id="42c2d-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42c2d-271">Range-Upper</span></span>            | <span data-ttu-id="42c2d-272">16</span><span class="sxs-lookup"><span data-stu-id="42c2d-272">16</span></span>                                                           |
| <span data-ttu-id="42c2d-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42c2d-273">Search-Flags</span></span>           | <span data-ttu-id="42c2d-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42c2d-274">0x00000000</span></span>                                                   |
| <span data-ttu-id="42c2d-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42c2d-275">System-Flags</span></span>           | <span data-ttu-id="42c2d-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42c2d-276">0x00000010</span></span>                                                   |
| <span data-ttu-id="42c2d-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="42c2d-277">Classes used in</span></span>        | [<span data-ttu-id="42c2d-278">**MSMQ-設定**</span><span class="sxs-lookup"><span data-stu-id="42c2d-278">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





