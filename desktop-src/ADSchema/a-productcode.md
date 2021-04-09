---
title: Product-Code 屬性
description: 此屬性包含特定產品版本之應用程式的唯一識別碼，以字串 GUID 表示，例如 \ 0034;12345678-1234-1234-1234-123456789012 \ 0034;。
ms.assetid: 1fb50a4c-1a6a-4231-a6b2-92f6bc4a1ead
ms.tgt_platform: multiple
keywords:
- Product-Code 屬性 AD 架構
- productCode 屬性 AD 架構
topic_type:
- apiref
api_name:
- Product-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51dc874552fc819de4f9c58b23809b9f5662ee6e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935228"
---
# <a name="product-code-attribute"></a><span data-ttu-id="bf31d-105">Product-Code 屬性</span><span class="sxs-lookup"><span data-stu-id="bf31d-105">Product-Code attribute</span></span>

<span data-ttu-id="bf31d-106">此屬性包含特定產品版本之應用程式的唯一識別碼（以字串 GUID 表示），例如 " {12345678-1234-1234-1234-123456789012} "。</span><span class="sxs-lookup"><span data-stu-id="bf31d-106">This attribute contains a unique identifier for an application for a particular product release, represented as a string GUID, for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="bf31d-107">此 GUID 中使用的字母必須為大寫。</span><span class="sxs-lookup"><span data-stu-id="bf31d-107">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="bf31d-108">此識別碼必須因不同版本和語言而有所不同。</span><span class="sxs-lookup"><span data-stu-id="bf31d-108">This ID must vary for different versions and languages.</span></span>



| <span data-ttu-id="bf31d-109">進入</span><span class="sxs-lookup"><span data-stu-id="bf31d-109">Entry</span></span> | <span data-ttu-id="bf31d-110">值</span><span class="sxs-lookup"><span data-stu-id="bf31d-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="bf31d-111">CN</span><span class="sxs-lookup"><span data-stu-id="bf31d-111">CN</span></span>                | <span data-ttu-id="bf31d-112">Product-Code</span><span class="sxs-lookup"><span data-stu-id="bf31d-112">Product-Code</span></span>                                          |
| <span data-ttu-id="bf31d-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="bf31d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="bf31d-114">productCode</span><span class="sxs-lookup"><span data-stu-id="bf31d-114">productCode</span></span>                                           |
| <span data-ttu-id="bf31d-115">大小</span><span class="sxs-lookup"><span data-stu-id="bf31d-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="bf31d-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="bf31d-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="bf31d-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="bf31d-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="bf31d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bf31d-118">Attribute-Id</span></span>      | <span data-ttu-id="bf31d-119">1.2.840.113556.1.4.818</span><span class="sxs-lookup"><span data-stu-id="bf31d-119">1.2.840.113556.1.4.818</span></span>                                |
| <span data-ttu-id="bf31d-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="bf31d-120">System-Id-Guid</span></span>    | <span data-ttu-id="bf31d-121">d9e18317-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="bf31d-121">d9e18317-8939-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="bf31d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf31d-122">Syntax</span></span>            | [<span data-ttu-id="bf31d-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="bf31d-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="bf31d-124">實作</span><span class="sxs-lookup"><span data-stu-id="bf31d-124">Implementations</span></span>

-   [<span data-ttu-id="bf31d-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bf31d-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bf31d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bf31d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bf31d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bf31d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bf31d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bf31d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bf31d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bf31d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bf31d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bf31d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bf31d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf31d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="bf31d-132">進入</span><span class="sxs-lookup"><span data-stu-id="bf31d-132">Entry</span></span> | <span data-ttu-id="bf31d-133">值</span><span class="sxs-lookup"><span data-stu-id="bf31d-133">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="bf31d-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bf31d-134">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="bf31d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf31d-135">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="bf31d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf31d-136">System-Only</span></span>            | <span data-ttu-id="bf31d-137">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-137">False</span></span>                                                            |
| <span data-ttu-id="bf31d-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bf31d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bf31d-139">對</span><span class="sxs-lookup"><span data-stu-id="bf31d-139">True</span></span>                                                             |
| <span data-ttu-id="bf31d-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bf31d-140">Is Indexed</span></span>             | <span data-ttu-id="bf31d-141">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-141">False</span></span>                                                            |
| <span data-ttu-id="bf31d-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bf31d-142">In Global Catalog</span></span>      | <span data-ttu-id="bf31d-143">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-143">False</span></span>                                                            |
| <span data-ttu-id="bf31d-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bf31d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf31d-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bf31d-145">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="bf31d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf31d-146">Range-Lower</span></span>            | <span data-ttu-id="bf31d-147">0</span><span class="sxs-lookup"><span data-stu-id="bf31d-147">0</span></span>                                                                |
| <span data-ttu-id="bf31d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf31d-148">Range-Upper</span></span>            | <span data-ttu-id="bf31d-149">16</span><span class="sxs-lookup"><span data-stu-id="bf31d-149">16</span></span>                                                               |
| <span data-ttu-id="bf31d-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31d-150">Search-Flags</span></span>           | <span data-ttu-id="bf31d-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf31d-151">0x00000000</span></span>                                                       |
| <span data-ttu-id="bf31d-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31d-152">System-Flags</span></span>           | <span data-ttu-id="bf31d-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf31d-153">0x00000010</span></span>                                                       |
| <span data-ttu-id="bf31d-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bf31d-154">Classes used in</span></span>        | [<span data-ttu-id="bf31d-155">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="bf31d-155">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bf31d-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf31d-156">Windows Server 2003</span></span>



| <span data-ttu-id="bf31d-157">進入</span><span class="sxs-lookup"><span data-stu-id="bf31d-157">Entry</span></span> | <span data-ttu-id="bf31d-158">值</span><span class="sxs-lookup"><span data-stu-id="bf31d-158">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="bf31d-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bf31d-159">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="bf31d-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf31d-160">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="bf31d-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf31d-161">System-Only</span></span>            | <span data-ttu-id="bf31d-162">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-162">False</span></span>                                                            |
| <span data-ttu-id="bf31d-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bf31d-163">Is-Single-Valued</span></span>       | <span data-ttu-id="bf31d-164">對</span><span class="sxs-lookup"><span data-stu-id="bf31d-164">True</span></span>                                                             |
| <span data-ttu-id="bf31d-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bf31d-165">Is Indexed</span></span>             | <span data-ttu-id="bf31d-166">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-166">False</span></span>                                                            |
| <span data-ttu-id="bf31d-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bf31d-167">In Global Catalog</span></span>      | <span data-ttu-id="bf31d-168">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-168">False</span></span>                                                            |
| <span data-ttu-id="bf31d-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bf31d-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf31d-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bf31d-170">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="bf31d-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf31d-171">Range-Lower</span></span>            | <span data-ttu-id="bf31d-172">0</span><span class="sxs-lookup"><span data-stu-id="bf31d-172">0</span></span>                                                                |
| <span data-ttu-id="bf31d-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf31d-173">Range-Upper</span></span>            | <span data-ttu-id="bf31d-174">16</span><span class="sxs-lookup"><span data-stu-id="bf31d-174">16</span></span>                                                               |
| <span data-ttu-id="bf31d-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31d-175">Search-Flags</span></span>           | <span data-ttu-id="bf31d-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf31d-176">0x00000000</span></span>                                                       |
| <span data-ttu-id="bf31d-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31d-177">System-Flags</span></span>           | <span data-ttu-id="bf31d-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf31d-178">0x00000010</span></span>                                                       |
| <span data-ttu-id="bf31d-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bf31d-179">Classes used in</span></span>        | [<span data-ttu-id="bf31d-180">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="bf31d-180">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bf31d-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bf31d-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bf31d-182">進入</span><span class="sxs-lookup"><span data-stu-id="bf31d-182">Entry</span></span> | <span data-ttu-id="bf31d-183">值</span><span class="sxs-lookup"><span data-stu-id="bf31d-183">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="bf31d-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bf31d-184">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="bf31d-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf31d-185">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="bf31d-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf31d-186">System-Only</span></span>            | <span data-ttu-id="bf31d-187">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-187">False</span></span>                                                            |
| <span data-ttu-id="bf31d-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bf31d-188">Is-Single-Valued</span></span>       | <span data-ttu-id="bf31d-189">對</span><span class="sxs-lookup"><span data-stu-id="bf31d-189">True</span></span>                                                             |
| <span data-ttu-id="bf31d-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bf31d-190">Is Indexed</span></span>             | <span data-ttu-id="bf31d-191">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-191">False</span></span>                                                            |
| <span data-ttu-id="bf31d-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bf31d-192">In Global Catalog</span></span>      | <span data-ttu-id="bf31d-193">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-193">False</span></span>                                                            |
| <span data-ttu-id="bf31d-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bf31d-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf31d-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bf31d-195">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="bf31d-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf31d-196">Range-Lower</span></span>            | <span data-ttu-id="bf31d-197">0</span><span class="sxs-lookup"><span data-stu-id="bf31d-197">0</span></span>                                                                |
| <span data-ttu-id="bf31d-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf31d-198">Range-Upper</span></span>            | <span data-ttu-id="bf31d-199">16</span><span class="sxs-lookup"><span data-stu-id="bf31d-199">16</span></span>                                                               |
| <span data-ttu-id="bf31d-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31d-200">Search-Flags</span></span>           | <span data-ttu-id="bf31d-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf31d-201">0x00000000</span></span>                                                       |
| <span data-ttu-id="bf31d-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31d-202">System-Flags</span></span>           | <span data-ttu-id="bf31d-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf31d-203">0x00000010</span></span>                                                       |
| <span data-ttu-id="bf31d-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bf31d-204">Classes used in</span></span>        | [<span data-ttu-id="bf31d-205">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="bf31d-205">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bf31d-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf31d-206">Windows Server 2008</span></span>



| <span data-ttu-id="bf31d-207">進入</span><span class="sxs-lookup"><span data-stu-id="bf31d-207">Entry</span></span> | <span data-ttu-id="bf31d-208">值</span><span class="sxs-lookup"><span data-stu-id="bf31d-208">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="bf31d-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bf31d-209">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="bf31d-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf31d-210">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="bf31d-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf31d-211">System-Only</span></span>            | <span data-ttu-id="bf31d-212">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-212">False</span></span>                                                            |
| <span data-ttu-id="bf31d-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bf31d-213">Is-Single-Valued</span></span>       | <span data-ttu-id="bf31d-214">對</span><span class="sxs-lookup"><span data-stu-id="bf31d-214">True</span></span>                                                             |
| <span data-ttu-id="bf31d-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bf31d-215">Is Indexed</span></span>             | <span data-ttu-id="bf31d-216">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-216">False</span></span>                                                            |
| <span data-ttu-id="bf31d-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bf31d-217">In Global Catalog</span></span>      | <span data-ttu-id="bf31d-218">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-218">False</span></span>                                                            |
| <span data-ttu-id="bf31d-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bf31d-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf31d-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bf31d-220">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="bf31d-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf31d-221">Range-Lower</span></span>            | <span data-ttu-id="bf31d-222">0</span><span class="sxs-lookup"><span data-stu-id="bf31d-222">0</span></span>                                                                |
| <span data-ttu-id="bf31d-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf31d-223">Range-Upper</span></span>            | <span data-ttu-id="bf31d-224">16</span><span class="sxs-lookup"><span data-stu-id="bf31d-224">16</span></span>                                                               |
| <span data-ttu-id="bf31d-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31d-225">Search-Flags</span></span>           | <span data-ttu-id="bf31d-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf31d-226">0x00000000</span></span>                                                       |
| <span data-ttu-id="bf31d-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31d-227">System-Flags</span></span>           | <span data-ttu-id="bf31d-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf31d-228">0x00000010</span></span>                                                       |
| <span data-ttu-id="bf31d-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bf31d-229">Classes used in</span></span>        | [<span data-ttu-id="bf31d-230">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="bf31d-230">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bf31d-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bf31d-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bf31d-232">進入</span><span class="sxs-lookup"><span data-stu-id="bf31d-232">Entry</span></span> | <span data-ttu-id="bf31d-233">值</span><span class="sxs-lookup"><span data-stu-id="bf31d-233">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="bf31d-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bf31d-234">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="bf31d-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf31d-235">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="bf31d-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf31d-236">System-Only</span></span>            | <span data-ttu-id="bf31d-237">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-237">False</span></span>                                                            |
| <span data-ttu-id="bf31d-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bf31d-238">Is-Single-Valued</span></span>       | <span data-ttu-id="bf31d-239">對</span><span class="sxs-lookup"><span data-stu-id="bf31d-239">True</span></span>                                                             |
| <span data-ttu-id="bf31d-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bf31d-240">Is Indexed</span></span>             | <span data-ttu-id="bf31d-241">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-241">False</span></span>                                                            |
| <span data-ttu-id="bf31d-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bf31d-242">In Global Catalog</span></span>      | <span data-ttu-id="bf31d-243">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-243">False</span></span>                                                            |
| <span data-ttu-id="bf31d-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bf31d-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf31d-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bf31d-245">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="bf31d-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf31d-246">Range-Lower</span></span>            | <span data-ttu-id="bf31d-247">0</span><span class="sxs-lookup"><span data-stu-id="bf31d-247">0</span></span>                                                                |
| <span data-ttu-id="bf31d-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf31d-248">Range-Upper</span></span>            | <span data-ttu-id="bf31d-249">16</span><span class="sxs-lookup"><span data-stu-id="bf31d-249">16</span></span>                                                               |
| <span data-ttu-id="bf31d-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31d-250">Search-Flags</span></span>           | <span data-ttu-id="bf31d-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf31d-251">0x00000000</span></span>                                                       |
| <span data-ttu-id="bf31d-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31d-252">System-Flags</span></span>           | <span data-ttu-id="bf31d-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf31d-253">0x00000010</span></span>                                                       |
| <span data-ttu-id="bf31d-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bf31d-254">Classes used in</span></span>        | [<span data-ttu-id="bf31d-255">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="bf31d-255">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bf31d-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf31d-256">Windows Server 2012</span></span>



| <span data-ttu-id="bf31d-257">進入</span><span class="sxs-lookup"><span data-stu-id="bf31d-257">Entry</span></span> | <span data-ttu-id="bf31d-258">值</span><span class="sxs-lookup"><span data-stu-id="bf31d-258">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="bf31d-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bf31d-259">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="bf31d-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf31d-260">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="bf31d-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf31d-261">System-Only</span></span>            | <span data-ttu-id="bf31d-262">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-262">False</span></span>                                                            |
| <span data-ttu-id="bf31d-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bf31d-263">Is-Single-Valued</span></span>       | <span data-ttu-id="bf31d-264">對</span><span class="sxs-lookup"><span data-stu-id="bf31d-264">True</span></span>                                                             |
| <span data-ttu-id="bf31d-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bf31d-265">Is Indexed</span></span>             | <span data-ttu-id="bf31d-266">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-266">False</span></span>                                                            |
| <span data-ttu-id="bf31d-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bf31d-267">In Global Catalog</span></span>      | <span data-ttu-id="bf31d-268">否</span><span class="sxs-lookup"><span data-stu-id="bf31d-268">False</span></span>                                                            |
| <span data-ttu-id="bf31d-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bf31d-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf31d-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bf31d-270">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="bf31d-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf31d-271">Range-Lower</span></span>            | <span data-ttu-id="bf31d-272">0</span><span class="sxs-lookup"><span data-stu-id="bf31d-272">0</span></span>                                                                |
| <span data-ttu-id="bf31d-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf31d-273">Range-Upper</span></span>            | <span data-ttu-id="bf31d-274">16</span><span class="sxs-lookup"><span data-stu-id="bf31d-274">16</span></span>                                                               |
| <span data-ttu-id="bf31d-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31d-275">Search-Flags</span></span>           | <span data-ttu-id="bf31d-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf31d-276">0x00000000</span></span>                                                       |
| <span data-ttu-id="bf31d-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31d-277">System-Flags</span></span>           | <span data-ttu-id="bf31d-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf31d-278">0x00000010</span></span>                                                       |
| <span data-ttu-id="bf31d-279">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bf31d-279">Classes used in</span></span>        | [<span data-ttu-id="bf31d-280">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="bf31d-280">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





