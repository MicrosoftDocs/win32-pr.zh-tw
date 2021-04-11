---
title: ms DS-允許對等身分的其他身分識別屬性
description: 這個屬性是用來進行存取檢查，以判斷要求者是否有許可權可以代表其他身分識別，來執行以此帳戶身分執行的服務。
ms.assetid: 38203665-4505-461b-b6ab-b634725ac2fa
ms.tgt_platform: multiple
keywords:
- ms DS-允許對等身分的其他身分識別屬性 AD 架構
- '>msds-allowedtoactonbehalfofotheridentity 屬性 AD 架構'
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dacd532b1d8a55b3656dc1d65fc1ebd940476c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845507"
---
# <a name="ms-ds-allowed-to-act-on-behalf-of-other-identity-attribute"></a><span data-ttu-id="216b3-105">ms DS-允許對等身分的其他身分識別屬性</span><span class="sxs-lookup"><span data-stu-id="216b3-105">ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity attribute</span></span>

<span data-ttu-id="216b3-106">這個屬性是用來進行存取檢查，以判斷要求者是否有許可權可以代表其他身分識別，來執行以此帳戶身分執行的服務。</span><span class="sxs-lookup"><span data-stu-id="216b3-106">This attribute is used for access checks to determine if a requestor has permission to act on the behalf of other identities to services running as this account.</span></span>



| <span data-ttu-id="216b3-107">進入</span><span class="sxs-lookup"><span data-stu-id="216b3-107">Entry</span></span> | <span data-ttu-id="216b3-108">值</span><span class="sxs-lookup"><span data-stu-id="216b3-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="216b3-109">CN</span><span class="sxs-lookup"><span data-stu-id="216b3-109">CN</span></span>                | <span data-ttu-id="216b3-110">以 ms DS 允許的身分識別，其他身分識別</span><span class="sxs-lookup"><span data-stu-id="216b3-110">ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity</span></span>    |
| <span data-ttu-id="216b3-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="216b3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="216b3-112">>msds-allowedtoactonbehalfofotheridentity</span><span class="sxs-lookup"><span data-stu-id="216b3-112">msDS-AllowedToActOnBehalfOfOtherIdentity</span></span>            |
| <span data-ttu-id="216b3-113">大小</span><span class="sxs-lookup"><span data-stu-id="216b3-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="216b3-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="216b3-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="216b3-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="216b3-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="216b3-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="216b3-116">Attribute-Id</span></span>      | <span data-ttu-id="216b3-117">1.2.840.113556.1.4.2182</span><span class="sxs-lookup"><span data-stu-id="216b3-117">1.2.840.113556.1.4.2182</span></span>                             |
| <span data-ttu-id="216b3-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="216b3-118">System-Id-Guid</span></span>    | <span data-ttu-id="216b3-119">3f78c3e5-f79a-46bd-a0b8-9d18116ddc79</span><span class="sxs-lookup"><span data-stu-id="216b3-119">3f78c3e5-f79a-46bd-a0b8-9d18116ddc79</span></span>                |
| <span data-ttu-id="216b3-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="216b3-120">Syntax</span></span>            | [<span data-ttu-id="216b3-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="216b3-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="216b3-122">實作</span><span class="sxs-lookup"><span data-stu-id="216b3-122">Implementations</span></span>

-   [<span data-ttu-id="216b3-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="216b3-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="216b3-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="216b3-124">Windows Server 2012</span></span>



| <span data-ttu-id="216b3-125">進入</span><span class="sxs-lookup"><span data-stu-id="216b3-125">Entry</span></span> | <span data-ttu-id="216b3-126">值</span><span class="sxs-lookup"><span data-stu-id="216b3-126">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="216b3-127">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="216b3-127">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="216b3-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="216b3-128">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="216b3-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="216b3-129">System-Only</span></span>            | <span data-ttu-id="216b3-130">對</span><span class="sxs-lookup"><span data-stu-id="216b3-130">True</span></span>                                                               |
| <span data-ttu-id="216b3-131">是-單一值</span><span class="sxs-lookup"><span data-stu-id="216b3-131">Is-Single-Valued</span></span>       | <span data-ttu-id="216b3-132">對</span><span class="sxs-lookup"><span data-stu-id="216b3-132">True</span></span>                                                               |
| <span data-ttu-id="216b3-133">已編制索引</span><span class="sxs-lookup"><span data-stu-id="216b3-133">Is Indexed</span></span>             | <span data-ttu-id="216b3-134">否</span><span class="sxs-lookup"><span data-stu-id="216b3-134">False</span></span>                                                              |
| <span data-ttu-id="216b3-135">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="216b3-135">In Global Catalog</span></span>      | <span data-ttu-id="216b3-136">否</span><span class="sxs-lookup"><span data-stu-id="216b3-136">False</span></span>                                                              |
| <span data-ttu-id="216b3-137">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="216b3-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="216b3-138">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="216b3-138">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="216b3-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="216b3-139">Range-Lower</span></span>            | <span data-ttu-id="216b3-140">0</span><span class="sxs-lookup"><span data-stu-id="216b3-140">0</span></span>                                                                  |
| <span data-ttu-id="216b3-141">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="216b3-141">Range-Upper</span></span>            | <span data-ttu-id="216b3-142">132096</span><span class="sxs-lookup"><span data-stu-id="216b3-142">132096</span></span>                                                             |
| <span data-ttu-id="216b3-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="216b3-143">Search-Flags</span></span>           | <span data-ttu-id="216b3-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="216b3-144">0x00000000</span></span>                                                         |
| <span data-ttu-id="216b3-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="216b3-145">System-Flags</span></span>           | <span data-ttu-id="216b3-146">0x00000010</span><span class="sxs-lookup"><span data-stu-id="216b3-146">0x00000010</span></span>                                                         |
| <span data-ttu-id="216b3-147">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="216b3-147">Classes used in</span></span>        | [<span data-ttu-id="216b3-148">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="216b3-148">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





