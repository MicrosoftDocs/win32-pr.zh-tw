---
title: 資源 URI
description: 資源 URI 是管理作業的相異類型識別碼，或管理服務用來執行 WS-Management 通訊協定的值。
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507931"
---
# <a name="resource-uris"></a><span data-ttu-id="c7e27-103">資源 URI</span><span class="sxs-lookup"><span data-stu-id="c7e27-103">Resource URIs</span></span>

<span data-ttu-id="c7e27-104">[*資源 URI*](windows-remote-management-glossary.md)是管理作業的相異類型識別碼，或管理服務用來執行 WS-Management 通訊協定的值。</span><span class="sxs-lookup"><span data-stu-id="c7e27-104">A [*resource URI*](windows-remote-management-glossary.md) is an identifier for a distinct type of management operation or value used by management services that implement the WS-Management protocol.</span></span> <span data-ttu-id="c7e27-105">管理值可能是電腦內的溫度。</span><span class="sxs-lookup"><span data-stu-id="c7e27-105">A management value could be the temperature inside a computer.</span></span> <span data-ttu-id="c7e27-106">管理作業的範例是啟動已停止的服務或設定磁片區使用者配額。</span><span class="sxs-lookup"><span data-stu-id="c7e27-106">An example of a management operation is starting a stopped service or setting a disk volume user quota.</span></span>

## <a name="resource-uri-format"></a><span data-ttu-id="c7e27-107">資源 URI 格式</span><span class="sxs-lookup"><span data-stu-id="c7e27-107">Resource URI Format</span></span>

<span data-ttu-id="c7e27-108">URI 是由前置詞和資源路徑所組成，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="c7e27-108">A URI consists of a prefix and a path to a resource as is shown in the following example:</span></span>

<span data-ttu-id="c7e27-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span><span class="sxs-lookup"><span data-stu-id="c7e27-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span></span>

<span data-ttu-id="c7e27-110">此架構規格指出 URI 是以正式 WS-Management 通訊協定的第1版為基礎，而且資源是 WMI 儲存機制的「根 cimv2」命名空間中的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) \\ 。</span><span class="sxs-lookup"><span data-stu-id="c7e27-110">This schema specification indicates that the URI is based on version 1 of the official WS-Management protocol and that the resource is a [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in the "root\\cimv2" namespace of the WMI repository.</span></span> <span data-ttu-id="c7e27-111">URI 首碼包含架構規格，例如 "schemas.microsoft.com/wbem/wsman/1/wmi" 和特定類型的資源，例如 **Win32 \_ LogicalDisk**。</span><span class="sxs-lookup"><span data-stu-id="c7e27-111">URI prefixes contain a schema specification, such as "schemas.microsoft.com/wbem/wsman/1/wmi" and a specific type of resource, such as **Win32\_LogicalDisk**.</span></span> <span data-ttu-id="c7e27-112">如需識別 WMI 類別之特定實例的詳細資訊，請參閱 [Windows 遠端管理和 wmi](windows-remote-management-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="c7e27-112">For more information about identifying a specific instance of a WMI class, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="c7e27-113">如需詳細資訊，請參閱 [URI 首碼](uri-prefixes.md)。</span><span class="sxs-lookup"><span data-stu-id="c7e27-113">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

## <a name="types-of-resource-uris"></a><span data-ttu-id="c7e27-114">資源 Uri 的類型</span><span class="sxs-lookup"><span data-stu-id="c7e27-114">Types of Resource URIs</span></span>

<span data-ttu-id="c7e27-115">雖然 [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) 是 Windows 作業系統之管理資料的主要來源，但也存在其他的管理架構來源。</span><span class="sxs-lookup"><span data-stu-id="c7e27-115">While [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) is the primary source of management data for Windows-based operating systems, other sources of management schema also exist.</span></span>

<span data-ttu-id="c7e27-116">下列清單描述 Windows 遠端管理所使用的幾種資源 Uri 類型：</span><span class="sxs-lookup"><span data-stu-id="c7e27-116">The following list describes several types of resource URIs used by Windows Remote Management:</span></span>

-   <span data-ttu-id="c7e27-117">WMI Uri</span><span class="sxs-lookup"><span data-stu-id="c7e27-117">WMI URIs</span></span>

    <span data-ttu-id="c7e27-118">這組 Uri 代表 [*通用訊息模型*](/windows/desktop/WmiSdk/gloss-c) 類別路徑，其中包含命名空間和類別。</span><span class="sxs-lookup"><span data-stu-id="c7e27-118">This group of URIs represent a [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) class path which includes namespace and class.</span></span>

    <span data-ttu-id="c7e27-119">WMI Uri 可用於：</span><span class="sxs-lookup"><span data-stu-id="c7e27-119">WMI URIs can be used in:</span></span>

    -   <span data-ttu-id="c7e27-120">[**會話**](session.md) 方法</span><span class="sxs-lookup"><span data-stu-id="c7e27-120">[**Session**](session.md) methods</span></span>
    -   <span data-ttu-id="c7e27-121">[**Iwsmansession.invoke**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) 方法</span><span class="sxs-lookup"><span data-stu-id="c7e27-121">[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) methods</span></span>
    -   <span data-ttu-id="c7e27-122">[**WSMan. CreateResourceLocator**](wsman-createresourcelocator.md) 或 [**IWSMan. CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator) 方法</span><span class="sxs-lookup"><span data-stu-id="c7e27-122">[**WSMan.CreateResourceLocator**](wsman-createresourcelocator.md) or [**IWSMan.CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator) methods</span></span>
    -   <span data-ttu-id="c7e27-123">[**ResourceLocator**](resourcelocator.md) 或 [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) 方法</span><span class="sxs-lookup"><span data-stu-id="c7e27-123">[**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) methods</span></span>

-   <span data-ttu-id="c7e27-124">IPMI Uri</span><span class="sxs-lookup"><span data-stu-id="c7e27-124">IPMI URIs</span></span>

    <span data-ttu-id="c7e27-125">這組 Uri 代表以 CIM 2.9 版為基礎的產業標準 Uri。</span><span class="sxs-lookup"><span data-stu-id="c7e27-125">This group of URIs represent industry standard URIs based upon CIM version 2.9.</span></span> <span data-ttu-id="c7e27-126">IPMI Uri 可以在 [**會話**](session.md) 方法中使用 [**Get**](session-get.md)、 [**Put**](session-put.md)、 [**列舉**](session-enumerate.md) 和 [**Invoke**](session-invoke.md)。</span><span class="sxs-lookup"><span data-stu-id="c7e27-126">IPMI URIs can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) , and [**Invoke**](session-invoke.md).</span></span>

    <span data-ttu-id="c7e27-127">例如 https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd。</span><span class="sxs-lookup"><span data-stu-id="c7e27-127">An example is https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span></span> <span data-ttu-id="c7e27-128">此資源是根據 [DMTF.org](https://www.dmtf.org/home) CIM 架構來定義。</span><span class="sxs-lookup"><span data-stu-id="c7e27-128">This resource is defined according to the [DMTF.org](https://www.dmtf.org/home) CIM schema.</span></span>

-   <span data-ttu-id="c7e27-129">WinRM 設定 Uri</span><span class="sxs-lookup"><span data-stu-id="c7e27-129">WinRM configuration URIs</span></span>

    <span data-ttu-id="c7e27-130">這組 Uri [*是 WinRM 接聽*](windows-remote-management-glossary.md) 程式設定的設定作業。</span><span class="sxs-lookup"><span data-stu-id="c7e27-130">This group of URIs are configuration operations for the WinRM [*listener*](windows-remote-management-glossary.md) configuration.</span></span>

    <span data-ttu-id="c7e27-131"> https://schemas.microsoft.com/wbem/wsman/1/config/listener 可以在 [**會話**](session.md) 方法中使用 [**Get**](session-get.md)、 [**Put**](session-put.md)、 [**Create**](session-create.md)、 [**Delete**](session-delete.md)和 [**列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="c7e27-131">https://schemas.microsoft.com/wbem/wsman/1/config/listener can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md), and [**Enumerate**](session-enumerate.md).</span></span>

-   <span data-ttu-id="c7e27-132">[*系統事件記錄*](windows-remote-management-glossary.md) 檔 () URI 的選取專案</span><span class="sxs-lookup"><span data-stu-id="c7e27-132">[*System Event Log*](windows-remote-management-glossary.md) (SEL) URIs</span></span>

    <span data-ttu-id="c7e27-133">這組 Uri 會訂閱來自 BMC 的事件收集器事件。</span><span class="sxs-lookup"><span data-stu-id="c7e27-133">This group of URIs subscribes to Event Collector events from the BMC.</span></span> <span data-ttu-id="c7e27-134">您可以使用 **Wevtutil** 命令列工具來訂閱這些事件。</span><span class="sxs-lookup"><span data-stu-id="c7e27-134">You can subscribe to these events using the **Wevtutil** command-line tool.</span></span> <span data-ttu-id="c7e27-135">如需詳細資訊，請參閱https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel。</span><span class="sxs-lookup"><span data-stu-id="c7e27-135">For more information, see https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span></span>

## <a name="case-sensitivity"></a><span data-ttu-id="c7e27-136">區分大小寫</span><span class="sxs-lookup"><span data-stu-id="c7e27-136">Case Sensitivity</span></span>

<span data-ttu-id="c7e27-137">[*WMI 外掛程式*](windows-remote-management-glossary.md)會保留在要求中收到的資源 URI 大小寫。</span><span class="sxs-lookup"><span data-stu-id="c7e27-137">The [*WMI plug-in*](windows-remote-management-glossary.md) preserves the case of the resource URI received in a request.</span></span> <span data-ttu-id="c7e27-138">不過，為了確保與其他 WS-Management 通訊協定的執行互通性，請在資源 URI 中針對要求的資源使用正確的大小寫。</span><span class="sxs-lookup"><span data-stu-id="c7e27-138">However, to ensure interoperability with other implementations of WS-Management protocol, use the correct case for the requested resource in resource URI.</span></span> <span data-ttu-id="c7e27-139">正確的大小寫是資源提供者所定義的拼寫。</span><span class="sxs-lookup"><span data-stu-id="c7e27-139">The correct case is the spelling defined by the resource provider.</span></span>

<span data-ttu-id="c7e27-140">雖然資源 Uri 不需要區分大小寫，但 [*片段*](windows-remote-management-glossary.md) XML 會有。</span><span class="sxs-lookup"><span data-stu-id="c7e27-140">While resource URIs do not require case-sensitivity, [*fragment*](windows-remote-management-glossary.md) XML does.</span></span> <span data-ttu-id="c7e27-141">片段只會指定一個屬性，而不會指定資源的整個屬性集。</span><span class="sxs-lookup"><span data-stu-id="c7e27-141">A fragment specifies just one property, rather than the entire set of properties for a resource.</span></span> <span data-ttu-id="c7e27-142">在 WMI 資源的案例中，片段語法會從資源實例取得一個屬性。</span><span class="sxs-lookup"><span data-stu-id="c7e27-142">In the case of WMI resources, fragment syntax gets one property from a resource instance.</span></span> <span data-ttu-id="c7e27-143">例如，從 [**Win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)取得 **版本** 屬性需要使用片段。</span><span class="sxs-lookup"><span data-stu-id="c7e27-143">For example, getting only the **Version** property from [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requires using a fragment.</span></span> <span data-ttu-id="c7e27-144">如需片段的詳細資訊，請參閱 [Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md)中的「將選取器新增至 ResourceLocator 或 IWSManResourceLocator 物件」。</span><span class="sxs-lookup"><span data-stu-id="c7e27-144">For more information about fragments, see "Adding a selector to a ResourceLocator or IWSManResourceLocator object" in [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="c7e27-145">依照 XML 和 [*XPath*](windows-remote-management-glossary.md) 標準， [*WMI 外掛程式*](windows-remote-management-glossary.md) 會針對定義方法之輸入參數的片段和 XML 強制區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c7e27-145">Following XML and [*XPath*](windows-remote-management-glossary.md) standards, the [*WMI plug-in*](windows-remote-management-glossary.md) enforces case-sensitivity for fragments and XML that defines the input parameters for a method.</span></span> <span data-ttu-id="c7e27-146">必須區分大小寫，才能支援 XPath 1.0/層級1標準。</span><span class="sxs-lookup"><span data-stu-id="c7e27-146">Case-sensitivity is required to support the XPath 1.0/Level 1 standard.</span></span> <span data-ttu-id="c7e27-147">若要透過 WinRM 取得 WMI 資料，區分大小寫表示 WMI 類別、屬性和方法的名稱必須符合 WMI 儲存機制中找到之名稱的大小寫。</span><span class="sxs-lookup"><span data-stu-id="c7e27-147">To get WMI data through WinRM, case-sensitivity means that the names of WMI classes, properties, and methods must match the case of the name found in the WMI repository.</span></span>

<span data-ttu-id="c7e27-148">如需詳細資訊，請參閱 [XPath 語法](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="c7e27-148">For more information, see [XPath Syntax](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span></span>

## <a name="case-sensitivity-examples"></a><span data-ttu-id="c7e27-149">區分大小寫範例</span><span class="sxs-lookup"><span data-stu-id="c7e27-149">Case Sensitivity Examples</span></span>

<span data-ttu-id="c7e27-150">例如，從 WMI [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)類別的實例取得 **安全 \_ 描述項** 屬性的腳本，不能使用大寫作為片段路徑中的名稱，只使用 URI。</span><span class="sxs-lookup"><span data-stu-id="c7e27-150">For example, a script that obtains the **SECURITY\_DESCRIPTOR** property from an instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class cannot use upper-case for the names in the fragment path, only the URI.</span></span> <span data-ttu-id="c7e27-151">WinRM [*WMI 外掛程式*](windows-remote-management-glossary.md) 會傳回下列 VBScript 範例的錯誤，因為提供給 **FRAGMENTPATH** 的 XPath XML 未使用正確的大小寫。</span><span class="sxs-lookup"><span data-stu-id="c7e27-151">The WinRM [*WMI plug-in*](windows-remote-management-glossary.md) returns an error for the following VBScript example because the XPath XML supplied for the **FragmentPath** does not use the correct case.</span></span> <span data-ttu-id="c7e27-152">在 WMI 儲存機制中，類別的拼寫為「Win32 \_ 服務」。</span><span class="sxs-lookup"><span data-stu-id="c7e27-152">In the WMI repository, the class is spelled "Win32\_Service".</span></span>


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



<span data-ttu-id="c7e27-153">下列版本的相同範例顯示 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 類別和 **安全 \_ 描述項** 屬性的正確用法。</span><span class="sxs-lookup"><span data-stu-id="c7e27-153">The following version of the same example shows the correct use of case for the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class and **SECURITY\_DESCRIPTOR** property.</span></span>


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a><span data-ttu-id="c7e27-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7e27-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7e27-155">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="c7e27-155">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="c7e27-156">遠端硬體管理</span><span class="sxs-lookup"><span data-stu-id="c7e27-156">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> <dt>

[<span data-ttu-id="c7e27-157">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="c7e27-157">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 