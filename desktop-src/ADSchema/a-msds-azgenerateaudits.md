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
# <a name="ms-ds-az-generate-audits-attribute"></a><span data-ttu-id="89b4f-105">ms DS-Az-產生-審核屬性</span><span class="sxs-lookup"><span data-stu-id="89b4f-105">ms-DS-Az-Generate-Audits attribute</span></span>

<span data-ttu-id="89b4f-106">此為布林值欄位，指出是否需要開啟執行時間審核 (包括存取檢查的檢查等) 。</span><span class="sxs-lookup"><span data-stu-id="89b4f-106">A Boolean field that indicates whether runtime audits need to be turned on (include audits for access checks, and so on).</span></span>



| <span data-ttu-id="89b4f-107">進入</span><span class="sxs-lookup"><span data-stu-id="89b4f-107">Entry</span></span> | <span data-ttu-id="89b4f-108">值</span><span class="sxs-lookup"><span data-stu-id="89b4f-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="89b4f-109">CN</span><span class="sxs-lookup"><span data-stu-id="89b4f-109">CN</span></span>                | <span data-ttu-id="89b4f-110">ms DS-Az-產生-審核</span><span class="sxs-lookup"><span data-stu-id="89b4f-110">ms-DS-Az-Generate-Audits</span></span>                |
| <span data-ttu-id="89b4f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="89b4f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="89b4f-112">AzGenerateAudits</span><span class="sxs-lookup"><span data-stu-id="89b4f-112">msDS-AzGenerateAudits</span></span>                   |
| <span data-ttu-id="89b4f-113">大小</span><span class="sxs-lookup"><span data-stu-id="89b4f-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="89b4f-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="89b4f-114">Update Privilege</span></span>  | <span data-ttu-id="89b4f-115">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="89b4f-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="89b4f-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="89b4f-116">Update Frequency</span></span>  | <span data-ttu-id="89b4f-117">在初始化或原則變更期間。</span><span class="sxs-lookup"><span data-stu-id="89b4f-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="89b4f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="89b4f-118">Attribute-Id</span></span>      | <span data-ttu-id="89b4f-119">1.2.840.113556.1.4.1805</span><span class="sxs-lookup"><span data-stu-id="89b4f-119">1.2.840.113556.1.4.1805</span></span>                 |
| <span data-ttu-id="89b4f-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="89b4f-120">System-Id-Guid</span></span>    | <span data-ttu-id="89b4f-121">f90abab0-186c-4418-bb85-88447c87222a</span><span class="sxs-lookup"><span data-stu-id="89b4f-121">f90abab0-186c-4418-bb85-88447c87222a</span></span>    |
| <span data-ttu-id="89b4f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="89b4f-122">Syntax</span></span>            | [<span data-ttu-id="89b4f-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="89b4f-123">**Boolean**</span></span>](s-boolean.md)            |



## <a name="implementations"></a><span data-ttu-id="89b4f-124">實作</span><span class="sxs-lookup"><span data-stu-id="89b4f-124">Implementations</span></span>

-   [<span data-ttu-id="89b4f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="89b4f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="89b4f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="89b4f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="89b4f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="89b4f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="89b4f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="89b4f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="89b4f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="89b4f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="89b4f-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="89b4f-130">Windows Server 2003</span></span>



| <span data-ttu-id="89b4f-131">進入</span><span class="sxs-lookup"><span data-stu-id="89b4f-131">Entry</span></span> | <span data-ttu-id="89b4f-132">值</span><span class="sxs-lookup"><span data-stu-id="89b4f-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89b4f-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="89b4f-133">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89b4f-134">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="89b4f-135">System-Only</span></span>            | <span data-ttu-id="89b4f-136">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-136">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="89b4f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="89b4f-138">對</span><span class="sxs-lookup"><span data-stu-id="89b4f-138">True</span></span>                                                                                                                               |
| <span data-ttu-id="89b4f-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="89b4f-139">Is Indexed</span></span>             | <span data-ttu-id="89b4f-140">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-140">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="89b4f-141">In Global Catalog</span></span>      | <span data-ttu-id="89b4f-142">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-142">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="89b4f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="89b4f-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="89b4f-144">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="89b4f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89b4f-145">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89b4f-146">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89b4f-147">Search-Flags</span></span>           | <span data-ttu-id="89b4f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89b4f-148">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="89b4f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89b4f-149">System-Flags</span></span>           | <span data-ttu-id="89b4f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89b4f-150">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="89b4f-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="89b4f-151">Classes used in</span></span>        | [<span data-ttu-id="89b4f-152">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="89b4f-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="89b4f-153">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="89b4f-153">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="89b4f-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="89b4f-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="89b4f-155">進入</span><span class="sxs-lookup"><span data-stu-id="89b4f-155">Entry</span></span> | <span data-ttu-id="89b4f-156">值</span><span class="sxs-lookup"><span data-stu-id="89b4f-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89b4f-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="89b4f-157">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89b4f-158">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="89b4f-159">System-Only</span></span>            | <span data-ttu-id="89b4f-160">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-160">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="89b4f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="89b4f-162">對</span><span class="sxs-lookup"><span data-stu-id="89b4f-162">True</span></span>                                                                                                                               |
| <span data-ttu-id="89b4f-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="89b4f-163">Is Indexed</span></span>             | <span data-ttu-id="89b4f-164">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-164">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="89b4f-165">In Global Catalog</span></span>      | <span data-ttu-id="89b4f-166">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-166">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="89b4f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="89b4f-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="89b4f-168">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="89b4f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89b4f-169">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89b4f-170">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89b4f-171">Search-Flags</span></span>           | <span data-ttu-id="89b4f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89b4f-172">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="89b4f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89b4f-173">System-Flags</span></span>           | <span data-ttu-id="89b4f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89b4f-174">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="89b4f-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="89b4f-175">Classes used in</span></span>        | [<span data-ttu-id="89b4f-176">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="89b4f-176">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="89b4f-177">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="89b4f-177">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="89b4f-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89b4f-178">Windows Server 2008</span></span>



| <span data-ttu-id="89b4f-179">進入</span><span class="sxs-lookup"><span data-stu-id="89b4f-179">Entry</span></span> | <span data-ttu-id="89b4f-180">值</span><span class="sxs-lookup"><span data-stu-id="89b4f-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89b4f-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="89b4f-181">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89b4f-182">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="89b4f-183">System-Only</span></span>            | <span data-ttu-id="89b4f-184">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-184">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="89b4f-185">Is-Single-Valued</span></span>       | <span data-ttu-id="89b4f-186">對</span><span class="sxs-lookup"><span data-stu-id="89b4f-186">True</span></span>                                                                                                                               |
| <span data-ttu-id="89b4f-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="89b4f-187">Is Indexed</span></span>             | <span data-ttu-id="89b4f-188">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-188">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="89b4f-189">In Global Catalog</span></span>      | <span data-ttu-id="89b4f-190">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-190">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="89b4f-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="89b4f-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="89b4f-192">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="89b4f-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89b4f-193">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89b4f-194">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89b4f-195">Search-Flags</span></span>           | <span data-ttu-id="89b4f-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89b4f-196">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="89b4f-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89b4f-197">System-Flags</span></span>           | <span data-ttu-id="89b4f-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89b4f-198">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="89b4f-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="89b4f-199">Classes used in</span></span>        | [<span data-ttu-id="89b4f-200">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="89b4f-200">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="89b4f-201">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="89b4f-201">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="89b4f-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="89b4f-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="89b4f-203">進入</span><span class="sxs-lookup"><span data-stu-id="89b4f-203">Entry</span></span> | <span data-ttu-id="89b4f-204">值</span><span class="sxs-lookup"><span data-stu-id="89b4f-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89b4f-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="89b4f-205">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89b4f-206">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="89b4f-207">System-Only</span></span>            | <span data-ttu-id="89b4f-208">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-208">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="89b4f-209">Is-Single-Valued</span></span>       | <span data-ttu-id="89b4f-210">對</span><span class="sxs-lookup"><span data-stu-id="89b4f-210">True</span></span>                                                                                                                               |
| <span data-ttu-id="89b4f-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="89b4f-211">Is Indexed</span></span>             | <span data-ttu-id="89b4f-212">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-212">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="89b4f-213">In Global Catalog</span></span>      | <span data-ttu-id="89b4f-214">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-214">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="89b4f-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="89b4f-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="89b4f-216">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="89b4f-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89b4f-217">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89b4f-218">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89b4f-219">Search-Flags</span></span>           | <span data-ttu-id="89b4f-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89b4f-220">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="89b4f-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89b4f-221">System-Flags</span></span>           | <span data-ttu-id="89b4f-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89b4f-222">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="89b4f-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="89b4f-223">Classes used in</span></span>        | [<span data-ttu-id="89b4f-224">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="89b4f-224">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="89b4f-225">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="89b4f-225">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="89b4f-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="89b4f-226">Windows Server 2012</span></span>



| <span data-ttu-id="89b4f-227">進入</span><span class="sxs-lookup"><span data-stu-id="89b4f-227">Entry</span></span> | <span data-ttu-id="89b4f-228">值</span><span class="sxs-lookup"><span data-stu-id="89b4f-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89b4f-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="89b4f-229">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89b4f-230">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="89b4f-231">System-Only</span></span>            | <span data-ttu-id="89b4f-232">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-232">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="89b4f-233">Is-Single-Valued</span></span>       | <span data-ttu-id="89b4f-234">對</span><span class="sxs-lookup"><span data-stu-id="89b4f-234">True</span></span>                                                                                                                               |
| <span data-ttu-id="89b4f-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="89b4f-235">Is Indexed</span></span>             | <span data-ttu-id="89b4f-236">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-236">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="89b4f-237">In Global Catalog</span></span>      | <span data-ttu-id="89b4f-238">否</span><span class="sxs-lookup"><span data-stu-id="89b4f-238">False</span></span>                                                                                                                              |
| <span data-ttu-id="89b4f-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="89b4f-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="89b4f-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="89b4f-240">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="89b4f-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89b4f-241">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89b4f-242">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="89b4f-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89b4f-243">Search-Flags</span></span>           | <span data-ttu-id="89b4f-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="89b4f-244">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="89b4f-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89b4f-245">System-Flags</span></span>           | <span data-ttu-id="89b4f-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89b4f-246">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="89b4f-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="89b4f-247">Classes used in</span></span>        | [<span data-ttu-id="89b4f-248">**ms-chap-Az-管理管理員**</span><span class="sxs-lookup"><span data-stu-id="89b4f-248">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="89b4f-249">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="89b4f-249">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



 

 





