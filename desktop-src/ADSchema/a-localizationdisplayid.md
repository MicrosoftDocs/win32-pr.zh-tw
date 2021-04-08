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
# <a name="localization-display-id-attribute"></a><span data-ttu-id="012fa-105">當地語系化-顯示識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="012fa-105">Localization-Display-Id attribute</span></span>

<span data-ttu-id="012fa-106">用來編制檔案 Extrts.mc 的索引，以取得物件的當地語系化 displayName 以進行 UI 用途。</span><span class="sxs-lookup"><span data-stu-id="012fa-106">Used to index into the file Extrts.mc to get the localized displayName for the objects for UI purposes.</span></span>



| <span data-ttu-id="012fa-107">進入</span><span class="sxs-lookup"><span data-stu-id="012fa-107">Entry</span></span> | <span data-ttu-id="012fa-108">值</span><span class="sxs-lookup"><span data-stu-id="012fa-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="012fa-109">CN</span><span class="sxs-lookup"><span data-stu-id="012fa-109">CN</span></span>                | <span data-ttu-id="012fa-110">當地語系化-顯示識別碼</span><span class="sxs-lookup"><span data-stu-id="012fa-110">Localization-Display-Id</span></span>              |
| <span data-ttu-id="012fa-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="012fa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="012fa-112">localizationDisplayId</span><span class="sxs-lookup"><span data-stu-id="012fa-112">localizationDisplayId</span></span>                |
| <span data-ttu-id="012fa-113">大小</span><span class="sxs-lookup"><span data-stu-id="012fa-113">Size</span></span>              | <span data-ttu-id="012fa-114">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="012fa-114">4 bytes</span></span>                              |
| <span data-ttu-id="012fa-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="012fa-115">Update Privilege</span></span>  | <span data-ttu-id="012fa-116">架構系統管理員</span><span class="sxs-lookup"><span data-stu-id="012fa-116">Schema administrator</span></span>                 |
| <span data-ttu-id="012fa-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="012fa-117">Update Frequency</span></span>  | <span data-ttu-id="012fa-118">永遠不應變更識別碼。</span><span class="sxs-lookup"><span data-stu-id="012fa-118">An ID should never be changed.</span></span>       |
| <span data-ttu-id="012fa-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="012fa-119">Attribute-Id</span></span>      | <span data-ttu-id="012fa-120">1.2.840.113556.1.4.1353</span><span class="sxs-lookup"><span data-stu-id="012fa-120">1.2.840.113556.1.4.1353</span></span>              |
| <span data-ttu-id="012fa-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="012fa-121">System-Id-Guid</span></span>    | <span data-ttu-id="012fa-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="012fa-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span></span> |
| <span data-ttu-id="012fa-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="012fa-123">Syntax</span></span>            | [<span data-ttu-id="012fa-124">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="012fa-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="012fa-125">實作</span><span class="sxs-lookup"><span data-stu-id="012fa-125">Implementations</span></span>

-   [<span data-ttu-id="012fa-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="012fa-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="012fa-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="012fa-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="012fa-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="012fa-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="012fa-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="012fa-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="012fa-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="012fa-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="012fa-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="012fa-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="012fa-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="012fa-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="012fa-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="012fa-133">Windows 2000 Server</span></span>



| <span data-ttu-id="012fa-134">進入</span><span class="sxs-lookup"><span data-stu-id="012fa-134">Entry</span></span> | <span data-ttu-id="012fa-135">值</span><span class="sxs-lookup"><span data-stu-id="012fa-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="012fa-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="012fa-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="012fa-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="012fa-138">System-Only</span></span>            | <span data-ttu-id="012fa-139">否</span><span class="sxs-lookup"><span data-stu-id="012fa-139">False</span></span>                                                           |
| <span data-ttu-id="012fa-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="012fa-140">Is-Single-Valued</span></span>       | <span data-ttu-id="012fa-141">對</span><span class="sxs-lookup"><span data-stu-id="012fa-141">True</span></span>                                                            |
| <span data-ttu-id="012fa-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="012fa-142">Is Indexed</span></span>             | <span data-ttu-id="012fa-143">否</span><span class="sxs-lookup"><span data-stu-id="012fa-143">False</span></span>                                                           |
| <span data-ttu-id="012fa-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="012fa-144">In Global Catalog</span></span>      | <span data-ttu-id="012fa-145">否</span><span class="sxs-lookup"><span data-stu-id="012fa-145">False</span></span>                                                           |
| <span data-ttu-id="012fa-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="012fa-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="012fa-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="012fa-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="012fa-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="012fa-148">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="012fa-149">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-150">Search-Flags</span></span>           | <span data-ttu-id="012fa-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="012fa-151">0x00000000</span></span>                                                      |
| <span data-ttu-id="012fa-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-152">System-Flags</span></span>           | <span data-ttu-id="012fa-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="012fa-153">0x00000010</span></span>                                                      |
| <span data-ttu-id="012fa-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="012fa-154">Classes used in</span></span>        | [<span data-ttu-id="012fa-155">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="012fa-155">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="012fa-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="012fa-156">Windows Server 2003</span></span>



| <span data-ttu-id="012fa-157">進入</span><span class="sxs-lookup"><span data-stu-id="012fa-157">Entry</span></span> | <span data-ttu-id="012fa-158">值</span><span class="sxs-lookup"><span data-stu-id="012fa-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="012fa-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="012fa-159">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="012fa-160">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="012fa-161">System-Only</span></span>            | <span data-ttu-id="012fa-162">否</span><span class="sxs-lookup"><span data-stu-id="012fa-162">False</span></span>                                                           |
| <span data-ttu-id="012fa-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="012fa-163">Is-Single-Valued</span></span>       | <span data-ttu-id="012fa-164">對</span><span class="sxs-lookup"><span data-stu-id="012fa-164">True</span></span>                                                            |
| <span data-ttu-id="012fa-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="012fa-165">Is Indexed</span></span>             | <span data-ttu-id="012fa-166">否</span><span class="sxs-lookup"><span data-stu-id="012fa-166">False</span></span>                                                           |
| <span data-ttu-id="012fa-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="012fa-167">In Global Catalog</span></span>      | <span data-ttu-id="012fa-168">否</span><span class="sxs-lookup"><span data-stu-id="012fa-168">False</span></span>                                                           |
| <span data-ttu-id="012fa-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="012fa-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="012fa-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="012fa-170">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="012fa-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="012fa-171">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="012fa-172">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-173">Search-Flags</span></span>           | <span data-ttu-id="012fa-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="012fa-174">0x00000000</span></span>                                                      |
| <span data-ttu-id="012fa-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-175">System-Flags</span></span>           | <span data-ttu-id="012fa-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="012fa-176">0x00000010</span></span>                                                      |
| <span data-ttu-id="012fa-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="012fa-177">Classes used in</span></span>        | [<span data-ttu-id="012fa-178">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="012fa-178">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="012fa-179">亞當</span><span class="sxs-lookup"><span data-stu-id="012fa-179">ADAM</span></span>



| <span data-ttu-id="012fa-180">進入</span><span class="sxs-lookup"><span data-stu-id="012fa-180">Entry</span></span> | <span data-ttu-id="012fa-181">值</span><span class="sxs-lookup"><span data-stu-id="012fa-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="012fa-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="012fa-182">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="012fa-183">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="012fa-184">System-Only</span></span>            | <span data-ttu-id="012fa-185">否</span><span class="sxs-lookup"><span data-stu-id="012fa-185">False</span></span>                                                           |
| <span data-ttu-id="012fa-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="012fa-186">Is-Single-Valued</span></span>       | <span data-ttu-id="012fa-187">對</span><span class="sxs-lookup"><span data-stu-id="012fa-187">True</span></span>                                                            |
| <span data-ttu-id="012fa-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="012fa-188">Is Indexed</span></span>             | <span data-ttu-id="012fa-189">否</span><span class="sxs-lookup"><span data-stu-id="012fa-189">False</span></span>                                                           |
| <span data-ttu-id="012fa-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="012fa-190">In Global Catalog</span></span>      | <span data-ttu-id="012fa-191">否</span><span class="sxs-lookup"><span data-stu-id="012fa-191">False</span></span>                                                           |
| <span data-ttu-id="012fa-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="012fa-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="012fa-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="012fa-193">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="012fa-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="012fa-194">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="012fa-195">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-196">Search-Flags</span></span>           | <span data-ttu-id="012fa-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="012fa-197">0x00000000</span></span>                                                      |
| <span data-ttu-id="012fa-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-198">System-Flags</span></span>           | <span data-ttu-id="012fa-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="012fa-199">0x00000010</span></span>                                                      |
| <span data-ttu-id="012fa-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="012fa-200">Classes used in</span></span>        | [<span data-ttu-id="012fa-201">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="012fa-201">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="012fa-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="012fa-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="012fa-203">進入</span><span class="sxs-lookup"><span data-stu-id="012fa-203">Entry</span></span> | <span data-ttu-id="012fa-204">值</span><span class="sxs-lookup"><span data-stu-id="012fa-204">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="012fa-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="012fa-205">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="012fa-206">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="012fa-207">System-Only</span></span>            | <span data-ttu-id="012fa-208">否</span><span class="sxs-lookup"><span data-stu-id="012fa-208">False</span></span>                                                           |
| <span data-ttu-id="012fa-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="012fa-209">Is-Single-Valued</span></span>       | <span data-ttu-id="012fa-210">對</span><span class="sxs-lookup"><span data-stu-id="012fa-210">True</span></span>                                                            |
| <span data-ttu-id="012fa-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="012fa-211">Is Indexed</span></span>             | <span data-ttu-id="012fa-212">否</span><span class="sxs-lookup"><span data-stu-id="012fa-212">False</span></span>                                                           |
| <span data-ttu-id="012fa-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="012fa-213">In Global Catalog</span></span>      | <span data-ttu-id="012fa-214">否</span><span class="sxs-lookup"><span data-stu-id="012fa-214">False</span></span>                                                           |
| <span data-ttu-id="012fa-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="012fa-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="012fa-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="012fa-216">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="012fa-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="012fa-217">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="012fa-218">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-219">Search-Flags</span></span>           | <span data-ttu-id="012fa-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="012fa-220">0x00000000</span></span>                                                      |
| <span data-ttu-id="012fa-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-221">System-Flags</span></span>           | <span data-ttu-id="012fa-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="012fa-222">0x00000010</span></span>                                                      |
| <span data-ttu-id="012fa-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="012fa-223">Classes used in</span></span>        | [<span data-ttu-id="012fa-224">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="012fa-224">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="012fa-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="012fa-225">Windows Server 2008</span></span>



| <span data-ttu-id="012fa-226">進入</span><span class="sxs-lookup"><span data-stu-id="012fa-226">Entry</span></span> | <span data-ttu-id="012fa-227">值</span><span class="sxs-lookup"><span data-stu-id="012fa-227">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="012fa-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="012fa-228">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="012fa-229">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="012fa-230">System-Only</span></span>            | <span data-ttu-id="012fa-231">否</span><span class="sxs-lookup"><span data-stu-id="012fa-231">False</span></span>                                                           |
| <span data-ttu-id="012fa-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="012fa-232">Is-Single-Valued</span></span>       | <span data-ttu-id="012fa-233">對</span><span class="sxs-lookup"><span data-stu-id="012fa-233">True</span></span>                                                            |
| <span data-ttu-id="012fa-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="012fa-234">Is Indexed</span></span>             | <span data-ttu-id="012fa-235">否</span><span class="sxs-lookup"><span data-stu-id="012fa-235">False</span></span>                                                           |
| <span data-ttu-id="012fa-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="012fa-236">In Global Catalog</span></span>      | <span data-ttu-id="012fa-237">否</span><span class="sxs-lookup"><span data-stu-id="012fa-237">False</span></span>                                                           |
| <span data-ttu-id="012fa-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="012fa-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="012fa-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="012fa-239">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="012fa-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="012fa-240">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="012fa-241">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-242">Search-Flags</span></span>           | <span data-ttu-id="012fa-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="012fa-243">0x00000000</span></span>                                                      |
| <span data-ttu-id="012fa-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-244">System-Flags</span></span>           | <span data-ttu-id="012fa-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="012fa-245">0x00000010</span></span>                                                      |
| <span data-ttu-id="012fa-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="012fa-246">Classes used in</span></span>        | [<span data-ttu-id="012fa-247">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="012fa-247">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="012fa-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="012fa-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="012fa-249">進入</span><span class="sxs-lookup"><span data-stu-id="012fa-249">Entry</span></span> | <span data-ttu-id="012fa-250">值</span><span class="sxs-lookup"><span data-stu-id="012fa-250">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="012fa-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="012fa-251">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="012fa-252">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="012fa-253">System-Only</span></span>            | <span data-ttu-id="012fa-254">否</span><span class="sxs-lookup"><span data-stu-id="012fa-254">False</span></span>                                                           |
| <span data-ttu-id="012fa-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="012fa-255">Is-Single-Valued</span></span>       | <span data-ttu-id="012fa-256">對</span><span class="sxs-lookup"><span data-stu-id="012fa-256">True</span></span>                                                            |
| <span data-ttu-id="012fa-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="012fa-257">Is Indexed</span></span>             | <span data-ttu-id="012fa-258">否</span><span class="sxs-lookup"><span data-stu-id="012fa-258">False</span></span>                                                           |
| <span data-ttu-id="012fa-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="012fa-259">In Global Catalog</span></span>      | <span data-ttu-id="012fa-260">否</span><span class="sxs-lookup"><span data-stu-id="012fa-260">False</span></span>                                                           |
| <span data-ttu-id="012fa-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="012fa-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="012fa-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="012fa-262">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="012fa-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="012fa-263">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="012fa-264">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-265">Search-Flags</span></span>           | <span data-ttu-id="012fa-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="012fa-266">0x00000000</span></span>                                                      |
| <span data-ttu-id="012fa-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-267">System-Flags</span></span>           | <span data-ttu-id="012fa-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="012fa-268">0x00000010</span></span>                                                      |
| <span data-ttu-id="012fa-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="012fa-269">Classes used in</span></span>        | [<span data-ttu-id="012fa-270">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="012fa-270">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="012fa-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="012fa-271">Windows Server 2012</span></span>



| <span data-ttu-id="012fa-272">進入</span><span class="sxs-lookup"><span data-stu-id="012fa-272">Entry</span></span> | <span data-ttu-id="012fa-273">值</span><span class="sxs-lookup"><span data-stu-id="012fa-273">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="012fa-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="012fa-274">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="012fa-275">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="012fa-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="012fa-276">System-Only</span></span>            | <span data-ttu-id="012fa-277">否</span><span class="sxs-lookup"><span data-stu-id="012fa-277">False</span></span>                                                           |
| <span data-ttu-id="012fa-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="012fa-278">Is-Single-Valued</span></span>       | <span data-ttu-id="012fa-279">對</span><span class="sxs-lookup"><span data-stu-id="012fa-279">True</span></span>                                                            |
| <span data-ttu-id="012fa-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="012fa-280">Is Indexed</span></span>             | <span data-ttu-id="012fa-281">否</span><span class="sxs-lookup"><span data-stu-id="012fa-281">False</span></span>                                                           |
| <span data-ttu-id="012fa-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="012fa-282">In Global Catalog</span></span>      | <span data-ttu-id="012fa-283">否</span><span class="sxs-lookup"><span data-stu-id="012fa-283">False</span></span>                                                           |
| <span data-ttu-id="012fa-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="012fa-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="012fa-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="012fa-285">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="012fa-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="012fa-286">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="012fa-287">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="012fa-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-288">Search-Flags</span></span>           | <span data-ttu-id="012fa-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="012fa-289">0x00000000</span></span>                                                      |
| <span data-ttu-id="012fa-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="012fa-290">System-Flags</span></span>           | <span data-ttu-id="012fa-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="012fa-291">0x00000010</span></span>                                                      |
| <span data-ttu-id="012fa-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="012fa-292">Classes used in</span></span>        | [<span data-ttu-id="012fa-293">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="012fa-293">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





