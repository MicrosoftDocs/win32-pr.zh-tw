---
title: ms-Authz-資源-條件屬性
description: 若為集中存取規則，這個屬性是識別套用原則之目標資源範圍的運算式。
ms.assetid: d3c1815e-3fa1-4106-82a1-74403f07fcde
ms.tgt_platform: multiple
keywords:
- ms/Authz-資源條件屬性 AD 架構
- msAuthz-ResourceCondition 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-Authz-Resource-Condition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3891e75763fd52d14d4ceaac560b33c824d06449
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108185"
---
# <a name="ms-authz-resource-condition-attribute"></a><span data-ttu-id="aedf6-105">ms-Authz-資源-條件屬性</span><span class="sxs-lookup"><span data-stu-id="aedf6-105">ms-Authz-Resource-Condition attribute</span></span>

<span data-ttu-id="aedf6-106">若為集中存取規則，這個屬性是識別套用原則之目標資源範圍的運算式。</span><span class="sxs-lookup"><span data-stu-id="aedf6-106">For a central access rule, this attribute is an expression that identifies the scope of the target resource to which the policy applies.</span></span>



| <span data-ttu-id="aedf6-107">進入</span><span class="sxs-lookup"><span data-stu-id="aedf6-107">Entry</span></span> | <span data-ttu-id="aedf6-108">值</span><span class="sxs-lookup"><span data-stu-id="aedf6-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="aedf6-109">CN</span><span class="sxs-lookup"><span data-stu-id="aedf6-109">CN</span></span>                | <span data-ttu-id="aedf6-110">ms-Authz-資源-條件</span><span class="sxs-lookup"><span data-stu-id="aedf6-110">ms-Authz-Resource-Condition</span></span>                 |
| <span data-ttu-id="aedf6-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="aedf6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="aedf6-112">msAuthz-ResourceCondition</span><span class="sxs-lookup"><span data-stu-id="aedf6-112">msAuthz-ResourceCondition</span></span>                   |
| <span data-ttu-id="aedf6-113">大小</span><span class="sxs-lookup"><span data-stu-id="aedf6-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="aedf6-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="aedf6-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="aedf6-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="aedf6-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="aedf6-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aedf6-116">Attribute-Id</span></span>      | <span data-ttu-id="aedf6-117">1.2.840.113556.1.4.2153</span><span class="sxs-lookup"><span data-stu-id="aedf6-117">1.2.840.113556.1.4.2153</span></span>                     |
| <span data-ttu-id="aedf6-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="aedf6-118">System-Id-Guid</span></span>    | <span data-ttu-id="aedf6-119">80997877-f874-4c68-864d-6e508a83bdbd</span><span class="sxs-lookup"><span data-stu-id="aedf6-119">80997877-f874-4c68-864d-6e508a83bdbd</span></span>        |
| <span data-ttu-id="aedf6-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="aedf6-120">Syntax</span></span>            | [<span data-ttu-id="aedf6-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="aedf6-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="aedf6-122">實作</span><span class="sxs-lookup"><span data-stu-id="aedf6-122">Implementations</span></span>

-   [<span data-ttu-id="aedf6-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aedf6-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="aedf6-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aedf6-124">Windows Server 2012</span></span>



| <span data-ttu-id="aedf6-125">進入</span><span class="sxs-lookup"><span data-stu-id="aedf6-125">Entry</span></span> | <span data-ttu-id="aedf6-126">值</span><span class="sxs-lookup"><span data-stu-id="aedf6-126">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="aedf6-127">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="aedf6-127">Link-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="aedf6-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aedf6-128">MAPI-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="aedf6-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="aedf6-129">System-Only</span></span>            | <span data-ttu-id="aedf6-130">否</span><span class="sxs-lookup"><span data-stu-id="aedf6-130">False</span></span>                                                                          |
| <span data-ttu-id="aedf6-131">是-單一值</span><span class="sxs-lookup"><span data-stu-id="aedf6-131">Is-Single-Valued</span></span>       | <span data-ttu-id="aedf6-132">對</span><span class="sxs-lookup"><span data-stu-id="aedf6-132">True</span></span>                                                                           |
| <span data-ttu-id="aedf6-133">已編制索引</span><span class="sxs-lookup"><span data-stu-id="aedf6-133">Is Indexed</span></span>             | <span data-ttu-id="aedf6-134">否</span><span class="sxs-lookup"><span data-stu-id="aedf6-134">False</span></span>                                                                          |
| <span data-ttu-id="aedf6-135">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="aedf6-135">In Global Catalog</span></span>      | <span data-ttu-id="aedf6-136">否</span><span class="sxs-lookup"><span data-stu-id="aedf6-136">False</span></span>                                                                          |
| <span data-ttu-id="aedf6-137">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="aedf6-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="aedf6-138">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="aedf6-138">O:BAG:BAD:S:</span></span>                                                                   |
| <span data-ttu-id="aedf6-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aedf6-139">Range-Lower</span></span>            | \-                                                                             |
| <span data-ttu-id="aedf6-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aedf6-140">Range-Upper</span></span>            | \-                                                                             |
| <span data-ttu-id="aedf6-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aedf6-141">Search-Flags</span></span>           | <span data-ttu-id="aedf6-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aedf6-142">0x00000000</span></span>                                                                     |
| <span data-ttu-id="aedf6-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aedf6-143">System-Flags</span></span>           | <span data-ttu-id="aedf6-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aedf6-144">0x00000010</span></span>                                                                     |
| <span data-ttu-id="aedf6-145">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="aedf6-145">Classes used in</span></span>        | [<span data-ttu-id="aedf6-146">**ms-Authz-存取-規則**</span><span class="sxs-lookup"><span data-stu-id="aedf6-146">**ms-Authz-Central-Access-Rule**</span></span>](c-msauthz-centralaccessrule.md)<br/> |



 

 





