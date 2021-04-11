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
# <a name="ms-ds-settings-attribute"></a><span data-ttu-id="87eb0-108">ms DS-Settings 屬性</span><span class="sxs-lookup"><span data-stu-id="87eb0-108">ms-DS-Settings attribute</span></span>

<span data-ttu-id="87eb0-109">用來儲存物件的設定。</span><span class="sxs-lookup"><span data-stu-id="87eb0-109">Used to store settings for an object.</span></span> <span data-ttu-id="87eb0-110">其用途僅由物件的擁有者決定。</span><span class="sxs-lookup"><span data-stu-id="87eb0-110">Its use is solely determined by the object's owner.</span></span> <span data-ttu-id="87eb0-111">建議您使用它來儲存名稱/值配對。</span><span class="sxs-lookup"><span data-stu-id="87eb0-111">We recommend using it to store name/value pairs.</span></span> <span data-ttu-id="87eb0-112">例如，color = blue。</span><span class="sxs-lookup"><span data-stu-id="87eb0-112">For example, color=blue.</span></span>



| <span data-ttu-id="87eb0-113">進入</span><span class="sxs-lookup"><span data-stu-id="87eb0-113">Entry</span></span> | <span data-ttu-id="87eb0-114">值</span><span class="sxs-lookup"><span data-stu-id="87eb0-114">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="87eb0-115">CN</span><span class="sxs-lookup"><span data-stu-id="87eb0-115">CN</span></span>                | <span data-ttu-id="87eb0-116">ms DS-設定</span><span class="sxs-lookup"><span data-stu-id="87eb0-116">ms-DS-Settings</span></span>                              |
| <span data-ttu-id="87eb0-117">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="87eb0-117">Ldap-Display-Name</span></span> | <span data-ttu-id="87eb0-118">設定</span><span class="sxs-lookup"><span data-stu-id="87eb0-118">msDS-Settings</span></span>                               |
| <span data-ttu-id="87eb0-119">大小</span><span class="sxs-lookup"><span data-stu-id="87eb0-119">Size</span></span>              | \-                                          |
| <span data-ttu-id="87eb0-120">更新許可權</span><span class="sxs-lookup"><span data-stu-id="87eb0-120">Update Privilege</span></span>  | <span data-ttu-id="87eb0-121">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="87eb0-121">Domain administrator</span></span>                        |
| <span data-ttu-id="87eb0-122">更新頻率</span><span class="sxs-lookup"><span data-stu-id="87eb0-122">Update Frequency</span></span>  | <span data-ttu-id="87eb0-123">每次設定值變更時。</span><span class="sxs-lookup"><span data-stu-id="87eb0-123">Each time the settings values change.</span></span>       |
| <span data-ttu-id="87eb0-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="87eb0-124">Attribute-Id</span></span>      | <span data-ttu-id="87eb0-125">1.2.840.113556.1.4.1697</span><span class="sxs-lookup"><span data-stu-id="87eb0-125">1.2.840.113556.1.4.1697</span></span>                     |
| <span data-ttu-id="87eb0-126">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="87eb0-126">System-Id-Guid</span></span>    | <span data-ttu-id="87eb0-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span><span class="sxs-lookup"><span data-stu-id="87eb0-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span></span>        |
| <span data-ttu-id="87eb0-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="87eb0-128">Syntax</span></span>            | [<span data-ttu-id="87eb0-129">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="87eb0-129">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="87eb0-130">實作</span><span class="sxs-lookup"><span data-stu-id="87eb0-130">Implementations</span></span>

-   [<span data-ttu-id="87eb0-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="87eb0-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="87eb0-132">**亞當**</span><span class="sxs-lookup"><span data-stu-id="87eb0-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="87eb0-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="87eb0-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="87eb0-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="87eb0-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="87eb0-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="87eb0-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="87eb0-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="87eb0-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="87eb0-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="87eb0-137">Windows Server 2003</span></span>



| <span data-ttu-id="87eb0-138">進入</span><span class="sxs-lookup"><span data-stu-id="87eb0-138">Entry</span></span> | <span data-ttu-id="87eb0-139">值</span><span class="sxs-lookup"><span data-stu-id="87eb0-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87eb0-140">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87eb0-140">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="87eb0-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87eb0-141">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="87eb0-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="87eb0-142">System-Only</span></span>            | <span data-ttu-id="87eb0-143">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-143">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-144">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87eb0-144">Is-Single-Valued</span></span>       | <span data-ttu-id="87eb0-145">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-145">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-146">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87eb0-146">Is Indexed</span></span>             | <span data-ttu-id="87eb0-147">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-147">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-148">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87eb0-148">In Global Catalog</span></span>      | <span data-ttu-id="87eb0-149">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-149">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-150">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87eb0-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="87eb0-151">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87eb0-151">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="87eb0-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87eb0-152">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="87eb0-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87eb0-153">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="87eb0-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87eb0-154">Search-Flags</span></span>           | <span data-ttu-id="87eb0-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87eb0-155">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="87eb0-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87eb0-156">System-Flags</span></span>           | <span data-ttu-id="87eb0-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87eb0-157">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="87eb0-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87eb0-158">Classes used in</span></span>        | [<span data-ttu-id="87eb0-159">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="87eb0-159">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="87eb0-160">**連接點**</span><span class="sxs-lookup"><span data-stu-id="87eb0-160">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="adam"></a><span data-ttu-id="87eb0-161">亞當</span><span class="sxs-lookup"><span data-stu-id="87eb0-161">ADAM</span></span>



| <span data-ttu-id="87eb0-162">進入</span><span class="sxs-lookup"><span data-stu-id="87eb0-162">Entry</span></span> | <span data-ttu-id="87eb0-163">值</span><span class="sxs-lookup"><span data-stu-id="87eb0-163">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="87eb0-164">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87eb0-164">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="87eb0-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87eb0-165">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="87eb0-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="87eb0-166">System-Only</span></span>            | <span data-ttu-id="87eb0-167">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-167">False</span></span>                                                            |
| <span data-ttu-id="87eb0-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87eb0-168">Is-Single-Valued</span></span>       | <span data-ttu-id="87eb0-169">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-169">False</span></span>                                                            |
| <span data-ttu-id="87eb0-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87eb0-170">Is Indexed</span></span>             | <span data-ttu-id="87eb0-171">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-171">False</span></span>                                                            |
| <span data-ttu-id="87eb0-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87eb0-172">In Global Catalog</span></span>      | <span data-ttu-id="87eb0-173">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-173">False</span></span>                                                            |
| <span data-ttu-id="87eb0-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87eb0-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="87eb0-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87eb0-175">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="87eb0-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87eb0-176">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="87eb0-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87eb0-177">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="87eb0-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87eb0-178">Search-Flags</span></span>           | <span data-ttu-id="87eb0-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87eb0-179">0x00000000</span></span>                                                       |
| <span data-ttu-id="87eb0-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87eb0-180">System-Flags</span></span>           | <span data-ttu-id="87eb0-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87eb0-181">0x00000000</span></span>                                                       |
| <span data-ttu-id="87eb0-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87eb0-182">Classes used in</span></span>        | [<span data-ttu-id="87eb0-183">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="87eb0-183">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="87eb0-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="87eb0-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="87eb0-185">進入</span><span class="sxs-lookup"><span data-stu-id="87eb0-185">Entry</span></span> | <span data-ttu-id="87eb0-186">值</span><span class="sxs-lookup"><span data-stu-id="87eb0-186">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87eb0-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87eb0-187">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="87eb0-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87eb0-188">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="87eb0-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="87eb0-189">System-Only</span></span>            | <span data-ttu-id="87eb0-190">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-190">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87eb0-191">Is-Single-Valued</span></span>       | <span data-ttu-id="87eb0-192">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-192">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87eb0-193">Is Indexed</span></span>             | <span data-ttu-id="87eb0-194">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-194">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87eb0-195">In Global Catalog</span></span>      | <span data-ttu-id="87eb0-196">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-196">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87eb0-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="87eb0-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87eb0-198">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="87eb0-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87eb0-199">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="87eb0-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87eb0-200">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="87eb0-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87eb0-201">Search-Flags</span></span>           | <span data-ttu-id="87eb0-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87eb0-202">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="87eb0-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87eb0-203">System-Flags</span></span>           | <span data-ttu-id="87eb0-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87eb0-204">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="87eb0-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87eb0-205">Classes used in</span></span>        | [<span data-ttu-id="87eb0-206">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="87eb0-206">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="87eb0-207">**連接點**</span><span class="sxs-lookup"><span data-stu-id="87eb0-207">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="87eb0-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87eb0-208">Windows Server 2008</span></span>



| <span data-ttu-id="87eb0-209">進入</span><span class="sxs-lookup"><span data-stu-id="87eb0-209">Entry</span></span> | <span data-ttu-id="87eb0-210">值</span><span class="sxs-lookup"><span data-stu-id="87eb0-210">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87eb0-211">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87eb0-211">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="87eb0-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87eb0-212">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="87eb0-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="87eb0-213">System-Only</span></span>            | <span data-ttu-id="87eb0-214">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-214">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87eb0-215">Is-Single-Valued</span></span>       | <span data-ttu-id="87eb0-216">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-216">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87eb0-217">Is Indexed</span></span>             | <span data-ttu-id="87eb0-218">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-218">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87eb0-219">In Global Catalog</span></span>      | <span data-ttu-id="87eb0-220">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-220">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87eb0-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="87eb0-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87eb0-222">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="87eb0-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87eb0-223">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="87eb0-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87eb0-224">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="87eb0-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87eb0-225">Search-Flags</span></span>           | <span data-ttu-id="87eb0-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87eb0-226">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="87eb0-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87eb0-227">System-Flags</span></span>           | <span data-ttu-id="87eb0-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87eb0-228">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="87eb0-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87eb0-229">Classes used in</span></span>        | [<span data-ttu-id="87eb0-230">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="87eb0-230">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="87eb0-231">**連接點**</span><span class="sxs-lookup"><span data-stu-id="87eb0-231">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="87eb0-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="87eb0-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="87eb0-233">進入</span><span class="sxs-lookup"><span data-stu-id="87eb0-233">Entry</span></span> | <span data-ttu-id="87eb0-234">值</span><span class="sxs-lookup"><span data-stu-id="87eb0-234">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87eb0-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87eb0-235">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="87eb0-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87eb0-236">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="87eb0-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="87eb0-237">System-Only</span></span>            | <span data-ttu-id="87eb0-238">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-238">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87eb0-239">Is-Single-Valued</span></span>       | <span data-ttu-id="87eb0-240">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-240">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87eb0-241">Is Indexed</span></span>             | <span data-ttu-id="87eb0-242">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-242">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87eb0-243">In Global Catalog</span></span>      | <span data-ttu-id="87eb0-244">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-244">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87eb0-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="87eb0-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87eb0-246">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="87eb0-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87eb0-247">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="87eb0-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87eb0-248">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="87eb0-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87eb0-249">Search-Flags</span></span>           | <span data-ttu-id="87eb0-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87eb0-250">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="87eb0-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87eb0-251">System-Flags</span></span>           | <span data-ttu-id="87eb0-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87eb0-252">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="87eb0-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87eb0-253">Classes used in</span></span>        | [<span data-ttu-id="87eb0-254">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="87eb0-254">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="87eb0-255">**連接點**</span><span class="sxs-lookup"><span data-stu-id="87eb0-255">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="87eb0-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="87eb0-256">Windows Server 2012</span></span>



| <span data-ttu-id="87eb0-257">進入</span><span class="sxs-lookup"><span data-stu-id="87eb0-257">Entry</span></span> | <span data-ttu-id="87eb0-258">值</span><span class="sxs-lookup"><span data-stu-id="87eb0-258">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87eb0-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="87eb0-259">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="87eb0-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87eb0-260">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="87eb0-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="87eb0-261">System-Only</span></span>            | <span data-ttu-id="87eb0-262">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-262">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="87eb0-263">Is-Single-Valued</span></span>       | <span data-ttu-id="87eb0-264">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-264">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="87eb0-265">Is Indexed</span></span>             | <span data-ttu-id="87eb0-266">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-266">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="87eb0-267">In Global Catalog</span></span>      | <span data-ttu-id="87eb0-268">否</span><span class="sxs-lookup"><span data-stu-id="87eb0-268">False</span></span>                                                                                                                     |
| <span data-ttu-id="87eb0-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="87eb0-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="87eb0-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="87eb0-270">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="87eb0-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87eb0-271">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="87eb0-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87eb0-272">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="87eb0-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87eb0-273">Search-Flags</span></span>           | <span data-ttu-id="87eb0-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87eb0-274">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="87eb0-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87eb0-275">System-Flags</span></span>           | <span data-ttu-id="87eb0-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="87eb0-276">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="87eb0-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="87eb0-277">Classes used in</span></span>        | [<span data-ttu-id="87eb0-278">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="87eb0-278">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="87eb0-279">**連接點**</span><span class="sxs-lookup"><span data-stu-id="87eb0-279">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



 

 





