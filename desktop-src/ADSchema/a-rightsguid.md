---
title: Rights-Guid 屬性
description: 用來代表存取控制專案內擴充許可權的 GUID。
ms.assetid: 6f3a654e-fead-41e7-8383-6dade1a2747e
ms.tgt_platform: multiple
keywords:
- Rights-Guid 屬性 AD 架構
- rightsGuid 屬性 AD 架構
topic_type:
- apiref
api_name:
- Rights-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da47ec8e4736dd13b6ba39da0208aed505aa8a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107961"
---
# <a name="rights-guid-attribute"></a><span data-ttu-id="81c96-105">Rights-Guid 屬性</span><span class="sxs-lookup"><span data-stu-id="81c96-105">Rights-Guid attribute</span></span>

<span data-ttu-id="81c96-106">用來代表存取控制專案內擴充許可權的 GUID。</span><span class="sxs-lookup"><span data-stu-id="81c96-106">The GUID used to represent an extended right within an access control entry.</span></span>



| <span data-ttu-id="81c96-107">進入</span><span class="sxs-lookup"><span data-stu-id="81c96-107">Entry</span></span> | <span data-ttu-id="81c96-108">值</span><span class="sxs-lookup"><span data-stu-id="81c96-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="81c96-109">CN</span><span class="sxs-lookup"><span data-stu-id="81c96-109">CN</span></span>                | <span data-ttu-id="81c96-110">Rights-Guid</span><span class="sxs-lookup"><span data-stu-id="81c96-110">Rights-Guid</span></span>                                 |
| <span data-ttu-id="81c96-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="81c96-111">Ldap-Display-Name</span></span> | <span data-ttu-id="81c96-112">rightsGuid</span><span class="sxs-lookup"><span data-stu-id="81c96-112">rightsGuid</span></span>                                  |
| <span data-ttu-id="81c96-113">大小</span><span class="sxs-lookup"><span data-stu-id="81c96-113">Size</span></span>              | <span data-ttu-id="81c96-114">16 個位元組</span><span class="sxs-lookup"><span data-stu-id="81c96-114">16 bytes</span></span>                                    |
| <span data-ttu-id="81c96-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="81c96-115">Update Privilege</span></span>  | <span data-ttu-id="81c96-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="81c96-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="81c96-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="81c96-117">Update Frequency</span></span>  | <span data-ttu-id="81c96-118">建立新的擴充許可權時。</span><span class="sxs-lookup"><span data-stu-id="81c96-118">When a new extended right is created.</span></span>       |
| <span data-ttu-id="81c96-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="81c96-119">Attribute-Id</span></span>      | <span data-ttu-id="81c96-120">1.2.840.113556.1.4.340</span><span class="sxs-lookup"><span data-stu-id="81c96-120">1.2.840.113556.1.4.340</span></span>                      |
| <span data-ttu-id="81c96-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="81c96-121">System-Id-Guid</span></span>    | <span data-ttu-id="81c96-122">8297931c-86d3-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="81c96-122">8297931c-86d3-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="81c96-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="81c96-123">Syntax</span></span>            | [<span data-ttu-id="81c96-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="81c96-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="81c96-125">實作</span><span class="sxs-lookup"><span data-stu-id="81c96-125">Implementations</span></span>

-   [<span data-ttu-id="81c96-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="81c96-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="81c96-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="81c96-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="81c96-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="81c96-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="81c96-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="81c96-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="81c96-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="81c96-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="81c96-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="81c96-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="81c96-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="81c96-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="81c96-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="81c96-133">Windows 2000 Server</span></span>



| <span data-ttu-id="81c96-134">進入</span><span class="sxs-lookup"><span data-stu-id="81c96-134">Entry</span></span> | <span data-ttu-id="81c96-135">值</span><span class="sxs-lookup"><span data-stu-id="81c96-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="81c96-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81c96-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81c96-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="81c96-138">System-Only</span></span>            | <span data-ttu-id="81c96-139">否</span><span class="sxs-lookup"><span data-stu-id="81c96-139">False</span></span>                                                           |
| <span data-ttu-id="81c96-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81c96-140">Is-Single-Valued</span></span>       | <span data-ttu-id="81c96-141">對</span><span class="sxs-lookup"><span data-stu-id="81c96-141">True</span></span>                                                            |
| <span data-ttu-id="81c96-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81c96-142">Is Indexed</span></span>             | <span data-ttu-id="81c96-143">否</span><span class="sxs-lookup"><span data-stu-id="81c96-143">False</span></span>                                                           |
| <span data-ttu-id="81c96-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81c96-144">In Global Catalog</span></span>      | <span data-ttu-id="81c96-145">否</span><span class="sxs-lookup"><span data-stu-id="81c96-145">False</span></span>                                                           |
| <span data-ttu-id="81c96-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81c96-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="81c96-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81c96-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="81c96-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81c96-148">Range-Lower</span></span>            | <span data-ttu-id="81c96-149">36</span><span class="sxs-lookup"><span data-stu-id="81c96-149">36</span></span>                                                              |
| <span data-ttu-id="81c96-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81c96-150">Range-Upper</span></span>            | <span data-ttu-id="81c96-151">36</span><span class="sxs-lookup"><span data-stu-id="81c96-151">36</span></span>                                                              |
| <span data-ttu-id="81c96-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-152">Search-Flags</span></span>           | <span data-ttu-id="81c96-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81c96-153">0x00000000</span></span>                                                      |
| <span data-ttu-id="81c96-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-154">System-Flags</span></span>           | <span data-ttu-id="81c96-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81c96-155">0x00000010</span></span>                                                      |
| <span data-ttu-id="81c96-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81c96-156">Classes used in</span></span>        | [<span data-ttu-id="81c96-157">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="81c96-157">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="81c96-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="81c96-158">Windows Server 2003</span></span>



| <span data-ttu-id="81c96-159">進入</span><span class="sxs-lookup"><span data-stu-id="81c96-159">Entry</span></span> | <span data-ttu-id="81c96-160">值</span><span class="sxs-lookup"><span data-stu-id="81c96-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="81c96-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81c96-161">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81c96-162">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="81c96-163">System-Only</span></span>            | <span data-ttu-id="81c96-164">否</span><span class="sxs-lookup"><span data-stu-id="81c96-164">False</span></span>                                                           |
| <span data-ttu-id="81c96-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81c96-165">Is-Single-Valued</span></span>       | <span data-ttu-id="81c96-166">對</span><span class="sxs-lookup"><span data-stu-id="81c96-166">True</span></span>                                                            |
| <span data-ttu-id="81c96-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81c96-167">Is Indexed</span></span>             | <span data-ttu-id="81c96-168">否</span><span class="sxs-lookup"><span data-stu-id="81c96-168">False</span></span>                                                           |
| <span data-ttu-id="81c96-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81c96-169">In Global Catalog</span></span>      | <span data-ttu-id="81c96-170">否</span><span class="sxs-lookup"><span data-stu-id="81c96-170">False</span></span>                                                           |
| <span data-ttu-id="81c96-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81c96-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="81c96-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81c96-172">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="81c96-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81c96-173">Range-Lower</span></span>            | <span data-ttu-id="81c96-174">36</span><span class="sxs-lookup"><span data-stu-id="81c96-174">36</span></span>                                                              |
| <span data-ttu-id="81c96-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81c96-175">Range-Upper</span></span>            | <span data-ttu-id="81c96-176">36</span><span class="sxs-lookup"><span data-stu-id="81c96-176">36</span></span>                                                              |
| <span data-ttu-id="81c96-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-177">Search-Flags</span></span>           | <span data-ttu-id="81c96-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81c96-178">0x00000000</span></span>                                                      |
| <span data-ttu-id="81c96-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-179">System-Flags</span></span>           | <span data-ttu-id="81c96-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81c96-180">0x00000010</span></span>                                                      |
| <span data-ttu-id="81c96-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81c96-181">Classes used in</span></span>        | [<span data-ttu-id="81c96-182">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="81c96-182">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="81c96-183">亞當</span><span class="sxs-lookup"><span data-stu-id="81c96-183">ADAM</span></span>



| <span data-ttu-id="81c96-184">進入</span><span class="sxs-lookup"><span data-stu-id="81c96-184">Entry</span></span> | <span data-ttu-id="81c96-185">值</span><span class="sxs-lookup"><span data-stu-id="81c96-185">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="81c96-186">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81c96-186">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81c96-187">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="81c96-188">System-Only</span></span>            | <span data-ttu-id="81c96-189">否</span><span class="sxs-lookup"><span data-stu-id="81c96-189">False</span></span>                                                           |
| <span data-ttu-id="81c96-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81c96-190">Is-Single-Valued</span></span>       | <span data-ttu-id="81c96-191">對</span><span class="sxs-lookup"><span data-stu-id="81c96-191">True</span></span>                                                            |
| <span data-ttu-id="81c96-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81c96-192">Is Indexed</span></span>             | <span data-ttu-id="81c96-193">否</span><span class="sxs-lookup"><span data-stu-id="81c96-193">False</span></span>                                                           |
| <span data-ttu-id="81c96-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81c96-194">In Global Catalog</span></span>      | <span data-ttu-id="81c96-195">否</span><span class="sxs-lookup"><span data-stu-id="81c96-195">False</span></span>                                                           |
| <span data-ttu-id="81c96-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81c96-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="81c96-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81c96-197">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="81c96-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81c96-198">Range-Lower</span></span>            | <span data-ttu-id="81c96-199">36</span><span class="sxs-lookup"><span data-stu-id="81c96-199">36</span></span>                                                              |
| <span data-ttu-id="81c96-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81c96-200">Range-Upper</span></span>            | <span data-ttu-id="81c96-201">36</span><span class="sxs-lookup"><span data-stu-id="81c96-201">36</span></span>                                                              |
| <span data-ttu-id="81c96-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-202">Search-Flags</span></span>           | <span data-ttu-id="81c96-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81c96-203">0x00000000</span></span>                                                      |
| <span data-ttu-id="81c96-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-204">System-Flags</span></span>           | <span data-ttu-id="81c96-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81c96-205">0x00000010</span></span>                                                      |
| <span data-ttu-id="81c96-206">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81c96-206">Classes used in</span></span>        | [<span data-ttu-id="81c96-207">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="81c96-207">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="81c96-208">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="81c96-208">Windows Server 2003 R2</span></span>



| <span data-ttu-id="81c96-209">進入</span><span class="sxs-lookup"><span data-stu-id="81c96-209">Entry</span></span> | <span data-ttu-id="81c96-210">值</span><span class="sxs-lookup"><span data-stu-id="81c96-210">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="81c96-211">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81c96-211">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81c96-212">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="81c96-213">System-Only</span></span>            | <span data-ttu-id="81c96-214">否</span><span class="sxs-lookup"><span data-stu-id="81c96-214">False</span></span>                                                           |
| <span data-ttu-id="81c96-215">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81c96-215">Is-Single-Valued</span></span>       | <span data-ttu-id="81c96-216">對</span><span class="sxs-lookup"><span data-stu-id="81c96-216">True</span></span>                                                            |
| <span data-ttu-id="81c96-217">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81c96-217">Is Indexed</span></span>             | <span data-ttu-id="81c96-218">否</span><span class="sxs-lookup"><span data-stu-id="81c96-218">False</span></span>                                                           |
| <span data-ttu-id="81c96-219">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81c96-219">In Global Catalog</span></span>      | <span data-ttu-id="81c96-220">否</span><span class="sxs-lookup"><span data-stu-id="81c96-220">False</span></span>                                                           |
| <span data-ttu-id="81c96-221">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81c96-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="81c96-222">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81c96-222">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="81c96-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81c96-223">Range-Lower</span></span>            | <span data-ttu-id="81c96-224">36</span><span class="sxs-lookup"><span data-stu-id="81c96-224">36</span></span>                                                              |
| <span data-ttu-id="81c96-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81c96-225">Range-Upper</span></span>            | <span data-ttu-id="81c96-226">36</span><span class="sxs-lookup"><span data-stu-id="81c96-226">36</span></span>                                                              |
| <span data-ttu-id="81c96-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-227">Search-Flags</span></span>           | <span data-ttu-id="81c96-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81c96-228">0x00000000</span></span>                                                      |
| <span data-ttu-id="81c96-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-229">System-Flags</span></span>           | <span data-ttu-id="81c96-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81c96-230">0x00000010</span></span>                                                      |
| <span data-ttu-id="81c96-231">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81c96-231">Classes used in</span></span>        | [<span data-ttu-id="81c96-232">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="81c96-232">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="81c96-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81c96-233">Windows Server 2008</span></span>



| <span data-ttu-id="81c96-234">進入</span><span class="sxs-lookup"><span data-stu-id="81c96-234">Entry</span></span> | <span data-ttu-id="81c96-235">值</span><span class="sxs-lookup"><span data-stu-id="81c96-235">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="81c96-236">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81c96-236">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81c96-237">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="81c96-238">System-Only</span></span>            | <span data-ttu-id="81c96-239">否</span><span class="sxs-lookup"><span data-stu-id="81c96-239">False</span></span>                                                           |
| <span data-ttu-id="81c96-240">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81c96-240">Is-Single-Valued</span></span>       | <span data-ttu-id="81c96-241">對</span><span class="sxs-lookup"><span data-stu-id="81c96-241">True</span></span>                                                            |
| <span data-ttu-id="81c96-242">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81c96-242">Is Indexed</span></span>             | <span data-ttu-id="81c96-243">否</span><span class="sxs-lookup"><span data-stu-id="81c96-243">False</span></span>                                                           |
| <span data-ttu-id="81c96-244">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81c96-244">In Global Catalog</span></span>      | <span data-ttu-id="81c96-245">否</span><span class="sxs-lookup"><span data-stu-id="81c96-245">False</span></span>                                                           |
| <span data-ttu-id="81c96-246">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81c96-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="81c96-247">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81c96-247">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="81c96-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81c96-248">Range-Lower</span></span>            | <span data-ttu-id="81c96-249">36</span><span class="sxs-lookup"><span data-stu-id="81c96-249">36</span></span>                                                              |
| <span data-ttu-id="81c96-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81c96-250">Range-Upper</span></span>            | <span data-ttu-id="81c96-251">36</span><span class="sxs-lookup"><span data-stu-id="81c96-251">36</span></span>                                                              |
| <span data-ttu-id="81c96-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-252">Search-Flags</span></span>           | <span data-ttu-id="81c96-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81c96-253">0x00000000</span></span>                                                      |
| <span data-ttu-id="81c96-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-254">System-Flags</span></span>           | <span data-ttu-id="81c96-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81c96-255">0x00000010</span></span>                                                      |
| <span data-ttu-id="81c96-256">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81c96-256">Classes used in</span></span>        | [<span data-ttu-id="81c96-257">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="81c96-257">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="81c96-258">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="81c96-258">Windows Server 2008 R2</span></span>



| <span data-ttu-id="81c96-259">進入</span><span class="sxs-lookup"><span data-stu-id="81c96-259">Entry</span></span> | <span data-ttu-id="81c96-260">值</span><span class="sxs-lookup"><span data-stu-id="81c96-260">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="81c96-261">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81c96-261">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81c96-262">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="81c96-263">System-Only</span></span>            | <span data-ttu-id="81c96-264">否</span><span class="sxs-lookup"><span data-stu-id="81c96-264">False</span></span>                                                           |
| <span data-ttu-id="81c96-265">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81c96-265">Is-Single-Valued</span></span>       | <span data-ttu-id="81c96-266">對</span><span class="sxs-lookup"><span data-stu-id="81c96-266">True</span></span>                                                            |
| <span data-ttu-id="81c96-267">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81c96-267">Is Indexed</span></span>             | <span data-ttu-id="81c96-268">否</span><span class="sxs-lookup"><span data-stu-id="81c96-268">False</span></span>                                                           |
| <span data-ttu-id="81c96-269">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81c96-269">In Global Catalog</span></span>      | <span data-ttu-id="81c96-270">否</span><span class="sxs-lookup"><span data-stu-id="81c96-270">False</span></span>                                                           |
| <span data-ttu-id="81c96-271">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81c96-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="81c96-272">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81c96-272">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="81c96-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81c96-273">Range-Lower</span></span>            | <span data-ttu-id="81c96-274">36</span><span class="sxs-lookup"><span data-stu-id="81c96-274">36</span></span>                                                              |
| <span data-ttu-id="81c96-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81c96-275">Range-Upper</span></span>            | <span data-ttu-id="81c96-276">36</span><span class="sxs-lookup"><span data-stu-id="81c96-276">36</span></span>                                                              |
| <span data-ttu-id="81c96-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-277">Search-Flags</span></span>           | <span data-ttu-id="81c96-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81c96-278">0x00000000</span></span>                                                      |
| <span data-ttu-id="81c96-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-279">System-Flags</span></span>           | <span data-ttu-id="81c96-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81c96-280">0x00000010</span></span>                                                      |
| <span data-ttu-id="81c96-281">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81c96-281">Classes used in</span></span>        | [<span data-ttu-id="81c96-282">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="81c96-282">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="81c96-283">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81c96-283">Windows Server 2012</span></span>



| <span data-ttu-id="81c96-284">進入</span><span class="sxs-lookup"><span data-stu-id="81c96-284">Entry</span></span> | <span data-ttu-id="81c96-285">值</span><span class="sxs-lookup"><span data-stu-id="81c96-285">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="81c96-286">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="81c96-286">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-287">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="81c96-287">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="81c96-288">System-Only</span><span class="sxs-lookup"><span data-stu-id="81c96-288">System-Only</span></span>            | <span data-ttu-id="81c96-289">否</span><span class="sxs-lookup"><span data-stu-id="81c96-289">False</span></span>                                                           |
| <span data-ttu-id="81c96-290">是-單一值</span><span class="sxs-lookup"><span data-stu-id="81c96-290">Is-Single-Valued</span></span>       | <span data-ttu-id="81c96-291">對</span><span class="sxs-lookup"><span data-stu-id="81c96-291">True</span></span>                                                            |
| <span data-ttu-id="81c96-292">已編制索引</span><span class="sxs-lookup"><span data-stu-id="81c96-292">Is Indexed</span></span>             | <span data-ttu-id="81c96-293">否</span><span class="sxs-lookup"><span data-stu-id="81c96-293">False</span></span>                                                           |
| <span data-ttu-id="81c96-294">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="81c96-294">In Global Catalog</span></span>      | <span data-ttu-id="81c96-295">否</span><span class="sxs-lookup"><span data-stu-id="81c96-295">False</span></span>                                                           |
| <span data-ttu-id="81c96-296">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="81c96-296">NT-Security-Descriptor</span></span> | <span data-ttu-id="81c96-297">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="81c96-297">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="81c96-298">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="81c96-298">Range-Lower</span></span>            | <span data-ttu-id="81c96-299">36</span><span class="sxs-lookup"><span data-stu-id="81c96-299">36</span></span>                                                              |
| <span data-ttu-id="81c96-300">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="81c96-300">Range-Upper</span></span>            | <span data-ttu-id="81c96-301">36</span><span class="sxs-lookup"><span data-stu-id="81c96-301">36</span></span>                                                              |
| <span data-ttu-id="81c96-302">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-302">Search-Flags</span></span>           | <span data-ttu-id="81c96-303">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81c96-303">0x00000000</span></span>                                                      |
| <span data-ttu-id="81c96-304">System-Flags</span><span class="sxs-lookup"><span data-stu-id="81c96-304">System-Flags</span></span>           | <span data-ttu-id="81c96-305">0x00000010</span><span class="sxs-lookup"><span data-stu-id="81c96-305">0x00000010</span></span>                                                      |
| <span data-ttu-id="81c96-306">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="81c96-306">Classes used in</span></span>        | [<span data-ttu-id="81c96-307">**Control-存取權限**</span><span class="sxs-lookup"><span data-stu-id="81c96-307">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





