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
# <a name="parent-guid-attribute"></a><span data-ttu-id="b74cc-106">Parent-GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="b74cc-106">Parent-GUID attribute</span></span>

<span data-ttu-id="b74cc-107">這是已建立來支援 DirSync 控制項的已建立屬性。</span><span class="sxs-lookup"><span data-stu-id="b74cc-107">This is a constructed attribute, invented to support the DirSync control.</span></span> <span data-ttu-id="b74cc-108">這個屬性會在複寫物件的建立、重新命名或移動時，保存物件父系的 objectGuid。</span><span class="sxs-lookup"><span data-stu-id="b74cc-108">This attribute holds the objectGuid of an object's parent when replicating an object's creation, rename, or move.</span></span>



| <span data-ttu-id="b74cc-109">進入</span><span class="sxs-lookup"><span data-stu-id="b74cc-109">Entry</span></span> | <span data-ttu-id="b74cc-110">值</span><span class="sxs-lookup"><span data-stu-id="b74cc-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b74cc-111">CN</span><span class="sxs-lookup"><span data-stu-id="b74cc-111">CN</span></span>                | <span data-ttu-id="b74cc-112">Parent-GUID</span><span class="sxs-lookup"><span data-stu-id="b74cc-112">Parent-GUID</span></span>                                           |
| <span data-ttu-id="b74cc-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b74cc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b74cc-114">parentGUID</span><span class="sxs-lookup"><span data-stu-id="b74cc-114">parentGUID</span></span>                                            |
| <span data-ttu-id="b74cc-115">大小</span><span class="sxs-lookup"><span data-stu-id="b74cc-115">Size</span></span>              | <span data-ttu-id="b74cc-116">16 個位元組</span><span class="sxs-lookup"><span data-stu-id="b74cc-116">16 bytes</span></span>                                              |
| <span data-ttu-id="b74cc-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b74cc-117">Update Privilege</span></span>  | <span data-ttu-id="b74cc-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="b74cc-118">This value is set by the system.</span></span>                      |
| <span data-ttu-id="b74cc-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b74cc-119">Update Frequency</span></span>  | <span data-ttu-id="b74cc-120">複寫期間</span><span class="sxs-lookup"><span data-stu-id="b74cc-120">During replication</span></span>                                    |
| <span data-ttu-id="b74cc-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b74cc-121">Attribute-Id</span></span>      | <span data-ttu-id="b74cc-122">1.2.840.113556.1.4.1224</span><span class="sxs-lookup"><span data-stu-id="b74cc-122">1.2.840.113556.1.4.1224</span></span>                               |
| <span data-ttu-id="b74cc-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b74cc-123">System-Id-Guid</span></span>    | <span data-ttu-id="b74cc-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="b74cc-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span></span>                  |
| <span data-ttu-id="b74cc-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="b74cc-125">Syntax</span></span>            | [<span data-ttu-id="b74cc-126">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b74cc-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b74cc-127">實作</span><span class="sxs-lookup"><span data-stu-id="b74cc-127">Implementations</span></span>

-   [<span data-ttu-id="b74cc-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b74cc-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b74cc-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b74cc-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b74cc-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="b74cc-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b74cc-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b74cc-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b74cc-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b74cc-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b74cc-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b74cc-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b74cc-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b74cc-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b74cc-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b74cc-135">Windows 2000 Server</span></span>



| <span data-ttu-id="b74cc-136">進入</span><span class="sxs-lookup"><span data-stu-id="b74cc-136">Entry</span></span> | <span data-ttu-id="b74cc-137">值</span><span class="sxs-lookup"><span data-stu-id="b74cc-137">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b74cc-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b74cc-138">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b74cc-139">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="b74cc-140">System-Only</span></span>            | <span data-ttu-id="b74cc-141">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-141">True</span></span>         |
| <span data-ttu-id="b74cc-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b74cc-142">Is-Single-Valued</span></span>       | <span data-ttu-id="b74cc-143">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-143">True</span></span>         |
| <span data-ttu-id="b74cc-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b74cc-144">Is Indexed</span></span>             | <span data-ttu-id="b74cc-145">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-145">False</span></span>        |
| <span data-ttu-id="b74cc-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b74cc-146">In Global Catalog</span></span>      | <span data-ttu-id="b74cc-147">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-147">False</span></span>        |
| <span data-ttu-id="b74cc-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b74cc-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="b74cc-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b74cc-149">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b74cc-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b74cc-150">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b74cc-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b74cc-151">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b74cc-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-152">Search-Flags</span></span>           | <span data-ttu-id="b74cc-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b74cc-153">0x00000000</span></span>   |
| <span data-ttu-id="b74cc-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-154">System-Flags</span></span>           | <span data-ttu-id="b74cc-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b74cc-155">0x08000014</span></span>   |
| <span data-ttu-id="b74cc-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b74cc-156">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="b74cc-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b74cc-157">Windows Server 2003</span></span>



| <span data-ttu-id="b74cc-158">進入</span><span class="sxs-lookup"><span data-stu-id="b74cc-158">Entry</span></span> | <span data-ttu-id="b74cc-159">值</span><span class="sxs-lookup"><span data-stu-id="b74cc-159">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b74cc-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b74cc-160">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b74cc-161">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="b74cc-162">System-Only</span></span>            | <span data-ttu-id="b74cc-163">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-163">True</span></span>         |
| <span data-ttu-id="b74cc-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b74cc-164">Is-Single-Valued</span></span>       | <span data-ttu-id="b74cc-165">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-165">True</span></span>         |
| <span data-ttu-id="b74cc-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b74cc-166">Is Indexed</span></span>             | <span data-ttu-id="b74cc-167">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-167">False</span></span>        |
| <span data-ttu-id="b74cc-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b74cc-168">In Global Catalog</span></span>      | <span data-ttu-id="b74cc-169">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-169">False</span></span>        |
| <span data-ttu-id="b74cc-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b74cc-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="b74cc-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b74cc-171">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b74cc-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b74cc-172">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b74cc-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b74cc-173">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b74cc-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-174">Search-Flags</span></span>           | <span data-ttu-id="b74cc-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b74cc-175">0x00000000</span></span>   |
| <span data-ttu-id="b74cc-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-176">System-Flags</span></span>           | <span data-ttu-id="b74cc-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b74cc-177">0x08000014</span></span>   |
| <span data-ttu-id="b74cc-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b74cc-178">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="b74cc-179">亞當</span><span class="sxs-lookup"><span data-stu-id="b74cc-179">ADAM</span></span>



| <span data-ttu-id="b74cc-180">進入</span><span class="sxs-lookup"><span data-stu-id="b74cc-180">Entry</span></span> | <span data-ttu-id="b74cc-181">值</span><span class="sxs-lookup"><span data-stu-id="b74cc-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b74cc-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b74cc-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b74cc-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b74cc-184">System-Only</span></span>            | <span data-ttu-id="b74cc-185">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-185">True</span></span>         |
| <span data-ttu-id="b74cc-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b74cc-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b74cc-187">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-187">True</span></span>         |
| <span data-ttu-id="b74cc-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b74cc-188">Is Indexed</span></span>             | <span data-ttu-id="b74cc-189">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-189">False</span></span>        |
| <span data-ttu-id="b74cc-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b74cc-190">In Global Catalog</span></span>      | <span data-ttu-id="b74cc-191">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-191">False</span></span>        |
| <span data-ttu-id="b74cc-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b74cc-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b74cc-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b74cc-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b74cc-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b74cc-194">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b74cc-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b74cc-195">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b74cc-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-196">Search-Flags</span></span>           | <span data-ttu-id="b74cc-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b74cc-197">0x00000000</span></span>   |
| <span data-ttu-id="b74cc-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-198">System-Flags</span></span>           | <span data-ttu-id="b74cc-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b74cc-199">0x08000014</span></span>   |
| <span data-ttu-id="b74cc-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b74cc-200">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b74cc-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b74cc-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b74cc-202">進入</span><span class="sxs-lookup"><span data-stu-id="b74cc-202">Entry</span></span> | <span data-ttu-id="b74cc-203">值</span><span class="sxs-lookup"><span data-stu-id="b74cc-203">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b74cc-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b74cc-204">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b74cc-205">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b74cc-206">System-Only</span></span>            | <span data-ttu-id="b74cc-207">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-207">True</span></span>         |
| <span data-ttu-id="b74cc-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b74cc-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b74cc-209">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-209">True</span></span>         |
| <span data-ttu-id="b74cc-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b74cc-210">Is Indexed</span></span>             | <span data-ttu-id="b74cc-211">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-211">False</span></span>        |
| <span data-ttu-id="b74cc-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b74cc-212">In Global Catalog</span></span>      | <span data-ttu-id="b74cc-213">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-213">False</span></span>        |
| <span data-ttu-id="b74cc-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b74cc-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b74cc-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b74cc-215">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b74cc-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b74cc-216">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b74cc-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b74cc-217">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b74cc-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-218">Search-Flags</span></span>           | <span data-ttu-id="b74cc-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b74cc-219">0x00000000</span></span>   |
| <span data-ttu-id="b74cc-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-220">System-Flags</span></span>           | <span data-ttu-id="b74cc-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b74cc-221">0x08000014</span></span>   |
| <span data-ttu-id="b74cc-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b74cc-222">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="b74cc-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b74cc-223">Windows Server 2008</span></span>



| <span data-ttu-id="b74cc-224">進入</span><span class="sxs-lookup"><span data-stu-id="b74cc-224">Entry</span></span> | <span data-ttu-id="b74cc-225">值</span><span class="sxs-lookup"><span data-stu-id="b74cc-225">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b74cc-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b74cc-226">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b74cc-227">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="b74cc-228">System-Only</span></span>            | <span data-ttu-id="b74cc-229">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-229">True</span></span>         |
| <span data-ttu-id="b74cc-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b74cc-230">Is-Single-Valued</span></span>       | <span data-ttu-id="b74cc-231">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-231">True</span></span>         |
| <span data-ttu-id="b74cc-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b74cc-232">Is Indexed</span></span>             | <span data-ttu-id="b74cc-233">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-233">False</span></span>        |
| <span data-ttu-id="b74cc-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b74cc-234">In Global Catalog</span></span>      | <span data-ttu-id="b74cc-235">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-235">False</span></span>        |
| <span data-ttu-id="b74cc-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b74cc-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="b74cc-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b74cc-237">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b74cc-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b74cc-238">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b74cc-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b74cc-239">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b74cc-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-240">Search-Flags</span></span>           | <span data-ttu-id="b74cc-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b74cc-241">0x00000000</span></span>   |
| <span data-ttu-id="b74cc-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-242">System-Flags</span></span>           | <span data-ttu-id="b74cc-243">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b74cc-243">0x08000014</span></span>   |
| <span data-ttu-id="b74cc-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b74cc-244">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b74cc-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b74cc-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b74cc-246">進入</span><span class="sxs-lookup"><span data-stu-id="b74cc-246">Entry</span></span> | <span data-ttu-id="b74cc-247">值</span><span class="sxs-lookup"><span data-stu-id="b74cc-247">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b74cc-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b74cc-248">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b74cc-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b74cc-250">System-Only</span></span>            | <span data-ttu-id="b74cc-251">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-251">True</span></span>         |
| <span data-ttu-id="b74cc-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b74cc-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b74cc-253">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-253">True</span></span>         |
| <span data-ttu-id="b74cc-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b74cc-254">Is Indexed</span></span>             | <span data-ttu-id="b74cc-255">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-255">False</span></span>        |
| <span data-ttu-id="b74cc-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b74cc-256">In Global Catalog</span></span>      | <span data-ttu-id="b74cc-257">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-257">False</span></span>        |
| <span data-ttu-id="b74cc-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b74cc-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b74cc-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b74cc-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b74cc-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b74cc-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b74cc-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b74cc-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b74cc-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-262">Search-Flags</span></span>           | <span data-ttu-id="b74cc-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b74cc-263">0x00000000</span></span>   |
| <span data-ttu-id="b74cc-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-264">System-Flags</span></span>           | <span data-ttu-id="b74cc-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b74cc-265">0x08000014</span></span>   |
| <span data-ttu-id="b74cc-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b74cc-266">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="b74cc-267">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b74cc-267">Windows Server 2012</span></span>



| <span data-ttu-id="b74cc-268">進入</span><span class="sxs-lookup"><span data-stu-id="b74cc-268">Entry</span></span> | <span data-ttu-id="b74cc-269">值</span><span class="sxs-lookup"><span data-stu-id="b74cc-269">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="b74cc-270">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b74cc-270">Link-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b74cc-271">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="b74cc-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="b74cc-272">System-Only</span></span>            | <span data-ttu-id="b74cc-273">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-273">True</span></span>         |
| <span data-ttu-id="b74cc-274">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b74cc-274">Is-Single-Valued</span></span>       | <span data-ttu-id="b74cc-275">對</span><span class="sxs-lookup"><span data-stu-id="b74cc-275">True</span></span>         |
| <span data-ttu-id="b74cc-276">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b74cc-276">Is Indexed</span></span>             | <span data-ttu-id="b74cc-277">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-277">False</span></span>        |
| <span data-ttu-id="b74cc-278">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b74cc-278">In Global Catalog</span></span>      | <span data-ttu-id="b74cc-279">否</span><span class="sxs-lookup"><span data-stu-id="b74cc-279">False</span></span>        |
| <span data-ttu-id="b74cc-280">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b74cc-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="b74cc-281">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b74cc-281">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="b74cc-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b74cc-282">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="b74cc-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b74cc-283">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="b74cc-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-284">Search-Flags</span></span>           | <span data-ttu-id="b74cc-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b74cc-285">0x00000000</span></span>   |
| <span data-ttu-id="b74cc-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b74cc-286">System-Flags</span></span>           | <span data-ttu-id="b74cc-287">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b74cc-287">0x08000014</span></span>   |
| <span data-ttu-id="b74cc-288">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b74cc-288">Classes used in</span></span>        | \-           |



 

 




