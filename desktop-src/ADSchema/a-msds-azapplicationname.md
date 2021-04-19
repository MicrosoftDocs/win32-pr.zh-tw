---
title: ms-chap-Az-應用程式名稱屬性
description: 可唯一識別應用程式物件的字串。
ms.assetid: 693a47f4-d3ae-4fae-8e5e-cbce41d00d45
ms.tgt_platform: multiple
keywords:
- ms DS-Az-應用程式名稱屬性 AD 架構
- AzApplicationName 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Az-Application-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24166af15a250ec284eeb600b81bb8bb7d264369
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973527"
---
# <a name="ms-ds-az-application-name-attribute"></a><span data-ttu-id="fe9d3-105">ms-chap-Az-應用程式名稱屬性</span><span class="sxs-lookup"><span data-stu-id="fe9d3-105">ms-DS-Az-Application-Name attribute</span></span>

<span data-ttu-id="fe9d3-106">可唯一識別應用程式物件的字串。</span><span class="sxs-lookup"><span data-stu-id="fe9d3-106">A string that uniquely identifies an application object.</span></span>



| <span data-ttu-id="fe9d3-107">進入</span><span class="sxs-lookup"><span data-stu-id="fe9d3-107">Entry</span></span> | <span data-ttu-id="fe9d3-108">值</span><span class="sxs-lookup"><span data-stu-id="fe9d3-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="fe9d3-109">CN</span><span class="sxs-lookup"><span data-stu-id="fe9d3-109">CN</span></span>                | <span data-ttu-id="fe9d3-110">ms-DS-Az-應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="fe9d3-110">ms-DS-Az-Application-Name</span></span>                   |
| <span data-ttu-id="fe9d3-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fe9d3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fe9d3-112">AzApplicationName</span><span class="sxs-lookup"><span data-stu-id="fe9d3-112">msDS-AzApplicationName</span></span>                      |
| <span data-ttu-id="fe9d3-113">大小</span><span class="sxs-lookup"><span data-stu-id="fe9d3-113">Size</span></span>              | <span data-ttu-id="fe9d3-114">128 個字元</span><span class="sxs-lookup"><span data-stu-id="fe9d3-114">128 characters</span></span>                              |
| <span data-ttu-id="fe9d3-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fe9d3-115">Update Privilege</span></span>  | <span data-ttu-id="fe9d3-116">AzRoles 系統管理員</span><span class="sxs-lookup"><span data-stu-id="fe9d3-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="fe9d3-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fe9d3-117">Update Frequency</span></span>  | <span data-ttu-id="fe9d3-118">在初始化或原則變更期間。</span><span class="sxs-lookup"><span data-stu-id="fe9d3-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="fe9d3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fe9d3-119">Attribute-Id</span></span>      | <span data-ttu-id="fe9d3-120">1.2.840.113556.1.4.1798</span><span class="sxs-lookup"><span data-stu-id="fe9d3-120">1.2.840.113556.1.4.1798</span></span>                     |
| <span data-ttu-id="fe9d3-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fe9d3-121">System-Id-Guid</span></span>    | <span data-ttu-id="fe9d3-122">db5b0728-6208-4876-83b7-95d3e5695275</span><span class="sxs-lookup"><span data-stu-id="fe9d3-122">db5b0728-6208-4876-83b7-95d3e5695275</span></span>        |
| <span data-ttu-id="fe9d3-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe9d3-123">Syntax</span></span>            | [<span data-ttu-id="fe9d3-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fe9d3-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="fe9d3-125">實作</span><span class="sxs-lookup"><span data-stu-id="fe9d3-125">Implementations</span></span>

-   [<span data-ttu-id="fe9d3-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fe9d3-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fe9d3-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fe9d3-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fe9d3-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fe9d3-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fe9d3-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fe9d3-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fe9d3-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fe9d3-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="fe9d3-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe9d3-131">Windows Server 2003</span></span>



| <span data-ttu-id="fe9d3-132">進入</span><span class="sxs-lookup"><span data-stu-id="fe9d3-132">Entry</span></span> | <span data-ttu-id="fe9d3-133">值</span><span class="sxs-lookup"><span data-stu-id="fe9d3-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="fe9d3-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe9d3-134">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="fe9d3-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe9d3-135">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="fe9d3-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe9d3-136">System-Only</span></span>            | <span data-ttu-id="fe9d3-137">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-137">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe9d3-138">Is-Single-Valued</span></span>       | <span data-ttu-id="fe9d3-139">對</span><span class="sxs-lookup"><span data-stu-id="fe9d3-139">True</span></span>                                                            |
| <span data-ttu-id="fe9d3-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe9d3-140">Is Indexed</span></span>             | <span data-ttu-id="fe9d3-141">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-141">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe9d3-142">In Global Catalog</span></span>      | <span data-ttu-id="fe9d3-143">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-143">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe9d3-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe9d3-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe9d3-145">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="fe9d3-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe9d3-146">Range-Lower</span></span>            | <span data-ttu-id="fe9d3-147">0</span><span class="sxs-lookup"><span data-stu-id="fe9d3-147">0</span></span>                                                               |
| <span data-ttu-id="fe9d3-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe9d3-148">Range-Upper</span></span>            | <span data-ttu-id="fe9d3-149">512</span><span class="sxs-lookup"><span data-stu-id="fe9d3-149">512</span></span>                                                             |
| <span data-ttu-id="fe9d3-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe9d3-150">Search-Flags</span></span>           | <span data-ttu-id="fe9d3-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe9d3-151">0x00000000</span></span>                                                      |
| <span data-ttu-id="fe9d3-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe9d3-152">System-Flags</span></span>           | <span data-ttu-id="fe9d3-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe9d3-153">0x00000010</span></span>                                                      |
| <span data-ttu-id="fe9d3-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe9d3-154">Classes used in</span></span>        | [<span data-ttu-id="fe9d3-155">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="fe9d3-155">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fe9d3-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fe9d3-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fe9d3-157">進入</span><span class="sxs-lookup"><span data-stu-id="fe9d3-157">Entry</span></span> | <span data-ttu-id="fe9d3-158">值</span><span class="sxs-lookup"><span data-stu-id="fe9d3-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="fe9d3-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe9d3-159">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="fe9d3-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe9d3-160">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="fe9d3-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe9d3-161">System-Only</span></span>            | <span data-ttu-id="fe9d3-162">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-162">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe9d3-163">Is-Single-Valued</span></span>       | <span data-ttu-id="fe9d3-164">對</span><span class="sxs-lookup"><span data-stu-id="fe9d3-164">True</span></span>                                                            |
| <span data-ttu-id="fe9d3-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe9d3-165">Is Indexed</span></span>             | <span data-ttu-id="fe9d3-166">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-166">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe9d3-167">In Global Catalog</span></span>      | <span data-ttu-id="fe9d3-168">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-168">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe9d3-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe9d3-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe9d3-170">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="fe9d3-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe9d3-171">Range-Lower</span></span>            | <span data-ttu-id="fe9d3-172">0</span><span class="sxs-lookup"><span data-stu-id="fe9d3-172">0</span></span>                                                               |
| <span data-ttu-id="fe9d3-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe9d3-173">Range-Upper</span></span>            | <span data-ttu-id="fe9d3-174">512</span><span class="sxs-lookup"><span data-stu-id="fe9d3-174">512</span></span>                                                             |
| <span data-ttu-id="fe9d3-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe9d3-175">Search-Flags</span></span>           | <span data-ttu-id="fe9d3-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe9d3-176">0x00000000</span></span>                                                      |
| <span data-ttu-id="fe9d3-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe9d3-177">System-Flags</span></span>           | <span data-ttu-id="fe9d3-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe9d3-178">0x00000010</span></span>                                                      |
| <span data-ttu-id="fe9d3-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe9d3-179">Classes used in</span></span>        | [<span data-ttu-id="fe9d3-180">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="fe9d3-180">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fe9d3-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe9d3-181">Windows Server 2008</span></span>



| <span data-ttu-id="fe9d3-182">進入</span><span class="sxs-lookup"><span data-stu-id="fe9d3-182">Entry</span></span> | <span data-ttu-id="fe9d3-183">值</span><span class="sxs-lookup"><span data-stu-id="fe9d3-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="fe9d3-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe9d3-184">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="fe9d3-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe9d3-185">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="fe9d3-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe9d3-186">System-Only</span></span>            | <span data-ttu-id="fe9d3-187">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-187">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe9d3-188">Is-Single-Valued</span></span>       | <span data-ttu-id="fe9d3-189">對</span><span class="sxs-lookup"><span data-stu-id="fe9d3-189">True</span></span>                                                            |
| <span data-ttu-id="fe9d3-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe9d3-190">Is Indexed</span></span>             | <span data-ttu-id="fe9d3-191">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-191">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe9d3-192">In Global Catalog</span></span>      | <span data-ttu-id="fe9d3-193">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-193">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe9d3-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe9d3-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe9d3-195">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="fe9d3-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe9d3-196">Range-Lower</span></span>            | <span data-ttu-id="fe9d3-197">0</span><span class="sxs-lookup"><span data-stu-id="fe9d3-197">0</span></span>                                                               |
| <span data-ttu-id="fe9d3-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe9d3-198">Range-Upper</span></span>            | <span data-ttu-id="fe9d3-199">512</span><span class="sxs-lookup"><span data-stu-id="fe9d3-199">512</span></span>                                                             |
| <span data-ttu-id="fe9d3-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe9d3-200">Search-Flags</span></span>           | <span data-ttu-id="fe9d3-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe9d3-201">0x00000000</span></span>                                                      |
| <span data-ttu-id="fe9d3-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe9d3-202">System-Flags</span></span>           | <span data-ttu-id="fe9d3-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe9d3-203">0x00000010</span></span>                                                      |
| <span data-ttu-id="fe9d3-204">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe9d3-204">Classes used in</span></span>        | [<span data-ttu-id="fe9d3-205">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="fe9d3-205">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fe9d3-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fe9d3-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fe9d3-207">進入</span><span class="sxs-lookup"><span data-stu-id="fe9d3-207">Entry</span></span> | <span data-ttu-id="fe9d3-208">值</span><span class="sxs-lookup"><span data-stu-id="fe9d3-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="fe9d3-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe9d3-209">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="fe9d3-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe9d3-210">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="fe9d3-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe9d3-211">System-Only</span></span>            | <span data-ttu-id="fe9d3-212">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-212">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe9d3-213">Is-Single-Valued</span></span>       | <span data-ttu-id="fe9d3-214">對</span><span class="sxs-lookup"><span data-stu-id="fe9d3-214">True</span></span>                                                            |
| <span data-ttu-id="fe9d3-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe9d3-215">Is Indexed</span></span>             | <span data-ttu-id="fe9d3-216">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-216">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe9d3-217">In Global Catalog</span></span>      | <span data-ttu-id="fe9d3-218">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-218">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe9d3-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe9d3-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe9d3-220">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="fe9d3-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe9d3-221">Range-Lower</span></span>            | <span data-ttu-id="fe9d3-222">0</span><span class="sxs-lookup"><span data-stu-id="fe9d3-222">0</span></span>                                                               |
| <span data-ttu-id="fe9d3-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe9d3-223">Range-Upper</span></span>            | <span data-ttu-id="fe9d3-224">512</span><span class="sxs-lookup"><span data-stu-id="fe9d3-224">512</span></span>                                                             |
| <span data-ttu-id="fe9d3-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe9d3-225">Search-Flags</span></span>           | <span data-ttu-id="fe9d3-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe9d3-226">0x00000000</span></span>                                                      |
| <span data-ttu-id="fe9d3-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe9d3-227">System-Flags</span></span>           | <span data-ttu-id="fe9d3-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe9d3-228">0x00000010</span></span>                                                      |
| <span data-ttu-id="fe9d3-229">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe9d3-229">Classes used in</span></span>        | [<span data-ttu-id="fe9d3-230">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="fe9d3-230">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fe9d3-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fe9d3-231">Windows Server 2012</span></span>



| <span data-ttu-id="fe9d3-232">進入</span><span class="sxs-lookup"><span data-stu-id="fe9d3-232">Entry</span></span> | <span data-ttu-id="fe9d3-233">值</span><span class="sxs-lookup"><span data-stu-id="fe9d3-233">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="fe9d3-234">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fe9d3-234">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="fe9d3-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fe9d3-235">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="fe9d3-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="fe9d3-236">System-Only</span></span>            | <span data-ttu-id="fe9d3-237">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-237">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-238">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fe9d3-238">Is-Single-Valued</span></span>       | <span data-ttu-id="fe9d3-239">對</span><span class="sxs-lookup"><span data-stu-id="fe9d3-239">True</span></span>                                                            |
| <span data-ttu-id="fe9d3-240">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fe9d3-240">Is Indexed</span></span>             | <span data-ttu-id="fe9d3-241">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-241">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-242">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fe9d3-242">In Global Catalog</span></span>      | <span data-ttu-id="fe9d3-243">否</span><span class="sxs-lookup"><span data-stu-id="fe9d3-243">False</span></span>                                                           |
| <span data-ttu-id="fe9d3-244">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fe9d3-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="fe9d3-245">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fe9d3-245">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="fe9d3-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fe9d3-246">Range-Lower</span></span>            | <span data-ttu-id="fe9d3-247">0</span><span class="sxs-lookup"><span data-stu-id="fe9d3-247">0</span></span>                                                               |
| <span data-ttu-id="fe9d3-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fe9d3-248">Range-Upper</span></span>            | <span data-ttu-id="fe9d3-249">512</span><span class="sxs-lookup"><span data-stu-id="fe9d3-249">512</span></span>                                                             |
| <span data-ttu-id="fe9d3-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fe9d3-250">Search-Flags</span></span>           | <span data-ttu-id="fe9d3-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fe9d3-251">0x00000000</span></span>                                                      |
| <span data-ttu-id="fe9d3-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fe9d3-252">System-Flags</span></span>           | <span data-ttu-id="fe9d3-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fe9d3-253">0x00000010</span></span>                                                      |
| <span data-ttu-id="fe9d3-254">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fe9d3-254">Classes used in</span></span>        | [<span data-ttu-id="fe9d3-255">**ms DS-Az-應用程式**</span><span class="sxs-lookup"><span data-stu-id="fe9d3-255">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



 

 





