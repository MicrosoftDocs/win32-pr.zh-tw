---
description: 不支援登出，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: e03fb15c-47d3-40ba-ae70-b7b0ba010004
title: 'IUserIdentityManager：：登出方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logoff
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 4266e6116e43b7b792c3040d7c86a60037ca4c44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971868"
---
# <a name="iuseridentitymanagerlogoff-method"></a><span data-ttu-id="0a40c-104">IUserIdentityManager：：登出方法</span><span class="sxs-lookup"><span data-stu-id="0a40c-104">IUserIdentityManager::Logoff method</span></span>

<span data-ttu-id="0a40c-105">\[不支援 **登出**，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="0a40c-105">\[**Logoff** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="0a40c-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="0a40c-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="0a40c-107">已取代。</span><span class="sxs-lookup"><span data-stu-id="0a40c-107">Deprecated.</span></span> <span data-ttu-id="0a40c-108">登出目前的身分識別。</span><span class="sxs-lookup"><span data-stu-id="0a40c-108">Log off the current identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a40c-109">語法</span><span class="sxs-lookup"><span data-stu-id="0a40c-109">Syntax</span></span>


```C++
HRESULT Logoff(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="0a40c-110">參數</span><span class="sxs-lookup"><span data-stu-id="0a40c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a40c-111">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0a40c-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a40c-112">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="0a40c-112">Type: **HWND**</span></span>

<span data-ttu-id="0a40c-113">**HWND** 值，可識別登出完成時，將會進入前景的視窗。</span><span class="sxs-lookup"><span data-stu-id="0a40c-113">An **HWND** value that identifies a window that will be brought into the foreground when the logoff is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a40c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a40c-114">Return value</span></span>

<span data-ttu-id="0a40c-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0a40c-115">Type: **HRESULT**</span></span>

<span data-ttu-id="0a40c-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0a40c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0a40c-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0a40c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a40c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a40c-118">Requirements</span></span>



| <span data-ttu-id="0a40c-119">需求</span><span class="sxs-lookup"><span data-stu-id="0a40c-119">Requirement</span></span> | <span data-ttu-id="0a40c-120">值</span><span class="sxs-lookup"><span data-stu-id="0a40c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a40c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a40c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0a40c-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a40c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0a40c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a40c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0a40c-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a40c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0a40c-125">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0a40c-125">End of client support</span></span><br/>    | <span data-ttu-id="0a40c-126">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0a40c-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="0a40c-127">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="0a40c-127">End of server support</span></span><br/>    | <span data-ttu-id="0a40c-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0a40c-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="0a40c-129">標頭</span><span class="sxs-lookup"><span data-stu-id="0a40c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a40c-130"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a40c-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a40c-131">Idl</span><span class="sxs-lookup"><span data-stu-id="0a40c-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0a40c-132"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0a40c-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="0a40c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0a40c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a40c-134"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a40c-134"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a40c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a40c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a40c-136">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="0a40c-136">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="0a40c-137">**IUserIdentityManager：： Logon**</span><span class="sxs-lookup"><span data-stu-id="0a40c-137">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="0a40c-138">**IUserIdentityManager::ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="0a40c-138">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




