---
title: COM-ProgID 屬性
description: 這個屬性會儲存在此應用程式封裝中所執行之 COM 物件程式識別碼的清單。
ms.assetid: 9d2945e4-f236-48f6-bed3-145d445ff653
ms.tgt_platform: multiple
keywords:
- COM-ProgID 屬性 AD 架構
- cOMProgID 屬性 AD 架構
topic_type:
- apiref
api_name:
- COM-ProgID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 686976732bedf2c4ba486186634720568d3b6c3c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970673"
---
# <a name="com-progid-attribute"></a><span data-ttu-id="fe3eb-105">COM-ProgID 屬性</span><span class="sxs-lookup"><span data-stu-id="fe3eb-105">COM-ProgID attribute</span></span>

<span data-ttu-id="fe3eb-106">這個屬性會儲存在此應用程式封裝中所執行之 COM 物件程式識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="fe3eb-106">This attribute stores the list of COM object program IDs that are implemented in this application package.</span></span>



| <span data-ttu-id="fe3eb-107">進入</span><span class="sxs-lookup"><span data-stu-id="fe3eb-107">Entry</span></span> | <span data-ttu-id="fe3eb-108">值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fe3eb-109">CN</span><span class="sxs-lookup"><span data-stu-id="fe3eb-109">CN</span></span>                | <span data-ttu-id="fe3eb-110">COM-ProgID</span><span class="sxs-lookup"><span data-stu-id="fe3eb-110">COM-ProgID</span></span>                                                                       |
| <span data-ttu-id="fe3eb-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fe3eb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fe3eb-112">cOMProgID</span><span class="sxs-lookup"><span data-stu-id="fe3eb-112">cOMProgID</span></span>                                                                        |
| <span data-ttu-id="fe3eb-113">大小</span><span class="sxs-lookup"><span data-stu-id="fe3eb-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="fe3eb-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fe3eb-114">Update Privilege</span></span>  | <span data-ttu-id="fe3eb-115">任何人都可以根據所建立物件的安全性來更新這個物件。</span><span class="sxs-lookup"><span data-stu-id="fe3eb-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="fe3eb-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fe3eb-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="fe3eb-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fe3eb-117">Attribute-Id</span></span>      | <span data-ttu-id="fe3eb-118">1.2.840.113556.1.4.21</span><span class="sxs-lookup"><span data-stu-id="fe3eb-118">1.2.840.113556.1.4.21</span></span>                                                            |
| <span data-ttu-id="fe3eb-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fe3eb-119">System-Id-Guid</span></span>    | <span data-ttu-id="fe3eb-120">bf96793d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="fe3eb-120">bf96793d-0de6-11d0-a285-00aa003049e2</span></span>                                             |
| <span data-ttu-id="fe3eb-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe3eb-121">Syntax</span></span>            | [<span data-ttu-id="fe3eb-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="fe3eb-123">實作</span><span class="sxs-lookup"><span data-stu-id="fe3eb-123">Implementations</span></span>

-   [<span data-ttu-id="fe3eb-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fe3eb-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fe3eb-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fe3eb-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fe3eb-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fe3eb-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fe3eb-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fe3eb-130">Windows 2000 Server</span></span>



| <span data-ttu-id="fe3eb-131">進入</span><span class="sxs-lookup"><span data-stu-id="fe3eb-131">Entry</span></span> | <span data-ttu-id="fe3eb-132">值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3eb-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe3eb-133">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe3eb-134">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe3eb-135">System-Only</span></span>            | <span data-ttu-id="fe3eb-136">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-136">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-137">Is-Single-Valued</span></span>       | <span data-ttu-id="fe3eb-138">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-138">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe3eb-139">Is Indexed</span></span>             | <span data-ttu-id="fe3eb-140">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-140">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe3eb-141">In Global Catalog</span></span>      | <span data-ttu-id="fe3eb-142">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-142">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe3eb-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe3eb-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe3eb-144">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="fe3eb-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe3eb-145">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe3eb-146">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe3eb-147">Search-Flags</span></span>           | <span data-ttu-id="fe3eb-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe3eb-148">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="fe3eb-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe3eb-149">System-Flags</span></span>           | <span data-ttu-id="fe3eb-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe3eb-150">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="fe3eb-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe3eb-151">Classes used in</span></span>        | [<span data-ttu-id="fe3eb-152">**類別註冊**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-152">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="fe3eb-153">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-153">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fe3eb-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe3eb-154">Windows Server 2003</span></span>



| <span data-ttu-id="fe3eb-155">進入</span><span class="sxs-lookup"><span data-stu-id="fe3eb-155">Entry</span></span> | <span data-ttu-id="fe3eb-156">值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3eb-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe3eb-157">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe3eb-158">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe3eb-159">System-Only</span></span>            | <span data-ttu-id="fe3eb-160">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-160">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="fe3eb-162">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-162">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe3eb-163">Is Indexed</span></span>             | <span data-ttu-id="fe3eb-164">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-164">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe3eb-165">In Global Catalog</span></span>      | <span data-ttu-id="fe3eb-166">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-166">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe3eb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe3eb-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe3eb-168">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="fe3eb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe3eb-169">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe3eb-170">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe3eb-171">Search-Flags</span></span>           | <span data-ttu-id="fe3eb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe3eb-172">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="fe3eb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe3eb-173">System-Flags</span></span>           | <span data-ttu-id="fe3eb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe3eb-174">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="fe3eb-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe3eb-175">Classes used in</span></span>        | [<span data-ttu-id="fe3eb-176">**類別註冊**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-176">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="fe3eb-177">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-177">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fe3eb-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fe3eb-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fe3eb-179">進入</span><span class="sxs-lookup"><span data-stu-id="fe3eb-179">Entry</span></span> | <span data-ttu-id="fe3eb-180">值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3eb-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe3eb-181">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe3eb-182">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe3eb-183">System-Only</span></span>            | <span data-ttu-id="fe3eb-184">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-184">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="fe3eb-186">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-186">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe3eb-187">Is Indexed</span></span>             | <span data-ttu-id="fe3eb-188">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-188">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe3eb-189">In Global Catalog</span></span>      | <span data-ttu-id="fe3eb-190">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-190">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe3eb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe3eb-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe3eb-192">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="fe3eb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe3eb-193">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe3eb-194">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe3eb-195">Search-Flags</span></span>           | <span data-ttu-id="fe3eb-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe3eb-196">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="fe3eb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe3eb-197">System-Flags</span></span>           | <span data-ttu-id="fe3eb-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe3eb-198">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="fe3eb-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe3eb-199">Classes used in</span></span>        | [<span data-ttu-id="fe3eb-200">**類別註冊**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-200">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="fe3eb-201">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-201">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fe3eb-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe3eb-202">Windows Server 2008</span></span>



| <span data-ttu-id="fe3eb-203">進入</span><span class="sxs-lookup"><span data-stu-id="fe3eb-203">Entry</span></span> | <span data-ttu-id="fe3eb-204">值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-204">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3eb-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe3eb-205">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe3eb-206">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe3eb-207">System-Only</span></span>            | <span data-ttu-id="fe3eb-208">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-208">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-209">Is-Single-Valued</span></span>       | <span data-ttu-id="fe3eb-210">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-210">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe3eb-211">Is Indexed</span></span>             | <span data-ttu-id="fe3eb-212">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-212">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe3eb-213">In Global Catalog</span></span>      | <span data-ttu-id="fe3eb-214">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-214">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe3eb-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe3eb-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe3eb-216">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="fe3eb-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe3eb-217">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe3eb-218">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe3eb-219">Search-Flags</span></span>           | <span data-ttu-id="fe3eb-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe3eb-220">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="fe3eb-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe3eb-221">System-Flags</span></span>           | <span data-ttu-id="fe3eb-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe3eb-222">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="fe3eb-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe3eb-223">Classes used in</span></span>        | [<span data-ttu-id="fe3eb-224">**類別註冊**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-224">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="fe3eb-225">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-225">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fe3eb-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fe3eb-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fe3eb-227">進入</span><span class="sxs-lookup"><span data-stu-id="fe3eb-227">Entry</span></span> | <span data-ttu-id="fe3eb-228">值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-228">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3eb-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe3eb-229">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe3eb-230">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe3eb-231">System-Only</span></span>            | <span data-ttu-id="fe3eb-232">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-232">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-233">Is-Single-Valued</span></span>       | <span data-ttu-id="fe3eb-234">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-234">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe3eb-235">Is Indexed</span></span>             | <span data-ttu-id="fe3eb-236">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-236">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe3eb-237">In Global Catalog</span></span>      | <span data-ttu-id="fe3eb-238">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-238">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe3eb-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe3eb-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe3eb-240">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="fe3eb-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe3eb-241">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe3eb-242">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe3eb-243">Search-Flags</span></span>           | <span data-ttu-id="fe3eb-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe3eb-244">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="fe3eb-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe3eb-245">System-Flags</span></span>           | <span data-ttu-id="fe3eb-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe3eb-246">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="fe3eb-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe3eb-247">Classes used in</span></span>        | [<span data-ttu-id="fe3eb-248">**類別註冊**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-248">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="fe3eb-249">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-249">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fe3eb-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fe3eb-250">Windows Server 2012</span></span>



| <span data-ttu-id="fe3eb-251">進入</span><span class="sxs-lookup"><span data-stu-id="fe3eb-251">Entry</span></span> | <span data-ttu-id="fe3eb-252">值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-252">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3eb-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe3eb-253">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe3eb-254">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe3eb-255">System-Only</span></span>            | <span data-ttu-id="fe3eb-256">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-256">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe3eb-257">Is-Single-Valued</span></span>       | <span data-ttu-id="fe3eb-258">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-258">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe3eb-259">Is Indexed</span></span>             | <span data-ttu-id="fe3eb-260">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-260">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe3eb-261">In Global Catalog</span></span>      | <span data-ttu-id="fe3eb-262">否</span><span class="sxs-lookup"><span data-stu-id="fe3eb-262">False</span></span>                                                                                                                         |
| <span data-ttu-id="fe3eb-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe3eb-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe3eb-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe3eb-264">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="fe3eb-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe3eb-265">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe3eb-266">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="fe3eb-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe3eb-267">Search-Flags</span></span>           | <span data-ttu-id="fe3eb-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe3eb-268">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="fe3eb-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe3eb-269">System-Flags</span></span>           | <span data-ttu-id="fe3eb-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe3eb-270">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="fe3eb-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe3eb-271">Classes used in</span></span>        | [<span data-ttu-id="fe3eb-272">**類別註冊**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-272">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="fe3eb-273">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-273">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





