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
# <a name="product-code-attribute"></a><span data-ttu-id="6ca48-105">Product-Code 屬性</span><span class="sxs-lookup"><span data-stu-id="6ca48-105">Product-Code attribute</span></span>

<span data-ttu-id="6ca48-106">此屬性包含特定產品版本之應用程式的唯一識別碼（以字串 GUID 表示），例如 " {12345678-1234-1234-1234-123456789012} "。</span><span class="sxs-lookup"><span data-stu-id="6ca48-106">This attribute contains a unique identifier for an application for a particular product release, represented as a string GUID, for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="6ca48-107">此 GUID 中使用的字母必須為大寫。</span><span class="sxs-lookup"><span data-stu-id="6ca48-107">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="6ca48-108">此識別碼必須因不同版本和語言而有所不同。</span><span class="sxs-lookup"><span data-stu-id="6ca48-108">This ID must vary for different versions and languages.</span></span>



| <span data-ttu-id="6ca48-109">進入</span><span class="sxs-lookup"><span data-stu-id="6ca48-109">Entry</span></span> | <span data-ttu-id="6ca48-110">值</span><span class="sxs-lookup"><span data-stu-id="6ca48-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="6ca48-111">CN</span><span class="sxs-lookup"><span data-stu-id="6ca48-111">CN</span></span>                | <span data-ttu-id="6ca48-112">Product-Code</span><span class="sxs-lookup"><span data-stu-id="6ca48-112">Product-Code</span></span>                                          |
| <span data-ttu-id="6ca48-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6ca48-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6ca48-114">productCode</span><span class="sxs-lookup"><span data-stu-id="6ca48-114">productCode</span></span>                                           |
| <span data-ttu-id="6ca48-115">大小</span><span class="sxs-lookup"><span data-stu-id="6ca48-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="6ca48-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6ca48-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="6ca48-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6ca48-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="6ca48-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6ca48-118">Attribute-Id</span></span>      | <span data-ttu-id="6ca48-119">1.2.840.113556.1.4.818</span><span class="sxs-lookup"><span data-stu-id="6ca48-119">1.2.840.113556.1.4.818</span></span>                                |
| <span data-ttu-id="6ca48-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6ca48-120">System-Id-Guid</span></span>    | <span data-ttu-id="6ca48-121">d9e18317-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6ca48-121">d9e18317-8939-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="6ca48-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ca48-122">Syntax</span></span>            | [<span data-ttu-id="6ca48-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="6ca48-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="6ca48-124">實作</span><span class="sxs-lookup"><span data-stu-id="6ca48-124">Implementations</span></span>

-   [<span data-ttu-id="6ca48-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6ca48-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6ca48-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6ca48-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6ca48-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6ca48-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6ca48-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6ca48-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6ca48-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6ca48-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6ca48-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6ca48-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6ca48-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6ca48-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6ca48-132">進入</span><span class="sxs-lookup"><span data-stu-id="6ca48-132">Entry</span></span> | <span data-ttu-id="6ca48-133">值</span><span class="sxs-lookup"><span data-stu-id="6ca48-133">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6ca48-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ca48-134">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6ca48-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ca48-135">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6ca48-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ca48-136">System-Only</span></span>            | <span data-ttu-id="6ca48-137">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-137">False</span></span>                                                            |
| <span data-ttu-id="6ca48-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ca48-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6ca48-139">對</span><span class="sxs-lookup"><span data-stu-id="6ca48-139">True</span></span>                                                             |
| <span data-ttu-id="6ca48-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ca48-140">Is Indexed</span></span>             | <span data-ttu-id="6ca48-141">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-141">False</span></span>                                                            |
| <span data-ttu-id="6ca48-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ca48-142">In Global Catalog</span></span>      | <span data-ttu-id="6ca48-143">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-143">False</span></span>                                                            |
| <span data-ttu-id="6ca48-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ca48-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ca48-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ca48-145">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6ca48-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ca48-146">Range-Lower</span></span>            | <span data-ttu-id="6ca48-147">0</span><span class="sxs-lookup"><span data-stu-id="6ca48-147">0</span></span>                                                                |
| <span data-ttu-id="6ca48-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ca48-148">Range-Upper</span></span>            | <span data-ttu-id="6ca48-149">16</span><span class="sxs-lookup"><span data-stu-id="6ca48-149">16</span></span>                                                               |
| <span data-ttu-id="6ca48-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ca48-150">Search-Flags</span></span>           | <span data-ttu-id="6ca48-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ca48-151">0x00000000</span></span>                                                       |
| <span data-ttu-id="6ca48-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ca48-152">System-Flags</span></span>           | <span data-ttu-id="6ca48-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ca48-153">0x00000010</span></span>                                                       |
| <span data-ttu-id="6ca48-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ca48-154">Classes used in</span></span>        | [<span data-ttu-id="6ca48-155">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="6ca48-155">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6ca48-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ca48-156">Windows Server 2003</span></span>



| <span data-ttu-id="6ca48-157">進入</span><span class="sxs-lookup"><span data-stu-id="6ca48-157">Entry</span></span> | <span data-ttu-id="6ca48-158">值</span><span class="sxs-lookup"><span data-stu-id="6ca48-158">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6ca48-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ca48-159">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6ca48-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ca48-160">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6ca48-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ca48-161">System-Only</span></span>            | <span data-ttu-id="6ca48-162">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-162">False</span></span>                                                            |
| <span data-ttu-id="6ca48-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ca48-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6ca48-164">對</span><span class="sxs-lookup"><span data-stu-id="6ca48-164">True</span></span>                                                             |
| <span data-ttu-id="6ca48-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ca48-165">Is Indexed</span></span>             | <span data-ttu-id="6ca48-166">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-166">False</span></span>                                                            |
| <span data-ttu-id="6ca48-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ca48-167">In Global Catalog</span></span>      | <span data-ttu-id="6ca48-168">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-168">False</span></span>                                                            |
| <span data-ttu-id="6ca48-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ca48-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ca48-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ca48-170">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6ca48-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ca48-171">Range-Lower</span></span>            | <span data-ttu-id="6ca48-172">0</span><span class="sxs-lookup"><span data-stu-id="6ca48-172">0</span></span>                                                                |
| <span data-ttu-id="6ca48-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ca48-173">Range-Upper</span></span>            | <span data-ttu-id="6ca48-174">16</span><span class="sxs-lookup"><span data-stu-id="6ca48-174">16</span></span>                                                               |
| <span data-ttu-id="6ca48-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ca48-175">Search-Flags</span></span>           | <span data-ttu-id="6ca48-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ca48-176">0x00000000</span></span>                                                       |
| <span data-ttu-id="6ca48-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ca48-177">System-Flags</span></span>           | <span data-ttu-id="6ca48-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ca48-178">0x00000010</span></span>                                                       |
| <span data-ttu-id="6ca48-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ca48-179">Classes used in</span></span>        | [<span data-ttu-id="6ca48-180">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="6ca48-180">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6ca48-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6ca48-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6ca48-182">進入</span><span class="sxs-lookup"><span data-stu-id="6ca48-182">Entry</span></span> | <span data-ttu-id="6ca48-183">值</span><span class="sxs-lookup"><span data-stu-id="6ca48-183">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6ca48-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ca48-184">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6ca48-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ca48-185">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6ca48-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ca48-186">System-Only</span></span>            | <span data-ttu-id="6ca48-187">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-187">False</span></span>                                                            |
| <span data-ttu-id="6ca48-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ca48-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6ca48-189">對</span><span class="sxs-lookup"><span data-stu-id="6ca48-189">True</span></span>                                                             |
| <span data-ttu-id="6ca48-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ca48-190">Is Indexed</span></span>             | <span data-ttu-id="6ca48-191">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-191">False</span></span>                                                            |
| <span data-ttu-id="6ca48-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ca48-192">In Global Catalog</span></span>      | <span data-ttu-id="6ca48-193">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-193">False</span></span>                                                            |
| <span data-ttu-id="6ca48-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ca48-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ca48-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ca48-195">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6ca48-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ca48-196">Range-Lower</span></span>            | <span data-ttu-id="6ca48-197">0</span><span class="sxs-lookup"><span data-stu-id="6ca48-197">0</span></span>                                                                |
| <span data-ttu-id="6ca48-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ca48-198">Range-Upper</span></span>            | <span data-ttu-id="6ca48-199">16</span><span class="sxs-lookup"><span data-stu-id="6ca48-199">16</span></span>                                                               |
| <span data-ttu-id="6ca48-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ca48-200">Search-Flags</span></span>           | <span data-ttu-id="6ca48-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ca48-201">0x00000000</span></span>                                                       |
| <span data-ttu-id="6ca48-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ca48-202">System-Flags</span></span>           | <span data-ttu-id="6ca48-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ca48-203">0x00000010</span></span>                                                       |
| <span data-ttu-id="6ca48-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ca48-204">Classes used in</span></span>        | [<span data-ttu-id="6ca48-205">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="6ca48-205">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6ca48-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ca48-206">Windows Server 2008</span></span>



| <span data-ttu-id="6ca48-207">進入</span><span class="sxs-lookup"><span data-stu-id="6ca48-207">Entry</span></span> | <span data-ttu-id="6ca48-208">值</span><span class="sxs-lookup"><span data-stu-id="6ca48-208">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6ca48-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ca48-209">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6ca48-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ca48-210">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6ca48-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ca48-211">System-Only</span></span>            | <span data-ttu-id="6ca48-212">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-212">False</span></span>                                                            |
| <span data-ttu-id="6ca48-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ca48-213">Is-Single-Valued</span></span>       | <span data-ttu-id="6ca48-214">對</span><span class="sxs-lookup"><span data-stu-id="6ca48-214">True</span></span>                                                             |
| <span data-ttu-id="6ca48-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ca48-215">Is Indexed</span></span>             | <span data-ttu-id="6ca48-216">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-216">False</span></span>                                                            |
| <span data-ttu-id="6ca48-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ca48-217">In Global Catalog</span></span>      | <span data-ttu-id="6ca48-218">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-218">False</span></span>                                                            |
| <span data-ttu-id="6ca48-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ca48-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ca48-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ca48-220">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6ca48-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ca48-221">Range-Lower</span></span>            | <span data-ttu-id="6ca48-222">0</span><span class="sxs-lookup"><span data-stu-id="6ca48-222">0</span></span>                                                                |
| <span data-ttu-id="6ca48-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ca48-223">Range-Upper</span></span>            | <span data-ttu-id="6ca48-224">16</span><span class="sxs-lookup"><span data-stu-id="6ca48-224">16</span></span>                                                               |
| <span data-ttu-id="6ca48-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ca48-225">Search-Flags</span></span>           | <span data-ttu-id="6ca48-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ca48-226">0x00000000</span></span>                                                       |
| <span data-ttu-id="6ca48-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ca48-227">System-Flags</span></span>           | <span data-ttu-id="6ca48-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ca48-228">0x00000010</span></span>                                                       |
| <span data-ttu-id="6ca48-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ca48-229">Classes used in</span></span>        | [<span data-ttu-id="6ca48-230">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="6ca48-230">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6ca48-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6ca48-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6ca48-232">進入</span><span class="sxs-lookup"><span data-stu-id="6ca48-232">Entry</span></span> | <span data-ttu-id="6ca48-233">值</span><span class="sxs-lookup"><span data-stu-id="6ca48-233">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6ca48-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ca48-234">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6ca48-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ca48-235">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6ca48-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ca48-236">System-Only</span></span>            | <span data-ttu-id="6ca48-237">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-237">False</span></span>                                                            |
| <span data-ttu-id="6ca48-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ca48-238">Is-Single-Valued</span></span>       | <span data-ttu-id="6ca48-239">對</span><span class="sxs-lookup"><span data-stu-id="6ca48-239">True</span></span>                                                             |
| <span data-ttu-id="6ca48-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ca48-240">Is Indexed</span></span>             | <span data-ttu-id="6ca48-241">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-241">False</span></span>                                                            |
| <span data-ttu-id="6ca48-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ca48-242">In Global Catalog</span></span>      | <span data-ttu-id="6ca48-243">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-243">False</span></span>                                                            |
| <span data-ttu-id="6ca48-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ca48-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ca48-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ca48-245">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6ca48-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ca48-246">Range-Lower</span></span>            | <span data-ttu-id="6ca48-247">0</span><span class="sxs-lookup"><span data-stu-id="6ca48-247">0</span></span>                                                                |
| <span data-ttu-id="6ca48-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ca48-248">Range-Upper</span></span>            | <span data-ttu-id="6ca48-249">16</span><span class="sxs-lookup"><span data-stu-id="6ca48-249">16</span></span>                                                               |
| <span data-ttu-id="6ca48-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ca48-250">Search-Flags</span></span>           | <span data-ttu-id="6ca48-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ca48-251">0x00000000</span></span>                                                       |
| <span data-ttu-id="6ca48-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ca48-252">System-Flags</span></span>           | <span data-ttu-id="6ca48-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ca48-253">0x00000010</span></span>                                                       |
| <span data-ttu-id="6ca48-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ca48-254">Classes used in</span></span>        | [<span data-ttu-id="6ca48-255">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="6ca48-255">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6ca48-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ca48-256">Windows Server 2012</span></span>



| <span data-ttu-id="6ca48-257">進入</span><span class="sxs-lookup"><span data-stu-id="6ca48-257">Entry</span></span> | <span data-ttu-id="6ca48-258">值</span><span class="sxs-lookup"><span data-stu-id="6ca48-258">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6ca48-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6ca48-259">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6ca48-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ca48-260">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6ca48-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ca48-261">System-Only</span></span>            | <span data-ttu-id="6ca48-262">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-262">False</span></span>                                                            |
| <span data-ttu-id="6ca48-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6ca48-263">Is-Single-Valued</span></span>       | <span data-ttu-id="6ca48-264">對</span><span class="sxs-lookup"><span data-stu-id="6ca48-264">True</span></span>                                                             |
| <span data-ttu-id="6ca48-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6ca48-265">Is Indexed</span></span>             | <span data-ttu-id="6ca48-266">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-266">False</span></span>                                                            |
| <span data-ttu-id="6ca48-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6ca48-267">In Global Catalog</span></span>      | <span data-ttu-id="6ca48-268">否</span><span class="sxs-lookup"><span data-stu-id="6ca48-268">False</span></span>                                                            |
| <span data-ttu-id="6ca48-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6ca48-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ca48-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6ca48-270">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6ca48-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ca48-271">Range-Lower</span></span>            | <span data-ttu-id="6ca48-272">0</span><span class="sxs-lookup"><span data-stu-id="6ca48-272">0</span></span>                                                                |
| <span data-ttu-id="6ca48-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ca48-273">Range-Upper</span></span>            | <span data-ttu-id="6ca48-274">16</span><span class="sxs-lookup"><span data-stu-id="6ca48-274">16</span></span>                                                               |
| <span data-ttu-id="6ca48-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ca48-275">Search-Flags</span></span>           | <span data-ttu-id="6ca48-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ca48-276">0x00000000</span></span>                                                       |
| <span data-ttu-id="6ca48-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ca48-277">System-Flags</span></span>           | <span data-ttu-id="6ca48-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ca48-278">0x00000010</span></span>                                                       |
| <span data-ttu-id="6ca48-279">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6ca48-279">Classes used in</span></span>        | [<span data-ttu-id="6ca48-280">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="6ca48-280">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





