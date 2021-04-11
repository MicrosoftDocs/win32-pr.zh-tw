---
title: DMD-Name 屬性
description: 用來識別架構資料分割的名稱。 AD 未使用。
ms.assetid: 0ee35c32-add7-4b20-8d83-59b4b91df6ad
ms.tgt_platform: multiple
keywords:
- DMD-Name 屬性 AD 架構
- dmdName 屬性 AD 架構
topic_type:
- apiref
api_name:
- DMD-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25684af133748ca73c8ace31b0471a5d1e0a787
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935256"
---
# <a name="dmd-name-attribute"></a><span data-ttu-id="d03a5-106">DMD-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="d03a5-106">DMD-Name attribute</span></span>

<span data-ttu-id="d03a5-107">用來識別架構資料分割的名稱。</span><span class="sxs-lookup"><span data-stu-id="d03a5-107">A name used to identify the schema partition.</span></span> <span data-ttu-id="d03a5-108">AD 未使用。</span><span class="sxs-lookup"><span data-stu-id="d03a5-108">Not used by AD.</span></span>



| <span data-ttu-id="d03a5-109">進入</span><span class="sxs-lookup"><span data-stu-id="d03a5-109">Entry</span></span> | <span data-ttu-id="d03a5-110">值</span><span class="sxs-lookup"><span data-stu-id="d03a5-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d03a5-111">CN</span><span class="sxs-lookup"><span data-stu-id="d03a5-111">CN</span></span>                | <span data-ttu-id="d03a5-112">DMD-Name</span><span class="sxs-lookup"><span data-stu-id="d03a5-112">DMD-Name</span></span>                                    |
| <span data-ttu-id="d03a5-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d03a5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="d03a5-114">dmdName</span><span class="sxs-lookup"><span data-stu-id="d03a5-114">dmdName</span></span>                                     |
| <span data-ttu-id="d03a5-115">大小</span><span class="sxs-lookup"><span data-stu-id="d03a5-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="d03a5-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d03a5-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="d03a5-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d03a5-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="d03a5-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d03a5-118">Attribute-Id</span></span>      | <span data-ttu-id="d03a5-119">1.2.840.113556.1.2.598</span><span class="sxs-lookup"><span data-stu-id="d03a5-119">1.2.840.113556.1.2.598</span></span>                      |
| <span data-ttu-id="d03a5-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d03a5-120">System-Id-Guid</span></span>    | <span data-ttu-id="d03a5-121">167757b9-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d03a5-121">167757b9-47f3-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="d03a5-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d03a5-122">Syntax</span></span>            | [<span data-ttu-id="d03a5-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="d03a5-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d03a5-124">實作</span><span class="sxs-lookup"><span data-stu-id="d03a5-124">Implementations</span></span>

-   [<span data-ttu-id="d03a5-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d03a5-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d03a5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d03a5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d03a5-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="d03a5-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d03a5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d03a5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d03a5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d03a5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d03a5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d03a5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d03a5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d03a5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d03a5-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d03a5-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d03a5-133">進入</span><span class="sxs-lookup"><span data-stu-id="d03a5-133">Entry</span></span> | <span data-ttu-id="d03a5-134">值</span><span class="sxs-lookup"><span data-stu-id="d03a5-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d03a5-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d03a5-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d03a5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d03a5-136">MAPI-Id</span></span>                | <span data-ttu-id="d03a5-137">0x8C56</span><span class="sxs-lookup"><span data-stu-id="d03a5-137">0x8C56</span></span>                          |
| <span data-ttu-id="d03a5-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="d03a5-138">System-Only</span></span>            | <span data-ttu-id="d03a5-139">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-139">False</span></span>                           |
| <span data-ttu-id="d03a5-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d03a5-140">Is-Single-Valued</span></span>       | <span data-ttu-id="d03a5-141">對</span><span class="sxs-lookup"><span data-stu-id="d03a5-141">True</span></span>                            |
| <span data-ttu-id="d03a5-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d03a5-142">Is Indexed</span></span>             | <span data-ttu-id="d03a5-143">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-143">False</span></span>                           |
| <span data-ttu-id="d03a5-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d03a5-144">In Global Catalog</span></span>      | <span data-ttu-id="d03a5-145">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-145">False</span></span>                           |
| <span data-ttu-id="d03a5-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d03a5-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="d03a5-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d03a5-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d03a5-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d03a5-148">Range-Lower</span></span>            | <span data-ttu-id="d03a5-149">1</span><span class="sxs-lookup"><span data-stu-id="d03a5-149">1</span></span>                               |
| <span data-ttu-id="d03a5-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d03a5-150">Range-Upper</span></span>            | <span data-ttu-id="d03a5-151">1024</span><span class="sxs-lookup"><span data-stu-id="d03a5-151">1024</span></span>                            |
| <span data-ttu-id="d03a5-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-152">Search-Flags</span></span>           | <span data-ttu-id="d03a5-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d03a5-153">0x00000000</span></span>                      |
| <span data-ttu-id="d03a5-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-154">System-Flags</span></span>           | <span data-ttu-id="d03a5-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d03a5-155">0x00000010</span></span>                      |
| <span data-ttu-id="d03a5-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d03a5-156">Classes used in</span></span>        | [<span data-ttu-id="d03a5-157">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="d03a5-157">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d03a5-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d03a5-158">Windows Server 2003</span></span>



| <span data-ttu-id="d03a5-159">進入</span><span class="sxs-lookup"><span data-stu-id="d03a5-159">Entry</span></span> | <span data-ttu-id="d03a5-160">值</span><span class="sxs-lookup"><span data-stu-id="d03a5-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d03a5-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d03a5-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d03a5-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d03a5-162">MAPI-Id</span></span>                | <span data-ttu-id="d03a5-163">0x8C56</span><span class="sxs-lookup"><span data-stu-id="d03a5-163">0x8C56</span></span>                          |
| <span data-ttu-id="d03a5-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="d03a5-164">System-Only</span></span>            | <span data-ttu-id="d03a5-165">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-165">False</span></span>                           |
| <span data-ttu-id="d03a5-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d03a5-166">Is-Single-Valued</span></span>       | <span data-ttu-id="d03a5-167">對</span><span class="sxs-lookup"><span data-stu-id="d03a5-167">True</span></span>                            |
| <span data-ttu-id="d03a5-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d03a5-168">Is Indexed</span></span>             | <span data-ttu-id="d03a5-169">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-169">False</span></span>                           |
| <span data-ttu-id="d03a5-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d03a5-170">In Global Catalog</span></span>      | <span data-ttu-id="d03a5-171">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-171">False</span></span>                           |
| <span data-ttu-id="d03a5-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d03a5-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="d03a5-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d03a5-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d03a5-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d03a5-174">Range-Lower</span></span>            | <span data-ttu-id="d03a5-175">1</span><span class="sxs-lookup"><span data-stu-id="d03a5-175">1</span></span>                               |
| <span data-ttu-id="d03a5-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d03a5-176">Range-Upper</span></span>            | <span data-ttu-id="d03a5-177">1024</span><span class="sxs-lookup"><span data-stu-id="d03a5-177">1024</span></span>                            |
| <span data-ttu-id="d03a5-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-178">Search-Flags</span></span>           | <span data-ttu-id="d03a5-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d03a5-179">0x00000000</span></span>                      |
| <span data-ttu-id="d03a5-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-180">System-Flags</span></span>           | <span data-ttu-id="d03a5-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d03a5-181">0x00000010</span></span>                      |
| <span data-ttu-id="d03a5-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d03a5-182">Classes used in</span></span>        | [<span data-ttu-id="d03a5-183">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="d03a5-183">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d03a5-184">亞當</span><span class="sxs-lookup"><span data-stu-id="d03a5-184">ADAM</span></span>



| <span data-ttu-id="d03a5-185">進入</span><span class="sxs-lookup"><span data-stu-id="d03a5-185">Entry</span></span> | <span data-ttu-id="d03a5-186">值</span><span class="sxs-lookup"><span data-stu-id="d03a5-186">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d03a5-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d03a5-187">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d03a5-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d03a5-188">MAPI-Id</span></span>                | <span data-ttu-id="d03a5-189">0x8C56</span><span class="sxs-lookup"><span data-stu-id="d03a5-189">0x8C56</span></span>                          |
| <span data-ttu-id="d03a5-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="d03a5-190">System-Only</span></span>            | <span data-ttu-id="d03a5-191">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-191">False</span></span>                           |
| <span data-ttu-id="d03a5-192">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d03a5-192">Is-Single-Valued</span></span>       | <span data-ttu-id="d03a5-193">對</span><span class="sxs-lookup"><span data-stu-id="d03a5-193">True</span></span>                            |
| <span data-ttu-id="d03a5-194">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d03a5-194">Is Indexed</span></span>             | <span data-ttu-id="d03a5-195">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-195">False</span></span>                           |
| <span data-ttu-id="d03a5-196">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d03a5-196">In Global Catalog</span></span>      | <span data-ttu-id="d03a5-197">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-197">False</span></span>                           |
| <span data-ttu-id="d03a5-198">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d03a5-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="d03a5-199">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d03a5-199">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d03a5-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d03a5-200">Range-Lower</span></span>            | <span data-ttu-id="d03a5-201">1</span><span class="sxs-lookup"><span data-stu-id="d03a5-201">1</span></span>                               |
| <span data-ttu-id="d03a5-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d03a5-202">Range-Upper</span></span>            | <span data-ttu-id="d03a5-203">1024</span><span class="sxs-lookup"><span data-stu-id="d03a5-203">1024</span></span>                            |
| <span data-ttu-id="d03a5-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-204">Search-Flags</span></span>           | <span data-ttu-id="d03a5-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d03a5-205">0x00000000</span></span>                      |
| <span data-ttu-id="d03a5-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-206">System-Flags</span></span>           | <span data-ttu-id="d03a5-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d03a5-207">0x00000010</span></span>                      |
| <span data-ttu-id="d03a5-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d03a5-208">Classes used in</span></span>        | [<span data-ttu-id="d03a5-209">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="d03a5-209">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d03a5-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d03a5-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d03a5-211">進入</span><span class="sxs-lookup"><span data-stu-id="d03a5-211">Entry</span></span> | <span data-ttu-id="d03a5-212">值</span><span class="sxs-lookup"><span data-stu-id="d03a5-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d03a5-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d03a5-213">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d03a5-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d03a5-214">MAPI-Id</span></span>                | <span data-ttu-id="d03a5-215">0x8C56</span><span class="sxs-lookup"><span data-stu-id="d03a5-215">0x8C56</span></span>                          |
| <span data-ttu-id="d03a5-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="d03a5-216">System-Only</span></span>            | <span data-ttu-id="d03a5-217">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-217">False</span></span>                           |
| <span data-ttu-id="d03a5-218">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d03a5-218">Is-Single-Valued</span></span>       | <span data-ttu-id="d03a5-219">對</span><span class="sxs-lookup"><span data-stu-id="d03a5-219">True</span></span>                            |
| <span data-ttu-id="d03a5-220">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d03a5-220">Is Indexed</span></span>             | <span data-ttu-id="d03a5-221">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-221">False</span></span>                           |
| <span data-ttu-id="d03a5-222">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d03a5-222">In Global Catalog</span></span>      | <span data-ttu-id="d03a5-223">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-223">False</span></span>                           |
| <span data-ttu-id="d03a5-224">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d03a5-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="d03a5-225">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d03a5-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d03a5-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d03a5-226">Range-Lower</span></span>            | <span data-ttu-id="d03a5-227">1</span><span class="sxs-lookup"><span data-stu-id="d03a5-227">1</span></span>                               |
| <span data-ttu-id="d03a5-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d03a5-228">Range-Upper</span></span>            | <span data-ttu-id="d03a5-229">1024</span><span class="sxs-lookup"><span data-stu-id="d03a5-229">1024</span></span>                            |
| <span data-ttu-id="d03a5-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-230">Search-Flags</span></span>           | <span data-ttu-id="d03a5-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d03a5-231">0x00000000</span></span>                      |
| <span data-ttu-id="d03a5-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-232">System-Flags</span></span>           | <span data-ttu-id="d03a5-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d03a5-233">0x00000010</span></span>                      |
| <span data-ttu-id="d03a5-234">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d03a5-234">Classes used in</span></span>        | [<span data-ttu-id="d03a5-235">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="d03a5-235">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d03a5-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d03a5-236">Windows Server 2008</span></span>



| <span data-ttu-id="d03a5-237">進入</span><span class="sxs-lookup"><span data-stu-id="d03a5-237">Entry</span></span> | <span data-ttu-id="d03a5-238">值</span><span class="sxs-lookup"><span data-stu-id="d03a5-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d03a5-239">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d03a5-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d03a5-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d03a5-240">MAPI-Id</span></span>                | <span data-ttu-id="d03a5-241">0x8C56</span><span class="sxs-lookup"><span data-stu-id="d03a5-241">0x8C56</span></span>                          |
| <span data-ttu-id="d03a5-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="d03a5-242">System-Only</span></span>            | <span data-ttu-id="d03a5-243">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-243">False</span></span>                           |
| <span data-ttu-id="d03a5-244">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d03a5-244">Is-Single-Valued</span></span>       | <span data-ttu-id="d03a5-245">對</span><span class="sxs-lookup"><span data-stu-id="d03a5-245">True</span></span>                            |
| <span data-ttu-id="d03a5-246">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d03a5-246">Is Indexed</span></span>             | <span data-ttu-id="d03a5-247">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-247">False</span></span>                           |
| <span data-ttu-id="d03a5-248">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d03a5-248">In Global Catalog</span></span>      | <span data-ttu-id="d03a5-249">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-249">False</span></span>                           |
| <span data-ttu-id="d03a5-250">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d03a5-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="d03a5-251">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d03a5-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d03a5-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d03a5-252">Range-Lower</span></span>            | <span data-ttu-id="d03a5-253">1</span><span class="sxs-lookup"><span data-stu-id="d03a5-253">1</span></span>                               |
| <span data-ttu-id="d03a5-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d03a5-254">Range-Upper</span></span>            | <span data-ttu-id="d03a5-255">1024</span><span class="sxs-lookup"><span data-stu-id="d03a5-255">1024</span></span>                            |
| <span data-ttu-id="d03a5-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-256">Search-Flags</span></span>           | <span data-ttu-id="d03a5-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d03a5-257">0x00000000</span></span>                      |
| <span data-ttu-id="d03a5-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-258">System-Flags</span></span>           | <span data-ttu-id="d03a5-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d03a5-259">0x00000010</span></span>                      |
| <span data-ttu-id="d03a5-260">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d03a5-260">Classes used in</span></span>        | [<span data-ttu-id="d03a5-261">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="d03a5-261">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d03a5-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d03a5-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d03a5-263">進入</span><span class="sxs-lookup"><span data-stu-id="d03a5-263">Entry</span></span> | <span data-ttu-id="d03a5-264">值</span><span class="sxs-lookup"><span data-stu-id="d03a5-264">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d03a5-265">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d03a5-265">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d03a5-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d03a5-266">MAPI-Id</span></span>                | <span data-ttu-id="d03a5-267">0x8C56</span><span class="sxs-lookup"><span data-stu-id="d03a5-267">0x8C56</span></span>                          |
| <span data-ttu-id="d03a5-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="d03a5-268">System-Only</span></span>            | <span data-ttu-id="d03a5-269">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-269">False</span></span>                           |
| <span data-ttu-id="d03a5-270">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d03a5-270">Is-Single-Valued</span></span>       | <span data-ttu-id="d03a5-271">對</span><span class="sxs-lookup"><span data-stu-id="d03a5-271">True</span></span>                            |
| <span data-ttu-id="d03a5-272">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d03a5-272">Is Indexed</span></span>             | <span data-ttu-id="d03a5-273">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-273">False</span></span>                           |
| <span data-ttu-id="d03a5-274">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d03a5-274">In Global Catalog</span></span>      | <span data-ttu-id="d03a5-275">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-275">False</span></span>                           |
| <span data-ttu-id="d03a5-276">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d03a5-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="d03a5-277">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d03a5-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d03a5-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d03a5-278">Range-Lower</span></span>            | <span data-ttu-id="d03a5-279">1</span><span class="sxs-lookup"><span data-stu-id="d03a5-279">1</span></span>                               |
| <span data-ttu-id="d03a5-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d03a5-280">Range-Upper</span></span>            | <span data-ttu-id="d03a5-281">1024</span><span class="sxs-lookup"><span data-stu-id="d03a5-281">1024</span></span>                            |
| <span data-ttu-id="d03a5-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-282">Search-Flags</span></span>           | <span data-ttu-id="d03a5-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d03a5-283">0x00000000</span></span>                      |
| <span data-ttu-id="d03a5-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-284">System-Flags</span></span>           | <span data-ttu-id="d03a5-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d03a5-285">0x00000010</span></span>                      |
| <span data-ttu-id="d03a5-286">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d03a5-286">Classes used in</span></span>        | [<span data-ttu-id="d03a5-287">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="d03a5-287">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d03a5-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d03a5-288">Windows Server 2012</span></span>



| <span data-ttu-id="d03a5-289">進入</span><span class="sxs-lookup"><span data-stu-id="d03a5-289">Entry</span></span> | <span data-ttu-id="d03a5-290">值</span><span class="sxs-lookup"><span data-stu-id="d03a5-290">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d03a5-291">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d03a5-291">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d03a5-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d03a5-292">MAPI-Id</span></span>                | <span data-ttu-id="d03a5-293">0x8C56</span><span class="sxs-lookup"><span data-stu-id="d03a5-293">0x8C56</span></span>                          |
| <span data-ttu-id="d03a5-294">System-Only</span><span class="sxs-lookup"><span data-stu-id="d03a5-294">System-Only</span></span>            | <span data-ttu-id="d03a5-295">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-295">False</span></span>                           |
| <span data-ttu-id="d03a5-296">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d03a5-296">Is-Single-Valued</span></span>       | <span data-ttu-id="d03a5-297">對</span><span class="sxs-lookup"><span data-stu-id="d03a5-297">True</span></span>                            |
| <span data-ttu-id="d03a5-298">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d03a5-298">Is Indexed</span></span>             | <span data-ttu-id="d03a5-299">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-299">False</span></span>                           |
| <span data-ttu-id="d03a5-300">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d03a5-300">In Global Catalog</span></span>      | <span data-ttu-id="d03a5-301">否</span><span class="sxs-lookup"><span data-stu-id="d03a5-301">False</span></span>                           |
| <span data-ttu-id="d03a5-302">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d03a5-302">NT-Security-Descriptor</span></span> | <span data-ttu-id="d03a5-303">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d03a5-303">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d03a5-304">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d03a5-304">Range-Lower</span></span>            | <span data-ttu-id="d03a5-305">1</span><span class="sxs-lookup"><span data-stu-id="d03a5-305">1</span></span>                               |
| <span data-ttu-id="d03a5-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d03a5-306">Range-Upper</span></span>            | <span data-ttu-id="d03a5-307">1024</span><span class="sxs-lookup"><span data-stu-id="d03a5-307">1024</span></span>                            |
| <span data-ttu-id="d03a5-308">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-308">Search-Flags</span></span>           | <span data-ttu-id="d03a5-309">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d03a5-309">0x00000000</span></span>                      |
| <span data-ttu-id="d03a5-310">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d03a5-310">System-Flags</span></span>           | <span data-ttu-id="d03a5-311">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d03a5-311">0x00000010</span></span>                      |
| <span data-ttu-id="d03a5-312">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d03a5-312">Classes used in</span></span>        | [<span data-ttu-id="d03a5-313">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="d03a5-313">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





