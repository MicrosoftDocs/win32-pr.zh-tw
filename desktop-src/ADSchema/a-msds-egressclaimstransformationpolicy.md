---
title: ms DS-輸出-宣告-轉換-原則屬性
description: 這是輸出宣告的宣告轉換原則物件連結， (宣告將此樹系) 至受信任的網域。
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- ms DS-輸出-宣告-轉換-原則屬性 AD 架構
- EgressClaimsTransformationPolicy 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3978944b6ae85fcc5fd33682abec7dd3fff0057
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935424"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a><span data-ttu-id="4571b-105">ms DS-輸出-宣告-轉換-原則屬性</span><span class="sxs-lookup"><span data-stu-id="4571b-105">ms-DS-Egress-Claims-Transformation-Policy attribute</span></span>

<span data-ttu-id="4571b-106">這是輸出宣告的宣告轉換原則物件連結， (宣告將此樹系) 至受信任的網域。</span><span class="sxs-lookup"><span data-stu-id="4571b-106">This is a link to a Claims Transformation Policy Object for the egress claims (claims leaving this forest) to the Trusted Domain.</span></span> <span data-ttu-id="4571b-107">這僅適用于傳入或雙向跨樹系信任。</span><span class="sxs-lookup"><span data-stu-id="4571b-107">This is applicable only for an incoming or bidirectional Cross-Forest Trust.</span></span> <span data-ttu-id="4571b-108">當此連結不存在時，所有宣告都可依現狀允許輸出。</span><span class="sxs-lookup"><span data-stu-id="4571b-108">When this link is not present, all claims are allowed to egress as-is.</span></span>



| <span data-ttu-id="4571b-109">進入</span><span class="sxs-lookup"><span data-stu-id="4571b-109">Entry</span></span> | <span data-ttu-id="4571b-110">值</span><span class="sxs-lookup"><span data-stu-id="4571b-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="4571b-111">CN</span><span class="sxs-lookup"><span data-stu-id="4571b-111">CN</span></span>                | <span data-ttu-id="4571b-112">ms DS-輸出-宣告-轉換-原則</span><span class="sxs-lookup"><span data-stu-id="4571b-112">ms-DS-Egress-Claims-Transformation-Policy</span></span> |
| <span data-ttu-id="4571b-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4571b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4571b-114">EgressClaimsTransformationPolicy</span><span class="sxs-lookup"><span data-stu-id="4571b-114">msDS-EgressClaimsTransformationPolicy</span></span>     |
| <span data-ttu-id="4571b-115">大小</span><span class="sxs-lookup"><span data-stu-id="4571b-115">Size</span></span>              | \-                                        |
| <span data-ttu-id="4571b-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4571b-116">Update Privilege</span></span>  | \-                                        |
| <span data-ttu-id="4571b-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4571b-117">Update Frequency</span></span>  | \-                                        |
| <span data-ttu-id="4571b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4571b-118">Attribute-Id</span></span>      | <span data-ttu-id="4571b-119">1.2.840.113556.1.4.2192</span><span class="sxs-lookup"><span data-stu-id="4571b-119">1.2.840.113556.1.4.2192</span></span>                   |
| <span data-ttu-id="4571b-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4571b-120">System-Id-Guid</span></span>    | <span data-ttu-id="4571b-121">c137427e-9a73-b040-9190-1b095bb43288</span><span class="sxs-lookup"><span data-stu-id="4571b-121">c137427e-9a73-b040-9190-1b095bb43288</span></span>      |
| <span data-ttu-id="4571b-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4571b-122">Syntax</span></span>            | [<span data-ttu-id="4571b-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="4571b-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)   |



## <a name="implementations"></a><span data-ttu-id="4571b-124">實作</span><span class="sxs-lookup"><span data-stu-id="4571b-124">Implementations</span></span>

-   [<span data-ttu-id="4571b-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4571b-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="4571b-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4571b-126">Windows Server 2012</span></span>



| <span data-ttu-id="4571b-127">進入</span><span class="sxs-lookup"><span data-stu-id="4571b-127">Entry</span></span> | <span data-ttu-id="4571b-128">值</span><span class="sxs-lookup"><span data-stu-id="4571b-128">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4571b-129">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4571b-129">Link-Id</span></span>                | <span data-ttu-id="4571b-130">2192</span><span class="sxs-lookup"><span data-stu-id="4571b-130">2192</span></span>                                                 |
| <span data-ttu-id="4571b-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4571b-131">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4571b-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="4571b-132">System-Only</span></span>            | <span data-ttu-id="4571b-133">否</span><span class="sxs-lookup"><span data-stu-id="4571b-133">False</span></span>                                                |
| <span data-ttu-id="4571b-134">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4571b-134">Is-Single-Valued</span></span>       | <span data-ttu-id="4571b-135">對</span><span class="sxs-lookup"><span data-stu-id="4571b-135">True</span></span>                                                 |
| <span data-ttu-id="4571b-136">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4571b-136">Is Indexed</span></span>             | <span data-ttu-id="4571b-137">否</span><span class="sxs-lookup"><span data-stu-id="4571b-137">False</span></span>                                                |
| <span data-ttu-id="4571b-138">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4571b-138">In Global Catalog</span></span>      | <span data-ttu-id="4571b-139">否</span><span class="sxs-lookup"><span data-stu-id="4571b-139">False</span></span>                                                |
| <span data-ttu-id="4571b-140">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4571b-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="4571b-141">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4571b-141">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4571b-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4571b-142">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="4571b-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4571b-143">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="4571b-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4571b-144">Search-Flags</span></span>           | <span data-ttu-id="4571b-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4571b-145">0x00000000</span></span>                                           |
| <span data-ttu-id="4571b-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4571b-146">System-Flags</span></span>           | <span data-ttu-id="4571b-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4571b-147">0x00000010</span></span>                                           |
| <span data-ttu-id="4571b-148">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4571b-148">Classes used in</span></span>        | [<span data-ttu-id="4571b-149">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="4571b-149">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





