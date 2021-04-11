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
# <a name="install-ui-level-attribute"></a><span data-ttu-id="7b080-105">安裝-Ui 層級屬性</span><span class="sxs-lookup"><span data-stu-id="7b080-105">Install-Ui-Level attribute</span></span>

<span data-ttu-id="7b080-106">此屬性包含用於使用者介面之安裝 (層級) 類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="7b080-106">This attribute contains information for the type (level) of installation that is used for the user interface.</span></span> <span data-ttu-id="7b080-107">可能的安裝層級如下所示： 2 INSTALLUILEVEL \_ 無無訊息安裝 (無訊息安裝) 3 INSTALLUILEVEL \_ 基本 (簡單安裝，錯誤處理) 4 INSTALLUILEVEL \_ 減少 (撰寫的 ui \_</span><span class="sxs-lookup"><span data-stu-id="7b080-107">Possible installation levels are as follows: 2 INSTALLUILEVEL\_NONE (silent installation) 3 INSTALLUILEVEL\_BASIC (simple installation with error handling) 4 INSTALLUILEVEL\_REDUCED (authored UI, wizard dialog boxes suppressed) 5 INSTALLUILEVEL\_FULL (authored UI with wizards, progress, errors)</span></span>



| <span data-ttu-id="7b080-108">進入</span><span class="sxs-lookup"><span data-stu-id="7b080-108">Entry</span></span> | <span data-ttu-id="7b080-109">值</span><span class="sxs-lookup"><span data-stu-id="7b080-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7b080-110">CN</span><span class="sxs-lookup"><span data-stu-id="7b080-110">CN</span></span>                | <span data-ttu-id="7b080-111">安裝-Ui 層級</span><span class="sxs-lookup"><span data-stu-id="7b080-111">Install-Ui-Level</span></span>                     |
| <span data-ttu-id="7b080-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7b080-112">Ldap-Display-Name</span></span> | <span data-ttu-id="7b080-113">installUiLevel</span><span class="sxs-lookup"><span data-stu-id="7b080-113">installUiLevel</span></span>                       |
| <span data-ttu-id="7b080-114">大小</span><span class="sxs-lookup"><span data-stu-id="7b080-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="7b080-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7b080-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7b080-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7b080-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7b080-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7b080-117">Attribute-Id</span></span>      | <span data-ttu-id="7b080-118">1.2.840.113556.1.4.847</span><span class="sxs-lookup"><span data-stu-id="7b080-118">1.2.840.113556.1.4.847</span></span>               |
| <span data-ttu-id="7b080-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7b080-119">System-Id-Guid</span></span>    | <span data-ttu-id="7b080-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7b080-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="7b080-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b080-121">Syntax</span></span>            | [<span data-ttu-id="7b080-122">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="7b080-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="7b080-123">實作</span><span class="sxs-lookup"><span data-stu-id="7b080-123">Implementations</span></span>

-   [<span data-ttu-id="7b080-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7b080-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7b080-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7b080-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7b080-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7b080-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7b080-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7b080-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7b080-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7b080-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7b080-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7b080-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7b080-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7b080-130">Windows 2000 Server</span></span>



| <span data-ttu-id="7b080-131">進入</span><span class="sxs-lookup"><span data-stu-id="7b080-131">Entry</span></span> | <span data-ttu-id="7b080-132">值</span><span class="sxs-lookup"><span data-stu-id="7b080-132">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="7b080-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b080-133">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7b080-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b080-134">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7b080-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b080-135">System-Only</span></span>            | <span data-ttu-id="7b080-136">否</span><span class="sxs-lookup"><span data-stu-id="7b080-136">False</span></span>                                                            |
| <span data-ttu-id="7b080-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b080-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7b080-138">對</span><span class="sxs-lookup"><span data-stu-id="7b080-138">True</span></span>                                                             |
| <span data-ttu-id="7b080-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b080-139">Is Indexed</span></span>             | <span data-ttu-id="7b080-140">否</span><span class="sxs-lookup"><span data-stu-id="7b080-140">False</span></span>                                                            |
| <span data-ttu-id="7b080-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b080-141">In Global Catalog</span></span>      | <span data-ttu-id="7b080-142">否</span><span class="sxs-lookup"><span data-stu-id="7b080-142">False</span></span>                                                            |
| <span data-ttu-id="7b080-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b080-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b080-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b080-144">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="7b080-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b080-145">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="7b080-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b080-146">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="7b080-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b080-147">Search-Flags</span></span>           | <span data-ttu-id="7b080-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b080-148">0x00000000</span></span>                                                       |
| <span data-ttu-id="7b080-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b080-149">System-Flags</span></span>           | <span data-ttu-id="7b080-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b080-150">0x00000010</span></span>                                                       |
| <span data-ttu-id="7b080-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b080-151">Classes used in</span></span>        | [<span data-ttu-id="7b080-152">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="7b080-152">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7b080-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7b080-153">Windows Server 2003</span></span>



| <span data-ttu-id="7b080-154">進入</span><span class="sxs-lookup"><span data-stu-id="7b080-154">Entry</span></span> | <span data-ttu-id="7b080-155">值</span><span class="sxs-lookup"><span data-stu-id="7b080-155">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="7b080-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b080-156">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7b080-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b080-157">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7b080-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b080-158">System-Only</span></span>            | <span data-ttu-id="7b080-159">否</span><span class="sxs-lookup"><span data-stu-id="7b080-159">False</span></span>                                                            |
| <span data-ttu-id="7b080-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b080-160">Is-Single-Valued</span></span>       | <span data-ttu-id="7b080-161">對</span><span class="sxs-lookup"><span data-stu-id="7b080-161">True</span></span>                                                             |
| <span data-ttu-id="7b080-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b080-162">Is Indexed</span></span>             | <span data-ttu-id="7b080-163">否</span><span class="sxs-lookup"><span data-stu-id="7b080-163">False</span></span>                                                            |
| <span data-ttu-id="7b080-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b080-164">In Global Catalog</span></span>      | <span data-ttu-id="7b080-165">否</span><span class="sxs-lookup"><span data-stu-id="7b080-165">False</span></span>                                                            |
| <span data-ttu-id="7b080-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b080-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b080-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b080-167">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="7b080-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b080-168">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="7b080-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b080-169">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="7b080-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b080-170">Search-Flags</span></span>           | <span data-ttu-id="7b080-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b080-171">0x00000000</span></span>                                                       |
| <span data-ttu-id="7b080-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b080-172">System-Flags</span></span>           | <span data-ttu-id="7b080-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b080-173">0x00000010</span></span>                                                       |
| <span data-ttu-id="7b080-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b080-174">Classes used in</span></span>        | [<span data-ttu-id="7b080-175">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="7b080-175">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7b080-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7b080-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7b080-177">進入</span><span class="sxs-lookup"><span data-stu-id="7b080-177">Entry</span></span> | <span data-ttu-id="7b080-178">值</span><span class="sxs-lookup"><span data-stu-id="7b080-178">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="7b080-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b080-179">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7b080-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b080-180">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7b080-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b080-181">System-Only</span></span>            | <span data-ttu-id="7b080-182">否</span><span class="sxs-lookup"><span data-stu-id="7b080-182">False</span></span>                                                            |
| <span data-ttu-id="7b080-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b080-183">Is-Single-Valued</span></span>       | <span data-ttu-id="7b080-184">對</span><span class="sxs-lookup"><span data-stu-id="7b080-184">True</span></span>                                                             |
| <span data-ttu-id="7b080-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b080-185">Is Indexed</span></span>             | <span data-ttu-id="7b080-186">否</span><span class="sxs-lookup"><span data-stu-id="7b080-186">False</span></span>                                                            |
| <span data-ttu-id="7b080-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b080-187">In Global Catalog</span></span>      | <span data-ttu-id="7b080-188">否</span><span class="sxs-lookup"><span data-stu-id="7b080-188">False</span></span>                                                            |
| <span data-ttu-id="7b080-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b080-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b080-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b080-190">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="7b080-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b080-191">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="7b080-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b080-192">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="7b080-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b080-193">Search-Flags</span></span>           | <span data-ttu-id="7b080-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b080-194">0x00000000</span></span>                                                       |
| <span data-ttu-id="7b080-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b080-195">System-Flags</span></span>           | <span data-ttu-id="7b080-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b080-196">0x00000010</span></span>                                                       |
| <span data-ttu-id="7b080-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b080-197">Classes used in</span></span>        | [<span data-ttu-id="7b080-198">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="7b080-198">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7b080-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b080-199">Windows Server 2008</span></span>



| <span data-ttu-id="7b080-200">進入</span><span class="sxs-lookup"><span data-stu-id="7b080-200">Entry</span></span> | <span data-ttu-id="7b080-201">值</span><span class="sxs-lookup"><span data-stu-id="7b080-201">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="7b080-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b080-202">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7b080-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b080-203">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7b080-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b080-204">System-Only</span></span>            | <span data-ttu-id="7b080-205">否</span><span class="sxs-lookup"><span data-stu-id="7b080-205">False</span></span>                                                            |
| <span data-ttu-id="7b080-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b080-206">Is-Single-Valued</span></span>       | <span data-ttu-id="7b080-207">對</span><span class="sxs-lookup"><span data-stu-id="7b080-207">True</span></span>                                                             |
| <span data-ttu-id="7b080-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b080-208">Is Indexed</span></span>             | <span data-ttu-id="7b080-209">否</span><span class="sxs-lookup"><span data-stu-id="7b080-209">False</span></span>                                                            |
| <span data-ttu-id="7b080-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b080-210">In Global Catalog</span></span>      | <span data-ttu-id="7b080-211">否</span><span class="sxs-lookup"><span data-stu-id="7b080-211">False</span></span>                                                            |
| <span data-ttu-id="7b080-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b080-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b080-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b080-213">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="7b080-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b080-214">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="7b080-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b080-215">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="7b080-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b080-216">Search-Flags</span></span>           | <span data-ttu-id="7b080-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b080-217">0x00000000</span></span>                                                       |
| <span data-ttu-id="7b080-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b080-218">System-Flags</span></span>           | <span data-ttu-id="7b080-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b080-219">0x00000010</span></span>                                                       |
| <span data-ttu-id="7b080-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b080-220">Classes used in</span></span>        | [<span data-ttu-id="7b080-221">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="7b080-221">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7b080-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7b080-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7b080-223">進入</span><span class="sxs-lookup"><span data-stu-id="7b080-223">Entry</span></span> | <span data-ttu-id="7b080-224">值</span><span class="sxs-lookup"><span data-stu-id="7b080-224">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="7b080-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b080-225">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7b080-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b080-226">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7b080-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b080-227">System-Only</span></span>            | <span data-ttu-id="7b080-228">否</span><span class="sxs-lookup"><span data-stu-id="7b080-228">False</span></span>                                                            |
| <span data-ttu-id="7b080-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b080-229">Is-Single-Valued</span></span>       | <span data-ttu-id="7b080-230">對</span><span class="sxs-lookup"><span data-stu-id="7b080-230">True</span></span>                                                             |
| <span data-ttu-id="7b080-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b080-231">Is Indexed</span></span>             | <span data-ttu-id="7b080-232">否</span><span class="sxs-lookup"><span data-stu-id="7b080-232">False</span></span>                                                            |
| <span data-ttu-id="7b080-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b080-233">In Global Catalog</span></span>      | <span data-ttu-id="7b080-234">否</span><span class="sxs-lookup"><span data-stu-id="7b080-234">False</span></span>                                                            |
| <span data-ttu-id="7b080-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b080-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b080-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b080-236">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="7b080-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b080-237">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="7b080-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b080-238">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="7b080-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b080-239">Search-Flags</span></span>           | <span data-ttu-id="7b080-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b080-240">0x00000000</span></span>                                                       |
| <span data-ttu-id="7b080-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b080-241">System-Flags</span></span>           | <span data-ttu-id="7b080-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b080-242">0x00000010</span></span>                                                       |
| <span data-ttu-id="7b080-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b080-243">Classes used in</span></span>        | [<span data-ttu-id="7b080-244">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="7b080-244">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7b080-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b080-245">Windows Server 2012</span></span>



| <span data-ttu-id="7b080-246">進入</span><span class="sxs-lookup"><span data-stu-id="7b080-246">Entry</span></span> | <span data-ttu-id="7b080-247">值</span><span class="sxs-lookup"><span data-stu-id="7b080-247">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="7b080-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7b080-248">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7b080-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7b080-249">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7b080-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="7b080-250">System-Only</span></span>            | <span data-ttu-id="7b080-251">否</span><span class="sxs-lookup"><span data-stu-id="7b080-251">False</span></span>                                                            |
| <span data-ttu-id="7b080-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7b080-252">Is-Single-Valued</span></span>       | <span data-ttu-id="7b080-253">對</span><span class="sxs-lookup"><span data-stu-id="7b080-253">True</span></span>                                                             |
| <span data-ttu-id="7b080-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7b080-254">Is Indexed</span></span>             | <span data-ttu-id="7b080-255">否</span><span class="sxs-lookup"><span data-stu-id="7b080-255">False</span></span>                                                            |
| <span data-ttu-id="7b080-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7b080-256">In Global Catalog</span></span>      | <span data-ttu-id="7b080-257">否</span><span class="sxs-lookup"><span data-stu-id="7b080-257">False</span></span>                                                            |
| <span data-ttu-id="7b080-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7b080-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="7b080-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7b080-259">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="7b080-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7b080-260">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="7b080-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7b080-261">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="7b080-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7b080-262">Search-Flags</span></span>           | <span data-ttu-id="7b080-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7b080-263">0x00000000</span></span>                                                       |
| <span data-ttu-id="7b080-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7b080-264">System-Flags</span></span>           | <span data-ttu-id="7b080-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7b080-265">0x00000010</span></span>                                                       |
| <span data-ttu-id="7b080-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7b080-266">Classes used in</span></span>        | [<span data-ttu-id="7b080-267">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="7b080-267">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





