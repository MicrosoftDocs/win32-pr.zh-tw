---
description: ImpersonationLevel 屬性是一個整數，可定義指派給此物件的 COM 模擬層級。
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: SWbemSecurity. ImpersonationLevel 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3b996d5920aba91fddf880ee9ddf6bf8081fb39f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852627"
---
# <a name="swbemsecurityimpersonationlevel-property"></a><span data-ttu-id="e2803-103">SWbemSecurity. ImpersonationLevel 屬性</span><span class="sxs-lookup"><span data-stu-id="e2803-103">SWbemSecurity.ImpersonationLevel property</span></span>

<span data-ttu-id="e2803-104">**ImpersonationLevel** 屬性是一個整數，可定義指派給此物件的 COM 模擬層級。</span><span class="sxs-lookup"><span data-stu-id="e2803-104">The **ImpersonationLevel** property is an integer that defines the COM impersonation level that is assigned to this object.</span></span> <span data-ttu-id="e2803-105">這項設定會決定 Windows Management Instrumentation (WMI) 是否可以在呼叫其他進程時偵測或使用您的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="e2803-105">This setting determines if processes owned by Windows Management Instrumentation (WMI) can detect or use your security credentials when making calls to other processes.</span></span> <span data-ttu-id="e2803-106">如需模擬層級的詳細資訊，請參閱 [設定用戶端 \_ 應用程式 \_ 處理安全性](setting-client-application-process-security.md)。</span><span class="sxs-lookup"><span data-stu-id="e2803-106">For more information about impersonation levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span>

<span data-ttu-id="e2803-107">如果您未明確設定 SWBemSecurity 中的模擬層級，或在安全物件上設定 **ImpersonationLevel** 屬性，則 WMI 會將預設模擬等級設定為 [預設模擬層級](setting-the-default-process-security-level-using-vbscript.md)登錄機碼中指定的值。</span><span class="sxs-lookup"><span data-stu-id="e2803-107">If you do not set the impersonation level specifically in either a moniker, or by setting the **SWBemSecurity.ImpersonationLevel** property on a securable object, WMI sets the default impersonation level to the value specified in the [default impersonation level registry key](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="e2803-108">如果此設定不足，提供者就不會為您的要求提供服務，而 WMI API 的呼叫可能會失敗，並出現錯誤碼 **wbemErrAccessDenied** (2147749891/0x80041003) 。</span><span class="sxs-lookup"><span data-stu-id="e2803-108">If this setting is not sufficient, the provider does not service your request, and the call to the WMI API can fail with an error code of **wbemErrAccessDenied** (2147749891/0x80041003).</span></span>

<span data-ttu-id="e2803-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="e2803-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e2803-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2803-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2803-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2803-111">Syntax</span></span>


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="e2803-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="e2803-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="e2803-113">備註</span><span class="sxs-lookup"><span data-stu-id="e2803-113">Remarks</span></span>

<span data-ttu-id="e2803-114">您可以將此屬性設定為下列其中一個值，做為 DCOM 模擬等級：</span><span class="sxs-lookup"><span data-stu-id="e2803-114">As a DCOM impersonation level, this property can be set to one of the following values:</span></span>



| <span data-ttu-id="e2803-115">值</span><span class="sxs-lookup"><span data-stu-id="e2803-115">Value</span></span>           | <span data-ttu-id="e2803-116">描述</span><span class="sxs-lookup"><span data-stu-id="e2803-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2803-117">**匿名**</span><span class="sxs-lookup"><span data-stu-id="e2803-117">**Anonymous**</span></span>   | <span data-ttu-id="e2803-118">隱藏呼叫端的認證。</span><span class="sxs-lookup"><span data-stu-id="e2803-118">Hides the credentials of the caller.</span></span> <span data-ttu-id="e2803-119">WMI 實際上不支援此模擬等級;如果腳本指定 impersonationLevel = Anonymous，WMI 將會以無訊息模式升級模擬等級來識別。</span><span class="sxs-lookup"><span data-stu-id="e2803-119">WMI does not actually support this impersonation level; if a script specifies impersonationLevel=Anonymous, WMI will silently upgrade the impersonation level to Identify.</span></span> <span data-ttu-id="e2803-120">不過，這在某些方面是無意義的練習，因為使用識別層級的腳本可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="e2803-120">This is in some ways a meaningless exercise, however, because scripts using the Identify level are likely to fail.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e2803-121">**識別**</span><span class="sxs-lookup"><span data-stu-id="e2803-121">**Identify**</span></span>    | <span data-ttu-id="e2803-122">可讓物件查詢呼叫端的認證。</span><span class="sxs-lookup"><span data-stu-id="e2803-122">Enables objects to query the credentials of the caller.</span></span> <span data-ttu-id="e2803-123">使用此模擬等級的腳本可能會失敗;識別層級通常可讓您不需要檢查存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="e2803-123">Scripts using this impersonation level are likely to fail; the Identify level typically lets you do no more than check access control lists.</span></span> <span data-ttu-id="e2803-124">您將無法使用 [識別] 對遠端電腦執行腳本。</span><span class="sxs-lookup"><span data-stu-id="e2803-124">You will not be able to run scripts against remote computers using Identify.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="e2803-125">**Impersonate**</span><span class="sxs-lookup"><span data-stu-id="e2803-125">**Impersonate**</span></span> | <span data-ttu-id="e2803-126">讓物件能夠使用呼叫端的認證。</span><span class="sxs-lookup"><span data-stu-id="e2803-126">Enables objects to use the credentials of the caller.</span></span> <span data-ttu-id="e2803-127">建議您搭配使用此模擬層級與 WMI 腳本。</span><span class="sxs-lookup"><span data-stu-id="e2803-127">It is recommended that you use this impersonation level with WMI scripts.</span></span> <span data-ttu-id="e2803-128">當您這樣做時，WMI 腳本會使用您的使用者認證;如此一來，它就能夠執行您可以執行的任何工作。</span><span class="sxs-lookup"><span data-stu-id="e2803-128">When you do so, the WMI script will use your user credentials; as a result, it will be able to perform any tasks that you are able to perform.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="e2803-129">**代理人**</span><span class="sxs-lookup"><span data-stu-id="e2803-129">**Delegate**</span></span>    | <span data-ttu-id="e2803-130">可讓物件允許其他物件使用呼叫端的認證。</span><span class="sxs-lookup"><span data-stu-id="e2803-130">Enables objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="e2803-131">委派可讓腳本在遠端電腦上使用您的認證，然後讓該遠端電腦在另一部遠端電腦上使用您的認證。</span><span class="sxs-lookup"><span data-stu-id="e2803-131">Delegation allows a script to use your credentials on a remote computer and then enables that remote computer to use your credentials on another remote computer.</span></span> <span data-ttu-id="e2803-132">雖然您可以在 WMI 腳本中使用此模擬層級，但您應該只在必要時才這麼做，因為它可能會造成安全性風險。</span><span class="sxs-lookup"><span data-stu-id="e2803-132">While you can use this impersonation level within WMI scripts, you should do so only if necessary because it might pose a security risk.</span></span><br/> <span data-ttu-id="e2803-133">除非交易中所有相關的使用者帳戶和電腦帳戶都已在 Active Directory 中標示為受信任，否則您無法使用委派模擬層級。</span><span class="sxs-lookup"><span data-stu-id="e2803-133">You cannot use the Delegate impersonation level unless all the user accounts and computer accounts involved in the transaction have all been marked as Trusted for delegation in Active Directory.</span></span> <span data-ttu-id="e2803-134">這有助於將安全性風險降至最低。</span><span class="sxs-lookup"><span data-stu-id="e2803-134">This helps minimize the security risks.</span></span> <span data-ttu-id="e2803-135">雖然遠端電腦可以使用您的認證，但只有在與交易相關的任何其他電腦都受信任可進行委派時，才可以這樣做。</span><span class="sxs-lookup"><span data-stu-id="e2803-135">Although a remote computer can use your credentials, it can do so only if both it and any other computers involved in the transaction are trusted for delegation.</span></span><br/> |



 

<span data-ttu-id="e2803-136">如上所述，匿名模擬會隱藏您的認證，並識別允許遠端物件查詢您的認證，但遠端物件無法模擬您的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="e2803-136">As noted, Anonymous impersonation hides your credentials and Identify permits a remote object to query your credentials, but the remote object cannot impersonate your security context.</span></span> <span data-ttu-id="e2803-137"> (換句話說，雖然遠端物件知道您的身分，但它無法「假裝」您 ) 。使用這兩種設定的其中一種來存取遠端電腦的 WMI 腳本通常會失敗。</span><span class="sxs-lookup"><span data-stu-id="e2803-137">(In other words, although the remote object knows who you are, it cannot "pretend" to be you.) WMI scripts accessing remote computers using one of these two settings will generally fail.</span></span> <span data-ttu-id="e2803-138">事實上，大部分的腳本都是在本機電腦上使用這兩種設定的其中一種來執行也會失敗。</span><span class="sxs-lookup"><span data-stu-id="e2803-138">In fact, most scripts run on the local computer using one of these two settings will also fail.</span></span>

<span data-ttu-id="e2803-139">模擬允許遠端 WMI 服務使用您的安全性內容來執行要求的作業。</span><span class="sxs-lookup"><span data-stu-id="e2803-139">Impersonate permits the remote WMI service to use your security context to perform the requested operation.</span></span> <span data-ttu-id="e2803-140">如果您的認證具有足夠的許可權可執行預定的作業，則使用模擬設定的遠端 WMI 要求通常會成功。</span><span class="sxs-lookup"><span data-stu-id="e2803-140">A remote WMI request that uses the Impersonate setting typically succeeds, provided your credentials have sufficient privileges to perform the intended operation.</span></span> <span data-ttu-id="e2803-141">換句話說，您不能使用 WMI 來 (遠端執行動作，或者) 您沒有在 WMI 外部執行的許可權。</span><span class="sxs-lookup"><span data-stu-id="e2803-141">In other words, you cannot use WMI to perform an action (remotely or otherwise) that you do not have permission to perform outside WMI.</span></span>

<span data-ttu-id="e2803-142">將 impersonationLevel 設定為 Delegate，可讓遠端 WMI 服務將您的認證傳遞給其他物件，而且通常會被視為安全性風險。</span><span class="sxs-lookup"><span data-stu-id="e2803-142">Setting impersonationLevel to Delegate permits the remote WMI service to pass your credentials on to other objects and is generally considered a security risk.</span></span>

<span data-ttu-id="e2803-143">您可以設定 [**SWbemServices**](swbemservices.md)、 [**SWbemObject**](swbemobject.md)、 [**swbemobjectset 搭配使用**](swbemobjectset.md)、 [**SWbemObjectPath**](swbemobjectpath.md)和 [**wbemscripting.swbemlocator**](swbemlocator.md) 物件的模擬層級，方法是將 **ImpersonationLevel** 屬性設定為所需的值。</span><span class="sxs-lookup"><span data-stu-id="e2803-143">You can set the impersonation level of an [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) object by setting the **ImpersonationLevel** property to the desired value.</span></span> <span data-ttu-id="e2803-144">下列範例說明如何設定 **SWbemObject** 物件的模擬等級：</span><span class="sxs-lookup"><span data-stu-id="e2803-144">The following example shows you how to set the impersonation level for an **SWbemObject** object:</span></span>


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



<span data-ttu-id="e2803-145">您也可以將模擬層級指定為標記的一部分。</span><span class="sxs-lookup"><span data-stu-id="e2803-145">You can also specify impersonation levels as part of a moniker.</span></span> <span data-ttu-id="e2803-146">下列範例會設定驗證層級和模擬等級，並抓取 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)的實例。</span><span class="sxs-lookup"><span data-stu-id="e2803-146">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
```



## <a name="requirements"></a><span data-ttu-id="e2803-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2803-147">Requirements</span></span>



| <span data-ttu-id="e2803-148">需求</span><span class="sxs-lookup"><span data-stu-id="e2803-148">Requirement</span></span> | <span data-ttu-id="e2803-149">值</span><span class="sxs-lookup"><span data-stu-id="e2803-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2803-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2803-150">Minimum supported client</span></span><br/> | <span data-ttu-id="e2803-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2803-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2803-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2803-152">Minimum supported server</span></span><br/> | <span data-ttu-id="e2803-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2803-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2803-154">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e2803-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2803-155"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e2803-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e2803-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e2803-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2803-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2803-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e2803-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="e2803-158">CLSID</span></span><br/>                    | <span data-ttu-id="e2803-159">CLSID \_ SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="e2803-159">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="e2803-160">IID</span><span class="sxs-lookup"><span data-stu-id="e2803-160">IID</span></span><br/>                      | <span data-ttu-id="e2803-161">IID \_ ISWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="e2803-161">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="e2803-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2803-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2803-163">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="e2803-163">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="e2803-164">設定用戶端 \_ 應用程式 \_ 處理安全性</span><span class="sxs-lookup"><span data-stu-id="e2803-164">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="e2803-165">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="e2803-165">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

