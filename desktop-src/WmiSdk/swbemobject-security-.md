---
description: '\_SWbemObject 物件的 security 屬性是用來讀取或設定 SWbemObject 物件的安全性設定。'
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: 'SWbemObject.Security_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f4d4b9aec7b6d800fa27609abd5d0cb1f3a435a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320664"
---
# <a name="swbemobjectsecurity_-property"></a><span data-ttu-id="c6ddb-103">SWbemObject 安全性 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="c6ddb-103">SWbemObject.Security\_ property</span></span>

<span data-ttu-id="c6ddb-104">[**SWbemObject**](swbemobject.md)物件的 **security \_** 屬性是用來讀取或設定 **SWbemObject** 物件的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="c6ddb-104">The **Security\_** property of the [**SWbemObject**](swbemobject.md) object is used to read, or set the security settings for an **SWbemObject** object.</span></span> <span data-ttu-id="c6ddb-105">這個屬性是 [**SWbemSecurity**](swbemsecurity.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="c6ddb-105">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="c6ddb-106">此物件中的安全性設定不會指出對 Windows Management Instrumentation (WMI) 的連線所進行的驗證、模擬或許可權設定，或是當物件在非同步呼叫中傳遞到接收時，對 proxy 的安全性有效。</span><span class="sxs-lookup"><span data-stu-id="c6ddb-106">The security settings in this object do not indicate the authentication, impersonation, or privilege settings made on a connection to Windows Management Instrumentation (WMI), or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="c6ddb-107">如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。</span><span class="sxs-lookup"><span data-stu-id="c6ddb-107">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

> [!Note]  
> <span data-ttu-id="c6ddb-108">將 [**SWbemObject**](swbemobject.md)物件的 [**安全性 \_** ] 屬性設定為 **Null** ，會將無限存取權授與所有人。</span><span class="sxs-lookup"><span data-stu-id="c6ddb-108">Setting the **Security\_** property of an [**SWbemObject**](swbemobject.md) object to **NULL** grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="c6ddb-109">如需詳細資訊，請參閱 [**SWbemSecurity**](swbemsecurity.md)。</span><span class="sxs-lookup"><span data-stu-id="c6ddb-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="c6ddb-110">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="c6ddb-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c6ddb-111">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c6ddb-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ddb-112">語法</span><span class="sxs-lookup"><span data-stu-id="c6ddb-112">Syntax</span></span>


```VB
SWbemObject.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="c6ddb-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="c6ddb-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="c6ddb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6ddb-114">Requirements</span></span>



| <span data-ttu-id="c6ddb-115">需求</span><span class="sxs-lookup"><span data-stu-id="c6ddb-115">Requirement</span></span> | <span data-ttu-id="c6ddb-116">值</span><span class="sxs-lookup"><span data-stu-id="c6ddb-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ddb-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6ddb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ddb-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6ddb-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6ddb-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6ddb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ddb-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6ddb-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6ddb-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c6ddb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6ddb-122"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6ddb-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6ddb-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c6ddb-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c6ddb-124"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c6ddb-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c6ddb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c6ddb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6ddb-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6ddb-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c6ddb-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="c6ddb-127">CLSID</span></span><br/>                    | <span data-ttu-id="c6ddb-128">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="c6ddb-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="c6ddb-129">IID</span><span class="sxs-lookup"><span data-stu-id="c6ddb-129">IID</span></span><br/>                      | <span data-ttu-id="c6ddb-130">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="c6ddb-130">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="c6ddb-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6ddb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ddb-132">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="c6ddb-132">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="c6ddb-133">建立 WMI 應用程式或腳本</span><span class="sxs-lookup"><span data-stu-id="c6ddb-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="c6ddb-134">設定用戶端 \_ 應用程式 \_ 處理安全性</span><span class="sxs-lookup"><span data-stu-id="c6ddb-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="c6ddb-135">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="c6ddb-135">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="c6ddb-136">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="c6ddb-136">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="c6ddb-137">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="c6ddb-137">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="c6ddb-138">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="c6ddb-138">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="c6ddb-139">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="c6ddb-139">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




