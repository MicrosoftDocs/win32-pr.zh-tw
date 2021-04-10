---
title: Title 屬性
description: 包含使用者職稱。 這個屬性通常用來指出正式的職稱，例如資深程式設計師，而非 occupational 類別，例如程式設計師。 它通常不會用於尾碼標題（例如 Esq）。 或 DDS。
ms.assetid: 4a6899a7-ddbf-4dd0-b088-3739716f33df
ms.tgt_platform: multiple
keywords:
- Title 屬性 AD 架構
- title 屬性 AD 架構
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbb4dae862db9fc363b22647bd5e56a98e9e60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845280"
---
# <a name="title-attribute-ad-schema"></a><span data-ttu-id="186eb-108">標題屬性 (AD 架構) </span><span class="sxs-lookup"><span data-stu-id="186eb-108">Title attribute (AD Schema)</span></span>

<span data-ttu-id="186eb-109">包含使用者職稱。</span><span class="sxs-lookup"><span data-stu-id="186eb-109">Contains the user's job title.</span></span> <span data-ttu-id="186eb-110">這個屬性通常用來指出正式的職稱，例如資深程式設計師，而非 occupational 類別，例如程式設計師。</span><span class="sxs-lookup"><span data-stu-id="186eb-110">This property is commonly used to indicate the formal job title, such as Senior Programmer, rather than occupational class, such as programmer.</span></span> <span data-ttu-id="186eb-111">它通常不會用於尾碼標題（例如 Esq）。</span><span class="sxs-lookup"><span data-stu-id="186eb-111">It is not typically used for suffix titles such as Esq.</span></span> <span data-ttu-id="186eb-112">或 DDS。</span><span class="sxs-lookup"><span data-stu-id="186eb-112">or DDS.</span></span>



| <span data-ttu-id="186eb-113">進入</span><span class="sxs-lookup"><span data-stu-id="186eb-113">Entry</span></span> | <span data-ttu-id="186eb-114">值</span><span class="sxs-lookup"><span data-stu-id="186eb-114">Value</span></span> |
|-------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="186eb-115">CN</span><span class="sxs-lookup"><span data-stu-id="186eb-115">CN</span></span>                | <span data-ttu-id="186eb-116">標題</span><span class="sxs-lookup"><span data-stu-id="186eb-116">Title</span></span>                                                                     |
| <span data-ttu-id="186eb-117">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="186eb-117">Ldap-Display-Name</span></span> | <span data-ttu-id="186eb-118">title</span><span class="sxs-lookup"><span data-stu-id="186eb-118">title</span></span>                                                                     |
| <span data-ttu-id="186eb-119">大小</span><span class="sxs-lookup"><span data-stu-id="186eb-119">Size</span></span>              | \-                                                                        |
| <span data-ttu-id="186eb-120">更新許可權</span><span class="sxs-lookup"><span data-stu-id="186eb-120">Update Privilege</span></span>  | <span data-ttu-id="186eb-121">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="186eb-121">Domain administrator or account owner.</span></span>                                    |
| <span data-ttu-id="186eb-122">更新頻率</span><span class="sxs-lookup"><span data-stu-id="186eb-122">Update Frequency</span></span>  | <span data-ttu-id="186eb-123">當使用者的記錄建立時，以及每次需要變更標題時。</span><span class="sxs-lookup"><span data-stu-id="186eb-123">When the user's record is created and whenever the title needs to change.</span></span> |
| <span data-ttu-id="186eb-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="186eb-124">Attribute-Id</span></span>      | <span data-ttu-id="186eb-125">2.5.4.12</span><span class="sxs-lookup"><span data-stu-id="186eb-125">2.5.4.12</span></span>                                                                  |
| <span data-ttu-id="186eb-126">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="186eb-126">System-Id-Guid</span></span>    | <span data-ttu-id="186eb-127">bf967a55-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="186eb-127">bf967a55-0de6-11d0-a285-00aa003049e2</span></span>                                      |
| <span data-ttu-id="186eb-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="186eb-128">Syntax</span></span>            | [<span data-ttu-id="186eb-129">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="186eb-129">**String(Unicode)**</span></span>](s-string-unicode.md)                               |



## <a name="implementations"></a><span data-ttu-id="186eb-130">實作</span><span class="sxs-lookup"><span data-stu-id="186eb-130">Implementations</span></span>

-   [<span data-ttu-id="186eb-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="186eb-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="186eb-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="186eb-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="186eb-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="186eb-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="186eb-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="186eb-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="186eb-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="186eb-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="186eb-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="186eb-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="186eb-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="186eb-137">Windows 2000 Server</span></span>



| <span data-ttu-id="186eb-138">進入</span><span class="sxs-lookup"><span data-stu-id="186eb-138">Entry</span></span> | <span data-ttu-id="186eb-139">值</span><span class="sxs-lookup"><span data-stu-id="186eb-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186eb-140">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="186eb-140">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="186eb-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="186eb-141">MAPI-Id</span></span>                | <span data-ttu-id="186eb-142">0x3A17</span><span class="sxs-lookup"><span data-stu-id="186eb-142">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="186eb-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="186eb-143">System-Only</span></span>            | <span data-ttu-id="186eb-144">否</span><span class="sxs-lookup"><span data-stu-id="186eb-144">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-145">是-單一值</span><span class="sxs-lookup"><span data-stu-id="186eb-145">Is-Single-Valued</span></span>       | <span data-ttu-id="186eb-146">對</span><span class="sxs-lookup"><span data-stu-id="186eb-146">True</span></span>                                                                                                                            |
| <span data-ttu-id="186eb-147">已編制索引</span><span class="sxs-lookup"><span data-stu-id="186eb-147">Is Indexed</span></span>             | <span data-ttu-id="186eb-148">否</span><span class="sxs-lookup"><span data-stu-id="186eb-148">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-149">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="186eb-149">In Global Catalog</span></span>      | <span data-ttu-id="186eb-150">否</span><span class="sxs-lookup"><span data-stu-id="186eb-150">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-151">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="186eb-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="186eb-152">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="186eb-152">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="186eb-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="186eb-153">Range-Lower</span></span>            | <span data-ttu-id="186eb-154">1</span><span class="sxs-lookup"><span data-stu-id="186eb-154">1</span></span>                                                                                                                               |
| <span data-ttu-id="186eb-155">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="186eb-155">Range-Upper</span></span>            | <span data-ttu-id="186eb-156">64</span><span class="sxs-lookup"><span data-stu-id="186eb-156">64</span></span>                                                                                                                              |
| <span data-ttu-id="186eb-157">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="186eb-157">Search-Flags</span></span>           | <span data-ttu-id="186eb-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="186eb-158">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="186eb-159">System-Flags</span><span class="sxs-lookup"><span data-stu-id="186eb-159">System-Flags</span></span>           | <span data-ttu-id="186eb-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="186eb-160">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="186eb-161">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="186eb-161">Classes used in</span></span>        | [<span data-ttu-id="186eb-162">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="186eb-162">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="186eb-163">**居住人**</span><span class="sxs-lookup"><span data-stu-id="186eb-163">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="186eb-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="186eb-164">Windows Server 2003</span></span>



| <span data-ttu-id="186eb-165">進入</span><span class="sxs-lookup"><span data-stu-id="186eb-165">Entry</span></span> | <span data-ttu-id="186eb-166">值</span><span class="sxs-lookup"><span data-stu-id="186eb-166">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186eb-167">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="186eb-167">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="186eb-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="186eb-168">MAPI-Id</span></span>                | <span data-ttu-id="186eb-169">0x3A17</span><span class="sxs-lookup"><span data-stu-id="186eb-169">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="186eb-170">System-Only</span><span class="sxs-lookup"><span data-stu-id="186eb-170">System-Only</span></span>            | <span data-ttu-id="186eb-171">否</span><span class="sxs-lookup"><span data-stu-id="186eb-171">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-172">是-單一值</span><span class="sxs-lookup"><span data-stu-id="186eb-172">Is-Single-Valued</span></span>       | <span data-ttu-id="186eb-173">對</span><span class="sxs-lookup"><span data-stu-id="186eb-173">True</span></span>                                                                                                                            |
| <span data-ttu-id="186eb-174">已編制索引</span><span class="sxs-lookup"><span data-stu-id="186eb-174">Is Indexed</span></span>             | <span data-ttu-id="186eb-175">否</span><span class="sxs-lookup"><span data-stu-id="186eb-175">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-176">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="186eb-176">In Global Catalog</span></span>      | <span data-ttu-id="186eb-177">否</span><span class="sxs-lookup"><span data-stu-id="186eb-177">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-178">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="186eb-178">NT-Security-Descriptor</span></span> | <span data-ttu-id="186eb-179">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="186eb-179">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="186eb-180">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="186eb-180">Range-Lower</span></span>            | <span data-ttu-id="186eb-181">1</span><span class="sxs-lookup"><span data-stu-id="186eb-181">1</span></span>                                                                                                                               |
| <span data-ttu-id="186eb-182">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="186eb-182">Range-Upper</span></span>            | <span data-ttu-id="186eb-183">64</span><span class="sxs-lookup"><span data-stu-id="186eb-183">64</span></span>                                                                                                                              |
| <span data-ttu-id="186eb-184">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="186eb-184">Search-Flags</span></span>           | <span data-ttu-id="186eb-185">0x00000000</span><span class="sxs-lookup"><span data-stu-id="186eb-185">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="186eb-186">System-Flags</span><span class="sxs-lookup"><span data-stu-id="186eb-186">System-Flags</span></span>           | <span data-ttu-id="186eb-187">0x00000010</span><span class="sxs-lookup"><span data-stu-id="186eb-187">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="186eb-188">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="186eb-188">Classes used in</span></span>        | [<span data-ttu-id="186eb-189">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="186eb-189">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="186eb-190">**居住人**</span><span class="sxs-lookup"><span data-stu-id="186eb-190">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="186eb-191">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="186eb-191">Windows Server 2003 R2</span></span>



| <span data-ttu-id="186eb-192">進入</span><span class="sxs-lookup"><span data-stu-id="186eb-192">Entry</span></span> | <span data-ttu-id="186eb-193">值</span><span class="sxs-lookup"><span data-stu-id="186eb-193">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186eb-194">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="186eb-194">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="186eb-195">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="186eb-195">MAPI-Id</span></span>                | <span data-ttu-id="186eb-196">0x3A17</span><span class="sxs-lookup"><span data-stu-id="186eb-196">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="186eb-197">System-Only</span><span class="sxs-lookup"><span data-stu-id="186eb-197">System-Only</span></span>            | <span data-ttu-id="186eb-198">否</span><span class="sxs-lookup"><span data-stu-id="186eb-198">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-199">是-單一值</span><span class="sxs-lookup"><span data-stu-id="186eb-199">Is-Single-Valued</span></span>       | <span data-ttu-id="186eb-200">對</span><span class="sxs-lookup"><span data-stu-id="186eb-200">True</span></span>                                                                                                                            |
| <span data-ttu-id="186eb-201">已編制索引</span><span class="sxs-lookup"><span data-stu-id="186eb-201">Is Indexed</span></span>             | <span data-ttu-id="186eb-202">否</span><span class="sxs-lookup"><span data-stu-id="186eb-202">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-203">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="186eb-203">In Global Catalog</span></span>      | <span data-ttu-id="186eb-204">否</span><span class="sxs-lookup"><span data-stu-id="186eb-204">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-205">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="186eb-205">NT-Security-Descriptor</span></span> | <span data-ttu-id="186eb-206">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="186eb-206">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="186eb-207">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="186eb-207">Range-Lower</span></span>            | <span data-ttu-id="186eb-208">1</span><span class="sxs-lookup"><span data-stu-id="186eb-208">1</span></span>                                                                                                                               |
| <span data-ttu-id="186eb-209">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="186eb-209">Range-Upper</span></span>            | <span data-ttu-id="186eb-210">64</span><span class="sxs-lookup"><span data-stu-id="186eb-210">64</span></span>                                                                                                                              |
| <span data-ttu-id="186eb-211">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="186eb-211">Search-Flags</span></span>           | <span data-ttu-id="186eb-212">0x00000000</span><span class="sxs-lookup"><span data-stu-id="186eb-212">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="186eb-213">System-Flags</span><span class="sxs-lookup"><span data-stu-id="186eb-213">System-Flags</span></span>           | <span data-ttu-id="186eb-214">0x00000010</span><span class="sxs-lookup"><span data-stu-id="186eb-214">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="186eb-215">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="186eb-215">Classes used in</span></span>        | [<span data-ttu-id="186eb-216">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="186eb-216">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="186eb-217">**居住人**</span><span class="sxs-lookup"><span data-stu-id="186eb-217">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="186eb-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="186eb-218">Windows Server 2008</span></span>



| <span data-ttu-id="186eb-219">進入</span><span class="sxs-lookup"><span data-stu-id="186eb-219">Entry</span></span> | <span data-ttu-id="186eb-220">值</span><span class="sxs-lookup"><span data-stu-id="186eb-220">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186eb-221">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="186eb-221">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="186eb-222">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="186eb-222">MAPI-Id</span></span>                | <span data-ttu-id="186eb-223">0x3A17</span><span class="sxs-lookup"><span data-stu-id="186eb-223">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="186eb-224">System-Only</span><span class="sxs-lookup"><span data-stu-id="186eb-224">System-Only</span></span>            | <span data-ttu-id="186eb-225">否</span><span class="sxs-lookup"><span data-stu-id="186eb-225">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-226">是-單一值</span><span class="sxs-lookup"><span data-stu-id="186eb-226">Is-Single-Valued</span></span>       | <span data-ttu-id="186eb-227">對</span><span class="sxs-lookup"><span data-stu-id="186eb-227">True</span></span>                                                                                                                            |
| <span data-ttu-id="186eb-228">已編制索引</span><span class="sxs-lookup"><span data-stu-id="186eb-228">Is Indexed</span></span>             | <span data-ttu-id="186eb-229">否</span><span class="sxs-lookup"><span data-stu-id="186eb-229">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-230">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="186eb-230">In Global Catalog</span></span>      | <span data-ttu-id="186eb-231">否</span><span class="sxs-lookup"><span data-stu-id="186eb-231">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-232">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="186eb-232">NT-Security-Descriptor</span></span> | <span data-ttu-id="186eb-233">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="186eb-233">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="186eb-234">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="186eb-234">Range-Lower</span></span>            | <span data-ttu-id="186eb-235">1</span><span class="sxs-lookup"><span data-stu-id="186eb-235">1</span></span>                                                                                                                               |
| <span data-ttu-id="186eb-236">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="186eb-236">Range-Upper</span></span>            | <span data-ttu-id="186eb-237">128</span><span class="sxs-lookup"><span data-stu-id="186eb-237">128</span></span>                                                                                                                             |
| <span data-ttu-id="186eb-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="186eb-238">Search-Flags</span></span>           | <span data-ttu-id="186eb-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="186eb-239">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="186eb-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="186eb-240">System-Flags</span></span>           | <span data-ttu-id="186eb-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="186eb-241">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="186eb-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="186eb-242">Classes used in</span></span>        | [<span data-ttu-id="186eb-243">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="186eb-243">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="186eb-244">**居住人**</span><span class="sxs-lookup"><span data-stu-id="186eb-244">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="186eb-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="186eb-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="186eb-246">進入</span><span class="sxs-lookup"><span data-stu-id="186eb-246">Entry</span></span> | <span data-ttu-id="186eb-247">值</span><span class="sxs-lookup"><span data-stu-id="186eb-247">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186eb-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="186eb-248">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="186eb-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="186eb-249">MAPI-Id</span></span>                | <span data-ttu-id="186eb-250">0x3A17</span><span class="sxs-lookup"><span data-stu-id="186eb-250">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="186eb-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="186eb-251">System-Only</span></span>            | <span data-ttu-id="186eb-252">否</span><span class="sxs-lookup"><span data-stu-id="186eb-252">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="186eb-253">Is-Single-Valued</span></span>       | <span data-ttu-id="186eb-254">對</span><span class="sxs-lookup"><span data-stu-id="186eb-254">True</span></span>                                                                                                                            |
| <span data-ttu-id="186eb-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="186eb-255">Is Indexed</span></span>             | <span data-ttu-id="186eb-256">否</span><span class="sxs-lookup"><span data-stu-id="186eb-256">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="186eb-257">In Global Catalog</span></span>      | <span data-ttu-id="186eb-258">否</span><span class="sxs-lookup"><span data-stu-id="186eb-258">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="186eb-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="186eb-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="186eb-260">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="186eb-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="186eb-261">Range-Lower</span></span>            | <span data-ttu-id="186eb-262">1</span><span class="sxs-lookup"><span data-stu-id="186eb-262">1</span></span>                                                                                                                               |
| <span data-ttu-id="186eb-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="186eb-263">Range-Upper</span></span>            | <span data-ttu-id="186eb-264">128</span><span class="sxs-lookup"><span data-stu-id="186eb-264">128</span></span>                                                                                                                             |
| <span data-ttu-id="186eb-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="186eb-265">Search-Flags</span></span>           | <span data-ttu-id="186eb-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="186eb-266">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="186eb-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="186eb-267">System-Flags</span></span>           | <span data-ttu-id="186eb-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="186eb-268">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="186eb-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="186eb-269">Classes used in</span></span>        | [<span data-ttu-id="186eb-270">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="186eb-270">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="186eb-271">**居住人**</span><span class="sxs-lookup"><span data-stu-id="186eb-271">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="186eb-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="186eb-272">Windows Server 2012</span></span>



| <span data-ttu-id="186eb-273">進入</span><span class="sxs-lookup"><span data-stu-id="186eb-273">Entry</span></span> | <span data-ttu-id="186eb-274">值</span><span class="sxs-lookup"><span data-stu-id="186eb-274">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186eb-275">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="186eb-275">Link-Id</span></span>                | \-                                                                                                                              |
| <span data-ttu-id="186eb-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="186eb-276">MAPI-Id</span></span>                | <span data-ttu-id="186eb-277">0x3A17</span><span class="sxs-lookup"><span data-stu-id="186eb-277">0x3A17</span></span>                                                                                                                          |
| <span data-ttu-id="186eb-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="186eb-278">System-Only</span></span>            | <span data-ttu-id="186eb-279">否</span><span class="sxs-lookup"><span data-stu-id="186eb-279">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="186eb-280">Is-Single-Valued</span></span>       | <span data-ttu-id="186eb-281">對</span><span class="sxs-lookup"><span data-stu-id="186eb-281">True</span></span>                                                                                                                            |
| <span data-ttu-id="186eb-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="186eb-282">Is Indexed</span></span>             | <span data-ttu-id="186eb-283">否</span><span class="sxs-lookup"><span data-stu-id="186eb-283">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="186eb-284">In Global Catalog</span></span>      | <span data-ttu-id="186eb-285">否</span><span class="sxs-lookup"><span data-stu-id="186eb-285">False</span></span>                                                                                                                           |
| <span data-ttu-id="186eb-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="186eb-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="186eb-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="186eb-287">O:BAG:BAD:S:</span></span>                                                                                                                    |
| <span data-ttu-id="186eb-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="186eb-288">Range-Lower</span></span>            | <span data-ttu-id="186eb-289">1</span><span class="sxs-lookup"><span data-stu-id="186eb-289">1</span></span>                                                                                                                               |
| <span data-ttu-id="186eb-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="186eb-290">Range-Upper</span></span>            | <span data-ttu-id="186eb-291">128</span><span class="sxs-lookup"><span data-stu-id="186eb-291">128</span></span>                                                                                                                             |
| <span data-ttu-id="186eb-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="186eb-292">Search-Flags</span></span>           | <span data-ttu-id="186eb-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="186eb-293">0x00000000</span></span>                                                                                                                      |
| <span data-ttu-id="186eb-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="186eb-294">System-Flags</span></span>           | <span data-ttu-id="186eb-295">0x00000010</span><span class="sxs-lookup"><span data-stu-id="186eb-295">0x00000010</span></span>                                                                                                                      |
| <span data-ttu-id="186eb-296">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="186eb-296">Classes used in</span></span>        | [<span data-ttu-id="186eb-297">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="186eb-297">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> [<span data-ttu-id="186eb-298">**居住人**</span><span class="sxs-lookup"><span data-stu-id="186eb-298">**Residential-Person**</span></span>](c-residentialperson.md)<br/> |



 

 





