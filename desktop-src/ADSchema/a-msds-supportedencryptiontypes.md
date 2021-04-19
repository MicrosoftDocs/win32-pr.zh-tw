---
title: 支援 ms DS-加密類型屬性
description: 使用者、電腦或信任帳戶所支援的加密演算法。請注意，KDC 會在產生此帳戶的服務票證時使用此資訊。
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- 支援的 ms DS-加密類型屬性 AD 架構
- '>msds-supportedencryptiontypes 屬性 AD 架構'
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab16959d1f1cd4405cb661a6026f3734a134f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971265"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a><span data-ttu-id="21991-105">支援 ms DS-加密類型屬性</span><span class="sxs-lookup"><span data-stu-id="21991-105">ms-DS-Supported-Encryption-Types attribute</span></span>

<span data-ttu-id="21991-106">使用者、電腦或信任帳戶支援的加密演算法。</span><span class="sxs-lookup"><span data-stu-id="21991-106">The encryption algorithms supported by user, computer or trust accounts.</span></span>

> [!Note]  
> <span data-ttu-id="21991-107">KDC 在產生此帳戶的服務票證時使用此資訊。</span><span class="sxs-lookup"><span data-stu-id="21991-107">The KDC uses this information while generating a service ticket for this account.</span></span> <span data-ttu-id="21991-108">服務與電腦可以在 Active Directory 中的個別帳戶上自動更新此屬性，因此需要此屬性的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="21991-108">Services and Computers can automatically update this attribute on their respective accounts in Active Directory, and therefore need write access to this attribute.</span></span>

 



| <span data-ttu-id="21991-109">進入</span><span class="sxs-lookup"><span data-stu-id="21991-109">Entry</span></span> | <span data-ttu-id="21991-110">值</span><span class="sxs-lookup"><span data-stu-id="21991-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="21991-111">CN</span><span class="sxs-lookup"><span data-stu-id="21991-111">CN</span></span>                | <span data-ttu-id="21991-112">支援的 ms DS-加密類型</span><span class="sxs-lookup"><span data-stu-id="21991-112">ms-DS-Supported-Encryption-Types</span></span>     |
| <span data-ttu-id="21991-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="21991-113">Ldap-Display-Name</span></span> | <span data-ttu-id="21991-114">msDS-SupportedEncryptionTypes</span><span class="sxs-lookup"><span data-stu-id="21991-114">msDS-SupportedEncryptionTypes</span></span>        |
| <span data-ttu-id="21991-115">大小</span><span class="sxs-lookup"><span data-stu-id="21991-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="21991-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="21991-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="21991-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="21991-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="21991-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="21991-118">Attribute-Id</span></span>      | <span data-ttu-id="21991-119">1.2.840.113556.1.4.1963</span><span class="sxs-lookup"><span data-stu-id="21991-119">1.2.840.113556.1.4.1963</span></span>              |
| <span data-ttu-id="21991-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="21991-120">System-Id-Guid</span></span>    | <span data-ttu-id="21991-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span><span class="sxs-lookup"><span data-stu-id="21991-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span></span> |
| <span data-ttu-id="21991-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="21991-122">Syntax</span></span>            | [<span data-ttu-id="21991-123">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="21991-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="21991-124">實作</span><span class="sxs-lookup"><span data-stu-id="21991-124">Implementations</span></span>

-   [<span data-ttu-id="21991-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="21991-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="21991-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="21991-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="21991-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="21991-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="21991-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21991-128">Windows Server 2008</span></span>



| <span data-ttu-id="21991-129">進入</span><span class="sxs-lookup"><span data-stu-id="21991-129">Entry</span></span> | <span data-ttu-id="21991-130">值</span><span class="sxs-lookup"><span data-stu-id="21991-130">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21991-131">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21991-131">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="21991-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21991-132">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="21991-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="21991-133">System-Only</span></span>            | <span data-ttu-id="21991-134">否</span><span class="sxs-lookup"><span data-stu-id="21991-134">False</span></span>                                                                                  |
| <span data-ttu-id="21991-135">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21991-135">Is-Single-Valued</span></span>       | <span data-ttu-id="21991-136">對</span><span class="sxs-lookup"><span data-stu-id="21991-136">True</span></span>                                                                                   |
| <span data-ttu-id="21991-137">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21991-137">Is Indexed</span></span>             | <span data-ttu-id="21991-138">否</span><span class="sxs-lookup"><span data-stu-id="21991-138">False</span></span>                                                                                  |
| <span data-ttu-id="21991-139">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21991-139">In Global Catalog</span></span>      | <span data-ttu-id="21991-140">否</span><span class="sxs-lookup"><span data-stu-id="21991-140">False</span></span>                                                                                  |
| <span data-ttu-id="21991-141">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21991-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="21991-142">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21991-142">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="21991-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21991-143">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="21991-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21991-144">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="21991-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21991-145">Search-Flags</span></span>           | <span data-ttu-id="21991-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21991-146">0x00000000</span></span>                                                                             |
| <span data-ttu-id="21991-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21991-147">System-Flags</span></span>           | <span data-ttu-id="21991-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21991-148">0x00000010</span></span>                                                                             |
| <span data-ttu-id="21991-149">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21991-149">Classes used in</span></span>        | [<span data-ttu-id="21991-150">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="21991-150">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="21991-151">**User**</span><span class="sxs-lookup"><span data-stu-id="21991-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="21991-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21991-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="21991-153">進入</span><span class="sxs-lookup"><span data-stu-id="21991-153">Entry</span></span> | <span data-ttu-id="21991-154">值</span><span class="sxs-lookup"><span data-stu-id="21991-154">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21991-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21991-155">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="21991-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21991-156">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="21991-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="21991-157">System-Only</span></span>            | <span data-ttu-id="21991-158">否</span><span class="sxs-lookup"><span data-stu-id="21991-158">False</span></span>                                                                                  |
| <span data-ttu-id="21991-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21991-159">Is-Single-Valued</span></span>       | <span data-ttu-id="21991-160">對</span><span class="sxs-lookup"><span data-stu-id="21991-160">True</span></span>                                                                                   |
| <span data-ttu-id="21991-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21991-161">Is Indexed</span></span>             | <span data-ttu-id="21991-162">否</span><span class="sxs-lookup"><span data-stu-id="21991-162">False</span></span>                                                                                  |
| <span data-ttu-id="21991-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21991-163">In Global Catalog</span></span>      | <span data-ttu-id="21991-164">否</span><span class="sxs-lookup"><span data-stu-id="21991-164">False</span></span>                                                                                  |
| <span data-ttu-id="21991-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21991-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="21991-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21991-166">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="21991-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21991-167">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="21991-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21991-168">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="21991-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21991-169">Search-Flags</span></span>           | <span data-ttu-id="21991-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21991-170">0x00000000</span></span>                                                                             |
| <span data-ttu-id="21991-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21991-171">System-Flags</span></span>           | <span data-ttu-id="21991-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21991-172">0x00000010</span></span>                                                                             |
| <span data-ttu-id="21991-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21991-173">Classes used in</span></span>        | [<span data-ttu-id="21991-174">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="21991-174">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="21991-175">**User**</span><span class="sxs-lookup"><span data-stu-id="21991-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="21991-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21991-176">Windows Server 2012</span></span>



| <span data-ttu-id="21991-177">進入</span><span class="sxs-lookup"><span data-stu-id="21991-177">Entry</span></span> | <span data-ttu-id="21991-178">值</span><span class="sxs-lookup"><span data-stu-id="21991-178">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21991-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="21991-179">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="21991-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21991-180">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="21991-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="21991-181">System-Only</span></span>            | <span data-ttu-id="21991-182">否</span><span class="sxs-lookup"><span data-stu-id="21991-182">False</span></span>                                                                                  |
| <span data-ttu-id="21991-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="21991-183">Is-Single-Valued</span></span>       | <span data-ttu-id="21991-184">對</span><span class="sxs-lookup"><span data-stu-id="21991-184">True</span></span>                                                                                   |
| <span data-ttu-id="21991-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="21991-185">Is Indexed</span></span>             | <span data-ttu-id="21991-186">否</span><span class="sxs-lookup"><span data-stu-id="21991-186">False</span></span>                                                                                  |
| <span data-ttu-id="21991-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="21991-187">In Global Catalog</span></span>      | <span data-ttu-id="21991-188">否</span><span class="sxs-lookup"><span data-stu-id="21991-188">False</span></span>                                                                                  |
| <span data-ttu-id="21991-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="21991-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="21991-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="21991-190">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="21991-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21991-191">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="21991-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21991-192">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="21991-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21991-193">Search-Flags</span></span>           | <span data-ttu-id="21991-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21991-194">0x00000000</span></span>                                                                             |
| <span data-ttu-id="21991-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21991-195">System-Flags</span></span>           | <span data-ttu-id="21991-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21991-196">0x00000010</span></span>                                                                             |
| <span data-ttu-id="21991-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="21991-197">Classes used in</span></span>        | [<span data-ttu-id="21991-198">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="21991-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="21991-199">**User**</span><span class="sxs-lookup"><span data-stu-id="21991-199">**User**</span></span>](c-user.md)<br/> |



 

 





