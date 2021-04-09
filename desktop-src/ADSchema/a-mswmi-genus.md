---
title: 拼出動植物屬性
description: 識別編碼的物件類型。
ms.assetid: 924363f5-dabf-46ce-a5de-bbecf401db61
ms.tgt_platform: multiple
keywords:
- 拼出動植物屬性 AD 架構
- msWMI-拼出動植物屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-WMI-Genus
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e901c0e9d64c02bee04e9a8e6b5cc50bbcb726a4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935512"
---
# <a name="ms-wmi-genus-attribute"></a><span data-ttu-id="589ed-105">拼出動植物屬性</span><span class="sxs-lookup"><span data-stu-id="589ed-105">ms-WMI-Genus attribute</span></span>

<span data-ttu-id="589ed-106">識別編碼的物件類型。</span><span class="sxs-lookup"><span data-stu-id="589ed-106">Identifies the object type of an encoding.</span></span>



| <span data-ttu-id="589ed-107">進入</span><span class="sxs-lookup"><span data-stu-id="589ed-107">Entry</span></span> | <span data-ttu-id="589ed-108">值</span><span class="sxs-lookup"><span data-stu-id="589ed-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="589ed-109">CN</span><span class="sxs-lookup"><span data-stu-id="589ed-109">CN</span></span>                | <span data-ttu-id="589ed-110">拼出動植物</span><span class="sxs-lookup"><span data-stu-id="589ed-110">ms-WMI-Genus</span></span>                                                    |
| <span data-ttu-id="589ed-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="589ed-111">Ldap-Display-Name</span></span> | <span data-ttu-id="589ed-112">msWMI-拼出動植物</span><span class="sxs-lookup"><span data-stu-id="589ed-112">msWMI-Genus</span></span>                                                     |
| <span data-ttu-id="589ed-113">大小</span><span class="sxs-lookup"><span data-stu-id="589ed-113">Size</span></span>              | <span data-ttu-id="589ed-114">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="589ed-114">4 bytes.</span></span> <span data-ttu-id="589ed-115">1表示類別。</span><span class="sxs-lookup"><span data-stu-id="589ed-115">1 indicates a class.</span></span> <span data-ttu-id="589ed-116">2表示實例。</span><span class="sxs-lookup"><span data-stu-id="589ed-116">2 indicates an instance.</span></span>          |
| <span data-ttu-id="589ed-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="589ed-117">Update Privilege</span></span>  | <span data-ttu-id="589ed-118">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="589ed-118">Domain administrator</span></span>                                            |
| <span data-ttu-id="589ed-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="589ed-119">Update Frequency</span></span>  | <span data-ttu-id="589ed-120">只要加入或修改包含屬性的類別。</span><span class="sxs-lookup"><span data-stu-id="589ed-120">Whenever a class containing the attribute is added or modified.</span></span> |
| <span data-ttu-id="589ed-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="589ed-121">Attribute-Id</span></span>      | <span data-ttu-id="589ed-122">1.2.840.113556.1.4.1677</span><span class="sxs-lookup"><span data-stu-id="589ed-122">1.2.840.113556.1.4.1677</span></span>                                         |
| <span data-ttu-id="589ed-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="589ed-123">System-Id-Guid</span></span>    | <span data-ttu-id="589ed-124">50c8673a-8f56-4614-9308-9e1340fb9af3</span><span class="sxs-lookup"><span data-stu-id="589ed-124">50c8673a-8f56-4614-9308-9e1340fb9af3</span></span>                            |
| <span data-ttu-id="589ed-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="589ed-125">Syntax</span></span>            | [<span data-ttu-id="589ed-126">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="589ed-126">**Enumeration**</span></span>](s-enumeration.md)                            |



## <a name="implementations"></a><span data-ttu-id="589ed-127">實作</span><span class="sxs-lookup"><span data-stu-id="589ed-127">Implementations</span></span>

-   [<span data-ttu-id="589ed-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="589ed-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="589ed-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="589ed-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="589ed-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="589ed-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="589ed-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="589ed-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="589ed-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="589ed-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="589ed-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="589ed-133">Windows Server 2003</span></span>



| <span data-ttu-id="589ed-134">進入</span><span class="sxs-lookup"><span data-stu-id="589ed-134">Entry</span></span> | <span data-ttu-id="589ed-135">值</span><span class="sxs-lookup"><span data-stu-id="589ed-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="589ed-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="589ed-136">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="589ed-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="589ed-137">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="589ed-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="589ed-138">System-Only</span></span>            | <span data-ttu-id="589ed-139">否</span><span class="sxs-lookup"><span data-stu-id="589ed-139">False</span></span>                                                              |
| <span data-ttu-id="589ed-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="589ed-140">Is-Single-Valued</span></span>       | <span data-ttu-id="589ed-141">對</span><span class="sxs-lookup"><span data-stu-id="589ed-141">True</span></span>                                                               |
| <span data-ttu-id="589ed-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="589ed-142">Is Indexed</span></span>             | <span data-ttu-id="589ed-143">否</span><span class="sxs-lookup"><span data-stu-id="589ed-143">False</span></span>                                                              |
| <span data-ttu-id="589ed-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="589ed-144">In Global Catalog</span></span>      | <span data-ttu-id="589ed-145">否</span><span class="sxs-lookup"><span data-stu-id="589ed-145">False</span></span>                                                              |
| <span data-ttu-id="589ed-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="589ed-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="589ed-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="589ed-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="589ed-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="589ed-148">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="589ed-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="589ed-149">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="589ed-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="589ed-150">Search-Flags</span></span>           | <span data-ttu-id="589ed-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="589ed-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="589ed-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="589ed-152">System-Flags</span></span>           | <span data-ttu-id="589ed-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="589ed-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="589ed-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="589ed-154">Classes used in</span></span>        | [<span data-ttu-id="589ed-155">**ObjectEncoding**</span><span class="sxs-lookup"><span data-stu-id="589ed-155">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="589ed-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="589ed-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="589ed-157">進入</span><span class="sxs-lookup"><span data-stu-id="589ed-157">Entry</span></span> | <span data-ttu-id="589ed-158">值</span><span class="sxs-lookup"><span data-stu-id="589ed-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="589ed-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="589ed-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="589ed-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="589ed-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="589ed-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="589ed-161">System-Only</span></span>            | <span data-ttu-id="589ed-162">否</span><span class="sxs-lookup"><span data-stu-id="589ed-162">False</span></span>                                                              |
| <span data-ttu-id="589ed-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="589ed-163">Is-Single-Valued</span></span>       | <span data-ttu-id="589ed-164">對</span><span class="sxs-lookup"><span data-stu-id="589ed-164">True</span></span>                                                               |
| <span data-ttu-id="589ed-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="589ed-165">Is Indexed</span></span>             | <span data-ttu-id="589ed-166">否</span><span class="sxs-lookup"><span data-stu-id="589ed-166">False</span></span>                                                              |
| <span data-ttu-id="589ed-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="589ed-167">In Global Catalog</span></span>      | <span data-ttu-id="589ed-168">否</span><span class="sxs-lookup"><span data-stu-id="589ed-168">False</span></span>                                                              |
| <span data-ttu-id="589ed-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="589ed-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="589ed-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="589ed-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="589ed-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="589ed-171">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="589ed-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="589ed-172">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="589ed-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="589ed-173">Search-Flags</span></span>           | <span data-ttu-id="589ed-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="589ed-174">0x00000000</span></span>                                                         |
| <span data-ttu-id="589ed-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="589ed-175">System-Flags</span></span>           | <span data-ttu-id="589ed-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="589ed-176">0x00000010</span></span>                                                         |
| <span data-ttu-id="589ed-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="589ed-177">Classes used in</span></span>        | [<span data-ttu-id="589ed-178">**ObjectEncoding**</span><span class="sxs-lookup"><span data-stu-id="589ed-178">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="589ed-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="589ed-179">Windows Server 2008</span></span>



| <span data-ttu-id="589ed-180">進入</span><span class="sxs-lookup"><span data-stu-id="589ed-180">Entry</span></span> | <span data-ttu-id="589ed-181">值</span><span class="sxs-lookup"><span data-stu-id="589ed-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="589ed-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="589ed-182">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="589ed-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="589ed-183">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="589ed-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="589ed-184">System-Only</span></span>            | <span data-ttu-id="589ed-185">否</span><span class="sxs-lookup"><span data-stu-id="589ed-185">False</span></span>                                                              |
| <span data-ttu-id="589ed-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="589ed-186">Is-Single-Valued</span></span>       | <span data-ttu-id="589ed-187">對</span><span class="sxs-lookup"><span data-stu-id="589ed-187">True</span></span>                                                               |
| <span data-ttu-id="589ed-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="589ed-188">Is Indexed</span></span>             | <span data-ttu-id="589ed-189">否</span><span class="sxs-lookup"><span data-stu-id="589ed-189">False</span></span>                                                              |
| <span data-ttu-id="589ed-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="589ed-190">In Global Catalog</span></span>      | <span data-ttu-id="589ed-191">否</span><span class="sxs-lookup"><span data-stu-id="589ed-191">False</span></span>                                                              |
| <span data-ttu-id="589ed-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="589ed-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="589ed-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="589ed-193">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="589ed-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="589ed-194">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="589ed-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="589ed-195">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="589ed-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="589ed-196">Search-Flags</span></span>           | <span data-ttu-id="589ed-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="589ed-197">0x00000000</span></span>                                                         |
| <span data-ttu-id="589ed-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="589ed-198">System-Flags</span></span>           | <span data-ttu-id="589ed-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="589ed-199">0x00000010</span></span>                                                         |
| <span data-ttu-id="589ed-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="589ed-200">Classes used in</span></span>        | [<span data-ttu-id="589ed-201">**ObjectEncoding**</span><span class="sxs-lookup"><span data-stu-id="589ed-201">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="589ed-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="589ed-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="589ed-203">進入</span><span class="sxs-lookup"><span data-stu-id="589ed-203">Entry</span></span> | <span data-ttu-id="589ed-204">值</span><span class="sxs-lookup"><span data-stu-id="589ed-204">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="589ed-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="589ed-205">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="589ed-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="589ed-206">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="589ed-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="589ed-207">System-Only</span></span>            | <span data-ttu-id="589ed-208">否</span><span class="sxs-lookup"><span data-stu-id="589ed-208">False</span></span>                                                              |
| <span data-ttu-id="589ed-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="589ed-209">Is-Single-Valued</span></span>       | <span data-ttu-id="589ed-210">對</span><span class="sxs-lookup"><span data-stu-id="589ed-210">True</span></span>                                                               |
| <span data-ttu-id="589ed-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="589ed-211">Is Indexed</span></span>             | <span data-ttu-id="589ed-212">否</span><span class="sxs-lookup"><span data-stu-id="589ed-212">False</span></span>                                                              |
| <span data-ttu-id="589ed-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="589ed-213">In Global Catalog</span></span>      | <span data-ttu-id="589ed-214">否</span><span class="sxs-lookup"><span data-stu-id="589ed-214">False</span></span>                                                              |
| <span data-ttu-id="589ed-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="589ed-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="589ed-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="589ed-216">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="589ed-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="589ed-217">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="589ed-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="589ed-218">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="589ed-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="589ed-219">Search-Flags</span></span>           | <span data-ttu-id="589ed-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="589ed-220">0x00000000</span></span>                                                         |
| <span data-ttu-id="589ed-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="589ed-221">System-Flags</span></span>           | <span data-ttu-id="589ed-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="589ed-222">0x00000010</span></span>                                                         |
| <span data-ttu-id="589ed-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="589ed-223">Classes used in</span></span>        | [<span data-ttu-id="589ed-224">**ObjectEncoding**</span><span class="sxs-lookup"><span data-stu-id="589ed-224">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="589ed-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="589ed-225">Windows Server 2012</span></span>



| <span data-ttu-id="589ed-226">進入</span><span class="sxs-lookup"><span data-stu-id="589ed-226">Entry</span></span> | <span data-ttu-id="589ed-227">值</span><span class="sxs-lookup"><span data-stu-id="589ed-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="589ed-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="589ed-228">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="589ed-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="589ed-229">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="589ed-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="589ed-230">System-Only</span></span>            | <span data-ttu-id="589ed-231">否</span><span class="sxs-lookup"><span data-stu-id="589ed-231">False</span></span>                                                              |
| <span data-ttu-id="589ed-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="589ed-232">Is-Single-Valued</span></span>       | <span data-ttu-id="589ed-233">對</span><span class="sxs-lookup"><span data-stu-id="589ed-233">True</span></span>                                                               |
| <span data-ttu-id="589ed-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="589ed-234">Is Indexed</span></span>             | <span data-ttu-id="589ed-235">否</span><span class="sxs-lookup"><span data-stu-id="589ed-235">False</span></span>                                                              |
| <span data-ttu-id="589ed-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="589ed-236">In Global Catalog</span></span>      | <span data-ttu-id="589ed-237">否</span><span class="sxs-lookup"><span data-stu-id="589ed-237">False</span></span>                                                              |
| <span data-ttu-id="589ed-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="589ed-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="589ed-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="589ed-239">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="589ed-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="589ed-240">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="589ed-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="589ed-241">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="589ed-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="589ed-242">Search-Flags</span></span>           | <span data-ttu-id="589ed-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="589ed-243">0x00000000</span></span>                                                         |
| <span data-ttu-id="589ed-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="589ed-244">System-Flags</span></span>           | <span data-ttu-id="589ed-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="589ed-245">0x00000010</span></span>                                                         |
| <span data-ttu-id="589ed-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="589ed-246">Classes used in</span></span>        | [<span data-ttu-id="589ed-247">**ObjectEncoding**</span><span class="sxs-lookup"><span data-stu-id="589ed-247">**ms-WMI-ObjectEncoding**</span></span>](c-mswmi-objectencoding.md)<br/> |



 

 





