---
title: ms-Authz------------ID 屬性
description: 若為集中存取原則，這個屬性會定義可用來識別套用至資源之原則集的 GUID。
ms.assetid: db1fe49b-f737-4202-bd6f-7bab64187c82
ms.tgt_platform: multiple
keywords:
- ms-Authz------------ID 屬性 AD 架構
- msAuthz-CentralAccessPolicyID 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-Authz-Central-Access-Policy-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bda6a6d8b28ac43f984034c63a259e74d49712e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108189"
---
# <a name="ms-authz-central-access-policy-id-attribute"></a><span data-ttu-id="2c66a-105">ms-Authz------------ID 屬性</span><span class="sxs-lookup"><span data-stu-id="2c66a-105">ms-Authz-Central-Access-Policy-ID attribute</span></span>

<span data-ttu-id="2c66a-106">若為集中存取原則，這個屬性會定義可用來識別套用至資源之原則集的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2c66a-106">For a Central Access Policy, this attribute defines a GUID that can be used to identify the set of policies when applied to a resource.</span></span>



| <span data-ttu-id="2c66a-107">進入</span><span class="sxs-lookup"><span data-stu-id="2c66a-107">Entry</span></span> | <span data-ttu-id="2c66a-108">值</span><span class="sxs-lookup"><span data-stu-id="2c66a-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2c66a-109">CN</span><span class="sxs-lookup"><span data-stu-id="2c66a-109">CN</span></span>                | <span data-ttu-id="2c66a-110">ms-Authz-存取原則-識別碼</span><span class="sxs-lookup"><span data-stu-id="2c66a-110">ms-Authz-Central-Access-Policy-ID</span></span>    |
| <span data-ttu-id="2c66a-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2c66a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2c66a-112">msAuthz-CentralAccessPolicyID</span><span class="sxs-lookup"><span data-stu-id="2c66a-112">msAuthz-CentralAccessPolicyID</span></span>        |
| <span data-ttu-id="2c66a-113">大小</span><span class="sxs-lookup"><span data-stu-id="2c66a-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="2c66a-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2c66a-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2c66a-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2c66a-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2c66a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2c66a-116">Attribute-Id</span></span>      | <span data-ttu-id="2c66a-117">1.2.840.113556.1.4.2154</span><span class="sxs-lookup"><span data-stu-id="2c66a-117">1.2.840.113556.1.4.2154</span></span>              |
| <span data-ttu-id="2c66a-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2c66a-118">System-Id-Guid</span></span>    | <span data-ttu-id="2c66a-119">62f29b60-be74-4630-9456-2f6691993a86</span><span class="sxs-lookup"><span data-stu-id="2c66a-119">62f29b60-be74-4630-9456-2f6691993a86</span></span> |
| <span data-ttu-id="2c66a-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c66a-120">Syntax</span></span>            | [<span data-ttu-id="2c66a-121">**(Sid) 的字串**</span><span class="sxs-lookup"><span data-stu-id="2c66a-121">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="2c66a-122">實作</span><span class="sxs-lookup"><span data-stu-id="2c66a-122">Implementations</span></span>

-   [<span data-ttu-id="2c66a-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2c66a-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="2c66a-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c66a-124">Windows Server 2012</span></span>



| <span data-ttu-id="2c66a-125">進入</span><span class="sxs-lookup"><span data-stu-id="2c66a-125">Entry</span></span> | <span data-ttu-id="2c66a-126">值</span><span class="sxs-lookup"><span data-stu-id="2c66a-126">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c66a-127">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2c66a-127">Link-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="2c66a-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c66a-128">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="2c66a-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c66a-129">System-Only</span></span>            | <span data-ttu-id="2c66a-130">否</span><span class="sxs-lookup"><span data-stu-id="2c66a-130">False</span></span>                                                                              |
| <span data-ttu-id="2c66a-131">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2c66a-131">Is-Single-Valued</span></span>       | <span data-ttu-id="2c66a-132">對</span><span class="sxs-lookup"><span data-stu-id="2c66a-132">True</span></span>                                                                               |
| <span data-ttu-id="2c66a-133">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2c66a-133">Is Indexed</span></span>             | <span data-ttu-id="2c66a-134">否</span><span class="sxs-lookup"><span data-stu-id="2c66a-134">False</span></span>                                                                              |
| <span data-ttu-id="2c66a-135">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2c66a-135">In Global Catalog</span></span>      | <span data-ttu-id="2c66a-136">否</span><span class="sxs-lookup"><span data-stu-id="2c66a-136">False</span></span>                                                                              |
| <span data-ttu-id="2c66a-137">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2c66a-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c66a-138">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2c66a-138">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="2c66a-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c66a-139">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="2c66a-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c66a-140">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="2c66a-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c66a-141">Search-Flags</span></span>           | <span data-ttu-id="2c66a-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c66a-142">0x00000000</span></span>                                                                         |
| <span data-ttu-id="2c66a-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c66a-143">System-Flags</span></span>           | <span data-ttu-id="2c66a-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c66a-144">0x00000010</span></span>                                                                         |
| <span data-ttu-id="2c66a-145">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2c66a-145">Classes used in</span></span>        | [<span data-ttu-id="2c66a-146">**ms-Authz-存取-原則**</span><span class="sxs-lookup"><span data-stu-id="2c66a-146">**ms-Authz-Central-Access-Policy**</span></span>](c-msauthz-centralaccesspolicy.md)<br/> |



 

 





