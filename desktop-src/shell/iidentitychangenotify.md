---
description: 已取代。 提供對系統上使用者身分識別的修改通知，以及切換目前使用者身分識別的使用者要求。
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: 'IIdentityChangeNotify 介面 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4a217b2cfb046bfb9ae5546e015264f74d00b1d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192675"
---
# <a name="iidentitychangenotify-interface"></a><span data-ttu-id="47452-104">IIdentityChangeNotify 介面</span><span class="sxs-lookup"><span data-stu-id="47452-104">IIdentityChangeNotify interface</span></span>

<span data-ttu-id="47452-105">\[**IIdentityChangeNotify** 介面可用於 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="47452-105">\[The **IIdentityChangeNotify** interface is available for use in Windows 2000.</span></span> <span data-ttu-id="47452-106">在 Windows XP 中，這項功能已由 [使用者帳戶取代為快速使用者切換和遠端桌面](fastuserswitching.md)，而且可能會在後續版本中變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="47452-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="47452-107">已取代。</span><span class="sxs-lookup"><span data-stu-id="47452-107">Deprecated.</span></span> <span data-ttu-id="47452-108">提供對系統上使用者身分識別的修改通知，以及切換目前使用者身分識別的使用者要求。</span><span class="sxs-lookup"><span data-stu-id="47452-108">Provides notification of modifications to user identities on the system, as well as user requests to switch the current user identity.</span></span>

## <a name="members"></a><span data-ttu-id="47452-109">成員</span><span class="sxs-lookup"><span data-stu-id="47452-109">Members</span></span>

<span data-ttu-id="47452-110">**IIdentityChangeNotify** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="47452-110">The **IIdentityChangeNotify** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="47452-111">**IIdentityChangeNotify** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="47452-111">**IIdentityChangeNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="47452-112">方法</span><span class="sxs-lookup"><span data-stu-id="47452-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="47452-113">方法</span><span class="sxs-lookup"><span data-stu-id="47452-113">Methods</span></span>

<span data-ttu-id="47452-114">**IIdentityChangeNotify** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="47452-114">The **IIdentityChangeNotify** interface has these methods.</span></span>



| <span data-ttu-id="47452-115">方法</span><span class="sxs-lookup"><span data-stu-id="47452-115">Method</span></span>                                                                                 | <span data-ttu-id="47452-116">描述</span><span class="sxs-lookup"><span data-stu-id="47452-116">Description</span></span>                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47452-117">**IdentityInformationChanged**</span><span class="sxs-lookup"><span data-stu-id="47452-117">**IdentityInformationChanged**</span></span>](iidentitychangenotify-identityinformationchanged.md) | <span data-ttu-id="47452-118">已取代。</span><span class="sxs-lookup"><span data-stu-id="47452-118">Deprecated.</span></span> <span data-ttu-id="47452-119">當使用者身分識別的相關資訊變更，或新增或刪除使用者身分識別時呼叫。</span><span class="sxs-lookup"><span data-stu-id="47452-119">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span><br/>  |
| [<span data-ttu-id="47452-120">**QuerySwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="47452-120">**QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)           | <span data-ttu-id="47452-121">已取代。</span><span class="sxs-lookup"><span data-stu-id="47452-121">Deprecated.</span></span> <span data-ttu-id="47452-122">當目前使用者要求切換其使用者身分識別，但在切換之前發生時呼叫。</span><span class="sxs-lookup"><span data-stu-id="47452-122">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span><br/> |
| [<span data-ttu-id="47452-123">**SwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="47452-123">**SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)                     | <span data-ttu-id="47452-124">已取代。</span><span class="sxs-lookup"><span data-stu-id="47452-124">Deprecated.</span></span> <span data-ttu-id="47452-125">當使用者身分識別切換時呼叫。</span><span class="sxs-lookup"><span data-stu-id="47452-125">Called when user identities are switched.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="47452-126">備註</span><span class="sxs-lookup"><span data-stu-id="47452-126">Remarks</span></span>

<span data-ttu-id="47452-127">若要執行通知，衍生介面必須藉由呼叫 [**IConnectionPoint：： Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise)和將指標傳遞至介面，來連接到 [**IUserIdentityManager**](iuseridentitymanager.md) 。</span><span class="sxs-lookup"><span data-stu-id="47452-127">To implement notifications, a derived interface must connect to the [**IUserIdentityManager**](iuseridentitymanager.md) by calling [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) and by passing a pointer to the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="47452-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="47452-128">Requirements</span></span>



| <span data-ttu-id="47452-129">需求</span><span class="sxs-lookup"><span data-stu-id="47452-129">Requirement</span></span> | <span data-ttu-id="47452-130">值</span><span class="sxs-lookup"><span data-stu-id="47452-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47452-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="47452-131">Minimum supported client</span></span><br/> | <span data-ttu-id="47452-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47452-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="47452-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="47452-133">Minimum supported server</span></span><br/> | <span data-ttu-id="47452-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47452-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="47452-135">標頭</span><span class="sxs-lookup"><span data-stu-id="47452-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="47452-136"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="47452-136"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="47452-137">Idl</span><span class="sxs-lookup"><span data-stu-id="47452-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47452-138"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="47452-138"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="47452-139">DLL</span><span class="sxs-lookup"><span data-stu-id="47452-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47452-140"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47452-140"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="47452-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47452-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47452-142">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="47452-142">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="47452-143">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="47452-143">**IConnectionPoint**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
