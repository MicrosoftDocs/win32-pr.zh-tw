---
title: msSFU-30-Order-Number 屬性
description: 包含一個值，此值會由 NIS 用來檢查對應是否已變更。
ms.assetid: b2e83980-2de4-4001-b65a-8073c9258b27
ms.tgt_platform: multiple
keywords:
- msSFU-30-Order-Number 屬性 AD 架構
- msSFU30OrderNumber 屬性 AD 架構
topic_type:
- apiref
api_name:
- msSFU-30-Order-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af67f1b5d6fdff8ca4a7739276443d67fa35679f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107705"
---
# <a name="mssfu-30-order-number-attribute"></a><span data-ttu-id="4baff-105">msSFU-30-Order-Number 屬性</span><span class="sxs-lookup"><span data-stu-id="4baff-105">msSFU-30-Order-Number attribute</span></span>

<span data-ttu-id="4baff-106">包含一個值，此值會由 NIS 用來檢查對應是否已變更。</span><span class="sxs-lookup"><span data-stu-id="4baff-106">Contains a value that is used by NIS to check if the map has changed.</span></span> <span data-ttu-id="4baff-107">每次儲存在 [**msSFU-30-網域資訊**](c-mssfu30domaininfo.md) 物件中的資料變更時，這個值就會遞增。</span><span class="sxs-lookup"><span data-stu-id="4baff-107">Every time the data stored in the [**msSFU-30-Domain-Info**](c-mssfu30domaininfo.md) object changes, this value is incremented.</span></span> <span data-ttu-id="4baff-108">此值可用來追蹤 **ypxfer** 呼叫之間的資料變更。</span><span class="sxs-lookup"><span data-stu-id="4baff-108">This value is used to track data changes between **ypxfer** calls.</span></span>



| <span data-ttu-id="4baff-109">進入</span><span class="sxs-lookup"><span data-stu-id="4baff-109">Entry</span></span> | <span data-ttu-id="4baff-110">值</span><span class="sxs-lookup"><span data-stu-id="4baff-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4baff-111">CN</span><span class="sxs-lookup"><span data-stu-id="4baff-111">CN</span></span>                | <span data-ttu-id="4baff-112">msSFU-30-訂購編號</span><span class="sxs-lookup"><span data-stu-id="4baff-112">msSFU-30-Order-Number</span></span>                       |
| <span data-ttu-id="4baff-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4baff-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4baff-114">msSFU30OrderNumber</span><span class="sxs-lookup"><span data-stu-id="4baff-114">msSFU30OrderNumber</span></span>                          |
| <span data-ttu-id="4baff-115">大小</span><span class="sxs-lookup"><span data-stu-id="4baff-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="4baff-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4baff-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="4baff-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4baff-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="4baff-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4baff-118">Attribute-Id</span></span>      | <span data-ttu-id="4baff-119">1.2.840.113556.1.6.18.1.308</span><span class="sxs-lookup"><span data-stu-id="4baff-119">1.2.840.113556.1.6.18.1.308</span></span>                 |
| <span data-ttu-id="4baff-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4baff-120">System-Id-Guid</span></span>    | <span data-ttu-id="4baff-121">02625f05-d1ee-4f9f-b366-55266becb95c</span><span class="sxs-lookup"><span data-stu-id="4baff-121">02625f05-d1ee-4f9f-b366-55266becb95c</span></span>        |
| <span data-ttu-id="4baff-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4baff-122">Syntax</span></span>            | [<span data-ttu-id="4baff-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4baff-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4baff-124">實作</span><span class="sxs-lookup"><span data-stu-id="4baff-124">Implementations</span></span>

-   [<span data-ttu-id="4baff-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4baff-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4baff-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4baff-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4baff-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4baff-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4baff-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4baff-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003-r2"></a><span data-ttu-id="4baff-129">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4baff-129">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4baff-130">進入</span><span class="sxs-lookup"><span data-stu-id="4baff-130">Entry</span></span> | <span data-ttu-id="4baff-131">值</span><span class="sxs-lookup"><span data-stu-id="4baff-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="4baff-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4baff-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="4baff-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4baff-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="4baff-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="4baff-134">System-Only</span></span>            | <span data-ttu-id="4baff-135">否</span><span class="sxs-lookup"><span data-stu-id="4baff-135">False</span></span>                                                          |
| <span data-ttu-id="4baff-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4baff-136">Is-Single-Valued</span></span>       | <span data-ttu-id="4baff-137">對</span><span class="sxs-lookup"><span data-stu-id="4baff-137">True</span></span>                                                           |
| <span data-ttu-id="4baff-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4baff-138">Is Indexed</span></span>             | <span data-ttu-id="4baff-139">對</span><span class="sxs-lookup"><span data-stu-id="4baff-139">True</span></span>                                                           |
| <span data-ttu-id="4baff-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4baff-140">In Global Catalog</span></span>      | <span data-ttu-id="4baff-141">否</span><span class="sxs-lookup"><span data-stu-id="4baff-141">False</span></span>                                                          |
| <span data-ttu-id="4baff-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4baff-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="4baff-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4baff-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="4baff-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4baff-144">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="4baff-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4baff-145">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="4baff-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4baff-146">Search-Flags</span></span>           | <span data-ttu-id="4baff-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4baff-147">0x00000001</span></span>                                                     |
| <span data-ttu-id="4baff-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4baff-148">System-Flags</span></span>           | <span data-ttu-id="4baff-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4baff-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="4baff-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4baff-150">Classes used in</span></span>        | [<span data-ttu-id="4baff-151">**msSFU-30-網域資訊**</span><span class="sxs-lookup"><span data-stu-id="4baff-151">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4baff-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4baff-152">Windows Server 2008</span></span>



| <span data-ttu-id="4baff-153">進入</span><span class="sxs-lookup"><span data-stu-id="4baff-153">Entry</span></span> | <span data-ttu-id="4baff-154">值</span><span class="sxs-lookup"><span data-stu-id="4baff-154">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="4baff-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4baff-155">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="4baff-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4baff-156">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="4baff-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="4baff-157">System-Only</span></span>            | <span data-ttu-id="4baff-158">否</span><span class="sxs-lookup"><span data-stu-id="4baff-158">False</span></span>                                                          |
| <span data-ttu-id="4baff-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4baff-159">Is-Single-Valued</span></span>       | <span data-ttu-id="4baff-160">對</span><span class="sxs-lookup"><span data-stu-id="4baff-160">True</span></span>                                                           |
| <span data-ttu-id="4baff-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4baff-161">Is Indexed</span></span>             | <span data-ttu-id="4baff-162">對</span><span class="sxs-lookup"><span data-stu-id="4baff-162">True</span></span>                                                           |
| <span data-ttu-id="4baff-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4baff-163">In Global Catalog</span></span>      | <span data-ttu-id="4baff-164">否</span><span class="sxs-lookup"><span data-stu-id="4baff-164">False</span></span>                                                          |
| <span data-ttu-id="4baff-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4baff-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="4baff-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4baff-166">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="4baff-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4baff-167">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="4baff-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4baff-168">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="4baff-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4baff-169">Search-Flags</span></span>           | <span data-ttu-id="4baff-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4baff-170">0x00000001</span></span>                                                     |
| <span data-ttu-id="4baff-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4baff-171">System-Flags</span></span>           | <span data-ttu-id="4baff-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4baff-172">0x00000000</span></span>                                                     |
| <span data-ttu-id="4baff-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4baff-173">Classes used in</span></span>        | [<span data-ttu-id="4baff-174">**msSFU-30-網域資訊**</span><span class="sxs-lookup"><span data-stu-id="4baff-174">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4baff-175">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4baff-175">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4baff-176">進入</span><span class="sxs-lookup"><span data-stu-id="4baff-176">Entry</span></span> | <span data-ttu-id="4baff-177">值</span><span class="sxs-lookup"><span data-stu-id="4baff-177">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="4baff-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4baff-178">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="4baff-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4baff-179">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="4baff-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="4baff-180">System-Only</span></span>            | <span data-ttu-id="4baff-181">否</span><span class="sxs-lookup"><span data-stu-id="4baff-181">False</span></span>                                                          |
| <span data-ttu-id="4baff-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4baff-182">Is-Single-Valued</span></span>       | <span data-ttu-id="4baff-183">對</span><span class="sxs-lookup"><span data-stu-id="4baff-183">True</span></span>                                                           |
| <span data-ttu-id="4baff-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4baff-184">Is Indexed</span></span>             | <span data-ttu-id="4baff-185">對</span><span class="sxs-lookup"><span data-stu-id="4baff-185">True</span></span>                                                           |
| <span data-ttu-id="4baff-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4baff-186">In Global Catalog</span></span>      | <span data-ttu-id="4baff-187">否</span><span class="sxs-lookup"><span data-stu-id="4baff-187">False</span></span>                                                          |
| <span data-ttu-id="4baff-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4baff-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="4baff-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4baff-189">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="4baff-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4baff-190">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="4baff-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4baff-191">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="4baff-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4baff-192">Search-Flags</span></span>           | <span data-ttu-id="4baff-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4baff-193">0x00000001</span></span>                                                     |
| <span data-ttu-id="4baff-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4baff-194">System-Flags</span></span>           | <span data-ttu-id="4baff-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4baff-195">0x00000000</span></span>                                                     |
| <span data-ttu-id="4baff-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4baff-196">Classes used in</span></span>        | [<span data-ttu-id="4baff-197">**msSFU-30-網域資訊**</span><span class="sxs-lookup"><span data-stu-id="4baff-197">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4baff-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4baff-198">Windows Server 2012</span></span>



| <span data-ttu-id="4baff-199">進入</span><span class="sxs-lookup"><span data-stu-id="4baff-199">Entry</span></span> | <span data-ttu-id="4baff-200">值</span><span class="sxs-lookup"><span data-stu-id="4baff-200">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="4baff-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4baff-201">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="4baff-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4baff-202">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="4baff-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="4baff-203">System-Only</span></span>            | <span data-ttu-id="4baff-204">否</span><span class="sxs-lookup"><span data-stu-id="4baff-204">False</span></span>                                                          |
| <span data-ttu-id="4baff-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4baff-205">Is-Single-Valued</span></span>       | <span data-ttu-id="4baff-206">對</span><span class="sxs-lookup"><span data-stu-id="4baff-206">True</span></span>                                                           |
| <span data-ttu-id="4baff-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4baff-207">Is Indexed</span></span>             | <span data-ttu-id="4baff-208">對</span><span class="sxs-lookup"><span data-stu-id="4baff-208">True</span></span>                                                           |
| <span data-ttu-id="4baff-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4baff-209">In Global Catalog</span></span>      | <span data-ttu-id="4baff-210">否</span><span class="sxs-lookup"><span data-stu-id="4baff-210">False</span></span>                                                          |
| <span data-ttu-id="4baff-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4baff-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="4baff-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4baff-212">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="4baff-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4baff-213">Range-Lower</span></span>            | \-                                                             |
| <span data-ttu-id="4baff-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4baff-214">Range-Upper</span></span>            | \-                                                             |
| <span data-ttu-id="4baff-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4baff-215">Search-Flags</span></span>           | <span data-ttu-id="4baff-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4baff-216">0x00000001</span></span>                                                     |
| <span data-ttu-id="4baff-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4baff-217">System-Flags</span></span>           | <span data-ttu-id="4baff-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4baff-218">0x00000000</span></span>                                                     |
| <span data-ttu-id="4baff-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4baff-219">Classes used in</span></span>        | [<span data-ttu-id="4baff-220">**msSFU-30-網域資訊**</span><span class="sxs-lookup"><span data-stu-id="4baff-220">**msSFU-30-Domain-Info**</span></span>](c-mssfu30domaininfo.md)<br/> |



 

 





