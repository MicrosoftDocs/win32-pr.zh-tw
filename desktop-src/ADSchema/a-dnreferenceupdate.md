---
title: DN-參考-更新屬性
description: 如果重新命名物件，這個屬性會用來追蹤所有已指派給物件的先前和目前名稱，讓連結的物件仍然可以找到它。
ms.assetid: 28e02a38-eed8-475c-a381-145857477ec6
ms.tgt_platform: multiple
keywords:
- DN-參考-更新屬性 AD 架構
- dNReferenceUpdate 屬性 AD 架構
topic_type:
- apiref
api_name:
- DN-Reference-Update
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71e8360be6e7ed6697363daa0f6ff32e2ec5fb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970267"
---
# <a name="dn-reference-update-attribute"></a><span data-ttu-id="a6865-105">DN-參考-更新屬性</span><span class="sxs-lookup"><span data-stu-id="a6865-105">DN-Reference-Update attribute</span></span>

<span data-ttu-id="a6865-106">如果重新命名物件，這個屬性會用來追蹤所有已指派給物件的先前和目前名稱，讓連結的物件仍然可以找到它。</span><span class="sxs-lookup"><span data-stu-id="a6865-106">If an object is renamed, this attribute is used to track all of the previous and current names that have been assigned to an object so that linked objects can still find it.</span></span>



| <span data-ttu-id="a6865-107">進入</span><span class="sxs-lookup"><span data-stu-id="a6865-107">Entry</span></span> | <span data-ttu-id="a6865-108">值</span><span class="sxs-lookup"><span data-stu-id="a6865-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="a6865-109">CN</span><span class="sxs-lookup"><span data-stu-id="a6865-109">CN</span></span>                | <span data-ttu-id="a6865-110">DN-參考-更新</span><span class="sxs-lookup"><span data-stu-id="a6865-110">DN-Reference-Update</span></span>                     |
| <span data-ttu-id="a6865-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a6865-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a6865-112">dNReferenceUpdate</span><span class="sxs-lookup"><span data-stu-id="a6865-112">dNReferenceUpdate</span></span>                       |
| <span data-ttu-id="a6865-113">大小</span><span class="sxs-lookup"><span data-stu-id="a6865-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="a6865-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a6865-114">Update Privilege</span></span>  | <span data-ttu-id="a6865-115">這是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="a6865-115">This is set by the system.</span></span>              |
| <span data-ttu-id="a6865-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a6865-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="a6865-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a6865-117">Attribute-Id</span></span>      | <span data-ttu-id="a6865-118">1.2.840.113556.1.4.1242</span><span class="sxs-lookup"><span data-stu-id="a6865-118">1.2.840.113556.1.4.1242</span></span>                 |
| <span data-ttu-id="a6865-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a6865-119">System-Id-Guid</span></span>    | <span data-ttu-id="a6865-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="a6865-120">2df90d86-009f-11d2-aa4c-00c04fd7d83a</span></span>    |
| <span data-ttu-id="a6865-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6865-121">Syntax</span></span>            | [<span data-ttu-id="a6865-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a6865-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="a6865-123">實作</span><span class="sxs-lookup"><span data-stu-id="a6865-123">Implementations</span></span>

-   [<span data-ttu-id="a6865-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a6865-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a6865-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a6865-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a6865-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a6865-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a6865-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a6865-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a6865-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a6865-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a6865-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a6865-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a6865-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a6865-130">Windows 2000 Server</span></span>



| <span data-ttu-id="a6865-131">進入</span><span class="sxs-lookup"><span data-stu-id="a6865-131">Entry</span></span> | <span data-ttu-id="a6865-132">值</span><span class="sxs-lookup"><span data-stu-id="a6865-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a6865-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6865-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a6865-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6865-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a6865-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6865-135">System-Only</span></span>            | <span data-ttu-id="a6865-136">對</span><span class="sxs-lookup"><span data-stu-id="a6865-136">True</span></span>                                                               |
| <span data-ttu-id="a6865-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6865-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a6865-138">否</span><span class="sxs-lookup"><span data-stu-id="a6865-138">False</span></span>                                                              |
| <span data-ttu-id="a6865-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6865-139">Is Indexed</span></span>             | <span data-ttu-id="a6865-140">否</span><span class="sxs-lookup"><span data-stu-id="a6865-140">False</span></span>                                                              |
| <span data-ttu-id="a6865-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6865-141">In Global Catalog</span></span>      | <span data-ttu-id="a6865-142">否</span><span class="sxs-lookup"><span data-stu-id="a6865-142">False</span></span>                                                              |
| <span data-ttu-id="a6865-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6865-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6865-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6865-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="a6865-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6865-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="a6865-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6865-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="a6865-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6865-147">Search-Flags</span></span>           | <span data-ttu-id="a6865-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a6865-148">0x00000008</span></span>                                                         |
| <span data-ttu-id="a6865-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6865-149">System-Flags</span></span>           | <span data-ttu-id="a6865-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6865-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="a6865-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6865-151">Classes used in</span></span>        | [<span data-ttu-id="a6865-152">**基礎結構-更新**</span><span class="sxs-lookup"><span data-stu-id="a6865-152">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a6865-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a6865-153">Windows Server 2003</span></span>



| <span data-ttu-id="a6865-154">進入</span><span class="sxs-lookup"><span data-stu-id="a6865-154">Entry</span></span> | <span data-ttu-id="a6865-155">值</span><span class="sxs-lookup"><span data-stu-id="a6865-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a6865-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6865-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a6865-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6865-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a6865-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6865-158">System-Only</span></span>            | <span data-ttu-id="a6865-159">對</span><span class="sxs-lookup"><span data-stu-id="a6865-159">True</span></span>                                                               |
| <span data-ttu-id="a6865-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6865-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a6865-161">否</span><span class="sxs-lookup"><span data-stu-id="a6865-161">False</span></span>                                                              |
| <span data-ttu-id="a6865-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6865-162">Is Indexed</span></span>             | <span data-ttu-id="a6865-163">否</span><span class="sxs-lookup"><span data-stu-id="a6865-163">False</span></span>                                                              |
| <span data-ttu-id="a6865-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6865-164">In Global Catalog</span></span>      | <span data-ttu-id="a6865-165">否</span><span class="sxs-lookup"><span data-stu-id="a6865-165">False</span></span>                                                              |
| <span data-ttu-id="a6865-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6865-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6865-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6865-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="a6865-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6865-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="a6865-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6865-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="a6865-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6865-170">Search-Flags</span></span>           | <span data-ttu-id="a6865-171">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a6865-171">0x00000008</span></span>                                                         |
| <span data-ttu-id="a6865-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6865-172">System-Flags</span></span>           | <span data-ttu-id="a6865-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6865-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="a6865-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6865-174">Classes used in</span></span>        | [<span data-ttu-id="a6865-175">**基礎結構-更新**</span><span class="sxs-lookup"><span data-stu-id="a6865-175">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a6865-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a6865-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a6865-177">進入</span><span class="sxs-lookup"><span data-stu-id="a6865-177">Entry</span></span> | <span data-ttu-id="a6865-178">值</span><span class="sxs-lookup"><span data-stu-id="a6865-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a6865-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6865-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a6865-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6865-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a6865-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6865-181">System-Only</span></span>            | <span data-ttu-id="a6865-182">對</span><span class="sxs-lookup"><span data-stu-id="a6865-182">True</span></span>                                                               |
| <span data-ttu-id="a6865-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6865-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a6865-184">否</span><span class="sxs-lookup"><span data-stu-id="a6865-184">False</span></span>                                                              |
| <span data-ttu-id="a6865-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6865-185">Is Indexed</span></span>             | <span data-ttu-id="a6865-186">否</span><span class="sxs-lookup"><span data-stu-id="a6865-186">False</span></span>                                                              |
| <span data-ttu-id="a6865-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6865-187">In Global Catalog</span></span>      | <span data-ttu-id="a6865-188">否</span><span class="sxs-lookup"><span data-stu-id="a6865-188">False</span></span>                                                              |
| <span data-ttu-id="a6865-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6865-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6865-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6865-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="a6865-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6865-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="a6865-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6865-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="a6865-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6865-193">Search-Flags</span></span>           | <span data-ttu-id="a6865-194">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a6865-194">0x00000008</span></span>                                                         |
| <span data-ttu-id="a6865-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6865-195">System-Flags</span></span>           | <span data-ttu-id="a6865-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6865-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="a6865-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6865-197">Classes used in</span></span>        | [<span data-ttu-id="a6865-198">**基礎結構-更新**</span><span class="sxs-lookup"><span data-stu-id="a6865-198">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a6865-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6865-199">Windows Server 2008</span></span>



| <span data-ttu-id="a6865-200">進入</span><span class="sxs-lookup"><span data-stu-id="a6865-200">Entry</span></span> | <span data-ttu-id="a6865-201">值</span><span class="sxs-lookup"><span data-stu-id="a6865-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a6865-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6865-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a6865-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6865-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a6865-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6865-204">System-Only</span></span>            | <span data-ttu-id="a6865-205">對</span><span class="sxs-lookup"><span data-stu-id="a6865-205">True</span></span>                                                               |
| <span data-ttu-id="a6865-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6865-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a6865-207">否</span><span class="sxs-lookup"><span data-stu-id="a6865-207">False</span></span>                                                              |
| <span data-ttu-id="a6865-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6865-208">Is Indexed</span></span>             | <span data-ttu-id="a6865-209">否</span><span class="sxs-lookup"><span data-stu-id="a6865-209">False</span></span>                                                              |
| <span data-ttu-id="a6865-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6865-210">In Global Catalog</span></span>      | <span data-ttu-id="a6865-211">否</span><span class="sxs-lookup"><span data-stu-id="a6865-211">False</span></span>                                                              |
| <span data-ttu-id="a6865-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6865-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6865-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6865-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="a6865-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6865-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="a6865-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6865-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="a6865-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6865-216">Search-Flags</span></span>           | <span data-ttu-id="a6865-217">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a6865-217">0x00000008</span></span>                                                         |
| <span data-ttu-id="a6865-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6865-218">System-Flags</span></span>           | <span data-ttu-id="a6865-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6865-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="a6865-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6865-220">Classes used in</span></span>        | [<span data-ttu-id="a6865-221">**基礎結構-更新**</span><span class="sxs-lookup"><span data-stu-id="a6865-221">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a6865-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a6865-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a6865-223">進入</span><span class="sxs-lookup"><span data-stu-id="a6865-223">Entry</span></span> | <span data-ttu-id="a6865-224">值</span><span class="sxs-lookup"><span data-stu-id="a6865-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a6865-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6865-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a6865-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6865-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a6865-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6865-227">System-Only</span></span>            | <span data-ttu-id="a6865-228">對</span><span class="sxs-lookup"><span data-stu-id="a6865-228">True</span></span>                                                               |
| <span data-ttu-id="a6865-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6865-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a6865-230">否</span><span class="sxs-lookup"><span data-stu-id="a6865-230">False</span></span>                                                              |
| <span data-ttu-id="a6865-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6865-231">Is Indexed</span></span>             | <span data-ttu-id="a6865-232">否</span><span class="sxs-lookup"><span data-stu-id="a6865-232">False</span></span>                                                              |
| <span data-ttu-id="a6865-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6865-233">In Global Catalog</span></span>      | <span data-ttu-id="a6865-234">否</span><span class="sxs-lookup"><span data-stu-id="a6865-234">False</span></span>                                                              |
| <span data-ttu-id="a6865-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6865-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6865-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6865-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="a6865-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6865-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="a6865-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6865-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="a6865-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6865-239">Search-Flags</span></span>           | <span data-ttu-id="a6865-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a6865-240">0x00000008</span></span>                                                         |
| <span data-ttu-id="a6865-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6865-241">System-Flags</span></span>           | <span data-ttu-id="a6865-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6865-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="a6865-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6865-243">Classes used in</span></span>        | [<span data-ttu-id="a6865-244">**基礎結構-更新**</span><span class="sxs-lookup"><span data-stu-id="a6865-244">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a6865-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a6865-245">Windows Server 2012</span></span>



| <span data-ttu-id="a6865-246">進入</span><span class="sxs-lookup"><span data-stu-id="a6865-246">Entry</span></span> | <span data-ttu-id="a6865-247">值</span><span class="sxs-lookup"><span data-stu-id="a6865-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a6865-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a6865-248">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a6865-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a6865-249">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="a6865-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="a6865-250">System-Only</span></span>            | <span data-ttu-id="a6865-251">對</span><span class="sxs-lookup"><span data-stu-id="a6865-251">True</span></span>                                                               |
| <span data-ttu-id="a6865-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a6865-252">Is-Single-Valued</span></span>       | <span data-ttu-id="a6865-253">否</span><span class="sxs-lookup"><span data-stu-id="a6865-253">False</span></span>                                                              |
| <span data-ttu-id="a6865-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a6865-254">Is Indexed</span></span>             | <span data-ttu-id="a6865-255">否</span><span class="sxs-lookup"><span data-stu-id="a6865-255">False</span></span>                                                              |
| <span data-ttu-id="a6865-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a6865-256">In Global Catalog</span></span>      | <span data-ttu-id="a6865-257">否</span><span class="sxs-lookup"><span data-stu-id="a6865-257">False</span></span>                                                              |
| <span data-ttu-id="a6865-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a6865-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="a6865-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a6865-259">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="a6865-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a6865-260">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="a6865-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a6865-261">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="a6865-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a6865-262">Search-Flags</span></span>           | <span data-ttu-id="a6865-263">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a6865-263">0x00000008</span></span>                                                         |
| <span data-ttu-id="a6865-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a6865-264">System-Flags</span></span>           | <span data-ttu-id="a6865-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a6865-265">0x00000010</span></span>                                                         |
| <span data-ttu-id="a6865-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a6865-266">Classes used in</span></span>        | [<span data-ttu-id="a6865-267">**基礎結構-更新**</span><span class="sxs-lookup"><span data-stu-id="a6865-267">**Infrastructure-Update**</span></span>](c-infrastructureupdate.md)<br/> |



 

 





