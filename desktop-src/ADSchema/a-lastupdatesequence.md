---
title: 上次更新順序屬性
description: 這個屬性包含已變更之類別存放區中最後一個專案的更新序號。
ms.assetid: fd434b8d-31b4-45f7-8d8f-048f61cabb92
ms.tgt_platform: multiple
keywords:
- 上次更新順序屬性 AD 架構
- lastUpdateSequence 屬性 AD 架構
topic_type:
- apiref
api_name:
- Last-Update-Sequence
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e670c6784ded96a1e81d98f5f1c9bfb859efaa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106967582"
---
# <a name="last-update-sequence-attribute"></a><span data-ttu-id="ce904-105">上次更新順序屬性</span><span class="sxs-lookup"><span data-stu-id="ce904-105">Last-Update-Sequence attribute</span></span>

<span data-ttu-id="ce904-106">這個屬性包含已變更之類別存放區中最後一個專案的更新序號。</span><span class="sxs-lookup"><span data-stu-id="ce904-106">This attribute contains the update sequence number for the last item in the class store that was changed.</span></span>



| <span data-ttu-id="ce904-107">進入</span><span class="sxs-lookup"><span data-stu-id="ce904-107">Entry</span></span> | <span data-ttu-id="ce904-108">值</span><span class="sxs-lookup"><span data-stu-id="ce904-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ce904-109">CN</span><span class="sxs-lookup"><span data-stu-id="ce904-109">CN</span></span>                | <span data-ttu-id="ce904-110">上次更新順序</span><span class="sxs-lookup"><span data-stu-id="ce904-110">Last-Update-Sequence</span></span>                        |
| <span data-ttu-id="ce904-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ce904-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ce904-112">lastUpdateSequence</span><span class="sxs-lookup"><span data-stu-id="ce904-112">lastUpdateSequence</span></span>                          |
| <span data-ttu-id="ce904-113">大小</span><span class="sxs-lookup"><span data-stu-id="ce904-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="ce904-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ce904-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="ce904-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ce904-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ce904-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ce904-116">Attribute-Id</span></span>      | <span data-ttu-id="ce904-117">1.2.840.113556.1.4.330</span><span class="sxs-lookup"><span data-stu-id="ce904-117">1.2.840.113556.1.4.330</span></span>                      |
| <span data-ttu-id="ce904-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ce904-118">System-Id-Guid</span></span>    | <span data-ttu-id="ce904-119">7d6c0e9c-7e20-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="ce904-119">7d6c0e9c-7e20-11d0-afd6-00c04fd930c9</span></span>        |
| <span data-ttu-id="ce904-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce904-120">Syntax</span></span>            | [<span data-ttu-id="ce904-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ce904-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ce904-122">實作</span><span class="sxs-lookup"><span data-stu-id="ce904-122">Implementations</span></span>

-   [<span data-ttu-id="ce904-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ce904-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ce904-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ce904-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ce904-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ce904-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ce904-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ce904-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ce904-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ce904-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ce904-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ce904-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ce904-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ce904-129">Windows 2000 Server</span></span>



| <span data-ttu-id="ce904-130">進入</span><span class="sxs-lookup"><span data-stu-id="ce904-130">Entry</span></span> | <span data-ttu-id="ce904-131">值</span><span class="sxs-lookup"><span data-stu-id="ce904-131">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce904-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ce904-132">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="ce904-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce904-133">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="ce904-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce904-134">System-Only</span></span>            | <span data-ttu-id="ce904-135">否</span><span class="sxs-lookup"><span data-stu-id="ce904-135">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ce904-136">Is-Single-Valued</span></span>       | <span data-ttu-id="ce904-137">對</span><span class="sxs-lookup"><span data-stu-id="ce904-137">True</span></span>                                                                                                            |
| <span data-ttu-id="ce904-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ce904-138">Is Indexed</span></span>             | <span data-ttu-id="ce904-139">否</span><span class="sxs-lookup"><span data-stu-id="ce904-139">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ce904-140">In Global Catalog</span></span>      | <span data-ttu-id="ce904-141">否</span><span class="sxs-lookup"><span data-stu-id="ce904-141">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ce904-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce904-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ce904-143">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="ce904-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce904-144">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="ce904-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce904-145">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="ce904-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce904-146">Search-Flags</span></span>           | <span data-ttu-id="ce904-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce904-147">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="ce904-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce904-148">System-Flags</span></span>           | <span data-ttu-id="ce904-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce904-149">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="ce904-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ce904-150">Classes used in</span></span>        | [<span data-ttu-id="ce904-151">**類別存放區**</span><span class="sxs-lookup"><span data-stu-id="ce904-151">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="ce904-152">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="ce904-152">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ce904-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce904-153">Windows Server 2003</span></span>



| <span data-ttu-id="ce904-154">進入</span><span class="sxs-lookup"><span data-stu-id="ce904-154">Entry</span></span> | <span data-ttu-id="ce904-155">值</span><span class="sxs-lookup"><span data-stu-id="ce904-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce904-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ce904-156">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="ce904-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce904-157">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="ce904-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce904-158">System-Only</span></span>            | <span data-ttu-id="ce904-159">否</span><span class="sxs-lookup"><span data-stu-id="ce904-159">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ce904-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ce904-161">對</span><span class="sxs-lookup"><span data-stu-id="ce904-161">True</span></span>                                                                                                            |
| <span data-ttu-id="ce904-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ce904-162">Is Indexed</span></span>             | <span data-ttu-id="ce904-163">否</span><span class="sxs-lookup"><span data-stu-id="ce904-163">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ce904-164">In Global Catalog</span></span>      | <span data-ttu-id="ce904-165">否</span><span class="sxs-lookup"><span data-stu-id="ce904-165">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ce904-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce904-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ce904-167">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="ce904-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce904-168">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="ce904-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce904-169">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="ce904-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce904-170">Search-Flags</span></span>           | <span data-ttu-id="ce904-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce904-171">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="ce904-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce904-172">System-Flags</span></span>           | <span data-ttu-id="ce904-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce904-173">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="ce904-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ce904-174">Classes used in</span></span>        | [<span data-ttu-id="ce904-175">**類別存放區**</span><span class="sxs-lookup"><span data-stu-id="ce904-175">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="ce904-176">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="ce904-176">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ce904-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ce904-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ce904-178">進入</span><span class="sxs-lookup"><span data-stu-id="ce904-178">Entry</span></span> | <span data-ttu-id="ce904-179">值</span><span class="sxs-lookup"><span data-stu-id="ce904-179">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce904-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ce904-180">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="ce904-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce904-181">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="ce904-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce904-182">System-Only</span></span>            | <span data-ttu-id="ce904-183">否</span><span class="sxs-lookup"><span data-stu-id="ce904-183">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ce904-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ce904-185">對</span><span class="sxs-lookup"><span data-stu-id="ce904-185">True</span></span>                                                                                                            |
| <span data-ttu-id="ce904-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ce904-186">Is Indexed</span></span>             | <span data-ttu-id="ce904-187">否</span><span class="sxs-lookup"><span data-stu-id="ce904-187">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ce904-188">In Global Catalog</span></span>      | <span data-ttu-id="ce904-189">否</span><span class="sxs-lookup"><span data-stu-id="ce904-189">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ce904-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce904-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ce904-191">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="ce904-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce904-192">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="ce904-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce904-193">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="ce904-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce904-194">Search-Flags</span></span>           | <span data-ttu-id="ce904-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce904-195">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="ce904-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce904-196">System-Flags</span></span>           | <span data-ttu-id="ce904-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce904-197">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="ce904-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ce904-198">Classes used in</span></span>        | [<span data-ttu-id="ce904-199">**類別存放區**</span><span class="sxs-lookup"><span data-stu-id="ce904-199">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="ce904-200">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="ce904-200">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ce904-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce904-201">Windows Server 2008</span></span>



| <span data-ttu-id="ce904-202">進入</span><span class="sxs-lookup"><span data-stu-id="ce904-202">Entry</span></span> | <span data-ttu-id="ce904-203">值</span><span class="sxs-lookup"><span data-stu-id="ce904-203">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce904-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ce904-204">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="ce904-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce904-205">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="ce904-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce904-206">System-Only</span></span>            | <span data-ttu-id="ce904-207">否</span><span class="sxs-lookup"><span data-stu-id="ce904-207">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ce904-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ce904-209">對</span><span class="sxs-lookup"><span data-stu-id="ce904-209">True</span></span>                                                                                                            |
| <span data-ttu-id="ce904-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ce904-210">Is Indexed</span></span>             | <span data-ttu-id="ce904-211">否</span><span class="sxs-lookup"><span data-stu-id="ce904-211">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ce904-212">In Global Catalog</span></span>      | <span data-ttu-id="ce904-213">否</span><span class="sxs-lookup"><span data-stu-id="ce904-213">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ce904-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce904-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ce904-215">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="ce904-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce904-216">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="ce904-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce904-217">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="ce904-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce904-218">Search-Flags</span></span>           | <span data-ttu-id="ce904-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce904-219">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="ce904-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce904-220">System-Flags</span></span>           | <span data-ttu-id="ce904-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce904-221">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="ce904-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ce904-222">Classes used in</span></span>        | [<span data-ttu-id="ce904-223">**類別存放區**</span><span class="sxs-lookup"><span data-stu-id="ce904-223">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="ce904-224">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="ce904-224">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ce904-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ce904-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ce904-226">進入</span><span class="sxs-lookup"><span data-stu-id="ce904-226">Entry</span></span> | <span data-ttu-id="ce904-227">值</span><span class="sxs-lookup"><span data-stu-id="ce904-227">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce904-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ce904-228">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="ce904-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce904-229">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="ce904-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce904-230">System-Only</span></span>            | <span data-ttu-id="ce904-231">否</span><span class="sxs-lookup"><span data-stu-id="ce904-231">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ce904-232">Is-Single-Valued</span></span>       | <span data-ttu-id="ce904-233">對</span><span class="sxs-lookup"><span data-stu-id="ce904-233">True</span></span>                                                                                                            |
| <span data-ttu-id="ce904-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ce904-234">Is Indexed</span></span>             | <span data-ttu-id="ce904-235">否</span><span class="sxs-lookup"><span data-stu-id="ce904-235">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ce904-236">In Global Catalog</span></span>      | <span data-ttu-id="ce904-237">否</span><span class="sxs-lookup"><span data-stu-id="ce904-237">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ce904-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce904-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ce904-239">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="ce904-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce904-240">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="ce904-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce904-241">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="ce904-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce904-242">Search-Flags</span></span>           | <span data-ttu-id="ce904-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce904-243">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="ce904-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce904-244">System-Flags</span></span>           | <span data-ttu-id="ce904-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce904-245">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="ce904-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ce904-246">Classes used in</span></span>        | [<span data-ttu-id="ce904-247">**類別存放區**</span><span class="sxs-lookup"><span data-stu-id="ce904-247">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="ce904-248">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="ce904-248">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ce904-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ce904-249">Windows Server 2012</span></span>



| <span data-ttu-id="ce904-250">進入</span><span class="sxs-lookup"><span data-stu-id="ce904-250">Entry</span></span> | <span data-ttu-id="ce904-251">值</span><span class="sxs-lookup"><span data-stu-id="ce904-251">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce904-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ce904-252">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="ce904-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce904-253">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="ce904-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce904-254">System-Only</span></span>            | <span data-ttu-id="ce904-255">否</span><span class="sxs-lookup"><span data-stu-id="ce904-255">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ce904-256">Is-Single-Valued</span></span>       | <span data-ttu-id="ce904-257">對</span><span class="sxs-lookup"><span data-stu-id="ce904-257">True</span></span>                                                                                                            |
| <span data-ttu-id="ce904-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ce904-258">Is Indexed</span></span>             | <span data-ttu-id="ce904-259">否</span><span class="sxs-lookup"><span data-stu-id="ce904-259">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ce904-260">In Global Catalog</span></span>      | <span data-ttu-id="ce904-261">否</span><span class="sxs-lookup"><span data-stu-id="ce904-261">False</span></span>                                                                                                           |
| <span data-ttu-id="ce904-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ce904-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce904-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ce904-263">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="ce904-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce904-264">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="ce904-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce904-265">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="ce904-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce904-266">Search-Flags</span></span>           | <span data-ttu-id="ce904-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce904-267">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="ce904-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce904-268">System-Flags</span></span>           | <span data-ttu-id="ce904-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce904-269">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="ce904-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ce904-270">Classes used in</span></span>        | [<span data-ttu-id="ce904-271">**類別存放區**</span><span class="sxs-lookup"><span data-stu-id="ce904-271">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="ce904-272">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="ce904-272">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





