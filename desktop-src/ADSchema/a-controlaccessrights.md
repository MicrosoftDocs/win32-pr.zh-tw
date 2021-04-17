---
title: 控制項存取權屬性
description: 由 DS 安全性用來判斷哪些使用者可以在主機物件上執行特定作業。
ms.assetid: 5e717160-519c-4e5a-b18f-05ee767a66a3
ms.tgt_platform: multiple
keywords:
- 控制項存取權屬性 AD 架構
- controlAccessRights 屬性 AD 架構
topic_type:
- apiref
api_name:
- Control-Access-Rights
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3ee9075cfaf4c5bbfbf17e8e2cfef6166be032
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467376"
---
# <a name="control-access-rights-attribute"></a><span data-ttu-id="75e2e-105">控制項存取權屬性</span><span class="sxs-lookup"><span data-stu-id="75e2e-105">Control-Access-Rights attribute</span></span>

<span data-ttu-id="75e2e-106">由 DS 安全性用來判斷哪些使用者可以在主機物件上執行特定作業。</span><span class="sxs-lookup"><span data-stu-id="75e2e-106">Used by DS Security to determine which users can perform specific operations on the host object.</span></span>



| <span data-ttu-id="75e2e-107">進入</span><span class="sxs-lookup"><span data-stu-id="75e2e-107">Entry</span></span> | <span data-ttu-id="75e2e-108">值</span><span class="sxs-lookup"><span data-stu-id="75e2e-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="75e2e-109">CN</span><span class="sxs-lookup"><span data-stu-id="75e2e-109">CN</span></span>                | <span data-ttu-id="75e2e-110">控制存取權</span><span class="sxs-lookup"><span data-stu-id="75e2e-110">Control-Access-Rights</span></span>                                 |
| <span data-ttu-id="75e2e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="75e2e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="75e2e-112">controlAccessRights</span><span class="sxs-lookup"><span data-stu-id="75e2e-112">controlAccessRights</span></span>                                   |
| <span data-ttu-id="75e2e-113">大小</span><span class="sxs-lookup"><span data-stu-id="75e2e-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="75e2e-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="75e2e-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="75e2e-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="75e2e-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="75e2e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="75e2e-116">Attribute-Id</span></span>      | <span data-ttu-id="75e2e-117">1.2.840.113556.1.4.200</span><span class="sxs-lookup"><span data-stu-id="75e2e-117">1.2.840.113556.1.4.200</span></span>                                |
| <span data-ttu-id="75e2e-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="75e2e-118">System-Id-Guid</span></span>    | <span data-ttu-id="75e2e-119">6da8a4fc-0e52-11d0-a286-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="75e2e-119">6da8a4fc-0e52-11d0-a286-00aa003049e2</span></span>                  |
| <span data-ttu-id="75e2e-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="75e2e-120">Syntax</span></span>            | [<span data-ttu-id="75e2e-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="75e2e-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="75e2e-122">實作</span><span class="sxs-lookup"><span data-stu-id="75e2e-122">Implementations</span></span>

-   [<span data-ttu-id="75e2e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="75e2e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="75e2e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="75e2e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="75e2e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="75e2e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="75e2e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="75e2e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="75e2e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="75e2e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="75e2e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="75e2e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="75e2e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="75e2e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="75e2e-130">進入</span><span class="sxs-lookup"><span data-stu-id="75e2e-130">Entry</span></span> | <span data-ttu-id="75e2e-131">值</span><span class="sxs-lookup"><span data-stu-id="75e2e-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75e2e-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75e2e-132">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="75e2e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75e2e-133">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="75e2e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="75e2e-134">System-Only</span></span>            | <span data-ttu-id="75e2e-135">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-135">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75e2e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="75e2e-137">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-137">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75e2e-138">Is Indexed</span></span>             | <span data-ttu-id="75e2e-139">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-139">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75e2e-140">In Global Catalog</span></span>      | <span data-ttu-id="75e2e-141">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-141">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75e2e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="75e2e-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75e2e-143">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="75e2e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75e2e-144">Range-Lower</span></span>            | <span data-ttu-id="75e2e-145">16</span><span class="sxs-lookup"><span data-stu-id="75e2e-145">16</span></span>                                                                                                                 |
| <span data-ttu-id="75e2e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75e2e-146">Range-Upper</span></span>            | <span data-ttu-id="75e2e-147">16</span><span class="sxs-lookup"><span data-stu-id="75e2e-147">16</span></span>                                                                                                                 |
| <span data-ttu-id="75e2e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75e2e-148">Search-Flags</span></span>           | <span data-ttu-id="75e2e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75e2e-149">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="75e2e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75e2e-150">System-Flags</span></span>           | <span data-ttu-id="75e2e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75e2e-151">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="75e2e-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75e2e-152">Classes used in</span></span>        | [<span data-ttu-id="75e2e-153">**Group**</span><span class="sxs-lookup"><span data-stu-id="75e2e-153">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="75e2e-154">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="75e2e-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="75e2e-155">**User**</span><span class="sxs-lookup"><span data-stu-id="75e2e-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="75e2e-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75e2e-156">Windows Server 2003</span></span>



| <span data-ttu-id="75e2e-157">進入</span><span class="sxs-lookup"><span data-stu-id="75e2e-157">Entry</span></span> | <span data-ttu-id="75e2e-158">值</span><span class="sxs-lookup"><span data-stu-id="75e2e-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75e2e-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75e2e-159">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="75e2e-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75e2e-160">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="75e2e-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="75e2e-161">System-Only</span></span>            | <span data-ttu-id="75e2e-162">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-162">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75e2e-163">Is-Single-Valued</span></span>       | <span data-ttu-id="75e2e-164">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-164">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75e2e-165">Is Indexed</span></span>             | <span data-ttu-id="75e2e-166">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-166">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75e2e-167">In Global Catalog</span></span>      | <span data-ttu-id="75e2e-168">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-168">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75e2e-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="75e2e-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75e2e-170">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="75e2e-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75e2e-171">Range-Lower</span></span>            | <span data-ttu-id="75e2e-172">16</span><span class="sxs-lookup"><span data-stu-id="75e2e-172">16</span></span>                                                                                                                 |
| <span data-ttu-id="75e2e-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75e2e-173">Range-Upper</span></span>            | <span data-ttu-id="75e2e-174">16</span><span class="sxs-lookup"><span data-stu-id="75e2e-174">16</span></span>                                                                                                                 |
| <span data-ttu-id="75e2e-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75e2e-175">Search-Flags</span></span>           | <span data-ttu-id="75e2e-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75e2e-176">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="75e2e-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75e2e-177">System-Flags</span></span>           | <span data-ttu-id="75e2e-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75e2e-178">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="75e2e-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75e2e-179">Classes used in</span></span>        | [<span data-ttu-id="75e2e-180">**Group**</span><span class="sxs-lookup"><span data-stu-id="75e2e-180">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="75e2e-181">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="75e2e-181">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="75e2e-182">**User**</span><span class="sxs-lookup"><span data-stu-id="75e2e-182">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="75e2e-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="75e2e-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="75e2e-184">進入</span><span class="sxs-lookup"><span data-stu-id="75e2e-184">Entry</span></span> | <span data-ttu-id="75e2e-185">值</span><span class="sxs-lookup"><span data-stu-id="75e2e-185">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75e2e-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75e2e-186">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="75e2e-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75e2e-187">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="75e2e-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="75e2e-188">System-Only</span></span>            | <span data-ttu-id="75e2e-189">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-189">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75e2e-190">Is-Single-Valued</span></span>       | <span data-ttu-id="75e2e-191">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-191">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75e2e-192">Is Indexed</span></span>             | <span data-ttu-id="75e2e-193">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-193">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75e2e-194">In Global Catalog</span></span>      | <span data-ttu-id="75e2e-195">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-195">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75e2e-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="75e2e-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75e2e-197">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="75e2e-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75e2e-198">Range-Lower</span></span>            | <span data-ttu-id="75e2e-199">16</span><span class="sxs-lookup"><span data-stu-id="75e2e-199">16</span></span>                                                                                                                 |
| <span data-ttu-id="75e2e-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75e2e-200">Range-Upper</span></span>            | <span data-ttu-id="75e2e-201">16</span><span class="sxs-lookup"><span data-stu-id="75e2e-201">16</span></span>                                                                                                                 |
| <span data-ttu-id="75e2e-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75e2e-202">Search-Flags</span></span>           | <span data-ttu-id="75e2e-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75e2e-203">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="75e2e-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75e2e-204">System-Flags</span></span>           | <span data-ttu-id="75e2e-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75e2e-205">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="75e2e-206">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75e2e-206">Classes used in</span></span>        | [<span data-ttu-id="75e2e-207">**Group**</span><span class="sxs-lookup"><span data-stu-id="75e2e-207">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="75e2e-208">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="75e2e-208">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="75e2e-209">**User**</span><span class="sxs-lookup"><span data-stu-id="75e2e-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="75e2e-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75e2e-210">Windows Server 2008</span></span>



| <span data-ttu-id="75e2e-211">進入</span><span class="sxs-lookup"><span data-stu-id="75e2e-211">Entry</span></span> | <span data-ttu-id="75e2e-212">值</span><span class="sxs-lookup"><span data-stu-id="75e2e-212">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75e2e-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75e2e-213">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="75e2e-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75e2e-214">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="75e2e-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="75e2e-215">System-Only</span></span>            | <span data-ttu-id="75e2e-216">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-216">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75e2e-217">Is-Single-Valued</span></span>       | <span data-ttu-id="75e2e-218">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-218">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75e2e-219">Is Indexed</span></span>             | <span data-ttu-id="75e2e-220">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-220">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75e2e-221">In Global Catalog</span></span>      | <span data-ttu-id="75e2e-222">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-222">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75e2e-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="75e2e-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75e2e-224">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="75e2e-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75e2e-225">Range-Lower</span></span>            | <span data-ttu-id="75e2e-226">16</span><span class="sxs-lookup"><span data-stu-id="75e2e-226">16</span></span>                                                                                                                 |
| <span data-ttu-id="75e2e-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75e2e-227">Range-Upper</span></span>            | <span data-ttu-id="75e2e-228">16</span><span class="sxs-lookup"><span data-stu-id="75e2e-228">16</span></span>                                                                                                                 |
| <span data-ttu-id="75e2e-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75e2e-229">Search-Flags</span></span>           | <span data-ttu-id="75e2e-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75e2e-230">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="75e2e-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75e2e-231">System-Flags</span></span>           | <span data-ttu-id="75e2e-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75e2e-232">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="75e2e-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75e2e-233">Classes used in</span></span>        | [<span data-ttu-id="75e2e-234">**Group**</span><span class="sxs-lookup"><span data-stu-id="75e2e-234">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="75e2e-235">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="75e2e-235">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="75e2e-236">**User**</span><span class="sxs-lookup"><span data-stu-id="75e2e-236">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="75e2e-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="75e2e-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="75e2e-238">進入</span><span class="sxs-lookup"><span data-stu-id="75e2e-238">Entry</span></span> | <span data-ttu-id="75e2e-239">值</span><span class="sxs-lookup"><span data-stu-id="75e2e-239">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75e2e-240">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75e2e-240">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="75e2e-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75e2e-241">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="75e2e-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="75e2e-242">System-Only</span></span>            | <span data-ttu-id="75e2e-243">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-243">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-244">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75e2e-244">Is-Single-Valued</span></span>       | <span data-ttu-id="75e2e-245">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-245">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-246">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75e2e-246">Is Indexed</span></span>             | <span data-ttu-id="75e2e-247">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-247">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-248">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75e2e-248">In Global Catalog</span></span>      | <span data-ttu-id="75e2e-249">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-249">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-250">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75e2e-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="75e2e-251">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75e2e-251">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="75e2e-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75e2e-252">Range-Lower</span></span>            | <span data-ttu-id="75e2e-253">16</span><span class="sxs-lookup"><span data-stu-id="75e2e-253">16</span></span>                                                                                                                 |
| <span data-ttu-id="75e2e-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75e2e-254">Range-Upper</span></span>            | <span data-ttu-id="75e2e-255">16</span><span class="sxs-lookup"><span data-stu-id="75e2e-255">16</span></span>                                                                                                                 |
| <span data-ttu-id="75e2e-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75e2e-256">Search-Flags</span></span>           | <span data-ttu-id="75e2e-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75e2e-257">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="75e2e-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75e2e-258">System-Flags</span></span>           | <span data-ttu-id="75e2e-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75e2e-259">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="75e2e-260">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75e2e-260">Classes used in</span></span>        | [<span data-ttu-id="75e2e-261">**Group**</span><span class="sxs-lookup"><span data-stu-id="75e2e-261">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="75e2e-262">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="75e2e-262">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="75e2e-263">**User**</span><span class="sxs-lookup"><span data-stu-id="75e2e-263">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="75e2e-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="75e2e-264">Windows Server 2012</span></span>



| <span data-ttu-id="75e2e-265">進入</span><span class="sxs-lookup"><span data-stu-id="75e2e-265">Entry</span></span> | <span data-ttu-id="75e2e-266">值</span><span class="sxs-lookup"><span data-stu-id="75e2e-266">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75e2e-267">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75e2e-267">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="75e2e-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75e2e-268">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="75e2e-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="75e2e-269">System-Only</span></span>            | <span data-ttu-id="75e2e-270">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-270">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-271">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75e2e-271">Is-Single-Valued</span></span>       | <span data-ttu-id="75e2e-272">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-272">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-273">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75e2e-273">Is Indexed</span></span>             | <span data-ttu-id="75e2e-274">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-274">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-275">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75e2e-275">In Global Catalog</span></span>      | <span data-ttu-id="75e2e-276">否</span><span class="sxs-lookup"><span data-stu-id="75e2e-276">False</span></span>                                                                                                              |
| <span data-ttu-id="75e2e-277">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75e2e-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="75e2e-278">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75e2e-278">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="75e2e-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75e2e-279">Range-Lower</span></span>            | <span data-ttu-id="75e2e-280">16</span><span class="sxs-lookup"><span data-stu-id="75e2e-280">16</span></span>                                                                                                                 |
| <span data-ttu-id="75e2e-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75e2e-281">Range-Upper</span></span>            | <span data-ttu-id="75e2e-282">16</span><span class="sxs-lookup"><span data-stu-id="75e2e-282">16</span></span>                                                                                                                 |
| <span data-ttu-id="75e2e-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75e2e-283">Search-Flags</span></span>           | <span data-ttu-id="75e2e-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75e2e-284">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="75e2e-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75e2e-285">System-Flags</span></span>           | <span data-ttu-id="75e2e-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75e2e-286">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="75e2e-287">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75e2e-287">Classes used in</span></span>        | [<span data-ttu-id="75e2e-288">**Group**</span><span class="sxs-lookup"><span data-stu-id="75e2e-288">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="75e2e-289">**Sam-網域**</span><span class="sxs-lookup"><span data-stu-id="75e2e-289">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="75e2e-290">**User**</span><span class="sxs-lookup"><span data-stu-id="75e2e-290">**User**</span></span>](c-user.md)<br/> |



 

 





