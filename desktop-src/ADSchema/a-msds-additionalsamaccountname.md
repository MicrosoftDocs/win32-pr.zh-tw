---
title: ms-DS-其他 Sam-帳戶名稱屬性
description: 這個屬性是用來儲存 SAM 帳戶名稱，這些名稱會對應至以 ms DS 為依據的 DNS 主機名稱。
ms.assetid: eb69e1d4-42b7-42e1-aeae-77188db307ef
ms.tgt_platform: multiple
keywords:
- ms DS-其他-Sam-帳戶名稱屬性 AD 架構
- AdditionalSamAccountName 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Additional-Sam-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a437c30e6ddb0e551498480f7589791bce59feaf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970669"
---
# <a name="ms-ds-additional-sam-account-name-attribute"></a><span data-ttu-id="90911-105">ms-DS-其他 Sam-帳戶名稱屬性</span><span class="sxs-lookup"><span data-stu-id="90911-105">ms-DS-Additional-Sam-Account-Name attribute</span></span>

<span data-ttu-id="90911-106">這個屬性是用來儲存 SAM 帳戶名稱，這些名稱會對應至以 ms DS 為依據的 DNS 主機名稱。</span><span class="sxs-lookup"><span data-stu-id="90911-106">This attribute is used to store the SAM account names that correspond to the DNS host names in ms-DS-Additional-Dns-Host-Name.</span></span>



| <span data-ttu-id="90911-107">進入</span><span class="sxs-lookup"><span data-stu-id="90911-107">Entry</span></span> | <span data-ttu-id="90911-108">值</span><span class="sxs-lookup"><span data-stu-id="90911-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="90911-109">CN</span><span class="sxs-lookup"><span data-stu-id="90911-109">CN</span></span>                | <span data-ttu-id="90911-110">ms DS-其他-Sam-帳戶-名稱</span><span class="sxs-lookup"><span data-stu-id="90911-110">ms-DS-Additional-Sam-Account-Name</span></span>           |
| <span data-ttu-id="90911-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="90911-111">Ldap-Display-Name</span></span> | <span data-ttu-id="90911-112">AdditionalSamAccountName</span><span class="sxs-lookup"><span data-stu-id="90911-112">msDS-AdditionalSamAccountName</span></span>               |
| <span data-ttu-id="90911-113">大小</span><span class="sxs-lookup"><span data-stu-id="90911-113">Size</span></span>              | <span data-ttu-id="90911-114">小於20位元組。</span><span class="sxs-lookup"><span data-stu-id="90911-114">Less than 20 bytes.</span></span>                         |
| <span data-ttu-id="90911-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="90911-115">Update Privilege</span></span>  | <span data-ttu-id="90911-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="90911-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="90911-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="90911-117">Update Frequency</span></span>  | <span data-ttu-id="90911-118">當 DC 重新命名時。</span><span class="sxs-lookup"><span data-stu-id="90911-118">When the DC is renamed.</span></span>                     |
| <span data-ttu-id="90911-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="90911-119">Attribute-Id</span></span>      | <span data-ttu-id="90911-120">1.2.840.113556.1.4.1718</span><span class="sxs-lookup"><span data-stu-id="90911-120">1.2.840.113556.1.4.1718</span></span>                     |
| <span data-ttu-id="90911-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="90911-121">System-Id-Guid</span></span>    | <span data-ttu-id="90911-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span><span class="sxs-lookup"><span data-stu-id="90911-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span></span>        |
| <span data-ttu-id="90911-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="90911-123">Syntax</span></span>            | [<span data-ttu-id="90911-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="90911-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="90911-125">實作</span><span class="sxs-lookup"><span data-stu-id="90911-125">Implementations</span></span>

-   [<span data-ttu-id="90911-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="90911-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="90911-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="90911-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="90911-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="90911-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="90911-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="90911-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="90911-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="90911-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="90911-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90911-131">Windows Server 2003</span></span>



| <span data-ttu-id="90911-132">進入</span><span class="sxs-lookup"><span data-stu-id="90911-132">Entry</span></span> | <span data-ttu-id="90911-133">值</span><span class="sxs-lookup"><span data-stu-id="90911-133">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="90911-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="90911-134">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="90911-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90911-135">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="90911-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="90911-136">System-Only</span></span>            | <span data-ttu-id="90911-137">對</span><span class="sxs-lookup"><span data-stu-id="90911-137">True</span></span>                                      |
| <span data-ttu-id="90911-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="90911-138">Is-Single-Valued</span></span>       | <span data-ttu-id="90911-139">否</span><span class="sxs-lookup"><span data-stu-id="90911-139">False</span></span>                                     |
| <span data-ttu-id="90911-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="90911-140">Is Indexed</span></span>             | <span data-ttu-id="90911-141">對</span><span class="sxs-lookup"><span data-stu-id="90911-141">True</span></span>                                      |
| <span data-ttu-id="90911-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="90911-142">In Global Catalog</span></span>      | <span data-ttu-id="90911-143">否</span><span class="sxs-lookup"><span data-stu-id="90911-143">False</span></span>                                     |
| <span data-ttu-id="90911-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="90911-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="90911-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="90911-145">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="90911-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90911-146">Range-Lower</span></span>            | <span data-ttu-id="90911-147">0</span><span class="sxs-lookup"><span data-stu-id="90911-147">0</span></span>                                         |
| <span data-ttu-id="90911-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90911-148">Range-Upper</span></span>            | <span data-ttu-id="90911-149">256</span><span class="sxs-lookup"><span data-stu-id="90911-149">256</span></span>                                       |
| <span data-ttu-id="90911-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90911-150">Search-Flags</span></span>           | <span data-ttu-id="90911-151">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="90911-151">0x0000000D</span></span>                                |
| <span data-ttu-id="90911-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90911-152">System-Flags</span></span>           | <span data-ttu-id="90911-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90911-153">0x00000010</span></span>                                |
| <span data-ttu-id="90911-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="90911-154">Classes used in</span></span>        | [<span data-ttu-id="90911-155">**電腦**</span><span class="sxs-lookup"><span data-stu-id="90911-155">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="90911-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="90911-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="90911-157">進入</span><span class="sxs-lookup"><span data-stu-id="90911-157">Entry</span></span> | <span data-ttu-id="90911-158">值</span><span class="sxs-lookup"><span data-stu-id="90911-158">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="90911-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="90911-159">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="90911-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90911-160">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="90911-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="90911-161">System-Only</span></span>            | <span data-ttu-id="90911-162">對</span><span class="sxs-lookup"><span data-stu-id="90911-162">True</span></span>                                      |
| <span data-ttu-id="90911-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="90911-163">Is-Single-Valued</span></span>       | <span data-ttu-id="90911-164">否</span><span class="sxs-lookup"><span data-stu-id="90911-164">False</span></span>                                     |
| <span data-ttu-id="90911-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="90911-165">Is Indexed</span></span>             | <span data-ttu-id="90911-166">對</span><span class="sxs-lookup"><span data-stu-id="90911-166">True</span></span>                                      |
| <span data-ttu-id="90911-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="90911-167">In Global Catalog</span></span>      | <span data-ttu-id="90911-168">否</span><span class="sxs-lookup"><span data-stu-id="90911-168">False</span></span>                                     |
| <span data-ttu-id="90911-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="90911-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="90911-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="90911-170">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="90911-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90911-171">Range-Lower</span></span>            | <span data-ttu-id="90911-172">0</span><span class="sxs-lookup"><span data-stu-id="90911-172">0</span></span>                                         |
| <span data-ttu-id="90911-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90911-173">Range-Upper</span></span>            | <span data-ttu-id="90911-174">256</span><span class="sxs-lookup"><span data-stu-id="90911-174">256</span></span>                                       |
| <span data-ttu-id="90911-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90911-175">Search-Flags</span></span>           | <span data-ttu-id="90911-176">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="90911-176">0x0000000D</span></span>                                |
| <span data-ttu-id="90911-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90911-177">System-Flags</span></span>           | <span data-ttu-id="90911-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90911-178">0x00000010</span></span>                                |
| <span data-ttu-id="90911-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="90911-179">Classes used in</span></span>        | [<span data-ttu-id="90911-180">**電腦**</span><span class="sxs-lookup"><span data-stu-id="90911-180">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="90911-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90911-181">Windows Server 2008</span></span>



| <span data-ttu-id="90911-182">進入</span><span class="sxs-lookup"><span data-stu-id="90911-182">Entry</span></span> | <span data-ttu-id="90911-183">值</span><span class="sxs-lookup"><span data-stu-id="90911-183">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="90911-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="90911-184">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="90911-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90911-185">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="90911-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="90911-186">System-Only</span></span>            | <span data-ttu-id="90911-187">對</span><span class="sxs-lookup"><span data-stu-id="90911-187">True</span></span>                                      |
| <span data-ttu-id="90911-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="90911-188">Is-Single-Valued</span></span>       | <span data-ttu-id="90911-189">否</span><span class="sxs-lookup"><span data-stu-id="90911-189">False</span></span>                                     |
| <span data-ttu-id="90911-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="90911-190">Is Indexed</span></span>             | <span data-ttu-id="90911-191">對</span><span class="sxs-lookup"><span data-stu-id="90911-191">True</span></span>                                      |
| <span data-ttu-id="90911-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="90911-192">In Global Catalog</span></span>      | <span data-ttu-id="90911-193">否</span><span class="sxs-lookup"><span data-stu-id="90911-193">False</span></span>                                     |
| <span data-ttu-id="90911-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="90911-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="90911-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="90911-195">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="90911-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90911-196">Range-Lower</span></span>            | <span data-ttu-id="90911-197">0</span><span class="sxs-lookup"><span data-stu-id="90911-197">0</span></span>                                         |
| <span data-ttu-id="90911-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90911-198">Range-Upper</span></span>            | <span data-ttu-id="90911-199">256</span><span class="sxs-lookup"><span data-stu-id="90911-199">256</span></span>                                       |
| <span data-ttu-id="90911-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90911-200">Search-Flags</span></span>           | <span data-ttu-id="90911-201">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="90911-201">0x0000000D</span></span>                                |
| <span data-ttu-id="90911-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90911-202">System-Flags</span></span>           | <span data-ttu-id="90911-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90911-203">0x00000010</span></span>                                |
| <span data-ttu-id="90911-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="90911-204">Classes used in</span></span>        | [<span data-ttu-id="90911-205">**電腦**</span><span class="sxs-lookup"><span data-stu-id="90911-205">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="90911-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="90911-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="90911-207">進入</span><span class="sxs-lookup"><span data-stu-id="90911-207">Entry</span></span> | <span data-ttu-id="90911-208">值</span><span class="sxs-lookup"><span data-stu-id="90911-208">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="90911-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="90911-209">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="90911-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90911-210">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="90911-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="90911-211">System-Only</span></span>            | <span data-ttu-id="90911-212">對</span><span class="sxs-lookup"><span data-stu-id="90911-212">True</span></span>                                      |
| <span data-ttu-id="90911-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="90911-213">Is-Single-Valued</span></span>       | <span data-ttu-id="90911-214">否</span><span class="sxs-lookup"><span data-stu-id="90911-214">False</span></span>                                     |
| <span data-ttu-id="90911-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="90911-215">Is Indexed</span></span>             | <span data-ttu-id="90911-216">對</span><span class="sxs-lookup"><span data-stu-id="90911-216">True</span></span>                                      |
| <span data-ttu-id="90911-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="90911-217">In Global Catalog</span></span>      | <span data-ttu-id="90911-218">否</span><span class="sxs-lookup"><span data-stu-id="90911-218">False</span></span>                                     |
| <span data-ttu-id="90911-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="90911-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="90911-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="90911-220">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="90911-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90911-221">Range-Lower</span></span>            | <span data-ttu-id="90911-222">0</span><span class="sxs-lookup"><span data-stu-id="90911-222">0</span></span>                                         |
| <span data-ttu-id="90911-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90911-223">Range-Upper</span></span>            | <span data-ttu-id="90911-224">256</span><span class="sxs-lookup"><span data-stu-id="90911-224">256</span></span>                                       |
| <span data-ttu-id="90911-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90911-225">Search-Flags</span></span>           | <span data-ttu-id="90911-226">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="90911-226">0x0000000D</span></span>                                |
| <span data-ttu-id="90911-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90911-227">System-Flags</span></span>           | <span data-ttu-id="90911-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90911-228">0x00000010</span></span>                                |
| <span data-ttu-id="90911-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="90911-229">Classes used in</span></span>        | [<span data-ttu-id="90911-230">**電腦**</span><span class="sxs-lookup"><span data-stu-id="90911-230">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="90911-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90911-231">Windows Server 2012</span></span>



| <span data-ttu-id="90911-232">進入</span><span class="sxs-lookup"><span data-stu-id="90911-232">Entry</span></span> | <span data-ttu-id="90911-233">值</span><span class="sxs-lookup"><span data-stu-id="90911-233">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="90911-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="90911-234">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="90911-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90911-235">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="90911-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="90911-236">System-Only</span></span>            | <span data-ttu-id="90911-237">對</span><span class="sxs-lookup"><span data-stu-id="90911-237">True</span></span>                                      |
| <span data-ttu-id="90911-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="90911-238">Is-Single-Valued</span></span>       | <span data-ttu-id="90911-239">否</span><span class="sxs-lookup"><span data-stu-id="90911-239">False</span></span>                                     |
| <span data-ttu-id="90911-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="90911-240">Is Indexed</span></span>             | <span data-ttu-id="90911-241">對</span><span class="sxs-lookup"><span data-stu-id="90911-241">True</span></span>                                      |
| <span data-ttu-id="90911-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="90911-242">In Global Catalog</span></span>      | <span data-ttu-id="90911-243">否</span><span class="sxs-lookup"><span data-stu-id="90911-243">False</span></span>                                     |
| <span data-ttu-id="90911-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="90911-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="90911-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="90911-245">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="90911-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90911-246">Range-Lower</span></span>            | <span data-ttu-id="90911-247">0</span><span class="sxs-lookup"><span data-stu-id="90911-247">0</span></span>                                         |
| <span data-ttu-id="90911-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90911-248">Range-Upper</span></span>            | <span data-ttu-id="90911-249">256</span><span class="sxs-lookup"><span data-stu-id="90911-249">256</span></span>                                       |
| <span data-ttu-id="90911-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90911-250">Search-Flags</span></span>           | <span data-ttu-id="90911-251">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="90911-251">0x0000000D</span></span>                                |
| <span data-ttu-id="90911-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90911-252">System-Flags</span></span>           | <span data-ttu-id="90911-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90911-253">0x00000010</span></span>                                |
| <span data-ttu-id="90911-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="90911-254">Classes used in</span></span>        | [<span data-ttu-id="90911-255">**電腦**</span><span class="sxs-lookup"><span data-stu-id="90911-255">**Computer**</span></span>](c-computer.md)<br/> |



 

 





