---
title: ms ds-架構延伸模組屬性
description: 用來將延伸模組的相關資訊儲存至架構物件的二進位 BLOB。
ms.assetid: a2ffc4c6-ec33-4265-9a1e-c07597d2af50
ms.tgt_platform: multiple
keywords:
- ms ds-架構-延伸模組屬性 AD 架構
- 架構延伸模組屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-ds-Schema-Extensions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f524e28f2d45d03f7851fc46d32e986968f81bfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467348"
---
# <a name="ms-ds-schema-extensions-attribute"></a><span data-ttu-id="173fd-105">ms ds-架構延伸模組屬性</span><span class="sxs-lookup"><span data-stu-id="173fd-105">ms-ds-Schema-Extensions attribute</span></span>

<span data-ttu-id="173fd-106">用來將延伸模組的相關資訊儲存至架構物件的二進位 BLOB。</span><span class="sxs-lookup"><span data-stu-id="173fd-106">A binary BLOB used to store information about extensions to schema objects.</span></span>



| <span data-ttu-id="173fd-107">進入</span><span class="sxs-lookup"><span data-stu-id="173fd-107">Entry</span></span> | <span data-ttu-id="173fd-108">值</span><span class="sxs-lookup"><span data-stu-id="173fd-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="173fd-109">CN</span><span class="sxs-lookup"><span data-stu-id="173fd-109">CN</span></span>                | <span data-ttu-id="173fd-110">ms ds-架構-擴充功能</span><span class="sxs-lookup"><span data-stu-id="173fd-110">ms-ds-Schema-Extensions</span></span>                               |
| <span data-ttu-id="173fd-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="173fd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="173fd-112">架構延伸模組</span><span class="sxs-lookup"><span data-stu-id="173fd-112">msDs-Schema-Extensions</span></span>                                |
| <span data-ttu-id="173fd-113">大小</span><span class="sxs-lookup"><span data-stu-id="173fd-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="173fd-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="173fd-114">Update Privilege</span></span>  | <span data-ttu-id="173fd-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="173fd-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="173fd-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="173fd-116">Update Frequency</span></span>  | <span data-ttu-id="173fd-117">延伸架構時。</span><span class="sxs-lookup"><span data-stu-id="173fd-117">When the schema is extended.</span></span>                          |
| <span data-ttu-id="173fd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="173fd-118">Attribute-Id</span></span>      | <span data-ttu-id="173fd-119">1.2.840.113556.1.4.1440</span><span class="sxs-lookup"><span data-stu-id="173fd-119">1.2.840.113556.1.4.1440</span></span>                               |
| <span data-ttu-id="173fd-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="173fd-120">System-Id-Guid</span></span>    | <span data-ttu-id="173fd-121">b39a61be-ed07-4cab-9a4a-4963ed0141e1</span><span class="sxs-lookup"><span data-stu-id="173fd-121">b39a61be-ed07-4cab-9a4a-4963ed0141e1</span></span>                  |
| <span data-ttu-id="173fd-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="173fd-122">Syntax</span></span>            | [<span data-ttu-id="173fd-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="173fd-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="173fd-124">實作</span><span class="sxs-lookup"><span data-stu-id="173fd-124">Implementations</span></span>

-   [<span data-ttu-id="173fd-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="173fd-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="173fd-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="173fd-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="173fd-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="173fd-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="173fd-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="173fd-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="173fd-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="173fd-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="173fd-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="173fd-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="173fd-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="173fd-131">Windows Server 2003</span></span>



| <span data-ttu-id="173fd-132">進入</span><span class="sxs-lookup"><span data-stu-id="173fd-132">Entry</span></span> | <span data-ttu-id="173fd-133">值</span><span class="sxs-lookup"><span data-stu-id="173fd-133">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="173fd-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="173fd-134">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="173fd-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="173fd-135">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="173fd-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="173fd-136">System-Only</span></span>            | <span data-ttu-id="173fd-137">對</span><span class="sxs-lookup"><span data-stu-id="173fd-137">True</span></span>                                                                                                                                      |
| <span data-ttu-id="173fd-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="173fd-138">Is-Single-Valued</span></span>       | <span data-ttu-id="173fd-139">否</span><span class="sxs-lookup"><span data-stu-id="173fd-139">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="173fd-140">Is Indexed</span></span>             | <span data-ttu-id="173fd-141">否</span><span class="sxs-lookup"><span data-stu-id="173fd-141">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="173fd-142">In Global Catalog</span></span>      | <span data-ttu-id="173fd-143">否</span><span class="sxs-lookup"><span data-stu-id="173fd-143">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="173fd-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="173fd-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="173fd-145">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="173fd-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="173fd-146">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="173fd-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="173fd-147">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="173fd-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="173fd-148">Search-Flags</span></span>           | <span data-ttu-id="173fd-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="173fd-149">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="173fd-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="173fd-150">System-Flags</span></span>           | <span data-ttu-id="173fd-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="173fd-151">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="173fd-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="173fd-152">Classes used in</span></span>        | [<span data-ttu-id="173fd-153">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="173fd-153">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="173fd-154">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="173fd-154">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="173fd-155">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="173fd-155">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="173fd-156">亞當</span><span class="sxs-lookup"><span data-stu-id="173fd-156">ADAM</span></span>



| <span data-ttu-id="173fd-157">進入</span><span class="sxs-lookup"><span data-stu-id="173fd-157">Entry</span></span> | <span data-ttu-id="173fd-158">值</span><span class="sxs-lookup"><span data-stu-id="173fd-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="173fd-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="173fd-159">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="173fd-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="173fd-160">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="173fd-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="173fd-161">System-Only</span></span>            | <span data-ttu-id="173fd-162">對</span><span class="sxs-lookup"><span data-stu-id="173fd-162">True</span></span>                                                                                                                                      |
| <span data-ttu-id="173fd-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="173fd-163">Is-Single-Valued</span></span>       | <span data-ttu-id="173fd-164">否</span><span class="sxs-lookup"><span data-stu-id="173fd-164">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="173fd-165">Is Indexed</span></span>             | <span data-ttu-id="173fd-166">否</span><span class="sxs-lookup"><span data-stu-id="173fd-166">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="173fd-167">In Global Catalog</span></span>      | <span data-ttu-id="173fd-168">否</span><span class="sxs-lookup"><span data-stu-id="173fd-168">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="173fd-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="173fd-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="173fd-170">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="173fd-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="173fd-171">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="173fd-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="173fd-172">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="173fd-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="173fd-173">Search-Flags</span></span>           | <span data-ttu-id="173fd-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="173fd-174">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="173fd-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="173fd-175">System-Flags</span></span>           | <span data-ttu-id="173fd-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="173fd-176">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="173fd-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="173fd-177">Classes used in</span></span>        | [<span data-ttu-id="173fd-178">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="173fd-178">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="173fd-179">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="173fd-179">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="173fd-180">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="173fd-180">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="173fd-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="173fd-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="173fd-182">進入</span><span class="sxs-lookup"><span data-stu-id="173fd-182">Entry</span></span> | <span data-ttu-id="173fd-183">值</span><span class="sxs-lookup"><span data-stu-id="173fd-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="173fd-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="173fd-184">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="173fd-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="173fd-185">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="173fd-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="173fd-186">System-Only</span></span>            | <span data-ttu-id="173fd-187">對</span><span class="sxs-lookup"><span data-stu-id="173fd-187">True</span></span>                                                                                                                                      |
| <span data-ttu-id="173fd-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="173fd-188">Is-Single-Valued</span></span>       | <span data-ttu-id="173fd-189">否</span><span class="sxs-lookup"><span data-stu-id="173fd-189">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="173fd-190">Is Indexed</span></span>             | <span data-ttu-id="173fd-191">否</span><span class="sxs-lookup"><span data-stu-id="173fd-191">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="173fd-192">In Global Catalog</span></span>      | <span data-ttu-id="173fd-193">否</span><span class="sxs-lookup"><span data-stu-id="173fd-193">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="173fd-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="173fd-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="173fd-195">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="173fd-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="173fd-196">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="173fd-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="173fd-197">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="173fd-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="173fd-198">Search-Flags</span></span>           | <span data-ttu-id="173fd-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="173fd-199">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="173fd-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="173fd-200">System-Flags</span></span>           | <span data-ttu-id="173fd-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="173fd-201">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="173fd-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="173fd-202">Classes used in</span></span>        | [<span data-ttu-id="173fd-203">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="173fd-203">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="173fd-204">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="173fd-204">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="173fd-205">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="173fd-205">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="173fd-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="173fd-206">Windows Server 2008</span></span>



| <span data-ttu-id="173fd-207">進入</span><span class="sxs-lookup"><span data-stu-id="173fd-207">Entry</span></span> | <span data-ttu-id="173fd-208">值</span><span class="sxs-lookup"><span data-stu-id="173fd-208">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="173fd-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="173fd-209">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="173fd-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="173fd-210">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="173fd-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="173fd-211">System-Only</span></span>            | <span data-ttu-id="173fd-212">對</span><span class="sxs-lookup"><span data-stu-id="173fd-212">True</span></span>                                                                                                                                      |
| <span data-ttu-id="173fd-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="173fd-213">Is-Single-Valued</span></span>       | <span data-ttu-id="173fd-214">否</span><span class="sxs-lookup"><span data-stu-id="173fd-214">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="173fd-215">Is Indexed</span></span>             | <span data-ttu-id="173fd-216">否</span><span class="sxs-lookup"><span data-stu-id="173fd-216">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="173fd-217">In Global Catalog</span></span>      | <span data-ttu-id="173fd-218">否</span><span class="sxs-lookup"><span data-stu-id="173fd-218">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="173fd-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="173fd-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="173fd-220">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="173fd-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="173fd-221">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="173fd-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="173fd-222">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="173fd-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="173fd-223">Search-Flags</span></span>           | <span data-ttu-id="173fd-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="173fd-224">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="173fd-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="173fd-225">System-Flags</span></span>           | <span data-ttu-id="173fd-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="173fd-226">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="173fd-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="173fd-227">Classes used in</span></span>        | [<span data-ttu-id="173fd-228">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="173fd-228">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="173fd-229">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="173fd-229">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="173fd-230">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="173fd-230">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="173fd-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="173fd-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="173fd-232">進入</span><span class="sxs-lookup"><span data-stu-id="173fd-232">Entry</span></span> | <span data-ttu-id="173fd-233">值</span><span class="sxs-lookup"><span data-stu-id="173fd-233">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="173fd-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="173fd-234">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="173fd-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="173fd-235">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="173fd-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="173fd-236">System-Only</span></span>            | <span data-ttu-id="173fd-237">對</span><span class="sxs-lookup"><span data-stu-id="173fd-237">True</span></span>                                                                                                                                      |
| <span data-ttu-id="173fd-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="173fd-238">Is-Single-Valued</span></span>       | <span data-ttu-id="173fd-239">否</span><span class="sxs-lookup"><span data-stu-id="173fd-239">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="173fd-240">Is Indexed</span></span>             | <span data-ttu-id="173fd-241">否</span><span class="sxs-lookup"><span data-stu-id="173fd-241">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="173fd-242">In Global Catalog</span></span>      | <span data-ttu-id="173fd-243">否</span><span class="sxs-lookup"><span data-stu-id="173fd-243">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="173fd-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="173fd-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="173fd-245">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="173fd-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="173fd-246">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="173fd-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="173fd-247">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="173fd-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="173fd-248">Search-Flags</span></span>           | <span data-ttu-id="173fd-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="173fd-249">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="173fd-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="173fd-250">System-Flags</span></span>           | <span data-ttu-id="173fd-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="173fd-251">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="173fd-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="173fd-252">Classes used in</span></span>        | [<span data-ttu-id="173fd-253">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="173fd-253">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="173fd-254">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="173fd-254">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="173fd-255">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="173fd-255">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="173fd-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="173fd-256">Windows Server 2012</span></span>



| <span data-ttu-id="173fd-257">進入</span><span class="sxs-lookup"><span data-stu-id="173fd-257">Entry</span></span> | <span data-ttu-id="173fd-258">值</span><span class="sxs-lookup"><span data-stu-id="173fd-258">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="173fd-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="173fd-259">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="173fd-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="173fd-260">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="173fd-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="173fd-261">System-Only</span></span>            | <span data-ttu-id="173fd-262">對</span><span class="sxs-lookup"><span data-stu-id="173fd-262">True</span></span>                                                                                                                                      |
| <span data-ttu-id="173fd-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="173fd-263">Is-Single-Valued</span></span>       | <span data-ttu-id="173fd-264">否</span><span class="sxs-lookup"><span data-stu-id="173fd-264">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="173fd-265">Is Indexed</span></span>             | <span data-ttu-id="173fd-266">否</span><span class="sxs-lookup"><span data-stu-id="173fd-266">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="173fd-267">In Global Catalog</span></span>      | <span data-ttu-id="173fd-268">否</span><span class="sxs-lookup"><span data-stu-id="173fd-268">False</span></span>                                                                                                                                     |
| <span data-ttu-id="173fd-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="173fd-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="173fd-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="173fd-270">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="173fd-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="173fd-271">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="173fd-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="173fd-272">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="173fd-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="173fd-273">Search-Flags</span></span>           | <span data-ttu-id="173fd-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="173fd-274">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="173fd-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="173fd-275">System-Flags</span></span>           | <span data-ttu-id="173fd-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="173fd-276">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="173fd-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="173fd-277">Classes used in</span></span>        | [<span data-ttu-id="173fd-278">**屬性-架構**</span><span class="sxs-lookup"><span data-stu-id="173fd-278">**Attribute-Schema**</span></span>](c-attributeschema.md)<br/> [<span data-ttu-id="173fd-279">**類別架構**</span><span class="sxs-lookup"><span data-stu-id="173fd-279">**Class-Schema**</span></span>](c-classschema.md)<br/> [<span data-ttu-id="173fd-280">**Dmd**</span><span class="sxs-lookup"><span data-stu-id="173fd-280">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





