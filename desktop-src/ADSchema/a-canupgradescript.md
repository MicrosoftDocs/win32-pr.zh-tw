---
title: 可升級-腳本屬性
description: 這個屬性會儲存可以升級的應用程式封裝清單，或可升級此應用程式封裝的應用程式封裝。
ms.assetid: 95dea9c7-dbbd-42fb-ab32-6b89490aa5d6
ms.tgt_platform: multiple
keywords:
- 可以-升級-腳本屬性 AD 架構
- canUpgradeScript 屬性 AD 架構
topic_type:
- apiref
api_name:
- Can-Upgrade-Script
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e5b90c45d124a8647dd5d3a0af9c4a2ca6c4f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970271"
---
# <a name="can-upgrade-script-attribute"></a><span data-ttu-id="1f556-105">可升級-腳本屬性</span><span class="sxs-lookup"><span data-stu-id="1f556-105">Can-Upgrade-Script attribute</span></span>

<span data-ttu-id="1f556-106">這個屬性會儲存可以升級的應用程式封裝清單，或可升級此應用程式封裝的應用程式封裝。</span><span class="sxs-lookup"><span data-stu-id="1f556-106">This attribute stores the list of application packages that can be upgraded by or which can upgrade this application package.</span></span>



| <span data-ttu-id="1f556-107">進入</span><span class="sxs-lookup"><span data-stu-id="1f556-107">Entry</span></span> | <span data-ttu-id="1f556-108">值</span><span class="sxs-lookup"><span data-stu-id="1f556-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1f556-109">CN</span><span class="sxs-lookup"><span data-stu-id="1f556-109">CN</span></span>                | <span data-ttu-id="1f556-110">可升級-腳本</span><span class="sxs-lookup"><span data-stu-id="1f556-110">Can-Upgrade-Script</span></span>                          |
| <span data-ttu-id="1f556-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1f556-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1f556-112">canUpgradeScript</span><span class="sxs-lookup"><span data-stu-id="1f556-112">canUpgradeScript</span></span>                            |
| <span data-ttu-id="1f556-113">大小</span><span class="sxs-lookup"><span data-stu-id="1f556-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="1f556-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1f556-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="1f556-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1f556-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="1f556-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1f556-116">Attribute-Id</span></span>      | <span data-ttu-id="1f556-117">1.2.840.113556.1.4.815</span><span class="sxs-lookup"><span data-stu-id="1f556-117">1.2.840.113556.1.4.815</span></span>                      |
| <span data-ttu-id="1f556-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1f556-118">System-Id-Guid</span></span>    | <span data-ttu-id="1f556-119">d9e18314-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1f556-119">d9e18314-8939-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="1f556-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f556-120">Syntax</span></span>            | [<span data-ttu-id="1f556-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1f556-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1f556-122">實作</span><span class="sxs-lookup"><span data-stu-id="1f556-122">Implementations</span></span>

-   [<span data-ttu-id="1f556-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1f556-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1f556-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1f556-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1f556-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1f556-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1f556-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1f556-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1f556-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1f556-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1f556-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1f556-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1f556-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1f556-129">Windows 2000 Server</span></span>



| <span data-ttu-id="1f556-130">進入</span><span class="sxs-lookup"><span data-stu-id="1f556-130">Entry</span></span> | <span data-ttu-id="1f556-131">值</span><span class="sxs-lookup"><span data-stu-id="1f556-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f556-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1f556-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f556-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f556-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f556-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f556-134">System-Only</span></span>            | <span data-ttu-id="1f556-135">否</span><span class="sxs-lookup"><span data-stu-id="1f556-135">False</span></span>                                                            |
| <span data-ttu-id="1f556-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1f556-136">Is-Single-Valued</span></span>       | <span data-ttu-id="1f556-137">否</span><span class="sxs-lookup"><span data-stu-id="1f556-137">False</span></span>                                                            |
| <span data-ttu-id="1f556-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1f556-138">Is Indexed</span></span>             | <span data-ttu-id="1f556-139">否</span><span class="sxs-lookup"><span data-stu-id="1f556-139">False</span></span>                                                            |
| <span data-ttu-id="1f556-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1f556-140">In Global Catalog</span></span>      | <span data-ttu-id="1f556-141">否</span><span class="sxs-lookup"><span data-stu-id="1f556-141">False</span></span>                                                            |
| <span data-ttu-id="1f556-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1f556-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f556-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1f556-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f556-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f556-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="1f556-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f556-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="1f556-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f556-146">Search-Flags</span></span>           | <span data-ttu-id="1f556-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f556-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f556-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f556-148">System-Flags</span></span>           | <span data-ttu-id="1f556-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f556-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="1f556-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1f556-150">Classes used in</span></span>        | [<span data-ttu-id="1f556-151">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="1f556-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1f556-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f556-152">Windows Server 2003</span></span>



| <span data-ttu-id="1f556-153">進入</span><span class="sxs-lookup"><span data-stu-id="1f556-153">Entry</span></span> | <span data-ttu-id="1f556-154">值</span><span class="sxs-lookup"><span data-stu-id="1f556-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f556-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1f556-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f556-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f556-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f556-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f556-157">System-Only</span></span>            | <span data-ttu-id="1f556-158">否</span><span class="sxs-lookup"><span data-stu-id="1f556-158">False</span></span>                                                            |
| <span data-ttu-id="1f556-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1f556-159">Is-Single-Valued</span></span>       | <span data-ttu-id="1f556-160">否</span><span class="sxs-lookup"><span data-stu-id="1f556-160">False</span></span>                                                            |
| <span data-ttu-id="1f556-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1f556-161">Is Indexed</span></span>             | <span data-ttu-id="1f556-162">否</span><span class="sxs-lookup"><span data-stu-id="1f556-162">False</span></span>                                                            |
| <span data-ttu-id="1f556-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1f556-163">In Global Catalog</span></span>      | <span data-ttu-id="1f556-164">否</span><span class="sxs-lookup"><span data-stu-id="1f556-164">False</span></span>                                                            |
| <span data-ttu-id="1f556-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1f556-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f556-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1f556-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f556-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f556-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="1f556-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f556-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="1f556-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f556-169">Search-Flags</span></span>           | <span data-ttu-id="1f556-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f556-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f556-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f556-171">System-Flags</span></span>           | <span data-ttu-id="1f556-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f556-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="1f556-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1f556-173">Classes used in</span></span>        | [<span data-ttu-id="1f556-174">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="1f556-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1f556-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1f556-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1f556-176">進入</span><span class="sxs-lookup"><span data-stu-id="1f556-176">Entry</span></span> | <span data-ttu-id="1f556-177">值</span><span class="sxs-lookup"><span data-stu-id="1f556-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f556-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1f556-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f556-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f556-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f556-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f556-180">System-Only</span></span>            | <span data-ttu-id="1f556-181">否</span><span class="sxs-lookup"><span data-stu-id="1f556-181">False</span></span>                                                            |
| <span data-ttu-id="1f556-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1f556-182">Is-Single-Valued</span></span>       | <span data-ttu-id="1f556-183">否</span><span class="sxs-lookup"><span data-stu-id="1f556-183">False</span></span>                                                            |
| <span data-ttu-id="1f556-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1f556-184">Is Indexed</span></span>             | <span data-ttu-id="1f556-185">否</span><span class="sxs-lookup"><span data-stu-id="1f556-185">False</span></span>                                                            |
| <span data-ttu-id="1f556-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1f556-186">In Global Catalog</span></span>      | <span data-ttu-id="1f556-187">否</span><span class="sxs-lookup"><span data-stu-id="1f556-187">False</span></span>                                                            |
| <span data-ttu-id="1f556-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1f556-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f556-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1f556-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f556-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f556-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="1f556-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f556-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="1f556-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f556-192">Search-Flags</span></span>           | <span data-ttu-id="1f556-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f556-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f556-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f556-194">System-Flags</span></span>           | <span data-ttu-id="1f556-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f556-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="1f556-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1f556-196">Classes used in</span></span>        | [<span data-ttu-id="1f556-197">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="1f556-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1f556-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f556-198">Windows Server 2008</span></span>



| <span data-ttu-id="1f556-199">進入</span><span class="sxs-lookup"><span data-stu-id="1f556-199">Entry</span></span> | <span data-ttu-id="1f556-200">值</span><span class="sxs-lookup"><span data-stu-id="1f556-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f556-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1f556-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f556-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f556-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f556-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f556-203">System-Only</span></span>            | <span data-ttu-id="1f556-204">否</span><span class="sxs-lookup"><span data-stu-id="1f556-204">False</span></span>                                                            |
| <span data-ttu-id="1f556-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1f556-205">Is-Single-Valued</span></span>       | <span data-ttu-id="1f556-206">否</span><span class="sxs-lookup"><span data-stu-id="1f556-206">False</span></span>                                                            |
| <span data-ttu-id="1f556-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1f556-207">Is Indexed</span></span>             | <span data-ttu-id="1f556-208">否</span><span class="sxs-lookup"><span data-stu-id="1f556-208">False</span></span>                                                            |
| <span data-ttu-id="1f556-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1f556-209">In Global Catalog</span></span>      | <span data-ttu-id="1f556-210">否</span><span class="sxs-lookup"><span data-stu-id="1f556-210">False</span></span>                                                            |
| <span data-ttu-id="1f556-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1f556-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f556-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1f556-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f556-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f556-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="1f556-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f556-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="1f556-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f556-215">Search-Flags</span></span>           | <span data-ttu-id="1f556-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f556-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f556-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f556-217">System-Flags</span></span>           | <span data-ttu-id="1f556-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f556-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="1f556-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1f556-219">Classes used in</span></span>        | [<span data-ttu-id="1f556-220">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="1f556-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1f556-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1f556-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1f556-222">進入</span><span class="sxs-lookup"><span data-stu-id="1f556-222">Entry</span></span> | <span data-ttu-id="1f556-223">值</span><span class="sxs-lookup"><span data-stu-id="1f556-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f556-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1f556-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f556-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f556-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f556-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f556-226">System-Only</span></span>            | <span data-ttu-id="1f556-227">否</span><span class="sxs-lookup"><span data-stu-id="1f556-227">False</span></span>                                                            |
| <span data-ttu-id="1f556-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1f556-228">Is-Single-Valued</span></span>       | <span data-ttu-id="1f556-229">否</span><span class="sxs-lookup"><span data-stu-id="1f556-229">False</span></span>                                                            |
| <span data-ttu-id="1f556-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1f556-230">Is Indexed</span></span>             | <span data-ttu-id="1f556-231">否</span><span class="sxs-lookup"><span data-stu-id="1f556-231">False</span></span>                                                            |
| <span data-ttu-id="1f556-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1f556-232">In Global Catalog</span></span>      | <span data-ttu-id="1f556-233">否</span><span class="sxs-lookup"><span data-stu-id="1f556-233">False</span></span>                                                            |
| <span data-ttu-id="1f556-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1f556-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f556-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1f556-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f556-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f556-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="1f556-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f556-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="1f556-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f556-238">Search-Flags</span></span>           | <span data-ttu-id="1f556-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f556-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f556-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f556-240">System-Flags</span></span>           | <span data-ttu-id="1f556-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f556-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="1f556-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1f556-242">Classes used in</span></span>        | [<span data-ttu-id="1f556-243">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="1f556-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1f556-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1f556-244">Windows Server 2012</span></span>



| <span data-ttu-id="1f556-245">進入</span><span class="sxs-lookup"><span data-stu-id="1f556-245">Entry</span></span> | <span data-ttu-id="1f556-246">值</span><span class="sxs-lookup"><span data-stu-id="1f556-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1f556-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1f556-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f556-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f556-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="1f556-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f556-249">System-Only</span></span>            | <span data-ttu-id="1f556-250">否</span><span class="sxs-lookup"><span data-stu-id="1f556-250">False</span></span>                                                            |
| <span data-ttu-id="1f556-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1f556-251">Is-Single-Valued</span></span>       | <span data-ttu-id="1f556-252">否</span><span class="sxs-lookup"><span data-stu-id="1f556-252">False</span></span>                                                            |
| <span data-ttu-id="1f556-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1f556-253">Is Indexed</span></span>             | <span data-ttu-id="1f556-254">否</span><span class="sxs-lookup"><span data-stu-id="1f556-254">False</span></span>                                                            |
| <span data-ttu-id="1f556-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1f556-255">In Global Catalog</span></span>      | <span data-ttu-id="1f556-256">否</span><span class="sxs-lookup"><span data-stu-id="1f556-256">False</span></span>                                                            |
| <span data-ttu-id="1f556-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1f556-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f556-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1f556-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="1f556-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f556-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="1f556-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f556-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="1f556-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f556-261">Search-Flags</span></span>           | <span data-ttu-id="1f556-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1f556-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="1f556-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f556-263">System-Flags</span></span>           | <span data-ttu-id="1f556-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f556-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="1f556-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1f556-265">Classes used in</span></span>        | [<span data-ttu-id="1f556-266">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="1f556-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





