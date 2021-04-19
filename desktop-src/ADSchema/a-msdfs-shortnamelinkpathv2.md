---
title: ms-DFS-簡短名稱-連結路徑-v2 屬性
description: 相對於 DFS 根目標共用的簡短名稱 DFS 連結路徑 (也就是沒有伺服器/網域和 DFS 命名空間名稱元件) 。 使用正斜線 (/) ，而不是反斜線 (\) ，因此可以完成 LDAP 搜尋，而不需要使用 esc。
ms.assetid: 0589d3f5-9734-4f95-bba9-22f13bb1c9f1
ms.tgt_platform: multiple
keywords:
- ms-DFS-簡短名稱-連結路徑-v2 屬性 AD 架構
- msDFS-ShortNameLinkPathv2 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DFS-Short-Name-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a536abdf13bed7acc99c1036d3c259493994b28
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973118"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="e050d-106">ms-DFS-簡短名稱-連結路徑-v2 屬性</span><span class="sxs-lookup"><span data-stu-id="e050d-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="e050d-107">相對於 DFS 根目標共用的簡短名稱 DFS 連結路徑 (也就是沒有伺服器/網域和 DFS 命名空間名稱元件) 。</span><span class="sxs-lookup"><span data-stu-id="e050d-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="e050d-108">使用正斜線 (/) ，而不是反斜線 (\) ，因此可以完成 LDAP 搜尋，而不需要使用 esc。</span><span class="sxs-lookup"><span data-stu-id="e050d-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="e050d-109">進入</span><span class="sxs-lookup"><span data-stu-id="e050d-109">Entry</span></span> | <span data-ttu-id="e050d-110">值</span><span class="sxs-lookup"><span data-stu-id="e050d-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e050d-111">CN</span><span class="sxs-lookup"><span data-stu-id="e050d-111">CN</span></span>                | <span data-ttu-id="e050d-112">ms-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="e050d-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="e050d-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e050d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e050d-114">msDFS-ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="e050d-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="e050d-115">大小</span><span class="sxs-lookup"><span data-stu-id="e050d-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="e050d-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e050d-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="e050d-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e050d-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e050d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e050d-118">Attribute-Id</span></span>      | <span data-ttu-id="e050d-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="e050d-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="e050d-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e050d-120">System-Id-Guid</span></span>    | <span data-ttu-id="e050d-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="e050d-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="e050d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="e050d-122">Syntax</span></span>            | [<span data-ttu-id="e050d-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e050d-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e050d-124">實作</span><span class="sxs-lookup"><span data-stu-id="e050d-124">Implementations</span></span>

-   [<span data-ttu-id="e050d-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e050d-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e050d-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e050d-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e050d-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e050d-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="e050d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e050d-128">Windows Server 2008</span></span>



| <span data-ttu-id="e050d-129">進入</span><span class="sxs-lookup"><span data-stu-id="e050d-129">Entry</span></span> | <span data-ttu-id="e050d-130">值</span><span class="sxs-lookup"><span data-stu-id="e050d-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e050d-131">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e050d-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e050d-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e050d-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e050d-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="e050d-133">System-Only</span></span>            | <span data-ttu-id="e050d-134">否</span><span class="sxs-lookup"><span data-stu-id="e050d-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="e050d-135">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e050d-135">Is-Single-Valued</span></span>       | <span data-ttu-id="e050d-136">對</span><span class="sxs-lookup"><span data-stu-id="e050d-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="e050d-137">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e050d-137">Is Indexed</span></span>             | <span data-ttu-id="e050d-138">否</span><span class="sxs-lookup"><span data-stu-id="e050d-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="e050d-139">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e050d-139">In Global Catalog</span></span>      | <span data-ttu-id="e050d-140">否</span><span class="sxs-lookup"><span data-stu-id="e050d-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="e050d-141">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e050d-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="e050d-142">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e050d-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="e050d-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e050d-143">Range-Lower</span></span>            | <span data-ttu-id="e050d-144">0</span><span class="sxs-lookup"><span data-stu-id="e050d-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="e050d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e050d-145">Range-Upper</span></span>            | <span data-ttu-id="e050d-146">32766</span><span class="sxs-lookup"><span data-stu-id="e050d-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="e050d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e050d-147">Search-Flags</span></span>           | <span data-ttu-id="e050d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e050d-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="e050d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e050d-149">System-Flags</span></span>           | <span data-ttu-id="e050d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e050d-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="e050d-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e050d-151">Classes used in</span></span>        | [<span data-ttu-id="e050d-152">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="e050d-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="e050d-153">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="e050d-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e050d-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e050d-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e050d-155">進入</span><span class="sxs-lookup"><span data-stu-id="e050d-155">Entry</span></span> | <span data-ttu-id="e050d-156">值</span><span class="sxs-lookup"><span data-stu-id="e050d-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e050d-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e050d-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e050d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e050d-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e050d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e050d-159">System-Only</span></span>            | <span data-ttu-id="e050d-160">否</span><span class="sxs-lookup"><span data-stu-id="e050d-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="e050d-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e050d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e050d-162">對</span><span class="sxs-lookup"><span data-stu-id="e050d-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="e050d-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e050d-163">Is Indexed</span></span>             | <span data-ttu-id="e050d-164">否</span><span class="sxs-lookup"><span data-stu-id="e050d-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="e050d-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e050d-165">In Global Catalog</span></span>      | <span data-ttu-id="e050d-166">否</span><span class="sxs-lookup"><span data-stu-id="e050d-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="e050d-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e050d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e050d-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e050d-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="e050d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e050d-169">Range-Lower</span></span>            | <span data-ttu-id="e050d-170">0</span><span class="sxs-lookup"><span data-stu-id="e050d-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="e050d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e050d-171">Range-Upper</span></span>            | <span data-ttu-id="e050d-172">32766</span><span class="sxs-lookup"><span data-stu-id="e050d-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="e050d-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e050d-173">Search-Flags</span></span>           | <span data-ttu-id="e050d-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e050d-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="e050d-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e050d-175">System-Flags</span></span>           | <span data-ttu-id="e050d-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e050d-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="e050d-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e050d-177">Classes used in</span></span>        | [<span data-ttu-id="e050d-178">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="e050d-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="e050d-179">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="e050d-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e050d-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e050d-180">Windows Server 2012</span></span>



| <span data-ttu-id="e050d-181">進入</span><span class="sxs-lookup"><span data-stu-id="e050d-181">Entry</span></span> | <span data-ttu-id="e050d-182">值</span><span class="sxs-lookup"><span data-stu-id="e050d-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e050d-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e050d-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e050d-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e050d-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e050d-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="e050d-185">System-Only</span></span>            | <span data-ttu-id="e050d-186">否</span><span class="sxs-lookup"><span data-stu-id="e050d-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="e050d-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e050d-187">Is-Single-Valued</span></span>       | <span data-ttu-id="e050d-188">對</span><span class="sxs-lookup"><span data-stu-id="e050d-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="e050d-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e050d-189">Is Indexed</span></span>             | <span data-ttu-id="e050d-190">否</span><span class="sxs-lookup"><span data-stu-id="e050d-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="e050d-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e050d-191">In Global Catalog</span></span>      | <span data-ttu-id="e050d-192">否</span><span class="sxs-lookup"><span data-stu-id="e050d-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="e050d-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e050d-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="e050d-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e050d-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="e050d-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e050d-195">Range-Lower</span></span>            | <span data-ttu-id="e050d-196">0</span><span class="sxs-lookup"><span data-stu-id="e050d-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="e050d-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e050d-197">Range-Upper</span></span>            | <span data-ttu-id="e050d-198">32766</span><span class="sxs-lookup"><span data-stu-id="e050d-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="e050d-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e050d-199">Search-Flags</span></span>           | <span data-ttu-id="e050d-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e050d-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="e050d-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e050d-201">System-Flags</span></span>           | <span data-ttu-id="e050d-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e050d-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="e050d-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e050d-203">Classes used in</span></span>        | [<span data-ttu-id="e050d-204">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="e050d-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="e050d-205">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="e050d-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





