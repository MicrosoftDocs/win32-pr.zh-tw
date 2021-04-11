---
title: Max-Storage 屬性
description: 使用者可以使用的最大磁碟空間量。 使用 [使用者 MAXSTORAGE 無限制] 中指定的值 \_ \_ 來使用所有可用的磁碟空間。
ms.assetid: 69302641-ecfc-4b0f-81f8-f69b48c6faa7
ms.tgt_platform: multiple
keywords:
- Max-Storage 屬性 AD 架構
- maxStorage 屬性 AD 架構
topic_type:
- apiref
api_name:
- Max-Storage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6caff3f85de7073818096324445b63a3c1c9be
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845223"
---
# <a name="max-storage-attribute"></a><span data-ttu-id="f7384-106">Max-Storage 屬性</span><span class="sxs-lookup"><span data-stu-id="f7384-106">Max-Storage attribute</span></span>

<span data-ttu-id="f7384-107">使用者可以使用的最大磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="f7384-107">The maximum amount of disk space the user can use.</span></span> <span data-ttu-id="f7384-108">使用 [使用者 MAXSTORAGE 無限制] 中指定的值 \_ \_ 來使用所有可用的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="f7384-108">Use the value specified in USER\_MAXSTORAGE\_UNLIMITED to use all available disk space.</span></span>



| <span data-ttu-id="f7384-109">進入</span><span class="sxs-lookup"><span data-stu-id="f7384-109">Entry</span></span> | <span data-ttu-id="f7384-110">值</span><span class="sxs-lookup"><span data-stu-id="f7384-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="f7384-111">CN</span><span class="sxs-lookup"><span data-stu-id="f7384-111">CN</span></span>                | <span data-ttu-id="f7384-112">Max-Storage</span><span class="sxs-lookup"><span data-stu-id="f7384-112">Max-Storage</span></span>                                                |
| <span data-ttu-id="f7384-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f7384-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f7384-114">maxStorage</span><span class="sxs-lookup"><span data-stu-id="f7384-114">maxStorage</span></span>                                                 |
| <span data-ttu-id="f7384-115">大小</span><span class="sxs-lookup"><span data-stu-id="f7384-115">Size</span></span>              | <span data-ttu-id="f7384-116">8位元組：使用者 \_ MAXSTORAGE 無 \_ 限制的 ( (不帶正負號的 long) -1L) </span><span class="sxs-lookup"><span data-stu-id="f7384-116">8 bytes: USER\_MAXSTORAGE\_UNLIMITED ((unsigned long) -1L)</span></span> |
| <span data-ttu-id="f7384-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f7384-117">Update Privilege</span></span>  | <span data-ttu-id="f7384-118">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="f7384-118">Domain administrator</span></span>                                       |
| <span data-ttu-id="f7384-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f7384-119">Update Frequency</span></span>  | <span data-ttu-id="f7384-120">每次需要變更磁片配額時。</span><span class="sxs-lookup"><span data-stu-id="f7384-120">Whenever the disk quota needs to change.</span></span>                   |
| <span data-ttu-id="f7384-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f7384-121">Attribute-Id</span></span>      | <span data-ttu-id="f7384-122">1.2.840.113556.1.4.76</span><span class="sxs-lookup"><span data-stu-id="f7384-122">1.2.840.113556.1.4.76</span></span>                                      |
| <span data-ttu-id="f7384-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f7384-123">System-Id-Guid</span></span>    | <span data-ttu-id="f7384-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f7384-124">bf9679bd-0de6-11d0-a285-00aa003049e2</span></span>                       |
| <span data-ttu-id="f7384-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7384-125">Syntax</span></span>            | [<span data-ttu-id="f7384-126">**間隔**</span><span class="sxs-lookup"><span data-stu-id="f7384-126">**Interval**</span></span>](s-interval.md)                             |



## <a name="implementations"></a><span data-ttu-id="f7384-127">實作</span><span class="sxs-lookup"><span data-stu-id="f7384-127">Implementations</span></span>

-   [<span data-ttu-id="f7384-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f7384-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f7384-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f7384-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f7384-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f7384-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f7384-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f7384-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f7384-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f7384-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f7384-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f7384-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f7384-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7384-134">Windows 2000 Server</span></span>



| <span data-ttu-id="f7384-135">進入</span><span class="sxs-lookup"><span data-stu-id="f7384-135">Entry</span></span> | <span data-ttu-id="f7384-136">值</span><span class="sxs-lookup"><span data-stu-id="f7384-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7384-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f7384-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7384-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7384-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7384-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7384-139">System-Only</span></span>            | <span data-ttu-id="f7384-140">否</span><span class="sxs-lookup"><span data-stu-id="f7384-140">False</span></span>                             |
| <span data-ttu-id="f7384-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f7384-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f7384-142">對</span><span class="sxs-lookup"><span data-stu-id="f7384-142">True</span></span>                              |
| <span data-ttu-id="f7384-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f7384-143">Is Indexed</span></span>             | <span data-ttu-id="f7384-144">否</span><span class="sxs-lookup"><span data-stu-id="f7384-144">False</span></span>                             |
| <span data-ttu-id="f7384-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f7384-145">In Global Catalog</span></span>      | <span data-ttu-id="f7384-146">否</span><span class="sxs-lookup"><span data-stu-id="f7384-146">False</span></span>                             |
| <span data-ttu-id="f7384-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f7384-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7384-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f7384-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7384-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7384-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7384-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7384-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7384-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7384-151">Search-Flags</span></span>           | <span data-ttu-id="f7384-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7384-152">0x00000010</span></span>                        |
| <span data-ttu-id="f7384-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7384-153">System-Flags</span></span>           | <span data-ttu-id="f7384-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7384-154">0x00000010</span></span>                        |
| <span data-ttu-id="f7384-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f7384-155">Classes used in</span></span>        | [<span data-ttu-id="f7384-156">**User**</span><span class="sxs-lookup"><span data-stu-id="f7384-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f7384-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7384-157">Windows Server 2003</span></span>



| <span data-ttu-id="f7384-158">進入</span><span class="sxs-lookup"><span data-stu-id="f7384-158">Entry</span></span> | <span data-ttu-id="f7384-159">值</span><span class="sxs-lookup"><span data-stu-id="f7384-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7384-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f7384-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7384-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7384-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7384-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7384-162">System-Only</span></span>            | <span data-ttu-id="f7384-163">否</span><span class="sxs-lookup"><span data-stu-id="f7384-163">False</span></span>                             |
| <span data-ttu-id="f7384-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f7384-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f7384-165">對</span><span class="sxs-lookup"><span data-stu-id="f7384-165">True</span></span>                              |
| <span data-ttu-id="f7384-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f7384-166">Is Indexed</span></span>             | <span data-ttu-id="f7384-167">否</span><span class="sxs-lookup"><span data-stu-id="f7384-167">False</span></span>                             |
| <span data-ttu-id="f7384-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f7384-168">In Global Catalog</span></span>      | <span data-ttu-id="f7384-169">否</span><span class="sxs-lookup"><span data-stu-id="f7384-169">False</span></span>                             |
| <span data-ttu-id="f7384-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f7384-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7384-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f7384-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7384-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7384-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7384-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7384-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7384-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7384-174">Search-Flags</span></span>           | <span data-ttu-id="f7384-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7384-175">0x00000010</span></span>                        |
| <span data-ttu-id="f7384-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7384-176">System-Flags</span></span>           | <span data-ttu-id="f7384-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7384-177">0x00000010</span></span>                        |
| <span data-ttu-id="f7384-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f7384-178">Classes used in</span></span>        | [<span data-ttu-id="f7384-179">**User**</span><span class="sxs-lookup"><span data-stu-id="f7384-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f7384-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f7384-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f7384-181">進入</span><span class="sxs-lookup"><span data-stu-id="f7384-181">Entry</span></span> | <span data-ttu-id="f7384-182">值</span><span class="sxs-lookup"><span data-stu-id="f7384-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7384-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f7384-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7384-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7384-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7384-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7384-185">System-Only</span></span>            | <span data-ttu-id="f7384-186">否</span><span class="sxs-lookup"><span data-stu-id="f7384-186">False</span></span>                             |
| <span data-ttu-id="f7384-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f7384-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f7384-188">對</span><span class="sxs-lookup"><span data-stu-id="f7384-188">True</span></span>                              |
| <span data-ttu-id="f7384-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f7384-189">Is Indexed</span></span>             | <span data-ttu-id="f7384-190">否</span><span class="sxs-lookup"><span data-stu-id="f7384-190">False</span></span>                             |
| <span data-ttu-id="f7384-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f7384-191">In Global Catalog</span></span>      | <span data-ttu-id="f7384-192">否</span><span class="sxs-lookup"><span data-stu-id="f7384-192">False</span></span>                             |
| <span data-ttu-id="f7384-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f7384-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7384-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f7384-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7384-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7384-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7384-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7384-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7384-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7384-197">Search-Flags</span></span>           | <span data-ttu-id="f7384-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7384-198">0x00000010</span></span>                        |
| <span data-ttu-id="f7384-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7384-199">System-Flags</span></span>           | <span data-ttu-id="f7384-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7384-200">0x00000010</span></span>                        |
| <span data-ttu-id="f7384-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f7384-201">Classes used in</span></span>        | [<span data-ttu-id="f7384-202">**User**</span><span class="sxs-lookup"><span data-stu-id="f7384-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f7384-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7384-203">Windows Server 2008</span></span>



| <span data-ttu-id="f7384-204">進入</span><span class="sxs-lookup"><span data-stu-id="f7384-204">Entry</span></span> | <span data-ttu-id="f7384-205">值</span><span class="sxs-lookup"><span data-stu-id="f7384-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7384-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f7384-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7384-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7384-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7384-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7384-208">System-Only</span></span>            | <span data-ttu-id="f7384-209">否</span><span class="sxs-lookup"><span data-stu-id="f7384-209">False</span></span>                             |
| <span data-ttu-id="f7384-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f7384-210">Is-Single-Valued</span></span>       | <span data-ttu-id="f7384-211">對</span><span class="sxs-lookup"><span data-stu-id="f7384-211">True</span></span>                              |
| <span data-ttu-id="f7384-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f7384-212">Is Indexed</span></span>             | <span data-ttu-id="f7384-213">否</span><span class="sxs-lookup"><span data-stu-id="f7384-213">False</span></span>                             |
| <span data-ttu-id="f7384-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f7384-214">In Global Catalog</span></span>      | <span data-ttu-id="f7384-215">否</span><span class="sxs-lookup"><span data-stu-id="f7384-215">False</span></span>                             |
| <span data-ttu-id="f7384-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f7384-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7384-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f7384-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7384-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7384-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7384-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7384-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7384-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7384-220">Search-Flags</span></span>           | <span data-ttu-id="f7384-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7384-221">0x00000010</span></span>                        |
| <span data-ttu-id="f7384-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7384-222">System-Flags</span></span>           | <span data-ttu-id="f7384-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7384-223">0x00000010</span></span>                        |
| <span data-ttu-id="f7384-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f7384-224">Classes used in</span></span>        | [<span data-ttu-id="f7384-225">**User**</span><span class="sxs-lookup"><span data-stu-id="f7384-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f7384-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7384-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f7384-227">進入</span><span class="sxs-lookup"><span data-stu-id="f7384-227">Entry</span></span> | <span data-ttu-id="f7384-228">值</span><span class="sxs-lookup"><span data-stu-id="f7384-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7384-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f7384-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7384-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7384-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7384-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7384-231">System-Only</span></span>            | <span data-ttu-id="f7384-232">否</span><span class="sxs-lookup"><span data-stu-id="f7384-232">False</span></span>                             |
| <span data-ttu-id="f7384-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f7384-233">Is-Single-Valued</span></span>       | <span data-ttu-id="f7384-234">對</span><span class="sxs-lookup"><span data-stu-id="f7384-234">True</span></span>                              |
| <span data-ttu-id="f7384-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f7384-235">Is Indexed</span></span>             | <span data-ttu-id="f7384-236">否</span><span class="sxs-lookup"><span data-stu-id="f7384-236">False</span></span>                             |
| <span data-ttu-id="f7384-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f7384-237">In Global Catalog</span></span>      | <span data-ttu-id="f7384-238">否</span><span class="sxs-lookup"><span data-stu-id="f7384-238">False</span></span>                             |
| <span data-ttu-id="f7384-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f7384-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7384-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f7384-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7384-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7384-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7384-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7384-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7384-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7384-243">Search-Flags</span></span>           | <span data-ttu-id="f7384-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7384-244">0x00000010</span></span>                        |
| <span data-ttu-id="f7384-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7384-245">System-Flags</span></span>           | <span data-ttu-id="f7384-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7384-246">0x00000010</span></span>                        |
| <span data-ttu-id="f7384-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f7384-247">Classes used in</span></span>        | [<span data-ttu-id="f7384-248">**User**</span><span class="sxs-lookup"><span data-stu-id="f7384-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f7384-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7384-249">Windows Server 2012</span></span>



| <span data-ttu-id="f7384-250">進入</span><span class="sxs-lookup"><span data-stu-id="f7384-250">Entry</span></span> | <span data-ttu-id="f7384-251">值</span><span class="sxs-lookup"><span data-stu-id="f7384-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f7384-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f7384-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f7384-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7384-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f7384-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7384-254">System-Only</span></span>            | <span data-ttu-id="f7384-255">否</span><span class="sxs-lookup"><span data-stu-id="f7384-255">False</span></span>                             |
| <span data-ttu-id="f7384-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f7384-256">Is-Single-Valued</span></span>       | <span data-ttu-id="f7384-257">對</span><span class="sxs-lookup"><span data-stu-id="f7384-257">True</span></span>                              |
| <span data-ttu-id="f7384-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f7384-258">Is Indexed</span></span>             | <span data-ttu-id="f7384-259">否</span><span class="sxs-lookup"><span data-stu-id="f7384-259">False</span></span>                             |
| <span data-ttu-id="f7384-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f7384-260">In Global Catalog</span></span>      | <span data-ttu-id="f7384-261">否</span><span class="sxs-lookup"><span data-stu-id="f7384-261">False</span></span>                             |
| <span data-ttu-id="f7384-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f7384-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7384-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f7384-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f7384-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7384-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f7384-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7384-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f7384-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7384-266">Search-Flags</span></span>           | <span data-ttu-id="f7384-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7384-267">0x00000010</span></span>                        |
| <span data-ttu-id="f7384-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7384-268">System-Flags</span></span>           | <span data-ttu-id="f7384-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7384-269">0x00000010</span></span>                        |
| <span data-ttu-id="f7384-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f7384-270">Classes used in</span></span>        | [<span data-ttu-id="f7384-271">**User**</span><span class="sxs-lookup"><span data-stu-id="f7384-271">**User**</span></span>](c-user.md)<br/> |



 

 





