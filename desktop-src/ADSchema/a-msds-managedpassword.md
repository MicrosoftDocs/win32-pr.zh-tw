---
title: ManagedPassword 屬性
description: 此結構化屬性會傳回 blob，其中包含群組 MSA 的純文字先前和目前的密碼、TimeUntilEpochExpires 和 TimeUntilNextScheduledUpdate。
ms.assetid: bcabb20f-46f3-4c15-b71b-a8dfc43678bc
ms.tgt_platform: multiple
keywords:
- ManagedPassword 屬性 AD 架構
- ManagedPassword 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-ManagedPassword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a440f1849e01ae4930b72441f75b17ce51a0566b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107813"
---
# <a name="ms-ds-managedpassword-attribute"></a><span data-ttu-id="6b090-105">ManagedPassword 屬性</span><span class="sxs-lookup"><span data-stu-id="6b090-105">ms-DS-ManagedPassword attribute</span></span>

<span data-ttu-id="6b090-106">此結構化屬性會傳回 blob，其中包含群組 MSA 的純文字先前和目前的密碼、TimeUntilEpochExpires 和 TimeUntilNextScheduledUpdate。</span><span class="sxs-lookup"><span data-stu-id="6b090-106">This constructed attribute returns a blob that contains the clear-text previous and current password, TimeUntilEpochExpires, and TimeUntilNextScheduledUpdate for a group MSA.</span></span>



| <span data-ttu-id="6b090-107">進入</span><span class="sxs-lookup"><span data-stu-id="6b090-107">Entry</span></span> | <span data-ttu-id="6b090-108">值</span><span class="sxs-lookup"><span data-stu-id="6b090-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="6b090-109">CN</span><span class="sxs-lookup"><span data-stu-id="6b090-109">CN</span></span>                | <span data-ttu-id="6b090-110">ManagedPassword</span><span class="sxs-lookup"><span data-stu-id="6b090-110">ms-DS-ManagedPassword</span></span>                                 |
| <span data-ttu-id="6b090-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6b090-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6b090-112">ManagedPassword</span><span class="sxs-lookup"><span data-stu-id="6b090-112">msDS-ManagedPassword</span></span>                                  |
| <span data-ttu-id="6b090-113">大小</span><span class="sxs-lookup"><span data-stu-id="6b090-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="6b090-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6b090-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="6b090-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6b090-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="6b090-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6b090-116">Attribute-Id</span></span>      | <span data-ttu-id="6b090-117">1.2.840.113556.1.4.2196</span><span class="sxs-lookup"><span data-stu-id="6b090-117">1.2.840.113556.1.4.2196</span></span>                               |
| <span data-ttu-id="6b090-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6b090-118">System-Id-Guid</span></span>    | <span data-ttu-id="6b090-119">e362ed86-b728-0842-b27d-2dea7a9df218</span><span class="sxs-lookup"><span data-stu-id="6b090-119">e362ed86-b728-0842-b27d-2dea7a9df218</span></span>                  |
| <span data-ttu-id="6b090-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b090-120">Syntax</span></span>            | [<span data-ttu-id="6b090-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="6b090-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="6b090-122">實作</span><span class="sxs-lookup"><span data-stu-id="6b090-122">Implementations</span></span>

-   [<span data-ttu-id="6b090-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6b090-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="6b090-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6b090-124">Windows Server 2012</span></span>



| <span data-ttu-id="6b090-125">進入</span><span class="sxs-lookup"><span data-stu-id="6b090-125">Entry</span></span> | <span data-ttu-id="6b090-126">值</span><span class="sxs-lookup"><span data-stu-id="6b090-126">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b090-127">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6b090-127">Link-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="6b090-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6b090-128">MAPI-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="6b090-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="6b090-129">System-Only</span></span>            | <span data-ttu-id="6b090-130">否</span><span class="sxs-lookup"><span data-stu-id="6b090-130">False</span></span>                                                                                       |
| <span data-ttu-id="6b090-131">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6b090-131">Is-Single-Valued</span></span>       | <span data-ttu-id="6b090-132">對</span><span class="sxs-lookup"><span data-stu-id="6b090-132">True</span></span>                                                                                        |
| <span data-ttu-id="6b090-133">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6b090-133">Is Indexed</span></span>             | <span data-ttu-id="6b090-134">否</span><span class="sxs-lookup"><span data-stu-id="6b090-134">False</span></span>                                                                                       |
| <span data-ttu-id="6b090-135">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6b090-135">In Global Catalog</span></span>      | <span data-ttu-id="6b090-136">否</span><span class="sxs-lookup"><span data-stu-id="6b090-136">False</span></span>                                                                                       |
| <span data-ttu-id="6b090-137">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6b090-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="6b090-138">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6b090-138">O:BAG:BAD:S:</span></span>                                                                                |
| <span data-ttu-id="6b090-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6b090-139">Range-Lower</span></span>            | \-                                                                                          |
| <span data-ttu-id="6b090-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6b090-140">Range-Upper</span></span>            | \-                                                                                          |
| <span data-ttu-id="6b090-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6b090-141">Search-Flags</span></span>           | <span data-ttu-id="6b090-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b090-142">0x00000000</span></span>                                                                                  |
| <span data-ttu-id="6b090-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6b090-143">System-Flags</span></span>           | <span data-ttu-id="6b090-144">0x00000014</span><span class="sxs-lookup"><span data-stu-id="6b090-144">0x00000014</span></span>                                                                                  |
| <span data-ttu-id="6b090-145">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6b090-145">Classes used in</span></span>        | [<span data-ttu-id="6b090-146">**ms-DS-群組管理-服務-帳戶**</span><span class="sxs-lookup"><span data-stu-id="6b090-146">**ms-DS-Group-Managed-Service-Account**</span></span>](c-msds-groupmanagedserviceaccount.md)<br/> |



 

 





