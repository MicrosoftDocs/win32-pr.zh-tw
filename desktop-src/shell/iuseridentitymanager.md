---
description: IUserIdentityManager 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: 'IUserIdentityManager 介面 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847623"
---
# <a name="iuseridentitymanager-interface"></a><span data-ttu-id="fa927-104">IUserIdentityManager 介面</span><span class="sxs-lookup"><span data-stu-id="fa927-104">IUserIdentityManager interface</span></span>

<span data-ttu-id="fa927-105">\[**IUserIdentityManager** 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="fa927-105">\[**IUserIdentityManager** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="fa927-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="fa927-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="fa927-107">公開方法，以識別、列舉和管理系統上的使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="fa927-107">Exposes methods that identify, enumerate, and manage user identities on the system.</span></span>

## <a name="members"></a><span data-ttu-id="fa927-108">成員</span><span class="sxs-lookup"><span data-stu-id="fa927-108">Members</span></span>

<span data-ttu-id="fa927-109">**IUserIdentityManager** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="fa927-109">The **IUserIdentityManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fa927-110">**IUserIdentityManager** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fa927-110">**IUserIdentityManager** also has these types of members:</span></span>

-   [<span data-ttu-id="fa927-111">方法</span><span class="sxs-lookup"><span data-stu-id="fa927-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fa927-112">方法</span><span class="sxs-lookup"><span data-stu-id="fa927-112">Methods</span></span>

<span data-ttu-id="fa927-113">**IUserIdentityManager** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fa927-113">The **IUserIdentityManager** interface has these methods.</span></span>



| <span data-ttu-id="fa927-114">方法</span><span class="sxs-lookup"><span data-stu-id="fa927-114">Method</span></span>                                                                  | <span data-ttu-id="fa927-115">描述</span><span class="sxs-lookup"><span data-stu-id="fa927-115">Description</span></span>                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa927-116">**EnumIdentities**</span><span class="sxs-lookup"><span data-stu-id="fa927-116">**EnumIdentities**</span></span>](iuseridentitymanager-enumidentities.md)           | <span data-ttu-id="fa927-117">已取代。</span><span class="sxs-lookup"><span data-stu-id="fa927-117">Deprecated.</span></span> <span data-ttu-id="fa927-118">取得 [**IEnumUserIdentity**](ienumuseridentity.md) 物件，可用來列舉系統上存在的使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="fa927-118">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span><br/> |
| [<span data-ttu-id="fa927-119">**GetIdentityByCookie**</span><span class="sxs-lookup"><span data-stu-id="fa927-119">**GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md) | <span data-ttu-id="fa927-120">已取代。</span><span class="sxs-lookup"><span data-stu-id="fa927-120">Deprecated.</span></span> <span data-ttu-id="fa927-121">依據用來唯一識別它的 cookie 取得特定使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="fa927-121">Gets a specific user identity by the cookie used to uniquely identify it.</span></span><br/>                                                                        |
| [<span data-ttu-id="fa927-122">**登出**</span><span class="sxs-lookup"><span data-stu-id="fa927-122">**Logoff**</span></span>](iuseridentitymanager-logoff.md)                           | <span data-ttu-id="fa927-123">已取代。</span><span class="sxs-lookup"><span data-stu-id="fa927-123">Deprecated.</span></span> <span data-ttu-id="fa927-124">登出目前的身分識別。</span><span class="sxs-lookup"><span data-stu-id="fa927-124">Log off the current identity.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="fa927-125">**登入**</span><span class="sxs-lookup"><span data-stu-id="fa927-125">**Logon**</span></span>](iuseridentitymanager-logon.md)                             | <span data-ttu-id="fa927-126">已取代。</span><span class="sxs-lookup"><span data-stu-id="fa927-126">Deprecated.</span></span> <span data-ttu-id="fa927-127">向使用者顯示 UI，讓使用者可以選擇使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="fa927-127">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="fa927-128">如果成功，將會登入並取出使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="fa927-128">If successful, the user identity will be logged on and retrieved.</span></span><br/>        |
| [<span data-ttu-id="fa927-129">**ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="fa927-129">**ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)       | <span data-ttu-id="fa927-130">已取代。</span><span class="sxs-lookup"><span data-stu-id="fa927-130">Deprecated.</span></span> <span data-ttu-id="fa927-131">向使用者顯示 UI，讓使用者可以管理使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="fa927-131">Displays a UI to the user, allowing the user to manage user identities.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="fa927-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa927-132">Requirements</span></span>



| <span data-ttu-id="fa927-133">需求</span><span class="sxs-lookup"><span data-stu-id="fa927-133">Requirement</span></span> | <span data-ttu-id="fa927-134">值</span><span class="sxs-lookup"><span data-stu-id="fa927-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa927-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa927-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fa927-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa927-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fa927-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa927-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fa927-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa927-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fa927-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="fa927-139">End of client support</span></span><br/>    | <span data-ttu-id="fa927-140">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fa927-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="fa927-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="fa927-141">End of server support</span></span><br/>    | <span data-ttu-id="fa927-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fa927-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="fa927-143">標頭</span><span class="sxs-lookup"><span data-stu-id="fa927-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa927-144"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa927-144"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa927-145">Idl</span><span class="sxs-lookup"><span data-stu-id="fa927-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa927-146"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa927-146"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="fa927-147">DLL</span><span class="sxs-lookup"><span data-stu-id="fa927-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa927-148"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa927-148"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa927-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa927-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa927-150">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="fa927-150">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="fa927-151">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="fa927-151">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="fa927-152">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="fa927-152">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="fa927-153">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="fa927-153">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> </dl>

 

 
