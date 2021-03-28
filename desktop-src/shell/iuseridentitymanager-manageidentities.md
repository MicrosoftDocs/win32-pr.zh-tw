---
description: IUserIdentityManager：： ManageIdentities 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'IUserIdentityManager：： ManageIdentities 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: b5b782a56324faf19dd1527d2cd363d26f0e337c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317951"
---
# <a name="iuseridentitymanagermanageidentities-method"></a><span data-ttu-id="b6e9b-104">IUserIdentityManager：： ManageIdentities 方法</span><span class="sxs-lookup"><span data-stu-id="b6e9b-104">IUserIdentityManager::ManageIdentities method</span></span>

<span data-ttu-id="b6e9b-105">\[**IUserIdentityManager：： ManageIdentities** 不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b6e9b-105">\[**IUserIdentityManager::ManageIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="b6e9b-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="b6e9b-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="b6e9b-107">向使用者顯示 UI，讓使用者可以管理使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="b6e9b-107">Displays a UI to the user, allowing the user to manage user identities.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6e9b-108">語法</span><span class="sxs-lookup"><span data-stu-id="b6e9b-108">Syntax</span></span>


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b6e9b-109">參數</span><span class="sxs-lookup"><span data-stu-id="b6e9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6e9b-110">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6e9b-110">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e9b-111">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="b6e9b-111">Type: **HWND**</span></span>

<span data-ttu-id="b6e9b-112">**HWND** 值，這個值會識別在關閉 UI 之後將會進入前景的視窗。</span><span class="sxs-lookup"><span data-stu-id="b6e9b-112">An **HWND** value that identifies a window that will be brought to the foreground after the UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="b6e9b-113">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6e9b-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e9b-114">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b6e9b-114">Type: **DWORD**</span></span>

<span data-ttu-id="b6e9b-115">定義 UI 行為方式的選擇性旗標。</span><span class="sxs-lookup"><span data-stu-id="b6e9b-115">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="b6e9b-116">設定為 UIMI \_ 建立 \_ 新 \_ 的身分識別，以提示使用者建立新的身分識別。</span><span class="sxs-lookup"><span data-stu-id="b6e9b-116">Set to UIMI\_CREATE\_NEW\_IDENTITY to prompt the user to create a new identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6e9b-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6e9b-117">Return value</span></span>

<span data-ttu-id="b6e9b-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b6e9b-118">Type: **HRESULT**</span></span>

<span data-ttu-id="b6e9b-119">管理作業的結果。</span><span class="sxs-lookup"><span data-stu-id="b6e9b-119">The result of the management operation.</span></span> <span data-ttu-id="b6e9b-120">如果成功，則會傳回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="b6e9b-120">If successful, it returns S\_OK.</span></span> <span data-ttu-id="b6e9b-121">否則，它會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b6e9b-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="b6e9b-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b6e9b-122">Return code</span></span>                                                                                            | <span data-ttu-id="b6e9b-123">Description</span><span class="sxs-lookup"><span data-stu-id="b6e9b-123">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="b6e9b-124"><dt>**E 身分識別 \_ \_ 已停用**</dt></span><span class="sxs-lookup"><span data-stu-id="b6e9b-124"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="b6e9b-125">系統上的身分識別管理已停用。</span><span class="sxs-lookup"><span data-stu-id="b6e9b-125">Identity management is disabled on the system.</span></span><br/> |
| <dl> <span data-ttu-id="b6e9b-126"><dt>**E \_ 使用者已 \_ 取消**</dt></span><span class="sxs-lookup"><span data-stu-id="b6e9b-126"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="b6e9b-127">使用者已取消對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b6e9b-127">The user canceled the dialog.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="b6e9b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6e9b-128">Requirements</span></span>



| <span data-ttu-id="b6e9b-129">需求</span><span class="sxs-lookup"><span data-stu-id="b6e9b-129">Requirement</span></span> | <span data-ttu-id="b6e9b-130">值</span><span class="sxs-lookup"><span data-stu-id="b6e9b-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e9b-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6e9b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e9b-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6e9b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b6e9b-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6e9b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e9b-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6e9b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b6e9b-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b6e9b-135">End of client support</span></span><br/>    | <span data-ttu-id="b6e9b-136">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b6e9b-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="b6e9b-137">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="b6e9b-137">End of server support</span></span><br/>    | <span data-ttu-id="b6e9b-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b6e9b-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="b6e9b-139">標頭</span><span class="sxs-lookup"><span data-stu-id="b6e9b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6e9b-140"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6e9b-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6e9b-141">Idl</span><span class="sxs-lookup"><span data-stu-id="b6e9b-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6e9b-142"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6e9b-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="b6e9b-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b6e9b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6e9b-144"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6e9b-144"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6e9b-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6e9b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e9b-146">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="b6e9b-146">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="b6e9b-147">**IUserIdentityManager：： Logon**</span><span class="sxs-lookup"><span data-stu-id="b6e9b-147">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="b6e9b-148">**IUserIdentityManager：：登出**</span><span class="sxs-lookup"><span data-stu-id="b6e9b-148">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




