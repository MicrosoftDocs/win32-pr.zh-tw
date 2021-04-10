---
title: SMTP 電子郵件地址屬性
description: 一般郵寄地址屬性。 在方塊中用來做為伺服器物件的選擇性屬性，在這種情況下，以郵件為基礎的 DS 複寫 (如果電腦已設定) 。
ms.assetid: 54fd710c-d140-4d46-9db3-0c72fb5fb08c
ms.tgt_platform: multiple
keywords:
- SMTP 郵寄地址屬性 AD 架構
- mailAddress 屬性 AD 架構
topic_type:
- apiref
api_name:
- SMTP-Mail-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1828c59af346ab5a5741aaa03358b711484089
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107226"
---
# <a name="smtp-mail-address-attribute"></a><span data-ttu-id="f0ec2-106">SMTP 電子郵件地址屬性</span><span class="sxs-lookup"><span data-stu-id="f0ec2-106">SMTP-Mail-Address attribute</span></span>

<span data-ttu-id="f0ec2-107">一般郵寄地址屬性。</span><span class="sxs-lookup"><span data-stu-id="f0ec2-107">Generic mail address attribute.</span></span> <span data-ttu-id="f0ec2-108">在方塊中用來做為伺服器物件的選擇性屬性，在這種情況下，以郵件為基礎的 DS 複寫 (如果電腦已設定) 。</span><span class="sxs-lookup"><span data-stu-id="f0ec2-108">Used in the box as an optional attribute of server objects, where it is consumed by mail-based DS replication (if the computers are so configured).</span></span>



| <span data-ttu-id="f0ec2-109">進入</span><span class="sxs-lookup"><span data-stu-id="f0ec2-109">Entry</span></span> | <span data-ttu-id="f0ec2-110">值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f0ec2-111">CN</span><span class="sxs-lookup"><span data-stu-id="f0ec2-111">CN</span></span>                | <span data-ttu-id="f0ec2-112">SMTP-郵寄地址</span><span class="sxs-lookup"><span data-stu-id="f0ec2-112">SMTP-Mail-Address</span></span>                           |
| <span data-ttu-id="f0ec2-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f0ec2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f0ec2-114">mailAddress</span><span class="sxs-lookup"><span data-stu-id="f0ec2-114">mailAddress</span></span>                                 |
| <span data-ttu-id="f0ec2-115">大小</span><span class="sxs-lookup"><span data-stu-id="f0ec2-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="f0ec2-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f0ec2-116">Update Privilege</span></span>  | <span data-ttu-id="f0ec2-117">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="f0ec2-117">Domain administrator</span></span>                        |
| <span data-ttu-id="f0ec2-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f0ec2-118">Update Frequency</span></span>  | <span data-ttu-id="f0ec2-119">幾乎不會</span><span class="sxs-lookup"><span data-stu-id="f0ec2-119">Almost never</span></span>                                |
| <span data-ttu-id="f0ec2-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f0ec2-120">Attribute-Id</span></span>      | <span data-ttu-id="f0ec2-121">1.2.840.113556.1.4.786</span><span class="sxs-lookup"><span data-stu-id="f0ec2-121">1.2.840.113556.1.4.786</span></span>                      |
| <span data-ttu-id="f0ec2-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f0ec2-122">System-Id-Guid</span></span>    | <span data-ttu-id="f0ec2-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f0ec2-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="f0ec2-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0ec2-124">Syntax</span></span>            | [<span data-ttu-id="f0ec2-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f0ec2-126">實作</span><span class="sxs-lookup"><span data-stu-id="f0ec2-126">Implementations</span></span>

-   [<span data-ttu-id="f0ec2-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f0ec2-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f0ec2-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f0ec2-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f0ec2-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f0ec2-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f0ec2-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f0ec2-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f0ec2-134">Windows 2000 Server</span></span>



| <span data-ttu-id="f0ec2-135">進入</span><span class="sxs-lookup"><span data-stu-id="f0ec2-135">Entry</span></span> | <span data-ttu-id="f0ec2-136">值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-136">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="f0ec2-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ec2-137">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ec2-138">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ec2-139">System-Only</span></span>            | <span data-ttu-id="f0ec2-140">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-140">False</span></span>                                 |
| <span data-ttu-id="f0ec2-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ec2-142">對</span><span class="sxs-lookup"><span data-stu-id="f0ec2-142">True</span></span>                                  |
| <span data-ttu-id="f0ec2-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ec2-143">Is Indexed</span></span>             | <span data-ttu-id="f0ec2-144">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-144">False</span></span>                                 |
| <span data-ttu-id="f0ec2-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ec2-145">In Global Catalog</span></span>      | <span data-ttu-id="f0ec2-146">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-146">False</span></span>                                 |
| <span data-ttu-id="f0ec2-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ec2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ec2-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ec2-148">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="f0ec2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ec2-149">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ec2-150">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-151">Search-Flags</span></span>           | <span data-ttu-id="f0ec2-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ec2-152">0x00000000</span></span>                            |
| <span data-ttu-id="f0ec2-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-153">System-Flags</span></span>           | <span data-ttu-id="f0ec2-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ec2-154">0x00000010</span></span>                            |
| <span data-ttu-id="f0ec2-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ec2-155">Classes used in</span></span>        | [<span data-ttu-id="f0ec2-156">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-156">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f0ec2-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0ec2-157">Windows Server 2003</span></span>



| <span data-ttu-id="f0ec2-158">進入</span><span class="sxs-lookup"><span data-stu-id="f0ec2-158">Entry</span></span> | <span data-ttu-id="f0ec2-159">值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-159">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="f0ec2-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ec2-160">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ec2-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ec2-162">System-Only</span></span>            | <span data-ttu-id="f0ec2-163">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-163">False</span></span>                                 |
| <span data-ttu-id="f0ec2-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ec2-165">對</span><span class="sxs-lookup"><span data-stu-id="f0ec2-165">True</span></span>                                  |
| <span data-ttu-id="f0ec2-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ec2-166">Is Indexed</span></span>             | <span data-ttu-id="f0ec2-167">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-167">False</span></span>                                 |
| <span data-ttu-id="f0ec2-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ec2-168">In Global Catalog</span></span>      | <span data-ttu-id="f0ec2-169">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-169">False</span></span>                                 |
| <span data-ttu-id="f0ec2-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ec2-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ec2-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ec2-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="f0ec2-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ec2-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ec2-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-174">Search-Flags</span></span>           | <span data-ttu-id="f0ec2-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ec2-175">0x00000000</span></span>                            |
| <span data-ttu-id="f0ec2-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-176">System-Flags</span></span>           | <span data-ttu-id="f0ec2-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ec2-177">0x00000010</span></span>                            |
| <span data-ttu-id="f0ec2-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ec2-178">Classes used in</span></span>        | [<span data-ttu-id="f0ec2-179">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-179">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f0ec2-180">亞當</span><span class="sxs-lookup"><span data-stu-id="f0ec2-180">ADAM</span></span>



| <span data-ttu-id="f0ec2-181">進入</span><span class="sxs-lookup"><span data-stu-id="f0ec2-181">Entry</span></span> | <span data-ttu-id="f0ec2-182">值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="f0ec2-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ec2-183">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ec2-184">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ec2-185">System-Only</span></span>            | <span data-ttu-id="f0ec2-186">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-186">False</span></span>                                 |
| <span data-ttu-id="f0ec2-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ec2-188">對</span><span class="sxs-lookup"><span data-stu-id="f0ec2-188">True</span></span>                                  |
| <span data-ttu-id="f0ec2-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ec2-189">Is Indexed</span></span>             | <span data-ttu-id="f0ec2-190">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-190">False</span></span>                                 |
| <span data-ttu-id="f0ec2-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ec2-191">In Global Catalog</span></span>      | <span data-ttu-id="f0ec2-192">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-192">False</span></span>                                 |
| <span data-ttu-id="f0ec2-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ec2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ec2-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ec2-194">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="f0ec2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ec2-195">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ec2-196">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-197">Search-Flags</span></span>           | <span data-ttu-id="f0ec2-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ec2-198">0x00000000</span></span>                            |
| <span data-ttu-id="f0ec2-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-199">System-Flags</span></span>           | <span data-ttu-id="f0ec2-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ec2-200">0x00000010</span></span>                            |
| <span data-ttu-id="f0ec2-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ec2-201">Classes used in</span></span>        | [<span data-ttu-id="f0ec2-202">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-202">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f0ec2-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f0ec2-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f0ec2-204">進入</span><span class="sxs-lookup"><span data-stu-id="f0ec2-204">Entry</span></span> | <span data-ttu-id="f0ec2-205">值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-205">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="f0ec2-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ec2-206">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ec2-207">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ec2-208">System-Only</span></span>            | <span data-ttu-id="f0ec2-209">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-209">False</span></span>                                 |
| <span data-ttu-id="f0ec2-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-210">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ec2-211">對</span><span class="sxs-lookup"><span data-stu-id="f0ec2-211">True</span></span>                                  |
| <span data-ttu-id="f0ec2-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ec2-212">Is Indexed</span></span>             | <span data-ttu-id="f0ec2-213">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-213">False</span></span>                                 |
| <span data-ttu-id="f0ec2-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ec2-214">In Global Catalog</span></span>      | <span data-ttu-id="f0ec2-215">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-215">False</span></span>                                 |
| <span data-ttu-id="f0ec2-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ec2-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ec2-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ec2-217">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="f0ec2-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ec2-218">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ec2-219">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-220">Search-Flags</span></span>           | <span data-ttu-id="f0ec2-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ec2-221">0x00000000</span></span>                            |
| <span data-ttu-id="f0ec2-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-222">System-Flags</span></span>           | <span data-ttu-id="f0ec2-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ec2-223">0x00000010</span></span>                            |
| <span data-ttu-id="f0ec2-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ec2-224">Classes used in</span></span>        | [<span data-ttu-id="f0ec2-225">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-225">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f0ec2-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0ec2-226">Windows Server 2008</span></span>



| <span data-ttu-id="f0ec2-227">進入</span><span class="sxs-lookup"><span data-stu-id="f0ec2-227">Entry</span></span> | <span data-ttu-id="f0ec2-228">值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-228">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="f0ec2-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ec2-229">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ec2-230">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ec2-231">System-Only</span></span>            | <span data-ttu-id="f0ec2-232">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-232">False</span></span>                                 |
| <span data-ttu-id="f0ec2-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-233">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ec2-234">對</span><span class="sxs-lookup"><span data-stu-id="f0ec2-234">True</span></span>                                  |
| <span data-ttu-id="f0ec2-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ec2-235">Is Indexed</span></span>             | <span data-ttu-id="f0ec2-236">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-236">False</span></span>                                 |
| <span data-ttu-id="f0ec2-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ec2-237">In Global Catalog</span></span>      | <span data-ttu-id="f0ec2-238">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-238">False</span></span>                                 |
| <span data-ttu-id="f0ec2-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ec2-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ec2-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ec2-240">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="f0ec2-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ec2-241">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ec2-242">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-243">Search-Flags</span></span>           | <span data-ttu-id="f0ec2-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ec2-244">0x00000000</span></span>                            |
| <span data-ttu-id="f0ec2-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-245">System-Flags</span></span>           | <span data-ttu-id="f0ec2-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ec2-246">0x00000010</span></span>                            |
| <span data-ttu-id="f0ec2-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ec2-247">Classes used in</span></span>        | [<span data-ttu-id="f0ec2-248">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-248">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f0ec2-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0ec2-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f0ec2-250">進入</span><span class="sxs-lookup"><span data-stu-id="f0ec2-250">Entry</span></span> | <span data-ttu-id="f0ec2-251">值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-251">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="f0ec2-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ec2-252">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ec2-253">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ec2-254">System-Only</span></span>            | <span data-ttu-id="f0ec2-255">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-255">False</span></span>                                 |
| <span data-ttu-id="f0ec2-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-256">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ec2-257">對</span><span class="sxs-lookup"><span data-stu-id="f0ec2-257">True</span></span>                                  |
| <span data-ttu-id="f0ec2-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ec2-258">Is Indexed</span></span>             | <span data-ttu-id="f0ec2-259">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-259">False</span></span>                                 |
| <span data-ttu-id="f0ec2-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ec2-260">In Global Catalog</span></span>      | <span data-ttu-id="f0ec2-261">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-261">False</span></span>                                 |
| <span data-ttu-id="f0ec2-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ec2-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ec2-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ec2-263">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="f0ec2-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ec2-264">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ec2-265">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-266">Search-Flags</span></span>           | <span data-ttu-id="f0ec2-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ec2-267">0x00000000</span></span>                            |
| <span data-ttu-id="f0ec2-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-268">System-Flags</span></span>           | <span data-ttu-id="f0ec2-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ec2-269">0x00000010</span></span>                            |
| <span data-ttu-id="f0ec2-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ec2-270">Classes used in</span></span>        | [<span data-ttu-id="f0ec2-271">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-271">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f0ec2-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0ec2-272">Windows Server 2012</span></span>



| <span data-ttu-id="f0ec2-273">進入</span><span class="sxs-lookup"><span data-stu-id="f0ec2-273">Entry</span></span> | <span data-ttu-id="f0ec2-274">值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-274">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="f0ec2-275">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ec2-275">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0ec2-276">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="f0ec2-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0ec2-277">System-Only</span></span>            | <span data-ttu-id="f0ec2-278">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-278">False</span></span>                                 |
| <span data-ttu-id="f0ec2-279">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0ec2-279">Is-Single-Valued</span></span>       | <span data-ttu-id="f0ec2-280">對</span><span class="sxs-lookup"><span data-stu-id="f0ec2-280">True</span></span>                                  |
| <span data-ttu-id="f0ec2-281">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0ec2-281">Is Indexed</span></span>             | <span data-ttu-id="f0ec2-282">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-282">False</span></span>                                 |
| <span data-ttu-id="f0ec2-283">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0ec2-283">In Global Catalog</span></span>      | <span data-ttu-id="f0ec2-284">否</span><span class="sxs-lookup"><span data-stu-id="f0ec2-284">False</span></span>                                 |
| <span data-ttu-id="f0ec2-285">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0ec2-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0ec2-286">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0ec2-286">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="f0ec2-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0ec2-287">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0ec2-288">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="f0ec2-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-289">Search-Flags</span></span>           | <span data-ttu-id="f0ec2-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0ec2-290">0x00000000</span></span>                            |
| <span data-ttu-id="f0ec2-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0ec2-291">System-Flags</span></span>           | <span data-ttu-id="f0ec2-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0ec2-292">0x00000010</span></span>                            |
| <span data-ttu-id="f0ec2-293">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0ec2-293">Classes used in</span></span>        | [<span data-ttu-id="f0ec2-294">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="f0ec2-294">**Server**</span></span>](c-server.md)<br/> |



 

 





