---
title: ms-DS-使用者-密碼-非必要屬性
description: 指出這個屬性所參考的帳戶是否需要密碼。
ms.assetid: 86779c6f-d05c-409a-afe4-99ebf7c0593e
ms.tgt_platform: multiple
keywords:
- ms DS-使用者-密碼-不需要的屬性 AD 架構
- UserPasswordNotRequired 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Not-Required
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8ebb439af9a960d2dc0721940d9f4d2ab852b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108212"
---
# <a name="ms-ds-user-password-not-required-attribute"></a><span data-ttu-id="c6471-105">ms-DS-使用者-密碼-非必要屬性</span><span class="sxs-lookup"><span data-stu-id="c6471-105">ms-DS-User-Password-Not-Required attribute</span></span>

<span data-ttu-id="c6471-106">指出這個屬性所參考的帳戶是否需要密碼。</span><span class="sxs-lookup"><span data-stu-id="c6471-106">Indicates whether a password is required for the account that this attribute references.</span></span> <span data-ttu-id="c6471-107">如果不需要密碼，則為 True;否則為 False。</span><span class="sxs-lookup"><span data-stu-id="c6471-107">True if a password is not required; otherwise, False.</span></span>



| <span data-ttu-id="c6471-108">進入</span><span class="sxs-lookup"><span data-stu-id="c6471-108">Entry</span></span> | <span data-ttu-id="c6471-109">值</span><span class="sxs-lookup"><span data-stu-id="c6471-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c6471-110">CN</span><span class="sxs-lookup"><span data-stu-id="c6471-110">CN</span></span>                | <span data-ttu-id="c6471-111">ms-DS-使用者-密碼-非必要</span><span class="sxs-lookup"><span data-stu-id="c6471-111">ms-DS-User-Password-Not-Required</span></span>     |
| <span data-ttu-id="c6471-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c6471-112">Ldap-Display-Name</span></span> | <span data-ttu-id="c6471-113">UserPasswordNotRequired</span><span class="sxs-lookup"><span data-stu-id="c6471-113">ms-DS-UserPasswordNotRequired</span></span>        |
| <span data-ttu-id="c6471-114">大小</span><span class="sxs-lookup"><span data-stu-id="c6471-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="c6471-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c6471-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c6471-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c6471-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c6471-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c6471-117">Attribute-Id</span></span>      | <span data-ttu-id="c6471-118">1.2.840.113556.1.4.1854</span><span class="sxs-lookup"><span data-stu-id="c6471-118">1.2.840.113556.1.4.1854</span></span>              |
| <span data-ttu-id="c6471-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c6471-119">System-Id-Guid</span></span>    | <span data-ttu-id="c6471-120">8f066172-a25e-4f53-8dcd-0a67d5fb883d</span><span class="sxs-lookup"><span data-stu-id="c6471-120">8f066172-a25e-4f53-8dcd-0a67d5fb883d</span></span> |
| <span data-ttu-id="c6471-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6471-121">Syntax</span></span>            | [<span data-ttu-id="c6471-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c6471-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="c6471-123">實作</span><span class="sxs-lookup"><span data-stu-id="c6471-123">Implementations</span></span>

-   [<span data-ttu-id="c6471-124">**亞當**</span><span class="sxs-lookup"><span data-stu-id="c6471-124">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="c6471-125">亞當</span><span class="sxs-lookup"><span data-stu-id="c6471-125">ADAM</span></span>



| <span data-ttu-id="c6471-126">進入</span><span class="sxs-lookup"><span data-stu-id="c6471-126">Entry</span></span> | <span data-ttu-id="c6471-127">值</span><span class="sxs-lookup"><span data-stu-id="c6471-127">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="c6471-128">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c6471-128">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="c6471-129">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6471-129">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="c6471-130">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6471-130">System-Only</span></span>            | <span data-ttu-id="c6471-131">否</span><span class="sxs-lookup"><span data-stu-id="c6471-131">False</span></span>                                                             |
| <span data-ttu-id="c6471-132">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c6471-132">Is-Single-Valued</span></span>       | <span data-ttu-id="c6471-133">對</span><span class="sxs-lookup"><span data-stu-id="c6471-133">True</span></span>                                                              |
| <span data-ttu-id="c6471-134">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c6471-134">Is Indexed</span></span>             | <span data-ttu-id="c6471-135">否</span><span class="sxs-lookup"><span data-stu-id="c6471-135">False</span></span>                                                             |
| <span data-ttu-id="c6471-136">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c6471-136">In Global Catalog</span></span>      | <span data-ttu-id="c6471-137">否</span><span class="sxs-lookup"><span data-stu-id="c6471-137">False</span></span>                                                             |
| <span data-ttu-id="c6471-138">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c6471-138">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6471-139">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c6471-139">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="c6471-140">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6471-140">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="c6471-141">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6471-141">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="c6471-142">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6471-142">Search-Flags</span></span>           | <span data-ttu-id="c6471-143">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6471-143">0x00000000</span></span>                                                        |
| <span data-ttu-id="c6471-144">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6471-144">System-Flags</span></span>           | <span data-ttu-id="c6471-145">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6471-145">0x00000010</span></span>                                                        |
| <span data-ttu-id="c6471-146">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c6471-146">Classes used in</span></span>        | [<span data-ttu-id="c6471-147">**ms DS 可系結-物件**</span><span class="sxs-lookup"><span data-stu-id="c6471-147">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c6471-148">備註</span><span class="sxs-lookup"><span data-stu-id="c6471-148">Remarks</span></span>

<span data-ttu-id="c6471-149">在 ADAM 中，這個屬性會取代 [**userAccountControl**](a-useraccountcontrol.md)屬性的 [**ADS \_ UF \_ PASSWD \_ NOTREQD**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum)旗標。</span><span class="sxs-lookup"><span data-stu-id="c6471-149">In ADAM, this attribute replaces the [**ADS\_UF\_PASSWD\_NOTREQD**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

