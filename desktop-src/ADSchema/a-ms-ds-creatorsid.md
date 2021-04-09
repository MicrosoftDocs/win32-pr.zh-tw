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
# <a name="ms-ds-creator-sid-attribute"></a><span data-ttu-id="f433f-105">MS DS-Creator-SID 屬性</span><span class="sxs-lookup"><span data-stu-id="f433f-105">MS-DS-Creator-SID attribute</span></span>

<span data-ttu-id="f433f-106">包含此屬性之物件的建立者的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="f433f-106">The security ID of the creator of the object that contains this attribute.</span></span>



| <span data-ttu-id="f433f-107">進入</span><span class="sxs-lookup"><span data-stu-id="f433f-107">Entry</span></span> | <span data-ttu-id="f433f-108">值</span><span class="sxs-lookup"><span data-stu-id="f433f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f433f-109">CN</span><span class="sxs-lookup"><span data-stu-id="f433f-109">CN</span></span>                | <span data-ttu-id="f433f-110">MS-DS-Creator-SID</span><span class="sxs-lookup"><span data-stu-id="f433f-110">MS-DS-Creator-SID</span></span>                    |
| <span data-ttu-id="f433f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f433f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f433f-112">CreatorSID</span><span class="sxs-lookup"><span data-stu-id="f433f-112">mS-DS-CreatorSID</span></span>                     |
| <span data-ttu-id="f433f-113">大小</span><span class="sxs-lookup"><span data-stu-id="f433f-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="f433f-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f433f-114">Update Privilege</span></span>  | <span data-ttu-id="f433f-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="f433f-115">This value is set by the system.</span></span>     |
| <span data-ttu-id="f433f-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f433f-116">Update Frequency</span></span>  | <span data-ttu-id="f433f-117">每次建立新的物件時。</span><span class="sxs-lookup"><span data-stu-id="f433f-117">Whenever a new object is created.</span></span>    |
| <span data-ttu-id="f433f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f433f-118">Attribute-Id</span></span>      | <span data-ttu-id="f433f-119">1.2.840.113556.1.4.1410</span><span class="sxs-lookup"><span data-stu-id="f433f-119">1.2.840.113556.1.4.1410</span></span>              |
| <span data-ttu-id="f433f-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f433f-120">System-Id-Guid</span></span>    | <span data-ttu-id="f433f-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="f433f-121">c5e60132-1480-11d3-91c1-0000f87a57d4</span></span> |
| <span data-ttu-id="f433f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f433f-122">Syntax</span></span>            | [<span data-ttu-id="f433f-123">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="f433f-123">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="f433f-124">實作</span><span class="sxs-lookup"><span data-stu-id="f433f-124">Implementations</span></span>

-   [<span data-ttu-id="f433f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f433f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f433f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f433f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f433f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f433f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f433f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f433f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f433f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f433f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f433f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f433f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f433f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f433f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f433f-132">進入</span><span class="sxs-lookup"><span data-stu-id="f433f-132">Entry</span></span> | <span data-ttu-id="f433f-133">值</span><span class="sxs-lookup"><span data-stu-id="f433f-133">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f433f-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f433f-134">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f433f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f433f-135">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f433f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f433f-136">System-Only</span></span>            | <span data-ttu-id="f433f-137">對</span><span class="sxs-lookup"><span data-stu-id="f433f-137">True</span></span>                              |
| <span data-ttu-id="f433f-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f433f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f433f-139">對</span><span class="sxs-lookup"><span data-stu-id="f433f-139">True</span></span>                              |
| <span data-ttu-id="f433f-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f433f-140">Is Indexed</span></span>             | <span data-ttu-id="f433f-141">對</span><span class="sxs-lookup"><span data-stu-id="f433f-141">True</span></span>                              |
| <span data-ttu-id="f433f-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f433f-142">In Global Catalog</span></span>      | <span data-ttu-id="f433f-143">否</span><span class="sxs-lookup"><span data-stu-id="f433f-143">False</span></span>                             |
| <span data-ttu-id="f433f-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f433f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f433f-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f433f-145">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f433f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f433f-146">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f433f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f433f-147">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f433f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f433f-148">Search-Flags</span></span>           | <span data-ttu-id="f433f-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f433f-149">0x00000001</span></span>                        |
| <span data-ttu-id="f433f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f433f-150">System-Flags</span></span>           | <span data-ttu-id="f433f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f433f-151">0x00000010</span></span>                        |
| <span data-ttu-id="f433f-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f433f-152">Classes used in</span></span>        | [<span data-ttu-id="f433f-153">**User**</span><span class="sxs-lookup"><span data-stu-id="f433f-153">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f433f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f433f-154">Windows Server 2003</span></span>



| <span data-ttu-id="f433f-155">進入</span><span class="sxs-lookup"><span data-stu-id="f433f-155">Entry</span></span> | <span data-ttu-id="f433f-156">值</span><span class="sxs-lookup"><span data-stu-id="f433f-156">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f433f-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f433f-157">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f433f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f433f-158">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f433f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f433f-159">System-Only</span></span>            | <span data-ttu-id="f433f-160">對</span><span class="sxs-lookup"><span data-stu-id="f433f-160">True</span></span>                              |
| <span data-ttu-id="f433f-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f433f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f433f-162">對</span><span class="sxs-lookup"><span data-stu-id="f433f-162">True</span></span>                              |
| <span data-ttu-id="f433f-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f433f-163">Is Indexed</span></span>             | <span data-ttu-id="f433f-164">對</span><span class="sxs-lookup"><span data-stu-id="f433f-164">True</span></span>                              |
| <span data-ttu-id="f433f-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f433f-165">In Global Catalog</span></span>      | <span data-ttu-id="f433f-166">否</span><span class="sxs-lookup"><span data-stu-id="f433f-166">False</span></span>                             |
| <span data-ttu-id="f433f-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f433f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f433f-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f433f-168">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f433f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f433f-169">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f433f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f433f-170">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f433f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f433f-171">Search-Flags</span></span>           | <span data-ttu-id="f433f-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f433f-172">0x00000001</span></span>                        |
| <span data-ttu-id="f433f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f433f-173">System-Flags</span></span>           | <span data-ttu-id="f433f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f433f-174">0x00000010</span></span>                        |
| <span data-ttu-id="f433f-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f433f-175">Classes used in</span></span>        | [<span data-ttu-id="f433f-176">**User**</span><span class="sxs-lookup"><span data-stu-id="f433f-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f433f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f433f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f433f-178">進入</span><span class="sxs-lookup"><span data-stu-id="f433f-178">Entry</span></span> | <span data-ttu-id="f433f-179">值</span><span class="sxs-lookup"><span data-stu-id="f433f-179">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f433f-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f433f-180">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f433f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f433f-181">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f433f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f433f-182">System-Only</span></span>            | <span data-ttu-id="f433f-183">對</span><span class="sxs-lookup"><span data-stu-id="f433f-183">True</span></span>                              |
| <span data-ttu-id="f433f-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f433f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f433f-185">對</span><span class="sxs-lookup"><span data-stu-id="f433f-185">True</span></span>                              |
| <span data-ttu-id="f433f-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f433f-186">Is Indexed</span></span>             | <span data-ttu-id="f433f-187">對</span><span class="sxs-lookup"><span data-stu-id="f433f-187">True</span></span>                              |
| <span data-ttu-id="f433f-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f433f-188">In Global Catalog</span></span>      | <span data-ttu-id="f433f-189">否</span><span class="sxs-lookup"><span data-stu-id="f433f-189">False</span></span>                             |
| <span data-ttu-id="f433f-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f433f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f433f-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f433f-191">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f433f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f433f-192">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f433f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f433f-193">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f433f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f433f-194">Search-Flags</span></span>           | <span data-ttu-id="f433f-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f433f-195">0x00000001</span></span>                        |
| <span data-ttu-id="f433f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f433f-196">System-Flags</span></span>           | <span data-ttu-id="f433f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f433f-197">0x00000010</span></span>                        |
| <span data-ttu-id="f433f-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f433f-198">Classes used in</span></span>        | [<span data-ttu-id="f433f-199">**User**</span><span class="sxs-lookup"><span data-stu-id="f433f-199">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f433f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f433f-200">Windows Server 2008</span></span>



| <span data-ttu-id="f433f-201">進入</span><span class="sxs-lookup"><span data-stu-id="f433f-201">Entry</span></span> | <span data-ttu-id="f433f-202">值</span><span class="sxs-lookup"><span data-stu-id="f433f-202">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f433f-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f433f-203">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f433f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f433f-204">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f433f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="f433f-205">System-Only</span></span>            | <span data-ttu-id="f433f-206">對</span><span class="sxs-lookup"><span data-stu-id="f433f-206">True</span></span>                              |
| <span data-ttu-id="f433f-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f433f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="f433f-208">對</span><span class="sxs-lookup"><span data-stu-id="f433f-208">True</span></span>                              |
| <span data-ttu-id="f433f-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f433f-209">Is Indexed</span></span>             | <span data-ttu-id="f433f-210">對</span><span class="sxs-lookup"><span data-stu-id="f433f-210">True</span></span>                              |
| <span data-ttu-id="f433f-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f433f-211">In Global Catalog</span></span>      | <span data-ttu-id="f433f-212">否</span><span class="sxs-lookup"><span data-stu-id="f433f-212">False</span></span>                             |
| <span data-ttu-id="f433f-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f433f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="f433f-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f433f-214">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f433f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f433f-215">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f433f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f433f-216">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f433f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f433f-217">Search-Flags</span></span>           | <span data-ttu-id="f433f-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f433f-218">0x00000001</span></span>                        |
| <span data-ttu-id="f433f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f433f-219">System-Flags</span></span>           | <span data-ttu-id="f433f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f433f-220">0x00000010</span></span>                        |
| <span data-ttu-id="f433f-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f433f-221">Classes used in</span></span>        | [<span data-ttu-id="f433f-222">**User**</span><span class="sxs-lookup"><span data-stu-id="f433f-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f433f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f433f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f433f-224">進入</span><span class="sxs-lookup"><span data-stu-id="f433f-224">Entry</span></span> | <span data-ttu-id="f433f-225">值</span><span class="sxs-lookup"><span data-stu-id="f433f-225">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f433f-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f433f-226">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f433f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f433f-227">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f433f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="f433f-228">System-Only</span></span>            | <span data-ttu-id="f433f-229">對</span><span class="sxs-lookup"><span data-stu-id="f433f-229">True</span></span>                              |
| <span data-ttu-id="f433f-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f433f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="f433f-231">對</span><span class="sxs-lookup"><span data-stu-id="f433f-231">True</span></span>                              |
| <span data-ttu-id="f433f-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f433f-232">Is Indexed</span></span>             | <span data-ttu-id="f433f-233">對</span><span class="sxs-lookup"><span data-stu-id="f433f-233">True</span></span>                              |
| <span data-ttu-id="f433f-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f433f-234">In Global Catalog</span></span>      | <span data-ttu-id="f433f-235">否</span><span class="sxs-lookup"><span data-stu-id="f433f-235">False</span></span>                             |
| <span data-ttu-id="f433f-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f433f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="f433f-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f433f-237">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f433f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f433f-238">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f433f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f433f-239">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f433f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f433f-240">Search-Flags</span></span>           | <span data-ttu-id="f433f-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f433f-241">0x00000001</span></span>                        |
| <span data-ttu-id="f433f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f433f-242">System-Flags</span></span>           | <span data-ttu-id="f433f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f433f-243">0x00000010</span></span>                        |
| <span data-ttu-id="f433f-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f433f-244">Classes used in</span></span>        | [<span data-ttu-id="f433f-245">**User**</span><span class="sxs-lookup"><span data-stu-id="f433f-245">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f433f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f433f-246">Windows Server 2012</span></span>



| <span data-ttu-id="f433f-247">進入</span><span class="sxs-lookup"><span data-stu-id="f433f-247">Entry</span></span> | <span data-ttu-id="f433f-248">值</span><span class="sxs-lookup"><span data-stu-id="f433f-248">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f433f-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f433f-249">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f433f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f433f-250">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f433f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="f433f-251">System-Only</span></span>            | <span data-ttu-id="f433f-252">對</span><span class="sxs-lookup"><span data-stu-id="f433f-252">True</span></span>                              |
| <span data-ttu-id="f433f-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f433f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="f433f-254">對</span><span class="sxs-lookup"><span data-stu-id="f433f-254">True</span></span>                              |
| <span data-ttu-id="f433f-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f433f-255">Is Indexed</span></span>             | <span data-ttu-id="f433f-256">對</span><span class="sxs-lookup"><span data-stu-id="f433f-256">True</span></span>                              |
| <span data-ttu-id="f433f-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f433f-257">In Global Catalog</span></span>      | <span data-ttu-id="f433f-258">否</span><span class="sxs-lookup"><span data-stu-id="f433f-258">False</span></span>                             |
| <span data-ttu-id="f433f-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f433f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="f433f-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f433f-260">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f433f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f433f-261">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f433f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f433f-262">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f433f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f433f-263">Search-Flags</span></span>           | <span data-ttu-id="f433f-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f433f-264">0x00000001</span></span>                        |
| <span data-ttu-id="f433f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f433f-265">System-Flags</span></span>           | <span data-ttu-id="f433f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f433f-266">0x00000010</span></span>                        |
| <span data-ttu-id="f433f-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f433f-267">Classes used in</span></span>        | [<span data-ttu-id="f433f-268">**User**</span><span class="sxs-lookup"><span data-stu-id="f433f-268">**User**</span></span>](c-user.md)<br/> |



 

 





