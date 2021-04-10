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
# <a name="domain-component-attribute"></a><span data-ttu-id="eeb4b-106">Domain-Component 屬性</span><span class="sxs-lookup"><span data-stu-id="eeb4b-106">Domain-Component attribute</span></span>

<span data-ttu-id="eeb4b-107">網域和 DNS 物件的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="eeb4b-107">The naming attribute for Domain and DNS objects.</span></span> <span data-ttu-id="eeb4b-108">通常會顯示為 dc = DomainName。</span><span class="sxs-lookup"><span data-stu-id="eeb4b-108">Usually displayed as dc=DomainName.</span></span>



| <span data-ttu-id="eeb4b-109">進入</span><span class="sxs-lookup"><span data-stu-id="eeb4b-109">Entry</span></span> | <span data-ttu-id="eeb4b-110">值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="eeb4b-111">CN</span><span class="sxs-lookup"><span data-stu-id="eeb4b-111">CN</span></span>                | <span data-ttu-id="eeb4b-112">Domain-Component</span><span class="sxs-lookup"><span data-stu-id="eeb4b-112">Domain-Component</span></span>                            |
| <span data-ttu-id="eeb4b-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="eeb4b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="eeb4b-114">dc</span><span class="sxs-lookup"><span data-stu-id="eeb4b-114">dc</span></span>                                          |
| <span data-ttu-id="eeb4b-115">大小</span><span class="sxs-lookup"><span data-stu-id="eeb4b-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="eeb4b-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="eeb4b-116">Update Privilege</span></span>  | <span data-ttu-id="eeb4b-117">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="eeb4b-117">Domain administrator</span></span>                        |
| <span data-ttu-id="eeb4b-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="eeb4b-118">Update Frequency</span></span>  | <span data-ttu-id="eeb4b-119">建立網域時。</span><span class="sxs-lookup"><span data-stu-id="eeb4b-119">When the domain is created.</span></span>                 |
| <span data-ttu-id="eeb4b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="eeb4b-120">Attribute-Id</span></span>      | <span data-ttu-id="eeb4b-121">0.9.2342.19200300.100.1.25</span><span class="sxs-lookup"><span data-stu-id="eeb4b-121">0.9.2342.19200300.100.1.25</span></span>                  |
| <span data-ttu-id="eeb4b-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="eeb4b-122">System-Id-Guid</span></span>    | <span data-ttu-id="eeb4b-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="eeb4b-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span></span>        |
| <span data-ttu-id="eeb4b-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="eeb4b-124">Syntax</span></span>            | [<span data-ttu-id="eeb4b-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="eeb4b-126">實作</span><span class="sxs-lookup"><span data-stu-id="eeb4b-126">Implementations</span></span>

-   [<span data-ttu-id="eeb4b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="eeb4b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="eeb4b-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="eeb4b-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="eeb4b-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="eeb4b-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="eeb4b-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="eeb4b-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eeb4b-134">Windows 2000 Server</span></span>



| <span data-ttu-id="eeb4b-135">進入</span><span class="sxs-lookup"><span data-stu-id="eeb4b-135">Entry</span></span> | <span data-ttu-id="eeb4b-136">值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-136">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb4b-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="eeb4b-137">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="eeb4b-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eeb4b-138">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="eeb4b-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="eeb4b-139">System-Only</span></span>            | <span data-ttu-id="eeb4b-140">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-140">False</span></span>                                                                                                                   |
| <span data-ttu-id="eeb4b-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-141">Is-Single-Valued</span></span>       | <span data-ttu-id="eeb4b-142">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-142">True</span></span>                                                                                                                    |
| <span data-ttu-id="eeb4b-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="eeb4b-143">Is Indexed</span></span>             | <span data-ttu-id="eeb4b-144">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-144">False</span></span>                                                                                                                   |
| <span data-ttu-id="eeb4b-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="eeb4b-145">In Global Catalog</span></span>      | <span data-ttu-id="eeb4b-146">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-146">True</span></span>                                                                                                                    |
| <span data-ttu-id="eeb4b-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="eeb4b-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="eeb4b-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="eeb4b-148">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="eeb4b-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eeb4b-149">Range-Lower</span></span>            | <span data-ttu-id="eeb4b-150">1</span><span class="sxs-lookup"><span data-stu-id="eeb4b-150">1</span></span>                                                                                                                       |
| <span data-ttu-id="eeb4b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eeb4b-151">Range-Upper</span></span>            | <span data-ttu-id="eeb4b-152">255</span><span class="sxs-lookup"><span data-stu-id="eeb4b-152">255</span></span>                                                                                                                     |
| <span data-ttu-id="eeb4b-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-153">Search-Flags</span></span>           | <span data-ttu-id="eeb4b-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eeb4b-154">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="eeb4b-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-155">System-Flags</span></span>           | <span data-ttu-id="eeb4b-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eeb4b-156">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="eeb4b-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="eeb4b-157">Classes used in</span></span>        | [<span data-ttu-id="eeb4b-158">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="eeb4b-159">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-159">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="eeb4b-160">**域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-160">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="eeb4b-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eeb4b-161">Windows Server 2003</span></span>



| <span data-ttu-id="eeb4b-162">進入</span><span class="sxs-lookup"><span data-stu-id="eeb4b-162">Entry</span></span> | <span data-ttu-id="eeb4b-163">值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-163">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb4b-164">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="eeb4b-164">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="eeb4b-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eeb4b-165">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="eeb4b-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="eeb4b-166">System-Only</span></span>            | <span data-ttu-id="eeb4b-167">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-167">False</span></span>                                                                                                                   |
| <span data-ttu-id="eeb4b-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-168">Is-Single-Valued</span></span>       | <span data-ttu-id="eeb4b-169">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-169">True</span></span>                                                                                                                    |
| <span data-ttu-id="eeb4b-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="eeb4b-170">Is Indexed</span></span>             | <span data-ttu-id="eeb4b-171">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-171">False</span></span>                                                                                                                   |
| <span data-ttu-id="eeb4b-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="eeb4b-172">In Global Catalog</span></span>      | <span data-ttu-id="eeb4b-173">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-173">True</span></span>                                                                                                                    |
| <span data-ttu-id="eeb4b-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="eeb4b-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="eeb4b-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="eeb4b-175">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="eeb4b-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eeb4b-176">Range-Lower</span></span>            | <span data-ttu-id="eeb4b-177">1</span><span class="sxs-lookup"><span data-stu-id="eeb4b-177">1</span></span>                                                                                                                       |
| <span data-ttu-id="eeb4b-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eeb4b-178">Range-Upper</span></span>            | <span data-ttu-id="eeb4b-179">255</span><span class="sxs-lookup"><span data-stu-id="eeb4b-179">255</span></span>                                                                                                                     |
| <span data-ttu-id="eeb4b-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-180">Search-Flags</span></span>           | <span data-ttu-id="eeb4b-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eeb4b-181">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="eeb4b-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-182">System-Flags</span></span>           | <span data-ttu-id="eeb4b-183">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eeb4b-183">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="eeb4b-184">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="eeb4b-184">Classes used in</span></span>        | [<span data-ttu-id="eeb4b-185">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-185">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="eeb4b-186">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-186">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="eeb4b-187">**域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-187">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="adam"></a><span data-ttu-id="eeb4b-188">亞當</span><span class="sxs-lookup"><span data-stu-id="eeb4b-188">ADAM</span></span>



| <span data-ttu-id="eeb4b-189">進入</span><span class="sxs-lookup"><span data-stu-id="eeb4b-189">Entry</span></span> | <span data-ttu-id="eeb4b-190">值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-190">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="eeb4b-191">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="eeb4b-191">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="eeb4b-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eeb4b-192">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="eeb4b-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="eeb4b-193">System-Only</span></span>            | <span data-ttu-id="eeb4b-194">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-194">False</span></span>                                 |
| <span data-ttu-id="eeb4b-195">是-單一值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-195">Is-Single-Valued</span></span>       | <span data-ttu-id="eeb4b-196">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-196">True</span></span>                                  |
| <span data-ttu-id="eeb4b-197">已編制索引</span><span class="sxs-lookup"><span data-stu-id="eeb4b-197">Is Indexed</span></span>             | <span data-ttu-id="eeb4b-198">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-198">False</span></span>                                 |
| <span data-ttu-id="eeb4b-199">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="eeb4b-199">In Global Catalog</span></span>      | <span data-ttu-id="eeb4b-200">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-200">True</span></span>                                  |
| <span data-ttu-id="eeb4b-201">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="eeb4b-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="eeb4b-202">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="eeb4b-202">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="eeb4b-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eeb4b-203">Range-Lower</span></span>            | <span data-ttu-id="eeb4b-204">1</span><span class="sxs-lookup"><span data-stu-id="eeb4b-204">1</span></span>                                     |
| <span data-ttu-id="eeb4b-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eeb4b-205">Range-Upper</span></span>            | <span data-ttu-id="eeb4b-206">255</span><span class="sxs-lookup"><span data-stu-id="eeb4b-206">255</span></span>                                   |
| <span data-ttu-id="eeb4b-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-207">Search-Flags</span></span>           | <span data-ttu-id="eeb4b-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eeb4b-208">0x00000000</span></span>                            |
| <span data-ttu-id="eeb4b-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-209">System-Flags</span></span>           | <span data-ttu-id="eeb4b-210">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eeb4b-210">0x00000012</span></span>                            |
| <span data-ttu-id="eeb4b-211">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="eeb4b-211">Classes used in</span></span>        | [<span data-ttu-id="eeb4b-212">**域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-212">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="eeb4b-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="eeb4b-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="eeb4b-214">進入</span><span class="sxs-lookup"><span data-stu-id="eeb4b-214">Entry</span></span> | <span data-ttu-id="eeb4b-215">值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-215">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb4b-216">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="eeb4b-216">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="eeb4b-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eeb4b-217">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="eeb4b-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="eeb4b-218">System-Only</span></span>            | <span data-ttu-id="eeb4b-219">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-219">False</span></span>                                                                                                                   |
| <span data-ttu-id="eeb4b-220">是-單一值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-220">Is-Single-Valued</span></span>       | <span data-ttu-id="eeb4b-221">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-221">True</span></span>                                                                                                                    |
| <span data-ttu-id="eeb4b-222">已編制索引</span><span class="sxs-lookup"><span data-stu-id="eeb4b-222">Is Indexed</span></span>             | <span data-ttu-id="eeb4b-223">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-223">False</span></span>                                                                                                                   |
| <span data-ttu-id="eeb4b-224">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="eeb4b-224">In Global Catalog</span></span>      | <span data-ttu-id="eeb4b-225">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-225">True</span></span>                                                                                                                    |
| <span data-ttu-id="eeb4b-226">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="eeb4b-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="eeb4b-227">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="eeb4b-227">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="eeb4b-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eeb4b-228">Range-Lower</span></span>            | <span data-ttu-id="eeb4b-229">1</span><span class="sxs-lookup"><span data-stu-id="eeb4b-229">1</span></span>                                                                                                                       |
| <span data-ttu-id="eeb4b-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eeb4b-230">Range-Upper</span></span>            | <span data-ttu-id="eeb4b-231">255</span><span class="sxs-lookup"><span data-stu-id="eeb4b-231">255</span></span>                                                                                                                     |
| <span data-ttu-id="eeb4b-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-232">Search-Flags</span></span>           | <span data-ttu-id="eeb4b-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eeb4b-233">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="eeb4b-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-234">System-Flags</span></span>           | <span data-ttu-id="eeb4b-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eeb4b-235">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="eeb4b-236">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="eeb4b-236">Classes used in</span></span>        | [<span data-ttu-id="eeb4b-237">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-237">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="eeb4b-238">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-238">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="eeb4b-239">**域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-239">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="eeb4b-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eeb4b-240">Windows Server 2008</span></span>



| <span data-ttu-id="eeb4b-241">進入</span><span class="sxs-lookup"><span data-stu-id="eeb4b-241">Entry</span></span> | <span data-ttu-id="eeb4b-242">值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-242">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb4b-243">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="eeb4b-243">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="eeb4b-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eeb4b-244">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="eeb4b-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="eeb4b-245">System-Only</span></span>            | <span data-ttu-id="eeb4b-246">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-246">False</span></span>                                                                                                                   |
| <span data-ttu-id="eeb4b-247">是-單一值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-247">Is-Single-Valued</span></span>       | <span data-ttu-id="eeb4b-248">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-248">True</span></span>                                                                                                                    |
| <span data-ttu-id="eeb4b-249">已編制索引</span><span class="sxs-lookup"><span data-stu-id="eeb4b-249">Is Indexed</span></span>             | <span data-ttu-id="eeb4b-250">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-250">False</span></span>                                                                                                                   |
| <span data-ttu-id="eeb4b-251">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="eeb4b-251">In Global Catalog</span></span>      | <span data-ttu-id="eeb4b-252">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-252">True</span></span>                                                                                                                    |
| <span data-ttu-id="eeb4b-253">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="eeb4b-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="eeb4b-254">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="eeb4b-254">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="eeb4b-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eeb4b-255">Range-Lower</span></span>            | <span data-ttu-id="eeb4b-256">1</span><span class="sxs-lookup"><span data-stu-id="eeb4b-256">1</span></span>                                                                                                                       |
| <span data-ttu-id="eeb4b-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eeb4b-257">Range-Upper</span></span>            | <span data-ttu-id="eeb4b-258">255</span><span class="sxs-lookup"><span data-stu-id="eeb4b-258">255</span></span>                                                                                                                     |
| <span data-ttu-id="eeb4b-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-259">Search-Flags</span></span>           | <span data-ttu-id="eeb4b-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eeb4b-260">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="eeb4b-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-261">System-Flags</span></span>           | <span data-ttu-id="eeb4b-262">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eeb4b-262">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="eeb4b-263">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="eeb4b-263">Classes used in</span></span>        | [<span data-ttu-id="eeb4b-264">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-264">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="eeb4b-265">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-265">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="eeb4b-266">**域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-266">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="eeb4b-267">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eeb4b-267">Windows Server 2008 R2</span></span>



| <span data-ttu-id="eeb4b-268">進入</span><span class="sxs-lookup"><span data-stu-id="eeb4b-268">Entry</span></span> | <span data-ttu-id="eeb4b-269">值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-269">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb4b-270">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="eeb4b-270">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="eeb4b-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eeb4b-271">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="eeb4b-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="eeb4b-272">System-Only</span></span>            | <span data-ttu-id="eeb4b-273">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-273">False</span></span>                                                                                                                   |
| <span data-ttu-id="eeb4b-274">是-單一值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-274">Is-Single-Valued</span></span>       | <span data-ttu-id="eeb4b-275">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-275">True</span></span>                                                                                                                    |
| <span data-ttu-id="eeb4b-276">已編制索引</span><span class="sxs-lookup"><span data-stu-id="eeb4b-276">Is Indexed</span></span>             | <span data-ttu-id="eeb4b-277">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-277">False</span></span>                                                                                                                   |
| <span data-ttu-id="eeb4b-278">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="eeb4b-278">In Global Catalog</span></span>      | <span data-ttu-id="eeb4b-279">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-279">True</span></span>                                                                                                                    |
| <span data-ttu-id="eeb4b-280">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="eeb4b-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="eeb4b-281">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="eeb4b-281">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="eeb4b-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eeb4b-282">Range-Lower</span></span>            | <span data-ttu-id="eeb4b-283">1</span><span class="sxs-lookup"><span data-stu-id="eeb4b-283">1</span></span>                                                                                                                       |
| <span data-ttu-id="eeb4b-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eeb4b-284">Range-Upper</span></span>            | <span data-ttu-id="eeb4b-285">255</span><span class="sxs-lookup"><span data-stu-id="eeb4b-285">255</span></span>                                                                                                                     |
| <span data-ttu-id="eeb4b-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-286">Search-Flags</span></span>           | <span data-ttu-id="eeb4b-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eeb4b-287">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="eeb4b-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-288">System-Flags</span></span>           | <span data-ttu-id="eeb4b-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eeb4b-289">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="eeb4b-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="eeb4b-290">Classes used in</span></span>        | [<span data-ttu-id="eeb4b-291">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-291">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="eeb4b-292">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-292">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="eeb4b-293">**域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-293">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="eeb4b-294">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eeb4b-294">Windows Server 2012</span></span>



| <span data-ttu-id="eeb4b-295">進入</span><span class="sxs-lookup"><span data-stu-id="eeb4b-295">Entry</span></span> | <span data-ttu-id="eeb4b-296">值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-296">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb4b-297">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="eeb4b-297">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="eeb4b-298">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eeb4b-298">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="eeb4b-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="eeb4b-299">System-Only</span></span>            | <span data-ttu-id="eeb4b-300">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-300">False</span></span>                                                                                                                   |
| <span data-ttu-id="eeb4b-301">是-單一值</span><span class="sxs-lookup"><span data-stu-id="eeb4b-301">Is-Single-Valued</span></span>       | <span data-ttu-id="eeb4b-302">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-302">True</span></span>                                                                                                                    |
| <span data-ttu-id="eeb4b-303">已編制索引</span><span class="sxs-lookup"><span data-stu-id="eeb4b-303">Is Indexed</span></span>             | <span data-ttu-id="eeb4b-304">否</span><span class="sxs-lookup"><span data-stu-id="eeb4b-304">False</span></span>                                                                                                                   |
| <span data-ttu-id="eeb4b-305">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="eeb4b-305">In Global Catalog</span></span>      | <span data-ttu-id="eeb4b-306">對</span><span class="sxs-lookup"><span data-stu-id="eeb4b-306">True</span></span>                                                                                                                    |
| <span data-ttu-id="eeb4b-307">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="eeb4b-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="eeb4b-308">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="eeb4b-308">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="eeb4b-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eeb4b-309">Range-Lower</span></span>            | <span data-ttu-id="eeb4b-310">1</span><span class="sxs-lookup"><span data-stu-id="eeb4b-310">1</span></span>                                                                                                                       |
| <span data-ttu-id="eeb4b-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eeb4b-311">Range-Upper</span></span>            | <span data-ttu-id="eeb4b-312">255</span><span class="sxs-lookup"><span data-stu-id="eeb4b-312">255</span></span>                                                                                                                     |
| <span data-ttu-id="eeb4b-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-313">Search-Flags</span></span>           | <span data-ttu-id="eeb4b-314">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eeb4b-314">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="eeb4b-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eeb4b-315">System-Flags</span></span>           | <span data-ttu-id="eeb4b-316">0x00000012</span><span class="sxs-lookup"><span data-stu-id="eeb4b-316">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="eeb4b-317">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="eeb4b-317">Classes used in</span></span>        | [<span data-ttu-id="eeb4b-318">**Dns-Node**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-318">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="eeb4b-319">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-319">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="eeb4b-320">**域**</span><span class="sxs-lookup"><span data-stu-id="eeb4b-320">**Domain**</span></span>](c-domain.md)<br/> |



 

 





