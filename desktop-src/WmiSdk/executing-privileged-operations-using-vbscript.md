---
description: 如果您使用適用于 WMI 的腳本 API，您可以設定特定的安全性許可權。
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: 使用 VBScript 執行特殊許可權作業
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115860"
---
# <a name="executing-privileged-operations-using-vbscript"></a><span data-ttu-id="076fa-103">使用 VBScript 執行特殊許可權作業</span><span class="sxs-lookup"><span data-stu-id="076fa-103">Executing Privileged Operations Using VBScript</span></span>

<span data-ttu-id="076fa-104">如果您使用適用于 WMI 的腳本 API，您可以設定特定的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="076fa-104">If you use the scripting API for WMI, you can set specific security privileges.</span></span> <span data-ttu-id="076fa-105">例如，您可以設定安全性許可權來要求作業系統關機，或是檢查安全性事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="076fa-105">For example, you can set the security privileges to request an operating system shutdown, or to examine the security event log.</span></span> <span data-ttu-id="076fa-106">如需詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。</span><span class="sxs-lookup"><span data-stu-id="076fa-106">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="076fa-107">當您在電腦上存取 WMI 時，只需要設定許可權。</span><span class="sxs-lookup"><span data-stu-id="076fa-107">You only need to set privileges when you are accessing WMI on your computer.</span></span> <span data-ttu-id="076fa-108">當您存取遠端主機時，COM RPC 會自動設定許可權。</span><span class="sxs-lookup"><span data-stu-id="076fa-108">When you are accessing a remote host, COM RPC automatically sets the privileges.</span></span> <span data-ttu-id="076fa-109">若要判斷所有必要的許可權，請參閱您要存取的特定 WMI 類別的檔，例如 [**Win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)。</span><span class="sxs-lookup"><span data-stu-id="076fa-109">To determine all the required privileges, consult the documentation for the specific WMI classes that you want to access, such as [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span> <span data-ttu-id="076fa-110">如需詳細資訊，請參閱 [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="076fa-110">For more information, see [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>

<span data-ttu-id="076fa-111">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="076fa-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="076fa-112">從安全性物件設定許可權 \_</span><span class="sxs-lookup"><span data-stu-id="076fa-112">Setting a Privilege from the Security\_ Object</span></span>](/windows)
-   [<span data-ttu-id="076fa-113">將許可權設定為標記的一部分</span><span class="sxs-lookup"><span data-stu-id="076fa-113">Setting a Privilege as Part of a Moniker</span></span>](#setting-a-privilege-as-part-of-a-moniker)
-   [<span data-ttu-id="076fa-114">撤銷和重設許可權</span><span class="sxs-lookup"><span data-stu-id="076fa-114">Revoking and Resetting Privileges</span></span>](#revoking-and-resetting-privileges)
-   [<span data-ttu-id="076fa-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="076fa-115">Related topics</span></span>](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a><span data-ttu-id="076fa-116">從安全性物件設定許可權 \_</span><span class="sxs-lookup"><span data-stu-id="076fa-116">Setting a Privilege from the Security\_ Object</span></span>

<span data-ttu-id="076fa-117">使用下列程式，在 Visual Basic 中設定安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="076fa-117">Use the following procedure to set security privileges in Visual Basic.</span></span>

<span data-ttu-id="076fa-118">**若要在 Visual Basic 中設定許可權**</span><span class="sxs-lookup"><span data-stu-id="076fa-118">**To set privileges in Visual Basic**</span></span>

1.  <span data-ttu-id="076fa-119">建立 [**wbemscripting.swbemlocator**](swbemlocator.md)類型的物件。</span><span class="sxs-lookup"><span data-stu-id="076fa-119">Create an object of type [**SWbemLocator**](swbemlocator.md).</span></span>
2.  <span data-ttu-id="076fa-120">將新的許可權新增至 [**wbemscripting.swbemlocator. Security \_**](swbemlocator-security-.md)物件。</span><span class="sxs-lookup"><span data-stu-id="076fa-120">Add the new privilege to the [**SWbemLocator.Security\_**](swbemlocator-security-.md) object.</span></span>

    <span data-ttu-id="076fa-121">[**安全性 \_**](swbemlocator-security-.md)物件包含 [**swbemobjectset 搭配使用**](swbemobjectset.md)集合。</span><span class="sxs-lookup"><span data-stu-id="076fa-121">The [**Security\_**](swbemlocator-security-.md) object contains an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="076fa-122">集合中的物件是 [**SWbemSecurity**](swbemsecurity.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="076fa-122">The objects in the set are [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="076fa-123">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="076fa-123">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

3.  <span data-ttu-id="076fa-124">登入 WMI 並取出 [**SWbemServices**](swbemservices.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="076fa-124">Log on to WMI and retrieve an [**SWbemServices**](swbemservices.md) object.</span></span>

    <span data-ttu-id="076fa-125">[**SWbemServices**](swbemservices.md)物件會繼承在上一個步驟中設定的許可權。</span><span class="sxs-lookup"><span data-stu-id="076fa-125">The [**SWbemServices**](swbemservices.md) object inherits the privilege that is set in the previous step.</span></span>

<span data-ttu-id="076fa-126">您也可以使用 [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) 方法來設定許可權。</span><span class="sxs-lookup"><span data-stu-id="076fa-126">You can also set a privilege using the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method.</span></span>

## <a name="setting-a-privilege-as-part-of-a-moniker"></a><span data-ttu-id="076fa-127">將許可權設定為標記的一部分</span><span class="sxs-lookup"><span data-stu-id="076fa-127">Setting a Privilege as Part of a Moniker</span></span>

<span data-ttu-id="076fa-128">您可以將許可權設定為「標記」的一部分。</span><span class="sxs-lookup"><span data-stu-id="076fa-128">You can set a privilege as part of a moniker.</span></span>

<span data-ttu-id="076fa-129">下列範例示範如何將 debug 許可權加入至標記。</span><span class="sxs-lookup"><span data-stu-id="076fa-129">The following example shows you how to add a debug privilege to a moniker.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a><span data-ttu-id="076fa-130">撤銷和重設許可權</span><span class="sxs-lookup"><span data-stu-id="076fa-130">Revoking and Resetting Privileges</span></span>

<span data-ttu-id="076fa-131">下列範例會示範如何設定 **SeDebugPrivilege** 許可權，以及撤銷 **SeRemoteShutdownPrivilege** 許可權。</span><span class="sxs-lookup"><span data-stu-id="076fa-131">The following example shows you how to set the **SeDebugPrivilege** privilege, and revoke the **SeRemoteShutdownPrivilege** privilege.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a><span data-ttu-id="076fa-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="076fa-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="076fa-133">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="076fa-133">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="076fa-134">執行具有特殊許可權的作業</span><span class="sxs-lookup"><span data-stu-id="076fa-134">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> </dl>

 

 
