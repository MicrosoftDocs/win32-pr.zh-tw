---
title: ms DS-使用配額的屬性
description: 目錄資料庫中安全性主體所耗用的目前配額。
ms.assetid: 3a31c0c7-9791-4e00-81e5-ee596f94e3c9
ms.tgt_platform: multiple
keywords:
- ms DS-使用配額的屬性 AD 架構
- QuotaUsed 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Quota-Used
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59cc425c83fd7f1a85f41cd9d23e234115e0b55
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "107001644"
---
# <a name="ms-ds-quota-used-attribute"></a><span data-ttu-id="7e8ea-105">ms DS-使用配額的屬性</span><span class="sxs-lookup"><span data-stu-id="7e8ea-105">ms-DS-Quota-Used attribute</span></span>

<span data-ttu-id="7e8ea-106">目錄資料庫中安全性主體所耗用的目前配額。</span><span class="sxs-lookup"><span data-stu-id="7e8ea-106">The current quota consumed by a security principal in the directory database.</span></span>



| <span data-ttu-id="7e8ea-107">進入</span><span class="sxs-lookup"><span data-stu-id="7e8ea-107">Entry</span></span> | <span data-ttu-id="7e8ea-108">值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7e8ea-109">CN</span><span class="sxs-lookup"><span data-stu-id="7e8ea-109">CN</span></span>                | <span data-ttu-id="7e8ea-110">ms DS-使用配額</span><span class="sxs-lookup"><span data-stu-id="7e8ea-110">ms-DS-Quota-Used</span></span>                     |
| <span data-ttu-id="7e8ea-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7e8ea-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7e8ea-112">QuotaUsed</span><span class="sxs-lookup"><span data-stu-id="7e8ea-112">msDS-QuotaUsed</span></span>                       |
| <span data-ttu-id="7e8ea-113">大小</span><span class="sxs-lookup"><span data-stu-id="7e8ea-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="7e8ea-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7e8ea-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7e8ea-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7e8ea-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7e8ea-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7e8ea-116">Attribute-Id</span></span>      | <span data-ttu-id="7e8ea-117">1.2.840.113556.1.4.1849</span><span class="sxs-lookup"><span data-stu-id="7e8ea-117">1.2.840.113556.1.4.1849</span></span>              |
| <span data-ttu-id="7e8ea-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7e8ea-118">System-Id-Guid</span></span>    | <span data-ttu-id="7e8ea-119">b5a84308-615d-4bb7-b05f-2f1746aa439f</span><span class="sxs-lookup"><span data-stu-id="7e8ea-119">b5a84308-615d-4bb7-b05f-2f1746aa439f</span></span> |
| <span data-ttu-id="7e8ea-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e8ea-120">Syntax</span></span>            | [<span data-ttu-id="7e8ea-121">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="7e8ea-122">實作</span><span class="sxs-lookup"><span data-stu-id="7e8ea-122">Implementations</span></span>

-   [<span data-ttu-id="7e8ea-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7e8ea-124">**亞當**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7e8ea-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7e8ea-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7e8ea-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7e8ea-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7e8ea-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e8ea-129">Windows Server 2003</span></span>



| <span data-ttu-id="7e8ea-130">進入</span><span class="sxs-lookup"><span data-stu-id="7e8ea-130">Entry</span></span> | <span data-ttu-id="7e8ea-131">值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="7e8ea-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e8ea-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7e8ea-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e8ea-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7e8ea-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e8ea-134">System-Only</span></span>            | <span data-ttu-id="7e8ea-135">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-135">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-136">Is-Single-Valued</span></span>       | <span data-ttu-id="7e8ea-137">對</span><span class="sxs-lookup"><span data-stu-id="7e8ea-137">True</span></span>                                                              |
| <span data-ttu-id="7e8ea-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e8ea-138">Is Indexed</span></span>             | <span data-ttu-id="7e8ea-139">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-139">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e8ea-140">In Global Catalog</span></span>      | <span data-ttu-id="7e8ea-141">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-141">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e8ea-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e8ea-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e8ea-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="7e8ea-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e8ea-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="7e8ea-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e8ea-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="7e8ea-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e8ea-146">Search-Flags</span></span>           | <span data-ttu-id="7e8ea-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e8ea-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="7e8ea-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e8ea-148">System-Flags</span></span>           | <span data-ttu-id="7e8ea-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7e8ea-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="7e8ea-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e8ea-150">Classes used in</span></span>        | [<span data-ttu-id="7e8ea-151">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7e8ea-152">亞當</span><span class="sxs-lookup"><span data-stu-id="7e8ea-152">ADAM</span></span>



| <span data-ttu-id="7e8ea-153">進入</span><span class="sxs-lookup"><span data-stu-id="7e8ea-153">Entry</span></span> | <span data-ttu-id="7e8ea-154">值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="7e8ea-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e8ea-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7e8ea-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e8ea-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7e8ea-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e8ea-157">System-Only</span></span>            | <span data-ttu-id="7e8ea-158">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-158">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-159">Is-Single-Valued</span></span>       | <span data-ttu-id="7e8ea-160">對</span><span class="sxs-lookup"><span data-stu-id="7e8ea-160">True</span></span>                                                              |
| <span data-ttu-id="7e8ea-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e8ea-161">Is Indexed</span></span>             | <span data-ttu-id="7e8ea-162">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-162">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e8ea-163">In Global Catalog</span></span>      | <span data-ttu-id="7e8ea-164">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-164">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e8ea-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e8ea-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e8ea-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="7e8ea-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e8ea-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="7e8ea-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e8ea-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="7e8ea-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e8ea-169">Search-Flags</span></span>           | <span data-ttu-id="7e8ea-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e8ea-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="7e8ea-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e8ea-171">System-Flags</span></span>           | <span data-ttu-id="7e8ea-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7e8ea-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="7e8ea-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e8ea-173">Classes used in</span></span>        | [<span data-ttu-id="7e8ea-174">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7e8ea-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7e8ea-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7e8ea-176">進入</span><span class="sxs-lookup"><span data-stu-id="7e8ea-176">Entry</span></span> | <span data-ttu-id="7e8ea-177">值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="7e8ea-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e8ea-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7e8ea-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e8ea-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7e8ea-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e8ea-180">System-Only</span></span>            | <span data-ttu-id="7e8ea-181">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-181">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-182">Is-Single-Valued</span></span>       | <span data-ttu-id="7e8ea-183">對</span><span class="sxs-lookup"><span data-stu-id="7e8ea-183">True</span></span>                                                              |
| <span data-ttu-id="7e8ea-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e8ea-184">Is Indexed</span></span>             | <span data-ttu-id="7e8ea-185">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-185">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e8ea-186">In Global Catalog</span></span>      | <span data-ttu-id="7e8ea-187">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-187">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e8ea-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e8ea-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e8ea-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="7e8ea-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e8ea-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="7e8ea-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e8ea-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="7e8ea-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e8ea-192">Search-Flags</span></span>           | <span data-ttu-id="7e8ea-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e8ea-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="7e8ea-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e8ea-194">System-Flags</span></span>           | <span data-ttu-id="7e8ea-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7e8ea-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="7e8ea-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e8ea-196">Classes used in</span></span>        | [<span data-ttu-id="7e8ea-197">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7e8ea-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e8ea-198">Windows Server 2008</span></span>



| <span data-ttu-id="7e8ea-199">進入</span><span class="sxs-lookup"><span data-stu-id="7e8ea-199">Entry</span></span> | <span data-ttu-id="7e8ea-200">值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="7e8ea-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e8ea-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7e8ea-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e8ea-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7e8ea-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e8ea-203">System-Only</span></span>            | <span data-ttu-id="7e8ea-204">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-204">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-205">Is-Single-Valued</span></span>       | <span data-ttu-id="7e8ea-206">對</span><span class="sxs-lookup"><span data-stu-id="7e8ea-206">True</span></span>                                                              |
| <span data-ttu-id="7e8ea-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e8ea-207">Is Indexed</span></span>             | <span data-ttu-id="7e8ea-208">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-208">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e8ea-209">In Global Catalog</span></span>      | <span data-ttu-id="7e8ea-210">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-210">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e8ea-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e8ea-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e8ea-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="7e8ea-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e8ea-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="7e8ea-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e8ea-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="7e8ea-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e8ea-215">Search-Flags</span></span>           | <span data-ttu-id="7e8ea-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e8ea-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="7e8ea-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e8ea-217">System-Flags</span></span>           | <span data-ttu-id="7e8ea-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7e8ea-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="7e8ea-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e8ea-219">Classes used in</span></span>        | [<span data-ttu-id="7e8ea-220">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7e8ea-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e8ea-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7e8ea-222">進入</span><span class="sxs-lookup"><span data-stu-id="7e8ea-222">Entry</span></span> | <span data-ttu-id="7e8ea-223">值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="7e8ea-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e8ea-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7e8ea-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e8ea-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7e8ea-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e8ea-226">System-Only</span></span>            | <span data-ttu-id="7e8ea-227">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-227">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-228">Is-Single-Valued</span></span>       | <span data-ttu-id="7e8ea-229">對</span><span class="sxs-lookup"><span data-stu-id="7e8ea-229">True</span></span>                                                              |
| <span data-ttu-id="7e8ea-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e8ea-230">Is Indexed</span></span>             | <span data-ttu-id="7e8ea-231">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-231">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e8ea-232">In Global Catalog</span></span>      | <span data-ttu-id="7e8ea-233">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-233">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e8ea-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e8ea-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e8ea-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="7e8ea-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e8ea-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="7e8ea-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e8ea-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="7e8ea-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e8ea-238">Search-Flags</span></span>           | <span data-ttu-id="7e8ea-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e8ea-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="7e8ea-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e8ea-240">System-Flags</span></span>           | <span data-ttu-id="7e8ea-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7e8ea-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="7e8ea-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e8ea-242">Classes used in</span></span>        | [<span data-ttu-id="7e8ea-243">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7e8ea-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e8ea-244">Windows Server 2012</span></span>



| <span data-ttu-id="7e8ea-245">進入</span><span class="sxs-lookup"><span data-stu-id="7e8ea-245">Entry</span></span> | <span data-ttu-id="7e8ea-246">值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="7e8ea-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7e8ea-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7e8ea-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e8ea-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="7e8ea-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e8ea-249">System-Only</span></span>            | <span data-ttu-id="7e8ea-250">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-250">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7e8ea-251">Is-Single-Valued</span></span>       | <span data-ttu-id="7e8ea-252">對</span><span class="sxs-lookup"><span data-stu-id="7e8ea-252">True</span></span>                                                              |
| <span data-ttu-id="7e8ea-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7e8ea-253">Is Indexed</span></span>             | <span data-ttu-id="7e8ea-254">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-254">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7e8ea-255">In Global Catalog</span></span>      | <span data-ttu-id="7e8ea-256">否</span><span class="sxs-lookup"><span data-stu-id="7e8ea-256">False</span></span>                                                             |
| <span data-ttu-id="7e8ea-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7e8ea-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e8ea-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7e8ea-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="7e8ea-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e8ea-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="7e8ea-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e8ea-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="7e8ea-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e8ea-261">Search-Flags</span></span>           | <span data-ttu-id="7e8ea-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e8ea-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="7e8ea-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e8ea-263">System-Flags</span></span>           | <span data-ttu-id="7e8ea-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="7e8ea-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="7e8ea-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7e8ea-265">Classes used in</span></span>        | [<span data-ttu-id="7e8ea-266">**ms DS-配額-容器**</span><span class="sxs-lookup"><span data-stu-id="7e8ea-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





