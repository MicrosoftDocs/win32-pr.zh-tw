---
title: ms DS-使用者-帳戶-自動鎖定屬性
description: 指出此屬性參考的帳戶是否已被鎖定。
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- ms DS-使用者-帳戶-自動鎖定的屬性 AD 架構
- UserAccountAutoLocked 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6623a1b348af14fecc8dab41a44439bf2d745bf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104025584"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a><span data-ttu-id="39be8-105">ms DS-使用者-帳戶-自動鎖定屬性</span><span class="sxs-lookup"><span data-stu-id="39be8-105">ms-DS-User-Account-Auto-Locked attribute</span></span>

<span data-ttu-id="39be8-106">指出此屬性參考的帳戶是否已被鎖定。如果帳戶遭到鎖定，則為 True;否則為 False。</span><span class="sxs-lookup"><span data-stu-id="39be8-106">Indicates whether the account that this attribute references has been locked out. True if the account is locked out; otherwise, False.</span></span>



| <span data-ttu-id="39be8-107">進入</span><span class="sxs-lookup"><span data-stu-id="39be8-107">Entry</span></span> | <span data-ttu-id="39be8-108">值</span><span class="sxs-lookup"><span data-stu-id="39be8-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="39be8-109">CN</span><span class="sxs-lookup"><span data-stu-id="39be8-109">CN</span></span>                | <span data-ttu-id="39be8-110">ms DS-使用者-帳戶-自動鎖定</span><span class="sxs-lookup"><span data-stu-id="39be8-110">ms-DS-User-Account-Auto-Locked</span></span>       |
| <span data-ttu-id="39be8-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="39be8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="39be8-112">UserAccountAutoLocked</span><span class="sxs-lookup"><span data-stu-id="39be8-112">ms-DS-UserAccountAutoLocked</span></span>          |
| <span data-ttu-id="39be8-113">大小</span><span class="sxs-lookup"><span data-stu-id="39be8-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="39be8-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="39be8-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="39be8-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="39be8-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="39be8-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="39be8-116">Attribute-Id</span></span>      | <span data-ttu-id="39be8-117">1.2.840.113556.1.4.1857</span><span class="sxs-lookup"><span data-stu-id="39be8-117">1.2.840.113556.1.4.1857</span></span>              |
| <span data-ttu-id="39be8-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="39be8-118">System-Id-Guid</span></span>    | <span data-ttu-id="39be8-119">f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d</span><span class="sxs-lookup"><span data-stu-id="39be8-119">f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d</span></span> |
| <span data-ttu-id="39be8-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="39be8-120">Syntax</span></span>            | [<span data-ttu-id="39be8-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="39be8-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="39be8-122">實作</span><span class="sxs-lookup"><span data-stu-id="39be8-122">Implementations</span></span>

-   [<span data-ttu-id="39be8-123">**亞當**</span><span class="sxs-lookup"><span data-stu-id="39be8-123">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="39be8-124">亞當</span><span class="sxs-lookup"><span data-stu-id="39be8-124">ADAM</span></span>



| <span data-ttu-id="39be8-125">進入</span><span class="sxs-lookup"><span data-stu-id="39be8-125">Entry</span></span> | <span data-ttu-id="39be8-126">值</span><span class="sxs-lookup"><span data-stu-id="39be8-126">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="39be8-127">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="39be8-127">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="39be8-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39be8-128">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="39be8-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="39be8-129">System-Only</span></span>            | <span data-ttu-id="39be8-130">否</span><span class="sxs-lookup"><span data-stu-id="39be8-130">False</span></span>                                                             |
| <span data-ttu-id="39be8-131">是-單一值</span><span class="sxs-lookup"><span data-stu-id="39be8-131">Is-Single-Valued</span></span>       | <span data-ttu-id="39be8-132">對</span><span class="sxs-lookup"><span data-stu-id="39be8-132">True</span></span>                                                              |
| <span data-ttu-id="39be8-133">已編制索引</span><span class="sxs-lookup"><span data-stu-id="39be8-133">Is Indexed</span></span>             | <span data-ttu-id="39be8-134">否</span><span class="sxs-lookup"><span data-stu-id="39be8-134">False</span></span>                                                             |
| <span data-ttu-id="39be8-135">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="39be8-135">In Global Catalog</span></span>      | <span data-ttu-id="39be8-136">否</span><span class="sxs-lookup"><span data-stu-id="39be8-136">False</span></span>                                                             |
| <span data-ttu-id="39be8-137">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="39be8-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="39be8-138">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="39be8-138">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="39be8-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39be8-139">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="39be8-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39be8-140">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="39be8-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39be8-141">Search-Flags</span></span>           | <span data-ttu-id="39be8-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39be8-142">0x00000000</span></span>                                                        |
| <span data-ttu-id="39be8-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39be8-143">System-Flags</span></span>           | <span data-ttu-id="39be8-144">0x00000014</span><span class="sxs-lookup"><span data-stu-id="39be8-144">0x00000014</span></span>                                                        |
| <span data-ttu-id="39be8-145">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="39be8-145">Classes used in</span></span>        | [<span data-ttu-id="39be8-146">**ms DS 可系結-物件**</span><span class="sxs-lookup"><span data-stu-id="39be8-146">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="39be8-147">備註</span><span class="sxs-lookup"><span data-stu-id="39be8-147">Remarks</span></span>

<span data-ttu-id="39be8-148">在 ADAM 中，這個屬性會取代 [**userAccountControl**](a-useraccountcontrol.md)屬性的 [**ADS \_ UF \_ 鎖定**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum)旗標。</span><span class="sxs-lookup"><span data-stu-id="39be8-148">In ADAM, this attribute replaces the [**ADS\_UF\_LOCKOUT**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

