---
title: 從本機電腦取得資料
description: 雖然 Windows 遠端管理和 WS-Management 通訊協定是針對遠端通訊明確設計，但是在本機電腦上建立會話是最簡單的情況。
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682384"
---
# <a name="obtaining-data-from-the-local-computer"></a><span data-ttu-id="01762-103">從本機電腦取得資料</span><span class="sxs-lookup"><span data-stu-id="01762-103">Obtaining Data from the Local Computer</span></span>

<span data-ttu-id="01762-104">雖然 Windows 遠端管理和 WS-Management 通訊協定是針對遠端通訊明確設計，但是在本機電腦上建立會話是最簡單的情況。</span><span class="sxs-lookup"><span data-stu-id="01762-104">Although Windows Remote Management and WS-Management protocol are explicitly designed for remote communication, establishing a session on the local computer is the simplest case.</span></span> <span data-ttu-id="01762-105">某些腳本可能需要在本機電腦和遠端電腦上存取資料。</span><span class="sxs-lookup"><span data-stu-id="01762-105">Some scripts may require access data on the local computer as well as remote computers.</span></span>

<span data-ttu-id="01762-106">**WinRM 2.0 版：  **</span><span class="sxs-lookup"><span data-stu-id="01762-106">**WinRM version 2.0:  **</span></span>

<span data-ttu-id="01762-107">所有作業都會被視為遠端，而且必須先啟動 WinRM 服務，才能執行任何操作。</span><span class="sxs-lookup"><span data-stu-id="01762-107">All operations are considered remote and the WinRM service must be started before any operation is performed.</span></span> <span data-ttu-id="01762-108">如果未指定遠端目的地，則預設會使用 localhost，而且所有作業都會傳送至本機 WinRM 服務。</span><span class="sxs-lookup"><span data-stu-id="01762-108">If a remote destination is not specified, then the localhost is used by default, and all operations will be sent to the local WinRM service.</span></span> <span data-ttu-id="01762-109">如需啟動 WinRM 服務的詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。</span><span class="sxs-lookup"><span data-stu-id="01762-109">For more information about starting the WinRM service, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="01762-110">使用 WinRM 服務進行本機作業時，應該考慮下列因素：</span><span class="sxs-lookup"><span data-stu-id="01762-110">When using the WinRM service for local operations, the following factors should be considered:</span></span>

-   <span data-ttu-id="01762-111">本機 WinRM 設定只能由系統管理員讀取。</span><span class="sxs-lookup"><span data-stu-id="01762-111">The local WinRM configuration can only be read by administrators.</span></span>
-   <span data-ttu-id="01762-112">WMI 命名空間必須設定遠端啟用許可權。</span><span class="sxs-lookup"><span data-stu-id="01762-112">WMI namespaces must have remote enable permissions set.</span></span> <span data-ttu-id="01762-113">如需詳細資訊，請參閱 [保護遠端 WMI 連接](../wmisdk/securing-a-remote-wmi-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="01762-113">For more information, see [Securing a Remote WMI Connection](../wmisdk/securing-a-remote-wmi-connection.md).</span></span>
-   <span data-ttu-id="01762-114">如果 [*未建立 winrm 接聽*](windows-remote-management-glossary.md) 程式，則 winrm 服務會接聽埠47001上的本機要求。</span><span class="sxs-lookup"><span data-stu-id="01762-114">If a WinRM [*listener*](windows-remote-management-glossary.md) is not created, then the WinRM service listens for local requests on port 47001.</span></span>

<span data-ttu-id="01762-115">每個 WinRM 腳本都必須先藉由建立 [**會話**](session.md) 物件來建立會話或連接到電腦。</span><span class="sxs-lookup"><span data-stu-id="01762-115">Every WinRM script must start by establishing a session or connection to a computer by creating a [**Session**](session.md) object.</span></span> <span data-ttu-id="01762-116">建立會話之後，您可以使用 **會話** 物件方法（例如 [**session. 列舉**](session-enumerate.md) 或 [**session. Invoke**](session-invoke.md) ）來取得資料或執行方法。</span><span class="sxs-lookup"><span data-stu-id="01762-116">After the session is created, you can use the **Session** object methods, such as [**Session.Enumerate**](session-enumerate.md) or [**Session.Invoke**](session-invoke.md) to obtain data or to execute methods.</span></span>

<span data-ttu-id="01762-117">建立會話有點 [類似于連線至 Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) ([WMI](/windows/desktop/WmiSdk/wmi-start-page)) 命名空間。</span><span class="sxs-lookup"><span data-stu-id="01762-117">The creation of a session is somewhat similar to [connecting](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) to a Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page)) namespace.</span></span> <span data-ttu-id="01762-118">此會話基本上是一層，可讓您透過 [*SOAP*](windows-remote-management-glossary.md) 訊息和 WS-Management 的通訊協定來傳送和接收資料。</span><span class="sxs-lookup"><span data-stu-id="01762-118">The session is essentially a layer that allows you to send and receive data through [*SOAP*](windows-remote-management-glossary.md) messages and the WS-Management protocol.</span></span> <span data-ttu-id="01762-119">如需詳細資訊，請參閱 [WS-Management 通訊協定](ws-management-protocol.md)。</span><span class="sxs-lookup"><span data-stu-id="01762-119">For more information, see [WS-Management Protocol](ws-management-protocol.md).</span></span>

<span data-ttu-id="01762-120">呼叫 [**CreateSession**](wsman-createsession.md) 方法來建立 [**會話**](session.md) 物件將會啟動連接到本機 WinRM 的 [*會話*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="01762-120">Calling the [**WSMan.CreateSession**](wsman-createsession.md) method to create a [**Session**](session.md) object will start a [*session*](windows-remote-management-glossary.md) that connects to the local WinRM.</span></span>

<span data-ttu-id="01762-121">**建立 WSMan 會話並取得資料**</span><span class="sxs-lookup"><span data-stu-id="01762-121">**To Create a WSMan Session and Obtain Data**</span></span>

1.  <span data-ttu-id="01762-122">建立 [**WSMan**](wsman.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="01762-122">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="01762-123">藉由呼叫 [**WSMan. CreateSession**](wsman-createsession.md) 方法來建立會話。</span><span class="sxs-lookup"><span data-stu-id="01762-123">Create a session by calling the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="01762-124">此會話會以您的登入使用者名稱和密碼執行，並可透過本機 WinRM 取得資料。</span><span class="sxs-lookup"><span data-stu-id="01762-124">This session runs under your logon username and password and can obtain data through the local WinRM.</span></span>

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  <span data-ttu-id="01762-125">建立資源 [*URI*](windows-remote-management-glossary.md) 來識別您想要管理的資源，或您想要為其取得資料的 [*資源*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="01762-125">Create a resource [*URI*](windows-remote-management-glossary.md) to identify the [*resource*](windows-remote-management-glossary.md) you want to manage or for which you want to obtain data.</span></span> <span data-ttu-id="01762-126">如需有關如何格式化 URI 的詳細資訊，請參閱 [資源 uri](resource-uris.md)。</span><span class="sxs-lookup"><span data-stu-id="01762-126">For more information about formatting a URI, see [Resource URIs](resource-uris.md).</span></span> <span data-ttu-id="01762-127">此資源 URI 適用于 WMI [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 類別的特定實例，也就是 Winmgmt 服務。</span><span class="sxs-lookup"><span data-stu-id="01762-127">This resource URI is for a specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the Winmgmt service.</span></span> <span data-ttu-id="01762-128">如需詳細資訊，請參閱 [Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="01762-128">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  <span data-ttu-id="01762-129">呼叫使用資源 URI 取得或列舉資料的 [**會話**](session.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="01762-129">Call [**Session**](session.md) methods that get or enumerate data using the resource URI.</span></span> <span data-ttu-id="01762-130">如需詳細資訊，請參閱 [WinRM 腳本 API](winrm-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="01762-130">For more information, see [WinRM Scripting API](winrm-scripting-api.md).</span></span>

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  <span data-ttu-id="01762-131">若要從另一部電腦取得或管理資料，或使用不同的驗證方法，請參閱 [從遠端電腦取得資料](obtaining-data-from-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="01762-131">To get or manage data from another computer or use different methods of authentication, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span>

<span data-ttu-id="01762-132">下列 VBScript 程式碼範例顯示完整的腳本，該腳本會取得名為 "Winmgmt" 的 WMI [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 的特定實例。</span><span class="sxs-lookup"><span data-stu-id="01762-132">The following VBScript code example shows the complete script that obtains the specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) named "Winmgmt".</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



<span data-ttu-id="01762-133">下列 VBScript 程式碼範例顯示具有資料轉換的完整腳本。</span><span class="sxs-lookup"><span data-stu-id="01762-133">The following VBScript code example shows the complete script with the data transform.</span></span> <span data-ttu-id="01762-134">如需詳細資訊，請參閱 [顯示 WinRM 腳本的 XML 輸出](displaying-xml-output-from-winrm-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="01762-134">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a><span data-ttu-id="01762-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="01762-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01762-136">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="01762-136">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="01762-137">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="01762-137">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="01762-138">Windows 遠端管理參考</span><span class="sxs-lookup"><span data-stu-id="01762-138">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 