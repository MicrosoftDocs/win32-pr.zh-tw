---
title: Windows 遠端管理和 WMI
description: Windows 遠端管理可以用來取出 Windows Management Instrumentation 所公開的資料。
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6942e89ea2e63ef809f3452e6ce55a493662c938
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106981764"
---
# <a name="windows-remote-management-and-wmi"></a><span data-ttu-id="3687a-103">Windows 遠端管理和 WMI</span><span class="sxs-lookup"><span data-stu-id="3687a-103">Windows Remote Management and WMI</span></span>

<span data-ttu-id="3687a-104">Windows 遠端管理可以用來取得 Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) 和 [MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)) 所公開的資料。</span><span class="sxs-lookup"><span data-stu-id="3687a-104">Windows Remote Management can be used to retrieve data exposed by Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) and [MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)).</span></span> <span data-ttu-id="3687a-105">您可以使用使用 [Winrm 腳本 API](winrm-scripting-api.md) 的腳本或應用程式，或透過 **winrm** 命令列工具，來取得 WMI 資料。</span><span class="sxs-lookup"><span data-stu-id="3687a-105">You can obtain WMI data with scripts or applications that use the [WinRM Scripting API](winrm-scripting-api.md) or through the **Winrm** command-line tool.</span></span>

<span data-ttu-id="3687a-106">WinRM 支援大部分常見的 WMI 類別和作業，包括內嵌的物件。</span><span class="sxs-lookup"><span data-stu-id="3687a-106">WinRM supports most of the familiar WMI classes and operations, including embedded objects.</span></span> <span data-ttu-id="3687a-107">WinRM 可以利用 WMI 收集 [*資源*](windows-remote-management-glossary.md) 的相關資料，或管理以 Windows 為基礎之作業系統上的資源。</span><span class="sxs-lookup"><span data-stu-id="3687a-107">WinRM can leverage WMI to collect data about [*resources*](windows-remote-management-glossary.md) or to manage resources on a Windows-based operating system.</span></span> <span data-ttu-id="3687a-108">這表示您可以透過現有的 [WMI 類別](/windows/desktop/WmiSdk/wmi-classes)集，取得有關您企業中之物件（例如磁片、網路介面卡、服務或進程）的資料。</span><span class="sxs-lookup"><span data-stu-id="3687a-108">That means that you can obtain data about objects such as disks, network adapters, services, or processes in your enterprise through the existing set of [WMI classes](/windows/desktop/WmiSdk/wmi-classes).</span></span> <span data-ttu-id="3687a-109">您也可以存取標準 WMI [IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)所提供的硬體資料。</span><span class="sxs-lookup"><span data-stu-id="3687a-109">You can also access the hardware data that is available from the standard WMI [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

## <a name="identifying-a-wmi-resource"></a><span data-ttu-id="3687a-110">識別 WMI 資源</span><span class="sxs-lookup"><span data-stu-id="3687a-110">Identifying a WMI Resource</span></span>

<span data-ttu-id="3687a-111">您可以使用 WinRM 中的 [*資源*](windows-remote-management-glossary.md) 或 WS-Management 通訊協定來參考 WMI 類別：受管理的實體類型，例如服務或磁片。</span><span class="sxs-lookup"><span data-stu-id="3687a-111">You can reference a WMI class as a [*resource*](windows-remote-management-glossary.md) in WinRM and in the WS-Management protocol: a type of managed entity, like a service or a disk.</span></span>

<span data-ttu-id="3687a-112">WMI 類別或方法是由 [*URI*](windows-remote-management-glossary.md)所識別，就像使用 WS-Management 通訊協定時的任何其他資源一樣。</span><span class="sxs-lookup"><span data-stu-id="3687a-112">A WMI class or method is identified by a [*URI*](windows-remote-management-glossary.md), just as any other resource is when using the WS-Management protocol.</span></span> <span data-ttu-id="3687a-113">URI 可以指定 WMI 資源 (類別) 、WMI 動作 (方法) ，或是在透過網路傳送的 [*訊息*](windows-remote-management-glossary.md) 中識別類別的特定實例。</span><span class="sxs-lookup"><span data-stu-id="3687a-113">The URI can specify a WMI resource (class), a WMI action (method), or identify a specific instance of a class in [*messages*](windows-remote-management-glossary.md) sent over a network.</span></span> <span data-ttu-id="3687a-114">如需詳細資訊，請參閱 [資源 uri](resource-uris.md)。</span><span class="sxs-lookup"><span data-stu-id="3687a-114">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a><span data-ttu-id="3687a-115">建立 WMI 類別的 URI 前置詞</span><span class="sxs-lookup"><span data-stu-id="3687a-115">Constructing the URI Prefix for WMI Classes</span></span>

<span data-ttu-id="3687a-116">URI 前置詞包含固定部分和 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="3687a-116">The URI prefix contains a fixed part and the WMI namespace.</span></span> <span data-ttu-id="3687a-117">例如，Windows Server 中包含前置詞固定部分的 URI 前置詞為： `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` 。</span><span class="sxs-lookup"><span data-stu-id="3687a-117">For example, the URI prefix in Windows Server that contains the fixed part of the prefix is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>`.</span></span> <span data-ttu-id="3687a-118">這可讓您為任何 WMI 命名空間產生 URI 前置詞。</span><span class="sxs-lookup"><span data-stu-id="3687a-118">This allows the URI prefix to be generated for any WMI namespace.</span></span> <span data-ttu-id="3687a-119">例如，若要存取 **根 \\ 預設** WMI 命名空間，請使用下列 URI 首碼： `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` 。</span><span class="sxs-lookup"><span data-stu-id="3687a-119">For example, to access the **root\\default** WMI namespace, use the following URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/`.</span></span>

<span data-ttu-id="3687a-120">大部分的管理 WMI 類別都是在 **根 \\ cimv2** 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="3687a-120">The majority of the WMI classes for management are in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="3687a-121">若要存取 **根 \\ cimv2** 命名空間中的類別和實例，請使用 URI 首碼： `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` 。</span><span class="sxs-lookup"><span data-stu-id="3687a-121">To access classes and instances in **root\\cimv2** namespace, use the URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`.</span></span> <span data-ttu-id="3687a-122">如需詳細資訊，請參閱 [資源 uri](resource-uris.md)。</span><span class="sxs-lookup"><span data-stu-id="3687a-122">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="generating-a-complete-uri-for-wmi-classes"></a><span data-ttu-id="3687a-123">產生 WMI 類別的完整 URI</span><span class="sxs-lookup"><span data-stu-id="3687a-123">Generating a Complete URI for WMI Classes</span></span>

<span data-ttu-id="3687a-124">您提供給 **Winrm** 命令列工具或腳本的 URI，是由前置詞加上資源規格所組成。</span><span class="sxs-lookup"><span data-stu-id="3687a-124">The URI that you supply, either to the **Winrm** command-line tool or to a script, consists of the prefix plus the resource specification.</span></span>

<span data-ttu-id="3687a-125">下列程式說明如何產生資源 URI，以取得 WMI 類別或在列舉作業中使用。</span><span class="sxs-lookup"><span data-stu-id="3687a-125">The following procedure describes how to generate a resource URI either to get a WMI class or to use in an enumerate operation.</span></span>

<span data-ttu-id="3687a-126">**產生 WMI 類別的資源 URI**</span><span class="sxs-lookup"><span data-stu-id="3687a-126">**To generate a resource URI for a WMI class**</span></span>

1.  <span data-ttu-id="3687a-127">以表示應使用 WS-Management 通訊協定架構的前置詞開頭。</span><span class="sxs-lookup"><span data-stu-id="3687a-127">Start with the prefix that indicates the WS-Management protocol schema should be used.</span></span>

    https://schemas.microsoft.com/wbem/wsman/1

    <span data-ttu-id="3687a-128">WMI 類別的資源 URI 前置詞一律相同。</span><span class="sxs-lookup"><span data-stu-id="3687a-128">The resource URI prefix for WMI classes is always the same.</span></span> <span data-ttu-id="3687a-129">如需詳細資訊，請參閱 [URI 首碼](uri-prefixes.md)。</span><span class="sxs-lookup"><span data-stu-id="3687a-129">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

2.  <span data-ttu-id="3687a-130">將 WMI 命名空間新增至前置詞。</span><span class="sxs-lookup"><span data-stu-id="3687a-130">Add the WMI namespace to the prefix.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  <span data-ttu-id="3687a-131">新增類別名稱。</span><span class="sxs-lookup"><span data-stu-id="3687a-131">Add the class name.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  <span data-ttu-id="3687a-132">若要設定屬性的值，或叫用特定的方法，請為類別新增必要的索引鍵值或值。</span><span class="sxs-lookup"><span data-stu-id="3687a-132">To set the value of a property, or to invoke a specific method, add the required key value or values for the class.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    <span data-ttu-id="3687a-133">如果您將金鑰值保留空白，則不會改變原始的屬性值。</span><span class="sxs-lookup"><span data-stu-id="3687a-133">If you leave the key value blank, you will not alter the original property value.</span></span>

    > [!Note]  
    > <span data-ttu-id="3687a-134">將索引鍵值保留空白會將屬性值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3687a-134">Leaving the key value blank sets the property value to **NULL**.</span></span>

     

## <a name="locating-a-wmi-resource-with-winrm"></a><span data-ttu-id="3687a-135">使用 WinRM 找出 WMI 資源</span><span class="sxs-lookup"><span data-stu-id="3687a-135">Locating a WMI Resource with WinRM</span></span>

<span data-ttu-id="3687a-136">您可以透過命令列工具、 **Winrm**，或透過使用 [winrm 腳本 API](winrm-scripting-api.md)的 VISUAL BASIC 腳本來取得 WMI 資料。</span><span class="sxs-lookup"><span data-stu-id="3687a-136">You can obtain WMI data either through the command-line tool, **Winrm**, or through a Visual Basic script that uses the [WinRM Scripting API](winrm-scripting-api.md).</span></span> <span data-ttu-id="3687a-137">您未使用 [WMI 路徑](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) 來找出資源。</span><span class="sxs-lookup"><span data-stu-id="3687a-137">You do not use a [WMI path](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) to locate a resource.</span></span> <span data-ttu-id="3687a-138">相反地，您會將 WMI 命名空間和階層轉換成 [*URI*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="3687a-138">Instead, you convert the WMI namespace and hierarchy to a [*URI*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="3687a-139">WMI 類別的 WinRM URI 包含兩個部分： [URI 前置](uri-prefixes.md) 詞和您想要存取的類別。</span><span class="sxs-lookup"><span data-stu-id="3687a-139">The WinRM URI for a WMI class contains two parts: the [URI prefix](uri-prefixes.md) and the class that you want to access.</span></span>

<span data-ttu-id="3687a-140">例如，您可以將下列 URI 提供給 [**會話。列舉**](session-enumerate.md) 方法可列出電腦上的所有服務。</span><span class="sxs-lookup"><span data-stu-id="3687a-140">For example, the following URI can be supplied to the [**Session.Enumerate**](session-enumerate.md) method to list all the services on a computer.</span></span> <span data-ttu-id="3687a-141">URI 前置詞為 `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` ，而類別是 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)。</span><span class="sxs-lookup"><span data-stu-id="3687a-141">The URI prefix is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`, and the class is [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

<span data-ttu-id="3687a-142">在 WMI 中，以數種方式列出資源或類別的所有實例資料：</span><span class="sxs-lookup"><span data-stu-id="3687a-142">In WMI, list the data for all of the instances of a resource or class in several ways:</span></span>

-   <span data-ttu-id="3687a-143">該資源之所有實例的查詢。</span><span class="sxs-lookup"><span data-stu-id="3687a-143">A query for all the instances of that resource.</span></span>

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   <span data-ttu-id="3687a-144">呼叫 [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof)或 [**\_ SWbemObject 實例**](/windows/desktop/WmiSdk/swbemobject-instances-)。</span><span class="sxs-lookup"><span data-stu-id="3687a-144">A call to [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) or [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span>

    `Set colServices = InstancesOf("Win32_Service")`

<span data-ttu-id="3687a-145">在 WinRM 中，有一種方式可列出資源的所有實例： [**Session。列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="3687a-145">In WinRM, there is one way to list all of the instances of a resource: [**Session.Enumerate**](session-enumerate.md).</span></span>


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a><span data-ttu-id="3687a-146">尋找 WMI 資源的特定實例</span><span class="sxs-lookup"><span data-stu-id="3687a-146">Locating a Specific Instance of a WMI Resource</span></span>

<span data-ttu-id="3687a-147">在 WMI 中，您可以藉由指定索引鍵屬性的值，或查詢符合屬性值清單的實例，來指定類別的特定實例。</span><span class="sxs-lookup"><span data-stu-id="3687a-147">In WMI, you can designate a particular instance of a class either by specifying values for the key properties or by querying for an instance that matches a list of property values.</span></span> <span data-ttu-id="3687a-148">索引鍵屬性具有 WMI [**金鑰限定詞**](/windows/desktop/WmiSdk/key-qualifier)。</span><span class="sxs-lookup"><span data-stu-id="3687a-148">Key properties have the WMI [**Key qualifier**](/windows/desktop/WmiSdk/key-qualifier).</span></span>

<span data-ttu-id="3687a-149">您可以透過數種方式取得類別的特定實例：</span><span class="sxs-lookup"><span data-stu-id="3687a-149">You can obtain a specific instance of a class in several ways:</span></span>

-   <span data-ttu-id="3687a-150">呼叫 [**Session。**](session-enumerate.md) 使用 *篩選* 和 *方言* 參數列舉來建立查詢。</span><span class="sxs-lookup"><span data-stu-id="3687a-150">A call to [**Session.Enumerate**](session-enumerate.md) with the *filter* and *dialect* parameters to create a query.</span></span>

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   <span data-ttu-id="3687a-151">呼叫 [**SWbemServices。 Get**](/windows/desktop/WmiSdk/swbemservices-get)。</span><span class="sxs-lookup"><span data-stu-id="3687a-151">A call to [**SWbemServices.Get**](/windows/desktop/WmiSdk/swbemservices-get).</span></span> <span data-ttu-id="3687a-152">若為 [**Session**](session-get.md)，您必須提供一或多個特定的索引鍵值，並在前面加上問號 (？ ) 。</span><span class="sxs-lookup"><span data-stu-id="3687a-152">For [**Session.Get**](session-get.md), you must supply one or more specific key values, preceded by a question mark (?).</span></span>

    <span data-ttu-id="3687a-153">特定實例之 URI 的格式為 `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` 。</span><span class="sxs-lookup"><span data-stu-id="3687a-153">The format of the URI for a specific instance is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    <span data-ttu-id="3687a-154">WMI 類別可以有一個以上的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3687a-154">A WMI class may have more than one key.</span></span> <span data-ttu-id="3687a-155">索引鍵名稱/值組是以 "+" 符號分隔。</span><span class="sxs-lookup"><span data-stu-id="3687a-155">Key name-value pairs are separated by a "+" sign.</span></span> <span data-ttu-id="3687a-156">在此情況下，格式為： `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` 。</span><span class="sxs-lookup"><span data-stu-id="3687a-156">In that case, the format is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2`.</span></span>

    <span data-ttu-id="3687a-157">取得單一 WMI 物件的 WinRM 語法與 WMI 不同。</span><span class="sxs-lookup"><span data-stu-id="3687a-157">The WinRM syntax to obtain a singleton WMI object is different from WMI.</span></span> <span data-ttu-id="3687a-158">Singleton 是定義的 WMI 類別，因此只允許一個實例。</span><span class="sxs-lookup"><span data-stu-id="3687a-158">A singleton is a WMI class defined so that only one instance is allowed.</span></span> <span data-ttu-id="3687a-159">[**Win32 \_CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) 或 [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) 是 WMI singleton 類別的範例。</span><span class="sxs-lookup"><span data-stu-id="3687a-159">[**Win32\_CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) or [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) are examples of a WMI singleton class.</span></span>

    <span data-ttu-id="3687a-160">下列 VBScript 程式碼範例會顯示 singleton 的 WMI 語法。</span><span class="sxs-lookup"><span data-stu-id="3687a-160">The WMI syntax for singletons is shown in the following VBScript code example.</span></span>

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    <span data-ttu-id="3687a-161">下列範例顯示不使用 "@" 的 WinRM singleton 語法。</span><span class="sxs-lookup"><span data-stu-id="3687a-161">The following example shows the WinRM singleton syntax which does not use "@".</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   <span data-ttu-id="3687a-162">將 [*選取器*](windows-remote-management-glossary.md) 加入至 [**ResourceLocator**](resourcelocator.md) 或 [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) 物件。</span><span class="sxs-lookup"><span data-stu-id="3687a-162">Adding a [*selector*](windows-remote-management-glossary.md) to a [**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object.</span></span>

    <span data-ttu-id="3687a-163">下列 VBScript 程式碼範例顯示如何使用選取器來取得特定的 [**Win32 \_ 處理器**](/windows/desktop/CIMWin32Prov/win32-processor)實例。</span><span class="sxs-lookup"><span data-stu-id="3687a-163">The following VBScript code example shows how to use a selector to get a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="3687a-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="3687a-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3687a-165">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="3687a-165">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="3687a-166">URI 首碼</span><span class="sxs-lookup"><span data-stu-id="3687a-166">URI Prefixes</span></span>](uri-prefixes.md)
</dt> <dt>

[<span data-ttu-id="3687a-167">資源 URI</span><span class="sxs-lookup"><span data-stu-id="3687a-167">Resource URIs</span></span>](resource-uris.md)
</dt> <dt>

[<span data-ttu-id="3687a-168">Windows 遠端管理中的腳本</span><span class="sxs-lookup"><span data-stu-id="3687a-168">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>
