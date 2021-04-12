---
description: 許可權屬性是 SWbemPrivilegeSet 物件。 這個屬性是用來啟用或停用特定的 Windows 許可權。 您可能需要使用 Windows Management Instrumentation (WMI) API 來設定這些許可權的其中之一，以執行特定工作。
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: SWbemSecurity) 的許可權屬性 (>wbemdisp.tlb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192053"
---
# <a name="swbemsecurityprivileges-property"></a><span data-ttu-id="ff430-105">SWbemSecurity 許可權屬性</span><span class="sxs-lookup"><span data-stu-id="ff430-105">SWbemSecurity.Privileges property</span></span>

<span data-ttu-id="ff430-106">**許可權** 屬性是 [**SWbemPrivilegeSet**](swbemprivilegeset.md)物件。</span><span class="sxs-lookup"><span data-stu-id="ff430-106">The **Privileges** property is an [**SWbemPrivilegeSet**](swbemprivilegeset.md) object.</span></span> <span data-ttu-id="ff430-107">這個屬性是用來啟用或停用特定的 Windows 許可權。</span><span class="sxs-lookup"><span data-stu-id="ff430-107">This property is used to enable or disable specific Windows privileges.</span></span> <span data-ttu-id="ff430-108">您可能需要使用 Windows Management Instrumentation (WMI) API 來設定這些許可權的其中之一，以執行特定工作。</span><span class="sxs-lookup"><span data-stu-id="ff430-108">You may need to set one of these privileges to perform specific tasks using the Windows Management Instrumentation (WMI) API.</span></span>

<span data-ttu-id="ff430-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="ff430-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="ff430-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ff430-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff430-111">語法</span><span class="sxs-lookup"><span data-stu-id="ff430-111">Syntax</span></span>


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a><span data-ttu-id="ff430-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="ff430-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="ff430-113">備註</span><span class="sxs-lookup"><span data-stu-id="ff430-113">Remarks</span></span>

<span data-ttu-id="ff430-114">這項設定可讓您授與或撤銷許可權，作為 WMI 標記字串的一部分。</span><span class="sxs-lookup"><span data-stu-id="ff430-114">This setting allows you to grant or revoke privileges as part of a WMI moniker string.</span></span> <span data-ttu-id="ff430-115">如需適用值的完整清單，請參閱 [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) 和 [**許可權常數**](privilege-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="ff430-115">For the complete list of applicable values, see [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) and [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="ff430-116">您可以藉由將 [**wbemscripting.swbemlocator**](swbemprivilege.md)物件新增至 [**許可權**] 屬性，來變更為 [**SWbemServices**](swbemservices.md)、 [**SWbemObject**](swbemobject.md)、 [**swbemobjectset 搭配使用**](swbemobjectset.md)、 [**SWbemObjectPath**](swbemobjectpath.md)和 [**SWbemPrivilege**](swbemlocator.md)物件定義的許可權。</span><span class="sxs-lookup"><span data-stu-id="ff430-116">You can change the privileges defined for the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by adding [**SWbemPrivilege**](swbemprivilege.md) objects to the **Privileges** property.</span></span>

<span data-ttu-id="ff430-117">不同版本的 Windows 如何處理許可權的變更有一些基本差異。</span><span class="sxs-lookup"><span data-stu-id="ff430-117">There are fundamental differences in how different versions of Windows handle changes to privileges.</span></span> <span data-ttu-id="ff430-118">如果您開發的應用程式只用于 Windows 平臺，您可以隨時設定或撤銷許可權。</span><span class="sxs-lookup"><span data-stu-id="ff430-118">If you are developing an application that is only used on Windows platforms, you can set or revoke privileges at any time.</span></span>

<span data-ttu-id="ff430-119">下列範例會在初始的標記連接上設定 **SeDebugPrivilege** ，以取得 [**SWbemServices**](swbemservices.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ff430-119">The following example sets the **SeDebugPrivilege** on the initial moniker connection to obtain an [**SWbemServices**](swbemservices.md) object.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



<span data-ttu-id="ff430-120">如需有關如何針對標記連接格式化安全性字串的詳細資訊，請參閱 [**許可權常數**](privilege-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="ff430-120">For more information about how to format the security string for a moniker connection, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="ff430-121">下列範例會執行相同的工作，但它會在初始登入 WMI 之後設定許可權。</span><span class="sxs-lookup"><span data-stu-id="ff430-121">The following example performs the same task, but it sets the privilege after the initial log on to WMI.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



<span data-ttu-id="ff430-122">請注意，若要呼叫 [**SwbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md)，您必須使用安全性許可權的完整名稱，例如 "SeDebugPrivilege" 而不是 "Debug"。</span><span class="sxs-lookup"><span data-stu-id="ff430-122">Note that for calls to [**SwbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md), you must use the full name of the security privilege, for example, "SeDebugPrivilege" instead of "Debug".</span></span>

## <a name="requirements"></a><span data-ttu-id="ff430-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff430-123">Requirements</span></span>



| <span data-ttu-id="ff430-124">需求</span><span class="sxs-lookup"><span data-stu-id="ff430-124">Requirement</span></span> | <span data-ttu-id="ff430-125">值</span><span class="sxs-lookup"><span data-stu-id="ff430-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff430-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff430-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ff430-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff430-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff430-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff430-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ff430-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff430-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff430-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ff430-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff430-131"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff430-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff430-132">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ff430-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff430-133"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ff430-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ff430-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ff430-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff430-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff430-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff430-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="ff430-136">CLSID</span></span><br/>                    | <span data-ttu-id="ff430-137">CLSID \_ SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="ff430-137">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="ff430-138">IID</span><span class="sxs-lookup"><span data-stu-id="ff430-138">IID</span></span><br/>                      | <span data-ttu-id="ff430-139">IID \_ ISWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="ff430-139">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="ff430-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff430-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff430-141">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="ff430-141">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="ff430-142">執行具有特殊許可權的作業</span><span class="sxs-lookup"><span data-stu-id="ff430-142">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="ff430-143">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="ff430-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> </dl>

 

 




