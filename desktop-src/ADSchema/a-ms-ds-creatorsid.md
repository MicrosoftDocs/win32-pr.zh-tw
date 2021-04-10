---
title: MS DS-Creator-SID 屬性
description: 包含此屬性之物件的建立者的安全識別碼。
ms.assetid: 5e643c56-bfe9-4489-89a9-5ce56f90f288
ms.tgt_platform: multiple
keywords:
- MS DS-Creator-SID 屬性 AD 架構
- CreatorSID 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-DS-Creator-SID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b5b5635773271c4864ac2c8ec1898edcc9a9f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935278"
---
# <a name="ms-ds-creator-sid-attribute"></a><span data-ttu-id="9b375-105">MS DS-Creator-SID 屬性</span><span class="sxs-lookup"><span data-stu-id="9b375-105">MS-DS-Creator-SID attribute</span></span>

<span data-ttu-id="9b375-106">包含此屬性之物件的建立者的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b375-106">The security ID of the creator of the object that contains this attribute.</span></span>



| <span data-ttu-id="9b375-107">進入</span><span class="sxs-lookup"><span data-stu-id="9b375-107">Entry</span></span> | <span data-ttu-id="9b375-108">值</span><span class="sxs-lookup"><span data-stu-id="9b375-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="9b375-109">CN</span><span class="sxs-lookup"><span data-stu-id="9b375-109">CN</span></span>                | <span data-ttu-id="9b375-110">MS-DS-Creator-SID</span><span class="sxs-lookup"><span data-stu-id="9b375-110">MS-DS-Creator-SID</span></span>                    |
| <span data-ttu-id="9b375-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9b375-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9b375-112">CreatorSID</span><span class="sxs-lookup"><span data-stu-id="9b375-112">mS-DS-CreatorSID</span></span>                     |
| <span data-ttu-id="9b375-113">大小</span><span class="sxs-lookup"><span data-stu-id="9b375-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="9b375-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9b375-114">Update Privilege</span></span>  | <span data-ttu-id="9b375-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="9b375-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="9b375-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9b375-116">Update Frequency</span></span>  | <span data-ttu-id="9b375-117">每次建立新的物件時。</span><span class="sxs-lookup"><span data-stu-id="9b375-117">Whenever a new object is created.</span></span>    |
| <span data-ttu-id="9b375-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9b375-118">Attribute-Id</span></span>      | <span data-ttu-id="9b375-119">1.2.840.113556.1.4.1410</span><span class="sxs-lookup"><span data-stu-id="9b375-119">1.2.840.113556.1.4.1410</span></span>              |
| <span data-ttu-id="9b375-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9b375-120">System-Id-Guid</span></span>    | <span data-ttu-id="9b375-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="9b375-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span></span> |
| <span data-ttu-id="9b375-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b375-122">Syntax</span></span>            | [<span data-ttu-id="9b375-123">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="9b375-123">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="9b375-124">實作</span><span class="sxs-lookup"><span data-stu-id="9b375-124">Implementations</span></span>

-   [<span data-ttu-id="9b375-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9b375-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9b375-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9b375-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9b375-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9b375-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9b375-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9b375-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9b375-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9b375-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9b375-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9b375-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9b375-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9b375-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9b375-132">進入</span><span class="sxs-lookup"><span data-stu-id="9b375-132">Entry</span></span> | <span data-ttu-id="9b375-133">值</span><span class="sxs-lookup"><span data-stu-id="9b375-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9b375-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9b375-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9b375-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b375-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9b375-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b375-136">System-Only</span></span>            | <span data-ttu-id="9b375-137">對</span><span class="sxs-lookup"><span data-stu-id="9b375-137">True</span></span>                              |
| <span data-ttu-id="9b375-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9b375-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9b375-139">對</span><span class="sxs-lookup"><span data-stu-id="9b375-139">True</span></span>                              |
| <span data-ttu-id="9b375-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9b375-140">Is Indexed</span></span>             | <span data-ttu-id="9b375-141">對</span><span class="sxs-lookup"><span data-stu-id="9b375-141">True</span></span>                              |
| <span data-ttu-id="9b375-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9b375-142">In Global Catalog</span></span>      | <span data-ttu-id="9b375-143">否</span><span class="sxs-lookup"><span data-stu-id="9b375-143">False</span></span>                             |
| <span data-ttu-id="9b375-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9b375-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b375-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9b375-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9b375-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b375-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9b375-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b375-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9b375-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b375-148">Search-Flags</span></span>           | <span data-ttu-id="9b375-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b375-149">0x00000001</span></span>                        |
| <span data-ttu-id="9b375-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b375-150">System-Flags</span></span>           | <span data-ttu-id="9b375-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b375-151">0x00000010</span></span>                        |
| <span data-ttu-id="9b375-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9b375-152">Classes used in</span></span>        | [<span data-ttu-id="9b375-153">**User**</span><span class="sxs-lookup"><span data-stu-id="9b375-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9b375-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9b375-154">Windows Server 2003</span></span>



| <span data-ttu-id="9b375-155">進入</span><span class="sxs-lookup"><span data-stu-id="9b375-155">Entry</span></span> | <span data-ttu-id="9b375-156">值</span><span class="sxs-lookup"><span data-stu-id="9b375-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9b375-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9b375-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9b375-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b375-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9b375-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b375-159">System-Only</span></span>            | <span data-ttu-id="9b375-160">對</span><span class="sxs-lookup"><span data-stu-id="9b375-160">True</span></span>                              |
| <span data-ttu-id="9b375-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9b375-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9b375-162">對</span><span class="sxs-lookup"><span data-stu-id="9b375-162">True</span></span>                              |
| <span data-ttu-id="9b375-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9b375-163">Is Indexed</span></span>             | <span data-ttu-id="9b375-164">對</span><span class="sxs-lookup"><span data-stu-id="9b375-164">True</span></span>                              |
| <span data-ttu-id="9b375-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9b375-165">In Global Catalog</span></span>      | <span data-ttu-id="9b375-166">否</span><span class="sxs-lookup"><span data-stu-id="9b375-166">False</span></span>                             |
| <span data-ttu-id="9b375-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9b375-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b375-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9b375-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9b375-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b375-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9b375-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b375-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9b375-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b375-171">Search-Flags</span></span>           | <span data-ttu-id="9b375-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b375-172">0x00000001</span></span>                        |
| <span data-ttu-id="9b375-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b375-173">System-Flags</span></span>           | <span data-ttu-id="9b375-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b375-174">0x00000010</span></span>                        |
| <span data-ttu-id="9b375-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9b375-175">Classes used in</span></span>        | [<span data-ttu-id="9b375-176">**User**</span><span class="sxs-lookup"><span data-stu-id="9b375-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9b375-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9b375-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9b375-178">進入</span><span class="sxs-lookup"><span data-stu-id="9b375-178">Entry</span></span> | <span data-ttu-id="9b375-179">值</span><span class="sxs-lookup"><span data-stu-id="9b375-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9b375-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9b375-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9b375-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b375-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9b375-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b375-182">System-Only</span></span>            | <span data-ttu-id="9b375-183">對</span><span class="sxs-lookup"><span data-stu-id="9b375-183">True</span></span>                              |
| <span data-ttu-id="9b375-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9b375-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9b375-185">對</span><span class="sxs-lookup"><span data-stu-id="9b375-185">True</span></span>                              |
| <span data-ttu-id="9b375-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9b375-186">Is Indexed</span></span>             | <span data-ttu-id="9b375-187">對</span><span class="sxs-lookup"><span data-stu-id="9b375-187">True</span></span>                              |
| <span data-ttu-id="9b375-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9b375-188">In Global Catalog</span></span>      | <span data-ttu-id="9b375-189">否</span><span class="sxs-lookup"><span data-stu-id="9b375-189">False</span></span>                             |
| <span data-ttu-id="9b375-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9b375-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b375-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9b375-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9b375-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b375-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9b375-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b375-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9b375-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b375-194">Search-Flags</span></span>           | <span data-ttu-id="9b375-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b375-195">0x00000001</span></span>                        |
| <span data-ttu-id="9b375-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b375-196">System-Flags</span></span>           | <span data-ttu-id="9b375-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b375-197">0x00000010</span></span>                        |
| <span data-ttu-id="9b375-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9b375-198">Classes used in</span></span>        | [<span data-ttu-id="9b375-199">**User**</span><span class="sxs-lookup"><span data-stu-id="9b375-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9b375-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b375-200">Windows Server 2008</span></span>



| <span data-ttu-id="9b375-201">進入</span><span class="sxs-lookup"><span data-stu-id="9b375-201">Entry</span></span> | <span data-ttu-id="9b375-202">值</span><span class="sxs-lookup"><span data-stu-id="9b375-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9b375-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9b375-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9b375-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b375-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9b375-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b375-205">System-Only</span></span>            | <span data-ttu-id="9b375-206">對</span><span class="sxs-lookup"><span data-stu-id="9b375-206">True</span></span>                              |
| <span data-ttu-id="9b375-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9b375-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9b375-208">對</span><span class="sxs-lookup"><span data-stu-id="9b375-208">True</span></span>                              |
| <span data-ttu-id="9b375-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9b375-209">Is Indexed</span></span>             | <span data-ttu-id="9b375-210">對</span><span class="sxs-lookup"><span data-stu-id="9b375-210">True</span></span>                              |
| <span data-ttu-id="9b375-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9b375-211">In Global Catalog</span></span>      | <span data-ttu-id="9b375-212">否</span><span class="sxs-lookup"><span data-stu-id="9b375-212">False</span></span>                             |
| <span data-ttu-id="9b375-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9b375-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b375-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9b375-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9b375-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b375-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9b375-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b375-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9b375-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b375-217">Search-Flags</span></span>           | <span data-ttu-id="9b375-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b375-218">0x00000001</span></span>                        |
| <span data-ttu-id="9b375-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b375-219">System-Flags</span></span>           | <span data-ttu-id="9b375-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b375-220">0x00000010</span></span>                        |
| <span data-ttu-id="9b375-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9b375-221">Classes used in</span></span>        | [<span data-ttu-id="9b375-222">**User**</span><span class="sxs-lookup"><span data-stu-id="9b375-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9b375-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b375-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9b375-224">進入</span><span class="sxs-lookup"><span data-stu-id="9b375-224">Entry</span></span> | <span data-ttu-id="9b375-225">值</span><span class="sxs-lookup"><span data-stu-id="9b375-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9b375-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9b375-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9b375-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b375-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9b375-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b375-228">System-Only</span></span>            | <span data-ttu-id="9b375-229">對</span><span class="sxs-lookup"><span data-stu-id="9b375-229">True</span></span>                              |
| <span data-ttu-id="9b375-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9b375-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9b375-231">對</span><span class="sxs-lookup"><span data-stu-id="9b375-231">True</span></span>                              |
| <span data-ttu-id="9b375-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9b375-232">Is Indexed</span></span>             | <span data-ttu-id="9b375-233">對</span><span class="sxs-lookup"><span data-stu-id="9b375-233">True</span></span>                              |
| <span data-ttu-id="9b375-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9b375-234">In Global Catalog</span></span>      | <span data-ttu-id="9b375-235">否</span><span class="sxs-lookup"><span data-stu-id="9b375-235">False</span></span>                             |
| <span data-ttu-id="9b375-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9b375-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b375-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9b375-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9b375-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b375-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9b375-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b375-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9b375-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b375-240">Search-Flags</span></span>           | <span data-ttu-id="9b375-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b375-241">0x00000001</span></span>                        |
| <span data-ttu-id="9b375-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b375-242">System-Flags</span></span>           | <span data-ttu-id="9b375-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b375-243">0x00000010</span></span>                        |
| <span data-ttu-id="9b375-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9b375-244">Classes used in</span></span>        | [<span data-ttu-id="9b375-245">**User**</span><span class="sxs-lookup"><span data-stu-id="9b375-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9b375-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b375-246">Windows Server 2012</span></span>



| <span data-ttu-id="9b375-247">進入</span><span class="sxs-lookup"><span data-stu-id="9b375-247">Entry</span></span> | <span data-ttu-id="9b375-248">值</span><span class="sxs-lookup"><span data-stu-id="9b375-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="9b375-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9b375-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="9b375-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9b375-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="9b375-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9b375-251">System-Only</span></span>            | <span data-ttu-id="9b375-252">對</span><span class="sxs-lookup"><span data-stu-id="9b375-252">True</span></span>                              |
| <span data-ttu-id="9b375-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9b375-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9b375-254">對</span><span class="sxs-lookup"><span data-stu-id="9b375-254">True</span></span>                              |
| <span data-ttu-id="9b375-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9b375-255">Is Indexed</span></span>             | <span data-ttu-id="9b375-256">對</span><span class="sxs-lookup"><span data-stu-id="9b375-256">True</span></span>                              |
| <span data-ttu-id="9b375-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9b375-257">In Global Catalog</span></span>      | <span data-ttu-id="9b375-258">否</span><span class="sxs-lookup"><span data-stu-id="9b375-258">False</span></span>                             |
| <span data-ttu-id="9b375-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9b375-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9b375-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9b375-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="9b375-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9b375-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="9b375-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9b375-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="9b375-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9b375-263">Search-Flags</span></span>           | <span data-ttu-id="9b375-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9b375-264">0x00000001</span></span>                        |
| <span data-ttu-id="9b375-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9b375-265">System-Flags</span></span>           | <span data-ttu-id="9b375-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9b375-266">0x00000010</span></span>                        |
| <span data-ttu-id="9b375-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9b375-267">Classes used in</span></span>        | [<span data-ttu-id="9b375-268">**User**</span><span class="sxs-lookup"><span data-stu-id="9b375-268">**User**</span></span>](c-user.md)<br/> |



 

 





