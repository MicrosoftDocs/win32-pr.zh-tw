---
title: 當地語系化-顯示識別碼屬性
description: 用來編制檔案 Extrts.mc 的索引，以取得物件的當地語系化 displayName 以進行 UI 用途。
ms.assetid: ed99d499-0064-4832-81ad-75fb3c8c548d
ms.tgt_platform: multiple
keywords:
- 當地語系化-顯示識別碼屬性 AD 架構
- localizationDisplayId 屬性 AD 架構
topic_type:
- apiref
api_name:
- Localization-Display-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4d9453b04bd5c944784b68ff5e4442f00bf65f5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687079"
---
# <a name="localization-display-id-attribute"></a><span data-ttu-id="32231-105">當地語系化-顯示識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="32231-105">Localization-Display-Id attribute</span></span>

<span data-ttu-id="32231-106">用來編制檔案 Extrts.mc 的索引，以取得物件的當地語系化 displayName 以進行 UI 用途。</span><span class="sxs-lookup"><span data-stu-id="32231-106">Used to index into the file Extrts.mc to get the localized displayName for the objects for UI purposes.</span></span>



| <span data-ttu-id="32231-107">進入</span><span class="sxs-lookup"><span data-stu-id="32231-107">Entry</span></span> | <span data-ttu-id="32231-108">值</span><span class="sxs-lookup"><span data-stu-id="32231-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="32231-109">CN</span><span class="sxs-lookup"><span data-stu-id="32231-109">CN</span></span>                | <span data-ttu-id="32231-110">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="32231-110">Localization-Display-Id</span></span>              |
| <span data-ttu-id="32231-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="32231-111">Ldap-Display-Name</span></span> | <span data-ttu-id="32231-112">localizationDisplayId</span><span class="sxs-lookup"><span data-stu-id="32231-112">localizationDisplayId</span></span>                |
| <span data-ttu-id="32231-113">大小</span><span class="sxs-lookup"><span data-stu-id="32231-113">Size</span></span>              | <span data-ttu-id="32231-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="32231-114">4 bytes</span></span>                              |
| <span data-ttu-id="32231-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="32231-115">Update Privilege</span></span>  | <span data-ttu-id="32231-116">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="32231-116">Schema administrator</span></span>                 |
| <span data-ttu-id="32231-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="32231-117">Update Frequency</span></span>  | <span data-ttu-id="32231-118">永遠不應變更識別碼。</span><span class="sxs-lookup"><span data-stu-id="32231-118">An ID should never be changed.</span></span>       |
| <span data-ttu-id="32231-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="32231-119">Attribute-Id</span></span>      | <span data-ttu-id="32231-120">1.2.840.113556.1.4.1353</span><span class="sxs-lookup"><span data-stu-id="32231-120">1.2.840.113556.1.4.1353</span></span>              |
| <span data-ttu-id="32231-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="32231-121">System-Id-Guid</span></span>    | <span data-ttu-id="32231-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="32231-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span></span> |
| <span data-ttu-id="32231-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="32231-123">Syntax</span></span>            | [<span data-ttu-id="32231-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="32231-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="32231-125">實作</span><span class="sxs-lookup"><span data-stu-id="32231-125">Implementations</span></span>

-   [<span data-ttu-id="32231-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="32231-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="32231-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="32231-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="32231-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="32231-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="32231-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="32231-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="32231-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="32231-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="32231-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="32231-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="32231-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="32231-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="32231-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32231-133">Windows 2000 Server</span></span>



| <span data-ttu-id="32231-134">進入</span><span class="sxs-lookup"><span data-stu-id="32231-134">Entry</span></span> | <span data-ttu-id="32231-135">值</span><span class="sxs-lookup"><span data-stu-id="32231-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="32231-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32231-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32231-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="32231-138">System-Only</span></span>            | <span data-ttu-id="32231-139">否</span><span class="sxs-lookup"><span data-stu-id="32231-139">False</span></span>                                                           |
| <span data-ttu-id="32231-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32231-140">Is-Single-Valued</span></span>       | <span data-ttu-id="32231-141">對</span><span class="sxs-lookup"><span data-stu-id="32231-141">True</span></span>                                                            |
| <span data-ttu-id="32231-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32231-142">Is Indexed</span></span>             | <span data-ttu-id="32231-143">否</span><span class="sxs-lookup"><span data-stu-id="32231-143">False</span></span>                                                           |
| <span data-ttu-id="32231-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32231-144">In Global Catalog</span></span>      | <span data-ttu-id="32231-145">否</span><span class="sxs-lookup"><span data-stu-id="32231-145">False</span></span>                                                           |
| <span data-ttu-id="32231-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32231-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="32231-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32231-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="32231-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32231-148">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="32231-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32231-149">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="32231-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-150">Search-Flags</span></span>           | <span data-ttu-id="32231-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32231-151">0x00000000</span></span>                                                      |
| <span data-ttu-id="32231-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-152">System-Flags</span></span>           | <span data-ttu-id="32231-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32231-153">0x00000010</span></span>                                                      |
| <span data-ttu-id="32231-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32231-154">Classes used in</span></span>        | [<span data-ttu-id="32231-155">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="32231-155">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="32231-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="32231-156">Windows Server 2003</span></span>



| <span data-ttu-id="32231-157">進入</span><span class="sxs-lookup"><span data-stu-id="32231-157">Entry</span></span> | <span data-ttu-id="32231-158">值</span><span class="sxs-lookup"><span data-stu-id="32231-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="32231-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32231-159">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32231-160">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="32231-161">System-Only</span></span>            | <span data-ttu-id="32231-162">否</span><span class="sxs-lookup"><span data-stu-id="32231-162">False</span></span>                                                           |
| <span data-ttu-id="32231-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32231-163">Is-Single-Valued</span></span>       | <span data-ttu-id="32231-164">對</span><span class="sxs-lookup"><span data-stu-id="32231-164">True</span></span>                                                            |
| <span data-ttu-id="32231-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32231-165">Is Indexed</span></span>             | <span data-ttu-id="32231-166">否</span><span class="sxs-lookup"><span data-stu-id="32231-166">False</span></span>                                                           |
| <span data-ttu-id="32231-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32231-167">In Global Catalog</span></span>      | <span data-ttu-id="32231-168">否</span><span class="sxs-lookup"><span data-stu-id="32231-168">False</span></span>                                                           |
| <span data-ttu-id="32231-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32231-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="32231-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32231-170">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="32231-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32231-171">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="32231-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32231-172">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="32231-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-173">Search-Flags</span></span>           | <span data-ttu-id="32231-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32231-174">0x00000000</span></span>                                                      |
| <span data-ttu-id="32231-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-175">System-Flags</span></span>           | <span data-ttu-id="32231-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32231-176">0x00000010</span></span>                                                      |
| <span data-ttu-id="32231-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32231-177">Classes used in</span></span>        | [<span data-ttu-id="32231-178">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="32231-178">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="32231-179">亞當</span><span class="sxs-lookup"><span data-stu-id="32231-179">ADAM</span></span>



| <span data-ttu-id="32231-180">進入</span><span class="sxs-lookup"><span data-stu-id="32231-180">Entry</span></span> | <span data-ttu-id="32231-181">值</span><span class="sxs-lookup"><span data-stu-id="32231-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="32231-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32231-182">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32231-183">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="32231-184">System-Only</span></span>            | <span data-ttu-id="32231-185">否</span><span class="sxs-lookup"><span data-stu-id="32231-185">False</span></span>                                                           |
| <span data-ttu-id="32231-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32231-186">Is-Single-Valued</span></span>       | <span data-ttu-id="32231-187">對</span><span class="sxs-lookup"><span data-stu-id="32231-187">True</span></span>                                                            |
| <span data-ttu-id="32231-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32231-188">Is Indexed</span></span>             | <span data-ttu-id="32231-189">否</span><span class="sxs-lookup"><span data-stu-id="32231-189">False</span></span>                                                           |
| <span data-ttu-id="32231-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32231-190">In Global Catalog</span></span>      | <span data-ttu-id="32231-191">否</span><span class="sxs-lookup"><span data-stu-id="32231-191">False</span></span>                                                           |
| <span data-ttu-id="32231-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32231-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="32231-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32231-193">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="32231-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32231-194">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="32231-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32231-195">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="32231-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-196">Search-Flags</span></span>           | <span data-ttu-id="32231-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32231-197">0x00000000</span></span>                                                      |
| <span data-ttu-id="32231-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-198">System-Flags</span></span>           | <span data-ttu-id="32231-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32231-199">0x00000010</span></span>                                                      |
| <span data-ttu-id="32231-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32231-200">Classes used in</span></span>        | [<span data-ttu-id="32231-201">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="32231-201">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="32231-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="32231-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="32231-203">進入</span><span class="sxs-lookup"><span data-stu-id="32231-203">Entry</span></span> | <span data-ttu-id="32231-204">值</span><span class="sxs-lookup"><span data-stu-id="32231-204">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="32231-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32231-205">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32231-206">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="32231-207">System-Only</span></span>            | <span data-ttu-id="32231-208">否</span><span class="sxs-lookup"><span data-stu-id="32231-208">False</span></span>                                                           |
| <span data-ttu-id="32231-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32231-209">Is-Single-Valued</span></span>       | <span data-ttu-id="32231-210">對</span><span class="sxs-lookup"><span data-stu-id="32231-210">True</span></span>                                                            |
| <span data-ttu-id="32231-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32231-211">Is Indexed</span></span>             | <span data-ttu-id="32231-212">否</span><span class="sxs-lookup"><span data-stu-id="32231-212">False</span></span>                                                           |
| <span data-ttu-id="32231-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32231-213">In Global Catalog</span></span>      | <span data-ttu-id="32231-214">否</span><span class="sxs-lookup"><span data-stu-id="32231-214">False</span></span>                                                           |
| <span data-ttu-id="32231-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32231-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="32231-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32231-216">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="32231-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32231-217">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="32231-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32231-218">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="32231-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-219">Search-Flags</span></span>           | <span data-ttu-id="32231-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32231-220">0x00000000</span></span>                                                      |
| <span data-ttu-id="32231-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-221">System-Flags</span></span>           | <span data-ttu-id="32231-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32231-222">0x00000010</span></span>                                                      |
| <span data-ttu-id="32231-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32231-223">Classes used in</span></span>        | [<span data-ttu-id="32231-224">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="32231-224">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="32231-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32231-225">Windows Server 2008</span></span>



| <span data-ttu-id="32231-226">進入</span><span class="sxs-lookup"><span data-stu-id="32231-226">Entry</span></span> | <span data-ttu-id="32231-227">值</span><span class="sxs-lookup"><span data-stu-id="32231-227">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="32231-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32231-228">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32231-229">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="32231-230">System-Only</span></span>            | <span data-ttu-id="32231-231">否</span><span class="sxs-lookup"><span data-stu-id="32231-231">False</span></span>                                                           |
| <span data-ttu-id="32231-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32231-232">Is-Single-Valued</span></span>       | <span data-ttu-id="32231-233">對</span><span class="sxs-lookup"><span data-stu-id="32231-233">True</span></span>                                                            |
| <span data-ttu-id="32231-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32231-234">Is Indexed</span></span>             | <span data-ttu-id="32231-235">否</span><span class="sxs-lookup"><span data-stu-id="32231-235">False</span></span>                                                           |
| <span data-ttu-id="32231-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32231-236">In Global Catalog</span></span>      | <span data-ttu-id="32231-237">否</span><span class="sxs-lookup"><span data-stu-id="32231-237">False</span></span>                                                           |
| <span data-ttu-id="32231-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32231-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="32231-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32231-239">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="32231-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32231-240">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="32231-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32231-241">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="32231-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-242">Search-Flags</span></span>           | <span data-ttu-id="32231-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32231-243">0x00000000</span></span>                                                      |
| <span data-ttu-id="32231-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-244">System-Flags</span></span>           | <span data-ttu-id="32231-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32231-245">0x00000010</span></span>                                                      |
| <span data-ttu-id="32231-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32231-246">Classes used in</span></span>        | [<span data-ttu-id="32231-247">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="32231-247">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="32231-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32231-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="32231-249">進入</span><span class="sxs-lookup"><span data-stu-id="32231-249">Entry</span></span> | <span data-ttu-id="32231-250">值</span><span class="sxs-lookup"><span data-stu-id="32231-250">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="32231-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32231-251">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32231-252">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="32231-253">System-Only</span></span>            | <span data-ttu-id="32231-254">否</span><span class="sxs-lookup"><span data-stu-id="32231-254">False</span></span>                                                           |
| <span data-ttu-id="32231-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32231-255">Is-Single-Valued</span></span>       | <span data-ttu-id="32231-256">對</span><span class="sxs-lookup"><span data-stu-id="32231-256">True</span></span>                                                            |
| <span data-ttu-id="32231-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32231-257">Is Indexed</span></span>             | <span data-ttu-id="32231-258">否</span><span class="sxs-lookup"><span data-stu-id="32231-258">False</span></span>                                                           |
| <span data-ttu-id="32231-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32231-259">In Global Catalog</span></span>      | <span data-ttu-id="32231-260">否</span><span class="sxs-lookup"><span data-stu-id="32231-260">False</span></span>                                                           |
| <span data-ttu-id="32231-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32231-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="32231-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32231-262">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="32231-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32231-263">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="32231-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32231-264">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="32231-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-265">Search-Flags</span></span>           | <span data-ttu-id="32231-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32231-266">0x00000000</span></span>                                                      |
| <span data-ttu-id="32231-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-267">System-Flags</span></span>           | <span data-ttu-id="32231-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32231-268">0x00000010</span></span>                                                      |
| <span data-ttu-id="32231-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32231-269">Classes used in</span></span>        | [<span data-ttu-id="32231-270">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="32231-270">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="32231-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="32231-271">Windows Server 2012</span></span>



| <span data-ttu-id="32231-272">進入</span><span class="sxs-lookup"><span data-stu-id="32231-272">Entry</span></span> | <span data-ttu-id="32231-273">值</span><span class="sxs-lookup"><span data-stu-id="32231-273">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="32231-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="32231-274">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="32231-275">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="32231-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="32231-276">System-Only</span></span>            | <span data-ttu-id="32231-277">否</span><span class="sxs-lookup"><span data-stu-id="32231-277">False</span></span>                                                           |
| <span data-ttu-id="32231-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="32231-278">Is-Single-Valued</span></span>       | <span data-ttu-id="32231-279">對</span><span class="sxs-lookup"><span data-stu-id="32231-279">True</span></span>                                                            |
| <span data-ttu-id="32231-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="32231-280">Is Indexed</span></span>             | <span data-ttu-id="32231-281">否</span><span class="sxs-lookup"><span data-stu-id="32231-281">False</span></span>                                                           |
| <span data-ttu-id="32231-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="32231-282">In Global Catalog</span></span>      | <span data-ttu-id="32231-283">否</span><span class="sxs-lookup"><span data-stu-id="32231-283">False</span></span>                                                           |
| <span data-ttu-id="32231-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="32231-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="32231-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="32231-285">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="32231-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="32231-286">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="32231-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="32231-287">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="32231-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-288">Search-Flags</span></span>           | <span data-ttu-id="32231-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32231-289">0x00000000</span></span>                                                      |
| <span data-ttu-id="32231-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="32231-290">System-Flags</span></span>           | <span data-ttu-id="32231-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="32231-291">0x00000010</span></span>                                                      |
| <span data-ttu-id="32231-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="32231-292">Classes used in</span></span>        | [<span data-ttu-id="32231-293">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="32231-293">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





