---
title: ms DS-篩選-容器屬性
description: 多重值的字串，其中包含類別名稱，這些類別是用來決定在篩選時應該由 Active Directory 消費者和電腦嵌入式管理單元顯示的容器類型。
ms.assetid: 765ac0e1-59d2-44a9-a01e-9cdf7d040c93
ms.tgt_platform: multiple
keywords:
- ms DS-篩選-容器屬性 AD 架構
- FilterContainers 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Filter-Containers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8156b1baa2fe86ec0322a9161ce5231a7e23f32e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108140"
---
# <a name="ms-ds-filter-containers-attribute"></a><span data-ttu-id="7a9f9-105">ms DS-篩選-容器屬性</span><span class="sxs-lookup"><span data-stu-id="7a9f9-105">ms-DS-Filter-Containers attribute</span></span>

<span data-ttu-id="7a9f9-106">多重值的字串，其中包含類別名稱，這些類別是用來決定在篩選時應該由 Active Directory 消費者和電腦嵌入式管理單元顯示的容器類型。</span><span class="sxs-lookup"><span data-stu-id="7a9f9-106">A multiple-valued string that contains the names of classes used to determine which container types should be shown by the Active Directory Users and Computers snap-in when filtering.</span></span>



| <span data-ttu-id="7a9f9-107">進入</span><span class="sxs-lookup"><span data-stu-id="7a9f9-107">Entry</span></span> | <span data-ttu-id="7a9f9-108">值</span><span class="sxs-lookup"><span data-stu-id="7a9f9-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7a9f9-109">CN</span><span class="sxs-lookup"><span data-stu-id="7a9f9-109">CN</span></span>                | <span data-ttu-id="7a9f9-110">ms-DS-篩選-容器</span><span class="sxs-lookup"><span data-stu-id="7a9f9-110">ms-DS-Filter-Containers</span></span>                     |
| <span data-ttu-id="7a9f9-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7a9f9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7a9f9-112">FilterContainers</span><span class="sxs-lookup"><span data-stu-id="7a9f9-112">msDS-FilterContainers</span></span>                       |
| <span data-ttu-id="7a9f9-113">大小</span><span class="sxs-lookup"><span data-stu-id="7a9f9-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="7a9f9-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7a9f9-114">Update Privilege</span></span>  | <span data-ttu-id="7a9f9-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="7a9f9-115">Domain administrator</span></span>                        |
| <span data-ttu-id="7a9f9-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7a9f9-116">Update Frequency</span></span>  | <span data-ttu-id="7a9f9-117">當容器類型清單變更時。</span><span class="sxs-lookup"><span data-stu-id="7a9f9-117">When the list of container types changes.</span></span>   |
| <span data-ttu-id="7a9f9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7a9f9-118">Attribute-Id</span></span>      | <span data-ttu-id="7a9f9-119">1.2.840.113556.1.4.1703</span><span class="sxs-lookup"><span data-stu-id="7a9f9-119">1.2.840.113556.1.4.1703</span></span>                     |
| <span data-ttu-id="7a9f9-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7a9f9-120">System-Id-Guid</span></span>    | <span data-ttu-id="7a9f9-121">fb00dcdf-ac37-483a-9c12-ac53a6603033</span><span class="sxs-lookup"><span data-stu-id="7a9f9-121">fb00dcdf-ac37-483a-9c12-ac53a6603033</span></span>        |
| <span data-ttu-id="7a9f9-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a9f9-122">Syntax</span></span>            | [<span data-ttu-id="7a9f9-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7a9f9-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7a9f9-124">實作</span><span class="sxs-lookup"><span data-stu-id="7a9f9-124">Implementations</span></span>

-   [<span data-ttu-id="7a9f9-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7a9f9-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7a9f9-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7a9f9-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7a9f9-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7a9f9-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7a9f9-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7a9f9-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7a9f9-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7a9f9-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="7a9f9-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7a9f9-130">Windows Server 2003</span></span>



| <span data-ttu-id="7a9f9-131">進入</span><span class="sxs-lookup"><span data-stu-id="7a9f9-131">Entry</span></span> | <span data-ttu-id="7a9f9-132">值</span><span class="sxs-lookup"><span data-stu-id="7a9f9-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="7a9f9-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7a9f9-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="7a9f9-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a9f9-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="7a9f9-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a9f9-135">System-Only</span></span>            | <span data-ttu-id="7a9f9-136">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-136">False</span></span>                                               |
| <span data-ttu-id="7a9f9-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7a9f9-137">Is-Single-Valued</span></span>       | <span data-ttu-id="7a9f9-138">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-138">False</span></span>                                               |
| <span data-ttu-id="7a9f9-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7a9f9-139">Is Indexed</span></span>             | <span data-ttu-id="7a9f9-140">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-140">False</span></span>                                               |
| <span data-ttu-id="7a9f9-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7a9f9-141">In Global Catalog</span></span>      | <span data-ttu-id="7a9f9-142">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-142">False</span></span>                                               |
| <span data-ttu-id="7a9f9-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7a9f9-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a9f9-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7a9f9-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="7a9f9-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a9f9-145">Range-Lower</span></span>            | <span data-ttu-id="7a9f9-146">1</span><span class="sxs-lookup"><span data-stu-id="7a9f9-146">1</span></span>                                                   |
| <span data-ttu-id="7a9f9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a9f9-147">Range-Upper</span></span>            | <span data-ttu-id="7a9f9-148">64</span><span class="sxs-lookup"><span data-stu-id="7a9f9-148">64</span></span>                                                  |
| <span data-ttu-id="7a9f9-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9f9-149">Search-Flags</span></span>           | <span data-ttu-id="7a9f9-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a9f9-150">0x00000000</span></span>                                          |
| <span data-ttu-id="7a9f9-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9f9-151">System-Flags</span></span>           | <span data-ttu-id="7a9f9-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a9f9-152">0x00000010</span></span>                                          |
| <span data-ttu-id="7a9f9-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7a9f9-153">Classes used in</span></span>        | [<span data-ttu-id="7a9f9-154">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="7a9f9-154">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7a9f9-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7a9f9-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7a9f9-156">進入</span><span class="sxs-lookup"><span data-stu-id="7a9f9-156">Entry</span></span> | <span data-ttu-id="7a9f9-157">值</span><span class="sxs-lookup"><span data-stu-id="7a9f9-157">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="7a9f9-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7a9f9-158">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="7a9f9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a9f9-159">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="7a9f9-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a9f9-160">System-Only</span></span>            | <span data-ttu-id="7a9f9-161">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-161">False</span></span>                                               |
| <span data-ttu-id="7a9f9-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7a9f9-162">Is-Single-Valued</span></span>       | <span data-ttu-id="7a9f9-163">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-163">False</span></span>                                               |
| <span data-ttu-id="7a9f9-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7a9f9-164">Is Indexed</span></span>             | <span data-ttu-id="7a9f9-165">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-165">False</span></span>                                               |
| <span data-ttu-id="7a9f9-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7a9f9-166">In Global Catalog</span></span>      | <span data-ttu-id="7a9f9-167">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-167">False</span></span>                                               |
| <span data-ttu-id="7a9f9-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7a9f9-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a9f9-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7a9f9-169">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="7a9f9-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a9f9-170">Range-Lower</span></span>            | <span data-ttu-id="7a9f9-171">1</span><span class="sxs-lookup"><span data-stu-id="7a9f9-171">1</span></span>                                                   |
| <span data-ttu-id="7a9f9-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a9f9-172">Range-Upper</span></span>            | <span data-ttu-id="7a9f9-173">64</span><span class="sxs-lookup"><span data-stu-id="7a9f9-173">64</span></span>                                                  |
| <span data-ttu-id="7a9f9-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9f9-174">Search-Flags</span></span>           | <span data-ttu-id="7a9f9-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a9f9-175">0x00000000</span></span>                                          |
| <span data-ttu-id="7a9f9-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9f9-176">System-Flags</span></span>           | <span data-ttu-id="7a9f9-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a9f9-177">0x00000010</span></span>                                          |
| <span data-ttu-id="7a9f9-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7a9f9-178">Classes used in</span></span>        | [<span data-ttu-id="7a9f9-179">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="7a9f9-179">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7a9f9-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a9f9-180">Windows Server 2008</span></span>



| <span data-ttu-id="7a9f9-181">進入</span><span class="sxs-lookup"><span data-stu-id="7a9f9-181">Entry</span></span> | <span data-ttu-id="7a9f9-182">值</span><span class="sxs-lookup"><span data-stu-id="7a9f9-182">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="7a9f9-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7a9f9-183">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="7a9f9-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a9f9-184">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="7a9f9-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a9f9-185">System-Only</span></span>            | <span data-ttu-id="7a9f9-186">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-186">False</span></span>                                               |
| <span data-ttu-id="7a9f9-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7a9f9-187">Is-Single-Valued</span></span>       | <span data-ttu-id="7a9f9-188">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-188">False</span></span>                                               |
| <span data-ttu-id="7a9f9-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7a9f9-189">Is Indexed</span></span>             | <span data-ttu-id="7a9f9-190">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-190">False</span></span>                                               |
| <span data-ttu-id="7a9f9-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7a9f9-191">In Global Catalog</span></span>      | <span data-ttu-id="7a9f9-192">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-192">False</span></span>                                               |
| <span data-ttu-id="7a9f9-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7a9f9-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a9f9-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7a9f9-194">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="7a9f9-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a9f9-195">Range-Lower</span></span>            | <span data-ttu-id="7a9f9-196">1</span><span class="sxs-lookup"><span data-stu-id="7a9f9-196">1</span></span>                                                   |
| <span data-ttu-id="7a9f9-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a9f9-197">Range-Upper</span></span>            | <span data-ttu-id="7a9f9-198">64</span><span class="sxs-lookup"><span data-stu-id="7a9f9-198">64</span></span>                                                  |
| <span data-ttu-id="7a9f9-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9f9-199">Search-Flags</span></span>           | <span data-ttu-id="7a9f9-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a9f9-200">0x00000000</span></span>                                          |
| <span data-ttu-id="7a9f9-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9f9-201">System-Flags</span></span>           | <span data-ttu-id="7a9f9-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a9f9-202">0x00000010</span></span>                                          |
| <span data-ttu-id="7a9f9-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7a9f9-203">Classes used in</span></span>        | [<span data-ttu-id="7a9f9-204">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="7a9f9-204">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7a9f9-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a9f9-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7a9f9-206">進入</span><span class="sxs-lookup"><span data-stu-id="7a9f9-206">Entry</span></span> | <span data-ttu-id="7a9f9-207">值</span><span class="sxs-lookup"><span data-stu-id="7a9f9-207">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="7a9f9-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7a9f9-208">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="7a9f9-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a9f9-209">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="7a9f9-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a9f9-210">System-Only</span></span>            | <span data-ttu-id="7a9f9-211">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-211">False</span></span>                                               |
| <span data-ttu-id="7a9f9-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7a9f9-212">Is-Single-Valued</span></span>       | <span data-ttu-id="7a9f9-213">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-213">False</span></span>                                               |
| <span data-ttu-id="7a9f9-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7a9f9-214">Is Indexed</span></span>             | <span data-ttu-id="7a9f9-215">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-215">False</span></span>                                               |
| <span data-ttu-id="7a9f9-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7a9f9-216">In Global Catalog</span></span>      | <span data-ttu-id="7a9f9-217">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-217">False</span></span>                                               |
| <span data-ttu-id="7a9f9-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7a9f9-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a9f9-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7a9f9-219">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="7a9f9-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a9f9-220">Range-Lower</span></span>            | <span data-ttu-id="7a9f9-221">1</span><span class="sxs-lookup"><span data-stu-id="7a9f9-221">1</span></span>                                                   |
| <span data-ttu-id="7a9f9-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a9f9-222">Range-Upper</span></span>            | <span data-ttu-id="7a9f9-223">64</span><span class="sxs-lookup"><span data-stu-id="7a9f9-223">64</span></span>                                                  |
| <span data-ttu-id="7a9f9-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9f9-224">Search-Flags</span></span>           | <span data-ttu-id="7a9f9-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a9f9-225">0x00000000</span></span>                                          |
| <span data-ttu-id="7a9f9-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9f9-226">System-Flags</span></span>           | <span data-ttu-id="7a9f9-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a9f9-227">0x00000010</span></span>                                          |
| <span data-ttu-id="7a9f9-228">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7a9f9-228">Classes used in</span></span>        | [<span data-ttu-id="7a9f9-229">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="7a9f9-229">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7a9f9-230">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a9f9-230">Windows Server 2012</span></span>



| <span data-ttu-id="7a9f9-231">進入</span><span class="sxs-lookup"><span data-stu-id="7a9f9-231">Entry</span></span> | <span data-ttu-id="7a9f9-232">值</span><span class="sxs-lookup"><span data-stu-id="7a9f9-232">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="7a9f9-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7a9f9-233">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="7a9f9-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7a9f9-234">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="7a9f9-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="7a9f9-235">System-Only</span></span>            | <span data-ttu-id="7a9f9-236">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-236">False</span></span>                                               |
| <span data-ttu-id="7a9f9-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7a9f9-237">Is-Single-Valued</span></span>       | <span data-ttu-id="7a9f9-238">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-238">False</span></span>                                               |
| <span data-ttu-id="7a9f9-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7a9f9-239">Is Indexed</span></span>             | <span data-ttu-id="7a9f9-240">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-240">False</span></span>                                               |
| <span data-ttu-id="7a9f9-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7a9f9-241">In Global Catalog</span></span>      | <span data-ttu-id="7a9f9-242">否</span><span class="sxs-lookup"><span data-stu-id="7a9f9-242">False</span></span>                                               |
| <span data-ttu-id="7a9f9-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7a9f9-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="7a9f9-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7a9f9-244">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="7a9f9-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7a9f9-245">Range-Lower</span></span>            | <span data-ttu-id="7a9f9-246">1</span><span class="sxs-lookup"><span data-stu-id="7a9f9-246">1</span></span>                                                   |
| <span data-ttu-id="7a9f9-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7a9f9-247">Range-Upper</span></span>            | <span data-ttu-id="7a9f9-248">64</span><span class="sxs-lookup"><span data-stu-id="7a9f9-248">64</span></span>                                                  |
| <span data-ttu-id="7a9f9-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9f9-249">Search-Flags</span></span>           | <span data-ttu-id="7a9f9-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7a9f9-250">0x00000000</span></span>                                          |
| <span data-ttu-id="7a9f9-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7a9f9-251">System-Flags</span></span>           | <span data-ttu-id="7a9f9-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a9f9-252">0x00000010</span></span>                                          |
| <span data-ttu-id="7a9f9-253">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7a9f9-253">Classes used in</span></span>        | [<span data-ttu-id="7a9f9-254">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="7a9f9-254">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



 

 





