---
title: ms-WMI-Name 屬性
description: 最上層原則物件的顯示名稱。 用於通用類別目錄中。
ms.assetid: 4c07e4ba-7f3f-4066-b4cd-2c6d738d7421
ms.tgt_platform: multiple
keywords:
- ms-WMI-Name 屬性 AD 架構
- msWMI-Name 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-WMI-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e49d5a57a9056e6f7201d3cdd53039c4f74b590f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107675"
---
# <a name="ms-wmi-name-attribute"></a><span data-ttu-id="e31f1-106">ms-WMI-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="e31f1-106">ms-WMI-Name attribute</span></span>

<span data-ttu-id="e31f1-107">最上層原則物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e31f1-107">The display name for top-level policy objects.</span></span> <span data-ttu-id="e31f1-108">用於通用類別目錄中。</span><span class="sxs-lookup"><span data-stu-id="e31f1-108">Used in the Global Catalog.</span></span>



| <span data-ttu-id="e31f1-109">進入</span><span class="sxs-lookup"><span data-stu-id="e31f1-109">Entry</span></span> | <span data-ttu-id="e31f1-110">值</span><span class="sxs-lookup"><span data-stu-id="e31f1-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e31f1-111">CN</span><span class="sxs-lookup"><span data-stu-id="e31f1-111">CN</span></span>                | <span data-ttu-id="e31f1-112">ms-WMI-名稱</span><span class="sxs-lookup"><span data-stu-id="e31f1-112">ms-WMI-Name</span></span>                                 |
| <span data-ttu-id="e31f1-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e31f1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e31f1-114">msWMI-名稱</span><span class="sxs-lookup"><span data-stu-id="e31f1-114">msWMI-Name</span></span>                                  |
| <span data-ttu-id="e31f1-115">大小</span><span class="sxs-lookup"><span data-stu-id="e31f1-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="e31f1-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e31f1-116">Update Privilege</span></span>  | <span data-ttu-id="e31f1-117">群組原則系統管理員</span><span class="sxs-lookup"><span data-stu-id="e31f1-117">Group Policy Administrator</span></span>                  |
| <span data-ttu-id="e31f1-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e31f1-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e31f1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e31f1-119">Attribute-Id</span></span>      | <span data-ttu-id="e31f1-120">1.2.840.113556.1.4.1639</span><span class="sxs-lookup"><span data-stu-id="e31f1-120">1.2.840.113556.1.4.1639</span></span>                     |
| <span data-ttu-id="e31f1-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e31f1-121">System-Id-Guid</span></span>    | <span data-ttu-id="e31f1-122">c6c8ace5-7e81-42af-ad72-77412c5941c4</span><span class="sxs-lookup"><span data-stu-id="e31f1-122">c6c8ace5-7e81-42af-ad72-77412c5941c4</span></span>        |
| <span data-ttu-id="e31f1-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e31f1-123">Syntax</span></span>            | [<span data-ttu-id="e31f1-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e31f1-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e31f1-125">實作</span><span class="sxs-lookup"><span data-stu-id="e31f1-125">Implementations</span></span>

-   [<span data-ttu-id="e31f1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e31f1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e31f1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e31f1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e31f1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e31f1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e31f1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e31f1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e31f1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e31f1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e31f1-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e31f1-131">Windows Server 2003</span></span>



| <span data-ttu-id="e31f1-132">進入</span><span class="sxs-lookup"><span data-stu-id="e31f1-132">Entry</span></span> | <span data-ttu-id="e31f1-133">值</span><span class="sxs-lookup"><span data-stu-id="e31f1-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31f1-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e31f1-134">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="e31f1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31f1-135">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="e31f1-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31f1-136">System-Only</span></span>            | <span data-ttu-id="e31f1-137">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-137">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e31f1-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e31f1-139">對</span><span class="sxs-lookup"><span data-stu-id="e31f1-139">True</span></span>                                                                                                            |
| <span data-ttu-id="e31f1-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e31f1-140">Is Indexed</span></span>             | <span data-ttu-id="e31f1-141">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-141">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e31f1-142">In Global Catalog</span></span>      | <span data-ttu-id="e31f1-143">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-143">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e31f1-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31f1-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e31f1-145">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="e31f1-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31f1-146">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="e31f1-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31f1-147">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="e31f1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31f1-148">Search-Flags</span></span>           | <span data-ttu-id="e31f1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31f1-149">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="e31f1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31f1-150">System-Flags</span></span>           | <span data-ttu-id="e31f1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31f1-151">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="e31f1-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e31f1-152">Classes used in</span></span>        | [<span data-ttu-id="e31f1-153">**PolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="e31f1-153">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> [<span data-ttu-id="e31f1-154">**ms-WMI-Som**</span><span class="sxs-lookup"><span data-stu-id="e31f1-154">**ms-WMI-Som**</span></span>](c-mswmi-som.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e31f1-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e31f1-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e31f1-156">進入</span><span class="sxs-lookup"><span data-stu-id="e31f1-156">Entry</span></span> | <span data-ttu-id="e31f1-157">值</span><span class="sxs-lookup"><span data-stu-id="e31f1-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31f1-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e31f1-158">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="e31f1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31f1-159">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="e31f1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31f1-160">System-Only</span></span>            | <span data-ttu-id="e31f1-161">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-161">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e31f1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="e31f1-163">對</span><span class="sxs-lookup"><span data-stu-id="e31f1-163">True</span></span>                                                                                                            |
| <span data-ttu-id="e31f1-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e31f1-164">Is Indexed</span></span>             | <span data-ttu-id="e31f1-165">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-165">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e31f1-166">In Global Catalog</span></span>      | <span data-ttu-id="e31f1-167">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-167">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e31f1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31f1-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e31f1-169">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="e31f1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31f1-170">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="e31f1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31f1-171">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="e31f1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31f1-172">Search-Flags</span></span>           | <span data-ttu-id="e31f1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31f1-173">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="e31f1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31f1-174">System-Flags</span></span>           | <span data-ttu-id="e31f1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31f1-175">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="e31f1-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e31f1-176">Classes used in</span></span>        | [<span data-ttu-id="e31f1-177">**PolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="e31f1-177">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> [<span data-ttu-id="e31f1-178">**ms-WMI-Som**</span><span class="sxs-lookup"><span data-stu-id="e31f1-178">**ms-WMI-Som**</span></span>](c-mswmi-som.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e31f1-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e31f1-179">Windows Server 2008</span></span>



| <span data-ttu-id="e31f1-180">進入</span><span class="sxs-lookup"><span data-stu-id="e31f1-180">Entry</span></span> | <span data-ttu-id="e31f1-181">值</span><span class="sxs-lookup"><span data-stu-id="e31f1-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31f1-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e31f1-182">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="e31f1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31f1-183">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="e31f1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31f1-184">System-Only</span></span>            | <span data-ttu-id="e31f1-185">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-185">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e31f1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e31f1-187">對</span><span class="sxs-lookup"><span data-stu-id="e31f1-187">True</span></span>                                                                                                            |
| <span data-ttu-id="e31f1-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e31f1-188">Is Indexed</span></span>             | <span data-ttu-id="e31f1-189">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-189">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e31f1-190">In Global Catalog</span></span>      | <span data-ttu-id="e31f1-191">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-191">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e31f1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31f1-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e31f1-193">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="e31f1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31f1-194">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="e31f1-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31f1-195">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="e31f1-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31f1-196">Search-Flags</span></span>           | <span data-ttu-id="e31f1-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31f1-197">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="e31f1-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31f1-198">System-Flags</span></span>           | <span data-ttu-id="e31f1-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31f1-199">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="e31f1-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e31f1-200">Classes used in</span></span>        | [<span data-ttu-id="e31f1-201">**PolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="e31f1-201">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> [<span data-ttu-id="e31f1-202">**ms-WMI-Som**</span><span class="sxs-lookup"><span data-stu-id="e31f1-202">**ms-WMI-Som**</span></span>](c-mswmi-som.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e31f1-203">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e31f1-203">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e31f1-204">進入</span><span class="sxs-lookup"><span data-stu-id="e31f1-204">Entry</span></span> | <span data-ttu-id="e31f1-205">值</span><span class="sxs-lookup"><span data-stu-id="e31f1-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31f1-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e31f1-206">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="e31f1-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31f1-207">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="e31f1-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31f1-208">System-Only</span></span>            | <span data-ttu-id="e31f1-209">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-209">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e31f1-210">Is-Single-Valued</span></span>       | <span data-ttu-id="e31f1-211">對</span><span class="sxs-lookup"><span data-stu-id="e31f1-211">True</span></span>                                                                                                            |
| <span data-ttu-id="e31f1-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e31f1-212">Is Indexed</span></span>             | <span data-ttu-id="e31f1-213">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-213">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e31f1-214">In Global Catalog</span></span>      | <span data-ttu-id="e31f1-215">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-215">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e31f1-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31f1-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e31f1-217">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="e31f1-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31f1-218">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="e31f1-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31f1-219">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="e31f1-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31f1-220">Search-Flags</span></span>           | <span data-ttu-id="e31f1-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31f1-221">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="e31f1-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31f1-222">System-Flags</span></span>           | <span data-ttu-id="e31f1-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31f1-223">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="e31f1-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e31f1-224">Classes used in</span></span>        | [<span data-ttu-id="e31f1-225">**PolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="e31f1-225">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> [<span data-ttu-id="e31f1-226">**ms-WMI-Som**</span><span class="sxs-lookup"><span data-stu-id="e31f1-226">**ms-WMI-Som**</span></span>](c-mswmi-som.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e31f1-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e31f1-227">Windows Server 2012</span></span>



| <span data-ttu-id="e31f1-228">進入</span><span class="sxs-lookup"><span data-stu-id="e31f1-228">Entry</span></span> | <span data-ttu-id="e31f1-229">值</span><span class="sxs-lookup"><span data-stu-id="e31f1-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31f1-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e31f1-230">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="e31f1-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e31f1-231">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="e31f1-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="e31f1-232">System-Only</span></span>            | <span data-ttu-id="e31f1-233">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-233">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e31f1-234">Is-Single-Valued</span></span>       | <span data-ttu-id="e31f1-235">對</span><span class="sxs-lookup"><span data-stu-id="e31f1-235">True</span></span>                                                                                                            |
| <span data-ttu-id="e31f1-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e31f1-236">Is Indexed</span></span>             | <span data-ttu-id="e31f1-237">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-237">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e31f1-238">In Global Catalog</span></span>      | <span data-ttu-id="e31f1-239">否</span><span class="sxs-lookup"><span data-stu-id="e31f1-239">False</span></span>                                                                                                           |
| <span data-ttu-id="e31f1-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e31f1-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="e31f1-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e31f1-241">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="e31f1-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e31f1-242">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="e31f1-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e31f1-243">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="e31f1-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e31f1-244">Search-Flags</span></span>           | <span data-ttu-id="e31f1-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e31f1-245">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="e31f1-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e31f1-246">System-Flags</span></span>           | <span data-ttu-id="e31f1-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e31f1-247">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="e31f1-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e31f1-248">Classes used in</span></span>        | [<span data-ttu-id="e31f1-249">**PolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="e31f1-249">**ms-WMI-PolicyTemplate**</span></span>](c-mswmi-policytemplate.md)<br/> [<span data-ttu-id="e31f1-250">**ms-WMI-Som**</span><span class="sxs-lookup"><span data-stu-id="e31f1-250">**ms-WMI-Som**</span></span>](c-mswmi-som.md)<br/> |



 

 





