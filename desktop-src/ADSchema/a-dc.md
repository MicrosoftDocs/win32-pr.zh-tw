---
title: Domain-Component 屬性
description: 網域和 DNS 物件的命名屬性。 通常會顯示為 dc DomainName。
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Domain-Component 屬性 AD 架構
- dc 屬性 AD 架構
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97a6958d51c6e0e29f70685b2624fb194d42e05
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107148"
---
# <a name="domain-component-attribute"></a><span data-ttu-id="dd0c7-106">Domain-Component 屬性</span><span class="sxs-lookup"><span data-stu-id="dd0c7-106">Domain-Component attribute</span></span>

<span data-ttu-id="dd0c7-107">網域和 DNS 物件的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="dd0c7-107">The naming attribute for Domain and DNS objects.</span></span> <span data-ttu-id="dd0c7-108">通常會顯示為 dc = DomainName。</span><span class="sxs-lookup"><span data-stu-id="dd0c7-108">Usually displayed as dc=DomainName.</span></span>



| <span data-ttu-id="dd0c7-109">進入</span><span class="sxs-lookup"><span data-stu-id="dd0c7-109">Entry</span></span> | <span data-ttu-id="dd0c7-110">值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="dd0c7-111">CN</span><span class="sxs-lookup"><span data-stu-id="dd0c7-111">CN</span></span>                | <span data-ttu-id="dd0c7-112">Domain-Component</span><span class="sxs-lookup"><span data-stu-id="dd0c7-112">Domain-Component</span></span>                            |
| <span data-ttu-id="dd0c7-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="dd0c7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dd0c7-114">dc</span><span class="sxs-lookup"><span data-stu-id="dd0c7-114">dc</span></span>                                          |
| <span data-ttu-id="dd0c7-115">大小</span><span class="sxs-lookup"><span data-stu-id="dd0c7-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="dd0c7-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="dd0c7-116">Update Privilege</span></span>  | <span data-ttu-id="dd0c7-117">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="dd0c7-117">Domain administrator</span></span>                        |
| <span data-ttu-id="dd0c7-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="dd0c7-118">Update Frequency</span></span>  | <span data-ttu-id="dd0c7-119">建立網域時。</span><span class="sxs-lookup"><span data-stu-id="dd0c7-119">When the domain is created.</span></span>                 |
| <span data-ttu-id="dd0c7-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dd0c7-120">Attribute-Id</span></span>      | <span data-ttu-id="dd0c7-121">0.9.2342.19200300.100.1.25</span><span class="sxs-lookup"><span data-stu-id="dd0c7-121">0.9.2342.19200300.100.1.25</span></span>                  |
| <span data-ttu-id="dd0c7-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="dd0c7-122">System-Id-Guid</span></span>    | <span data-ttu-id="dd0c7-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="dd0c7-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span></span>        |
| <span data-ttu-id="dd0c7-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd0c7-124">Syntax</span></span>            | [<span data-ttu-id="dd0c7-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="dd0c7-126">實作</span><span class="sxs-lookup"><span data-stu-id="dd0c7-126">Implementations</span></span>

-   [<span data-ttu-id="dd0c7-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dd0c7-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dd0c7-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="dd0c7-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dd0c7-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dd0c7-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dd0c7-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dd0c7-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dd0c7-134">Windows 2000 Server</span></span>



| <span data-ttu-id="dd0c7-135">進入</span><span class="sxs-lookup"><span data-stu-id="dd0c7-135">Entry</span></span> | <span data-ttu-id="dd0c7-136">值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-136">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0c7-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd0c7-137">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="dd0c7-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd0c7-138">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="dd0c7-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd0c7-139">System-Only</span></span>            | <span data-ttu-id="dd0c7-140">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-140">False</span></span>                                                                                                                   |
| <span data-ttu-id="dd0c7-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-141">Is-Single-Valued</span></span>       | <span data-ttu-id="dd0c7-142">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-142">True</span></span>                                                                                                                    |
| <span data-ttu-id="dd0c7-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd0c7-143">Is Indexed</span></span>             | <span data-ttu-id="dd0c7-144">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-144">False</span></span>                                                                                                                   |
| <span data-ttu-id="dd0c7-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd0c7-145">In Global Catalog</span></span>      | <span data-ttu-id="dd0c7-146">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-146">True</span></span>                                                                                                                    |
| <span data-ttu-id="dd0c7-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd0c7-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd0c7-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd0c7-148">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="dd0c7-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd0c7-149">Range-Lower</span></span>            | <span data-ttu-id="dd0c7-150">1</span><span class="sxs-lookup"><span data-stu-id="dd0c7-150">1</span></span>                                                                                                                       |
| <span data-ttu-id="dd0c7-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd0c7-151">Range-Upper</span></span>            | <span data-ttu-id="dd0c7-152">255</span><span class="sxs-lookup"><span data-stu-id="dd0c7-152">255</span></span>                                                                                                                     |
| <span data-ttu-id="dd0c7-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-153">Search-Flags</span></span>           | <span data-ttu-id="dd0c7-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd0c7-154">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="dd0c7-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-155">System-Flags</span></span>           | <span data-ttu-id="dd0c7-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="dd0c7-156">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="dd0c7-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd0c7-157">Classes used in</span></span>        | [<span data-ttu-id="dd0c7-158">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="dd0c7-159">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-159">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="dd0c7-160">**域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-160">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dd0c7-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd0c7-161">Windows Server 2003</span></span>



| <span data-ttu-id="dd0c7-162">進入</span><span class="sxs-lookup"><span data-stu-id="dd0c7-162">Entry</span></span> | <span data-ttu-id="dd0c7-163">值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-163">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0c7-164">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd0c7-164">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="dd0c7-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd0c7-165">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="dd0c7-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd0c7-166">System-Only</span></span>            | <span data-ttu-id="dd0c7-167">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-167">False</span></span>                                                                                                                   |
| <span data-ttu-id="dd0c7-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-168">Is-Single-Valued</span></span>       | <span data-ttu-id="dd0c7-169">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-169">True</span></span>                                                                                                                    |
| <span data-ttu-id="dd0c7-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd0c7-170">Is Indexed</span></span>             | <span data-ttu-id="dd0c7-171">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-171">False</span></span>                                                                                                                   |
| <span data-ttu-id="dd0c7-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd0c7-172">In Global Catalog</span></span>      | <span data-ttu-id="dd0c7-173">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-173">True</span></span>                                                                                                                    |
| <span data-ttu-id="dd0c7-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd0c7-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd0c7-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd0c7-175">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="dd0c7-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd0c7-176">Range-Lower</span></span>            | <span data-ttu-id="dd0c7-177">1</span><span class="sxs-lookup"><span data-stu-id="dd0c7-177">1</span></span>                                                                                                                       |
| <span data-ttu-id="dd0c7-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd0c7-178">Range-Upper</span></span>            | <span data-ttu-id="dd0c7-179">255</span><span class="sxs-lookup"><span data-stu-id="dd0c7-179">255</span></span>                                                                                                                     |
| <span data-ttu-id="dd0c7-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-180">Search-Flags</span></span>           | <span data-ttu-id="dd0c7-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd0c7-181">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="dd0c7-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-182">System-Flags</span></span>           | <span data-ttu-id="dd0c7-183">0x00000012</span><span class="sxs-lookup"><span data-stu-id="dd0c7-183">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="dd0c7-184">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd0c7-184">Classes used in</span></span>        | [<span data-ttu-id="dd0c7-185">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-185">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="dd0c7-186">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-186">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="dd0c7-187">**域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-187">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="adam"></a><span data-ttu-id="dd0c7-188">亞當</span><span class="sxs-lookup"><span data-stu-id="dd0c7-188">ADAM</span></span>



| <span data-ttu-id="dd0c7-189">進入</span><span class="sxs-lookup"><span data-stu-id="dd0c7-189">Entry</span></span> | <span data-ttu-id="dd0c7-190">值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-190">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="dd0c7-191">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd0c7-191">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="dd0c7-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd0c7-192">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="dd0c7-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd0c7-193">System-Only</span></span>            | <span data-ttu-id="dd0c7-194">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-194">False</span></span>                                 |
| <span data-ttu-id="dd0c7-195">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-195">Is-Single-Valued</span></span>       | <span data-ttu-id="dd0c7-196">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-196">True</span></span>                                  |
| <span data-ttu-id="dd0c7-197">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd0c7-197">Is Indexed</span></span>             | <span data-ttu-id="dd0c7-198">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-198">False</span></span>                                 |
| <span data-ttu-id="dd0c7-199">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd0c7-199">In Global Catalog</span></span>      | <span data-ttu-id="dd0c7-200">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-200">True</span></span>                                  |
| <span data-ttu-id="dd0c7-201">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd0c7-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd0c7-202">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd0c7-202">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="dd0c7-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd0c7-203">Range-Lower</span></span>            | <span data-ttu-id="dd0c7-204">1</span><span class="sxs-lookup"><span data-stu-id="dd0c7-204">1</span></span>                                     |
| <span data-ttu-id="dd0c7-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd0c7-205">Range-Upper</span></span>            | <span data-ttu-id="dd0c7-206">255</span><span class="sxs-lookup"><span data-stu-id="dd0c7-206">255</span></span>                                   |
| <span data-ttu-id="dd0c7-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-207">Search-Flags</span></span>           | <span data-ttu-id="dd0c7-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd0c7-208">0x00000000</span></span>                            |
| <span data-ttu-id="dd0c7-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-209">System-Flags</span></span>           | <span data-ttu-id="dd0c7-210">0x00000012</span><span class="sxs-lookup"><span data-stu-id="dd0c7-210">0x00000012</span></span>                            |
| <span data-ttu-id="dd0c7-211">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd0c7-211">Classes used in</span></span>        | [<span data-ttu-id="dd0c7-212">**域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-212">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dd0c7-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dd0c7-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dd0c7-214">進入</span><span class="sxs-lookup"><span data-stu-id="dd0c7-214">Entry</span></span> | <span data-ttu-id="dd0c7-215">值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-215">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0c7-216">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd0c7-216">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="dd0c7-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd0c7-217">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="dd0c7-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd0c7-218">System-Only</span></span>            | <span data-ttu-id="dd0c7-219">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-219">False</span></span>                                                                                                                   |
| <span data-ttu-id="dd0c7-220">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-220">Is-Single-Valued</span></span>       | <span data-ttu-id="dd0c7-221">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-221">True</span></span>                                                                                                                    |
| <span data-ttu-id="dd0c7-222">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd0c7-222">Is Indexed</span></span>             | <span data-ttu-id="dd0c7-223">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-223">False</span></span>                                                                                                                   |
| <span data-ttu-id="dd0c7-224">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd0c7-224">In Global Catalog</span></span>      | <span data-ttu-id="dd0c7-225">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-225">True</span></span>                                                                                                                    |
| <span data-ttu-id="dd0c7-226">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd0c7-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd0c7-227">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd0c7-227">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="dd0c7-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd0c7-228">Range-Lower</span></span>            | <span data-ttu-id="dd0c7-229">1</span><span class="sxs-lookup"><span data-stu-id="dd0c7-229">1</span></span>                                                                                                                       |
| <span data-ttu-id="dd0c7-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd0c7-230">Range-Upper</span></span>            | <span data-ttu-id="dd0c7-231">255</span><span class="sxs-lookup"><span data-stu-id="dd0c7-231">255</span></span>                                                                                                                     |
| <span data-ttu-id="dd0c7-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-232">Search-Flags</span></span>           | <span data-ttu-id="dd0c7-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd0c7-233">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="dd0c7-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-234">System-Flags</span></span>           | <span data-ttu-id="dd0c7-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="dd0c7-235">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="dd0c7-236">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd0c7-236">Classes used in</span></span>        | [<span data-ttu-id="dd0c7-237">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-237">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="dd0c7-238">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-238">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="dd0c7-239">**域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-239">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dd0c7-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd0c7-240">Windows Server 2008</span></span>



| <span data-ttu-id="dd0c7-241">進入</span><span class="sxs-lookup"><span data-stu-id="dd0c7-241">Entry</span></span> | <span data-ttu-id="dd0c7-242">值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-242">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0c7-243">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd0c7-243">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="dd0c7-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd0c7-244">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="dd0c7-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd0c7-245">System-Only</span></span>            | <span data-ttu-id="dd0c7-246">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-246">False</span></span>                                                                                                                   |
| <span data-ttu-id="dd0c7-247">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-247">Is-Single-Valued</span></span>       | <span data-ttu-id="dd0c7-248">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-248">True</span></span>                                                                                                                    |
| <span data-ttu-id="dd0c7-249">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd0c7-249">Is Indexed</span></span>             | <span data-ttu-id="dd0c7-250">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-250">False</span></span>                                                                                                                   |
| <span data-ttu-id="dd0c7-251">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd0c7-251">In Global Catalog</span></span>      | <span data-ttu-id="dd0c7-252">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-252">True</span></span>                                                                                                                    |
| <span data-ttu-id="dd0c7-253">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd0c7-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd0c7-254">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd0c7-254">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="dd0c7-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd0c7-255">Range-Lower</span></span>            | <span data-ttu-id="dd0c7-256">1</span><span class="sxs-lookup"><span data-stu-id="dd0c7-256">1</span></span>                                                                                                                       |
| <span data-ttu-id="dd0c7-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd0c7-257">Range-Upper</span></span>            | <span data-ttu-id="dd0c7-258">255</span><span class="sxs-lookup"><span data-stu-id="dd0c7-258">255</span></span>                                                                                                                     |
| <span data-ttu-id="dd0c7-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-259">Search-Flags</span></span>           | <span data-ttu-id="dd0c7-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd0c7-260">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="dd0c7-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-261">System-Flags</span></span>           | <span data-ttu-id="dd0c7-262">0x00000012</span><span class="sxs-lookup"><span data-stu-id="dd0c7-262">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="dd0c7-263">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd0c7-263">Classes used in</span></span>        | [<span data-ttu-id="dd0c7-264">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-264">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="dd0c7-265">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-265">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="dd0c7-266">**域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-266">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dd0c7-267">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dd0c7-267">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dd0c7-268">進入</span><span class="sxs-lookup"><span data-stu-id="dd0c7-268">Entry</span></span> | <span data-ttu-id="dd0c7-269">值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-269">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0c7-270">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd0c7-270">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="dd0c7-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd0c7-271">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="dd0c7-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd0c7-272">System-Only</span></span>            | <span data-ttu-id="dd0c7-273">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-273">False</span></span>                                                                                                                   |
| <span data-ttu-id="dd0c7-274">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-274">Is-Single-Valued</span></span>       | <span data-ttu-id="dd0c7-275">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-275">True</span></span>                                                                                                                    |
| <span data-ttu-id="dd0c7-276">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd0c7-276">Is Indexed</span></span>             | <span data-ttu-id="dd0c7-277">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-277">False</span></span>                                                                                                                   |
| <span data-ttu-id="dd0c7-278">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd0c7-278">In Global Catalog</span></span>      | <span data-ttu-id="dd0c7-279">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-279">True</span></span>                                                                                                                    |
| <span data-ttu-id="dd0c7-280">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd0c7-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd0c7-281">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd0c7-281">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="dd0c7-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd0c7-282">Range-Lower</span></span>            | <span data-ttu-id="dd0c7-283">1</span><span class="sxs-lookup"><span data-stu-id="dd0c7-283">1</span></span>                                                                                                                       |
| <span data-ttu-id="dd0c7-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd0c7-284">Range-Upper</span></span>            | <span data-ttu-id="dd0c7-285">255</span><span class="sxs-lookup"><span data-stu-id="dd0c7-285">255</span></span>                                                                                                                     |
| <span data-ttu-id="dd0c7-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-286">Search-Flags</span></span>           | <span data-ttu-id="dd0c7-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd0c7-287">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="dd0c7-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-288">System-Flags</span></span>           | <span data-ttu-id="dd0c7-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="dd0c7-289">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="dd0c7-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd0c7-290">Classes used in</span></span>        | [<span data-ttu-id="dd0c7-291">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-291">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="dd0c7-292">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-292">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="dd0c7-293">**域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-293">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dd0c7-294">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dd0c7-294">Windows Server 2012</span></span>



| <span data-ttu-id="dd0c7-295">進入</span><span class="sxs-lookup"><span data-stu-id="dd0c7-295">Entry</span></span> | <span data-ttu-id="dd0c7-296">值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-296">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0c7-297">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dd0c7-297">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="dd0c7-298">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dd0c7-298">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="dd0c7-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="dd0c7-299">System-Only</span></span>            | <span data-ttu-id="dd0c7-300">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-300">False</span></span>                                                                                                                   |
| <span data-ttu-id="dd0c7-301">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dd0c7-301">Is-Single-Valued</span></span>       | <span data-ttu-id="dd0c7-302">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-302">True</span></span>                                                                                                                    |
| <span data-ttu-id="dd0c7-303">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dd0c7-303">Is Indexed</span></span>             | <span data-ttu-id="dd0c7-304">否</span><span class="sxs-lookup"><span data-stu-id="dd0c7-304">False</span></span>                                                                                                                   |
| <span data-ttu-id="dd0c7-305">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dd0c7-305">In Global Catalog</span></span>      | <span data-ttu-id="dd0c7-306">對</span><span class="sxs-lookup"><span data-stu-id="dd0c7-306">True</span></span>                                                                                                                    |
| <span data-ttu-id="dd0c7-307">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dd0c7-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="dd0c7-308">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dd0c7-308">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="dd0c7-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dd0c7-309">Range-Lower</span></span>            | <span data-ttu-id="dd0c7-310">1</span><span class="sxs-lookup"><span data-stu-id="dd0c7-310">1</span></span>                                                                                                                       |
| <span data-ttu-id="dd0c7-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dd0c7-311">Range-Upper</span></span>            | <span data-ttu-id="dd0c7-312">255</span><span class="sxs-lookup"><span data-stu-id="dd0c7-312">255</span></span>                                                                                                                     |
| <span data-ttu-id="dd0c7-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-313">Search-Flags</span></span>           | <span data-ttu-id="dd0c7-314">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd0c7-314">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="dd0c7-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dd0c7-315">System-Flags</span></span>           | <span data-ttu-id="dd0c7-316">0x00000012</span><span class="sxs-lookup"><span data-stu-id="dd0c7-316">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="dd0c7-317">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dd0c7-317">Classes used in</span></span>        | [<span data-ttu-id="dd0c7-318">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-318">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="dd0c7-319">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-319">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="dd0c7-320">**域**</span><span class="sxs-lookup"><span data-stu-id="dd0c7-320">**Domain**</span></span>](c-domain.md)<br/> |



 

 





