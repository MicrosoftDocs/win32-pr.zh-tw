---
title: ms DS-使用者加密-文字-允許的屬性
description: 指出 Active Directory 是否會以可還原的加密格式儲存密碼。
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- ms DS-使用者加密-文字-允許的屬性 AD 架構
- UserEncryptedTextPasswordAllowed 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d99ae61566ceec94336fd58951214dfc3255d2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467200"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a><span data-ttu-id="8f25a-105">ms DS-使用者加密-文字-允許的屬性</span><span class="sxs-lookup"><span data-stu-id="8f25a-105">ms-DS-User-Encrypted-Text-Password-Allowed attribute</span></span>

<span data-ttu-id="8f25a-106">指出 Active Directory 是否會以可還原的加密格式儲存密碼。</span><span class="sxs-lookup"><span data-stu-id="8f25a-106">Indicates whether Active Directory will store the password in the reversible encryption format.</span></span> <span data-ttu-id="8f25a-107">如果密碼以可還原的加密格式儲存，則為 True;否則為 False。</span><span class="sxs-lookup"><span data-stu-id="8f25a-107">True if the password is stored in the reversible encryption format; otherwise, False.</span></span>

> [!Note]  
> <span data-ttu-id="8f25a-108">[Active Directory 輕量型目錄服務](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services)不會使用這個屬性，而且只會隨附于 userAccountControl 的完整性/同位。</span><span class="sxs-lookup"><span data-stu-id="8f25a-108">This attribute is not used by [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) and is only included for completeness/parity with userAccountControl.</span></span> <span data-ttu-id="8f25a-109">AD LDS 不會以可還原的加密儲存密碼，無論此屬性在任何指定的物件上的值為何，或是與電腦本身的可還原加密有關的電腦安全性策略。</span><span class="sxs-lookup"><span data-stu-id="8f25a-109">AD LDS does not store passwords with reversible encryption, regardless of this attribute's value on any given object or the computer security policy pertaining to reversible encryption on the computer itself.</span></span>

 



| <span data-ttu-id="8f25a-110">進入</span><span class="sxs-lookup"><span data-stu-id="8f25a-110">Entry</span></span> | <span data-ttu-id="8f25a-111">值</span><span class="sxs-lookup"><span data-stu-id="8f25a-111">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="8f25a-112">CN</span><span class="sxs-lookup"><span data-stu-id="8f25a-112">CN</span></span>                | <span data-ttu-id="8f25a-113">ms DS-使用者加密-文字-允許的密碼</span><span class="sxs-lookup"><span data-stu-id="8f25a-113">ms-DS-User-Encrypted-Text-Password-Allowed</span></span> |
| <span data-ttu-id="8f25a-114">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8f25a-114">Ldap-Display-Name</span></span> | <span data-ttu-id="8f25a-115">UserEncryptedTextPasswordAllowed</span><span class="sxs-lookup"><span data-stu-id="8f25a-115">ms-DS-UserEncryptedTextPasswordAllowed</span></span>     |
| <span data-ttu-id="8f25a-116">大小</span><span class="sxs-lookup"><span data-stu-id="8f25a-116">Size</span></span>              | \-                                         |
| <span data-ttu-id="8f25a-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8f25a-117">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="8f25a-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8f25a-118">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="8f25a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8f25a-119">Attribute-Id</span></span>      | <span data-ttu-id="8f25a-120">1.2.840.113556.1.4.1856</span><span class="sxs-lookup"><span data-stu-id="8f25a-120">1.2.840.113556.1.4.1856</span></span>                    |
| <span data-ttu-id="8f25a-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8f25a-121">System-Id-Guid</span></span>    | <span data-ttu-id="8f25a-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span><span class="sxs-lookup"><span data-stu-id="8f25a-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span></span>       |
| <span data-ttu-id="8f25a-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f25a-123">Syntax</span></span>            | [<span data-ttu-id="8f25a-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f25a-124">**Boolean**</span></span>](s-boolean.md)               |



## <a name="implementations"></a><span data-ttu-id="8f25a-125">實作</span><span class="sxs-lookup"><span data-stu-id="8f25a-125">Implementations</span></span>

-   [<span data-ttu-id="8f25a-126">**亞當**</span><span class="sxs-lookup"><span data-stu-id="8f25a-126">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="8f25a-127">亞當</span><span class="sxs-lookup"><span data-stu-id="8f25a-127">ADAM</span></span>



| <span data-ttu-id="8f25a-128">進入</span><span class="sxs-lookup"><span data-stu-id="8f25a-128">Entry</span></span> | <span data-ttu-id="8f25a-129">值</span><span class="sxs-lookup"><span data-stu-id="8f25a-129">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="8f25a-130">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8f25a-130">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8f25a-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8f25a-131">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="8f25a-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="8f25a-132">System-Only</span></span>            | <span data-ttu-id="8f25a-133">否</span><span class="sxs-lookup"><span data-stu-id="8f25a-133">False</span></span>                                                             |
| <span data-ttu-id="8f25a-134">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8f25a-134">Is-Single-Valued</span></span>       | <span data-ttu-id="8f25a-135">對</span><span class="sxs-lookup"><span data-stu-id="8f25a-135">True</span></span>                                                              |
| <span data-ttu-id="8f25a-136">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8f25a-136">Is Indexed</span></span>             | <span data-ttu-id="8f25a-137">否</span><span class="sxs-lookup"><span data-stu-id="8f25a-137">False</span></span>                                                             |
| <span data-ttu-id="8f25a-138">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8f25a-138">In Global Catalog</span></span>      | <span data-ttu-id="8f25a-139">否</span><span class="sxs-lookup"><span data-stu-id="8f25a-139">False</span></span>                                                             |
| <span data-ttu-id="8f25a-140">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8f25a-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="8f25a-141">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8f25a-141">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="8f25a-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8f25a-142">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="8f25a-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8f25a-143">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="8f25a-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8f25a-144">Search-Flags</span></span>           | <span data-ttu-id="8f25a-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8f25a-145">0x00000000</span></span>                                                        |
| <span data-ttu-id="8f25a-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8f25a-146">System-Flags</span></span>           | <span data-ttu-id="8f25a-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8f25a-147">0x00000010</span></span>                                                        |
| <span data-ttu-id="8f25a-148">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8f25a-148">Classes used in</span></span>        | [<span data-ttu-id="8f25a-149">**ms DS 可系結-物件**</span><span class="sxs-lookup"><span data-stu-id="8f25a-149">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8f25a-150">備註</span><span class="sxs-lookup"><span data-stu-id="8f25a-150">Remarks</span></span>

<span data-ttu-id="8f25a-151">在 ADAM 中，這個屬性會取代 [**userAccountControl**](a-useraccountcontrol.md)屬性的 [**ADS 已 \_ \_ 加密 \_ 文字 \_ 密碼 \_ 允許**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum)旗標。</span><span class="sxs-lookup"><span data-stu-id="8f25a-151">In ADAM, this attribute replaces the [**ADS\_UF\_ENCRYPTED\_TEXT\_PASSWORD\_ALLOWED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

