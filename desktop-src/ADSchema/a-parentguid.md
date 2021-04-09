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
# <a name="parent-guid-attribute"></a><span data-ttu-id="6a0a3-106">Parent-GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="6a0a3-106">Parent-GUID attribute</span></span>

<span data-ttu-id="6a0a3-107">這是已建立來支援 DirSync 控制項的已建立屬性。</span><span class="sxs-lookup"><span data-stu-id="6a0a3-107">This is a constructed attribute, invented to support the DirSync control.</span></span> <span data-ttu-id="6a0a3-108">這個屬性會在複寫物件的建立、重新命名或移動時，保存物件父系的 objectGuid。</span><span class="sxs-lookup"><span data-stu-id="6a0a3-108">This attribute holds the objectGuid of an object's parent when replicating an object's creation, rename, or move.</span></span>



| <span data-ttu-id="6a0a3-109">進入</span><span class="sxs-lookup"><span data-stu-id="6a0a3-109">Entry</span></span> | <span data-ttu-id="6a0a3-110">值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="6a0a3-111">CN</span><span class="sxs-lookup"><span data-stu-id="6a0a3-111">CN</span></span>                | <span data-ttu-id="6a0a3-112">Parent-GUID</span><span class="sxs-lookup"><span data-stu-id="6a0a3-112">Parent-GUID</span></span>                                           |
| <span data-ttu-id="6a0a3-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6a0a3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6a0a3-114">parentGUID</span><span class="sxs-lookup"><span data-stu-id="6a0a3-114">parentGUID</span></span>                                            |
| <span data-ttu-id="6a0a3-115">大小</span><span class="sxs-lookup"><span data-stu-id="6a0a3-115">Size</span></span>              | <span data-ttu-id="6a0a3-116">16 個位元組</span><span class="sxs-lookup"><span data-stu-id="6a0a3-116">16 bytes</span></span>                                              |
| <span data-ttu-id="6a0a3-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6a0a3-117">Update Privilege</span></span>  | <span data-ttu-id="6a0a3-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="6a0a3-118">This value is set by the system.</span></span>                      |
| <span data-ttu-id="6a0a3-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6a0a3-119">Update Frequency</span></span>  | <span data-ttu-id="6a0a3-120">複寫期間</span><span class="sxs-lookup"><span data-stu-id="6a0a3-120">During replication</span></span>                                    |
| <span data-ttu-id="6a0a3-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6a0a3-121">Attribute-Id</span></span>      | <span data-ttu-id="6a0a3-122">1.2.840.113556.1.4.1224</span><span class="sxs-lookup"><span data-stu-id="6a0a3-122">1.2.840.113556.1.4.1224</span></span>                               |
| <span data-ttu-id="6a0a3-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6a0a3-123">System-Id-Guid</span></span>    | <span data-ttu-id="6a0a3-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="6a0a3-124">2df90d74-009f-11d2-aa4c-00c04fd7d83a</span></span>                  |
| <span data-ttu-id="6a0a3-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a0a3-125">Syntax</span></span>            | [<span data-ttu-id="6a0a3-126">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="6a0a3-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="6a0a3-127">實作</span><span class="sxs-lookup"><span data-stu-id="6a0a3-127">Implementations</span></span>

-   [<span data-ttu-id="6a0a3-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6a0a3-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6a0a3-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6a0a3-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6a0a3-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="6a0a3-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6a0a3-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6a0a3-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6a0a3-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6a0a3-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6a0a3-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6a0a3-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6a0a3-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6a0a3-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6a0a3-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6a0a3-135">Windows 2000 Server</span></span>



| <span data-ttu-id="6a0a3-136">進入</span><span class="sxs-lookup"><span data-stu-id="6a0a3-136">Entry</span></span> | <span data-ttu-id="6a0a3-137">值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-137">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="6a0a3-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a0a3-138">Link-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a0a3-139">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a0a3-140">System-Only</span></span>            | <span data-ttu-id="6a0a3-141">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-141">True</span></span>         |
| <span data-ttu-id="6a0a3-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-142">Is-Single-Valued</span></span>       | <span data-ttu-id="6a0a3-143">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-143">True</span></span>         |
| <span data-ttu-id="6a0a3-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a0a3-144">Is Indexed</span></span>             | <span data-ttu-id="6a0a3-145">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-145">False</span></span>        |
| <span data-ttu-id="6a0a3-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a0a3-146">In Global Catalog</span></span>      | <span data-ttu-id="6a0a3-147">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-147">False</span></span>        |
| <span data-ttu-id="6a0a3-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a0a3-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a0a3-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a0a3-149">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="6a0a3-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a0a3-150">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="6a0a3-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a0a3-151">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="6a0a3-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-152">Search-Flags</span></span>           | <span data-ttu-id="6a0a3-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a0a3-153">0x00000000</span></span>   |
| <span data-ttu-id="6a0a3-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-154">System-Flags</span></span>           | <span data-ttu-id="6a0a3-155">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a0a3-155">0x08000014</span></span>   |
| <span data-ttu-id="6a0a3-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a0a3-156">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003"></a><span data-ttu-id="6a0a3-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a0a3-157">Windows Server 2003</span></span>



| <span data-ttu-id="6a0a3-158">進入</span><span class="sxs-lookup"><span data-stu-id="6a0a3-158">Entry</span></span> | <span data-ttu-id="6a0a3-159">值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-159">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="6a0a3-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a0a3-160">Link-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a0a3-161">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a0a3-162">System-Only</span></span>            | <span data-ttu-id="6a0a3-163">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-163">True</span></span>         |
| <span data-ttu-id="6a0a3-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-164">Is-Single-Valued</span></span>       | <span data-ttu-id="6a0a3-165">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-165">True</span></span>         |
| <span data-ttu-id="6a0a3-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a0a3-166">Is Indexed</span></span>             | <span data-ttu-id="6a0a3-167">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-167">False</span></span>        |
| <span data-ttu-id="6a0a3-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a0a3-168">In Global Catalog</span></span>      | <span data-ttu-id="6a0a3-169">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-169">False</span></span>        |
| <span data-ttu-id="6a0a3-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a0a3-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a0a3-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a0a3-171">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="6a0a3-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a0a3-172">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="6a0a3-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a0a3-173">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="6a0a3-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-174">Search-Flags</span></span>           | <span data-ttu-id="6a0a3-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a0a3-175">0x00000000</span></span>   |
| <span data-ttu-id="6a0a3-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-176">System-Flags</span></span>           | <span data-ttu-id="6a0a3-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a0a3-177">0x08000014</span></span>   |
| <span data-ttu-id="6a0a3-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a0a3-178">Classes used in</span></span>        | \-           |



## <a name="adam"></a><span data-ttu-id="6a0a3-179">亞當</span><span class="sxs-lookup"><span data-stu-id="6a0a3-179">ADAM</span></span>



| <span data-ttu-id="6a0a3-180">進入</span><span class="sxs-lookup"><span data-stu-id="6a0a3-180">Entry</span></span> | <span data-ttu-id="6a0a3-181">值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-181">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="6a0a3-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a0a3-182">Link-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a0a3-183">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a0a3-184">System-Only</span></span>            | <span data-ttu-id="6a0a3-185">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-185">True</span></span>         |
| <span data-ttu-id="6a0a3-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-186">Is-Single-Valued</span></span>       | <span data-ttu-id="6a0a3-187">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-187">True</span></span>         |
| <span data-ttu-id="6a0a3-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a0a3-188">Is Indexed</span></span>             | <span data-ttu-id="6a0a3-189">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-189">False</span></span>        |
| <span data-ttu-id="6a0a3-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a0a3-190">In Global Catalog</span></span>      | <span data-ttu-id="6a0a3-191">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-191">False</span></span>        |
| <span data-ttu-id="6a0a3-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a0a3-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a0a3-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a0a3-193">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="6a0a3-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a0a3-194">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="6a0a3-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a0a3-195">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="6a0a3-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-196">Search-Flags</span></span>           | <span data-ttu-id="6a0a3-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a0a3-197">0x00000000</span></span>   |
| <span data-ttu-id="6a0a3-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-198">System-Flags</span></span>           | <span data-ttu-id="6a0a3-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a0a3-199">0x08000014</span></span>   |
| <span data-ttu-id="6a0a3-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a0a3-200">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6a0a3-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6a0a3-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6a0a3-202">進入</span><span class="sxs-lookup"><span data-stu-id="6a0a3-202">Entry</span></span> | <span data-ttu-id="6a0a3-203">值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-203">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="6a0a3-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a0a3-204">Link-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a0a3-205">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a0a3-206">System-Only</span></span>            | <span data-ttu-id="6a0a3-207">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-207">True</span></span>         |
| <span data-ttu-id="6a0a3-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-208">Is-Single-Valued</span></span>       | <span data-ttu-id="6a0a3-209">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-209">True</span></span>         |
| <span data-ttu-id="6a0a3-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a0a3-210">Is Indexed</span></span>             | <span data-ttu-id="6a0a3-211">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-211">False</span></span>        |
| <span data-ttu-id="6a0a3-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a0a3-212">In Global Catalog</span></span>      | <span data-ttu-id="6a0a3-213">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-213">False</span></span>        |
| <span data-ttu-id="6a0a3-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a0a3-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a0a3-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a0a3-215">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="6a0a3-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a0a3-216">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="6a0a3-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a0a3-217">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="6a0a3-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-218">Search-Flags</span></span>           | <span data-ttu-id="6a0a3-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a0a3-219">0x00000000</span></span>   |
| <span data-ttu-id="6a0a3-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-220">System-Flags</span></span>           | <span data-ttu-id="6a0a3-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a0a3-221">0x08000014</span></span>   |
| <span data-ttu-id="6a0a3-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a0a3-222">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008"></a><span data-ttu-id="6a0a3-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a0a3-223">Windows Server 2008</span></span>



| <span data-ttu-id="6a0a3-224">進入</span><span class="sxs-lookup"><span data-stu-id="6a0a3-224">Entry</span></span> | <span data-ttu-id="6a0a3-225">值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-225">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="6a0a3-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a0a3-226">Link-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a0a3-227">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a0a3-228">System-Only</span></span>            | <span data-ttu-id="6a0a3-229">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-229">True</span></span>         |
| <span data-ttu-id="6a0a3-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-230">Is-Single-Valued</span></span>       | <span data-ttu-id="6a0a3-231">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-231">True</span></span>         |
| <span data-ttu-id="6a0a3-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a0a3-232">Is Indexed</span></span>             | <span data-ttu-id="6a0a3-233">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-233">False</span></span>        |
| <span data-ttu-id="6a0a3-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a0a3-234">In Global Catalog</span></span>      | <span data-ttu-id="6a0a3-235">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-235">False</span></span>        |
| <span data-ttu-id="6a0a3-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a0a3-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a0a3-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a0a3-237">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="6a0a3-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a0a3-238">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="6a0a3-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a0a3-239">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="6a0a3-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-240">Search-Flags</span></span>           | <span data-ttu-id="6a0a3-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a0a3-241">0x00000000</span></span>   |
| <span data-ttu-id="6a0a3-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-242">System-Flags</span></span>           | <span data-ttu-id="6a0a3-243">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a0a3-243">0x08000014</span></span>   |
| <span data-ttu-id="6a0a3-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a0a3-244">Classes used in</span></span>        | \-           |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6a0a3-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a0a3-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6a0a3-246">進入</span><span class="sxs-lookup"><span data-stu-id="6a0a3-246">Entry</span></span> | <span data-ttu-id="6a0a3-247">值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-247">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="6a0a3-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a0a3-248">Link-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a0a3-249">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a0a3-250">System-Only</span></span>            | <span data-ttu-id="6a0a3-251">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-251">True</span></span>         |
| <span data-ttu-id="6a0a3-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-252">Is-Single-Valued</span></span>       | <span data-ttu-id="6a0a3-253">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-253">True</span></span>         |
| <span data-ttu-id="6a0a3-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a0a3-254">Is Indexed</span></span>             | <span data-ttu-id="6a0a3-255">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-255">False</span></span>        |
| <span data-ttu-id="6a0a3-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a0a3-256">In Global Catalog</span></span>      | <span data-ttu-id="6a0a3-257">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-257">False</span></span>        |
| <span data-ttu-id="6a0a3-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a0a3-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a0a3-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a0a3-259">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="6a0a3-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a0a3-260">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="6a0a3-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a0a3-261">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="6a0a3-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-262">Search-Flags</span></span>           | <span data-ttu-id="6a0a3-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a0a3-263">0x00000000</span></span>   |
| <span data-ttu-id="6a0a3-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-264">System-Flags</span></span>           | <span data-ttu-id="6a0a3-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a0a3-265">0x08000014</span></span>   |
| <span data-ttu-id="6a0a3-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a0a3-266">Classes used in</span></span>        | \-           |



## <a name="windows-server-2012"></a><span data-ttu-id="6a0a3-267">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a0a3-267">Windows Server 2012</span></span>



| <span data-ttu-id="6a0a3-268">進入</span><span class="sxs-lookup"><span data-stu-id="6a0a3-268">Entry</span></span> | <span data-ttu-id="6a0a3-269">值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-269">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="6a0a3-270">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a0a3-270">Link-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a0a3-271">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="6a0a3-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a0a3-272">System-Only</span></span>            | <span data-ttu-id="6a0a3-273">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-273">True</span></span>         |
| <span data-ttu-id="6a0a3-274">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a0a3-274">Is-Single-Valued</span></span>       | <span data-ttu-id="6a0a3-275">對</span><span class="sxs-lookup"><span data-stu-id="6a0a3-275">True</span></span>         |
| <span data-ttu-id="6a0a3-276">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a0a3-276">Is Indexed</span></span>             | <span data-ttu-id="6a0a3-277">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-277">False</span></span>        |
| <span data-ttu-id="6a0a3-278">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a0a3-278">In Global Catalog</span></span>      | <span data-ttu-id="6a0a3-279">否</span><span class="sxs-lookup"><span data-stu-id="6a0a3-279">False</span></span>        |
| <span data-ttu-id="6a0a3-280">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a0a3-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a0a3-281">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a0a3-281">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="6a0a3-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a0a3-282">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="6a0a3-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a0a3-283">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="6a0a3-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-284">Search-Flags</span></span>           | <span data-ttu-id="6a0a3-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6a0a3-285">0x00000000</span></span>   |
| <span data-ttu-id="6a0a3-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a0a3-286">System-Flags</span></span>           | <span data-ttu-id="6a0a3-287">0x08000014</span><span class="sxs-lookup"><span data-stu-id="6a0a3-287">0x08000014</span></span>   |
| <span data-ttu-id="6a0a3-288">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a0a3-288">Classes used in</span></span>        | \-           |



 

 




