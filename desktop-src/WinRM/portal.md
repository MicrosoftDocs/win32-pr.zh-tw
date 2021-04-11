---
title: Windows 遠端管理
description: Windows 遠端管理 (Windows 遠端管理) 是 Microsoft WS-Management 通訊協定的採用，這是一種標準的 SOAP 型、可供防火牆使用的通訊協定，可讓不同廠商的硬體與作業系統交互操作。
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Windows 遠端管理 (WinRM) 、起始頁
- WS-Management
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27311699fe0321eddc1d3117b17acf3e49e9d518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933270"
---
# <a name="windows-remote-management"></a><span data-ttu-id="47bef-105">Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="47bef-105">Windows Remote Management</span></span>

## <a name="purpose"></a><span data-ttu-id="47bef-106">目的</span><span class="sxs-lookup"><span data-stu-id="47bef-106">Purpose</span></span>

<span data-ttu-id="47bef-107">Windows 遠端管理 (WinRM) 是 Microsoft 在 [WS-Management 通訊協定](ws-management-protocol.md)方面的實作，它是以簡易物件存取通訊協定 (SOAP) 為基礎、防火牆適用的通訊協定，允許不同廠商的硬體和作業系統互相操作。</span><span class="sxs-lookup"><span data-stu-id="47bef-107">Windows Remote Management (WinRM) is the Microsoft implementation of [WS-Management Protocol](ws-management-protocol.md), a standard Simple Object Access Protocol (SOAP)-based, firewall-friendly protocol that allows hardware and operating systems, from different vendors, to interoperate.</span></span>

<span data-ttu-id="47bef-108">WS-Management 通訊協定規格提供了一種常見的方式，讓系統在整個 IT 基礎結構之間存取及交換管理資訊。</span><span class="sxs-lookup"><span data-stu-id="47bef-108">The WS-Management protocol specification provides a common way for systems to access and exchange management information across an IT infrastructure.</span></span> <span data-ttu-id="47bef-109">WinRM 和 [*智慧型平臺管理介面 (IPMI)*](windows-remote-management-glossary.md)，而 [事件收集器](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) 則是 [Windows 硬體管理](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) 功能的元件。</span><span class="sxs-lookup"><span data-stu-id="47bef-109">WinRM and [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md), along with the [Event Collector](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) are components of the [Windows Hardware Management](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) features.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="47bef-110">適用時</span><span class="sxs-lookup"><span data-stu-id="47bef-110">Where applicable</span></span>

<span data-ttu-id="47bef-111">您可以使用 WinRM 腳本物件、WinRM 命令列工具或 Windows 遠端 Shell 命令列工具 WinRS 來取得本機和遠端電腦上的管理資料，這些電腦可能會有 [*(bmc)*](windows-remote-management-glossary.md)的基礎板管理控制器。</span><span class="sxs-lookup"><span data-stu-id="47bef-111">You can use WinRM scripting objects, the WinRM command-line tool, or the Windows Remote Shell command line tool WinRS to obtain management data from local and remote computers that may have [*baseboard management controllers (BMCs)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="47bef-112">如果電腦執行包含 WinRM 的 Windows 作業系統版本，管理資料會由 [Windows Management Instrumentation (WMI) ](/windows/desktop/WmiSdk/wmi-start-page)提供。</span><span class="sxs-lookup"><span data-stu-id="47bef-112">If the computer runs a Windows-based operating system version that includes WinRM, the management data is supplied by [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

<span data-ttu-id="47bef-113">您也可以從企業中 Windows 以外的作業系統上執行的 WS-Management 通訊協定實作獲取硬體和系統資料。</span><span class="sxs-lookup"><span data-stu-id="47bef-113">You can also obtain hardware and system data from WS-Management protocol implementations running on operating systems other than Windows in your enterprise.</span></span> <span data-ttu-id="47bef-114">WinRM 會透過以 SOAP 為基礎的 WS-Management 通訊協定與遠端電腦建立工作階段，而不是透過與 DCOM 的連線，就像 WMI 一樣。</span><span class="sxs-lookup"><span data-stu-id="47bef-114">WinRM establishes a session with a remote computer through the SOAP-based WS-Management protocol rather than a connection through DCOM, as WMI does.</span></span> <span data-ttu-id="47bef-115">傳回到 WS-Management 通訊協定的資料會使用 XML 格式，而不是物件格式。</span><span class="sxs-lookup"><span data-stu-id="47bef-115">Data returned to WS-Management protocol are formatted in XML rather than in objects.</span></span>

<span data-ttu-id="47bef-116">[智慧型平臺管理介面 (IPMI) ](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI 提供者是標準的 wmi 提供者，其類別可從具有適當硬體的電腦取得 BMC 感應器資料。</span><span class="sxs-lookup"><span data-stu-id="47bef-116">The [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI provider is a standard WMI provider with classes that obtain BMC sensor data from computers with appropriate hardware.</span></span> <span data-ttu-id="47bef-117">您可以使用 WinRM 腳本 API、WMI [腳本](/windows/desktop/WmiSdk/scripting-api-for-wmi)或 [COM](/windows/desktop/WmiSdk/com-api-for-wmi) api 來存取 IPMI 資料。</span><span class="sxs-lookup"><span data-stu-id="47bef-117">IPMI data can be accessed using the WinRM scripting API, the WMI [Scripting](/windows/desktop/WmiSdk/scripting-api-for-wmi), or [COM](/windows/desktop/WmiSdk/com-api-for-wmi) APIs.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="47bef-118">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="47bef-118">Developer audience</span></span>

<span data-ttu-id="47bef-119">開發人員物件是一位 IT 專業人員，負責撰寫腳本，以自動化伺服器的管理，或 ISV 開發人員為管理應用程式取得資料。</span><span class="sxs-lookup"><span data-stu-id="47bef-119">The developer audience is the IT Pro who writes scripts to automate the management of servers or the ISV developer obtaining data for management applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="47bef-120">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="47bef-120">Run-time requirements</span></span>

<span data-ttu-id="47bef-121">WinRM 是作業系統的一部分。</span><span class="sxs-lookup"><span data-stu-id="47bef-121">WinRM is part of the operating system.</span></span> <span data-ttu-id="47bef-122">不過，若要從遠端電腦取得資料，您必須 [*設定 WinRM 接聽*](windows-remote-management-glossary.md#l)程式。</span><span class="sxs-lookup"><span data-stu-id="47bef-122">However, to obtain data from remote computers, you must configure a WinRM [*listener*](windows-remote-management-glossary.md#l).</span></span> <span data-ttu-id="47bef-123">如需詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。</span><span class="sxs-lookup"><span data-stu-id="47bef-123">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="47bef-124">如果在系統啟動時偵測到 BMC，則會載入 IPMI 提供者;否則，仍然可以使用 WinRM 腳本物件和 WinRM 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="47bef-124">If a BMC is detected at system startup, then the IPMI provider loads; otherwise, the WinRM scripting objects and the WinRM command-line tool are still available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="47bef-125">本節內容</span><span class="sxs-lookup"><span data-stu-id="47bef-125">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="47bef-126">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="47bef-126">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="47bef-127">連結至公用 WS-Management 通訊協定規格、WinRM 架構、與 WMI 的關聯性、使用 IPMI 提供者的硬體管理、設定和安裝。</span><span class="sxs-lookup"><span data-stu-id="47bef-127">Link to public WS-Management protocol specification, WinRM architecture, relationship to WMI, hardware management with the IPMI provider, configuration and installation.</span></span>

</dd> <dt>

[<span data-ttu-id="47bef-128">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="47bef-128">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="47bef-129">開始使用 WinRM 腳本 API 和硬體管理。</span><span class="sxs-lookup"><span data-stu-id="47bef-129">Getting started using the WinRM scripting API and hardware management.</span></span>

</dd> <dt>

[<span data-ttu-id="47bef-130">Windows 遠端管理參考</span><span class="sxs-lookup"><span data-stu-id="47bef-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dd>

<span data-ttu-id="47bef-131">由 Microsoft Web Services for Management 所定義的指令碼介面清單 (WS-MANAGEMENT) 自動化和由 IPMI 提供者所建立之 WMI 類別的類別定義，以及與 IPMI 驅動程式通訊的類別，以取得基礎板 [管理控制器 (BMC) ](windows-remote-management-glossary.md) 資料。</span><span class="sxs-lookup"><span data-stu-id="47bef-131">List of scripting interfaces defined by Microsoft Web Services for Management (WS-Management) Automation and class definitions of the WMI classes created by the IPMI provider and classes that communicate with the IPMI driver to obtain [baseboard management controller (BMC)](windows-remote-management-glossary.md) data.</span></span>

</dd> </dl>

 

 