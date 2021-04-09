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
# <a name="ms-ds-settings-attribute"></a><span data-ttu-id="f42bc-108">ms DS-Settings 屬性</span><span class="sxs-lookup"><span data-stu-id="f42bc-108">ms-DS-Settings attribute</span></span>

<span data-ttu-id="f42bc-109">用來儲存物件的設定。</span><span class="sxs-lookup"><span data-stu-id="f42bc-109">Used to store settings for an object.</span></span> <span data-ttu-id="f42bc-110">其用途僅由物件的擁有者決定。</span><span class="sxs-lookup"><span data-stu-id="f42bc-110">Its use is solely determined by the object's owner.</span></span> <span data-ttu-id="f42bc-111">建議您使用它來儲存名稱/值配對。</span><span class="sxs-lookup"><span data-stu-id="f42bc-111">We recommend using it to store name/value pairs.</span></span> <span data-ttu-id="f42bc-112">例如，color = blue。</span><span class="sxs-lookup"><span data-stu-id="f42bc-112">For example, color=blue.</span></span>



| <span data-ttu-id="f42bc-113">進入</span><span class="sxs-lookup"><span data-stu-id="f42bc-113">Entry</span></span> | <span data-ttu-id="f42bc-114">值</span><span class="sxs-lookup"><span data-stu-id="f42bc-114">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f42bc-115">CN</span><span class="sxs-lookup"><span data-stu-id="f42bc-115">CN</span></span>                | <span data-ttu-id="f42bc-116">ms DS-設定</span><span class="sxs-lookup"><span data-stu-id="f42bc-116">ms-DS-Settings</span></span>                              |
| <span data-ttu-id="f42bc-117">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f42bc-117">Ldap-Display-Name</span></span> | <span data-ttu-id="f42bc-118">設定</span><span class="sxs-lookup"><span data-stu-id="f42bc-118">msDS-Settings</span></span>                               |
| <span data-ttu-id="f42bc-119">大小</span><span class="sxs-lookup"><span data-stu-id="f42bc-119">Size</span></span>              | \-                                          |
| <span data-ttu-id="f42bc-120">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f42bc-120">Update Privilege</span></span>  | <span data-ttu-id="f42bc-121">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="f42bc-121">Domain administrator</span></span>                        |
| <span data-ttu-id="f42bc-122">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f42bc-122">Update Frequency</span></span>  | <span data-ttu-id="f42bc-123">每次設定值變更時。</span><span class="sxs-lookup"><span data-stu-id="f42bc-123">Each time the settings values change.</span></span>       |
| <span data-ttu-id="f42bc-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f42bc-124">Attribute-Id</span></span>      | <span data-ttu-id="f42bc-125">1.2.840.113556.1.4.1697</span><span class="sxs-lookup"><span data-stu-id="f42bc-125">1.2.840.113556.1.4.1697</span></span>                     |
| <span data-ttu-id="f42bc-126">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f42bc-126">System-Id-Guid</span></span>    | <span data-ttu-id="f42bc-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span><span class="sxs-lookup"><span data-stu-id="f42bc-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span></span>        |
| <span data-ttu-id="f42bc-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="f42bc-128">Syntax</span></span>            | [<span data-ttu-id="f42bc-129">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f42bc-129">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f42bc-130">實作</span><span class="sxs-lookup"><span data-stu-id="f42bc-130">Implementations</span></span>

-   [<span data-ttu-id="f42bc-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f42bc-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f42bc-132">**亞當**</span><span class="sxs-lookup"><span data-stu-id="f42bc-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f42bc-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f42bc-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f42bc-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f42bc-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f42bc-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f42bc-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f42bc-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f42bc-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f42bc-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f42bc-137">Windows Server 2003</span></span>



| <span data-ttu-id="f42bc-138">進入</span><span class="sxs-lookup"><span data-stu-id="f42bc-138">Entry</span></span> | <span data-ttu-id="f42bc-139">值</span><span class="sxs-lookup"><span data-stu-id="f42bc-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f42bc-140">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f42bc-140">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f42bc-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f42bc-141">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f42bc-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="f42bc-142">System-Only</span></span>            | <span data-ttu-id="f42bc-143">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-143">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-144">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f42bc-144">Is-Single-Valued</span></span>       | <span data-ttu-id="f42bc-145">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-145">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-146">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f42bc-146">Is Indexed</span></span>             | <span data-ttu-id="f42bc-147">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-147">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-148">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f42bc-148">In Global Catalog</span></span>      | <span data-ttu-id="f42bc-149">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-149">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-150">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f42bc-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="f42bc-151">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f42bc-151">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="f42bc-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f42bc-152">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f42bc-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f42bc-153">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f42bc-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bc-154">Search-Flags</span></span>           | <span data-ttu-id="f42bc-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bc-155">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f42bc-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bc-156">System-Flags</span></span>           | <span data-ttu-id="f42bc-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bc-157">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f42bc-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f42bc-158">Classes used in</span></span>        | [<span data-ttu-id="f42bc-159">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="f42bc-159">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="f42bc-160">**連接點**</span><span class="sxs-lookup"><span data-stu-id="f42bc-160">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f42bc-161">亞當</span><span class="sxs-lookup"><span data-stu-id="f42bc-161">ADAM</span></span>



| <span data-ttu-id="f42bc-162">進入</span><span class="sxs-lookup"><span data-stu-id="f42bc-162">Entry</span></span> | <span data-ttu-id="f42bc-163">值</span><span class="sxs-lookup"><span data-stu-id="f42bc-163">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f42bc-164">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f42bc-164">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f42bc-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f42bc-165">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f42bc-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="f42bc-166">System-Only</span></span>            | <span data-ttu-id="f42bc-167">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-167">False</span></span>                                                            |
| <span data-ttu-id="f42bc-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f42bc-168">Is-Single-Valued</span></span>       | <span data-ttu-id="f42bc-169">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-169">False</span></span>                                                            |
| <span data-ttu-id="f42bc-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f42bc-170">Is Indexed</span></span>             | <span data-ttu-id="f42bc-171">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-171">False</span></span>                                                            |
| <span data-ttu-id="f42bc-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f42bc-172">In Global Catalog</span></span>      | <span data-ttu-id="f42bc-173">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-173">False</span></span>                                                            |
| <span data-ttu-id="f42bc-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f42bc-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="f42bc-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f42bc-175">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f42bc-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f42bc-176">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f42bc-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f42bc-177">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f42bc-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bc-178">Search-Flags</span></span>           | <span data-ttu-id="f42bc-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bc-179">0x00000000</span></span>                                                       |
| <span data-ttu-id="f42bc-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bc-180">System-Flags</span></span>           | <span data-ttu-id="f42bc-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bc-181">0x00000000</span></span>                                                       |
| <span data-ttu-id="f42bc-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f42bc-182">Classes used in</span></span>        | [<span data-ttu-id="f42bc-183">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="f42bc-183">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f42bc-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f42bc-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f42bc-185">進入</span><span class="sxs-lookup"><span data-stu-id="f42bc-185">Entry</span></span> | <span data-ttu-id="f42bc-186">值</span><span class="sxs-lookup"><span data-stu-id="f42bc-186">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f42bc-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f42bc-187">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f42bc-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f42bc-188">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f42bc-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="f42bc-189">System-Only</span></span>            | <span data-ttu-id="f42bc-190">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-190">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f42bc-191">Is-Single-Valued</span></span>       | <span data-ttu-id="f42bc-192">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-192">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f42bc-193">Is Indexed</span></span>             | <span data-ttu-id="f42bc-194">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-194">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f42bc-195">In Global Catalog</span></span>      | <span data-ttu-id="f42bc-196">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-196">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f42bc-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="f42bc-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f42bc-198">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="f42bc-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f42bc-199">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f42bc-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f42bc-200">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f42bc-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bc-201">Search-Flags</span></span>           | <span data-ttu-id="f42bc-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bc-202">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f42bc-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bc-203">System-Flags</span></span>           | <span data-ttu-id="f42bc-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bc-204">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f42bc-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f42bc-205">Classes used in</span></span>        | [<span data-ttu-id="f42bc-206">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="f42bc-206">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="f42bc-207">**連接點**</span><span class="sxs-lookup"><span data-stu-id="f42bc-207">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f42bc-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f42bc-208">Windows Server 2008</span></span>



| <span data-ttu-id="f42bc-209">進入</span><span class="sxs-lookup"><span data-stu-id="f42bc-209">Entry</span></span> | <span data-ttu-id="f42bc-210">值</span><span class="sxs-lookup"><span data-stu-id="f42bc-210">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f42bc-211">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f42bc-211">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f42bc-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f42bc-212">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f42bc-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="f42bc-213">System-Only</span></span>            | <span data-ttu-id="f42bc-214">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-214">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f42bc-215">Is-Single-Valued</span></span>       | <span data-ttu-id="f42bc-216">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-216">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f42bc-217">Is Indexed</span></span>             | <span data-ttu-id="f42bc-218">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-218">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f42bc-219">In Global Catalog</span></span>      | <span data-ttu-id="f42bc-220">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-220">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f42bc-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="f42bc-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f42bc-222">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="f42bc-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f42bc-223">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f42bc-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f42bc-224">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f42bc-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bc-225">Search-Flags</span></span>           | <span data-ttu-id="f42bc-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bc-226">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f42bc-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bc-227">System-Flags</span></span>           | <span data-ttu-id="f42bc-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bc-228">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f42bc-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f42bc-229">Classes used in</span></span>        | [<span data-ttu-id="f42bc-230">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="f42bc-230">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="f42bc-231">**連接點**</span><span class="sxs-lookup"><span data-stu-id="f42bc-231">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f42bc-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f42bc-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f42bc-233">進入</span><span class="sxs-lookup"><span data-stu-id="f42bc-233">Entry</span></span> | <span data-ttu-id="f42bc-234">值</span><span class="sxs-lookup"><span data-stu-id="f42bc-234">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f42bc-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f42bc-235">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f42bc-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f42bc-236">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f42bc-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="f42bc-237">System-Only</span></span>            | <span data-ttu-id="f42bc-238">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-238">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f42bc-239">Is-Single-Valued</span></span>       | <span data-ttu-id="f42bc-240">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-240">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f42bc-241">Is Indexed</span></span>             | <span data-ttu-id="f42bc-242">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-242">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f42bc-243">In Global Catalog</span></span>      | <span data-ttu-id="f42bc-244">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-244">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f42bc-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="f42bc-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f42bc-246">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="f42bc-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f42bc-247">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f42bc-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f42bc-248">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f42bc-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bc-249">Search-Flags</span></span>           | <span data-ttu-id="f42bc-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bc-250">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f42bc-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bc-251">System-Flags</span></span>           | <span data-ttu-id="f42bc-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bc-252">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f42bc-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f42bc-253">Classes used in</span></span>        | [<span data-ttu-id="f42bc-254">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="f42bc-254">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="f42bc-255">**連接點**</span><span class="sxs-lookup"><span data-stu-id="f42bc-255">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f42bc-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f42bc-256">Windows Server 2012</span></span>



| <span data-ttu-id="f42bc-257">進入</span><span class="sxs-lookup"><span data-stu-id="f42bc-257">Entry</span></span> | <span data-ttu-id="f42bc-258">值</span><span class="sxs-lookup"><span data-stu-id="f42bc-258">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f42bc-259">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f42bc-259">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f42bc-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f42bc-260">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="f42bc-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="f42bc-261">System-Only</span></span>            | <span data-ttu-id="f42bc-262">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-262">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-263">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f42bc-263">Is-Single-Valued</span></span>       | <span data-ttu-id="f42bc-264">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-264">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-265">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f42bc-265">Is Indexed</span></span>             | <span data-ttu-id="f42bc-266">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-266">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-267">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f42bc-267">In Global Catalog</span></span>      | <span data-ttu-id="f42bc-268">否</span><span class="sxs-lookup"><span data-stu-id="f42bc-268">False</span></span>                                                                                                                     |
| <span data-ttu-id="f42bc-269">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f42bc-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="f42bc-270">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f42bc-270">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="f42bc-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f42bc-271">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f42bc-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f42bc-272">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="f42bc-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bc-273">Search-Flags</span></span>           | <span data-ttu-id="f42bc-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bc-274">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f42bc-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f42bc-275">System-Flags</span></span>           | <span data-ttu-id="f42bc-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f42bc-276">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="f42bc-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f42bc-277">Classes used in</span></span>        | [<span data-ttu-id="f42bc-278">**應用程式-設定**</span><span class="sxs-lookup"><span data-stu-id="f42bc-278">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="f42bc-279">**連接點**</span><span class="sxs-lookup"><span data-stu-id="f42bc-279">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



 

 





