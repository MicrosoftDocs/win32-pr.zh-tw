---
title: ms DS-複寫-驗證模式屬性
description: Ms DS-複寫驗證模式屬性是用來指定用來驗證複寫夥伴的驗證方法。
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- ms DS-複寫-驗證模式屬性 AD 架構
- Msds-replauthenticationmode 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b88c7e3223b946b56962b710b036ee6e0c36dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467350"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a><span data-ttu-id="37cb8-105">ms DS-複寫-驗證模式屬性</span><span class="sxs-lookup"><span data-stu-id="37cb8-105">ms-DS-Repl-Authentication-Mode attribute</span></span>

<span data-ttu-id="37cb8-106">**MS DS-複寫驗證模式** 屬性是用來指定用來驗證複寫夥伴的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="37cb8-106">The **ms-DS-Repl-Authentication-Mode** attribute is used to specify which authentication method is used to authenticate replication partners.</span></span> <span data-ttu-id="37cb8-107">這個屬性會套用至 ADAM 實例的設定磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="37cb8-107">This attribute applies to the configuration partition of an ADAM instance.</span></span>

<span data-ttu-id="37cb8-108">下列值是這個屬性的可能值。</span><span class="sxs-lookup"><span data-stu-id="37cb8-108">The following values are the possible values for this attribute.</span></span>

| <span data-ttu-id="37cb8-109">值</span><span class="sxs-lookup"><span data-stu-id="37cb8-109">Value</span></span>        | <span data-ttu-id="37cb8-110">驗證方法</span><span class="sxs-lookup"><span data-stu-id="37cb8-110">Authentication method</span></span>                          | <span data-ttu-id="37cb8-111">描述</span><span class="sxs-lookup"><span data-stu-id="37cb8-111">Description</span></span>                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37cb8-112">0</span><span class="sxs-lookup"><span data-stu-id="37cb8-112">0</span></span><br/> | <span data-ttu-id="37cb8-113">交涉傳遞</span><span class="sxs-lookup"><span data-stu-id="37cb8-113">Negotiated pass-through</span></span><br/>             | <span data-ttu-id="37cb8-114">設定集中的所有 ADAM 實例都使用與 ADAM 服務帳戶相同的帳戶名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="37cb8-114">All ADAM instances in the configuration set use an identical account name and password as the ADAM service account.</span></span><br/>                                                 |
| <span data-ttu-id="37cb8-115">1</span><span class="sxs-lookup"><span data-stu-id="37cb8-115">1</span></span><br/> | <span data-ttu-id="37cb8-116">已交涉</span><span class="sxs-lookup"><span data-stu-id="37cb8-116">Negotiated</span></span><br/>                          | <span data-ttu-id="37cb8-117">會先嘗試 Kerberos 驗證 (使用 SPN)；</span><span class="sxs-lookup"><span data-stu-id="37cb8-117">Kerberos authentication (using SPNs) is attempted first.</span></span> <span data-ttu-id="37cb8-118">如果 Kerberos 失敗，則會嘗試 NTLM 驗證。</span><span class="sxs-lookup"><span data-stu-id="37cb8-118">If Kerberos fails, NTLM authentication is attempted.</span></span> <span data-ttu-id="37cb8-119">如果 NTLM 失敗，ADAM 實例將不會複寫。</span><span class="sxs-lookup"><span data-stu-id="37cb8-119">If NTLM fails, the ADAM instances will not replicate.</span></span><br/> |
| <span data-ttu-id="37cb8-120">2</span><span class="sxs-lookup"><span data-stu-id="37cb8-120">2</span></span><br/> | <span data-ttu-id="37cb8-121">以 Kerberos 相互驗證</span><span class="sxs-lookup"><span data-stu-id="37cb8-121">Mutual authentication with Kerberos</span></span><br/> | <span data-ttu-id="37cb8-122">需要 Kerberos 驗證 (使用服務主要名稱 (SPN))。</span><span class="sxs-lookup"><span data-stu-id="37cb8-122">Kerberos authentication, using service principal names (SPNs), is required.</span></span> <span data-ttu-id="37cb8-123">如果 Kerberos 驗證失敗，ADAM 實例將不會複寫。</span><span class="sxs-lookup"><span data-stu-id="37cb8-123">If Kerberos authentication fails, the ADAM instances will not replicate.</span></span><br/>                |



 

<span data-ttu-id="37cb8-124">下表包含此屬性值的程式設計識別碼。</span><span class="sxs-lookup"><span data-stu-id="37cb8-124">The following table contains the programmatic identifiers for the values of this attribute.</span></span>

| <span data-ttu-id="37cb8-125">值</span><span class="sxs-lookup"><span data-stu-id="37cb8-125">Value</span></span>        | <span data-ttu-id="37cb8-126">從 Ntdsapi 的識別碼 () </span><span class="sxs-lookup"><span data-stu-id="37cb8-126">Identifier (from Ntdsapi.h)</span></span>                                               |
|--------------|---------------------------------------------------------------------------|
| <span data-ttu-id="37cb8-127">0</span><span class="sxs-lookup"><span data-stu-id="37cb8-127">0</span></span><br/> | <span data-ttu-id="37cb8-128">**ADAM \_ 複寫 \_ 驗證 \_ 模式 \_ 協商 \_ 傳遞 \_**</span><span class="sxs-lookup"><span data-stu-id="37cb8-128">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE\_PASS\_THROUGH**</span></span><br/> |
| <span data-ttu-id="37cb8-129">1</span><span class="sxs-lookup"><span data-stu-id="37cb8-129">1</span></span><br/> | <span data-ttu-id="37cb8-130">**ADAM \_ 複寫 \_ 驗證 \_ 模式的 \_ 協商**</span><span class="sxs-lookup"><span data-stu-id="37cb8-130">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE**</span></span><br/>                |
| <span data-ttu-id="37cb8-131">2</span><span class="sxs-lookup"><span data-stu-id="37cb8-131">2</span></span><br/> | <span data-ttu-id="37cb8-132">**需要 ADAM 複寫 \_ \_ 驗證 \_ 模式 \_ 相互 \_ 驗證 \_**</span><span class="sxs-lookup"><span data-stu-id="37cb8-132">**ADAM\_REPL\_AUTHENTICATION\_MODE\_MUTUAL\_AUTH\_REQUIRED**</span></span><br/>   |



 



| <span data-ttu-id="37cb8-133">進入</span><span class="sxs-lookup"><span data-stu-id="37cb8-133">Entry</span></span> | <span data-ttu-id="37cb8-134">值</span><span class="sxs-lookup"><span data-stu-id="37cb8-134">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="37cb8-135">CN</span><span class="sxs-lookup"><span data-stu-id="37cb8-135">CN</span></span>                | <span data-ttu-id="37cb8-136">ms-DS-複寫-驗證模式</span><span class="sxs-lookup"><span data-stu-id="37cb8-136">ms-DS-Repl-Authentication-Mode</span></span>       |
| <span data-ttu-id="37cb8-137">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="37cb8-137">Ldap-Display-Name</span></span> | <span data-ttu-id="37cb8-138">Msds-replauthenticationmode</span><span class="sxs-lookup"><span data-stu-id="37cb8-138">msDS-ReplAuthenticationMode</span></span>          |
| <span data-ttu-id="37cb8-139">大小</span><span class="sxs-lookup"><span data-stu-id="37cb8-139">Size</span></span>              | \-                                   |
| <span data-ttu-id="37cb8-140">更新許可權</span><span class="sxs-lookup"><span data-stu-id="37cb8-140">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="37cb8-141">更新頻率</span><span class="sxs-lookup"><span data-stu-id="37cb8-141">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="37cb8-142">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="37cb8-142">Attribute-Id</span></span>      | <span data-ttu-id="37cb8-143">1.2.840.113556.1.4.1861</span><span class="sxs-lookup"><span data-stu-id="37cb8-143">1.2.840.113556.1.4.1861</span></span>              |
| <span data-ttu-id="37cb8-144">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="37cb8-144">System-Id-Guid</span></span>    | <span data-ttu-id="37cb8-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span><span class="sxs-lookup"><span data-stu-id="37cb8-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span></span> |
| <span data-ttu-id="37cb8-146">Syntax</span><span class="sxs-lookup"><span data-stu-id="37cb8-146">Syntax</span></span>            | [<span data-ttu-id="37cb8-147">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="37cb8-147">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="37cb8-148">實作</span><span class="sxs-lookup"><span data-stu-id="37cb8-148">Implementations</span></span>

-   [<span data-ttu-id="37cb8-149">**亞當**</span><span class="sxs-lookup"><span data-stu-id="37cb8-149">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="37cb8-150">亞當</span><span class="sxs-lookup"><span data-stu-id="37cb8-150">ADAM</span></span>



| <span data-ttu-id="37cb8-151">進入</span><span class="sxs-lookup"><span data-stu-id="37cb8-151">Entry</span></span> | <span data-ttu-id="37cb8-152">值</span><span class="sxs-lookup"><span data-stu-id="37cb8-152">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="37cb8-153">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="37cb8-153">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="37cb8-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37cb8-154">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="37cb8-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="37cb8-155">System-Only</span></span>            | <span data-ttu-id="37cb8-156">否</span><span class="sxs-lookup"><span data-stu-id="37cb8-156">False</span></span>                                               |
| <span data-ttu-id="37cb8-157">是-單一值</span><span class="sxs-lookup"><span data-stu-id="37cb8-157">Is-Single-Valued</span></span>       | <span data-ttu-id="37cb8-158">對</span><span class="sxs-lookup"><span data-stu-id="37cb8-158">True</span></span>                                                |
| <span data-ttu-id="37cb8-159">已編制索引</span><span class="sxs-lookup"><span data-stu-id="37cb8-159">Is Indexed</span></span>             | <span data-ttu-id="37cb8-160">否</span><span class="sxs-lookup"><span data-stu-id="37cb8-160">False</span></span>                                               |
| <span data-ttu-id="37cb8-161">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="37cb8-161">In Global Catalog</span></span>      | <span data-ttu-id="37cb8-162">否</span><span class="sxs-lookup"><span data-stu-id="37cb8-162">False</span></span>                                               |
| <span data-ttu-id="37cb8-163">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="37cb8-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="37cb8-164">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="37cb8-164">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="37cb8-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37cb8-165">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="37cb8-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37cb8-166">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="37cb8-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37cb8-167">Search-Flags</span></span>           | <span data-ttu-id="37cb8-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="37cb8-168">0x00000000</span></span>                                          |
| <span data-ttu-id="37cb8-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37cb8-169">System-Flags</span></span>           | <span data-ttu-id="37cb8-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37cb8-170">0x00000010</span></span>                                          |
| <span data-ttu-id="37cb8-171">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="37cb8-171">Classes used in</span></span>        | [<span data-ttu-id="37cb8-172">**配置**</span><span class="sxs-lookup"><span data-stu-id="37cb8-172">**Configuration**</span></span>](c-configuration.md)<br/> |



 

 





