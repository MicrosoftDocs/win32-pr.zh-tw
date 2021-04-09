---
title: ms DS-Az-產生-審核屬性
description: 此為布林值欄位，指出是否需要開啟執行時間審核 (包括存取檢查的檢查等) 。
ms.assetid: 23578f6a-7e7f-4871-9503-73f2ce598173
ms.tgt_platform: multiple
keywords:
- ms DS-Az-產生-審核屬性 AD 架構
- AzGenerateAudits 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Az-Generate-Audits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645bdfd2f822139072391d401ecedfedee8680b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845500"
---
# <a name="ms-ds-az-generate-audits-attribute"></a><span data-ttu-id="57305-105">ms DS-Az-產生-審核屬性</span><span class="sxs-lookup"><span data-stu-id="57305-105">ms-DS-Az-Generate-Audits attribute</span></span>

<span data-ttu-id="57305-106">此為布林值欄位，指出是否需要開啟執行時間審核 (包括存取檢查的檢查等) 。</span><span class="sxs-lookup"><span data-stu-id="57305-106">A Boolean field that indicates whether runtime audits need to be turned on (include audits for access checks, and so on).</span></span>



| <span data-ttu-id="57305-107">進入</span><span class="sxs-lookup"><span data-stu-id="57305-107">Entry</span></span> | <span data-ttu-id="57305-108">值</span><span class="sxs-lookup"><span data-stu-id="57305-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="57305-109">CN</span><span class="sxs-lookup"><span data-stu-id="57305-109">CN</span></span>                | <span data-ttu-id="57305-110">ms DS-Az-產生-審核</span><span class="sxs-lookup"><span data-stu-id="57305-110">ms-DS-Az-Generate-Audits</span></span>                |
| <span data-ttu-id="57305-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="57305-111">Ldap-Display-Name</span></span> | <span data-ttu-id="57305-112">AzGenerateAudits</span><span class="sxs-lookup"><span data-stu-id="57305-112">msDS-AzGenerateAudits</span></span>                   |
| <span data-ttu-id="57305-113">大小</span><span class="sxs-lookup"><span data-stu-id="57305-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="57305-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="57305-114">Update Privilege</span></span>  | <span data-ttu-id="57305-115">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="57305-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="57305-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="57305-116">Update Frequency</span></span>  | <span data-ttu-id="57305-117">在初始化或原則變更期間。</span><span class="sxs-lookup"><span data-stu-id="57305-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="57305-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="57305-118">Attribute-Id</span></span>      | <span data-ttu-id="57305-119">1.2.840.113556.1.4.1805</span><span class="sxs-lookup"><span data-stu-id="57305-119">1.2.840.113556.1.4.1805</span></span>                 |
| <span data-ttu-id="57305-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="57305-120">System-Id-Guid</span></span>    | <span data-ttu-id="57305-121">f90abab0-186c-4418-bb85-88447c87222a</span><span class="sxs-lookup"><span data-stu-id="57305-121">f90abab0-186c-4418-bb85-88447c87222a</span></span>    |
| <span data-ttu-id="57305-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="57305-122">Syntax</span></span>            | [<span data-ttu-id="57305-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="57305-123">**Boolean**</span></span>](s-boolean.md)            |



## <a name="implementations"></a><span data-ttu-id="57305-124">實作</span><span class="sxs-lookup"><span data-stu-id="57305-124">Implementations</span></span>

-   [<span data-ttu-id="57305-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="57305-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="57305-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="57305-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="57305-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="57305-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="57305-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="57305-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="57305-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="57305-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="57305-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="57305-130">Windows Server 2003</span></span>



| <span data-ttu-id="57305-131">進入</span><span class="sxs-lookup"><span data-stu-id="57305-131">Entry</span></span> | <span data-ttu-id="57305-132">值</span><span class="sxs-lookup"><span data-stu-id="57305-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57305-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="57305-133">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57305-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57305-134">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57305-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="57305-135">System-Only</span></span>            | <span data-ttu-id="57305-136">否</span><span class="sxs-lookup"><span data-stu-id="57305-136">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="57305-137">Is-Single-Valued</span></span>       | <span data-ttu-id="57305-138">對</span><span class="sxs-lookup"><span data-stu-id="57305-138">True</span></span>                                                                                                                               |
| <span data-ttu-id="57305-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="57305-139">Is Indexed</span></span>             | <span data-ttu-id="57305-140">否</span><span class="sxs-lookup"><span data-stu-id="57305-140">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="57305-141">In Global Catalog</span></span>      | <span data-ttu-id="57305-142">否</span><span class="sxs-lookup"><span data-stu-id="57305-142">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="57305-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="57305-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="57305-144">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="57305-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57305-145">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57305-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57305-146">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57305-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57305-147">Search-Flags</span></span>           | <span data-ttu-id="57305-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57305-148">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="57305-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57305-149">System-Flags</span></span>           | <span data-ttu-id="57305-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57305-150">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="57305-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="57305-151">Classes used in</span></span>        | [<span data-ttu-id="57305-152">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="57305-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="57305-153">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="57305-153">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="57305-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="57305-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="57305-155">進入</span><span class="sxs-lookup"><span data-stu-id="57305-155">Entry</span></span> | <span data-ttu-id="57305-156">值</span><span class="sxs-lookup"><span data-stu-id="57305-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57305-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="57305-157">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57305-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57305-158">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57305-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="57305-159">System-Only</span></span>            | <span data-ttu-id="57305-160">否</span><span class="sxs-lookup"><span data-stu-id="57305-160">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="57305-161">Is-Single-Valued</span></span>       | <span data-ttu-id="57305-162">對</span><span class="sxs-lookup"><span data-stu-id="57305-162">True</span></span>                                                                                                                               |
| <span data-ttu-id="57305-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="57305-163">Is Indexed</span></span>             | <span data-ttu-id="57305-164">否</span><span class="sxs-lookup"><span data-stu-id="57305-164">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="57305-165">In Global Catalog</span></span>      | <span data-ttu-id="57305-166">否</span><span class="sxs-lookup"><span data-stu-id="57305-166">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="57305-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="57305-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="57305-168">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="57305-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57305-169">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57305-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57305-170">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57305-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57305-171">Search-Flags</span></span>           | <span data-ttu-id="57305-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57305-172">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="57305-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57305-173">System-Flags</span></span>           | <span data-ttu-id="57305-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57305-174">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="57305-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="57305-175">Classes used in</span></span>        | [<span data-ttu-id="57305-176">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="57305-176">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="57305-177">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="57305-177">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="57305-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57305-178">Windows Server 2008</span></span>



| <span data-ttu-id="57305-179">進入</span><span class="sxs-lookup"><span data-stu-id="57305-179">Entry</span></span> | <span data-ttu-id="57305-180">值</span><span class="sxs-lookup"><span data-stu-id="57305-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57305-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="57305-181">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57305-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57305-182">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57305-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="57305-183">System-Only</span></span>            | <span data-ttu-id="57305-184">否</span><span class="sxs-lookup"><span data-stu-id="57305-184">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="57305-185">Is-Single-Valued</span></span>       | <span data-ttu-id="57305-186">對</span><span class="sxs-lookup"><span data-stu-id="57305-186">True</span></span>                                                                                                                               |
| <span data-ttu-id="57305-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="57305-187">Is Indexed</span></span>             | <span data-ttu-id="57305-188">否</span><span class="sxs-lookup"><span data-stu-id="57305-188">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="57305-189">In Global Catalog</span></span>      | <span data-ttu-id="57305-190">否</span><span class="sxs-lookup"><span data-stu-id="57305-190">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="57305-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="57305-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="57305-192">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="57305-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57305-193">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57305-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57305-194">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57305-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57305-195">Search-Flags</span></span>           | <span data-ttu-id="57305-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57305-196">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="57305-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57305-197">System-Flags</span></span>           | <span data-ttu-id="57305-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57305-198">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="57305-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="57305-199">Classes used in</span></span>        | [<span data-ttu-id="57305-200">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="57305-200">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="57305-201">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="57305-201">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="57305-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="57305-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="57305-203">進入</span><span class="sxs-lookup"><span data-stu-id="57305-203">Entry</span></span> | <span data-ttu-id="57305-204">值</span><span class="sxs-lookup"><span data-stu-id="57305-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57305-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="57305-205">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57305-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57305-206">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57305-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="57305-207">System-Only</span></span>            | <span data-ttu-id="57305-208">否</span><span class="sxs-lookup"><span data-stu-id="57305-208">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="57305-209">Is-Single-Valued</span></span>       | <span data-ttu-id="57305-210">對</span><span class="sxs-lookup"><span data-stu-id="57305-210">True</span></span>                                                                                                                               |
| <span data-ttu-id="57305-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="57305-211">Is Indexed</span></span>             | <span data-ttu-id="57305-212">否</span><span class="sxs-lookup"><span data-stu-id="57305-212">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="57305-213">In Global Catalog</span></span>      | <span data-ttu-id="57305-214">否</span><span class="sxs-lookup"><span data-stu-id="57305-214">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="57305-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="57305-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="57305-216">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="57305-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57305-217">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57305-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57305-218">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57305-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57305-219">Search-Flags</span></span>           | <span data-ttu-id="57305-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57305-220">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="57305-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57305-221">System-Flags</span></span>           | <span data-ttu-id="57305-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57305-222">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="57305-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="57305-223">Classes used in</span></span>        | [<span data-ttu-id="57305-224">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="57305-224">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="57305-225">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="57305-225">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="57305-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="57305-226">Windows Server 2012</span></span>



| <span data-ttu-id="57305-227">進入</span><span class="sxs-lookup"><span data-stu-id="57305-227">Entry</span></span> | <span data-ttu-id="57305-228">值</span><span class="sxs-lookup"><span data-stu-id="57305-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57305-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="57305-229">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57305-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57305-230">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57305-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="57305-231">System-Only</span></span>            | <span data-ttu-id="57305-232">否</span><span class="sxs-lookup"><span data-stu-id="57305-232">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="57305-233">Is-Single-Valued</span></span>       | <span data-ttu-id="57305-234">對</span><span class="sxs-lookup"><span data-stu-id="57305-234">True</span></span>                                                                                                                               |
| <span data-ttu-id="57305-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="57305-235">Is Indexed</span></span>             | <span data-ttu-id="57305-236">否</span><span class="sxs-lookup"><span data-stu-id="57305-236">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="57305-237">In Global Catalog</span></span>      | <span data-ttu-id="57305-238">否</span><span class="sxs-lookup"><span data-stu-id="57305-238">False</span></span>                                                                                                                              |
| <span data-ttu-id="57305-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="57305-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="57305-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="57305-240">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="57305-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57305-241">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57305-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57305-242">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57305-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57305-243">Search-Flags</span></span>           | <span data-ttu-id="57305-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57305-244">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="57305-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57305-245">System-Flags</span></span>           | <span data-ttu-id="57305-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57305-246">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="57305-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="57305-247">Classes used in</span></span>        | [<span data-ttu-id="57305-248">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="57305-248">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="57305-249">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="57305-249">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



 

 





