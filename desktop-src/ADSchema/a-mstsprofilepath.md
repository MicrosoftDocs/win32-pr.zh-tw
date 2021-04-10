---
title: ms-TS-設定檔-Path 屬性
description: 終端機服務設定檔路徑指定當使用者登入終端機伺服器時，所要使用的漫遊或強制設定檔路徑。 設定檔路徑採用下列網路路徑格式： \\ \\ ServerName \\ ProfilesFolderName \\ UserName。
ms.assetid: 9b13f91d-c3ee-4862-800c-fda831dce859
ms.tgt_platform: multiple
keywords:
- ms-TS-設定檔-Path 屬性 AD 架構
- msTSProfilePath 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-TS-Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67243c2ef588bd1470a50417c0948b1ea4ea7fa9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935382"
---
# <a name="ms-ts-profile-path-attribute"></a><span data-ttu-id="3cc04-106">ms-TS-設定檔-Path 屬性</span><span class="sxs-lookup"><span data-stu-id="3cc04-106">ms-TS-Profile-Path attribute</span></span>

<span data-ttu-id="3cc04-107">終端機服務設定檔路徑指定當使用者登入終端機伺服器時，所要使用的漫遊或強制設定檔路徑。</span><span class="sxs-lookup"><span data-stu-id="3cc04-107">Terminal Services Profile Path specifies a roaming or mandatory profile path to use when the user logs on to the terminal server.</span></span> <span data-ttu-id="3cc04-108">設定檔路徑採用下列網路路徑格式： **\\\\** _ServerName_ *_\\_* _ProfilesFolderName_ *_\\_* _UserName_。</span><span class="sxs-lookup"><span data-stu-id="3cc04-108">The profile path is in the following network path format: **\\\\**_ServerName_*_\\_*_ProfilesFolderName_*_\\_*_UserName_.</span></span>



| <span data-ttu-id="3cc04-109">進入</span><span class="sxs-lookup"><span data-stu-id="3cc04-109">Entry</span></span> | <span data-ttu-id="3cc04-110">值</span><span class="sxs-lookup"><span data-stu-id="3cc04-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3cc04-111">CN</span><span class="sxs-lookup"><span data-stu-id="3cc04-111">CN</span></span>                | <span data-ttu-id="3cc04-112">ms-TS-Profile-Path</span><span class="sxs-lookup"><span data-stu-id="3cc04-112">ms-TS-Profile-Path</span></span>                          |
| <span data-ttu-id="3cc04-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3cc04-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3cc04-114">msTSProfilePath</span><span class="sxs-lookup"><span data-stu-id="3cc04-114">msTSProfilePath</span></span>                             |
| <span data-ttu-id="3cc04-115">大小</span><span class="sxs-lookup"><span data-stu-id="3cc04-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="3cc04-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="3cc04-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="3cc04-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="3cc04-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="3cc04-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3cc04-118">Attribute-Id</span></span>      | <span data-ttu-id="3cc04-119">1.2.840.113556.1.4.1976</span><span class="sxs-lookup"><span data-stu-id="3cc04-119">1.2.840.113556.1.4.1976</span></span>                     |
| <span data-ttu-id="3cc04-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="3cc04-120">System-Id-Guid</span></span>    | <span data-ttu-id="3cc04-121">e65c30db-316c-4060-a3a0-387b083f09cd</span><span class="sxs-lookup"><span data-stu-id="3cc04-121">e65c30db-316c-4060-a3a0-387b083f09cd</span></span>        |
| <span data-ttu-id="3cc04-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cc04-122">Syntax</span></span>            | [<span data-ttu-id="3cc04-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3cc04-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3cc04-124">實作</span><span class="sxs-lookup"><span data-stu-id="3cc04-124">Implementations</span></span>

-   [<span data-ttu-id="3cc04-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3cc04-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3cc04-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3cc04-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3cc04-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3cc04-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="3cc04-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cc04-128">Windows Server 2008</span></span>



| <span data-ttu-id="3cc04-129">進入</span><span class="sxs-lookup"><span data-stu-id="3cc04-129">Entry</span></span> | <span data-ttu-id="3cc04-130">值</span><span class="sxs-lookup"><span data-stu-id="3cc04-130">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="3cc04-131">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3cc04-131">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="3cc04-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cc04-132">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="3cc04-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cc04-133">System-Only</span></span>            | <span data-ttu-id="3cc04-134">否</span><span class="sxs-lookup"><span data-stu-id="3cc04-134">False</span></span>                             |
| <span data-ttu-id="3cc04-135">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3cc04-135">Is-Single-Valued</span></span>       | <span data-ttu-id="3cc04-136">對</span><span class="sxs-lookup"><span data-stu-id="3cc04-136">True</span></span>                              |
| <span data-ttu-id="3cc04-137">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3cc04-137">Is Indexed</span></span>             | <span data-ttu-id="3cc04-138">否</span><span class="sxs-lookup"><span data-stu-id="3cc04-138">False</span></span>                             |
| <span data-ttu-id="3cc04-139">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3cc04-139">In Global Catalog</span></span>      | <span data-ttu-id="3cc04-140">否</span><span class="sxs-lookup"><span data-stu-id="3cc04-140">False</span></span>                             |
| <span data-ttu-id="3cc04-141">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3cc04-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cc04-142">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3cc04-142">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="3cc04-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cc04-143">Range-Lower</span></span>            | <span data-ttu-id="3cc04-144">0</span><span class="sxs-lookup"><span data-stu-id="3cc04-144">0</span></span>                                 |
| <span data-ttu-id="3cc04-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cc04-145">Range-Upper</span></span>            | <span data-ttu-id="3cc04-146">32767</span><span class="sxs-lookup"><span data-stu-id="3cc04-146">32767</span></span>                             |
| <span data-ttu-id="3cc04-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cc04-147">Search-Flags</span></span>           | <span data-ttu-id="3cc04-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cc04-148">0x00000000</span></span>                        |
| <span data-ttu-id="3cc04-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cc04-149">System-Flags</span></span>           | <span data-ttu-id="3cc04-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3cc04-150">0x00000010</span></span>                        |
| <span data-ttu-id="3cc04-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3cc04-151">Classes used in</span></span>        | [<span data-ttu-id="3cc04-152">**User**</span><span class="sxs-lookup"><span data-stu-id="3cc04-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3cc04-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3cc04-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3cc04-154">進入</span><span class="sxs-lookup"><span data-stu-id="3cc04-154">Entry</span></span> | <span data-ttu-id="3cc04-155">值</span><span class="sxs-lookup"><span data-stu-id="3cc04-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="3cc04-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3cc04-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="3cc04-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cc04-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="3cc04-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cc04-158">System-Only</span></span>            | <span data-ttu-id="3cc04-159">否</span><span class="sxs-lookup"><span data-stu-id="3cc04-159">False</span></span>                             |
| <span data-ttu-id="3cc04-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3cc04-160">Is-Single-Valued</span></span>       | <span data-ttu-id="3cc04-161">對</span><span class="sxs-lookup"><span data-stu-id="3cc04-161">True</span></span>                              |
| <span data-ttu-id="3cc04-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3cc04-162">Is Indexed</span></span>             | <span data-ttu-id="3cc04-163">否</span><span class="sxs-lookup"><span data-stu-id="3cc04-163">False</span></span>                             |
| <span data-ttu-id="3cc04-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3cc04-164">In Global Catalog</span></span>      | <span data-ttu-id="3cc04-165">否</span><span class="sxs-lookup"><span data-stu-id="3cc04-165">False</span></span>                             |
| <span data-ttu-id="3cc04-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3cc04-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cc04-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3cc04-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="3cc04-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cc04-168">Range-Lower</span></span>            | <span data-ttu-id="3cc04-169">0</span><span class="sxs-lookup"><span data-stu-id="3cc04-169">0</span></span>                                 |
| <span data-ttu-id="3cc04-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cc04-170">Range-Upper</span></span>            | <span data-ttu-id="3cc04-171">32767</span><span class="sxs-lookup"><span data-stu-id="3cc04-171">32767</span></span>                             |
| <span data-ttu-id="3cc04-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cc04-172">Search-Flags</span></span>           | <span data-ttu-id="3cc04-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cc04-173">0x00000000</span></span>                        |
| <span data-ttu-id="3cc04-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cc04-174">System-Flags</span></span>           | <span data-ttu-id="3cc04-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3cc04-175">0x00000010</span></span>                        |
| <span data-ttu-id="3cc04-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3cc04-176">Classes used in</span></span>        | [<span data-ttu-id="3cc04-177">**User**</span><span class="sxs-lookup"><span data-stu-id="3cc04-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3cc04-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3cc04-178">Windows Server 2012</span></span>



| <span data-ttu-id="3cc04-179">進入</span><span class="sxs-lookup"><span data-stu-id="3cc04-179">Entry</span></span> | <span data-ttu-id="3cc04-180">值</span><span class="sxs-lookup"><span data-stu-id="3cc04-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="3cc04-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3cc04-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="3cc04-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3cc04-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="3cc04-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="3cc04-183">System-Only</span></span>            | <span data-ttu-id="3cc04-184">否</span><span class="sxs-lookup"><span data-stu-id="3cc04-184">False</span></span>                             |
| <span data-ttu-id="3cc04-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3cc04-185">Is-Single-Valued</span></span>       | <span data-ttu-id="3cc04-186">對</span><span class="sxs-lookup"><span data-stu-id="3cc04-186">True</span></span>                              |
| <span data-ttu-id="3cc04-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3cc04-187">Is Indexed</span></span>             | <span data-ttu-id="3cc04-188">否</span><span class="sxs-lookup"><span data-stu-id="3cc04-188">False</span></span>                             |
| <span data-ttu-id="3cc04-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3cc04-189">In Global Catalog</span></span>      | <span data-ttu-id="3cc04-190">否</span><span class="sxs-lookup"><span data-stu-id="3cc04-190">False</span></span>                             |
| <span data-ttu-id="3cc04-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3cc04-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="3cc04-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3cc04-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="3cc04-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3cc04-193">Range-Lower</span></span>            | <span data-ttu-id="3cc04-194">0</span><span class="sxs-lookup"><span data-stu-id="3cc04-194">0</span></span>                                 |
| <span data-ttu-id="3cc04-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3cc04-195">Range-Upper</span></span>            | <span data-ttu-id="3cc04-196">32767</span><span class="sxs-lookup"><span data-stu-id="3cc04-196">32767</span></span>                             |
| <span data-ttu-id="3cc04-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3cc04-197">Search-Flags</span></span>           | <span data-ttu-id="3cc04-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3cc04-198">0x00000000</span></span>                        |
| <span data-ttu-id="3cc04-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3cc04-199">System-Flags</span></span>           | <span data-ttu-id="3cc04-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3cc04-200">0x00000010</span></span>                        |
| <span data-ttu-id="3cc04-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3cc04-201">Classes used in</span></span>        | [<span data-ttu-id="3cc04-202">**User**</span><span class="sxs-lookup"><span data-stu-id="3cc04-202">**User**</span></span>](c-user.md)<br/> |



 

 





