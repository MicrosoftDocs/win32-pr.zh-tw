---
title: 簡短伺服器名稱屬性
description: 適用于列印伺服器的 Windows 2000 相容伺服器名稱。
ms.assetid: 639704f4-e2b6-43e1-9b1b-6afffe8f0f6a
ms.tgt_platform: multiple
keywords:
- 簡短伺服器名稱屬性 AD 架構
- shortServerName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Short-Server-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e71b7cf5687b530bf76c673187d5152089d885d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935486"
---
# <a name="short-server-name-attribute"></a><span data-ttu-id="dc70b-105">簡短伺服器名稱屬性</span><span class="sxs-lookup"><span data-stu-id="dc70b-105">Short-Server-Name attribute</span></span>

<span data-ttu-id="dc70b-106">適用于列印伺服器的 Windows 2000 相容伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="dc70b-106">Pre-Windows 2000 compatible server name for print servers.</span></span>



| <span data-ttu-id="dc70b-107">進入</span><span class="sxs-lookup"><span data-stu-id="dc70b-107">Entry</span></span> | <span data-ttu-id="dc70b-108">值</span><span class="sxs-lookup"><span data-stu-id="dc70b-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="dc70b-109">CN</span><span class="sxs-lookup"><span data-stu-id="dc70b-109">CN</span></span>                | <span data-ttu-id="dc70b-110">簡短伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="dc70b-110">Short-Server-Name</span></span>                           |
| <span data-ttu-id="dc70b-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="dc70b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dc70b-112">shortServerName</span><span class="sxs-lookup"><span data-stu-id="dc70b-112">shortServerName</span></span>                             |
| <span data-ttu-id="dc70b-113">大小</span><span class="sxs-lookup"><span data-stu-id="dc70b-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="dc70b-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="dc70b-114">Update Privilege</span></span>  | <span data-ttu-id="dc70b-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="dc70b-115">Domain administrator</span></span>                        |
| <span data-ttu-id="dc70b-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="dc70b-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="dc70b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dc70b-117">Attribute-Id</span></span>      | <span data-ttu-id="dc70b-118">1.2.840.113556.1.4.1209</span><span class="sxs-lookup"><span data-stu-id="dc70b-118">1.2.840.113556.1.4.1209</span></span>                     |
| <span data-ttu-id="dc70b-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="dc70b-119">System-Id-Guid</span></span>    | <span data-ttu-id="dc70b-120">45b01501-c419-11d1-bbc9-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="dc70b-120">45b01501-c419-11d1-bbc9-0080c76670c0</span></span>        |
| <span data-ttu-id="dc70b-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc70b-121">Syntax</span></span>            | [<span data-ttu-id="dc70b-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="dc70b-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="dc70b-123">實作</span><span class="sxs-lookup"><span data-stu-id="dc70b-123">Implementations</span></span>

-   [<span data-ttu-id="dc70b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dc70b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dc70b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dc70b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dc70b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dc70b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dc70b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dc70b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dc70b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dc70b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dc70b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dc70b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dc70b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc70b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="dc70b-131">進入</span><span class="sxs-lookup"><span data-stu-id="dc70b-131">Entry</span></span> | <span data-ttu-id="dc70b-132">值</span><span class="sxs-lookup"><span data-stu-id="dc70b-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="dc70b-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc70b-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="dc70b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc70b-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="dc70b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc70b-135">System-Only</span></span>            | <span data-ttu-id="dc70b-136">否</span><span class="sxs-lookup"><span data-stu-id="dc70b-136">False</span></span>                                          |
| <span data-ttu-id="dc70b-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc70b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="dc70b-138">對</span><span class="sxs-lookup"><span data-stu-id="dc70b-138">True</span></span>                                           |
| <span data-ttu-id="dc70b-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc70b-139">Is Indexed</span></span>             | <span data-ttu-id="dc70b-140">否</span><span class="sxs-lookup"><span data-stu-id="dc70b-140">False</span></span>                                          |
| <span data-ttu-id="dc70b-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc70b-141">In Global Catalog</span></span>      | <span data-ttu-id="dc70b-142">對</span><span class="sxs-lookup"><span data-stu-id="dc70b-142">True</span></span>                                           |
| <span data-ttu-id="dc70b-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc70b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc70b-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc70b-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="dc70b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc70b-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="dc70b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc70b-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="dc70b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc70b-147">Search-Flags</span></span>           | <span data-ttu-id="dc70b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc70b-148">0x00000000</span></span>                                     |
| <span data-ttu-id="dc70b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc70b-149">System-Flags</span></span>           | <span data-ttu-id="dc70b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc70b-150">0x00000010</span></span>                                     |
| <span data-ttu-id="dc70b-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc70b-151">Classes used in</span></span>        | [<span data-ttu-id="dc70b-152">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="dc70b-152">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dc70b-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc70b-153">Windows Server 2003</span></span>



| <span data-ttu-id="dc70b-154">進入</span><span class="sxs-lookup"><span data-stu-id="dc70b-154">Entry</span></span> | <span data-ttu-id="dc70b-155">值</span><span class="sxs-lookup"><span data-stu-id="dc70b-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="dc70b-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc70b-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="dc70b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc70b-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="dc70b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc70b-158">System-Only</span></span>            | <span data-ttu-id="dc70b-159">否</span><span class="sxs-lookup"><span data-stu-id="dc70b-159">False</span></span>                                          |
| <span data-ttu-id="dc70b-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc70b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="dc70b-161">對</span><span class="sxs-lookup"><span data-stu-id="dc70b-161">True</span></span>                                           |
| <span data-ttu-id="dc70b-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc70b-162">Is Indexed</span></span>             | <span data-ttu-id="dc70b-163">否</span><span class="sxs-lookup"><span data-stu-id="dc70b-163">False</span></span>                                          |
| <span data-ttu-id="dc70b-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc70b-164">In Global Catalog</span></span>      | <span data-ttu-id="dc70b-165">對</span><span class="sxs-lookup"><span data-stu-id="dc70b-165">True</span></span>                                           |
| <span data-ttu-id="dc70b-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc70b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc70b-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc70b-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="dc70b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc70b-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="dc70b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc70b-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="dc70b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc70b-170">Search-Flags</span></span>           | <span data-ttu-id="dc70b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc70b-171">0x00000000</span></span>                                     |
| <span data-ttu-id="dc70b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc70b-172">System-Flags</span></span>           | <span data-ttu-id="dc70b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc70b-173">0x00000010</span></span>                                     |
| <span data-ttu-id="dc70b-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc70b-174">Classes used in</span></span>        | [<span data-ttu-id="dc70b-175">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="dc70b-175">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dc70b-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dc70b-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dc70b-177">進入</span><span class="sxs-lookup"><span data-stu-id="dc70b-177">Entry</span></span> | <span data-ttu-id="dc70b-178">值</span><span class="sxs-lookup"><span data-stu-id="dc70b-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="dc70b-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc70b-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="dc70b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc70b-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="dc70b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc70b-181">System-Only</span></span>            | <span data-ttu-id="dc70b-182">否</span><span class="sxs-lookup"><span data-stu-id="dc70b-182">False</span></span>                                          |
| <span data-ttu-id="dc70b-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc70b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="dc70b-184">對</span><span class="sxs-lookup"><span data-stu-id="dc70b-184">True</span></span>                                           |
| <span data-ttu-id="dc70b-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc70b-185">Is Indexed</span></span>             | <span data-ttu-id="dc70b-186">否</span><span class="sxs-lookup"><span data-stu-id="dc70b-186">False</span></span>                                          |
| <span data-ttu-id="dc70b-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc70b-187">In Global Catalog</span></span>      | <span data-ttu-id="dc70b-188">對</span><span class="sxs-lookup"><span data-stu-id="dc70b-188">True</span></span>                                           |
| <span data-ttu-id="dc70b-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc70b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc70b-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc70b-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="dc70b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc70b-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="dc70b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc70b-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="dc70b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc70b-193">Search-Flags</span></span>           | <span data-ttu-id="dc70b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc70b-194">0x00000000</span></span>                                     |
| <span data-ttu-id="dc70b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc70b-195">System-Flags</span></span>           | <span data-ttu-id="dc70b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc70b-196">0x00000010</span></span>                                     |
| <span data-ttu-id="dc70b-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc70b-197">Classes used in</span></span>        | [<span data-ttu-id="dc70b-198">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="dc70b-198">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dc70b-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc70b-199">Windows Server 2008</span></span>



| <span data-ttu-id="dc70b-200">進入</span><span class="sxs-lookup"><span data-stu-id="dc70b-200">Entry</span></span> | <span data-ttu-id="dc70b-201">值</span><span class="sxs-lookup"><span data-stu-id="dc70b-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="dc70b-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc70b-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="dc70b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc70b-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="dc70b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc70b-204">System-Only</span></span>            | <span data-ttu-id="dc70b-205">否</span><span class="sxs-lookup"><span data-stu-id="dc70b-205">False</span></span>                                          |
| <span data-ttu-id="dc70b-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc70b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="dc70b-207">對</span><span class="sxs-lookup"><span data-stu-id="dc70b-207">True</span></span>                                           |
| <span data-ttu-id="dc70b-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc70b-208">Is Indexed</span></span>             | <span data-ttu-id="dc70b-209">否</span><span class="sxs-lookup"><span data-stu-id="dc70b-209">False</span></span>                                          |
| <span data-ttu-id="dc70b-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc70b-210">In Global Catalog</span></span>      | <span data-ttu-id="dc70b-211">對</span><span class="sxs-lookup"><span data-stu-id="dc70b-211">True</span></span>                                           |
| <span data-ttu-id="dc70b-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc70b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc70b-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc70b-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="dc70b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc70b-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="dc70b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc70b-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="dc70b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc70b-216">Search-Flags</span></span>           | <span data-ttu-id="dc70b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc70b-217">0x00000000</span></span>                                     |
| <span data-ttu-id="dc70b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc70b-218">System-Flags</span></span>           | <span data-ttu-id="dc70b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc70b-219">0x00000010</span></span>                                     |
| <span data-ttu-id="dc70b-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc70b-220">Classes used in</span></span>        | [<span data-ttu-id="dc70b-221">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="dc70b-221">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dc70b-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dc70b-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dc70b-223">進入</span><span class="sxs-lookup"><span data-stu-id="dc70b-223">Entry</span></span> | <span data-ttu-id="dc70b-224">值</span><span class="sxs-lookup"><span data-stu-id="dc70b-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="dc70b-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc70b-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="dc70b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc70b-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="dc70b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc70b-227">System-Only</span></span>            | <span data-ttu-id="dc70b-228">否</span><span class="sxs-lookup"><span data-stu-id="dc70b-228">False</span></span>                                          |
| <span data-ttu-id="dc70b-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc70b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="dc70b-230">對</span><span class="sxs-lookup"><span data-stu-id="dc70b-230">True</span></span>                                           |
| <span data-ttu-id="dc70b-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc70b-231">Is Indexed</span></span>             | <span data-ttu-id="dc70b-232">否</span><span class="sxs-lookup"><span data-stu-id="dc70b-232">False</span></span>                                          |
| <span data-ttu-id="dc70b-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc70b-233">In Global Catalog</span></span>      | <span data-ttu-id="dc70b-234">對</span><span class="sxs-lookup"><span data-stu-id="dc70b-234">True</span></span>                                           |
| <span data-ttu-id="dc70b-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc70b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc70b-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc70b-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="dc70b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc70b-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="dc70b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc70b-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="dc70b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc70b-239">Search-Flags</span></span>           | <span data-ttu-id="dc70b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc70b-240">0x00000000</span></span>                                     |
| <span data-ttu-id="dc70b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc70b-241">System-Flags</span></span>           | <span data-ttu-id="dc70b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc70b-242">0x00000010</span></span>                                     |
| <span data-ttu-id="dc70b-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc70b-243">Classes used in</span></span>        | [<span data-ttu-id="dc70b-244">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="dc70b-244">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dc70b-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc70b-245">Windows Server 2012</span></span>



| <span data-ttu-id="dc70b-246">進入</span><span class="sxs-lookup"><span data-stu-id="dc70b-246">Entry</span></span> | <span data-ttu-id="dc70b-247">值</span><span class="sxs-lookup"><span data-stu-id="dc70b-247">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="dc70b-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc70b-248">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="dc70b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc70b-249">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="dc70b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc70b-250">System-Only</span></span>            | <span data-ttu-id="dc70b-251">否</span><span class="sxs-lookup"><span data-stu-id="dc70b-251">False</span></span>                                          |
| <span data-ttu-id="dc70b-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc70b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="dc70b-253">對</span><span class="sxs-lookup"><span data-stu-id="dc70b-253">True</span></span>                                           |
| <span data-ttu-id="dc70b-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc70b-254">Is Indexed</span></span>             | <span data-ttu-id="dc70b-255">否</span><span class="sxs-lookup"><span data-stu-id="dc70b-255">False</span></span>                                          |
| <span data-ttu-id="dc70b-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc70b-256">In Global Catalog</span></span>      | <span data-ttu-id="dc70b-257">對</span><span class="sxs-lookup"><span data-stu-id="dc70b-257">True</span></span>                                           |
| <span data-ttu-id="dc70b-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc70b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc70b-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc70b-259">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="dc70b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc70b-260">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="dc70b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc70b-261">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="dc70b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc70b-262">Search-Flags</span></span>           | <span data-ttu-id="dc70b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc70b-263">0x00000000</span></span>                                     |
| <span data-ttu-id="dc70b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc70b-264">System-Flags</span></span>           | <span data-ttu-id="dc70b-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc70b-265">0x00000010</span></span>                                     |
| <span data-ttu-id="dc70b-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc70b-266">Classes used in</span></span>        | [<span data-ttu-id="dc70b-267">**列印佇列**</span><span class="sxs-lookup"><span data-stu-id="dc70b-267">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





