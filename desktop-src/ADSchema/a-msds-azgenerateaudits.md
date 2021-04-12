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
# <a name="ms-ds-az-generate-audits-attribute"></a><span data-ttu-id="c4c48-105">ms DS-Az-產生-審核屬性</span><span class="sxs-lookup"><span data-stu-id="c4c48-105">ms-DS-Az-Generate-Audits attribute</span></span>

<span data-ttu-id="c4c48-106">此為布林值欄位，指出是否需要開啟執行時間審核 (包括存取檢查的檢查等) 。</span><span class="sxs-lookup"><span data-stu-id="c4c48-106">A Boolean field that indicates whether runtime audits need to be turned on (include audits for access checks, and so on).</span></span>



| <span data-ttu-id="c4c48-107">進入</span><span class="sxs-lookup"><span data-stu-id="c4c48-107">Entry</span></span> | <span data-ttu-id="c4c48-108">值</span><span class="sxs-lookup"><span data-stu-id="c4c48-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c4c48-109">CN</span><span class="sxs-lookup"><span data-stu-id="c4c48-109">CN</span></span>                | <span data-ttu-id="c4c48-110">ms DS-Az-產生-審核</span><span class="sxs-lookup"><span data-stu-id="c4c48-110">ms-DS-Az-Generate-Audits</span></span>                |
| <span data-ttu-id="c4c48-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c4c48-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c4c48-112">AzGenerateAudits</span><span class="sxs-lookup"><span data-stu-id="c4c48-112">msDS-AzGenerateAudits</span></span>                   |
| <span data-ttu-id="c4c48-113">大小</span><span class="sxs-lookup"><span data-stu-id="c4c48-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c4c48-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c4c48-114">Update Privilege</span></span>  | <span data-ttu-id="c4c48-115">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="c4c48-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="c4c48-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c4c48-116">Update Frequency</span></span>  | <span data-ttu-id="c4c48-117">在初始化或原則變更期間。</span><span class="sxs-lookup"><span data-stu-id="c4c48-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="c4c48-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c4c48-118">Attribute-Id</span></span>      | <span data-ttu-id="c4c48-119">1.2.840.113556.1.4.1805</span><span class="sxs-lookup"><span data-stu-id="c4c48-119">1.2.840.113556.1.4.1805</span></span>                 |
| <span data-ttu-id="c4c48-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c4c48-120">System-Id-Guid</span></span>    | <span data-ttu-id="c4c48-121">f90abab0-186c-4418-bb85-88447c87222a</span><span class="sxs-lookup"><span data-stu-id="c4c48-121">f90abab0-186c-4418-bb85-88447c87222a</span></span>    |
| <span data-ttu-id="c4c48-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4c48-122">Syntax</span></span>            | [<span data-ttu-id="c4c48-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c4c48-123">**Boolean**</span></span>](s-boolean.md)            |



## <a name="implementations"></a><span data-ttu-id="c4c48-124">實作</span><span class="sxs-lookup"><span data-stu-id="c4c48-124">Implementations</span></span>

-   [<span data-ttu-id="c4c48-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c4c48-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c4c48-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c4c48-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c4c48-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c4c48-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c4c48-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c4c48-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c4c48-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c4c48-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c4c48-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c4c48-130">Windows Server 2003</span></span>



| <span data-ttu-id="c4c48-131">進入</span><span class="sxs-lookup"><span data-stu-id="c4c48-131">Entry</span></span> | <span data-ttu-id="c4c48-132">值</span><span class="sxs-lookup"><span data-stu-id="c4c48-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c48-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c4c48-133">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4c48-134">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4c48-135">System-Only</span></span>            | <span data-ttu-id="c4c48-136">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-136">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c4c48-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c4c48-138">對</span><span class="sxs-lookup"><span data-stu-id="c4c48-138">True</span></span>                                                                                                                               |
| <span data-ttu-id="c4c48-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c4c48-139">Is Indexed</span></span>             | <span data-ttu-id="c4c48-140">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-140">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c4c48-141">In Global Catalog</span></span>      | <span data-ttu-id="c4c48-142">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-142">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c4c48-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4c48-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c4c48-144">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="c4c48-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4c48-145">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4c48-146">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c48-147">Search-Flags</span></span>           | <span data-ttu-id="c4c48-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4c48-148">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="c4c48-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c48-149">System-Flags</span></span>           | <span data-ttu-id="c4c48-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4c48-150">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="c4c48-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c4c48-151">Classes used in</span></span>        | [<span data-ttu-id="c4c48-152">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="c4c48-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="c4c48-153">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="c4c48-153">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c4c48-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c4c48-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c4c48-155">進入</span><span class="sxs-lookup"><span data-stu-id="c4c48-155">Entry</span></span> | <span data-ttu-id="c4c48-156">值</span><span class="sxs-lookup"><span data-stu-id="c4c48-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c48-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c4c48-157">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4c48-158">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4c48-159">System-Only</span></span>            | <span data-ttu-id="c4c48-160">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-160">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c4c48-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c4c48-162">對</span><span class="sxs-lookup"><span data-stu-id="c4c48-162">True</span></span>                                                                                                                               |
| <span data-ttu-id="c4c48-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c4c48-163">Is Indexed</span></span>             | <span data-ttu-id="c4c48-164">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-164">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c4c48-165">In Global Catalog</span></span>      | <span data-ttu-id="c4c48-166">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-166">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c4c48-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4c48-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c4c48-168">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="c4c48-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4c48-169">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4c48-170">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c48-171">Search-Flags</span></span>           | <span data-ttu-id="c4c48-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4c48-172">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="c4c48-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c48-173">System-Flags</span></span>           | <span data-ttu-id="c4c48-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4c48-174">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="c4c48-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c4c48-175">Classes used in</span></span>        | [<span data-ttu-id="c4c48-176">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="c4c48-176">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="c4c48-177">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="c4c48-177">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c4c48-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4c48-178">Windows Server 2008</span></span>



| <span data-ttu-id="c4c48-179">進入</span><span class="sxs-lookup"><span data-stu-id="c4c48-179">Entry</span></span> | <span data-ttu-id="c4c48-180">值</span><span class="sxs-lookup"><span data-stu-id="c4c48-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c48-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c4c48-181">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4c48-182">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4c48-183">System-Only</span></span>            | <span data-ttu-id="c4c48-184">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-184">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c4c48-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c4c48-186">對</span><span class="sxs-lookup"><span data-stu-id="c4c48-186">True</span></span>                                                                                                                               |
| <span data-ttu-id="c4c48-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c4c48-187">Is Indexed</span></span>             | <span data-ttu-id="c4c48-188">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-188">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c4c48-189">In Global Catalog</span></span>      | <span data-ttu-id="c4c48-190">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-190">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c4c48-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4c48-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c4c48-192">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="c4c48-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4c48-193">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4c48-194">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c48-195">Search-Flags</span></span>           | <span data-ttu-id="c4c48-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4c48-196">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="c4c48-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c48-197">System-Flags</span></span>           | <span data-ttu-id="c4c48-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4c48-198">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="c4c48-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c4c48-199">Classes used in</span></span>        | [<span data-ttu-id="c4c48-200">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="c4c48-200">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="c4c48-201">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="c4c48-201">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c4c48-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c4c48-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c4c48-203">進入</span><span class="sxs-lookup"><span data-stu-id="c4c48-203">Entry</span></span> | <span data-ttu-id="c4c48-204">值</span><span class="sxs-lookup"><span data-stu-id="c4c48-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c48-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c4c48-205">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4c48-206">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4c48-207">System-Only</span></span>            | <span data-ttu-id="c4c48-208">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-208">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c4c48-209">Is-Single-Valued</span></span>       | <span data-ttu-id="c4c48-210">對</span><span class="sxs-lookup"><span data-stu-id="c4c48-210">True</span></span>                                                                                                                               |
| <span data-ttu-id="c4c48-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c4c48-211">Is Indexed</span></span>             | <span data-ttu-id="c4c48-212">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-212">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c4c48-213">In Global Catalog</span></span>      | <span data-ttu-id="c4c48-214">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-214">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c4c48-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4c48-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c4c48-216">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="c4c48-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4c48-217">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4c48-218">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c48-219">Search-Flags</span></span>           | <span data-ttu-id="c4c48-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4c48-220">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="c4c48-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c48-221">System-Flags</span></span>           | <span data-ttu-id="c4c48-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4c48-222">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="c4c48-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c4c48-223">Classes used in</span></span>        | [<span data-ttu-id="c4c48-224">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="c4c48-224">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="c4c48-225">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="c4c48-225">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c4c48-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4c48-226">Windows Server 2012</span></span>



| <span data-ttu-id="c4c48-227">進入</span><span class="sxs-lookup"><span data-stu-id="c4c48-227">Entry</span></span> | <span data-ttu-id="c4c48-228">值</span><span class="sxs-lookup"><span data-stu-id="c4c48-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c48-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c4c48-229">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4c48-230">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4c48-231">System-Only</span></span>            | <span data-ttu-id="c4c48-232">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-232">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c4c48-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c4c48-234">對</span><span class="sxs-lookup"><span data-stu-id="c4c48-234">True</span></span>                                                                                                                               |
| <span data-ttu-id="c4c48-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c4c48-235">Is Indexed</span></span>             | <span data-ttu-id="c4c48-236">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-236">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c4c48-237">In Global Catalog</span></span>      | <span data-ttu-id="c4c48-238">否</span><span class="sxs-lookup"><span data-stu-id="c4c48-238">False</span></span>                                                                                                                              |
| <span data-ttu-id="c4c48-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c4c48-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4c48-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c4c48-240">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="c4c48-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4c48-241">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4c48-242">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="c4c48-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c48-243">Search-Flags</span></span>           | <span data-ttu-id="c4c48-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4c48-244">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="c4c48-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4c48-245">System-Flags</span></span>           | <span data-ttu-id="c4c48-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4c48-246">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="c4c48-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c4c48-247">Classes used in</span></span>        | [<span data-ttu-id="c4c48-248">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="c4c48-248">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="c4c48-249">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="c4c48-249">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



 

 





