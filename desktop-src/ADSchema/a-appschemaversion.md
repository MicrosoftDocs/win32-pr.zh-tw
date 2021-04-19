---
title: 應用程式架構版本屬性
description: 這個屬性會儲存類別存放區的架構版本。 它是用來在架構變更之間提供正確的行為。
ms.assetid: e8c2ab2b-1b7f-4d4f-b9ea-4116a8e30277
ms.tgt_platform: multiple
keywords:
- 應用程式架構版本屬性 AD 架構
- appSchemaVersion 屬性 AD 架構
topic_type:
- apiref
api_name:
- App-Schema-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09265299a676ef6b9d319153c7efdbe3929ee883
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970028"
---
# <a name="app-schema-version-attribute"></a><span data-ttu-id="45d64-106">應用程式架構版本屬性</span><span class="sxs-lookup"><span data-stu-id="45d64-106">App-Schema-Version attribute</span></span>

<span data-ttu-id="45d64-107">這個屬性會儲存類別存放區的架構版本。</span><span class="sxs-lookup"><span data-stu-id="45d64-107">This attribute stores the schema version of the class store.</span></span> <span data-ttu-id="45d64-108">它是用來在架構變更之間提供正確的行為。</span><span class="sxs-lookup"><span data-stu-id="45d64-108">It is used to provide correct behavior across schema changes.</span></span>



| <span data-ttu-id="45d64-109">進入</span><span class="sxs-lookup"><span data-stu-id="45d64-109">Entry</span></span> | <span data-ttu-id="45d64-110">值</span><span class="sxs-lookup"><span data-stu-id="45d64-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="45d64-111">CN</span><span class="sxs-lookup"><span data-stu-id="45d64-111">CN</span></span>                | <span data-ttu-id="45d64-112">應用程式架構版本</span><span class="sxs-lookup"><span data-stu-id="45d64-112">App-Schema-Version</span></span>                   |
| <span data-ttu-id="45d64-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="45d64-113">Ldap-Display-Name</span></span> | <span data-ttu-id="45d64-114">appSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="45d64-114">appSchemaVersion</span></span>                     |
| <span data-ttu-id="45d64-115">大小</span><span class="sxs-lookup"><span data-stu-id="45d64-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="45d64-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="45d64-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="45d64-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="45d64-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="45d64-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="45d64-118">Attribute-Id</span></span>      | <span data-ttu-id="45d64-119">1.2.840.113556.1.4.848</span><span class="sxs-lookup"><span data-stu-id="45d64-119">1.2.840.113556.1.4.848</span></span>               |
| <span data-ttu-id="45d64-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="45d64-120">System-Id-Guid</span></span>    | <span data-ttu-id="45d64-121">96a7dd65-9118-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="45d64-121">96a7dd65-9118-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="45d64-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="45d64-122">Syntax</span></span>            | [<span data-ttu-id="45d64-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="45d64-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="45d64-124">實作</span><span class="sxs-lookup"><span data-stu-id="45d64-124">Implementations</span></span>

-   [<span data-ttu-id="45d64-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="45d64-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="45d64-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="45d64-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="45d64-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="45d64-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="45d64-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="45d64-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="45d64-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="45d64-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="45d64-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="45d64-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="45d64-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="45d64-131">Windows 2000 Server</span></span>



| <span data-ttu-id="45d64-132">進入</span><span class="sxs-lookup"><span data-stu-id="45d64-132">Entry</span></span> | <span data-ttu-id="45d64-133">值</span><span class="sxs-lookup"><span data-stu-id="45d64-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="45d64-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="45d64-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="45d64-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45d64-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="45d64-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="45d64-136">System-Only</span></span>            | <span data-ttu-id="45d64-137">否</span><span class="sxs-lookup"><span data-stu-id="45d64-137">False</span></span>                                          |
| <span data-ttu-id="45d64-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="45d64-138">Is-Single-Valued</span></span>       | <span data-ttu-id="45d64-139">對</span><span class="sxs-lookup"><span data-stu-id="45d64-139">True</span></span>                                           |
| <span data-ttu-id="45d64-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="45d64-140">Is Indexed</span></span>             | <span data-ttu-id="45d64-141">否</span><span class="sxs-lookup"><span data-stu-id="45d64-141">False</span></span>                                          |
| <span data-ttu-id="45d64-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="45d64-142">In Global Catalog</span></span>      | <span data-ttu-id="45d64-143">否</span><span class="sxs-lookup"><span data-stu-id="45d64-143">False</span></span>                                          |
| <span data-ttu-id="45d64-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="45d64-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="45d64-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="45d64-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="45d64-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45d64-146">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="45d64-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45d64-147">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="45d64-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45d64-148">Search-Flags</span></span>           | <span data-ttu-id="45d64-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45d64-149">0x00000000</span></span>                                     |
| <span data-ttu-id="45d64-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45d64-150">System-Flags</span></span>           | <span data-ttu-id="45d64-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45d64-151">0x00000010</span></span>                                     |
| <span data-ttu-id="45d64-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="45d64-152">Classes used in</span></span>        | [<span data-ttu-id="45d64-153">**類別存放區**</span><span class="sxs-lookup"><span data-stu-id="45d64-153">**Class-Store**</span></span>](c-classstore.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="45d64-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="45d64-154">Windows Server 2003</span></span>



| <span data-ttu-id="45d64-155">進入</span><span class="sxs-lookup"><span data-stu-id="45d64-155">Entry</span></span> | <span data-ttu-id="45d64-156">值</span><span class="sxs-lookup"><span data-stu-id="45d64-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45d64-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="45d64-157">Link-Id</span></span>                | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45d64-158">MAPI-Id</span></span>                | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="45d64-159">System-Only</span></span>            | <span data-ttu-id="45d64-160">否</span><span class="sxs-lookup"><span data-stu-id="45d64-160">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="45d64-161">Is-Single-Valued</span></span>       | <span data-ttu-id="45d64-162">對</span><span class="sxs-lookup"><span data-stu-id="45d64-162">True</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="45d64-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="45d64-163">Is Indexed</span></span>             | <span data-ttu-id="45d64-164">否</span><span class="sxs-lookup"><span data-stu-id="45d64-164">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="45d64-165">In Global Catalog</span></span>      | <span data-ttu-id="45d64-166">否</span><span class="sxs-lookup"><span data-stu-id="45d64-166">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="45d64-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="45d64-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="45d64-168">O:BAG:BAD:S:</span></span>                                                                                                                                                                          |
| <span data-ttu-id="45d64-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45d64-169">Range-Lower</span></span>            | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45d64-170">Range-Upper</span></span>            | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45d64-171">Search-Flags</span></span>           | <span data-ttu-id="45d64-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45d64-172">0x00000000</span></span>                                                                                                                                                                            |
| <span data-ttu-id="45d64-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45d64-173">System-Flags</span></span>           | <span data-ttu-id="45d64-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45d64-174">0x00000010</span></span>                                                                                                                                                                            |
| <span data-ttu-id="45d64-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="45d64-175">Classes used in</span></span>        | [<span data-ttu-id="45d64-176">**應用程式版本**</span><span class="sxs-lookup"><span data-stu-id="45d64-176">**Application-Version**</span></span>](c-applicationversion.md)<br/> [<span data-ttu-id="45d64-177">**類別存放區**</span><span class="sxs-lookup"><span data-stu-id="45d64-177">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="45d64-178">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="45d64-178">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="45d64-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="45d64-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="45d64-180">進入</span><span class="sxs-lookup"><span data-stu-id="45d64-180">Entry</span></span> | <span data-ttu-id="45d64-181">值</span><span class="sxs-lookup"><span data-stu-id="45d64-181">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45d64-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="45d64-182">Link-Id</span></span>                | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45d64-183">MAPI-Id</span></span>                | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="45d64-184">System-Only</span></span>            | <span data-ttu-id="45d64-185">否</span><span class="sxs-lookup"><span data-stu-id="45d64-185">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="45d64-186">Is-Single-Valued</span></span>       | <span data-ttu-id="45d64-187">對</span><span class="sxs-lookup"><span data-stu-id="45d64-187">True</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="45d64-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="45d64-188">Is Indexed</span></span>             | <span data-ttu-id="45d64-189">否</span><span class="sxs-lookup"><span data-stu-id="45d64-189">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="45d64-190">In Global Catalog</span></span>      | <span data-ttu-id="45d64-191">否</span><span class="sxs-lookup"><span data-stu-id="45d64-191">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="45d64-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="45d64-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="45d64-193">O:BAG:BAD:S:</span></span>                                                                                                                                                                          |
| <span data-ttu-id="45d64-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45d64-194">Range-Lower</span></span>            | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45d64-195">Range-Upper</span></span>            | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45d64-196">Search-Flags</span></span>           | <span data-ttu-id="45d64-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45d64-197">0x00000000</span></span>                                                                                                                                                                            |
| <span data-ttu-id="45d64-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45d64-198">System-Flags</span></span>           | <span data-ttu-id="45d64-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45d64-199">0x00000010</span></span>                                                                                                                                                                            |
| <span data-ttu-id="45d64-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="45d64-200">Classes used in</span></span>        | [<span data-ttu-id="45d64-201">**應用程式版本**</span><span class="sxs-lookup"><span data-stu-id="45d64-201">**Application-Version**</span></span>](c-applicationversion.md)<br/> [<span data-ttu-id="45d64-202">**類別存放區**</span><span class="sxs-lookup"><span data-stu-id="45d64-202">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="45d64-203">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="45d64-203">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="45d64-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45d64-204">Windows Server 2008</span></span>



| <span data-ttu-id="45d64-205">進入</span><span class="sxs-lookup"><span data-stu-id="45d64-205">Entry</span></span> | <span data-ttu-id="45d64-206">值</span><span class="sxs-lookup"><span data-stu-id="45d64-206">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45d64-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="45d64-207">Link-Id</span></span>                | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45d64-208">MAPI-Id</span></span>                | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="45d64-209">System-Only</span></span>            | <span data-ttu-id="45d64-210">否</span><span class="sxs-lookup"><span data-stu-id="45d64-210">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="45d64-211">Is-Single-Valued</span></span>       | <span data-ttu-id="45d64-212">對</span><span class="sxs-lookup"><span data-stu-id="45d64-212">True</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="45d64-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="45d64-213">Is Indexed</span></span>             | <span data-ttu-id="45d64-214">否</span><span class="sxs-lookup"><span data-stu-id="45d64-214">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="45d64-215">In Global Catalog</span></span>      | <span data-ttu-id="45d64-216">否</span><span class="sxs-lookup"><span data-stu-id="45d64-216">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="45d64-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="45d64-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="45d64-218">O:BAG:BAD:S:</span></span>                                                                                                                                                                          |
| <span data-ttu-id="45d64-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45d64-219">Range-Lower</span></span>            | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45d64-220">Range-Upper</span></span>            | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45d64-221">Search-Flags</span></span>           | <span data-ttu-id="45d64-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45d64-222">0x00000000</span></span>                                                                                                                                                                            |
| <span data-ttu-id="45d64-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45d64-223">System-Flags</span></span>           | <span data-ttu-id="45d64-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45d64-224">0x00000010</span></span>                                                                                                                                                                            |
| <span data-ttu-id="45d64-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="45d64-225">Classes used in</span></span>        | [<span data-ttu-id="45d64-226">**應用程式版本**</span><span class="sxs-lookup"><span data-stu-id="45d64-226">**Application-Version**</span></span>](c-applicationversion.md)<br/> [<span data-ttu-id="45d64-227">**類別存放區**</span><span class="sxs-lookup"><span data-stu-id="45d64-227">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="45d64-228">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="45d64-228">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="45d64-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45d64-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="45d64-230">進入</span><span class="sxs-lookup"><span data-stu-id="45d64-230">Entry</span></span> | <span data-ttu-id="45d64-231">值</span><span class="sxs-lookup"><span data-stu-id="45d64-231">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45d64-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="45d64-232">Link-Id</span></span>                | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45d64-233">MAPI-Id</span></span>                | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="45d64-234">System-Only</span></span>            | <span data-ttu-id="45d64-235">否</span><span class="sxs-lookup"><span data-stu-id="45d64-235">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="45d64-236">Is-Single-Valued</span></span>       | <span data-ttu-id="45d64-237">對</span><span class="sxs-lookup"><span data-stu-id="45d64-237">True</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="45d64-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="45d64-238">Is Indexed</span></span>             | <span data-ttu-id="45d64-239">否</span><span class="sxs-lookup"><span data-stu-id="45d64-239">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="45d64-240">In Global Catalog</span></span>      | <span data-ttu-id="45d64-241">否</span><span class="sxs-lookup"><span data-stu-id="45d64-241">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="45d64-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="45d64-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="45d64-243">O:BAG:BAD:S:</span></span>                                                                                                                                                                          |
| <span data-ttu-id="45d64-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45d64-244">Range-Lower</span></span>            | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45d64-245">Range-Upper</span></span>            | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45d64-246">Search-Flags</span></span>           | <span data-ttu-id="45d64-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45d64-247">0x00000000</span></span>                                                                                                                                                                            |
| <span data-ttu-id="45d64-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45d64-248">System-Flags</span></span>           | <span data-ttu-id="45d64-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45d64-249">0x00000010</span></span>                                                                                                                                                                            |
| <span data-ttu-id="45d64-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="45d64-250">Classes used in</span></span>        | [<span data-ttu-id="45d64-251">**應用程式版本**</span><span class="sxs-lookup"><span data-stu-id="45d64-251">**Application-Version**</span></span>](c-applicationversion.md)<br/> [<span data-ttu-id="45d64-252">**類別存放區**</span><span class="sxs-lookup"><span data-stu-id="45d64-252">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="45d64-253">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="45d64-253">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="45d64-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45d64-254">Windows Server 2012</span></span>



| <span data-ttu-id="45d64-255">進入</span><span class="sxs-lookup"><span data-stu-id="45d64-255">Entry</span></span> | <span data-ttu-id="45d64-256">值</span><span class="sxs-lookup"><span data-stu-id="45d64-256">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45d64-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="45d64-257">Link-Id</span></span>                | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="45d64-258">MAPI-Id</span></span>                | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="45d64-259">System-Only</span></span>            | <span data-ttu-id="45d64-260">否</span><span class="sxs-lookup"><span data-stu-id="45d64-260">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="45d64-261">Is-Single-Valued</span></span>       | <span data-ttu-id="45d64-262">對</span><span class="sxs-lookup"><span data-stu-id="45d64-262">True</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="45d64-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="45d64-263">Is Indexed</span></span>             | <span data-ttu-id="45d64-264">否</span><span class="sxs-lookup"><span data-stu-id="45d64-264">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="45d64-265">In Global Catalog</span></span>      | <span data-ttu-id="45d64-266">否</span><span class="sxs-lookup"><span data-stu-id="45d64-266">False</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="45d64-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="45d64-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="45d64-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="45d64-268">O:BAG:BAD:S:</span></span>                                                                                                                                                                          |
| <span data-ttu-id="45d64-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="45d64-269">Range-Lower</span></span>            | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="45d64-270">Range-Upper</span></span>            | \-                                                                                                                                                                                    |
| <span data-ttu-id="45d64-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="45d64-271">Search-Flags</span></span>           | <span data-ttu-id="45d64-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="45d64-272">0x00000000</span></span>                                                                                                                                                                            |
| <span data-ttu-id="45d64-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="45d64-273">System-Flags</span></span>           | <span data-ttu-id="45d64-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="45d64-274">0x00000010</span></span>                                                                                                                                                                            |
| <span data-ttu-id="45d64-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="45d64-275">Classes used in</span></span>        | [<span data-ttu-id="45d64-276">**應用程式版本**</span><span class="sxs-lookup"><span data-stu-id="45d64-276">**Application-Version**</span></span>](c-applicationversion.md)<br/> [<span data-ttu-id="45d64-277">**類別存放區**</span><span class="sxs-lookup"><span data-stu-id="45d64-277">**Class-Store**</span></span>](c-classstore.md)<br/> [<span data-ttu-id="45d64-278">**服務-連接點**</span><span class="sxs-lookup"><span data-stu-id="45d64-278">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



 

 





