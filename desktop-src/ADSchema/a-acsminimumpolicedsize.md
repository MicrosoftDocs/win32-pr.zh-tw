---
title: ACS-最小-Policed-大小屬性
description: ACS-最小 Policed 大小屬性僅供內部使用。
ms.assetid: 27b4273a-a625-430b-baa0-a6037e2aac1e
ms.tgt_platform: multiple
keywords:
- ACS-最小-Policed-大小的屬性 AD 架構
- aCSMinimumPolicedSize 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-Minimum-Policed-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3de4bb2b33a45ab7d10bad72ba286d1695b980a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106972914"
---
# <a name="acs-minimum-policed-size-attribute"></a><span data-ttu-id="88c2d-105">ACS-最小-Policed-大小屬性</span><span class="sxs-lookup"><span data-stu-id="88c2d-105">ACS-Minimum-Policed-Size attribute</span></span>

<span data-ttu-id="88c2d-106">**ACS-最小 Policed 大小** 屬性僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="88c2d-106">The **ACS-Minimum-Policed-Size** attribute is for internal use only.</span></span> <span data-ttu-id="88c2d-107">以 RFC2210 為基礎。</span><span class="sxs-lookup"><span data-stu-id="88c2d-107">Based on RFC2210.</span></span>



| <span data-ttu-id="88c2d-108">進入</span><span class="sxs-lookup"><span data-stu-id="88c2d-108">Entry</span></span> | <span data-ttu-id="88c2d-109">值</span><span class="sxs-lookup"><span data-stu-id="88c2d-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="88c2d-110">CN</span><span class="sxs-lookup"><span data-stu-id="88c2d-110">CN</span></span>                | <span data-ttu-id="88c2d-111">ACS-最小-Policed-大小</span><span class="sxs-lookup"><span data-stu-id="88c2d-111">ACS-Minimum-Policed-Size</span></span>             |
| <span data-ttu-id="88c2d-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="88c2d-112">Ldap-Display-Name</span></span> | <span data-ttu-id="88c2d-113">aCSMinimumPolicedSize</span><span class="sxs-lookup"><span data-stu-id="88c2d-113">aCSMinimumPolicedSize</span></span>                |
| <span data-ttu-id="88c2d-114">大小</span><span class="sxs-lookup"><span data-stu-id="88c2d-114">Size</span></span>              | <span data-ttu-id="88c2d-115">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="88c2d-115">8 bytes</span></span>                              |
| <span data-ttu-id="88c2d-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="88c2d-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="88c2d-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="88c2d-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="88c2d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="88c2d-118">Attribute-Id</span></span>      | <span data-ttu-id="88c2d-119">1.2.840.113556.1.4.1315</span><span class="sxs-lookup"><span data-stu-id="88c2d-119">1.2.840.113556.1.4.1315</span></span>              |
| <span data-ttu-id="88c2d-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="88c2d-120">System-Id-Guid</span></span>    | <span data-ttu-id="88c2d-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="88c2d-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="88c2d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="88c2d-122">Syntax</span></span>            | [<span data-ttu-id="88c2d-123">**間隔**</span><span class="sxs-lookup"><span data-stu-id="88c2d-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="88c2d-124">實作</span><span class="sxs-lookup"><span data-stu-id="88c2d-124">Implementations</span></span>

-   [<span data-ttu-id="88c2d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="88c2d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="88c2d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="88c2d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="88c2d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="88c2d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="88c2d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="88c2d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="88c2d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="88c2d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="88c2d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="88c2d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="88c2d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="88c2d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="88c2d-132">進入</span><span class="sxs-lookup"><span data-stu-id="88c2d-132">Entry</span></span> | <span data-ttu-id="88c2d-133">值</span><span class="sxs-lookup"><span data-stu-id="88c2d-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="88c2d-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88c2d-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="88c2d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c2d-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="88c2d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c2d-136">System-Only</span></span>            | <span data-ttu-id="88c2d-137">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-137">False</span></span>                                        |
| <span data-ttu-id="88c2d-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88c2d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="88c2d-139">對</span><span class="sxs-lookup"><span data-stu-id="88c2d-139">True</span></span>                                         |
| <span data-ttu-id="88c2d-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88c2d-140">Is Indexed</span></span>             | <span data-ttu-id="88c2d-141">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-141">False</span></span>                                        |
| <span data-ttu-id="88c2d-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88c2d-142">In Global Catalog</span></span>      | <span data-ttu-id="88c2d-143">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-143">False</span></span>                                        |
| <span data-ttu-id="88c2d-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88c2d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c2d-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88c2d-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="88c2d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c2d-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="88c2d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c2d-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="88c2d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c2d-148">Search-Flags</span></span>           | <span data-ttu-id="88c2d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c2d-149">0x00000000</span></span>                                   |
| <span data-ttu-id="88c2d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c2d-150">System-Flags</span></span>           | <span data-ttu-id="88c2d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c2d-151">0x00000010</span></span>                                   |
| <span data-ttu-id="88c2d-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88c2d-152">Classes used in</span></span>        | [<span data-ttu-id="88c2d-153">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="88c2d-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="88c2d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="88c2d-154">Windows Server 2003</span></span>



| <span data-ttu-id="88c2d-155">進入</span><span class="sxs-lookup"><span data-stu-id="88c2d-155">Entry</span></span> | <span data-ttu-id="88c2d-156">值</span><span class="sxs-lookup"><span data-stu-id="88c2d-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="88c2d-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88c2d-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="88c2d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c2d-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="88c2d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c2d-159">System-Only</span></span>            | <span data-ttu-id="88c2d-160">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-160">False</span></span>                                        |
| <span data-ttu-id="88c2d-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88c2d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="88c2d-162">對</span><span class="sxs-lookup"><span data-stu-id="88c2d-162">True</span></span>                                         |
| <span data-ttu-id="88c2d-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88c2d-163">Is Indexed</span></span>             | <span data-ttu-id="88c2d-164">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-164">False</span></span>                                        |
| <span data-ttu-id="88c2d-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88c2d-165">In Global Catalog</span></span>      | <span data-ttu-id="88c2d-166">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-166">False</span></span>                                        |
| <span data-ttu-id="88c2d-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88c2d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c2d-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88c2d-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="88c2d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c2d-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="88c2d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c2d-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="88c2d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c2d-171">Search-Flags</span></span>           | <span data-ttu-id="88c2d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c2d-172">0x00000000</span></span>                                   |
| <span data-ttu-id="88c2d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c2d-173">System-Flags</span></span>           | <span data-ttu-id="88c2d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c2d-174">0x00000010</span></span>                                   |
| <span data-ttu-id="88c2d-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88c2d-175">Classes used in</span></span>        | [<span data-ttu-id="88c2d-176">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="88c2d-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="88c2d-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="88c2d-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="88c2d-178">進入</span><span class="sxs-lookup"><span data-stu-id="88c2d-178">Entry</span></span> | <span data-ttu-id="88c2d-179">值</span><span class="sxs-lookup"><span data-stu-id="88c2d-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="88c2d-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88c2d-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="88c2d-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c2d-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="88c2d-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c2d-182">System-Only</span></span>            | <span data-ttu-id="88c2d-183">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-183">False</span></span>                                        |
| <span data-ttu-id="88c2d-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88c2d-184">Is-Single-Valued</span></span>       | <span data-ttu-id="88c2d-185">對</span><span class="sxs-lookup"><span data-stu-id="88c2d-185">True</span></span>                                         |
| <span data-ttu-id="88c2d-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88c2d-186">Is Indexed</span></span>             | <span data-ttu-id="88c2d-187">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-187">False</span></span>                                        |
| <span data-ttu-id="88c2d-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88c2d-188">In Global Catalog</span></span>      | <span data-ttu-id="88c2d-189">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-189">False</span></span>                                        |
| <span data-ttu-id="88c2d-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88c2d-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c2d-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88c2d-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="88c2d-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c2d-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="88c2d-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c2d-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="88c2d-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c2d-194">Search-Flags</span></span>           | <span data-ttu-id="88c2d-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c2d-195">0x00000000</span></span>                                   |
| <span data-ttu-id="88c2d-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c2d-196">System-Flags</span></span>           | <span data-ttu-id="88c2d-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c2d-197">0x00000010</span></span>                                   |
| <span data-ttu-id="88c2d-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88c2d-198">Classes used in</span></span>        | [<span data-ttu-id="88c2d-199">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="88c2d-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="88c2d-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88c2d-200">Windows Server 2008</span></span>



| <span data-ttu-id="88c2d-201">進入</span><span class="sxs-lookup"><span data-stu-id="88c2d-201">Entry</span></span> | <span data-ttu-id="88c2d-202">值</span><span class="sxs-lookup"><span data-stu-id="88c2d-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="88c2d-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88c2d-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="88c2d-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c2d-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="88c2d-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c2d-205">System-Only</span></span>            | <span data-ttu-id="88c2d-206">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-206">False</span></span>                                        |
| <span data-ttu-id="88c2d-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88c2d-207">Is-Single-Valued</span></span>       | <span data-ttu-id="88c2d-208">對</span><span class="sxs-lookup"><span data-stu-id="88c2d-208">True</span></span>                                         |
| <span data-ttu-id="88c2d-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88c2d-209">Is Indexed</span></span>             | <span data-ttu-id="88c2d-210">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-210">False</span></span>                                        |
| <span data-ttu-id="88c2d-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88c2d-211">In Global Catalog</span></span>      | <span data-ttu-id="88c2d-212">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-212">False</span></span>                                        |
| <span data-ttu-id="88c2d-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88c2d-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c2d-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88c2d-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="88c2d-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c2d-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="88c2d-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c2d-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="88c2d-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c2d-217">Search-Flags</span></span>           | <span data-ttu-id="88c2d-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c2d-218">0x00000000</span></span>                                   |
| <span data-ttu-id="88c2d-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c2d-219">System-Flags</span></span>           | <span data-ttu-id="88c2d-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c2d-220">0x00000010</span></span>                                   |
| <span data-ttu-id="88c2d-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88c2d-221">Classes used in</span></span>        | [<span data-ttu-id="88c2d-222">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="88c2d-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="88c2d-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88c2d-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="88c2d-224">進入</span><span class="sxs-lookup"><span data-stu-id="88c2d-224">Entry</span></span> | <span data-ttu-id="88c2d-225">值</span><span class="sxs-lookup"><span data-stu-id="88c2d-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="88c2d-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88c2d-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="88c2d-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c2d-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="88c2d-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c2d-228">System-Only</span></span>            | <span data-ttu-id="88c2d-229">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-229">False</span></span>                                        |
| <span data-ttu-id="88c2d-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88c2d-230">Is-Single-Valued</span></span>       | <span data-ttu-id="88c2d-231">對</span><span class="sxs-lookup"><span data-stu-id="88c2d-231">True</span></span>                                         |
| <span data-ttu-id="88c2d-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88c2d-232">Is Indexed</span></span>             | <span data-ttu-id="88c2d-233">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-233">False</span></span>                                        |
| <span data-ttu-id="88c2d-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88c2d-234">In Global Catalog</span></span>      | <span data-ttu-id="88c2d-235">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-235">False</span></span>                                        |
| <span data-ttu-id="88c2d-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88c2d-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c2d-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88c2d-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="88c2d-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c2d-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="88c2d-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c2d-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="88c2d-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c2d-240">Search-Flags</span></span>           | <span data-ttu-id="88c2d-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c2d-241">0x00000000</span></span>                                   |
| <span data-ttu-id="88c2d-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c2d-242">System-Flags</span></span>           | <span data-ttu-id="88c2d-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c2d-243">0x00000010</span></span>                                   |
| <span data-ttu-id="88c2d-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88c2d-244">Classes used in</span></span>        | [<span data-ttu-id="88c2d-245">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="88c2d-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="88c2d-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88c2d-246">Windows Server 2012</span></span>



| <span data-ttu-id="88c2d-247">進入</span><span class="sxs-lookup"><span data-stu-id="88c2d-247">Entry</span></span> | <span data-ttu-id="88c2d-248">值</span><span class="sxs-lookup"><span data-stu-id="88c2d-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="88c2d-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="88c2d-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="88c2d-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="88c2d-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="88c2d-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="88c2d-251">System-Only</span></span>            | <span data-ttu-id="88c2d-252">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-252">False</span></span>                                        |
| <span data-ttu-id="88c2d-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="88c2d-253">Is-Single-Valued</span></span>       | <span data-ttu-id="88c2d-254">對</span><span class="sxs-lookup"><span data-stu-id="88c2d-254">True</span></span>                                         |
| <span data-ttu-id="88c2d-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="88c2d-255">Is Indexed</span></span>             | <span data-ttu-id="88c2d-256">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-256">False</span></span>                                        |
| <span data-ttu-id="88c2d-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="88c2d-257">In Global Catalog</span></span>      | <span data-ttu-id="88c2d-258">否</span><span class="sxs-lookup"><span data-stu-id="88c2d-258">False</span></span>                                        |
| <span data-ttu-id="88c2d-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="88c2d-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="88c2d-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="88c2d-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="88c2d-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="88c2d-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="88c2d-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="88c2d-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="88c2d-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="88c2d-263">Search-Flags</span></span>           | <span data-ttu-id="88c2d-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88c2d-264">0x00000000</span></span>                                   |
| <span data-ttu-id="88c2d-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="88c2d-265">System-Flags</span></span>           | <span data-ttu-id="88c2d-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="88c2d-266">0x00000010</span></span>                                   |
| <span data-ttu-id="88c2d-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="88c2d-267">Classes used in</span></span>        | [<span data-ttu-id="88c2d-268">**ACS-原則**</span><span class="sxs-lookup"><span data-stu-id="88c2d-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





