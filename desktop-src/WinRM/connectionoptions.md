---
title: 'ConnectionOptions 物件 (WSManDisp) '
description: ConnectionOptions 物件會傳遞至 CreateSession 方法，以提供與遠端電腦上的本機帳戶相關聯的使用者名稱和密碼。
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- ConnectionOptions 物件 Windows 遠端管理
- ConnectionOptions 物件 Windows 遠端管理，說明
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 164eb886ce98266cab3109e773b731e002d1abac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968363"
---
# <a name="connectionoptions-object"></a><span data-ttu-id="96651-105">ConnectionOptions 物件</span><span class="sxs-lookup"><span data-stu-id="96651-105">ConnectionOptions object</span></span>

<span data-ttu-id="96651-106">**ConnectionOptions** 物件會傳遞至 [**CreateSession**](wsman-createsession.md)方法，以提供與遠端電腦上的本機帳戶相關聯的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="96651-106">The **ConnectionOptions** object is passed to the [**CreateSession**](wsman-createsession.md) method to provide the user name and password associated with the local account on the remote computer.</span></span> <span data-ttu-id="96651-107">如果未提供任何參數，則執行腳本之帳戶的認證會設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="96651-107">If no parameters are supplied, then the credentials of the account running the script are set to the default values.</span></span>

## <a name="members"></a><span data-ttu-id="96651-108">成員</span><span class="sxs-lookup"><span data-stu-id="96651-108">Members</span></span>

<span data-ttu-id="96651-109">**ConnectionOptions** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="96651-109">The **ConnectionOptions** object has these types of members:</span></span>

-   [<span data-ttu-id="96651-110">屬性</span><span class="sxs-lookup"><span data-stu-id="96651-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96651-111">屬性</span><span class="sxs-lookup"><span data-stu-id="96651-111">Properties</span></span>

<span data-ttu-id="96651-112">**ConnectionOptions** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="96651-112">The **ConnectionOptions** object has these properties.</span></span>



| <span data-ttu-id="96651-113">屬性</span><span class="sxs-lookup"><span data-stu-id="96651-113">Property</span></span>                                                  | <span data-ttu-id="96651-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="96651-114">Access type</span></span>           | <span data-ttu-id="96651-115">Description</span><span class="sxs-lookup"><span data-stu-id="96651-115">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96651-116">**密碼**</span><span class="sxs-lookup"><span data-stu-id="96651-116">**Password**</span></span>](connectionoptions-password.md)<br/> | <span data-ttu-id="96651-117">唯寫</span><span class="sxs-lookup"><span data-stu-id="96651-117">Write-only</span></span><br/> | <span data-ttu-id="96651-118">設定遠端電腦上的本機或網域帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="96651-118">Sets the password of a local or domain account on the remote computer.</span></span><br/>           |
| [<span data-ttu-id="96651-119">**使用者**</span><span class="sxs-lookup"><span data-stu-id="96651-119">**UserName**</span></span>](connectionoptions-username.md)<br/> | <span data-ttu-id="96651-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="96651-120">Read/write</span></span><br/> | <span data-ttu-id="96651-121">設定並取得遠端電腦上本機或網域帳戶的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="96651-121">Sets and gets the user name of a local or domain account on the remote computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="96651-122">備註</span><span class="sxs-lookup"><span data-stu-id="96651-122">Remarks</span></span>

<span data-ttu-id="96651-123">**ConnectionOptions** 物件會對應至 [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)介面。</span><span class="sxs-lookup"><span data-stu-id="96651-123">The **ConnectionOptions** object corresponds to the [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) interface.</span></span>

<span data-ttu-id="96651-124">如果 Windows 遠端管理用戶端應用程式是在模擬下執行，則如果您設定 [**Password**](connectionoptions-password.md) 屬性，就會發生失敗。</span><span class="sxs-lookup"><span data-stu-id="96651-124">If a Windows Remote Management client application is running under impersonation, then a failure occurs if you set the [**Password**](connectionoptions-password.md) property.</span></span> <span data-ttu-id="96651-125">用戶端應用程式是在本機或遠端電腦上將要求傳送至 WinRM 的腳本或其他程式。</span><span class="sxs-lookup"><span data-stu-id="96651-125">A client application is a script or other program that sends a request to WinRM on the local or a remote computer.</span></span> <span data-ttu-id="96651-126">用戶端應用程式可能會在模擬下執行，因為它呼叫的函式如 [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="96651-126">The client application may be running under impersonation because it called a function like [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)).</span></span> <span data-ttu-id="96651-127">如果 ASP 進程是在模擬用戶端的帳戶下執行，則 (ASP) 或服務的作用中伺服器頁面就無法要求使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="96651-127">An Active Server Page (ASP) or service cannot request a user name and password if the ASP process runs under an account that impersonates a client.</span></span>

<span data-ttu-id="96651-128">使用使用者 [**名稱**](connectionoptions-username.md)和 [**密碼**](connectionoptions-password.md)進行驗證時，應在 [**WSman. CreateSession**](wsman-createsession.md)呼叫上設定 **WSManFlagCredUserNamePassword** 旗標。</span><span class="sxs-lookup"><span data-stu-id="96651-128">The **WSManFlagCredUserNamePassword** flag should be set on the [**WSman.CreateSession**](wsman-createsession.md) call when using the [**UserName**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md) for authentication.</span></span>

## <a name="examples"></a><span data-ttu-id="96651-129">範例</span><span class="sxs-lookup"><span data-stu-id="96651-129">Examples</span></span>

<span data-ttu-id="96651-130">下列 VBScript 程式碼範例示範如何建立 **ConnectionOptions** 物件、在遠端電腦上設定帳戶的屬性，以及用來建立 [**會話**](session.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="96651-130">The following VBScript code example shows how to create a **ConnectionOptions** object, set the properties for the account on the remote computer, and use it in creating a [**Session**](session.md) object.</span></span>


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
```



## <a name="requirements"></a><span data-ttu-id="96651-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="96651-131">Requirements</span></span>



| <span data-ttu-id="96651-132">需求</span><span class="sxs-lookup"><span data-stu-id="96651-132">Requirement</span></span> | <span data-ttu-id="96651-133">值</span><span class="sxs-lookup"><span data-stu-id="96651-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="96651-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96651-134">Minimum supported client</span></span><br/> | <span data-ttu-id="96651-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96651-135">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="96651-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96651-136">Minimum supported server</span></span><br/> | <span data-ttu-id="96651-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96651-137">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="96651-138">標頭</span><span class="sxs-lookup"><span data-stu-id="96651-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="96651-139"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="96651-139"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="96651-140">Idl</span><span class="sxs-lookup"><span data-stu-id="96651-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96651-141"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="96651-141"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="96651-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="96651-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="96651-143"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="96651-143"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="96651-144">DLL</span><span class="sxs-lookup"><span data-stu-id="96651-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96651-145"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96651-145"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96651-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96651-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96651-147">遠端連線的驗證</span><span class="sxs-lookup"><span data-stu-id="96651-147">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="96651-148">WinRM 腳本 API</span><span class="sxs-lookup"><span data-stu-id="96651-148">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="96651-149">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="96651-149">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="96651-150">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="96651-150">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="96651-151">Windows 遠端管理中的腳本</span><span class="sxs-lookup"><span data-stu-id="96651-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="96651-152">從本機電腦取得資料</span><span class="sxs-lookup"><span data-stu-id="96651-152">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="96651-153">從遠端電腦取得資料</span><span class="sxs-lookup"><span data-stu-id="96651-153">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

