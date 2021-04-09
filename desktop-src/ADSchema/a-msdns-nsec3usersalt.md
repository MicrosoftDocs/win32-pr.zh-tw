---
title: ms-DNS-NSEC3-使用者-Salt 屬性
description: 屬性，定義簽署 DNS 區域時要使用的使用者指定的 NSEC3 salt 字串。 如果是空的，則會使用隨機 salt。
ms.assetid: b9829732-8a79-4f07-8644-9fe4ba05ba8f
ms.tgt_platform: multiple
keywords:
- ms-DNS-NSEC3-使用者-Salt 屬性 AD 架構
- msDNS-NSEC3UserSalt 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DNS-NSEC3-User-Salt
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d28acb28dec95ef13afc37f9d7f26d713d5cf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687055"
---
# <a name="ms-dns-nsec3-user-salt-attribute"></a><span data-ttu-id="5003d-106">ms-DNS-NSEC3-使用者-Salt 屬性</span><span class="sxs-lookup"><span data-stu-id="5003d-106">ms-DNS-NSEC3-User-Salt attribute</span></span>

<span data-ttu-id="5003d-107">屬性，定義簽署 DNS 區域時要使用的使用者指定的 NSEC3 salt 字串。</span><span class="sxs-lookup"><span data-stu-id="5003d-107">An attribute that defines a user-specified NSEC3 salt string to use when signing the DNS zone.</span></span> <span data-ttu-id="5003d-108">如果是空的，則會使用隨機 salt。</span><span class="sxs-lookup"><span data-stu-id="5003d-108">If empty, random salt will be used.</span></span>



| <span data-ttu-id="5003d-109">進入</span><span class="sxs-lookup"><span data-stu-id="5003d-109">Entry</span></span> | <span data-ttu-id="5003d-110">值</span><span class="sxs-lookup"><span data-stu-id="5003d-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5003d-111">CN</span><span class="sxs-lookup"><span data-stu-id="5003d-111">CN</span></span>                | <span data-ttu-id="5003d-112">ms-DNS-NSEC3-使用者-Salt</span><span class="sxs-lookup"><span data-stu-id="5003d-112">ms-DNS-NSEC3-User-Salt</span></span>                      |
| <span data-ttu-id="5003d-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="5003d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5003d-114">msDNS-NSEC3UserSalt</span><span class="sxs-lookup"><span data-stu-id="5003d-114">msDNS-NSEC3UserSalt</span></span>                         |
| <span data-ttu-id="5003d-115">大小</span><span class="sxs-lookup"><span data-stu-id="5003d-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="5003d-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="5003d-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="5003d-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="5003d-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5003d-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5003d-118">Attribute-Id</span></span>      | <span data-ttu-id="5003d-119">1.2.840.113556.1.4.2148</span><span class="sxs-lookup"><span data-stu-id="5003d-119">1.2.840.113556.1.4.2148</span></span>                     |
| <span data-ttu-id="5003d-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="5003d-120">System-Id-Guid</span></span>    | <span data-ttu-id="5003d-121">aff16770-9622-4fbc-a128-3088777605b9</span><span class="sxs-lookup"><span data-stu-id="5003d-121">aff16770-9622-4fbc-a128-3088777605b9</span></span>        |
| <span data-ttu-id="5003d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5003d-122">Syntax</span></span>            | [<span data-ttu-id="5003d-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5003d-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5003d-124">實作</span><span class="sxs-lookup"><span data-stu-id="5003d-124">Implementations</span></span>

-   [<span data-ttu-id="5003d-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5003d-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="5003d-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5003d-126">Windows Server 2012</span></span>



| <span data-ttu-id="5003d-127">進入</span><span class="sxs-lookup"><span data-stu-id="5003d-127">Entry</span></span> | <span data-ttu-id="5003d-128">值</span><span class="sxs-lookup"><span data-stu-id="5003d-128">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="5003d-129">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5003d-129">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="5003d-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5003d-130">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="5003d-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="5003d-131">System-Only</span></span>            | <span data-ttu-id="5003d-132">否</span><span class="sxs-lookup"><span data-stu-id="5003d-132">False</span></span>                                    |
| <span data-ttu-id="5003d-133">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5003d-133">Is-Single-Valued</span></span>       | <span data-ttu-id="5003d-134">對</span><span class="sxs-lookup"><span data-stu-id="5003d-134">True</span></span>                                     |
| <span data-ttu-id="5003d-135">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5003d-135">Is Indexed</span></span>             | <span data-ttu-id="5003d-136">否</span><span class="sxs-lookup"><span data-stu-id="5003d-136">False</span></span>                                    |
| <span data-ttu-id="5003d-137">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5003d-137">In Global Catalog</span></span>      | <span data-ttu-id="5003d-138">否</span><span class="sxs-lookup"><span data-stu-id="5003d-138">False</span></span>                                    |
| <span data-ttu-id="5003d-139">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5003d-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="5003d-140">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5003d-140">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="5003d-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5003d-141">Range-Lower</span></span>            | <span data-ttu-id="5003d-142">0</span><span class="sxs-lookup"><span data-stu-id="5003d-142">0</span></span>                                        |
| <span data-ttu-id="5003d-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5003d-143">Range-Upper</span></span>            | <span data-ttu-id="5003d-144">510</span><span class="sxs-lookup"><span data-stu-id="5003d-144">510</span></span>                                      |
| <span data-ttu-id="5003d-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5003d-145">Search-Flags</span></span>           | <span data-ttu-id="5003d-146">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5003d-146">0x00000008</span></span>                               |
| <span data-ttu-id="5003d-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5003d-147">System-Flags</span></span>           | <span data-ttu-id="5003d-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5003d-148">0x00000010</span></span>                               |
| <span data-ttu-id="5003d-149">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5003d-149">Classes used in</span></span>        | [<span data-ttu-id="5003d-150">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="5003d-150">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





