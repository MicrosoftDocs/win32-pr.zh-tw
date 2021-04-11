---
title: USN-Source 屬性
description: 從複寫變更到本機伺服器之遠端目錄中物件的 USN-Changed 屬性值。
ms.assetid: b307f84a-3ab1-4bfa-afc2-e74055f2a652
ms.tgt_platform: multiple
keywords:
- USN-Source 屬性 AD 架構
- uSNSource 屬性 AD 架構
topic_type:
- apiref
api_name:
- USN-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0998ffb73fc02511d77440550c8c669b35a98563
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385362"
---
# <a name="usn-source-attribute"></a><span data-ttu-id="a6e35-105">USN-Source 屬性</span><span class="sxs-lookup"><span data-stu-id="a6e35-105">USN-Source attribute</span></span>

<span data-ttu-id="a6e35-106">從複寫變更至本機伺服器的遠端目錄中，已變更之物件的 [**USN 變更**](a-usnchanged.md) 屬性值。</span><span class="sxs-lookup"><span data-stu-id="a6e35-106">Value of the [**USN-Changed**](a-usnchanged.md) attribute of the object from the remote directory that replicated the change to the local server.</span></span>



| <span data-ttu-id="a6e35-107">進入</span><span class="sxs-lookup"><span data-stu-id="a6e35-107">Entry</span></span> | <span data-ttu-id="a6e35-108">值</span><span class="sxs-lookup"><span data-stu-id="a6e35-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6e35-109">CN</span><span class="sxs-lookup"><span data-stu-id="a6e35-109">CN</span></span>                | <span data-ttu-id="a6e35-110">USN-Source</span><span class="sxs-lookup"><span data-stu-id="a6e35-110">USN-Source</span></span>                                                                                          |
| <span data-ttu-id="a6e35-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a6e35-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a6e35-112">uSNSource</span><span class="sxs-lookup"><span data-stu-id="a6e35-112">uSNSource</span></span>                                                                                           |
| <span data-ttu-id="a6e35-113">大小</span><span class="sxs-lookup"><span data-stu-id="a6e35-113">Size</span></span>              | <span data-ttu-id="a6e35-114">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="a6e35-114">8 bytes</span></span>                                                                                             |
| <span data-ttu-id="a6e35-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a6e35-115">Update Privilege</span></span>  | <span data-ttu-id="a6e35-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="a6e35-116">This value is set by the system.</span></span>                                                                    |
| <span data-ttu-id="a6e35-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a6e35-117">Update Frequency</span></span>  | <span data-ttu-id="a6e35-118">當將變更複製到本機目錄的遠端目錄上的物件變更時。</span><span class="sxs-lookup"><span data-stu-id="a6e35-118">When the object is changed on a remote directory that replicated the change to the local directory.</span></span> |
| <span data-ttu-id="a6e35-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a6e35-119">Attribute-Id</span></span>      | <span data-ttu-id="a6e35-120">1.2.840.113556.1.4.896</span><span class="sxs-lookup"><span data-stu-id="a6e35-120">1.2.840.113556.1.4.896</span></span>                                                                              |
| <span data-ttu-id="a6e35-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a6e35-121">System-Id-Guid</span></span>    | <span data-ttu-id="a6e35-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a6e35-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span></span>                                                                |
| <span data-ttu-id="a6e35-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6e35-123">Syntax</span></span>            | [<span data-ttu-id="a6e35-124">**間隔**</span><span class="sxs-lookup"><span data-stu-id="a6e35-124">**Interval**</span></span>](s-interval.md)                                                                      |



## <a name="implementations"></a><span data-ttu-id="a6e35-125">實作</span><span class="sxs-lookup"><span data-stu-id="a6e35-125">Implementations</span></span>

-   [<span data-ttu-id="a6e35-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a6e35-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a6e35-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a6e35-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a6e35-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="a6e35-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a6e35-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a6e35-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a6e35-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a6e35-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a6e35-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a6e35-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a6e35-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a6e35-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a6e35-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a6e35-133">Windows 2000 Server</span></span>



| <span data-ttu-id="a6e35-134">進入</span><span class="sxs-lookup"><span data-stu-id="a6e35-134">Entry</span></span> | <span data-ttu-id="a6e35-135">值</span><span class="sxs-lookup"><span data-stu-id="a6e35-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a6e35-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6e35-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a6e35-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6e35-137">MAPI-Id</span></span>                | <span data-ttu-id="a6e35-138">0x8157</span><span class="sxs-lookup"><span data-stu-id="a6e35-138">0x8157</span></span>                          |
| <span data-ttu-id="a6e35-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6e35-139">System-Only</span></span>            | <span data-ttu-id="a6e35-140">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-140">False</span></span>                           |
| <span data-ttu-id="a6e35-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6e35-141">Is-Single-Valued</span></span>       | <span data-ttu-id="a6e35-142">對</span><span class="sxs-lookup"><span data-stu-id="a6e35-142">True</span></span>                            |
| <span data-ttu-id="a6e35-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6e35-143">Is Indexed</span></span>             | <span data-ttu-id="a6e35-144">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-144">False</span></span>                           |
| <span data-ttu-id="a6e35-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6e35-145">In Global Catalog</span></span>      | <span data-ttu-id="a6e35-146">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-146">False</span></span>                           |
| <span data-ttu-id="a6e35-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6e35-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6e35-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6e35-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a6e35-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6e35-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a6e35-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6e35-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a6e35-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-151">Search-Flags</span></span>           | <span data-ttu-id="a6e35-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6e35-152">0x00000000</span></span>                      |
| <span data-ttu-id="a6e35-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-153">System-Flags</span></span>           | <span data-ttu-id="a6e35-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6e35-154">0x00000010</span></span>                      |
| <span data-ttu-id="a6e35-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6e35-155">Classes used in</span></span>        | [<span data-ttu-id="a6e35-156">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a6e35-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a6e35-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a6e35-157">Windows Server 2003</span></span>



| <span data-ttu-id="a6e35-158">進入</span><span class="sxs-lookup"><span data-stu-id="a6e35-158">Entry</span></span> | <span data-ttu-id="a6e35-159">值</span><span class="sxs-lookup"><span data-stu-id="a6e35-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a6e35-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6e35-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a6e35-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6e35-161">MAPI-Id</span></span>                | <span data-ttu-id="a6e35-162">0x8157</span><span class="sxs-lookup"><span data-stu-id="a6e35-162">0x8157</span></span>                          |
| <span data-ttu-id="a6e35-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6e35-163">System-Only</span></span>            | <span data-ttu-id="a6e35-164">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-164">False</span></span>                           |
| <span data-ttu-id="a6e35-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6e35-165">Is-Single-Valued</span></span>       | <span data-ttu-id="a6e35-166">對</span><span class="sxs-lookup"><span data-stu-id="a6e35-166">True</span></span>                            |
| <span data-ttu-id="a6e35-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6e35-167">Is Indexed</span></span>             | <span data-ttu-id="a6e35-168">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-168">False</span></span>                           |
| <span data-ttu-id="a6e35-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6e35-169">In Global Catalog</span></span>      | <span data-ttu-id="a6e35-170">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-170">False</span></span>                           |
| <span data-ttu-id="a6e35-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6e35-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6e35-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6e35-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a6e35-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6e35-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a6e35-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6e35-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a6e35-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-175">Search-Flags</span></span>           | <span data-ttu-id="a6e35-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6e35-176">0x00000000</span></span>                      |
| <span data-ttu-id="a6e35-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-177">System-Flags</span></span>           | <span data-ttu-id="a6e35-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6e35-178">0x00000010</span></span>                      |
| <span data-ttu-id="a6e35-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6e35-179">Classes used in</span></span>        | [<span data-ttu-id="a6e35-180">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a6e35-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a6e35-181">亞當</span><span class="sxs-lookup"><span data-stu-id="a6e35-181">ADAM</span></span>



| <span data-ttu-id="a6e35-182">進入</span><span class="sxs-lookup"><span data-stu-id="a6e35-182">Entry</span></span> | <span data-ttu-id="a6e35-183">值</span><span class="sxs-lookup"><span data-stu-id="a6e35-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a6e35-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6e35-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a6e35-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6e35-185">MAPI-Id</span></span>                | <span data-ttu-id="a6e35-186">0x8157</span><span class="sxs-lookup"><span data-stu-id="a6e35-186">0x8157</span></span>                          |
| <span data-ttu-id="a6e35-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6e35-187">System-Only</span></span>            | <span data-ttu-id="a6e35-188">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-188">False</span></span>                           |
| <span data-ttu-id="a6e35-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6e35-189">Is-Single-Valued</span></span>       | <span data-ttu-id="a6e35-190">對</span><span class="sxs-lookup"><span data-stu-id="a6e35-190">True</span></span>                            |
| <span data-ttu-id="a6e35-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6e35-191">Is Indexed</span></span>             | <span data-ttu-id="a6e35-192">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-192">False</span></span>                           |
| <span data-ttu-id="a6e35-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6e35-193">In Global Catalog</span></span>      | <span data-ttu-id="a6e35-194">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-194">False</span></span>                           |
| <span data-ttu-id="a6e35-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6e35-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6e35-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6e35-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a6e35-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6e35-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a6e35-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6e35-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a6e35-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-199">Search-Flags</span></span>           | <span data-ttu-id="a6e35-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6e35-200">0x00000000</span></span>                      |
| <span data-ttu-id="a6e35-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-201">System-Flags</span></span>           | <span data-ttu-id="a6e35-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6e35-202">0x00000010</span></span>                      |
| <span data-ttu-id="a6e35-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6e35-203">Classes used in</span></span>        | [<span data-ttu-id="a6e35-204">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a6e35-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a6e35-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a6e35-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a6e35-206">進入</span><span class="sxs-lookup"><span data-stu-id="a6e35-206">Entry</span></span> | <span data-ttu-id="a6e35-207">值</span><span class="sxs-lookup"><span data-stu-id="a6e35-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a6e35-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6e35-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a6e35-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6e35-209">MAPI-Id</span></span>                | <span data-ttu-id="a6e35-210">0x8157</span><span class="sxs-lookup"><span data-stu-id="a6e35-210">0x8157</span></span>                          |
| <span data-ttu-id="a6e35-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6e35-211">System-Only</span></span>            | <span data-ttu-id="a6e35-212">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-212">False</span></span>                           |
| <span data-ttu-id="a6e35-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6e35-213">Is-Single-Valued</span></span>       | <span data-ttu-id="a6e35-214">對</span><span class="sxs-lookup"><span data-stu-id="a6e35-214">True</span></span>                            |
| <span data-ttu-id="a6e35-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6e35-215">Is Indexed</span></span>             | <span data-ttu-id="a6e35-216">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-216">False</span></span>                           |
| <span data-ttu-id="a6e35-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6e35-217">In Global Catalog</span></span>      | <span data-ttu-id="a6e35-218">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-218">False</span></span>                           |
| <span data-ttu-id="a6e35-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6e35-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6e35-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6e35-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a6e35-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6e35-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a6e35-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6e35-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a6e35-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-223">Search-Flags</span></span>           | <span data-ttu-id="a6e35-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6e35-224">0x00000000</span></span>                      |
| <span data-ttu-id="a6e35-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-225">System-Flags</span></span>           | <span data-ttu-id="a6e35-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6e35-226">0x00000010</span></span>                      |
| <span data-ttu-id="a6e35-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6e35-227">Classes used in</span></span>        | [<span data-ttu-id="a6e35-228">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a6e35-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a6e35-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6e35-229">Windows Server 2008</span></span>



| <span data-ttu-id="a6e35-230">進入</span><span class="sxs-lookup"><span data-stu-id="a6e35-230">Entry</span></span> | <span data-ttu-id="a6e35-231">值</span><span class="sxs-lookup"><span data-stu-id="a6e35-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a6e35-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6e35-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a6e35-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6e35-233">MAPI-Id</span></span>                | <span data-ttu-id="a6e35-234">0x8157</span><span class="sxs-lookup"><span data-stu-id="a6e35-234">0x8157</span></span>                          |
| <span data-ttu-id="a6e35-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6e35-235">System-Only</span></span>            | <span data-ttu-id="a6e35-236">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-236">False</span></span>                           |
| <span data-ttu-id="a6e35-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6e35-237">Is-Single-Valued</span></span>       | <span data-ttu-id="a6e35-238">對</span><span class="sxs-lookup"><span data-stu-id="a6e35-238">True</span></span>                            |
| <span data-ttu-id="a6e35-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6e35-239">Is Indexed</span></span>             | <span data-ttu-id="a6e35-240">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-240">False</span></span>                           |
| <span data-ttu-id="a6e35-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6e35-241">In Global Catalog</span></span>      | <span data-ttu-id="a6e35-242">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-242">False</span></span>                           |
| <span data-ttu-id="a6e35-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6e35-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6e35-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6e35-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a6e35-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6e35-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a6e35-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6e35-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a6e35-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-247">Search-Flags</span></span>           | <span data-ttu-id="a6e35-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6e35-248">0x00000000</span></span>                      |
| <span data-ttu-id="a6e35-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-249">System-Flags</span></span>           | <span data-ttu-id="a6e35-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6e35-250">0x00000010</span></span>                      |
| <span data-ttu-id="a6e35-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6e35-251">Classes used in</span></span>        | [<span data-ttu-id="a6e35-252">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a6e35-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a6e35-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a6e35-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a6e35-254">進入</span><span class="sxs-lookup"><span data-stu-id="a6e35-254">Entry</span></span> | <span data-ttu-id="a6e35-255">值</span><span class="sxs-lookup"><span data-stu-id="a6e35-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a6e35-256">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6e35-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a6e35-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6e35-257">MAPI-Id</span></span>                | <span data-ttu-id="a6e35-258">0x8157</span><span class="sxs-lookup"><span data-stu-id="a6e35-258">0x8157</span></span>                          |
| <span data-ttu-id="a6e35-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6e35-259">System-Only</span></span>            | <span data-ttu-id="a6e35-260">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-260">False</span></span>                           |
| <span data-ttu-id="a6e35-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6e35-261">Is-Single-Valued</span></span>       | <span data-ttu-id="a6e35-262">對</span><span class="sxs-lookup"><span data-stu-id="a6e35-262">True</span></span>                            |
| <span data-ttu-id="a6e35-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6e35-263">Is Indexed</span></span>             | <span data-ttu-id="a6e35-264">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-264">False</span></span>                           |
| <span data-ttu-id="a6e35-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6e35-265">In Global Catalog</span></span>      | <span data-ttu-id="a6e35-266">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-266">False</span></span>                           |
| <span data-ttu-id="a6e35-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6e35-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6e35-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6e35-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a6e35-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6e35-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a6e35-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6e35-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a6e35-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-271">Search-Flags</span></span>           | <span data-ttu-id="a6e35-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6e35-272">0x00000000</span></span>                      |
| <span data-ttu-id="a6e35-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-273">System-Flags</span></span>           | <span data-ttu-id="a6e35-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6e35-274">0x00000010</span></span>                      |
| <span data-ttu-id="a6e35-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6e35-275">Classes used in</span></span>        | [<span data-ttu-id="a6e35-276">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a6e35-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a6e35-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a6e35-277">Windows Server 2012</span></span>



| <span data-ttu-id="a6e35-278">進入</span><span class="sxs-lookup"><span data-stu-id="a6e35-278">Entry</span></span> | <span data-ttu-id="a6e35-279">值</span><span class="sxs-lookup"><span data-stu-id="a6e35-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a6e35-280">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6e35-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a6e35-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6e35-281">MAPI-Id</span></span>                | <span data-ttu-id="a6e35-282">0x8157</span><span class="sxs-lookup"><span data-stu-id="a6e35-282">0x8157</span></span>                          |
| <span data-ttu-id="a6e35-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6e35-283">System-Only</span></span>            | <span data-ttu-id="a6e35-284">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-284">False</span></span>                           |
| <span data-ttu-id="a6e35-285">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6e35-285">Is-Single-Valued</span></span>       | <span data-ttu-id="a6e35-286">對</span><span class="sxs-lookup"><span data-stu-id="a6e35-286">True</span></span>                            |
| <span data-ttu-id="a6e35-287">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6e35-287">Is Indexed</span></span>             | <span data-ttu-id="a6e35-288">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-288">False</span></span>                           |
| <span data-ttu-id="a6e35-289">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6e35-289">In Global Catalog</span></span>      | <span data-ttu-id="a6e35-290">否</span><span class="sxs-lookup"><span data-stu-id="a6e35-290">False</span></span>                           |
| <span data-ttu-id="a6e35-291">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6e35-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6e35-292">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6e35-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a6e35-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6e35-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a6e35-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6e35-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a6e35-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-295">Search-Flags</span></span>           | <span data-ttu-id="a6e35-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a6e35-296">0x00000000</span></span>                      |
| <span data-ttu-id="a6e35-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6e35-297">System-Flags</span></span>           | <span data-ttu-id="a6e35-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6e35-298">0x00000010</span></span>                      |
| <span data-ttu-id="a6e35-299">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6e35-299">Classes used in</span></span>        | [<span data-ttu-id="a6e35-300">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a6e35-300">**Top**</span></span>](c-top.md)<br/> |



 

 





