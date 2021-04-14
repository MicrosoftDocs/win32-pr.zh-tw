---
title: 透過關聯遍歷進行的 DMTF 設定檔探索
description: Windows Management Instrumentation (WMI) 基礎結構的重要元件，是系統中可管理之實體的面向物件模型。
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b3f5883075ddf549330c422efec558195c8fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383074"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a><span data-ttu-id="c5fc9-103">透過關聯遍歷進行的 DMTF 設定檔探索</span><span class="sxs-lookup"><span data-stu-id="c5fc9-103">DMTF Profile Discovery Through Association Traversal</span></span>

<span data-ttu-id="c5fc9-104">Windows Management Instrumentation (WMI) 基礎結構的重要元件，是系統中可管理之實體的面向物件模型。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="c5fc9-105">此模型符合桌面管理工作強制 ([DMTF](https://www.dmtf.org/standards/wsman)) 所維護的標準，也稱為通用訊息模型 (CIM) 。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="c5fc9-106">模型中的某些類別，例如 [CIM \_ 資料檔案](../cimwin32prov/cim-datafile.md) 或 [Win32 \_ 進程](../cimwin32prov/win32-process.md)，會直接對應至可管理的實體。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-106">Some classes in the model, such as [CIM\_DataFile](../cimwin32prov/cim-datafile.md) or [Win32\_Process](../cimwin32prov/win32-process.md), correspond directly to manageable entities.</span></span> <span data-ttu-id="c5fc9-107">模型中的其他類別（例如 [Win32 \_ SystemServices](../cimwin32prov/win32-systemservices.md)）表示可管理實體之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-107">Other classes in the model, such as [Win32\_SystemServices](../cimwin32prov/win32-systemservices.md), represent relationships between manageable entities.</span></span> <span data-ttu-id="c5fc9-108">這些關聯性模型類別稱為「關聯類別」（Association class）。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-108">These relationship-modeling classes are known as Association classes.</span></span>

<span data-ttu-id="c5fc9-109">您可以使用 WMI 特定的查詢語言（WQL）來取出類別的實例，這些實例代表可管理的實體或關聯類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-109">Using the WMI-specific query language, WQL, you can retrieve instances of classes that represent manageable entities or instances of Association classes.</span></span> <span data-ttu-id="c5fc9-110">但是 WQL 是特定的實作為。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-110">But WQL is implementation specific.</span></span> <span data-ttu-id="c5fc9-111">它只適用于 Windows 對 DMTF 標準 (WMI) 的執行。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-111">It works only with the Windows implementation of the DMTF standard (WMI).</span></span> <span data-ttu-id="c5fc9-112">此外，用於抓取關聯類別的 WQL 語法相當複雜。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-112">In addition, the WQL syntax for retrieving Association classes is rather complicated.</span></span>

<span data-ttu-id="c5fc9-113">Windows 遠端管理 (WinRM) 基礎結構可提供絕佳的方法來利用 WMI 的功能。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-113">The Windows Remote Management (WinRM) infrastructure provides an excellent way to leverage the functionality of WMI.</span></span> <span data-ttu-id="c5fc9-114">舊版 WinRM 必須使用 WQL 來取出關聯類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-114">Early versions of WinRM had to use WQL to retrieve instances of Association classes.</span></span> <span data-ttu-id="c5fc9-115">WinRM 2.0 包含透過關聯進行的新功能，稱為「DMTF 設定檔探索」。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-115">WinRM 2.0 includes a new feature known as DMTF profile discovery through association traversal.</span></span> <span data-ttu-id="c5fc9-116">關聯性的「關聯」（association）可讓 WinRM 的使用者使用「DMTF CIM」系結規格中定義的標準篩選機制（AssociationFilter 方言）來取出關聯類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-116">Association traversal enables a user of WinRM to retrieve instances of Association classes by using a standard filtering mechanism, the AssociationFilter dialect, defined in the DMTF CIM binding specification.</span></span> <span data-ttu-id="c5fc9-117">如需有關關聯遍歷的詳細資訊，請參閱 WS-Management CIM 系結規格 ([https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man)) 。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-117">For more information on association traversal, see the WS-Management CIM Binding specification ([https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man)).</span></span>

<span data-ttu-id="c5fc9-118">Winrm 公用程式提供一種簡單的機制，可透過適當的關聯並取出裝置設定檔。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-118">The winrm utility provides a simple mechanism to traverse through the appropriate association and retrieve a device profile.</span></span>

## <a name="configuration-implementation-details"></a><span data-ttu-id="c5fc9-119">設定執行詳細資料</span><span class="sxs-lookup"><span data-stu-id="c5fc9-119">Configuration Implementation Details</span></span>

<span data-ttu-id="c5fc9-120">Winrm 公用程式現在支援關聯要求的方言。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-120">The winrm utility now supports a dialect for the association request.</span></span> <span data-ttu-id="c5fc9-121">您可以使用 winrm 公用程式來指定 URI 或別名。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-121">Either the URI or the alias can be specified using the winrm utility.</span></span>



| <span data-ttu-id="c5fc9-122">Alias</span><span class="sxs-lookup"><span data-stu-id="c5fc9-122">Alias</span></span>       | <span data-ttu-id="c5fc9-123">URI</span><span class="sxs-lookup"><span data-stu-id="c5fc9-123">URI</span></span>                                                               |
|-------------|-------------------------------------------------------------------|
| <span data-ttu-id="c5fc9-124">關聯</span><span class="sxs-lookup"><span data-stu-id="c5fc9-124">association</span></span> | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="c5fc9-125">使用 AssociationFilter 方言來抓取關聯類別的實例</span><span class="sxs-lookup"><span data-stu-id="c5fc9-125">Retrieving Instances of an Association Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="c5fc9-126">Winrm 公用程式可以取出特定來源實例的 WMI 關聯類別實例。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-126">The winrm utility can retrieve WMI association class instances of a particular source instance.</span></span> <span data-ttu-id="c5fc9-127">下列命令示範如何使用 winrm 公用程式來取出 [Win32 \_ 服務](../cimwin32prov/win32-service.md) 關聯類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-127">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) association classes.</span></span> <span data-ttu-id="c5fc9-128">參數「-關聯」必須用來傳回關聯類別。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-128">The switch "-associations" must be used to return association classes.</span></span>

<span data-ttu-id="c5fc9-129">**winrm 列舉 wmicimv2/ \* -方言：關聯-關聯-篩選： {object = win32 \_ service？ name = winrm; resultclassname = win32 \_ dependentservice; role = 相依}**</span><span class="sxs-lookup"><span data-stu-id="c5fc9-129">**winrm enumerate wmicimv2/\* -dialect:association -associations -filter:{object=win32\_service?name=winrm;resultclassname=win32\_dependentservice;role=dependent}**</span></span>

<span data-ttu-id="c5fc9-130">下列以文字為基礎的程式碼片段是上述命令的輸出：</span><span class="sxs-lookup"><span data-stu-id="c5fc9-130">The following text-based snippet is the output of the above command:</span></span>

``` syntax
Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = RpcSs
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null

Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_SystemDriver
            SelectorSet
                Selector: Name = HTTP
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null
```

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="c5fc9-131">使用 AssociationFilter 方言來取出相關類別的實例</span><span class="sxs-lookup"><span data-stu-id="c5fc9-131">Retrieving Instances of an Associated Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="c5fc9-132">Winrm 公用程式可以取出與特定來源實例相關聯的 WMI 類別實例。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-132">The winrm utility can retrieve WMI class instances that are associated with a particular source instance.</span></span> <span data-ttu-id="c5fc9-133">下列命令示範如何使用 winrm 公用程式來取出 [Win32 \_ 服務](../cimwin32prov/win32-service.md) 相關聯類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c5fc9-133">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) associated classes.</span></span>

<span data-ttu-id="c5fc9-134">**winrm 列舉 wmicimv2/ \* -方言：關聯-篩選： {object = win32 \_ service？ name = winrm; associationclassname = win32 \_ dependentservice; resultclassname = win32 \_ service; resultrole = antecedent; role = 相依}**</span><span class="sxs-lookup"><span data-stu-id="c5fc9-134">**winrm enumerate wmicimv2/\* -dialect:association -filter:{object=win32\_service?name=winrm;associationclassname=win32\_dependentservice;resultclassname=win32\_service;resultrole=antecedent;role=dependent}**</span></span>

<span data-ttu-id="c5fc9-135">下列以文字為基礎的程式碼片段是上述命令的輸出：</span><span class="sxs-lookup"><span data-stu-id="c5fc9-135">The following text-based snippet is the output of the above command:</span></span>

``` syntax
Win32_Service
    AcceptPause = false
    AcceptStop = false
    Caption = Remote Procedure Call (RPC)
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = The RPCSS service is the Service Control Manager for COM and DCOM servers. It performs object activations requests, object exporter resolutions and distributed garbage collection for COM and DCOM servers. If this service is stopped or disabled, programs using COM or DCOM will not function properly. It is strongly recommended that you have the RPCSS service running DesktopInteract = false
    DisplayName = Remote Procedure Call (RPC)
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = RpcSs
    PathName = C:\Windows\system32\svchost.exe -k rpcss
    ProcessId = 716
    ServiceSpecificExitCode = 0
    ServiceType = Share Process
    Started = true
    StartMode = Auto
    StartName = NT AUTHORITY\NetworkService
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = myComputer
    TagId = 0
    WaitHint = 0
```

 

 