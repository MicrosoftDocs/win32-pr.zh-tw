---
description: IUserIdentity2 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: 'IUserIdentity2 介面 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88142e462566a6afaf299096744a0b8f9ea83dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510772"
---
# <a name="iuseridentity2-interface"></a><span data-ttu-id="be32a-104">IUserIdentity2 介面</span><span class="sxs-lookup"><span data-stu-id="be32a-104">IUserIdentity2 interface</span></span>

<span data-ttu-id="be32a-105">\[**IUserIdentity2** 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="be32a-105">\[**IUserIdentity2** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="be32a-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="be32a-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="be32a-107">公開方法，以提供特定使用者身分識別的命名、密碼和序數控制項。</span><span class="sxs-lookup"><span data-stu-id="be32a-107">Exposes methods that provide naming, password, and ordinal control for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="be32a-108">成員</span><span class="sxs-lookup"><span data-stu-id="be32a-108">Members</span></span>

<span data-ttu-id="be32a-109">**IUserIdentity2** 介面繼承自 [**IUserIdentity**](iuseridentity.md)。</span><span class="sxs-lookup"><span data-stu-id="be32a-109">The **IUserIdentity2** interface inherits from [**IUserIdentity**](iuseridentity.md).</span></span> <span data-ttu-id="be32a-110">**IUserIdentity2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="be32a-110">**IUserIdentity2** also has these types of members:</span></span>

-   [<span data-ttu-id="be32a-111">方法</span><span class="sxs-lookup"><span data-stu-id="be32a-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be32a-112">方法</span><span class="sxs-lookup"><span data-stu-id="be32a-112">Methods</span></span>

<span data-ttu-id="be32a-113">**IUserIdentity2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="be32a-113">The **IUserIdentity2** interface has these methods.</span></span>



| <span data-ttu-id="be32a-114">方法</span><span class="sxs-lookup"><span data-stu-id="be32a-114">Method</span></span>                                                  | <span data-ttu-id="be32a-115">描述</span><span class="sxs-lookup"><span data-stu-id="be32a-115">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="be32a-116">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="be32a-116">**ChangePassword**</span></span>](iuseridentity2-changepassword.md) | <span data-ttu-id="be32a-117">已取代。</span><span class="sxs-lookup"><span data-stu-id="be32a-117">Deprecated.</span></span> <span data-ttu-id="be32a-118">為身分識別設定新的密碼。</span><span class="sxs-lookup"><span data-stu-id="be32a-118">Sets a new password for the identity.</span></span><br/>      |
| [<span data-ttu-id="be32a-119">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="be32a-119">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)         | <span data-ttu-id="be32a-120">已取代。</span><span class="sxs-lookup"><span data-stu-id="be32a-120">Deprecated.</span></span> <span data-ttu-id="be32a-121">取得此身分識別的序號。</span><span class="sxs-lookup"><span data-stu-id="be32a-121">Gets the ordinal number for this identity.</span></span><br/> |
| [<span data-ttu-id="be32a-122">**SetName**</span><span class="sxs-lookup"><span data-stu-id="be32a-122">**SetName**</span></span>](iuseridentity2-setname.md)               | <span data-ttu-id="be32a-123">已取代。</span><span class="sxs-lookup"><span data-stu-id="be32a-123">Deprecated.</span></span> <span data-ttu-id="be32a-124">設定身分識別的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="be32a-124">Sets the display name of the identity.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="be32a-125">備註</span><span class="sxs-lookup"><span data-stu-id="be32a-125">Remarks</span></span>

<span data-ttu-id="be32a-126">這個介面也會提供它所繼承之 [**IUserIdentity**](iuseridentity.md) 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="be32a-126">This interface also provides the methods of the [**IUserIdentity**](iuseridentity.md) interface, from which it inherits.</span></span>

## <a name="requirements"></a><span data-ttu-id="be32a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="be32a-127">Requirements</span></span>



| <span data-ttu-id="be32a-128">需求</span><span class="sxs-lookup"><span data-stu-id="be32a-128">Requirement</span></span> | <span data-ttu-id="be32a-129">值</span><span class="sxs-lookup"><span data-stu-id="be32a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be32a-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be32a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="be32a-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be32a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="be32a-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be32a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="be32a-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be32a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="be32a-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="be32a-134">End of client support</span></span><br/>    | <span data-ttu-id="be32a-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="be32a-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="be32a-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="be32a-136">End of server support</span></span><br/>    | <span data-ttu-id="be32a-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="be32a-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="be32a-138">標頭</span><span class="sxs-lookup"><span data-stu-id="be32a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="be32a-139"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="be32a-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="be32a-140">Idl</span><span class="sxs-lookup"><span data-stu-id="be32a-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be32a-141"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="be32a-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="be32a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="be32a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be32a-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be32a-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be32a-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be32a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be32a-145">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="be32a-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> </dl>

 

 




