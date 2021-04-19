---
description: SWbemSecurity 物件會取得或設定指派給物件的安全性設定，例如許可權、COM 模擬和驗證層級。
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: 'SWbemSecurity 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978874"
---
# <a name="swbemsecurity-object"></a><span data-ttu-id="19e17-103">SWbemSecurity 物件</span><span class="sxs-lookup"><span data-stu-id="19e17-103">SWbemSecurity object</span></span>

<span data-ttu-id="19e17-104">**SWbemSecurity** 物件會取得或設定指派給物件的安全性設定，例如許可權、COM 模擬和驗證層級。</span><span class="sxs-lookup"><span data-stu-id="19e17-104">The **SWbemSecurity** object gets or sets security settings, such as privileges, COM impersonations, and authentication levels assigned to an object.</span></span> <span data-ttu-id="19e17-105">[**Wbemscripting.swbemlocator**](swbemlocator.md)、 [**SWbemServices**](swbemservices.md)、 [**SWbemObject**](swbemobject.md)、 [**swbemobjectset 搭配使用**](swbemobjectset.md)、 [**SWbemObjectPath**](swbemobjectpath.md)、 [**SWbemLastError**](swbemlasterror.md)和 [**SWbemEventSource**](swbemeventsource.md)物件都有 **安全性 \_** 屬性，也就是 **SWbemSecurity** 物件。</span><span class="sxs-lookup"><span data-stu-id="19e17-105">The [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md), and [**SWbemEventSource**](swbemeventsource.md) objects have a **Security\_** property, which is the **SWbemSecurity** object.</span></span> <span data-ttu-id="19e17-106">當您取得實例或查看 WMI 安全性記錄檔時，可能需要設定 **安全性 \_** 物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="19e17-106">When you retrieve an instance or view the WMI security log, you might need to set the properties of the **Security\_** object.</span></span>

<span data-ttu-id="19e17-107">VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 呼叫無法建立安全性物件。</span><span class="sxs-lookup"><span data-stu-id="19e17-107">The VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call cannot create the Security object.</span></span> <span data-ttu-id="19e17-108">此物件中的安全性設定不會識別 WMI 連線上的驗證、模擬或許可權設定，或在非同步呼叫中將物件傳遞到接收時，對 proxy 的安全性有效。</span><span class="sxs-lookup"><span data-stu-id="19e17-108">The security settings in this object do not identify the authentication, impersonation, or privilege settings on a connection to WMI, or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="19e17-109">如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。</span><span class="sxs-lookup"><span data-stu-id="19e17-109">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

## <a name="members"></a><span data-ttu-id="19e17-110">成員</span><span class="sxs-lookup"><span data-stu-id="19e17-110">Members</span></span>

<span data-ttu-id="19e17-111">**SWbemSecurity** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="19e17-111">The **SWbemSecurity** object has these types of members:</span></span>

-   [<span data-ttu-id="19e17-112">屬性</span><span class="sxs-lookup"><span data-stu-id="19e17-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19e17-113">屬性</span><span class="sxs-lookup"><span data-stu-id="19e17-113">Properties</span></span>

<span data-ttu-id="19e17-114">**SWbemSecurity** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="19e17-114">The **SWbemSecurity** object has these properties.</span></span>



| <span data-ttu-id="19e17-115">屬性</span><span class="sxs-lookup"><span data-stu-id="19e17-115">Property</span></span>                                                                    | <span data-ttu-id="19e17-116">存取類型</span><span class="sxs-lookup"><span data-stu-id="19e17-116">Access type</span></span>           | <span data-ttu-id="19e17-117">Description</span><span class="sxs-lookup"><span data-stu-id="19e17-117">Description</span></span>                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19e17-118">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="19e17-118">**AuthenticationLevel**</span></span>](swbemsecurity-authenticationlevel.md)<br/> | <span data-ttu-id="19e17-119">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="19e17-119">Read/write</span></span><br/> | <span data-ttu-id="19e17-120">數值，定義指派給這個物件的 COM 驗證層級。</span><span class="sxs-lookup"><span data-stu-id="19e17-120">Numeric value that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="19e17-121">此設定會決定您如何保護從 WMI 傳送的資訊。</span><span class="sxs-lookup"><span data-stu-id="19e17-121">This setting determines how you protect information sent from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="19e17-122">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="19e17-122">**ImpersonationLevel**</span></span>](swbemsecurity-impersonationlevel.md)<br/>   | <span data-ttu-id="19e17-123">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="19e17-123">Read/write</span></span><br/> | <span data-ttu-id="19e17-124">數值，定義指派給這個物件的 COM 模擬層級。</span><span class="sxs-lookup"><span data-stu-id="19e17-124">Numeric value that defines the COM Impersonation level that is assigned to this object.</span></span> <span data-ttu-id="19e17-125">這項設定會決定 WMI 所擁有的進程是否可以在呼叫其他進程時，偵測或使用您的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="19e17-125">This setting determines if processes owned by WMI can detect or use your security credentials when making calls to other processes.</span></span><br/> |
| [<span data-ttu-id="19e17-126">**特權**</span><span class="sxs-lookup"><span data-stu-id="19e17-126">**Privileges**</span></span>](swbemsecurity-privileges.md)<br/>                   | <span data-ttu-id="19e17-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="19e17-127">Read-only</span></span><br/>  | <span data-ttu-id="19e17-128">[**SWbemPrivilegeSet**](swbemprivilegeset.md)物件，定義此物件的許可權。</span><span class="sxs-lookup"><span data-stu-id="19e17-128">An [**SWbemPrivilegeSet**](swbemprivilegeset.md) object that defines privileges for this object.</span></span> <span data-ttu-id="19e17-129">如需詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。</span><span class="sxs-lookup"><span data-stu-id="19e17-129">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="19e17-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="19e17-130">Requirements</span></span>



| <span data-ttu-id="19e17-131">需求</span><span class="sxs-lookup"><span data-stu-id="19e17-131">Requirement</span></span> | <span data-ttu-id="19e17-132">值</span><span class="sxs-lookup"><span data-stu-id="19e17-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19e17-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19e17-133">Minimum supported client</span></span><br/> | <span data-ttu-id="19e17-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19e17-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19e17-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19e17-135">Minimum supported server</span></span><br/> | <span data-ttu-id="19e17-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19e17-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19e17-137">標頭</span><span class="sxs-lookup"><span data-stu-id="19e17-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="19e17-138"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="19e17-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="19e17-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="19e17-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="19e17-140"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="19e17-140"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="19e17-141">DLL</span><span class="sxs-lookup"><span data-stu-id="19e17-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19e17-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19e17-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="19e17-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="19e17-143">CLSID</span></span><br/>                    | <span data-ttu-id="19e17-144">CLSID \_ SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="19e17-144">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="19e17-145">IID</span><span class="sxs-lookup"><span data-stu-id="19e17-145">IID</span></span><br/>                      | <span data-ttu-id="19e17-146">IID \_ ISWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="19e17-146">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="19e17-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19e17-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e17-148">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="19e17-148">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="19e17-149">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="19e17-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="19e17-150">設定用戶端 \_ 應用程式 \_ 處理安全性</span><span class="sxs-lookup"><span data-stu-id="19e17-150">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="19e17-151">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="19e17-151">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="19e17-152">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="19e17-152">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="19e17-153">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="19e17-153">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

