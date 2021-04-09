---
title: 安裝-Ui 層級屬性
description: 此屬性包含用於使用者介面之安裝 (層級) 類型的資訊。
ms.assetid: 718e04c7-ea96-4519-b312-12534ffd66df
ms.tgt_platform: multiple
keywords:
- 安裝-Ui 層級屬性 AD 架構
- installUiLevel 屬性 AD 架構
topic_type:
- apiref
api_name:
- Install-Ui-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b93900bb401d1bdcd72f8881fb78026745c4e8f6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935246"
---
# <a name="install-ui-level-attribute"></a><span data-ttu-id="77bb1-105">安裝-Ui 層級屬性</span><span class="sxs-lookup"><span data-stu-id="77bb1-105">Install-Ui-Level attribute</span></span>

<span data-ttu-id="77bb1-106">此屬性包含用於使用者介面之安裝 (層級) 類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="77bb1-106">This attribute contains information for the type (level) of installation that is used for the user interface.</span></span> <span data-ttu-id="77bb1-107">可能的安裝層級如下所示： 2 INSTALLUILEVEL \_ 無無訊息安裝 (無訊息安裝) 3 INSTALLUILEVEL \_ 基本 (簡單安裝，錯誤處理) 4 INSTALLUILEVEL \_ 減少 (撰寫的 ui \_</span><span class="sxs-lookup"><span data-stu-id="77bb1-107">Possible installation levels are as follows: 2 INSTALLUILEVEL\_NONE (silent installation) 3 INSTALLUILEVEL\_BASIC (simple installation with error handling) 4 INSTALLUILEVEL\_REDUCED (authored UI, wizard dialog boxes suppressed) 5 INSTALLUILEVEL\_FULL (authored UI with wizards, progress, errors)</span></span>



| <span data-ttu-id="77bb1-108">進入</span><span class="sxs-lookup"><span data-stu-id="77bb1-108">Entry</span></span> | <span data-ttu-id="77bb1-109">值</span><span class="sxs-lookup"><span data-stu-id="77bb1-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="77bb1-110">CN</span><span class="sxs-lookup"><span data-stu-id="77bb1-110">CN</span></span>                | <span data-ttu-id="77bb1-111">安裝-Ui 層級</span><span class="sxs-lookup"><span data-stu-id="77bb1-111">Install-Ui-Level</span></span>                     |
| <span data-ttu-id="77bb1-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="77bb1-112">Ldap-Display-Name</span></span> | <span data-ttu-id="77bb1-113">installUiLevel</span><span class="sxs-lookup"><span data-stu-id="77bb1-113">installUiLevel</span></span>                       |
| <span data-ttu-id="77bb1-114">大小</span><span class="sxs-lookup"><span data-stu-id="77bb1-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="77bb1-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="77bb1-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="77bb1-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="77bb1-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="77bb1-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="77bb1-117">Attribute-Id</span></span>      | <span data-ttu-id="77bb1-118">1.2.840.113556.1.4.847</span><span class="sxs-lookup"><span data-stu-id="77bb1-118">1.2.840.113556.1.4.847</span></span>               |
| <span data-ttu-id="77bb1-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="77bb1-119">System-Id-Guid</span></span>    | <span data-ttu-id="77bb1-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="77bb1-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="77bb1-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="77bb1-121">Syntax</span></span>            | [<span data-ttu-id="77bb1-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="77bb1-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="77bb1-123">實作</span><span class="sxs-lookup"><span data-stu-id="77bb1-123">Implementations</span></span>

-   [<span data-ttu-id="77bb1-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="77bb1-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="77bb1-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="77bb1-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="77bb1-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="77bb1-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="77bb1-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="77bb1-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="77bb1-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="77bb1-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="77bb1-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="77bb1-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="77bb1-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="77bb1-130">Windows 2000 Server</span></span>



| <span data-ttu-id="77bb1-131">進入</span><span class="sxs-lookup"><span data-stu-id="77bb1-131">Entry</span></span> | <span data-ttu-id="77bb1-132">值</span><span class="sxs-lookup"><span data-stu-id="77bb1-132">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="77bb1-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77bb1-133">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="77bb1-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77bb1-134">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="77bb1-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="77bb1-135">System-Only</span></span>            | <span data-ttu-id="77bb1-136">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-136">False</span></span>                                                            |
| <span data-ttu-id="77bb1-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77bb1-137">Is-Single-Valued</span></span>       | <span data-ttu-id="77bb1-138">對</span><span class="sxs-lookup"><span data-stu-id="77bb1-138">True</span></span>                                                             |
| <span data-ttu-id="77bb1-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77bb1-139">Is Indexed</span></span>             | <span data-ttu-id="77bb1-140">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-140">False</span></span>                                                            |
| <span data-ttu-id="77bb1-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77bb1-141">In Global Catalog</span></span>      | <span data-ttu-id="77bb1-142">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-142">False</span></span>                                                            |
| <span data-ttu-id="77bb1-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77bb1-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="77bb1-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77bb1-144">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="77bb1-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77bb1-145">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="77bb1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77bb1-146">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="77bb1-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77bb1-147">Search-Flags</span></span>           | <span data-ttu-id="77bb1-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77bb1-148">0x00000000</span></span>                                                       |
| <span data-ttu-id="77bb1-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77bb1-149">System-Flags</span></span>           | <span data-ttu-id="77bb1-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77bb1-150">0x00000010</span></span>                                                       |
| <span data-ttu-id="77bb1-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77bb1-151">Classes used in</span></span>        | [<span data-ttu-id="77bb1-152">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="77bb1-152">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="77bb1-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="77bb1-153">Windows Server 2003</span></span>



| <span data-ttu-id="77bb1-154">進入</span><span class="sxs-lookup"><span data-stu-id="77bb1-154">Entry</span></span> | <span data-ttu-id="77bb1-155">值</span><span class="sxs-lookup"><span data-stu-id="77bb1-155">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="77bb1-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77bb1-156">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="77bb1-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77bb1-157">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="77bb1-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="77bb1-158">System-Only</span></span>            | <span data-ttu-id="77bb1-159">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-159">False</span></span>                                                            |
| <span data-ttu-id="77bb1-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77bb1-160">Is-Single-Valued</span></span>       | <span data-ttu-id="77bb1-161">對</span><span class="sxs-lookup"><span data-stu-id="77bb1-161">True</span></span>                                                             |
| <span data-ttu-id="77bb1-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77bb1-162">Is Indexed</span></span>             | <span data-ttu-id="77bb1-163">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-163">False</span></span>                                                            |
| <span data-ttu-id="77bb1-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77bb1-164">In Global Catalog</span></span>      | <span data-ttu-id="77bb1-165">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-165">False</span></span>                                                            |
| <span data-ttu-id="77bb1-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77bb1-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="77bb1-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77bb1-167">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="77bb1-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77bb1-168">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="77bb1-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77bb1-169">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="77bb1-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77bb1-170">Search-Flags</span></span>           | <span data-ttu-id="77bb1-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77bb1-171">0x00000000</span></span>                                                       |
| <span data-ttu-id="77bb1-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77bb1-172">System-Flags</span></span>           | <span data-ttu-id="77bb1-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77bb1-173">0x00000010</span></span>                                                       |
| <span data-ttu-id="77bb1-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77bb1-174">Classes used in</span></span>        | [<span data-ttu-id="77bb1-175">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="77bb1-175">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="77bb1-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="77bb1-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="77bb1-177">進入</span><span class="sxs-lookup"><span data-stu-id="77bb1-177">Entry</span></span> | <span data-ttu-id="77bb1-178">值</span><span class="sxs-lookup"><span data-stu-id="77bb1-178">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="77bb1-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77bb1-179">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="77bb1-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77bb1-180">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="77bb1-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="77bb1-181">System-Only</span></span>            | <span data-ttu-id="77bb1-182">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-182">False</span></span>                                                            |
| <span data-ttu-id="77bb1-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77bb1-183">Is-Single-Valued</span></span>       | <span data-ttu-id="77bb1-184">對</span><span class="sxs-lookup"><span data-stu-id="77bb1-184">True</span></span>                                                             |
| <span data-ttu-id="77bb1-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77bb1-185">Is Indexed</span></span>             | <span data-ttu-id="77bb1-186">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-186">False</span></span>                                                            |
| <span data-ttu-id="77bb1-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77bb1-187">In Global Catalog</span></span>      | <span data-ttu-id="77bb1-188">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-188">False</span></span>                                                            |
| <span data-ttu-id="77bb1-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77bb1-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="77bb1-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77bb1-190">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="77bb1-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77bb1-191">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="77bb1-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77bb1-192">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="77bb1-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77bb1-193">Search-Flags</span></span>           | <span data-ttu-id="77bb1-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77bb1-194">0x00000000</span></span>                                                       |
| <span data-ttu-id="77bb1-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77bb1-195">System-Flags</span></span>           | <span data-ttu-id="77bb1-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77bb1-196">0x00000010</span></span>                                                       |
| <span data-ttu-id="77bb1-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77bb1-197">Classes used in</span></span>        | [<span data-ttu-id="77bb1-198">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="77bb1-198">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="77bb1-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77bb1-199">Windows Server 2008</span></span>



| <span data-ttu-id="77bb1-200">進入</span><span class="sxs-lookup"><span data-stu-id="77bb1-200">Entry</span></span> | <span data-ttu-id="77bb1-201">值</span><span class="sxs-lookup"><span data-stu-id="77bb1-201">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="77bb1-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77bb1-202">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="77bb1-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77bb1-203">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="77bb1-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="77bb1-204">System-Only</span></span>            | <span data-ttu-id="77bb1-205">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-205">False</span></span>                                                            |
| <span data-ttu-id="77bb1-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77bb1-206">Is-Single-Valued</span></span>       | <span data-ttu-id="77bb1-207">對</span><span class="sxs-lookup"><span data-stu-id="77bb1-207">True</span></span>                                                             |
| <span data-ttu-id="77bb1-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77bb1-208">Is Indexed</span></span>             | <span data-ttu-id="77bb1-209">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-209">False</span></span>                                                            |
| <span data-ttu-id="77bb1-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77bb1-210">In Global Catalog</span></span>      | <span data-ttu-id="77bb1-211">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-211">False</span></span>                                                            |
| <span data-ttu-id="77bb1-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77bb1-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="77bb1-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77bb1-213">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="77bb1-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77bb1-214">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="77bb1-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77bb1-215">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="77bb1-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77bb1-216">Search-Flags</span></span>           | <span data-ttu-id="77bb1-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77bb1-217">0x00000000</span></span>                                                       |
| <span data-ttu-id="77bb1-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77bb1-218">System-Flags</span></span>           | <span data-ttu-id="77bb1-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77bb1-219">0x00000010</span></span>                                                       |
| <span data-ttu-id="77bb1-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77bb1-220">Classes used in</span></span>        | [<span data-ttu-id="77bb1-221">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="77bb1-221">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="77bb1-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="77bb1-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="77bb1-223">進入</span><span class="sxs-lookup"><span data-stu-id="77bb1-223">Entry</span></span> | <span data-ttu-id="77bb1-224">值</span><span class="sxs-lookup"><span data-stu-id="77bb1-224">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="77bb1-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77bb1-225">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="77bb1-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77bb1-226">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="77bb1-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="77bb1-227">System-Only</span></span>            | <span data-ttu-id="77bb1-228">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-228">False</span></span>                                                            |
| <span data-ttu-id="77bb1-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77bb1-229">Is-Single-Valued</span></span>       | <span data-ttu-id="77bb1-230">對</span><span class="sxs-lookup"><span data-stu-id="77bb1-230">True</span></span>                                                             |
| <span data-ttu-id="77bb1-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77bb1-231">Is Indexed</span></span>             | <span data-ttu-id="77bb1-232">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-232">False</span></span>                                                            |
| <span data-ttu-id="77bb1-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77bb1-233">In Global Catalog</span></span>      | <span data-ttu-id="77bb1-234">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-234">False</span></span>                                                            |
| <span data-ttu-id="77bb1-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77bb1-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="77bb1-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77bb1-236">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="77bb1-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77bb1-237">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="77bb1-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77bb1-238">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="77bb1-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77bb1-239">Search-Flags</span></span>           | <span data-ttu-id="77bb1-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77bb1-240">0x00000000</span></span>                                                       |
| <span data-ttu-id="77bb1-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77bb1-241">System-Flags</span></span>           | <span data-ttu-id="77bb1-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77bb1-242">0x00000010</span></span>                                                       |
| <span data-ttu-id="77bb1-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77bb1-243">Classes used in</span></span>        | [<span data-ttu-id="77bb1-244">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="77bb1-244">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="77bb1-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77bb1-245">Windows Server 2012</span></span>



| <span data-ttu-id="77bb1-246">進入</span><span class="sxs-lookup"><span data-stu-id="77bb1-246">Entry</span></span> | <span data-ttu-id="77bb1-247">值</span><span class="sxs-lookup"><span data-stu-id="77bb1-247">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="77bb1-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="77bb1-248">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="77bb1-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77bb1-249">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="77bb1-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="77bb1-250">System-Only</span></span>            | <span data-ttu-id="77bb1-251">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-251">False</span></span>                                                            |
| <span data-ttu-id="77bb1-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="77bb1-252">Is-Single-Valued</span></span>       | <span data-ttu-id="77bb1-253">對</span><span class="sxs-lookup"><span data-stu-id="77bb1-253">True</span></span>                                                             |
| <span data-ttu-id="77bb1-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="77bb1-254">Is Indexed</span></span>             | <span data-ttu-id="77bb1-255">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-255">False</span></span>                                                            |
| <span data-ttu-id="77bb1-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="77bb1-256">In Global Catalog</span></span>      | <span data-ttu-id="77bb1-257">否</span><span class="sxs-lookup"><span data-stu-id="77bb1-257">False</span></span>                                                            |
| <span data-ttu-id="77bb1-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="77bb1-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="77bb1-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="77bb1-259">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="77bb1-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77bb1-260">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="77bb1-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77bb1-261">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="77bb1-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77bb1-262">Search-Flags</span></span>           | <span data-ttu-id="77bb1-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77bb1-263">0x00000000</span></span>                                                       |
| <span data-ttu-id="77bb1-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77bb1-264">System-Flags</span></span>           | <span data-ttu-id="77bb1-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77bb1-265">0x00000010</span></span>                                                       |
| <span data-ttu-id="77bb1-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="77bb1-266">Classes used in</span></span>        | [<span data-ttu-id="77bb1-267">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="77bb1-267">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





