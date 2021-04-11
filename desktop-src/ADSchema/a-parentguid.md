---
title: Parent-GUID 屬性
description: 這是已建立來支援 DirSync 控制項的已建立屬性。 這個屬性會在複寫物件的建立、重新命名或移動時，保存物件父系的 objectGuid。
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- Parent-GUID 屬性 AD 架構
- parentGUID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b01faf958f4add9c7788d630321d7c225f5026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845352"
---
# <a name="parent-guid-attribute"></a><span data-ttu-id="e332b-106">Parent-GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="e332b-106">Parent-GUID attribute</span></span>

<span data-ttu-id="e332b-107">這是已建立來支援 DirSync 控制項的已建立屬性。</span><span class="sxs-lookup"><span data-stu-id="e332b-107">This is a constructed attribute, invented to support the DirSync control.</span></span> <span data-ttu-id="e332b-108">這個屬性會在複寫物件的建立、重新命名或移動時，保存物件父系的 objectGuid。</span><span class="sxs-lookup"><span data-stu-id="e332b-108">This attribute holds the objectGuid of an object's parent when replicating an object's creation, rename, or move.</span></span>



| <span data-ttu-id="e332b-109">進入</span><span class="sxs-lookup"><span data-stu-id="e332b-109">Entry</span></span> | <span data-ttu-id="e332b-110">值</span><span class="sxs-lookup"><span data-stu-id="e332b-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="e332b-111">CN</span><span class="sxs-lookup"><span data-stu-id="e332b-111">CN</span></span>                | <span data-ttu-id="e332b-112">Parent-GUID</span><span class="sxs-lookup"><span data-stu-id="e332b-112">Parent-GUID</span></span>                                           |
| <span data-ttu-id="e332b-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e332b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e332b-114">parentGUID</span><span class="sxs-lookup"><span data-stu-id="e332b-114">parentGUID</span></span>                                            |
| <span data-ttu-id="e332b-115">大小</span><span class="sxs-lookup"><span data-stu-id="e332b-115">Size</span></span>              | <span data-ttu-id="e332b-116">16 個位元組</span><span class="sxs-lookup"><span data-stu-id="e332b-116">16 bytes</span></span>                                              |
| <span data-ttu-id="e332b-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e332b-117">Update Privilege</span></span>  | <span data-ttu-id="e332b-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="e332b-118">This value is set by the system.</span></span>                      |
| <span data-ttu-id="e332b-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e332b-119">Update Frequency</span></span>  | <span data-ttu-id="e332b-120">複寫期間</span><span class="sxs-lookup"><span data-stu-id="e332b-120">During replication</span></span>                                    |
| <span data-ttu-id="e332b-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e332b-121">Attribute-Id</span></span>      | <span data-ttu-id="e332b-122">1.2.840.113556.1.4.1224</span><span class="sxs-lookup"><span data-stu-id="e332b-122">1.2.840.113556.1.4.1224</span></span>                               |
| <span data-ttu-id="e332b-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e332b-123">System-Id-Guid</span></span>    | <span data-ttu-id="e332b-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="e332b-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span></span>                  |
| <span data-ttu-id="e332b-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="e332b-125">Syntax</span></span>            | [<span data-ttu-id="e332b-126">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="e332b-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="e332b-127">實作</span><span class="sxs-lookup"><span data-stu-id="e332b-127">Implementations</span></span>

-   [<span data-ttu-id="e332b-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e332b-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e332b-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e332b-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e332b-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e332b-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e332b-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e332b-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e332b-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e332b-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e332b-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e332b-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e332b-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e332b-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e332b-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e332b-135">Windows 2000 Server</span></span>



| <span data-ttu-id="e332b-136">進入</span><span class="sxs-lookup"><span data-stu-id="e332b-136">Entry</span></span> | <span data-ttu-id="e332b-137">值</span><span class="sxs-lookup"><span data-stu-id="e332b-137">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="e332b-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e332b-138">Link-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e332b-139">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="e332b-140">System-Only</span></span>            | <span data-ttu-id="e332b-141">對</span><span class="sxs-lookup"><span data-stu-id="e332b-141">True</span></span>         |
| <span data-ttu-id="e332b-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e332b-142">Is-Single-Valued</span></span>       | <span data-ttu-id="e332b-143">對</span><span class="sxs-lookup"><span data-stu-id="e332b-143">True</span></span>         |
| <span data-ttu-id="e332b-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e332b-144">Is Indexed</span></span>             | <span data-ttu-id="e332b-145">否</span><span class="sxs-lookup"><span data-stu-id="e332b-145">False</span></span>        |
| <span data-ttu-id="e332b-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e332b-146">In Global Catalog</span></span>      | <span data-ttu-id="e332b-147">否</span><span class="sxs-lookup"><span data-stu-id="e332b-147">False</span></span>        |
| <span data-ttu-id="e332b-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e332b-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="e332b-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e332b-149">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="e332b-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e332b-150">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="e332b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e332b-151">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="e332b-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-152">Search-Flags</span></span>           | <span data-ttu-id="e332b-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e332b-153">0x00000000</span></span>   |
| <span data-ttu-id="e332b-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-154">System-Flags</span></span>           | <span data-ttu-id="e332b-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e332b-155">0x08000014</span></span>   |
| <span data-ttu-id="e332b-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e332b-156">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="e332b-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e332b-157">Windows Server 2003</span></span>



| <span data-ttu-id="e332b-158">進入</span><span class="sxs-lookup"><span data-stu-id="e332b-158">Entry</span></span> | <span data-ttu-id="e332b-159">值</span><span class="sxs-lookup"><span data-stu-id="e332b-159">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="e332b-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e332b-160">Link-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e332b-161">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="e332b-162">System-Only</span></span>            | <span data-ttu-id="e332b-163">對</span><span class="sxs-lookup"><span data-stu-id="e332b-163">True</span></span>         |
| <span data-ttu-id="e332b-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e332b-164">Is-Single-Valued</span></span>       | <span data-ttu-id="e332b-165">對</span><span class="sxs-lookup"><span data-stu-id="e332b-165">True</span></span>         |
| <span data-ttu-id="e332b-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e332b-166">Is Indexed</span></span>             | <span data-ttu-id="e332b-167">否</span><span class="sxs-lookup"><span data-stu-id="e332b-167">False</span></span>        |
| <span data-ttu-id="e332b-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e332b-168">In Global Catalog</span></span>      | <span data-ttu-id="e332b-169">否</span><span class="sxs-lookup"><span data-stu-id="e332b-169">False</span></span>        |
| <span data-ttu-id="e332b-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e332b-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="e332b-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e332b-171">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="e332b-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e332b-172">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="e332b-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e332b-173">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="e332b-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-174">Search-Flags</span></span>           | <span data-ttu-id="e332b-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e332b-175">0x00000000</span></span>   |
| <span data-ttu-id="e332b-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-176">System-Flags</span></span>           | <span data-ttu-id="e332b-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e332b-177">0x08000014</span></span>   |
| <span data-ttu-id="e332b-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e332b-178">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="e332b-179">亞當</span><span class="sxs-lookup"><span data-stu-id="e332b-179">ADAM</span></span>



| <span data-ttu-id="e332b-180">進入</span><span class="sxs-lookup"><span data-stu-id="e332b-180">Entry</span></span> | <span data-ttu-id="e332b-181">值</span><span class="sxs-lookup"><span data-stu-id="e332b-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="e332b-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e332b-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e332b-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e332b-184">System-Only</span></span>            | <span data-ttu-id="e332b-185">對</span><span class="sxs-lookup"><span data-stu-id="e332b-185">True</span></span>         |
| <span data-ttu-id="e332b-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e332b-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e332b-187">對</span><span class="sxs-lookup"><span data-stu-id="e332b-187">True</span></span>         |
| <span data-ttu-id="e332b-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e332b-188">Is Indexed</span></span>             | <span data-ttu-id="e332b-189">否</span><span class="sxs-lookup"><span data-stu-id="e332b-189">False</span></span>        |
| <span data-ttu-id="e332b-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e332b-190">In Global Catalog</span></span>      | <span data-ttu-id="e332b-191">否</span><span class="sxs-lookup"><span data-stu-id="e332b-191">False</span></span>        |
| <span data-ttu-id="e332b-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e332b-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e332b-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e332b-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="e332b-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e332b-194">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="e332b-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e332b-195">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="e332b-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-196">Search-Flags</span></span>           | <span data-ttu-id="e332b-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e332b-197">0x00000000</span></span>   |
| <span data-ttu-id="e332b-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-198">System-Flags</span></span>           | <span data-ttu-id="e332b-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e332b-199">0x08000014</span></span>   |
| <span data-ttu-id="e332b-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e332b-200">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e332b-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e332b-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e332b-202">進入</span><span class="sxs-lookup"><span data-stu-id="e332b-202">Entry</span></span> | <span data-ttu-id="e332b-203">值</span><span class="sxs-lookup"><span data-stu-id="e332b-203">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="e332b-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e332b-204">Link-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e332b-205">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="e332b-206">System-Only</span></span>            | <span data-ttu-id="e332b-207">對</span><span class="sxs-lookup"><span data-stu-id="e332b-207">True</span></span>         |
| <span data-ttu-id="e332b-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e332b-208">Is-Single-Valued</span></span>       | <span data-ttu-id="e332b-209">對</span><span class="sxs-lookup"><span data-stu-id="e332b-209">True</span></span>         |
| <span data-ttu-id="e332b-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e332b-210">Is Indexed</span></span>             | <span data-ttu-id="e332b-211">否</span><span class="sxs-lookup"><span data-stu-id="e332b-211">False</span></span>        |
| <span data-ttu-id="e332b-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e332b-212">In Global Catalog</span></span>      | <span data-ttu-id="e332b-213">否</span><span class="sxs-lookup"><span data-stu-id="e332b-213">False</span></span>        |
| <span data-ttu-id="e332b-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e332b-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="e332b-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e332b-215">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="e332b-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e332b-216">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="e332b-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e332b-217">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="e332b-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-218">Search-Flags</span></span>           | <span data-ttu-id="e332b-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e332b-219">0x00000000</span></span>   |
| <span data-ttu-id="e332b-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-220">System-Flags</span></span>           | <span data-ttu-id="e332b-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e332b-221">0x08000014</span></span>   |
| <span data-ttu-id="e332b-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e332b-222">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="e332b-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e332b-223">Windows Server 2008</span></span>



| <span data-ttu-id="e332b-224">進入</span><span class="sxs-lookup"><span data-stu-id="e332b-224">Entry</span></span> | <span data-ttu-id="e332b-225">值</span><span class="sxs-lookup"><span data-stu-id="e332b-225">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="e332b-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e332b-226">Link-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e332b-227">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e332b-228">System-Only</span></span>            | <span data-ttu-id="e332b-229">對</span><span class="sxs-lookup"><span data-stu-id="e332b-229">True</span></span>         |
| <span data-ttu-id="e332b-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e332b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e332b-231">對</span><span class="sxs-lookup"><span data-stu-id="e332b-231">True</span></span>         |
| <span data-ttu-id="e332b-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e332b-232">Is Indexed</span></span>             | <span data-ttu-id="e332b-233">否</span><span class="sxs-lookup"><span data-stu-id="e332b-233">False</span></span>        |
| <span data-ttu-id="e332b-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e332b-234">In Global Catalog</span></span>      | <span data-ttu-id="e332b-235">否</span><span class="sxs-lookup"><span data-stu-id="e332b-235">False</span></span>        |
| <span data-ttu-id="e332b-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e332b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e332b-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e332b-237">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="e332b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e332b-238">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="e332b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e332b-239">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="e332b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-240">Search-Flags</span></span>           | <span data-ttu-id="e332b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e332b-241">0x00000000</span></span>   |
| <span data-ttu-id="e332b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-242">System-Flags</span></span>           | <span data-ttu-id="e332b-243">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e332b-243">0x08000014</span></span>   |
| <span data-ttu-id="e332b-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e332b-244">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e332b-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e332b-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e332b-246">進入</span><span class="sxs-lookup"><span data-stu-id="e332b-246">Entry</span></span> | <span data-ttu-id="e332b-247">值</span><span class="sxs-lookup"><span data-stu-id="e332b-247">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="e332b-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e332b-248">Link-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e332b-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e332b-250">System-Only</span></span>            | <span data-ttu-id="e332b-251">對</span><span class="sxs-lookup"><span data-stu-id="e332b-251">True</span></span>         |
| <span data-ttu-id="e332b-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e332b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e332b-253">對</span><span class="sxs-lookup"><span data-stu-id="e332b-253">True</span></span>         |
| <span data-ttu-id="e332b-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e332b-254">Is Indexed</span></span>             | <span data-ttu-id="e332b-255">否</span><span class="sxs-lookup"><span data-stu-id="e332b-255">False</span></span>        |
| <span data-ttu-id="e332b-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e332b-256">In Global Catalog</span></span>      | <span data-ttu-id="e332b-257">否</span><span class="sxs-lookup"><span data-stu-id="e332b-257">False</span></span>        |
| <span data-ttu-id="e332b-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e332b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e332b-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e332b-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="e332b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e332b-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="e332b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e332b-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="e332b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-262">Search-Flags</span></span>           | <span data-ttu-id="e332b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e332b-263">0x00000000</span></span>   |
| <span data-ttu-id="e332b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-264">System-Flags</span></span>           | <span data-ttu-id="e332b-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e332b-265">0x08000014</span></span>   |
| <span data-ttu-id="e332b-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e332b-266">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="e332b-267">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e332b-267">Windows Server 2012</span></span>



| <span data-ttu-id="e332b-268">進入</span><span class="sxs-lookup"><span data-stu-id="e332b-268">Entry</span></span> | <span data-ttu-id="e332b-269">值</span><span class="sxs-lookup"><span data-stu-id="e332b-269">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="e332b-270">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e332b-270">Link-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e332b-271">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="e332b-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="e332b-272">System-Only</span></span>            | <span data-ttu-id="e332b-273">對</span><span class="sxs-lookup"><span data-stu-id="e332b-273">True</span></span>         |
| <span data-ttu-id="e332b-274">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e332b-274">Is-Single-Valued</span></span>       | <span data-ttu-id="e332b-275">對</span><span class="sxs-lookup"><span data-stu-id="e332b-275">True</span></span>         |
| <span data-ttu-id="e332b-276">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e332b-276">Is Indexed</span></span>             | <span data-ttu-id="e332b-277">否</span><span class="sxs-lookup"><span data-stu-id="e332b-277">False</span></span>        |
| <span data-ttu-id="e332b-278">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e332b-278">In Global Catalog</span></span>      | <span data-ttu-id="e332b-279">否</span><span class="sxs-lookup"><span data-stu-id="e332b-279">False</span></span>        |
| <span data-ttu-id="e332b-280">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e332b-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="e332b-281">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e332b-281">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="e332b-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e332b-282">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="e332b-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e332b-283">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="e332b-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-284">Search-Flags</span></span>           | <span data-ttu-id="e332b-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e332b-285">0x00000000</span></span>   |
| <span data-ttu-id="e332b-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e332b-286">System-Flags</span></span>           | <span data-ttu-id="e332b-287">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e332b-287">0x08000014</span></span>   |
| <span data-ttu-id="e332b-288">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e332b-288">Classes used in</span></span>        | \-           |



 

 




