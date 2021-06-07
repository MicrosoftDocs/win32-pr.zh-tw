---
title: ms-DFS-連結-路徑-v2 屬性
description: 相對於 DFS 根目標共用的 DFS 連結路徑 (也就是，沒有伺服器/網域和 DFS 命名空間名稱元件) 。 使用正斜線 (/) ，而不是反斜線 (\) ，因此可以完成 LDAP 搜尋，而不需要使用 esc。
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- ms-DFS-連結-路徑-v2 屬性 AD 架構
- msDFS-LinkPathv2 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4659dbf00c6a53c77a23e98836ea1af4eeb4c38a
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386857"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="a48bc-106">ms-DFS-連結-路徑-v2 屬性</span><span class="sxs-lookup"><span data-stu-id="a48bc-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="a48bc-107">相對於 DFS 根目標共用的 DFS 連結路徑 (也就是，沒有伺服器/網域和 DFS 命名空間名稱元件) 。</span><span class="sxs-lookup"><span data-stu-id="a48bc-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="a48bc-108">使用正斜線 (/) ，而不是反斜線 (\\) ，如此就可以完成 LDAP 搜尋，而不需要使用 esc。</span><span class="sxs-lookup"><span data-stu-id="a48bc-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="a48bc-109">進入</span><span class="sxs-lookup"><span data-stu-id="a48bc-109">Entry</span></span> | <span data-ttu-id="a48bc-110">值</span><span class="sxs-lookup"><span data-stu-id="a48bc-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a48bc-111">CN</span><span class="sxs-lookup"><span data-stu-id="a48bc-111">CN</span></span>                | <span data-ttu-id="a48bc-112">ms-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="a48bc-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="a48bc-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a48bc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a48bc-114">msDFS-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="a48bc-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="a48bc-115">大小</span><span class="sxs-lookup"><span data-stu-id="a48bc-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="a48bc-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a48bc-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="a48bc-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a48bc-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a48bc-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a48bc-118">Attribute-Id</span></span>      | <span data-ttu-id="a48bc-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="a48bc-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="a48bc-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a48bc-120">System-Id-Guid</span></span>    | <span data-ttu-id="a48bc-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="a48bc-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="a48bc-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="a48bc-122">Syntax</span></span>            | [<span data-ttu-id="a48bc-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="a48bc-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a48bc-124">實作</span><span class="sxs-lookup"><span data-stu-id="a48bc-124">Implementations</span></span>

-   [<span data-ttu-id="a48bc-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a48bc-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a48bc-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a48bc-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a48bc-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a48bc-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="a48bc-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a48bc-128">Windows Server 2008</span></span>



| <span data-ttu-id="a48bc-129">進入</span><span class="sxs-lookup"><span data-stu-id="a48bc-129">Entry</span></span> | <span data-ttu-id="a48bc-130">值</span><span class="sxs-lookup"><span data-stu-id="a48bc-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a48bc-131">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a48bc-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="a48bc-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a48bc-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="a48bc-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="a48bc-133">System-Only</span></span>            | <span data-ttu-id="a48bc-134">False</span><span class="sxs-lookup"><span data-stu-id="a48bc-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="a48bc-135">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a48bc-135">Is-Single-Valued</span></span>       | <span data-ttu-id="a48bc-136">True</span><span class="sxs-lookup"><span data-stu-id="a48bc-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="a48bc-137">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a48bc-137">Is Indexed</span></span>             | <span data-ttu-id="a48bc-138">False</span><span class="sxs-lookup"><span data-stu-id="a48bc-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="a48bc-139">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a48bc-139">In Global Catalog</span></span>      | <span data-ttu-id="a48bc-140">False</span><span class="sxs-lookup"><span data-stu-id="a48bc-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="a48bc-141">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a48bc-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="a48bc-142">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a48bc-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="a48bc-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a48bc-143">Range-Lower</span></span>            | <span data-ttu-id="a48bc-144">0</span><span class="sxs-lookup"><span data-stu-id="a48bc-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="a48bc-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a48bc-145">Range-Upper</span></span>            | <span data-ttu-id="a48bc-146">32766</span><span class="sxs-lookup"><span data-stu-id="a48bc-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="a48bc-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a48bc-147">Search-Flags</span></span>           | <span data-ttu-id="a48bc-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a48bc-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="a48bc-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a48bc-149">System-Flags</span></span>           | <span data-ttu-id="a48bc-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a48bc-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a48bc-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a48bc-151">Classes used in</span></span>        | [<span data-ttu-id="a48bc-152">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="a48bc-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="a48bc-153">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="a48bc-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a48bc-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a48bc-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a48bc-155">進入</span><span class="sxs-lookup"><span data-stu-id="a48bc-155">Entry</span></span> | <span data-ttu-id="a48bc-156">值</span><span class="sxs-lookup"><span data-stu-id="a48bc-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a48bc-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a48bc-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="a48bc-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a48bc-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="a48bc-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a48bc-159">System-Only</span></span>            | <span data-ttu-id="a48bc-160">False</span><span class="sxs-lookup"><span data-stu-id="a48bc-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="a48bc-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a48bc-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a48bc-162">True</span><span class="sxs-lookup"><span data-stu-id="a48bc-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="a48bc-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a48bc-163">Is Indexed</span></span>             | <span data-ttu-id="a48bc-164">False</span><span class="sxs-lookup"><span data-stu-id="a48bc-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="a48bc-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a48bc-165">In Global Catalog</span></span>      | <span data-ttu-id="a48bc-166">False</span><span class="sxs-lookup"><span data-stu-id="a48bc-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="a48bc-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a48bc-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a48bc-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a48bc-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="a48bc-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a48bc-169">Range-Lower</span></span>            | <span data-ttu-id="a48bc-170">0</span><span class="sxs-lookup"><span data-stu-id="a48bc-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="a48bc-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a48bc-171">Range-Upper</span></span>            | <span data-ttu-id="a48bc-172">32766</span><span class="sxs-lookup"><span data-stu-id="a48bc-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="a48bc-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a48bc-173">Search-Flags</span></span>           | <span data-ttu-id="a48bc-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a48bc-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="a48bc-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a48bc-175">System-Flags</span></span>           | <span data-ttu-id="a48bc-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a48bc-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a48bc-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a48bc-177">Classes used in</span></span>        | [<span data-ttu-id="a48bc-178">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="a48bc-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="a48bc-179">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="a48bc-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a48bc-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a48bc-180">Windows Server 2012</span></span>



| <span data-ttu-id="a48bc-181">進入</span><span class="sxs-lookup"><span data-stu-id="a48bc-181">Entry</span></span> | <span data-ttu-id="a48bc-182">值</span><span class="sxs-lookup"><span data-stu-id="a48bc-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a48bc-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a48bc-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="a48bc-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a48bc-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="a48bc-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="a48bc-185">System-Only</span></span>            | <span data-ttu-id="a48bc-186">False</span><span class="sxs-lookup"><span data-stu-id="a48bc-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="a48bc-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a48bc-187">Is-Single-Valued</span></span>       | <span data-ttu-id="a48bc-188">True</span><span class="sxs-lookup"><span data-stu-id="a48bc-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="a48bc-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a48bc-189">Is Indexed</span></span>             | <span data-ttu-id="a48bc-190">False</span><span class="sxs-lookup"><span data-stu-id="a48bc-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="a48bc-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a48bc-191">In Global Catalog</span></span>      | <span data-ttu-id="a48bc-192">False</span><span class="sxs-lookup"><span data-stu-id="a48bc-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="a48bc-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a48bc-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="a48bc-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a48bc-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="a48bc-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a48bc-195">Range-Lower</span></span>            | <span data-ttu-id="a48bc-196">0</span><span class="sxs-lookup"><span data-stu-id="a48bc-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="a48bc-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a48bc-197">Range-Upper</span></span>            | <span data-ttu-id="a48bc-198">32766</span><span class="sxs-lookup"><span data-stu-id="a48bc-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="a48bc-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a48bc-199">Search-Flags</span></span>           | <span data-ttu-id="a48bc-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a48bc-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="a48bc-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a48bc-201">System-Flags</span></span>           | <span data-ttu-id="a48bc-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a48bc-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="a48bc-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a48bc-203">Classes used in</span></span>        | [<span data-ttu-id="a48bc-204">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="a48bc-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="a48bc-205">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="a48bc-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





