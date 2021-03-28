---
description: IUserIdentityManager：： Logon 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'IUserIdentityManager：： Logon 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eee6e0555d45d3f52173fce085d19c14f2ccfe8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111713"
---
# <a name="iuseridentitymanagerlogon-method"></a><span data-ttu-id="46d29-104">IUserIdentityManager：： Logon 方法</span><span class="sxs-lookup"><span data-stu-id="46d29-104">IUserIdentityManager::Logon method</span></span>

<span data-ttu-id="46d29-105">\[**IUserIdentityManager：： Logon** 不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="46d29-105">\[**IUserIdentityManager::Logon** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="46d29-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="46d29-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="46d29-107">向使用者顯示 UI，讓使用者可以選擇使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="46d29-107">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="46d29-108">如果成功，將會登入並取出使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="46d29-108">If successful, the user identity will be logged on and retrieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="46d29-109">語法</span><span class="sxs-lookup"><span data-stu-id="46d29-109">Syntax</span></span>


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="46d29-110">參數</span><span class="sxs-lookup"><span data-stu-id="46d29-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d29-111">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46d29-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46d29-112">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="46d29-112">Type: **HWND**</span></span>

<span data-ttu-id="46d29-113">**HWND** 值，這個值會識別在關閉登入 UI 之後將會帶入前景的視窗。</span><span class="sxs-lookup"><span data-stu-id="46d29-113">An **HWND** value that identifies a window that will be brought to the foreground after the logon UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="46d29-114">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46d29-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46d29-115">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="46d29-115">Type: **DWORD**</span></span>

<span data-ttu-id="46d29-116">定義 UI 行為方式的選擇性旗標。</span><span class="sxs-lookup"><span data-stu-id="46d29-116">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="46d29-117">設定為 UIL \_ 強制 \_ ui 以強制 ui 顯示，即使已經選擇身分識別也一樣。</span><span class="sxs-lookup"><span data-stu-id="46d29-117">Set to UIL\_FORCE\_UI to force the UI to display, even if an identity has already been chosen.</span></span>

</dd> <dt>

<span data-ttu-id="46d29-118">*ppIdentity* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="46d29-118">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46d29-119">類型： **[ **IUserIdentity**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="46d29-119">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="46d29-120">接收所選使用者識別之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="46d29-120">The address of the pointer that receives the chosen user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d29-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="46d29-121">Return value</span></span>

<span data-ttu-id="46d29-122">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="46d29-122">Type: **HRESULT**</span></span>

<span data-ttu-id="46d29-123">登入操作的結果。</span><span class="sxs-lookup"><span data-stu-id="46d29-123">Result of the logon operation.</span></span> <span data-ttu-id="46d29-124">如果成功，則會傳回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="46d29-124">If successful, it returns S\_OK.</span></span> <span data-ttu-id="46d29-125">否則，它會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="46d29-125">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="46d29-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="46d29-126">Return code</span></span>                                                                                            | <span data-ttu-id="46d29-127">Description</span><span class="sxs-lookup"><span data-stu-id="46d29-127">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="46d29-128"><dt>**E \_ 使用者已 \_ 取消**</dt></span><span class="sxs-lookup"><span data-stu-id="46d29-128"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="46d29-129">使用者已從 UI 取消登入操作。</span><span class="sxs-lookup"><span data-stu-id="46d29-129">The user canceled the logon operation from the UI.</span></span><br/>                               |
| <dl> <span data-ttu-id="46d29-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="46d29-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="46d29-131">無法建立使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="46d29-131">The user identity could not be created.</span></span><br/>                                          |
| <dl> <span data-ttu-id="46d29-132"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="46d29-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="46d29-133">作業意外失敗。</span><span class="sxs-lookup"><span data-stu-id="46d29-133">The operation failed unexpectedly.</span></span><br/>                                               |
| <dl> <span data-ttu-id="46d29-134"><dt>**E 身分識別 \_ \_ 已停用**</dt></span><span class="sxs-lookup"><span data-stu-id="46d29-134"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="46d29-135">系統上的身分識別管理已停用。</span><span class="sxs-lookup"><span data-stu-id="46d29-135">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="46d29-136"><dt>**S 身分識別 \_ \_ 已停用**</dt></span><span class="sxs-lookup"><span data-stu-id="46d29-136"><dt>**S\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="46d29-137">系統上的身分識別管理已停用。</span><span class="sxs-lookup"><span data-stu-id="46d29-137">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="46d29-138"><dt>**E 身分 \_ 識別 \_ 變更**</dt></span><span class="sxs-lookup"><span data-stu-id="46d29-138"><dt>**E\_IDENTITY\_CHANGING**</dt></span></span> </dl>   | <span data-ttu-id="46d29-139">系統目前正在切換身分識別，因此無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="46d29-139">The system is currently switching identities, and cannot complete the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="46d29-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="46d29-140">Requirements</span></span>



| <span data-ttu-id="46d29-141">需求</span><span class="sxs-lookup"><span data-stu-id="46d29-141">Requirement</span></span> | <span data-ttu-id="46d29-142">值</span><span class="sxs-lookup"><span data-stu-id="46d29-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46d29-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46d29-143">Minimum supported client</span></span><br/> | <span data-ttu-id="46d29-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46d29-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="46d29-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46d29-145">Minimum supported server</span></span><br/> | <span data-ttu-id="46d29-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46d29-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="46d29-147">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="46d29-147">End of client support</span></span><br/>    | <span data-ttu-id="46d29-148">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="46d29-148">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="46d29-149">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="46d29-149">End of server support</span></span><br/>    | <span data-ttu-id="46d29-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="46d29-150">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="46d29-151">標頭</span><span class="sxs-lookup"><span data-stu-id="46d29-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="46d29-152"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="46d29-152"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="46d29-153">Idl</span><span class="sxs-lookup"><span data-stu-id="46d29-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46d29-154"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="46d29-154"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="46d29-155">DLL</span><span class="sxs-lookup"><span data-stu-id="46d29-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46d29-156"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46d29-156"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d29-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46d29-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d29-158">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="46d29-158">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="46d29-159">**IUserIdentityManager：：登出**</span><span class="sxs-lookup"><span data-stu-id="46d29-159">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> <dt>

[<span data-ttu-id="46d29-160">**IUserIdentityManager::ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="46d29-160">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




