---
title: 父系-CA 屬性
description: 父 CA 的憑證授權單位單位 (CA) 物件的分辨名稱。
ms.assetid: ccb5b338-e67d-4f1b-b13c-257746ab39d1
ms.tgt_platform: multiple
keywords:
- 父系-CA 屬性 AD 架構
- parentCA 屬性 AD 架構
topic_type:
- apiref
api_name:
- Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c065c86548769ab8643a561c7aec3132728d5d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107984"
---
# <a name="parent-ca-attribute"></a><span data-ttu-id="ac68e-105">父系-CA 屬性</span><span class="sxs-lookup"><span data-stu-id="ac68e-105">Parent-CA attribute</span></span>

<span data-ttu-id="ac68e-106">父 CA 的憑證授權單位單位 (CA) 物件的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="ac68e-106">The distinguished name of a certification authority (CA) object for a parent CA.</span></span>



| <span data-ttu-id="ac68e-107">進入</span><span class="sxs-lookup"><span data-stu-id="ac68e-107">Entry</span></span> | <span data-ttu-id="ac68e-108">值</span><span class="sxs-lookup"><span data-stu-id="ac68e-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="ac68e-109">CN</span><span class="sxs-lookup"><span data-stu-id="ac68e-109">CN</span></span>                | <span data-ttu-id="ac68e-110">父系-CA</span><span class="sxs-lookup"><span data-stu-id="ac68e-110">Parent-CA</span></span>                               |
| <span data-ttu-id="ac68e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ac68e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ac68e-112">parentCA</span><span class="sxs-lookup"><span data-stu-id="ac68e-112">parentCA</span></span>                                |
| <span data-ttu-id="ac68e-113">大小</span><span class="sxs-lookup"><span data-stu-id="ac68e-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="ac68e-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ac68e-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="ac68e-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ac68e-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="ac68e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ac68e-116">Attribute-Id</span></span>      | <span data-ttu-id="ac68e-117">1.2.840.113556.1.4.557</span><span class="sxs-lookup"><span data-stu-id="ac68e-117">1.2.840.113556.1.4.557</span></span>                  |
| <span data-ttu-id="ac68e-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ac68e-118">System-Id-Guid</span></span>    | <span data-ttu-id="ac68e-119">5245801b-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ac68e-119">5245801b-ca6a-11d0-afff-0000f80367c1</span></span>    |
| <span data-ttu-id="ac68e-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac68e-120">Syntax</span></span>            | [<span data-ttu-id="ac68e-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="ac68e-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="ac68e-122">實作</span><span class="sxs-lookup"><span data-stu-id="ac68e-122">Implementations</span></span>

-   [<span data-ttu-id="ac68e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ac68e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ac68e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ac68e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ac68e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ac68e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ac68e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ac68e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ac68e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ac68e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ac68e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ac68e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ac68e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac68e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="ac68e-130">進入</span><span class="sxs-lookup"><span data-stu-id="ac68e-130">Entry</span></span> | <span data-ttu-id="ac68e-131">值</span><span class="sxs-lookup"><span data-stu-id="ac68e-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ac68e-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac68e-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="ac68e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac68e-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="ac68e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac68e-134">System-Only</span></span>            | <span data-ttu-id="ac68e-135">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-135">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac68e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="ac68e-137">對</span><span class="sxs-lookup"><span data-stu-id="ac68e-137">True</span></span>                                                                   |
| <span data-ttu-id="ac68e-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac68e-138">Is Indexed</span></span>             | <span data-ttu-id="ac68e-139">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-139">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac68e-140">In Global Catalog</span></span>      | <span data-ttu-id="ac68e-141">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-141">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac68e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac68e-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac68e-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="ac68e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac68e-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="ac68e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac68e-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="ac68e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac68e-146">Search-Flags</span></span>           | <span data-ttu-id="ac68e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac68e-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="ac68e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac68e-148">System-Flags</span></span>           | <span data-ttu-id="ac68e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac68e-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="ac68e-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac68e-150">Classes used in</span></span>        | [<span data-ttu-id="ac68e-151">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="ac68e-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ac68e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ac68e-152">Windows Server 2003</span></span>



| <span data-ttu-id="ac68e-153">進入</span><span class="sxs-lookup"><span data-stu-id="ac68e-153">Entry</span></span> | <span data-ttu-id="ac68e-154">值</span><span class="sxs-lookup"><span data-stu-id="ac68e-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ac68e-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac68e-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="ac68e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac68e-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="ac68e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac68e-157">System-Only</span></span>            | <span data-ttu-id="ac68e-158">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-158">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac68e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="ac68e-160">對</span><span class="sxs-lookup"><span data-stu-id="ac68e-160">True</span></span>                                                                   |
| <span data-ttu-id="ac68e-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac68e-161">Is Indexed</span></span>             | <span data-ttu-id="ac68e-162">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-162">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac68e-163">In Global Catalog</span></span>      | <span data-ttu-id="ac68e-164">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-164">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac68e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac68e-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac68e-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="ac68e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac68e-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="ac68e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac68e-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="ac68e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac68e-169">Search-Flags</span></span>           | <span data-ttu-id="ac68e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac68e-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="ac68e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac68e-171">System-Flags</span></span>           | <span data-ttu-id="ac68e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac68e-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="ac68e-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac68e-173">Classes used in</span></span>        | [<span data-ttu-id="ac68e-174">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="ac68e-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ac68e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ac68e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ac68e-176">進入</span><span class="sxs-lookup"><span data-stu-id="ac68e-176">Entry</span></span> | <span data-ttu-id="ac68e-177">值</span><span class="sxs-lookup"><span data-stu-id="ac68e-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ac68e-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac68e-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="ac68e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac68e-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="ac68e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac68e-180">System-Only</span></span>            | <span data-ttu-id="ac68e-181">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-181">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac68e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="ac68e-183">對</span><span class="sxs-lookup"><span data-stu-id="ac68e-183">True</span></span>                                                                   |
| <span data-ttu-id="ac68e-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac68e-184">Is Indexed</span></span>             | <span data-ttu-id="ac68e-185">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-185">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac68e-186">In Global Catalog</span></span>      | <span data-ttu-id="ac68e-187">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-187">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac68e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac68e-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac68e-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="ac68e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac68e-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="ac68e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac68e-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="ac68e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac68e-192">Search-Flags</span></span>           | <span data-ttu-id="ac68e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac68e-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="ac68e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac68e-194">System-Flags</span></span>           | <span data-ttu-id="ac68e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac68e-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="ac68e-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac68e-196">Classes used in</span></span>        | [<span data-ttu-id="ac68e-197">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="ac68e-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ac68e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac68e-198">Windows Server 2008</span></span>



| <span data-ttu-id="ac68e-199">進入</span><span class="sxs-lookup"><span data-stu-id="ac68e-199">Entry</span></span> | <span data-ttu-id="ac68e-200">值</span><span class="sxs-lookup"><span data-stu-id="ac68e-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ac68e-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac68e-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="ac68e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac68e-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="ac68e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac68e-203">System-Only</span></span>            | <span data-ttu-id="ac68e-204">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-204">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac68e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="ac68e-206">對</span><span class="sxs-lookup"><span data-stu-id="ac68e-206">True</span></span>                                                                   |
| <span data-ttu-id="ac68e-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac68e-207">Is Indexed</span></span>             | <span data-ttu-id="ac68e-208">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-208">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac68e-209">In Global Catalog</span></span>      | <span data-ttu-id="ac68e-210">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-210">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac68e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac68e-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac68e-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="ac68e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac68e-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="ac68e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac68e-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="ac68e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac68e-215">Search-Flags</span></span>           | <span data-ttu-id="ac68e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac68e-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="ac68e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac68e-217">System-Flags</span></span>           | <span data-ttu-id="ac68e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac68e-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="ac68e-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac68e-219">Classes used in</span></span>        | [<span data-ttu-id="ac68e-220">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="ac68e-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ac68e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ac68e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ac68e-222">進入</span><span class="sxs-lookup"><span data-stu-id="ac68e-222">Entry</span></span> | <span data-ttu-id="ac68e-223">值</span><span class="sxs-lookup"><span data-stu-id="ac68e-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ac68e-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac68e-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="ac68e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac68e-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="ac68e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac68e-226">System-Only</span></span>            | <span data-ttu-id="ac68e-227">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-227">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac68e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="ac68e-229">對</span><span class="sxs-lookup"><span data-stu-id="ac68e-229">True</span></span>                                                                   |
| <span data-ttu-id="ac68e-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac68e-230">Is Indexed</span></span>             | <span data-ttu-id="ac68e-231">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-231">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac68e-232">In Global Catalog</span></span>      | <span data-ttu-id="ac68e-233">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-233">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac68e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac68e-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac68e-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="ac68e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac68e-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="ac68e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac68e-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="ac68e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac68e-238">Search-Flags</span></span>           | <span data-ttu-id="ac68e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac68e-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="ac68e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac68e-240">System-Flags</span></span>           | <span data-ttu-id="ac68e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac68e-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="ac68e-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac68e-242">Classes used in</span></span>        | [<span data-ttu-id="ac68e-243">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="ac68e-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ac68e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac68e-244">Windows Server 2012</span></span>



| <span data-ttu-id="ac68e-245">進入</span><span class="sxs-lookup"><span data-stu-id="ac68e-245">Entry</span></span> | <span data-ttu-id="ac68e-246">值</span><span class="sxs-lookup"><span data-stu-id="ac68e-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ac68e-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ac68e-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="ac68e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ac68e-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="ac68e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="ac68e-249">System-Only</span></span>            | <span data-ttu-id="ac68e-250">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-250">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ac68e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="ac68e-252">對</span><span class="sxs-lookup"><span data-stu-id="ac68e-252">True</span></span>                                                                   |
| <span data-ttu-id="ac68e-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ac68e-253">Is Indexed</span></span>             | <span data-ttu-id="ac68e-254">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-254">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ac68e-255">In Global Catalog</span></span>      | <span data-ttu-id="ac68e-256">否</span><span class="sxs-lookup"><span data-stu-id="ac68e-256">False</span></span>                                                                  |
| <span data-ttu-id="ac68e-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ac68e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="ac68e-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ac68e-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="ac68e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ac68e-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="ac68e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ac68e-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="ac68e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ac68e-261">Search-Flags</span></span>           | <span data-ttu-id="ac68e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac68e-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="ac68e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ac68e-263">System-Flags</span></span>           | <span data-ttu-id="ac68e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ac68e-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="ac68e-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ac68e-265">Classes used in</span></span>        | [<span data-ttu-id="ac68e-266">**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="ac68e-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





