---
description: '\_Wbemscripting.swbemlocator 物件的 security 屬性是用來讀取或設定 wbemscripting.swbemlocator 物件的安全性設定。 這個屬性是 SWbemSecurity 物件。'
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: 'SWbemLocator.Security_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692191"
---
# <a name="swbemlocatorsecurity_-property"></a><span data-ttu-id="ab0e8-104">Wbemscripting.swbemlocator 安全性 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="ab0e8-104">SWbemLocator.Security\_ property</span></span>

<span data-ttu-id="ab0e8-105">[**Wbemscripting.swbemlocator**](swbemlocator.md)物件的 **security \_** 屬性是用來讀取或設定 **wbemscripting.swbemlocator** 物件的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="ab0e8-105">The **Security\_** property of the [**SWbemLocator**](swbemlocator.md) object is used to read or set the security settings for an **SWbemLocator** object.</span></span> <span data-ttu-id="ab0e8-106">這個屬性是 [**SWbemSecurity**](swbemsecurity.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ab0e8-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="ab0e8-107">將 [**wbemscripting.swbemlocator**](swbemlocator.md)物件的 [**安全性 \_** ] 屬性設定為 **Null** ，會將無限存取權授與所有人。</span><span class="sxs-lookup"><span data-stu-id="ab0e8-107">Setting the **Security\_** property of an [**SWbemLocator**](swbemlocator.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="ab0e8-108">如需詳細資訊，請參閱 [**SWbemSecurity**](swbemsecurity.md)。</span><span class="sxs-lookup"><span data-stu-id="ab0e8-108">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="ab0e8-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="ab0e8-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="ab0e8-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ab0e8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab0e8-111">語法</span><span class="sxs-lookup"><span data-stu-id="ab0e8-111">Syntax</span></span>


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="ab0e8-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="ab0e8-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="ab0e8-113">備註</span><span class="sxs-lookup"><span data-stu-id="ab0e8-113">Remarks</span></span>

<span data-ttu-id="ab0e8-114">**Wbemscripting.swbemlocator 安全性 \_** 物件的屬性沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="ab0e8-114">The properties of an **SWbemLocator.Security\_** object have no default values.</span></span> <span data-ttu-id="ab0e8-115">如果您在設定 [**wbemscripting.swbemlocator**](swbemlocator.md)物件之前嘗試取得 [**SWbemSecurity. AuthenticationLevel**](swbemsecurity-authenticationlevel.md)或 [**SWbemSecurity**](swbemsecurity-impersonationlevel.md)的值，就會產生 [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)錯誤結果。</span><span class="sxs-lookup"><span data-stu-id="ab0e8-115">If you attempt to get the value of [**SWbemSecurity.AuthenticationLevel**](swbemsecurity-authenticationlevel.md) or [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on an [**SWbemLocator**](swbemlocator.md) object before you have set it, an [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) error results.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab0e8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab0e8-116">Requirements</span></span>



| <span data-ttu-id="ab0e8-117">需求</span><span class="sxs-lookup"><span data-stu-id="ab0e8-117">Requirement</span></span> | <span data-ttu-id="ab0e8-118">值</span><span class="sxs-lookup"><span data-stu-id="ab0e8-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0e8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab0e8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab0e8-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab0e8-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab0e8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab0e8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab0e8-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab0e8-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab0e8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ab0e8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab0e8-124"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab0e8-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab0e8-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ab0e8-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="ab0e8-126"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ab0e8-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ab0e8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ab0e8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab0e8-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab0e8-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ab0e8-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="ab0e8-129">CLSID</span></span><br/>                    | <span data-ttu-id="ab0e8-130">CLSID \_ wbemscripting.swbemlocator</span><span class="sxs-lookup"><span data-stu-id="ab0e8-130">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="ab0e8-131">IID</span><span class="sxs-lookup"><span data-stu-id="ab0e8-131">IID</span></span><br/>                      | <span data-ttu-id="ab0e8-132">IID \_ ISWbemLocator</span><span class="sxs-lookup"><span data-stu-id="ab0e8-132">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="ab0e8-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab0e8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab0e8-134">**Wbemscripting.swbemlocator**</span><span class="sxs-lookup"><span data-stu-id="ab0e8-134">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="ab0e8-135">建立 WMI 應用程式或腳本</span><span class="sxs-lookup"><span data-stu-id="ab0e8-135">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="ab0e8-136">使用 VBScript 執行特殊許可權作業</span><span class="sxs-lookup"><span data-stu-id="ab0e8-136">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="ab0e8-137">設定用戶端 \_ 應用程式 \_ 處理安全性</span><span class="sxs-lookup"><span data-stu-id="ab0e8-137">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="ab0e8-138">**SWbemSecurity 物件**</span><span class="sxs-lookup"><span data-stu-id="ab0e8-138">**SWbemSecurity object**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="ab0e8-139">保護遠端 WMI 連接</span><span class="sxs-lookup"><span data-stu-id="ab0e8-139">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




