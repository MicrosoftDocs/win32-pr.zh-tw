---
title: ms DS-慣用-GC-Site 屬性
description: 在權杖評估期間，安全性帳戶管理員會使用 ms DS 慣用的 GC-Site 屬性進行群組擴充。
ms.assetid: f42d3787-4063-4804-a7b5-4798516ad47e
ms.tgt_platform: multiple
keywords:
- ms DS-慣用-GC-Site attribute AD 架構
- 慣用-GC-Site attribute AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Preferred-GC-Site
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172e12758ba0b365fa195cb4e1384c161cea3d14
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104187340"
---
# <a name="ms-ds-preferred-gc-site-attribute"></a><span data-ttu-id="a8cc8-105">ms DS-慣用-GC-Site 屬性</span><span class="sxs-lookup"><span data-stu-id="a8cc8-105">ms-DS-Preferred-GC-Site attribute</span></span>

<span data-ttu-id="a8cc8-106">在權杖評估期間，安全性帳戶管理員會使用 **MS DS 慣用的 GC-Site** 屬性進行群組擴充。</span><span class="sxs-lookup"><span data-stu-id="a8cc8-106">The **ms-DS-Preferred-GC-Site** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="a8cc8-107">進入</span><span class="sxs-lookup"><span data-stu-id="a8cc8-107">Entry</span></span> | <span data-ttu-id="a8cc8-108">值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="a8cc8-109">CN</span><span class="sxs-lookup"><span data-stu-id="a8cc8-109">CN</span></span>                | <span data-ttu-id="a8cc8-110">ms DS-慣用-GC-網站</span><span class="sxs-lookup"><span data-stu-id="a8cc8-110">ms-DS-Preferred-GC-Site</span></span>                 |
| <span data-ttu-id="a8cc8-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a8cc8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a8cc8-112">慣用-GC-網站</span><span class="sxs-lookup"><span data-stu-id="a8cc8-112">msDS-Preferred-GC-Site</span></span>                  |
| <span data-ttu-id="a8cc8-113">大小</span><span class="sxs-lookup"><span data-stu-id="a8cc8-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="a8cc8-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a8cc8-114">Update Privilege</span></span>  | <span data-ttu-id="a8cc8-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="a8cc8-115">Domain administrator</span></span>                    |
| <span data-ttu-id="a8cc8-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a8cc8-116">Update Frequency</span></span>  | <span data-ttu-id="a8cc8-117">以系統管理員的身分來決定。</span><span class="sxs-lookup"><span data-stu-id="a8cc8-117">At the administrator's discretion.</span></span>      |
| <span data-ttu-id="a8cc8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a8cc8-118">Attribute-Id</span></span>      | <span data-ttu-id="a8cc8-119">1.2.840.113556.1.4.1444</span><span class="sxs-lookup"><span data-stu-id="a8cc8-119">1.2.840.113556.1.4.1444</span></span>                 |
| <span data-ttu-id="a8cc8-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a8cc8-120">System-Id-Guid</span></span>    | <span data-ttu-id="a8cc8-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span><span class="sxs-lookup"><span data-stu-id="a8cc8-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span></span>    |
| <span data-ttu-id="a8cc8-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8cc8-122">Syntax</span></span>            | [<span data-ttu-id="a8cc8-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="a8cc8-124">實作</span><span class="sxs-lookup"><span data-stu-id="a8cc8-124">Implementations</span></span>

-   [<span data-ttu-id="a8cc8-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a8cc8-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a8cc8-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a8cc8-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a8cc8-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a8cc8-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a8cc8-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8cc8-131">Windows Server 2003</span></span>



| <span data-ttu-id="a8cc8-132">進入</span><span class="sxs-lookup"><span data-stu-id="a8cc8-132">Entry</span></span> | <span data-ttu-id="a8cc8-133">值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a8cc8-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a8cc8-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a8cc8-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8cc8-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a8cc8-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8cc8-136">System-Only</span></span>            | <span data-ttu-id="a8cc8-137">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-137">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a8cc8-139">對</span><span class="sxs-lookup"><span data-stu-id="a8cc8-139">True</span></span>                                                        |
| <span data-ttu-id="a8cc8-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a8cc8-140">Is Indexed</span></span>             | <span data-ttu-id="a8cc8-141">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-141">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a8cc8-142">In Global Catalog</span></span>      | <span data-ttu-id="a8cc8-143">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-143">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a8cc8-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8cc8-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a8cc8-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a8cc8-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8cc8-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a8cc8-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8cc8-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a8cc8-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8cc8-148">Search-Flags</span></span>           | <span data-ttu-id="a8cc8-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8cc8-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="a8cc8-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8cc8-150">System-Flags</span></span>           | <span data-ttu-id="a8cc8-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8cc8-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="a8cc8-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a8cc8-152">Classes used in</span></span>        | [<span data-ttu-id="a8cc8-153">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a8cc8-154">亞當</span><span class="sxs-lookup"><span data-stu-id="a8cc8-154">ADAM</span></span>



| <span data-ttu-id="a8cc8-155">進入</span><span class="sxs-lookup"><span data-stu-id="a8cc8-155">Entry</span></span> | <span data-ttu-id="a8cc8-156">值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a8cc8-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a8cc8-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a8cc8-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8cc8-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a8cc8-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8cc8-159">System-Only</span></span>            | <span data-ttu-id="a8cc8-160">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-160">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a8cc8-162">對</span><span class="sxs-lookup"><span data-stu-id="a8cc8-162">True</span></span>                                                        |
| <span data-ttu-id="a8cc8-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a8cc8-163">Is Indexed</span></span>             | <span data-ttu-id="a8cc8-164">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-164">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a8cc8-165">In Global Catalog</span></span>      | <span data-ttu-id="a8cc8-166">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-166">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a8cc8-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8cc8-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a8cc8-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a8cc8-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8cc8-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a8cc8-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8cc8-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a8cc8-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8cc8-171">Search-Flags</span></span>           | <span data-ttu-id="a8cc8-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8cc8-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="a8cc8-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8cc8-173">System-Flags</span></span>           | <span data-ttu-id="a8cc8-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8cc8-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="a8cc8-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a8cc8-175">Classes used in</span></span>        | [<span data-ttu-id="a8cc8-176">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a8cc8-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a8cc8-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a8cc8-178">進入</span><span class="sxs-lookup"><span data-stu-id="a8cc8-178">Entry</span></span> | <span data-ttu-id="a8cc8-179">值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a8cc8-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a8cc8-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a8cc8-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8cc8-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a8cc8-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8cc8-182">System-Only</span></span>            | <span data-ttu-id="a8cc8-183">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-183">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a8cc8-185">對</span><span class="sxs-lookup"><span data-stu-id="a8cc8-185">True</span></span>                                                        |
| <span data-ttu-id="a8cc8-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a8cc8-186">Is Indexed</span></span>             | <span data-ttu-id="a8cc8-187">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-187">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a8cc8-188">In Global Catalog</span></span>      | <span data-ttu-id="a8cc8-189">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-189">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a8cc8-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8cc8-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a8cc8-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a8cc8-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8cc8-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a8cc8-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8cc8-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a8cc8-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8cc8-194">Search-Flags</span></span>           | <span data-ttu-id="a8cc8-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8cc8-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="a8cc8-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8cc8-196">System-Flags</span></span>           | <span data-ttu-id="a8cc8-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8cc8-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="a8cc8-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a8cc8-198">Classes used in</span></span>        | [<span data-ttu-id="a8cc8-199">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a8cc8-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8cc8-200">Windows Server 2008</span></span>



| <span data-ttu-id="a8cc8-201">進入</span><span class="sxs-lookup"><span data-stu-id="a8cc8-201">Entry</span></span> | <span data-ttu-id="a8cc8-202">值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a8cc8-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a8cc8-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a8cc8-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8cc8-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a8cc8-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8cc8-205">System-Only</span></span>            | <span data-ttu-id="a8cc8-206">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-206">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a8cc8-208">對</span><span class="sxs-lookup"><span data-stu-id="a8cc8-208">True</span></span>                                                        |
| <span data-ttu-id="a8cc8-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a8cc8-209">Is Indexed</span></span>             | <span data-ttu-id="a8cc8-210">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-210">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a8cc8-211">In Global Catalog</span></span>      | <span data-ttu-id="a8cc8-212">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-212">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a8cc8-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8cc8-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a8cc8-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a8cc8-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8cc8-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a8cc8-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8cc8-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a8cc8-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8cc8-217">Search-Flags</span></span>           | <span data-ttu-id="a8cc8-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8cc8-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="a8cc8-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8cc8-219">System-Flags</span></span>           | <span data-ttu-id="a8cc8-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8cc8-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="a8cc8-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a8cc8-221">Classes used in</span></span>        | [<span data-ttu-id="a8cc8-222">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a8cc8-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a8cc8-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a8cc8-224">進入</span><span class="sxs-lookup"><span data-stu-id="a8cc8-224">Entry</span></span> | <span data-ttu-id="a8cc8-225">值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a8cc8-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a8cc8-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a8cc8-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8cc8-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a8cc8-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8cc8-228">System-Only</span></span>            | <span data-ttu-id="a8cc8-229">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-229">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a8cc8-231">對</span><span class="sxs-lookup"><span data-stu-id="a8cc8-231">True</span></span>                                                        |
| <span data-ttu-id="a8cc8-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a8cc8-232">Is Indexed</span></span>             | <span data-ttu-id="a8cc8-233">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-233">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a8cc8-234">In Global Catalog</span></span>      | <span data-ttu-id="a8cc8-235">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-235">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a8cc8-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8cc8-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a8cc8-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a8cc8-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8cc8-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a8cc8-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8cc8-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a8cc8-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8cc8-240">Search-Flags</span></span>           | <span data-ttu-id="a8cc8-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8cc8-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="a8cc8-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8cc8-242">System-Flags</span></span>           | <span data-ttu-id="a8cc8-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8cc8-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="a8cc8-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a8cc8-244">Classes used in</span></span>        | [<span data-ttu-id="a8cc8-245">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a8cc8-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8cc8-246">Windows Server 2012</span></span>



| <span data-ttu-id="a8cc8-247">進入</span><span class="sxs-lookup"><span data-stu-id="a8cc8-247">Entry</span></span> | <span data-ttu-id="a8cc8-248">值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a8cc8-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a8cc8-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a8cc8-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8cc8-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="a8cc8-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8cc8-251">System-Only</span></span>            | <span data-ttu-id="a8cc8-252">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-252">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a8cc8-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a8cc8-254">對</span><span class="sxs-lookup"><span data-stu-id="a8cc8-254">True</span></span>                                                        |
| <span data-ttu-id="a8cc8-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a8cc8-255">Is Indexed</span></span>             | <span data-ttu-id="a8cc8-256">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-256">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a8cc8-257">In Global Catalog</span></span>      | <span data-ttu-id="a8cc8-258">否</span><span class="sxs-lookup"><span data-stu-id="a8cc8-258">False</span></span>                                                       |
| <span data-ttu-id="a8cc8-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a8cc8-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8cc8-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a8cc8-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="a8cc8-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8cc8-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="a8cc8-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8cc8-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="a8cc8-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8cc8-263">Search-Flags</span></span>           | <span data-ttu-id="a8cc8-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a8cc8-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="a8cc8-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8cc8-265">System-Flags</span></span>           | <span data-ttu-id="a8cc8-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8cc8-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="a8cc8-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a8cc8-267">Classes used in</span></span>        | [<span data-ttu-id="a8cc8-268">**NTDS-Site-設定**</span><span class="sxs-lookup"><span data-stu-id="a8cc8-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





