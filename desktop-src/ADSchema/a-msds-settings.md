---
title: ms DS-Settings 屬性
description: 用來儲存物件的設定。 其用途僅由物件的擁有者決定。 建議您使用它來儲存名稱/值配對。 例如，藍色。
ms.assetid: 44e3a9e2-5528-4328-9cb7-1b6a4a77950a
ms.tgt_platform: multiple
keywords:
- ms DS-設定屬性 AD 架構
- 設定屬性的 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f466bd5aa5a904482ff9c84c1f818c12205f69c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845120"
---
# <a name="ms-ds-settings-attribute"></a><span data-ttu-id="7db93-108">ms DS-Settings 屬性</span><span class="sxs-lookup"><span data-stu-id="7db93-108">ms-DS-Settings attribute</span></span>

<span data-ttu-id="7db93-109">用來儲存物件的設定。</span><span class="sxs-lookup"><span data-stu-id="7db93-109">Used to store settings for an object.</span></span> <span data-ttu-id="7db93-110">其用途僅由物件的擁有者決定。</span><span class="sxs-lookup"><span data-stu-id="7db93-110">Its use is solely determined by the object's owner.</span></span> <span data-ttu-id="7db93-111">建議您使用它來儲存名稱/值配對。</span><span class="sxs-lookup"><span data-stu-id="7db93-111">We recommend using it to store name/value pairs.</span></span> <span data-ttu-id="7db93-112">例如，color = blue。</span><span class="sxs-lookup"><span data-stu-id="7db93-112">For example, color=blue.</span></span>



| <span data-ttu-id="7db93-113">進入</span><span class="sxs-lookup"><span data-stu-id="7db93-113">Entry</span></span> | <span data-ttu-id="7db93-114">值</span><span class="sxs-lookup"><span data-stu-id="7db93-114">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7db93-115">CN</span><span class="sxs-lookup"><span data-stu-id="7db93-115">CN</span></span>                | <span data-ttu-id="7db93-116">ms DS-設定</span><span class="sxs-lookup"><span data-stu-id="7db93-116">ms-DS-Settings</span></span>                              |
| <span data-ttu-id="7db93-117">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7db93-117">Ldap-Display-Name</span></span> | <span data-ttu-id="7db93-118">設定</span><span class="sxs-lookup"><span data-stu-id="7db93-118">msDS-Settings</span></span>                               |
| <span data-ttu-id="7db93-119">大小</span><span class="sxs-lookup"><span data-stu-id="7db93-119">Size</span></span>              | \-                                          |
| <span data-ttu-id="7db93-120">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7db93-120">Update Privilege</span></span>  | <span data-ttu-id="7db93-121">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="7db93-121">Domain administrator</span></span>                        |
| <span data-ttu-id="7db93-122">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7db93-122">Update Frequency</span></span>  | <span data-ttu-id="7db93-123">每次設定值變更時。</span><span class="sxs-lookup"><span data-stu-id="7db93-123">Each time the settings values change.</span></span>       |
| <span data-ttu-id="7db93-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7db93-124">Attribute-Id</span></span>      | <span data-ttu-id="7db93-125">1.2.840.113556.1.4.1697</span><span class="sxs-lookup"><span data-stu-id="7db93-125">1.2.840.113556.1.4.1697</span></span>                     |
| <span data-ttu-id="7db93-126">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7db93-126">System-Id-Guid</span></span>    | <span data-ttu-id="7db93-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span><span class="sxs-lookup"><span data-stu-id="7db93-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span></span>        |
| <span data-ttu-id="7db93-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="7db93-128">Syntax</span></span>            | [<span data-ttu-id="7db93-129">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7db93-129">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7db93-130">實作</span><span class="sxs-lookup"><span data-stu-id="7db93-130">Implementations</span></span>

-   [<span data-ttu-id="7db93-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7db93-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7db93-132">**亞當**</span><span class="sxs-lookup"><span data-stu-id="7db93-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7db93-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7db93-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7db93-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7db93-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7db93-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7db93-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7db93-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7db93-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7db93-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7db93-137">Windows Server 2003</span></span>



| <span data-ttu-id="7db93-138">進入</span><span class="sxs-lookup"><span data-stu-id="7db93-138">Entry</span></span> | <span data-ttu-id="7db93-139">值</span><span class="sxs-lookup"><span data-stu-id="7db93-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7db93-140">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7db93-140">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="7db93-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7db93-141">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="7db93-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="7db93-142">System-Only</span></span>            | <span data-ttu-id="7db93-143">否</span><span class="sxs-lookup"><span data-stu-id="7db93-143">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-144">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7db93-144">Is-Single-Valued</span></span>       | <span data-ttu-id="7db93-145">否</span><span class="sxs-lookup"><span data-stu-id="7db93-145">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-146">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7db93-146">Is Indexed</span></span>             | <span data-ttu-id="7db93-147">否</span><span class="sxs-lookup"><span data-stu-id="7db93-147">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-148">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7db93-148">In Global Catalog</span></span>      | <span data-ttu-id="7db93-149">否</span><span class="sxs-lookup"><span data-stu-id="7db93-149">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-150">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7db93-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="7db93-151">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7db93-151">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="7db93-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7db93-152">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="7db93-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7db93-153">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="7db93-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7db93-154">Search-Flags</span></span>           | <span data-ttu-id="7db93-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db93-155">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="7db93-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7db93-156">System-Flags</span></span>           | <span data-ttu-id="7db93-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db93-157">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="7db93-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7db93-158">Classes used in</span></span>        | [<span data-ttu-id="7db93-159">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="7db93-159">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="7db93-160">**連接點**</span><span class="sxs-lookup"><span data-stu-id="7db93-160">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7db93-161">亞當</span><span class="sxs-lookup"><span data-stu-id="7db93-161">ADAM</span></span>



| <span data-ttu-id="7db93-162">進入</span><span class="sxs-lookup"><span data-stu-id="7db93-162">Entry</span></span> | <span data-ttu-id="7db93-163">值</span><span class="sxs-lookup"><span data-stu-id="7db93-163">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="7db93-164">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7db93-164">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7db93-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7db93-165">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="7db93-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="7db93-166">System-Only</span></span>            | <span data-ttu-id="7db93-167">否</span><span class="sxs-lookup"><span data-stu-id="7db93-167">False</span></span>                                                            |
| <span data-ttu-id="7db93-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7db93-168">Is-Single-Valued</span></span>       | <span data-ttu-id="7db93-169">否</span><span class="sxs-lookup"><span data-stu-id="7db93-169">False</span></span>                                                            |
| <span data-ttu-id="7db93-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7db93-170">Is Indexed</span></span>             | <span data-ttu-id="7db93-171">否</span><span class="sxs-lookup"><span data-stu-id="7db93-171">False</span></span>                                                            |
| <span data-ttu-id="7db93-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7db93-172">In Global Catalog</span></span>      | <span data-ttu-id="7db93-173">否</span><span class="sxs-lookup"><span data-stu-id="7db93-173">False</span></span>                                                            |
| <span data-ttu-id="7db93-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7db93-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="7db93-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7db93-175">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="7db93-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7db93-176">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="7db93-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7db93-177">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="7db93-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7db93-178">Search-Flags</span></span>           | <span data-ttu-id="7db93-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db93-179">0x00000000</span></span>                                                       |
| <span data-ttu-id="7db93-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7db93-180">System-Flags</span></span>           | <span data-ttu-id="7db93-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db93-181">0x00000000</span></span>                                                       |
| <span data-ttu-id="7db93-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7db93-182">Classes used in</span></span>        | [<span data-ttu-id="7db93-183">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="7db93-183">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7db93-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7db93-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7db93-185">進入</span><span class="sxs-lookup"><span data-stu-id="7db93-185">Entry</span></span> | <span data-ttu-id="7db93-186">值</span><span class="sxs-lookup"><span data-stu-id="7db93-186">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7db93-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7db93-187">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="7db93-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7db93-188">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="7db93-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="7db93-189">System-Only</span></span>            | <span data-ttu-id="7db93-190">否</span><span class="sxs-lookup"><span data-stu-id="7db93-190">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7db93-191">Is-Single-Valued</span></span>       | <span data-ttu-id="7db93-192">否</span><span class="sxs-lookup"><span data-stu-id="7db93-192">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7db93-193">Is Indexed</span></span>             | <span data-ttu-id="7db93-194">否</span><span class="sxs-lookup"><span data-stu-id="7db93-194">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7db93-195">In Global Catalog</span></span>      | <span data-ttu-id="7db93-196">否</span><span class="sxs-lookup"><span data-stu-id="7db93-196">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7db93-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="7db93-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7db93-198">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="7db93-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7db93-199">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="7db93-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7db93-200">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="7db93-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7db93-201">Search-Flags</span></span>           | <span data-ttu-id="7db93-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db93-202">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="7db93-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7db93-203">System-Flags</span></span>           | <span data-ttu-id="7db93-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db93-204">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="7db93-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7db93-205">Classes used in</span></span>        | [<span data-ttu-id="7db93-206">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="7db93-206">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="7db93-207">**連接點**</span><span class="sxs-lookup"><span data-stu-id="7db93-207">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7db93-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7db93-208">Windows Server 2008</span></span>



| <span data-ttu-id="7db93-209">進入</span><span class="sxs-lookup"><span data-stu-id="7db93-209">Entry</span></span> | <span data-ttu-id="7db93-210">值</span><span class="sxs-lookup"><span data-stu-id="7db93-210">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7db93-211">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7db93-211">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="7db93-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7db93-212">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="7db93-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="7db93-213">System-Only</span></span>            | <span data-ttu-id="7db93-214">否</span><span class="sxs-lookup"><span data-stu-id="7db93-214">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7db93-215">Is-Single-Valued</span></span>       | <span data-ttu-id="7db93-216">否</span><span class="sxs-lookup"><span data-stu-id="7db93-216">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7db93-217">Is Indexed</span></span>             | <span data-ttu-id="7db93-218">否</span><span class="sxs-lookup"><span data-stu-id="7db93-218">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7db93-219">In Global Catalog</span></span>      | <span data-ttu-id="7db93-220">否</span><span class="sxs-lookup"><span data-stu-id="7db93-220">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7db93-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="7db93-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7db93-222">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="7db93-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7db93-223">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="7db93-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7db93-224">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="7db93-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7db93-225">Search-Flags</span></span>           | <span data-ttu-id="7db93-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db93-226">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="7db93-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7db93-227">System-Flags</span></span>           | <span data-ttu-id="7db93-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db93-228">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="7db93-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7db93-229">Classes used in</span></span>        | [<span data-ttu-id="7db93-230">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="7db93-230">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="7db93-231">**連接點**</span><span class="sxs-lookup"><span data-stu-id="7db93-231">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7db93-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7db93-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7db93-233">進入</span><span class="sxs-lookup"><span data-stu-id="7db93-233">Entry</span></span> | <span data-ttu-id="7db93-234">值</span><span class="sxs-lookup"><span data-stu-id="7db93-234">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7db93-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7db93-235">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="7db93-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7db93-236">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="7db93-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="7db93-237">System-Only</span></span>            | <span data-ttu-id="7db93-238">否</span><span class="sxs-lookup"><span data-stu-id="7db93-238">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7db93-239">Is-Single-Valued</span></span>       | <span data-ttu-id="7db93-240">否</span><span class="sxs-lookup"><span data-stu-id="7db93-240">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7db93-241">Is Indexed</span></span>             | <span data-ttu-id="7db93-242">否</span><span class="sxs-lookup"><span data-stu-id="7db93-242">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7db93-243">In Global Catalog</span></span>      | <span data-ttu-id="7db93-244">否</span><span class="sxs-lookup"><span data-stu-id="7db93-244">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7db93-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="7db93-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7db93-246">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="7db93-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7db93-247">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="7db93-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7db93-248">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="7db93-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7db93-249">Search-Flags</span></span>           | <span data-ttu-id="7db93-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db93-250">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="7db93-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7db93-251">System-Flags</span></span>           | <span data-ttu-id="7db93-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db93-252">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="7db93-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7db93-253">Classes used in</span></span>        | [<span data-ttu-id="7db93-254">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="7db93-254">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="7db93-255">**連接點**</span><span class="sxs-lookup"><span data-stu-id="7db93-255">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7db93-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7db93-256">Windows Server 2012</span></span>



| <span data-ttu-id="7db93-257">進入</span><span class="sxs-lookup"><span data-stu-id="7db93-257">Entry</span></span> | <span data-ttu-id="7db93-258">值</span><span class="sxs-lookup"><span data-stu-id="7db93-258">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7db93-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7db93-259">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="7db93-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7db93-260">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="7db93-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="7db93-261">System-Only</span></span>            | <span data-ttu-id="7db93-262">否</span><span class="sxs-lookup"><span data-stu-id="7db93-262">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7db93-263">Is-Single-Valued</span></span>       | <span data-ttu-id="7db93-264">否</span><span class="sxs-lookup"><span data-stu-id="7db93-264">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7db93-265">Is Indexed</span></span>             | <span data-ttu-id="7db93-266">否</span><span class="sxs-lookup"><span data-stu-id="7db93-266">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7db93-267">In Global Catalog</span></span>      | <span data-ttu-id="7db93-268">否</span><span class="sxs-lookup"><span data-stu-id="7db93-268">False</span></span>                                                                                                                     |
| <span data-ttu-id="7db93-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7db93-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="7db93-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7db93-270">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="7db93-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7db93-271">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="7db93-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7db93-272">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="7db93-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7db93-273">Search-Flags</span></span>           | <span data-ttu-id="7db93-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db93-274">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="7db93-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7db93-275">System-Flags</span></span>           | <span data-ttu-id="7db93-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7db93-276">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="7db93-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7db93-277">Classes used in</span></span>        | [<span data-ttu-id="7db93-278">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="7db93-278">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="7db93-279">**連接點**</span><span class="sxs-lookup"><span data-stu-id="7db93-279">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



 

 





