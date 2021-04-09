---
title: GroupMSAMembership 屬性
description: 這個屬性是用來進行存取檢查，以判斷要求者是否有權取得群組 MSA 的密碼。
ms.assetid: 1512826d-fb7e-4039-ad93-f9334fd1d485
ms.tgt_platform: multiple
keywords:
- GroupMSAMembership 屬性 AD 架構
- GroupMSAMembership 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-GroupMSAMembership
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184f7f682d5360a0524f58e07c3f468b96e15b14
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935422"
---
# <a name="ms-ds-groupmsamembership-attribute"></a><span data-ttu-id="4a4c7-105">GroupMSAMembership 屬性</span><span class="sxs-lookup"><span data-stu-id="4a4c7-105">ms-DS-GroupMSAMembership attribute</span></span>

<span data-ttu-id="4a4c7-106">這個屬性是用來進行存取檢查，以判斷要求者是否有權取得群組 MSA 的密碼。</span><span class="sxs-lookup"><span data-stu-id="4a4c7-106">This attribute is used for access checks to determine if a requestor has permission to retrieve the password for a group MSA.</span></span>



| <span data-ttu-id="4a4c7-107">進入</span><span class="sxs-lookup"><span data-stu-id="4a4c7-107">Entry</span></span> | <span data-ttu-id="4a4c7-108">值</span><span class="sxs-lookup"><span data-stu-id="4a4c7-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="4a4c7-109">CN</span><span class="sxs-lookup"><span data-stu-id="4a4c7-109">CN</span></span>                | <span data-ttu-id="4a4c7-110">GroupMSAMembership</span><span class="sxs-lookup"><span data-stu-id="4a4c7-110">ms-DS-GroupMSAMembership</span></span>                            |
| <span data-ttu-id="4a4c7-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4a4c7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4a4c7-112">GroupMSAMembership</span><span class="sxs-lookup"><span data-stu-id="4a4c7-112">msDS-GroupMSAMembership</span></span>                             |
| <span data-ttu-id="4a4c7-113">大小</span><span class="sxs-lookup"><span data-stu-id="4a4c7-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="4a4c7-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4a4c7-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="4a4c7-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4a4c7-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="4a4c7-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4a4c7-116">Attribute-Id</span></span>      | <span data-ttu-id="4a4c7-117">1.2.840.113556.1.4.2200</span><span class="sxs-lookup"><span data-stu-id="4a4c7-117">1.2.840.113556.1.4.2200</span></span>                             |
| <span data-ttu-id="4a4c7-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4a4c7-118">System-Id-Guid</span></span>    | <span data-ttu-id="4a4c7-119">888eedd6-ce04-df40-b462-b8a50e41ba38</span><span class="sxs-lookup"><span data-stu-id="4a4c7-119">888eedd6-ce04-df40-b462-b8a50e41ba38</span></span>                |
| <span data-ttu-id="4a4c7-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a4c7-120">Syntax</span></span>            | [<span data-ttu-id="4a4c7-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="4a4c7-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="4a4c7-122">實作</span><span class="sxs-lookup"><span data-stu-id="4a4c7-122">Implementations</span></span>

-   [<span data-ttu-id="4a4c7-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4a4c7-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="4a4c7-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a4c7-124">Windows Server 2012</span></span>



| <span data-ttu-id="4a4c7-125">進入</span><span class="sxs-lookup"><span data-stu-id="4a4c7-125">Entry</span></span> | <span data-ttu-id="4a4c7-126">值</span><span class="sxs-lookup"><span data-stu-id="4a4c7-126">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a4c7-127">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4a4c7-127">Link-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="4a4c7-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4a4c7-128">MAPI-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="4a4c7-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="4a4c7-129">System-Only</span></span>            | <span data-ttu-id="4a4c7-130">否</span><span class="sxs-lookup"><span data-stu-id="4a4c7-130">False</span></span>                                                                                       |
| <span data-ttu-id="4a4c7-131">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4a4c7-131">Is-Single-Valued</span></span>       | <span data-ttu-id="4a4c7-132">對</span><span class="sxs-lookup"><span data-stu-id="4a4c7-132">True</span></span>                                                                                        |
| <span data-ttu-id="4a4c7-133">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4a4c7-133">Is Indexed</span></span>             | <span data-ttu-id="4a4c7-134">否</span><span class="sxs-lookup"><span data-stu-id="4a4c7-134">False</span></span>                                                                                       |
| <span data-ttu-id="4a4c7-135">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4a4c7-135">In Global Catalog</span></span>      | <span data-ttu-id="4a4c7-136">否</span><span class="sxs-lookup"><span data-stu-id="4a4c7-136">False</span></span>                                                                                       |
| <span data-ttu-id="4a4c7-137">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4a4c7-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="4a4c7-138">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4a4c7-138">O:BAG:BAD:S:</span></span>                                                                                |
| <span data-ttu-id="4a4c7-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4a4c7-139">Range-Lower</span></span>            | \-                                                                                          |
| <span data-ttu-id="4a4c7-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4a4c7-140">Range-Upper</span></span>            | \-                                                                                          |
| <span data-ttu-id="4a4c7-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4a4c7-141">Search-Flags</span></span>           | <span data-ttu-id="4a4c7-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a4c7-142">0x00000000</span></span>                                                                                  |
| <span data-ttu-id="4a4c7-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4a4c7-143">System-Flags</span></span>           | <span data-ttu-id="4a4c7-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4a4c7-144">0x00000010</span></span>                                                                                  |
| <span data-ttu-id="4a4c7-145">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4a4c7-145">Classes used in</span></span>        | [<span data-ttu-id="4a4c7-146">**ms-DS-群組管理-服務-帳戶**</span><span class="sxs-lookup"><span data-stu-id="4a4c7-146">**ms-DS-Group-Managed-Service-Account**</span></span>](c-msds-groupmanagedserviceaccount.md)<br/> |



 

 





