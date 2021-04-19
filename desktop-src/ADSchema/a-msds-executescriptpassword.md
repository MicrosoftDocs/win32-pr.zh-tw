---
title: ExecuteScriptPassword 屬性
description: 在網域重新命名期間使用。 此值無法使用 LDAP 寫入或讀取。
ms.assetid: 381c3676-0a11-4e53-8093-f04dbf156250
ms.tgt_platform: multiple
keywords:
- ExecuteScriptPassword 屬性 AD 架構
- ExecuteScriptPassword 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-ExecuteScriptPassword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01ebb231404188235236442df1d4916814f0636
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971899"
---
# <a name="ms-ds-executescriptpassword-attribute"></a><span data-ttu-id="60e33-106">ExecuteScriptPassword 屬性</span><span class="sxs-lookup"><span data-stu-id="60e33-106">ms-DS-ExecuteScriptPassword attribute</span></span>

<span data-ttu-id="60e33-107">在網域重新命名期間使用。</span><span class="sxs-lookup"><span data-stu-id="60e33-107">Used during domain rename.</span></span> <span data-ttu-id="60e33-108">此值無法使用 LDAP 寫入或讀取。</span><span class="sxs-lookup"><span data-stu-id="60e33-108">This value cannot be written to or read from by using LDAP.</span></span>



| <span data-ttu-id="60e33-109">進入</span><span class="sxs-lookup"><span data-stu-id="60e33-109">Entry</span></span> | <span data-ttu-id="60e33-110">值</span><span class="sxs-lookup"><span data-stu-id="60e33-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="60e33-111">CN</span><span class="sxs-lookup"><span data-stu-id="60e33-111">CN</span></span>                | <span data-ttu-id="60e33-112">ExecuteScriptPassword</span><span class="sxs-lookup"><span data-stu-id="60e33-112">ms-DS-ExecuteScriptPassword</span></span>                           |
| <span data-ttu-id="60e33-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="60e33-113">Ldap-Display-Name</span></span> | <span data-ttu-id="60e33-114">ExecuteScriptPassword</span><span class="sxs-lookup"><span data-stu-id="60e33-114">msDS-ExecuteScriptPassword</span></span>                            |
| <span data-ttu-id="60e33-115">大小</span><span class="sxs-lookup"><span data-stu-id="60e33-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="60e33-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="60e33-116">Update Privilege</span></span>  | <span data-ttu-id="60e33-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="60e33-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="60e33-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="60e33-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="60e33-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="60e33-119">Attribute-Id</span></span>      | <span data-ttu-id="60e33-120">1.2.840.113556.1.4.1783</span><span class="sxs-lookup"><span data-stu-id="60e33-120">1.2.840.113556.1.4.1783</span></span>                               |
| <span data-ttu-id="60e33-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="60e33-121">System-Id-Guid</span></span>    | <span data-ttu-id="60e33-122">9d054a5a-d187-46c1-9d85-42dfc44a56dd</span><span class="sxs-lookup"><span data-stu-id="60e33-122">9d054a5a-d187-46c1-9d85-42dfc44a56dd</span></span>                  |
| <span data-ttu-id="60e33-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="60e33-123">Syntax</span></span>            | [<span data-ttu-id="60e33-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="60e33-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="60e33-125">實作</span><span class="sxs-lookup"><span data-stu-id="60e33-125">Implementations</span></span>

-   [<span data-ttu-id="60e33-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="60e33-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="60e33-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="60e33-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="60e33-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="60e33-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="60e33-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="60e33-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="60e33-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="60e33-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="60e33-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="60e33-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="60e33-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="60e33-132">Windows Server 2003</span></span>



| <span data-ttu-id="60e33-133">進入</span><span class="sxs-lookup"><span data-stu-id="60e33-133">Entry</span></span> | <span data-ttu-id="60e33-134">值</span><span class="sxs-lookup"><span data-stu-id="60e33-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="60e33-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="60e33-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="60e33-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60e33-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="60e33-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="60e33-137">System-Only</span></span>            | <span data-ttu-id="60e33-138">對</span><span class="sxs-lookup"><span data-stu-id="60e33-138">True</span></span>                                                          |
| <span data-ttu-id="60e33-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="60e33-139">Is-Single-Valued</span></span>       | <span data-ttu-id="60e33-140">對</span><span class="sxs-lookup"><span data-stu-id="60e33-140">True</span></span>                                                          |
| <span data-ttu-id="60e33-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="60e33-141">Is Indexed</span></span>             | <span data-ttu-id="60e33-142">否</span><span class="sxs-lookup"><span data-stu-id="60e33-142">False</span></span>                                                         |
| <span data-ttu-id="60e33-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="60e33-143">In Global Catalog</span></span>      | <span data-ttu-id="60e33-144">否</span><span class="sxs-lookup"><span data-stu-id="60e33-144">False</span></span>                                                         |
| <span data-ttu-id="60e33-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="60e33-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="60e33-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="60e33-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="60e33-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60e33-147">Range-Lower</span></span>            | <span data-ttu-id="60e33-148">0</span><span class="sxs-lookup"><span data-stu-id="60e33-148">0</span></span>                                                             |
| <span data-ttu-id="60e33-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60e33-149">Range-Upper</span></span>            | <span data-ttu-id="60e33-150">64</span><span class="sxs-lookup"><span data-stu-id="60e33-150">64</span></span>                                                            |
| <span data-ttu-id="60e33-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60e33-151">Search-Flags</span></span>           | <span data-ttu-id="60e33-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60e33-152">0x00000000</span></span>                                                    |
| <span data-ttu-id="60e33-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60e33-153">System-Flags</span></span>           | <span data-ttu-id="60e33-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="60e33-154">0x00000011</span></span>                                                    |
| <span data-ttu-id="60e33-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="60e33-155">Classes used in</span></span>        | [<span data-ttu-id="60e33-156">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="60e33-156">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="60e33-157">亞當</span><span class="sxs-lookup"><span data-stu-id="60e33-157">ADAM</span></span>



| <span data-ttu-id="60e33-158">進入</span><span class="sxs-lookup"><span data-stu-id="60e33-158">Entry</span></span> | <span data-ttu-id="60e33-159">值</span><span class="sxs-lookup"><span data-stu-id="60e33-159">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="60e33-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="60e33-160">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="60e33-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60e33-161">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="60e33-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="60e33-162">System-Only</span></span>            | <span data-ttu-id="60e33-163">對</span><span class="sxs-lookup"><span data-stu-id="60e33-163">True</span></span>                                                          |
| <span data-ttu-id="60e33-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="60e33-164">Is-Single-Valued</span></span>       | <span data-ttu-id="60e33-165">對</span><span class="sxs-lookup"><span data-stu-id="60e33-165">True</span></span>                                                          |
| <span data-ttu-id="60e33-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="60e33-166">Is Indexed</span></span>             | <span data-ttu-id="60e33-167">否</span><span class="sxs-lookup"><span data-stu-id="60e33-167">False</span></span>                                                         |
| <span data-ttu-id="60e33-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="60e33-168">In Global Catalog</span></span>      | <span data-ttu-id="60e33-169">否</span><span class="sxs-lookup"><span data-stu-id="60e33-169">False</span></span>                                                         |
| <span data-ttu-id="60e33-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="60e33-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="60e33-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="60e33-171">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="60e33-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60e33-172">Range-Lower</span></span>            | <span data-ttu-id="60e33-173">0</span><span class="sxs-lookup"><span data-stu-id="60e33-173">0</span></span>                                                             |
| <span data-ttu-id="60e33-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60e33-174">Range-Upper</span></span>            | <span data-ttu-id="60e33-175">64</span><span class="sxs-lookup"><span data-stu-id="60e33-175">64</span></span>                                                            |
| <span data-ttu-id="60e33-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60e33-176">Search-Flags</span></span>           | <span data-ttu-id="60e33-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60e33-177">0x00000000</span></span>                                                    |
| <span data-ttu-id="60e33-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60e33-178">System-Flags</span></span>           | <span data-ttu-id="60e33-179">0x00000011</span><span class="sxs-lookup"><span data-stu-id="60e33-179">0x00000011</span></span>                                                    |
| <span data-ttu-id="60e33-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="60e33-180">Classes used in</span></span>        | [<span data-ttu-id="60e33-181">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="60e33-181">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="60e33-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="60e33-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="60e33-183">進入</span><span class="sxs-lookup"><span data-stu-id="60e33-183">Entry</span></span> | <span data-ttu-id="60e33-184">值</span><span class="sxs-lookup"><span data-stu-id="60e33-184">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="60e33-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="60e33-185">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="60e33-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60e33-186">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="60e33-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="60e33-187">System-Only</span></span>            | <span data-ttu-id="60e33-188">對</span><span class="sxs-lookup"><span data-stu-id="60e33-188">True</span></span>                                                          |
| <span data-ttu-id="60e33-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="60e33-189">Is-Single-Valued</span></span>       | <span data-ttu-id="60e33-190">對</span><span class="sxs-lookup"><span data-stu-id="60e33-190">True</span></span>                                                          |
| <span data-ttu-id="60e33-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="60e33-191">Is Indexed</span></span>             | <span data-ttu-id="60e33-192">否</span><span class="sxs-lookup"><span data-stu-id="60e33-192">False</span></span>                                                         |
| <span data-ttu-id="60e33-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="60e33-193">In Global Catalog</span></span>      | <span data-ttu-id="60e33-194">否</span><span class="sxs-lookup"><span data-stu-id="60e33-194">False</span></span>                                                         |
| <span data-ttu-id="60e33-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="60e33-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="60e33-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="60e33-196">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="60e33-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60e33-197">Range-Lower</span></span>            | <span data-ttu-id="60e33-198">0</span><span class="sxs-lookup"><span data-stu-id="60e33-198">0</span></span>                                                             |
| <span data-ttu-id="60e33-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60e33-199">Range-Upper</span></span>            | <span data-ttu-id="60e33-200">64</span><span class="sxs-lookup"><span data-stu-id="60e33-200">64</span></span>                                                            |
| <span data-ttu-id="60e33-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60e33-201">Search-Flags</span></span>           | <span data-ttu-id="60e33-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60e33-202">0x00000000</span></span>                                                    |
| <span data-ttu-id="60e33-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60e33-203">System-Flags</span></span>           | <span data-ttu-id="60e33-204">0x00000011</span><span class="sxs-lookup"><span data-stu-id="60e33-204">0x00000011</span></span>                                                    |
| <span data-ttu-id="60e33-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="60e33-205">Classes used in</span></span>        | [<span data-ttu-id="60e33-206">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="60e33-206">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="60e33-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60e33-207">Windows Server 2008</span></span>



| <span data-ttu-id="60e33-208">進入</span><span class="sxs-lookup"><span data-stu-id="60e33-208">Entry</span></span> | <span data-ttu-id="60e33-209">值</span><span class="sxs-lookup"><span data-stu-id="60e33-209">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e33-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="60e33-210">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="60e33-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60e33-211">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="60e33-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="60e33-212">System-Only</span></span>            | <span data-ttu-id="60e33-213">對</span><span class="sxs-lookup"><span data-stu-id="60e33-213">True</span></span>                                                                                                    |
| <span data-ttu-id="60e33-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="60e33-214">Is-Single-Valued</span></span>       | <span data-ttu-id="60e33-215">對</span><span class="sxs-lookup"><span data-stu-id="60e33-215">True</span></span>                                                                                                    |
| <span data-ttu-id="60e33-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="60e33-216">Is Indexed</span></span>             | <span data-ttu-id="60e33-217">否</span><span class="sxs-lookup"><span data-stu-id="60e33-217">False</span></span>                                                                                                   |
| <span data-ttu-id="60e33-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="60e33-218">In Global Catalog</span></span>      | <span data-ttu-id="60e33-219">否</span><span class="sxs-lookup"><span data-stu-id="60e33-219">False</span></span>                                                                                                   |
| <span data-ttu-id="60e33-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="60e33-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="60e33-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="60e33-221">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="60e33-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60e33-222">Range-Lower</span></span>            | <span data-ttu-id="60e33-223">0</span><span class="sxs-lookup"><span data-stu-id="60e33-223">0</span></span>                                                                                                       |
| <span data-ttu-id="60e33-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60e33-224">Range-Upper</span></span>            | <span data-ttu-id="60e33-225">64</span><span class="sxs-lookup"><span data-stu-id="60e33-225">64</span></span>                                                                                                      |
| <span data-ttu-id="60e33-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60e33-226">Search-Flags</span></span>           | <span data-ttu-id="60e33-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60e33-227">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="60e33-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60e33-228">System-Flags</span></span>           | <span data-ttu-id="60e33-229">0x00000011</span><span class="sxs-lookup"><span data-stu-id="60e33-229">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="60e33-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="60e33-230">Classes used in</span></span>        | [<span data-ttu-id="60e33-231">**電腦**</span><span class="sxs-lookup"><span data-stu-id="60e33-231">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="60e33-232">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="60e33-232">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="60e33-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="60e33-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="60e33-234">進入</span><span class="sxs-lookup"><span data-stu-id="60e33-234">Entry</span></span> | <span data-ttu-id="60e33-235">值</span><span class="sxs-lookup"><span data-stu-id="60e33-235">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e33-236">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="60e33-236">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="60e33-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60e33-237">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="60e33-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="60e33-238">System-Only</span></span>            | <span data-ttu-id="60e33-239">對</span><span class="sxs-lookup"><span data-stu-id="60e33-239">True</span></span>                                                                                                    |
| <span data-ttu-id="60e33-240">是-單一值</span><span class="sxs-lookup"><span data-stu-id="60e33-240">Is-Single-Valued</span></span>       | <span data-ttu-id="60e33-241">對</span><span class="sxs-lookup"><span data-stu-id="60e33-241">True</span></span>                                                                                                    |
| <span data-ttu-id="60e33-242">已編制索引</span><span class="sxs-lookup"><span data-stu-id="60e33-242">Is Indexed</span></span>             | <span data-ttu-id="60e33-243">否</span><span class="sxs-lookup"><span data-stu-id="60e33-243">False</span></span>                                                                                                   |
| <span data-ttu-id="60e33-244">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="60e33-244">In Global Catalog</span></span>      | <span data-ttu-id="60e33-245">否</span><span class="sxs-lookup"><span data-stu-id="60e33-245">False</span></span>                                                                                                   |
| <span data-ttu-id="60e33-246">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="60e33-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="60e33-247">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="60e33-247">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="60e33-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60e33-248">Range-Lower</span></span>            | <span data-ttu-id="60e33-249">0</span><span class="sxs-lookup"><span data-stu-id="60e33-249">0</span></span>                                                                                                       |
| <span data-ttu-id="60e33-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60e33-250">Range-Upper</span></span>            | <span data-ttu-id="60e33-251">64</span><span class="sxs-lookup"><span data-stu-id="60e33-251">64</span></span>                                                                                                      |
| <span data-ttu-id="60e33-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60e33-252">Search-Flags</span></span>           | <span data-ttu-id="60e33-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60e33-253">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="60e33-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60e33-254">System-Flags</span></span>           | <span data-ttu-id="60e33-255">0x00000011</span><span class="sxs-lookup"><span data-stu-id="60e33-255">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="60e33-256">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="60e33-256">Classes used in</span></span>        | [<span data-ttu-id="60e33-257">**電腦**</span><span class="sxs-lookup"><span data-stu-id="60e33-257">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="60e33-258">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="60e33-258">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="60e33-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60e33-259">Windows Server 2012</span></span>



| <span data-ttu-id="60e33-260">進入</span><span class="sxs-lookup"><span data-stu-id="60e33-260">Entry</span></span> | <span data-ttu-id="60e33-261">值</span><span class="sxs-lookup"><span data-stu-id="60e33-261">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e33-262">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="60e33-262">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="60e33-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="60e33-263">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="60e33-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="60e33-264">System-Only</span></span>            | <span data-ttu-id="60e33-265">對</span><span class="sxs-lookup"><span data-stu-id="60e33-265">True</span></span>                                                                                                    |
| <span data-ttu-id="60e33-266">是-單一值</span><span class="sxs-lookup"><span data-stu-id="60e33-266">Is-Single-Valued</span></span>       | <span data-ttu-id="60e33-267">對</span><span class="sxs-lookup"><span data-stu-id="60e33-267">True</span></span>                                                                                                    |
| <span data-ttu-id="60e33-268">已編制索引</span><span class="sxs-lookup"><span data-stu-id="60e33-268">Is Indexed</span></span>             | <span data-ttu-id="60e33-269">否</span><span class="sxs-lookup"><span data-stu-id="60e33-269">False</span></span>                                                                                                   |
| <span data-ttu-id="60e33-270">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="60e33-270">In Global Catalog</span></span>      | <span data-ttu-id="60e33-271">否</span><span class="sxs-lookup"><span data-stu-id="60e33-271">False</span></span>                                                                                                   |
| <span data-ttu-id="60e33-272">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="60e33-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="60e33-273">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="60e33-273">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="60e33-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="60e33-274">Range-Lower</span></span>            | <span data-ttu-id="60e33-275">0</span><span class="sxs-lookup"><span data-stu-id="60e33-275">0</span></span>                                                                                                       |
| <span data-ttu-id="60e33-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="60e33-276">Range-Upper</span></span>            | <span data-ttu-id="60e33-277">64</span><span class="sxs-lookup"><span data-stu-id="60e33-277">64</span></span>                                                                                                      |
| <span data-ttu-id="60e33-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="60e33-278">Search-Flags</span></span>           | <span data-ttu-id="60e33-279">0x00000000</span><span class="sxs-lookup"><span data-stu-id="60e33-279">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="60e33-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="60e33-280">System-Flags</span></span>           | <span data-ttu-id="60e33-281">0x00000011</span><span class="sxs-lookup"><span data-stu-id="60e33-281">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="60e33-282">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="60e33-282">Classes used in</span></span>        | [<span data-ttu-id="60e33-283">**電腦**</span><span class="sxs-lookup"><span data-stu-id="60e33-283">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="60e33-284">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="60e33-284">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





