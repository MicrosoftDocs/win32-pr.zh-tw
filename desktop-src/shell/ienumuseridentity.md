---
description: IEnumUserIdentity 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: 'IEnumUserIdentity 介面 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973124"
---
# <a name="ienumuseridentity-interface"></a><span data-ttu-id="e63c8-104">IEnumUserIdentity 介面</span><span class="sxs-lookup"><span data-stu-id="e63c8-104">IEnumUserIdentity interface</span></span>

<span data-ttu-id="e63c8-105">\[**IEnumUserIdentity** 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="e63c8-105">\[**IEnumUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="e63c8-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="e63c8-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="e63c8-107">提供系統上所有使用者身分識別的列舉。</span><span class="sxs-lookup"><span data-stu-id="e63c8-107">Provides enumeration of all user identities present on the system.</span></span>

## <a name="members"></a><span data-ttu-id="e63c8-108">成員</span><span class="sxs-lookup"><span data-stu-id="e63c8-108">Members</span></span>

<span data-ttu-id="e63c8-109">**IEnumUserIdentity** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="e63c8-109">The **IEnumUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e63c8-110">**IEnumUserIdentity** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e63c8-110">**IEnumUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="e63c8-111">方法</span><span class="sxs-lookup"><span data-stu-id="e63c8-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e63c8-112">方法</span><span class="sxs-lookup"><span data-stu-id="e63c8-112">Methods</span></span>

<span data-ttu-id="e63c8-113">**IEnumUserIdentity** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e63c8-113">The **IEnumUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="e63c8-114">方法</span><span class="sxs-lookup"><span data-stu-id="e63c8-114">Method</span></span>                                         | <span data-ttu-id="e63c8-115">描述</span><span class="sxs-lookup"><span data-stu-id="e63c8-115">Description</span></span>                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e63c8-116">**克隆**</span><span class="sxs-lookup"><span data-stu-id="e63c8-116">**Clone**</span></span>](ienumuseridentity-clone.md)       | <span data-ttu-id="e63c8-117">已取代。</span><span class="sxs-lookup"><span data-stu-id="e63c8-117">Deprecated.</span></span> <span data-ttu-id="e63c8-118">取得目前列舉的複本。</span><span class="sxs-lookup"><span data-stu-id="e63c8-118">Gets a copy of the current enumeration.</span></span><br/>                                                               |
| [<span data-ttu-id="e63c8-119">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="e63c8-119">**GetCount**</span></span>](ienumuseridentity-getcount.md) | <span data-ttu-id="e63c8-120">已取代。</span><span class="sxs-lookup"><span data-stu-id="e63c8-120">Deprecated.</span></span> <span data-ttu-id="e63c8-121">取得目前在系統上的使用者身分識別計數。</span><span class="sxs-lookup"><span data-stu-id="e63c8-121">Gets the count of user identities currently on the system.</span></span><br/>                                            |
| [<span data-ttu-id="e63c8-122">**下一步**</span><span class="sxs-lookup"><span data-stu-id="e63c8-122">**Next**</span></span>](ienumuseridentity-next.md)         | <span data-ttu-id="e63c8-123">已取代。</span><span class="sxs-lookup"><span data-stu-id="e63c8-123">Deprecated.</span></span> <span data-ttu-id="e63c8-124">從列舉中抓取使用者識別介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="e63c8-124">Retrieves an array of user identity interfaces from the enumeration.</span></span><br/>                                  |
| [<span data-ttu-id="e63c8-125">**重設**</span><span class="sxs-lookup"><span data-stu-id="e63c8-125">**Reset**</span></span>](ienumuseridentity-reset.md)       | <span data-ttu-id="e63c8-126">已取代。</span><span class="sxs-lookup"><span data-stu-id="e63c8-126">Deprecated.</span></span> <span data-ttu-id="e63c8-127">重設列舉中已抓取介面的內部計數。</span><span class="sxs-lookup"><span data-stu-id="e63c8-127">Resets the internal count of retrieved interfaces in the enumeration.</span></span><br/>                                 |
| [<span data-ttu-id="e63c8-128">**跳過**</span><span class="sxs-lookup"><span data-stu-id="e63c8-128">**Skip**</span></span>](ienumuseridentity-skip.md)         | <span data-ttu-id="e63c8-129">已取代。</span><span class="sxs-lookup"><span data-stu-id="e63c8-129">Deprecated.</span></span> <span data-ttu-id="e63c8-130">在列舉中略過指定數目的使用者識別介面。</span><span class="sxs-lookup"><span data-stu-id="e63c8-130">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="e63c8-131">在抓取介面時使用。</span><span class="sxs-lookup"><span data-stu-id="e63c8-131">Used when retrieving interfaces.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e63c8-132">備註</span><span class="sxs-lookup"><span data-stu-id="e63c8-132">Remarks</span></span>

<span data-ttu-id="e63c8-133">若要取得系統上存在的使用者身分識別相關資訊，您可以使用此介面。</span><span class="sxs-lookup"><span data-stu-id="e63c8-133">To retrieve information about user identities present on the system, you can use this interface.</span></span> <span data-ttu-id="e63c8-134">從 [**IUserIdentityManager**](iuseridentitymanager.md) 介面中，您可以呼叫 [**IUserIdentityManager：： EnumIdentities**](iuseridentitymanager-enumidentities.md) 以抓取這個介面。</span><span class="sxs-lookup"><span data-stu-id="e63c8-134">From a [**IUserIdentityManager**](iuseridentitymanager.md) interface, you can call [**IUserIdentityManager::EnumIdentities**](iuseridentitymanager-enumidentities.md) to retrieve this interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e63c8-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="e63c8-135">Requirements</span></span>



| <span data-ttu-id="e63c8-136">需求</span><span class="sxs-lookup"><span data-stu-id="e63c8-136">Requirement</span></span> | <span data-ttu-id="e63c8-137">值</span><span class="sxs-lookup"><span data-stu-id="e63c8-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e63c8-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e63c8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e63c8-139">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e63c8-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e63c8-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e63c8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e63c8-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e63c8-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e63c8-142">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e63c8-142">End of client support</span></span><br/>    | <span data-ttu-id="e63c8-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e63c8-143">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="e63c8-144">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e63c8-144">End of server support</span></span><br/>    | <span data-ttu-id="e63c8-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e63c8-145">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="e63c8-146">標頭</span><span class="sxs-lookup"><span data-stu-id="e63c8-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="e63c8-147"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="e63c8-147"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="e63c8-148">Idl</span><span class="sxs-lookup"><span data-stu-id="e63c8-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e63c8-149"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e63c8-149"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="e63c8-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e63c8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e63c8-151"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e63c8-151"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e63c8-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e63c8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e63c8-153">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="e63c8-153">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> </dl>

 

 
