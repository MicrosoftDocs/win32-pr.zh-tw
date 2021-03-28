---
description: IUserIdentity 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: 'IUserIdentity 介面 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973113"
---
# <a name="iuseridentity-interface"></a><span data-ttu-id="14d01-104">IUserIdentity 介面</span><span class="sxs-lookup"><span data-stu-id="14d01-104">IUserIdentity interface</span></span>

<span data-ttu-id="14d01-105">\[**IUserIdentity** 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="14d01-105">\[**IUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="14d01-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="14d01-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="14d01-107">公開方法，以提供特定使用者身分識別的識別、登錄和資料夾資料。</span><span class="sxs-lookup"><span data-stu-id="14d01-107">Exposes methods that provide identification, registry, and folder data for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="14d01-108">成員</span><span class="sxs-lookup"><span data-stu-id="14d01-108">Members</span></span>

<span data-ttu-id="14d01-109">**IUserIdentity** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="14d01-109">The **IUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="14d01-110">**IUserIdentity** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="14d01-110">**IUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="14d01-111">方法</span><span class="sxs-lookup"><span data-stu-id="14d01-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="14d01-112">方法</span><span class="sxs-lookup"><span data-stu-id="14d01-112">Methods</span></span>

<span data-ttu-id="14d01-113">**IUserIdentity** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="14d01-113">The **IUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="14d01-114">方法</span><span class="sxs-lookup"><span data-stu-id="14d01-114">Method</span></span>                                                         | <span data-ttu-id="14d01-115">描述</span><span class="sxs-lookup"><span data-stu-id="14d01-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14d01-116">**System.windows.application.getcookie**</span><span class="sxs-lookup"><span data-stu-id="14d01-116">**GetCookie**</span></span>](iuseridentity-getcookie.md)                   | <span data-ttu-id="14d01-117">已取代。</span><span class="sxs-lookup"><span data-stu-id="14d01-117">Deprecated.</span></span> <span data-ttu-id="14d01-118">取得用來唯一識別此使用者識別的 cookie。</span><span class="sxs-lookup"><span data-stu-id="14d01-118">Gets the cookie used to uniquely identify this user identity.</span></span><br/>             |
| [<span data-ttu-id="14d01-119">**GetIdentityFolder**</span><span class="sxs-lookup"><span data-stu-id="14d01-119">**GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)   | <span data-ttu-id="14d01-120">已取代。</span><span class="sxs-lookup"><span data-stu-id="14d01-120">Deprecated.</span></span> <span data-ttu-id="14d01-121">取得與此身分識別相關聯的檔案資料夾。</span><span class="sxs-lookup"><span data-stu-id="14d01-121">Gets the file folder associated with this identity.</span></span><br/>                       |
| [<span data-ttu-id="14d01-122">**GetName**</span><span class="sxs-lookup"><span data-stu-id="14d01-122">**GetName**</span></span>](iuseridentity-getname.md)                       | <span data-ttu-id="14d01-123">已取代。</span><span class="sxs-lookup"><span data-stu-id="14d01-123">Deprecated.</span></span> <span data-ttu-id="14d01-124">取得與此使用者識別相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="14d01-124">Gets the name associated with this user identity.</span></span><br/>                         |
| [<span data-ttu-id="14d01-125">**OpenIdentityRegKey**</span><span class="sxs-lookup"><span data-stu-id="14d01-125">**OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md) | <span data-ttu-id="14d01-126">已取代。</span><span class="sxs-lookup"><span data-stu-id="14d01-126">Deprecated.</span></span> <span data-ttu-id="14d01-127">抓取登錄中對應此使用者識別的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="14d01-127">Retrieves the key in the registry that corresponds to this user identity.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="14d01-128">備註</span><span class="sxs-lookup"><span data-stu-id="14d01-128">Remarks</span></span>

<span data-ttu-id="14d01-129">這個介面所提供的資訊，會對應至系統上存在的特定使用者識別。</span><span class="sxs-lookup"><span data-stu-id="14d01-129">This interface provides information that corresponds to a specific user identity present on the system.</span></span> <span data-ttu-id="14d01-130">您可以存取這個使用者身分識別的身分識別資料夾、其登錄機碼及其識別碼，以及取得與使用者身分識別相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="14d01-130">You can access this user identity's identity folder, its registry key, and its identification cookie, as well as retrieve the name associated with the user identity.</span></span>

## <a name="requirements"></a><span data-ttu-id="14d01-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="14d01-131">Requirements</span></span>



| <span data-ttu-id="14d01-132">需求</span><span class="sxs-lookup"><span data-stu-id="14d01-132">Requirement</span></span> | <span data-ttu-id="14d01-133">值</span><span class="sxs-lookup"><span data-stu-id="14d01-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14d01-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14d01-134">Minimum supported client</span></span><br/> | <span data-ttu-id="14d01-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14d01-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="14d01-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14d01-136">Minimum supported server</span></span><br/> | <span data-ttu-id="14d01-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14d01-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="14d01-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="14d01-138">End of client support</span></span><br/>    | <span data-ttu-id="14d01-139">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="14d01-139">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="14d01-140">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="14d01-140">End of server support</span></span><br/>    | <span data-ttu-id="14d01-141">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14d01-141">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="14d01-142">標頭</span><span class="sxs-lookup"><span data-stu-id="14d01-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="14d01-143"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="14d01-143"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="14d01-144">Idl</span><span class="sxs-lookup"><span data-stu-id="14d01-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14d01-145"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="14d01-145"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="14d01-146">DLL</span><span class="sxs-lookup"><span data-stu-id="14d01-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14d01-147"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14d01-147"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14d01-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14d01-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d01-149">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="14d01-149">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="14d01-150">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="14d01-150">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="14d01-151">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="14d01-151">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> </dl>

 

 
