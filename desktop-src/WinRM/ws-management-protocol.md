---
title: WS-Management 通訊協定
description: 公用標準，可從遠端與任何執行通訊協定的電腦裝置交換管理資料。
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e01fdc860eeb5510dd78a4127fdc22b30d711a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093264"
---
# <a name="ws-management-protocol"></a><span data-ttu-id="06685-103">WS-Management 通訊協定</span><span class="sxs-lookup"><span data-stu-id="06685-103">WS-Management Protocol</span></span>

<span data-ttu-id="06685-104">WS-Management 通訊協定是由一組硬體和軟體製造商開發的一個公用標準，用來從遠端與實作通訊協定的任何電腦裝置交換管理資料。</span><span class="sxs-lookup"><span data-stu-id="06685-104">The WS-Management protocol was developed by a group of hardware and software manufacturers as a public standard for remotely exchanging management data with any computer device that implements the protocol.</span></span>

## <a name="standards"></a><span data-ttu-id="06685-105">標準</span><span class="sxs-lookup"><span data-stu-id="06685-105">Standards</span></span>

<span data-ttu-id="06685-106">如需 WS-Management 通訊協定的詳細資訊，請參閱 [管理的 Web 服務 (ws-management) 規格](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf)。</span><span class="sxs-lookup"><span data-stu-id="06685-106">For more information about WS-Management protocol, see [Web Services for Management (WS-Management) Specification](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span></span>

<span data-ttu-id="06685-107">通訊協定的目的是要為各種裝置類型的管理作業提供一致性和互通性， (包括固件) 和作業系統。</span><span class="sxs-lookup"><span data-stu-id="06685-107">The intent of the protocol is to provide consistency and interoperability for management operations across many types of devices (including firmware) and operating systems.</span></span> <span data-ttu-id="06685-108">您可以擴充 WS-Management 的通訊協定，因為 IT 產業會識別新的作業。</span><span class="sxs-lookup"><span data-stu-id="06685-108">WS-Management protocol can be extended as new operations are identified by the IT industry.</span></span>

<span data-ttu-id="06685-109">WS-Management 通訊協定目前的執行是以下列標準規格為基礎： HTTPS、SOAP over HTTP (WS-I 設定檔) 、SOAP 1.2、WS-ADDRESSING、WS-Transfer、WS-ADDRESSING 和 WS-事件。</span><span class="sxs-lookup"><span data-stu-id="06685-109">The current implementation of the WS-Management protocol is based on the following standard specifications: HTTPS, SOAP over HTTP (WS-I profile), SOAP 1.2, WS-Addressing, WS-Transfer, WS-Enumeration, and WS-Eventing.</span></span> <span data-ttu-id="06685-110">如需 WS-Management 標準和 XML 架構的詳細資訊，請參閱 <https://dmtf.org/standards/wsman></span><span class="sxs-lookup"><span data-stu-id="06685-110">For more information about the WS-Management standards and XML schemas see <https://dmtf.org/standards/wsman></span></span>

## <a name="messages"></a><span data-ttu-id="06685-111">訊息</span><span class="sxs-lookup"><span data-stu-id="06685-111">Messages</span></span>

<span data-ttu-id="06685-112">WS-Management 通訊協定提供使用各種 web 服務標準（例如 [*ws-addressing*](windows-remote-management-glossary.md)和 [*ws-傳輸*](windows-remote-management-glossary.md)）來建立 XML [*訊息*](windows-remote-management-glossary.md)的標準。</span><span class="sxs-lookup"><span data-stu-id="06685-112">The WS-Management protocol provides a standard for constructing XML [*messages*](windows-remote-management-glossary.md) using various web service standards such as [*WS-Addressing*](windows-remote-management-glossary.md) and [*WS-Transfer*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="06685-113">這些標準會定義 web 服務訊息的 XML 架構。</span><span class="sxs-lookup"><span data-stu-id="06685-113">These standards define XML schemas for web service messages.</span></span> <span data-ttu-id="06685-114">這些訊息會使用 [*資源 URI*](windows-remote-management-glossary.md)來參考 [*資源*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="06685-114">The messages refer to a [*resource*](windows-remote-management-glossary.md) using a [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="06685-115">WS-Management 通訊協定會為管理作業和值新增一組定義。</span><span class="sxs-lookup"><span data-stu-id="06685-115">The WS-Management protocol adds a set of definitions for management operations and values.</span></span> <span data-ttu-id="06685-116">例如，WS-Transfer 會定義資源的 Get、Put、Create 和 Delete 作業。</span><span class="sxs-lookup"><span data-stu-id="06685-116">For example, WS-Transfer defines the Get, Put, Create, and Delete operations for a resource.</span></span> <span data-ttu-id="06685-117">WS-Management 通訊協定會新增重新命名、部分取得和部分 Put。</span><span class="sxs-lookup"><span data-stu-id="06685-117">WS-Management protocol adds Rename, Partial Get, and Partial Put.</span></span>

<span data-ttu-id="06685-118">這些訊息遵循了 [*簡單物件存取通訊協定的慣例， (SOAP)*](windows-remote-management-glossary.md) ，而這些都是由所有的 web 服務通訊協定所使用。</span><span class="sxs-lookup"><span data-stu-id="06685-118">The messages follow the conventions of [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md) which is used by all web service protocols.</span></span>

<span data-ttu-id="06685-119">下列程式碼範例顯示含有 Get 作業的訊息。</span><span class="sxs-lookup"><span data-stu-id="06685-119">The following code example shows a message with a Get operation.</span></span> <span data-ttu-id="06685-120">此範例會顯示為協助您瞭解基礎訊息的外觀。</span><span class="sxs-lookup"><span data-stu-id="06685-120">This example is shown as an aid to understanding what the underlying messages look like.</span></span> <span data-ttu-id="06685-121">您不需要知道如何產生 SOAP 訊息。</span><span class="sxs-lookup"><span data-stu-id="06685-121">You do not need to know how to produce SOAP messages.</span></span> <span data-ttu-id="06685-122">當您使用 **winrm** 命令列工具執行命令或執行以 [winrm 腳本 API](winrm-scripting-api.md)撰寫的腳本時，Windows 遠端管理會將這些訊息組合。</span><span class="sxs-lookup"><span data-stu-id="06685-122">The messages are assembled by Windows Remote Management when you execute a command using the **Winrm** command-line tool or run a script written with the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="06685-123">此訊息是從名為 RemoteComputer 的伺服器取得具有 **DeviceID** 屬性 "c：" 的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)實例的要求。</span><span class="sxs-lookup"><span data-stu-id="06685-123">The message is a request to get the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) with a **DeviceID** property of "c:" from a server named RemoteComputer.</span></span> <span data-ttu-id="06685-124">要求會透過埠80使用 HTTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="06685-124">The request uses the HTTP transport through port 80.</span></span> <span data-ttu-id="06685-125">傳送要求的帳戶必須位於遠端電腦上的本機系統管理員群組中。</span><span class="sxs-lookup"><span data-stu-id="06685-125">The account sending the request must be in the local administrators group on the remote computer.</span></span>

<span data-ttu-id="06685-126">每個標記開頭的冒號前面的字元會指出哪個標準定義了 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="06685-126">The characters before the colon at the beginning of each tag indicate which standard defines the XML element.</span></span> <span data-ttu-id="06685-127">例如， ` <wsa:To>` 表示 To 專案是由 WS-Addressing 標準所定義，並 `<s:Header>` 指出 SOAP 訊息中標頭內容的開頭。</span><span class="sxs-lookup"><span data-stu-id="06685-127">For example, ` <wsa:To>` indicates that the To element is defined by the WS-Addressing standard and `<s:Header>` indicates the beginning of the header content in a SOAP message.</span></span> <span data-ttu-id="06685-128">請注意，大部分的訊息都是由 SOAP 或 WS-ADDRESSING 所定義的 XML 元素所組成。</span><span class="sxs-lookup"><span data-stu-id="06685-128">Be aware that the majority of the message is composed of XML elements defined by SOAP or WS-Addressing.</span></span> <span data-ttu-id="06685-129">WS-Management 通訊協定會新增 MaxEnvelopeSize、選取器和 SelectorSet。</span><span class="sxs-lookup"><span data-stu-id="06685-129">WS-Management protocol adds MaxEnvelopeSize, Selector, and SelectorSet.</span></span>


```XML
<s:Envelope xmlns:s="https://www.w3.org/2003/05/soap-envelope" 
            xmlns:a="https://schemas.xmlsoap.org/ws/2004/08/addressing" 
            xmlns:w="https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd">
  <s:Header>
    <a:To>https://RemoteComputer:80/wsman</a:To> 
    <w:ResourceURI s:mustUnderstand="true">
      http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_logicaldisk
    </w:ResourceURI> 
    <a:ReplyTo>
    <a:Address s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </a:Address> 
    </a:ReplyTo>
    <a:Action s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </a:Action> 
    <w:MaxEnvelopeSize s:mustUnderstand="true">153600</w:MaxEnvelopeSize> 
    <a:MessageID>uuid:4ED2993C-4339-4E99-81FC-C2FD3812781A</a:MessageID> 
    <w:Locale xml:lang="en-US" s:mustUnderstand="false"/> 
    <w:SelectorSet>
    <w:Selector Name="DeviceId">c:</w:Selector> 
    </w:SelectorSet>
    <w:OperationTimeout>PT60.000S</w:OperationTimeout> 
  </s:Header>
  <s:Body/> 
</s:Envelope>
```



## <a name="related-topics"></a><span data-ttu-id="06685-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="06685-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06685-131">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="06685-131">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="06685-132">遠端硬體管理</span><span class="sxs-lookup"><span data-stu-id="06685-132">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> </dl>

 

 