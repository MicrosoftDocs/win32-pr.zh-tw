---
title: RFC5011-索引鍵變換屬性
description: 屬性，定義是否應使用 RFC 5011 中定義的金鑰變換程式來維護 DNS 區域。
ms.assetid: 49ad29bb-63ea-4c69-9782-65c94d60569d
ms.tgt_platform: multiple
keywords:
- RFC5011-金鑰變換的屬性 AD 架構
- msDNS-RFC5011KeyRollovers 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DNS-RFC5011-Key-Rollovers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f07300f1fe0696e3f53b5db9380126f280dd1fb3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509712"
---
# <a name="ms-dns-rfc5011-key-rollovers-attribute"></a><span data-ttu-id="47a2f-105">RFC5011-索引鍵變換屬性</span><span class="sxs-lookup"><span data-stu-id="47a2f-105">ms-DNS-RFC5011-Key-Rollovers attribute</span></span>

<span data-ttu-id="47a2f-106">屬性，定義是否應使用 RFC 5011 中定義的金鑰變換程式來維護 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="47a2f-106">An attribute that defines whether or not the DNS zone should be maintained using key rollover procedures defined in RFC 5011.</span></span>



| <span data-ttu-id="47a2f-107">進入</span><span class="sxs-lookup"><span data-stu-id="47a2f-107">Entry</span></span> | <span data-ttu-id="47a2f-108">值</span><span class="sxs-lookup"><span data-stu-id="47a2f-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="47a2f-109">CN</span><span class="sxs-lookup"><span data-stu-id="47a2f-109">CN</span></span>                | <span data-ttu-id="47a2f-110">RFC5011-金鑰變換</span><span class="sxs-lookup"><span data-stu-id="47a2f-110">ms-DNS-RFC5011-Key-Rollovers</span></span>         |
| <span data-ttu-id="47a2f-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="47a2f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="47a2f-112">msDNS-RFC5011KeyRollovers</span><span class="sxs-lookup"><span data-stu-id="47a2f-112">msDNS-RFC5011KeyRollovers</span></span>            |
| <span data-ttu-id="47a2f-113">大小</span><span class="sxs-lookup"><span data-stu-id="47a2f-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="47a2f-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="47a2f-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="47a2f-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="47a2f-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="47a2f-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="47a2f-116">Attribute-Id</span></span>      | <span data-ttu-id="47a2f-117">1.2.840.113556.1.4.2135</span><span class="sxs-lookup"><span data-stu-id="47a2f-117">1.2.840.113556.1.4.2135</span></span>              |
| <span data-ttu-id="47a2f-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="47a2f-118">System-Id-Guid</span></span>    | <span data-ttu-id="47a2f-119">27d93c40-065a-43c0-bdd8-cdf2c7d120aa</span><span class="sxs-lookup"><span data-stu-id="47a2f-119">27d93c40-065a-43c0-bdd8-cdf2c7d120aa</span></span> |
| <span data-ttu-id="47a2f-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="47a2f-120">Syntax</span></span>            | [<span data-ttu-id="47a2f-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="47a2f-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="47a2f-122">實作</span><span class="sxs-lookup"><span data-stu-id="47a2f-122">Implementations</span></span>

-   [<span data-ttu-id="47a2f-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="47a2f-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="47a2f-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="47a2f-124">Windows Server 2012</span></span>



| <span data-ttu-id="47a2f-125">進入</span><span class="sxs-lookup"><span data-stu-id="47a2f-125">Entry</span></span> | <span data-ttu-id="47a2f-126">值</span><span class="sxs-lookup"><span data-stu-id="47a2f-126">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="47a2f-127">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="47a2f-127">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="47a2f-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="47a2f-128">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="47a2f-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="47a2f-129">System-Only</span></span>            | <span data-ttu-id="47a2f-130">否</span><span class="sxs-lookup"><span data-stu-id="47a2f-130">False</span></span>                                    |
| <span data-ttu-id="47a2f-131">是-單一值</span><span class="sxs-lookup"><span data-stu-id="47a2f-131">Is-Single-Valued</span></span>       | <span data-ttu-id="47a2f-132">對</span><span class="sxs-lookup"><span data-stu-id="47a2f-132">True</span></span>                                     |
| <span data-ttu-id="47a2f-133">已編制索引</span><span class="sxs-lookup"><span data-stu-id="47a2f-133">Is Indexed</span></span>             | <span data-ttu-id="47a2f-134">否</span><span class="sxs-lookup"><span data-stu-id="47a2f-134">False</span></span>                                    |
| <span data-ttu-id="47a2f-135">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="47a2f-135">In Global Catalog</span></span>      | <span data-ttu-id="47a2f-136">否</span><span class="sxs-lookup"><span data-stu-id="47a2f-136">False</span></span>                                    |
| <span data-ttu-id="47a2f-137">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="47a2f-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="47a2f-138">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="47a2f-138">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="47a2f-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="47a2f-139">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="47a2f-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="47a2f-140">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="47a2f-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="47a2f-141">Search-Flags</span></span>           | <span data-ttu-id="47a2f-142">0x00000008</span><span class="sxs-lookup"><span data-stu-id="47a2f-142">0x00000008</span></span>                               |
| <span data-ttu-id="47a2f-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="47a2f-143">System-Flags</span></span>           | <span data-ttu-id="47a2f-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="47a2f-144">0x00000010</span></span>                               |
| <span data-ttu-id="47a2f-145">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="47a2f-145">Classes used in</span></span>        | [<span data-ttu-id="47a2f-146">**Dns-區域**</span><span class="sxs-lookup"><span data-stu-id="47a2f-146">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





