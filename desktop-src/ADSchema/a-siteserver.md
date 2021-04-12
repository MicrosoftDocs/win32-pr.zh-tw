---
title: Site-Server 屬性
description: 授權主伺服器以取得指定的網站。
ms.assetid: bcae8c63-a953-4721-b2d1-96d0376592c6
ms.tgt_platform: multiple
keywords:
- Site-Server 屬性 AD 架構
- siteServer 屬性 AD 架構
topic_type:
- apiref
api_name:
- Site-Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785057cd9ea23c05d58541450dc4c92a502877e5
ms.sourcegitcommit: f10bb95039c20a9de79f21e3fcb93a543f30a00e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "104187368"
---
# <a name="site-server-attribute"></a><span data-ttu-id="9eb7c-105">Site-Server 屬性</span><span class="sxs-lookup"><span data-stu-id="9eb7c-105">Site-Server attribute</span></span>

<span data-ttu-id="9eb7c-106">授權主伺服器以取得指定的網站。</span><span class="sxs-lookup"><span data-stu-id="9eb7c-106">Licensing main server for a given Site.</span></span>



| <span data-ttu-id="9eb7c-107">進入</span><span class="sxs-lookup"><span data-stu-id="9eb7c-107">Entry</span></span> | <span data-ttu-id="9eb7c-108">值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-108">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="9eb7c-109">CN</span><span class="sxs-lookup"><span data-stu-id="9eb7c-109">CN</span></span>                | <span data-ttu-id="9eb7c-110">Site-Server</span><span class="sxs-lookup"><span data-stu-id="9eb7c-110">Site-Server</span></span>                                  |
| <span data-ttu-id="9eb7c-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9eb7c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9eb7c-112">siteServer</span><span class="sxs-lookup"><span data-stu-id="9eb7c-112">siteServer</span></span>                                   |
| <span data-ttu-id="9eb7c-113">大小</span><span class="sxs-lookup"><span data-stu-id="9eb7c-113">Size</span></span>              | \-                                           |
| <span data-ttu-id="9eb7c-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9eb7c-114">Update Privilege</span></span>  | <span data-ttu-id="9eb7c-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="9eb7c-115">Domain administrator</span></span>                         |
| <span data-ttu-id="9eb7c-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9eb7c-116">Update Frequency</span></span>  | <span data-ttu-id="9eb7c-117">每次需要變更授權網站。</span><span class="sxs-lookup"><span data-stu-id="9eb7c-117">Whenever the licensing site needs to change.</span></span> |
| <span data-ttu-id="9eb7c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9eb7c-118">Attribute-Id</span></span>      | <span data-ttu-id="9eb7c-119">1.2.840.113556.1.4.494</span><span class="sxs-lookup"><span data-stu-id="9eb7c-119">1.2.840.113556.1.4.494</span></span>                       |
| <span data-ttu-id="9eb7c-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9eb7c-120">System-Id-Guid</span></span>    | <span data-ttu-id="9eb7c-121">1be8f17c-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="9eb7c-121">1be8f17c-a9ff-11d0-afe2-00c04fd930c9</span></span>         |
| <span data-ttu-id="9eb7c-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="9eb7c-122">Syntax</span></span>            | [<span data-ttu-id="9eb7c-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)      |



## <a name="implementations"></a><span data-ttu-id="9eb7c-124">實作</span><span class="sxs-lookup"><span data-stu-id="9eb7c-124">Implementations</span></span>

-   [<span data-ttu-id="9eb7c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9eb7c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9eb7c-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9eb7c-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9eb7c-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9eb7c-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9eb7c-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9eb7c-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9eb7c-132">Windows 2000 Server</span></span>



| <span data-ttu-id="9eb7c-133">進入</span><span class="sxs-lookup"><span data-stu-id="9eb7c-133">Entry</span></span> | <span data-ttu-id="9eb7c-134">值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9eb7c-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9eb7c-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9eb7c-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb7c-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9eb7c-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb7c-137">System-Only</span></span>            | <span data-ttu-id="9eb7c-138">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-138">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb7c-140">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-140">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9eb7c-141">Is Indexed</span></span>             | <span data-ttu-id="9eb7c-142">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-142">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9eb7c-143">In Global Catalog</span></span>      | <span data-ttu-id="9eb7c-144">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-144">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9eb7c-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb7c-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9eb7c-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="9eb7c-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb7c-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="9eb7c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb7c-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="9eb7c-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-149">Search-Flags</span></span>           | <span data-ttu-id="9eb7c-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb7c-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="9eb7c-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-151">System-Flags</span></span>           | <span data-ttu-id="9eb7c-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb7c-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="9eb7c-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9eb7c-153">Classes used in</span></span>        | [<span data-ttu-id="9eb7c-154">**授權-網站-設定**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-154">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9eb7c-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9eb7c-155">Windows Server 2003</span></span>



| <span data-ttu-id="9eb7c-156">進入</span><span class="sxs-lookup"><span data-stu-id="9eb7c-156">Entry</span></span> | <span data-ttu-id="9eb7c-157">值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9eb7c-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9eb7c-158">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9eb7c-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb7c-159">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9eb7c-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb7c-160">System-Only</span></span>            | <span data-ttu-id="9eb7c-161">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-161">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-162">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb7c-163">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-163">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9eb7c-164">Is Indexed</span></span>             | <span data-ttu-id="9eb7c-165">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-165">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9eb7c-166">In Global Catalog</span></span>      | <span data-ttu-id="9eb7c-167">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-167">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9eb7c-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb7c-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9eb7c-169">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="9eb7c-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb7c-170">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="9eb7c-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb7c-171">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="9eb7c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-172">Search-Flags</span></span>           | <span data-ttu-id="9eb7c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb7c-173">0x00000000</span></span>                                                            |
| <span data-ttu-id="9eb7c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-174">System-Flags</span></span>           | <span data-ttu-id="9eb7c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb7c-175">0x00000010</span></span>                                                            |
| <span data-ttu-id="9eb7c-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9eb7c-176">Classes used in</span></span>        | [<span data-ttu-id="9eb7c-177">**授權-網站-設定**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-177">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9eb7c-178">亞當</span><span class="sxs-lookup"><span data-stu-id="9eb7c-178">ADAM</span></span>



| <span data-ttu-id="9eb7c-179">進入</span><span class="sxs-lookup"><span data-stu-id="9eb7c-179">Entry</span></span> | <span data-ttu-id="9eb7c-180">值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-180">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="9eb7c-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9eb7c-181">Link-Id</span></span>                | \-           |
| <span data-ttu-id="9eb7c-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb7c-182">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="9eb7c-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb7c-183">System-Only</span></span>            | <span data-ttu-id="9eb7c-184">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-184">False</span></span>        |
| <span data-ttu-id="9eb7c-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-185">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb7c-186">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-186">False</span></span>        |
| <span data-ttu-id="9eb7c-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9eb7c-187">Is Indexed</span></span>             | <span data-ttu-id="9eb7c-188">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-188">False</span></span>        |
| <span data-ttu-id="9eb7c-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9eb7c-189">In Global Catalog</span></span>      | <span data-ttu-id="9eb7c-190">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-190">False</span></span>        |
| <span data-ttu-id="9eb7c-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9eb7c-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb7c-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9eb7c-192">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="9eb7c-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb7c-193">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="9eb7c-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb7c-194">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="9eb7c-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-195">Search-Flags</span></span>           | <span data-ttu-id="9eb7c-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb7c-196">0x00000000</span></span>   |
| <span data-ttu-id="9eb7c-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-197">System-Flags</span></span>           | <span data-ttu-id="9eb7c-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb7c-198">0x00000010</span></span>   |
| <span data-ttu-id="9eb7c-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9eb7c-199">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9eb7c-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9eb7c-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9eb7c-201">進入</span><span class="sxs-lookup"><span data-stu-id="9eb7c-201">Entry</span></span> | <span data-ttu-id="9eb7c-202">值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-202">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9eb7c-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9eb7c-203">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9eb7c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb7c-204">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9eb7c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb7c-205">System-Only</span></span>            | <span data-ttu-id="9eb7c-206">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-206">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb7c-208">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-208">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9eb7c-209">Is Indexed</span></span>             | <span data-ttu-id="9eb7c-210">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-210">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9eb7c-211">In Global Catalog</span></span>      | <span data-ttu-id="9eb7c-212">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-212">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9eb7c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb7c-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9eb7c-214">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="9eb7c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb7c-215">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="9eb7c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb7c-216">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="9eb7c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-217">Search-Flags</span></span>           | <span data-ttu-id="9eb7c-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb7c-218">0x00000000</span></span>                                                            |
| <span data-ttu-id="9eb7c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-219">System-Flags</span></span>           | <span data-ttu-id="9eb7c-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb7c-220">0x00000010</span></span>                                                            |
| <span data-ttu-id="9eb7c-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9eb7c-221">Classes used in</span></span>        | [<span data-ttu-id="9eb7c-222">**授權-網站-設定**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-222">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9eb7c-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9eb7c-223">Windows Server 2008</span></span>



| <span data-ttu-id="9eb7c-224">進入</span><span class="sxs-lookup"><span data-stu-id="9eb7c-224">Entry</span></span> | <span data-ttu-id="9eb7c-225">值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-225">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9eb7c-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9eb7c-226">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9eb7c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb7c-227">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9eb7c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb7c-228">System-Only</span></span>            | <span data-ttu-id="9eb7c-229">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-229">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb7c-231">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-231">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9eb7c-232">Is Indexed</span></span>             | <span data-ttu-id="9eb7c-233">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-233">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9eb7c-234">In Global Catalog</span></span>      | <span data-ttu-id="9eb7c-235">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-235">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9eb7c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb7c-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9eb7c-237">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="9eb7c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb7c-238">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="9eb7c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb7c-239">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="9eb7c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-240">Search-Flags</span></span>           | <span data-ttu-id="9eb7c-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb7c-241">0x00000000</span></span>                                                            |
| <span data-ttu-id="9eb7c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-242">System-Flags</span></span>           | <span data-ttu-id="9eb7c-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb7c-243">0x00000010</span></span>                                                            |
| <span data-ttu-id="9eb7c-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9eb7c-244">Classes used in</span></span>        | [<span data-ttu-id="9eb7c-245">**授權-網站-設定**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-245">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9eb7c-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9eb7c-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9eb7c-247">進入</span><span class="sxs-lookup"><span data-stu-id="9eb7c-247">Entry</span></span> | <span data-ttu-id="9eb7c-248">值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-248">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9eb7c-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9eb7c-249">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9eb7c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb7c-250">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9eb7c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb7c-251">System-Only</span></span>            | <span data-ttu-id="9eb7c-252">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-252">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb7c-254">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-254">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9eb7c-255">Is Indexed</span></span>             | <span data-ttu-id="9eb7c-256">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-256">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9eb7c-257">In Global Catalog</span></span>      | <span data-ttu-id="9eb7c-258">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-258">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9eb7c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb7c-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9eb7c-260">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="9eb7c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb7c-261">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="9eb7c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb7c-262">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="9eb7c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-263">Search-Flags</span></span>           | <span data-ttu-id="9eb7c-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb7c-264">0x00000000</span></span>                                                            |
| <span data-ttu-id="9eb7c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-265">System-Flags</span></span>           | <span data-ttu-id="9eb7c-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb7c-266">0x00000010</span></span>                                                            |
| <span data-ttu-id="9eb7c-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9eb7c-267">Classes used in</span></span>        | [<span data-ttu-id="9eb7c-268">**授權-網站-設定**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-268">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9eb7c-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9eb7c-269">Windows Server 2012</span></span>



| <span data-ttu-id="9eb7c-270">進入</span><span class="sxs-lookup"><span data-stu-id="9eb7c-270">Entry</span></span> | <span data-ttu-id="9eb7c-271">值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-271">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9eb7c-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9eb7c-272">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9eb7c-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9eb7c-273">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="9eb7c-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="9eb7c-274">System-Only</span></span>            | <span data-ttu-id="9eb7c-275">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-275">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-276">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9eb7c-276">Is-Single-Valued</span></span>       | <span data-ttu-id="9eb7c-277">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-277">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-278">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9eb7c-278">Is Indexed</span></span>             | <span data-ttu-id="9eb7c-279">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-279">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-280">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9eb7c-280">In Global Catalog</span></span>      | <span data-ttu-id="9eb7c-281">否</span><span class="sxs-lookup"><span data-stu-id="9eb7c-281">False</span></span>                                                                 |
| <span data-ttu-id="9eb7c-282">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9eb7c-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="9eb7c-283">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9eb7c-283">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="9eb7c-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9eb7c-284">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="9eb7c-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9eb7c-285">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="9eb7c-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-286">Search-Flags</span></span>           | <span data-ttu-id="9eb7c-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9eb7c-287">0x00000000</span></span>                                                            |
| <span data-ttu-id="9eb7c-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9eb7c-288">System-Flags</span></span>           | <span data-ttu-id="9eb7c-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9eb7c-289">0x00000010</span></span>                                                            |
| <span data-ttu-id="9eb7c-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9eb7c-290">Classes used in</span></span>        | [<span data-ttu-id="9eb7c-291">**授權-網站-設定**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-291">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



 

 





