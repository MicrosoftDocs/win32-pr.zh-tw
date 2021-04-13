---
title: ms-DS-輸入-宣告-轉換-原則屬性
description: 這是輸入宣告的宣告轉換原則物件的連結， (宣告從受信任的網域輸入此樹系) 。
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- ms DS-輸入-宣告-轉換-原則屬性 AD 架構
- IngressClaimsTransformationPolicy 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50e3c187a4cb3b2a465257b408a1f5603c756ba
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509625"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a><span data-ttu-id="e5447-105">ms-DS-輸入-宣告-轉換-原則屬性</span><span class="sxs-lookup"><span data-stu-id="e5447-105">ms-DS-Ingress-Claims-Transformation-Policy attribute</span></span>

<span data-ttu-id="e5447-106">這是輸入宣告的宣告轉換原則物件的連結， (宣告從受信任的網域輸入此樹系) 。</span><span class="sxs-lookup"><span data-stu-id="e5447-106">This is a link to a Claims Transformation Policy Object for the ingress claims (claims entering this forest) from the Trusted Domain.</span></span> <span data-ttu-id="e5447-107">這僅適用于傳出或雙向跨樹系信任。</span><span class="sxs-lookup"><span data-stu-id="e5447-107">This is applicable only for an outgoing or bidirectional Cross-Forest Trust.</span></span> <span data-ttu-id="e5447-108">如果不存在此連結，則會捨棄所有輸入宣告。</span><span class="sxs-lookup"><span data-stu-id="e5447-108">If this link is absent, all the ingress claims are dropped.</span></span>



| <span data-ttu-id="e5447-109">進入</span><span class="sxs-lookup"><span data-stu-id="e5447-109">Entry</span></span> | <span data-ttu-id="e5447-110">值</span><span class="sxs-lookup"><span data-stu-id="e5447-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="e5447-111">CN</span><span class="sxs-lookup"><span data-stu-id="e5447-111">CN</span></span>                | <span data-ttu-id="e5447-112">ms-DS-輸入-宣告-轉換-原則</span><span class="sxs-lookup"><span data-stu-id="e5447-112">ms-DS-Ingress-Claims-Transformation-Policy</span></span> |
| <span data-ttu-id="e5447-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e5447-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e5447-114">IngressClaimsTransformationPolicy</span><span class="sxs-lookup"><span data-stu-id="e5447-114">msDS-IngressClaimsTransformationPolicy</span></span>     |
| <span data-ttu-id="e5447-115">大小</span><span class="sxs-lookup"><span data-stu-id="e5447-115">Size</span></span>              | \-                                         |
| <span data-ttu-id="e5447-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e5447-116">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="e5447-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e5447-117">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="e5447-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e5447-118">Attribute-Id</span></span>      | <span data-ttu-id="e5447-119">1.2.840.113556.1.4.2191</span><span class="sxs-lookup"><span data-stu-id="e5447-119">1.2.840.113556.1.4.2191</span></span>                    |
| <span data-ttu-id="e5447-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e5447-120">System-Id-Guid</span></span>    | <span data-ttu-id="e5447-121">86284c08-0c6e-1540-8b15-75147d23d20d</span><span class="sxs-lookup"><span data-stu-id="e5447-121">86284c08-0c6e-1540-8b15-75147d23d20d</span></span>       |
| <span data-ttu-id="e5447-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5447-122">Syntax</span></span>            | [<span data-ttu-id="e5447-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="e5447-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)    |



## <a name="implementations"></a><span data-ttu-id="e5447-124">實作</span><span class="sxs-lookup"><span data-stu-id="e5447-124">Implementations</span></span>

-   [<span data-ttu-id="e5447-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e5447-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="e5447-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5447-126">Windows Server 2012</span></span>



| <span data-ttu-id="e5447-127">進入</span><span class="sxs-lookup"><span data-stu-id="e5447-127">Entry</span></span> | <span data-ttu-id="e5447-128">值</span><span class="sxs-lookup"><span data-stu-id="e5447-128">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e5447-129">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e5447-129">Link-Id</span></span>                | <span data-ttu-id="e5447-130">2190</span><span class="sxs-lookup"><span data-stu-id="e5447-130">2190</span></span>                                                 |
| <span data-ttu-id="e5447-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5447-131">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5447-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5447-132">System-Only</span></span>            | <span data-ttu-id="e5447-133">否</span><span class="sxs-lookup"><span data-stu-id="e5447-133">False</span></span>                                                |
| <span data-ttu-id="e5447-134">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e5447-134">Is-Single-Valued</span></span>       | <span data-ttu-id="e5447-135">對</span><span class="sxs-lookup"><span data-stu-id="e5447-135">True</span></span>                                                 |
| <span data-ttu-id="e5447-136">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e5447-136">Is Indexed</span></span>             | <span data-ttu-id="e5447-137">否</span><span class="sxs-lookup"><span data-stu-id="e5447-137">False</span></span>                                                |
| <span data-ttu-id="e5447-138">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e5447-138">In Global Catalog</span></span>      | <span data-ttu-id="e5447-139">否</span><span class="sxs-lookup"><span data-stu-id="e5447-139">False</span></span>                                                |
| <span data-ttu-id="e5447-140">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e5447-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5447-141">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e5447-141">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e5447-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5447-142">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e5447-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5447-143">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e5447-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5447-144">Search-Flags</span></span>           | <span data-ttu-id="e5447-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5447-145">0x00000000</span></span>                                           |
| <span data-ttu-id="e5447-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5447-146">System-Flags</span></span>           | <span data-ttu-id="e5447-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5447-147">0x00000010</span></span>                                           |
| <span data-ttu-id="e5447-148">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e5447-148">Classes used in</span></span>        | [<span data-ttu-id="e5447-149">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="e5447-149">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





