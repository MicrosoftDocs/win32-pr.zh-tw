---
title: 在 Windows XP 中使用 Teredo
ms.assetid: 21590e3b-03de-48a4-b142-5d1934dacc38
description: 深入瞭解：在 Windows XP 中使用 Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29abb2b4056564be29708ceb00742b37d363d7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027484"
---
# <a name="using-teredo-in-windows-xp"></a><span data-ttu-id="914f9-103">在 Windows XP 中使用 Teredo</span><span class="sxs-lookup"><span data-stu-id="914f9-103">Using Teredo in Windows XP</span></span>

<span data-ttu-id="914f9-104">若要在執行 Windows XP Service Pack 1 的電腦上使用 Teredo 用戶端或主機特定轉送 (SP1) 搭配 Advanced 網路套件、Windows XP Service pack 2 (SP2) 、Windows Server 2003 （含 Service pack 1） (SP1) 或 Windows Server 2003 Service Pack 2 (SP2) ，應用程式開發人員必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="914f9-104">To use the Teredo client or host-specific relay on computers running Windows XP with Service Pack 1 (SP1) with the Advanced Networking Pack, Windows XP with Service Pack 2 (SP2), Windows Server 2003 with Service Pack 1 (SP1), or Windows Server 2003 with Service Pack 2 (SP2), an application developer must do the following:</span></span>

-   <span data-ttu-id="914f9-105">使用新的 Windows 通訊端2程式設計項目， (可同時支援 IPv4 和 IPv6) 的函式和結構，確保應用程式與 IPv6 相容。</span><span class="sxs-lookup"><span data-stu-id="914f9-105">Ensure that the application is compatible with IPv6 by using new Windows Sockets 2 programming elements (functions and structures) that support both IPv4 and IPv6.</span></span> <span data-ttu-id="914f9-106">如需詳細資訊，請參閱 [Windows 通訊端應用程式的 IPv6 指南](../winsock/ipv6-guide-for-windows-sockets-applications-2.md)。</span><span class="sxs-lookup"><span data-stu-id="914f9-106">For more information, see the [IPv6 Guide for Windows Sockets Applications](../winsock/ipv6-guide-for-windows-sockets-applications-2.md).</span></span>
-   <span data-ttu-id="914f9-107">藉由將 [IPV6 \_ 保護 \_ 等級 Windows 通訊端通訊端] 選項設定為保護層級不 \_ \_ 受限制的層級，啟用在應用程式中使用 Teredo。</span><span class="sxs-lookup"><span data-stu-id="914f9-107">Enable the use of Teredo in your application by setting the IPV6\_PROTECTION\_LEVEL Windows Sockets socket option to the PROTECTION\_LEVEL\_UNRESTRICTED level.</span></span> <span data-ttu-id="914f9-108">如需詳細資訊，請參閱 [使用 IPV6 \_ 保護 \_ 層級](/previous-versions/aa916826(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="914f9-108">For more information, see [Using IPV6\_PROTECTION\_LEVEL](/previous-versions/aa916826(v=msdn.10)).</span></span> <span data-ttu-id="914f9-109">您也可以透過 .NET Framework 類別的 [系統 .net](/dotnet/api/system.net.sockets?view=netcore-3.1) 來設定此選項。</span><span class="sxs-lookup"><span data-stu-id="914f9-109">You can also set this option through the [System.Net.Sockets](/dotnet/api/system.net.sockets?view=netcore-3.1) .NET Framework class.</span></span>
-   <span data-ttu-id="914f9-110">建立 Windows 防火牆的例外狀況，以允許未經要求的連入 Teredo 流量。</span><span class="sxs-lookup"><span data-stu-id="914f9-110">Create an exception for the Windows Firewall to allow unsolicited incoming Teredo traffic.</span></span> <span data-ttu-id="914f9-111">您可以使用 [Windows 防火牆](/previous-versions/windows/desktop/ics/windows-firewall-start-page) api，針對指派給 Teredo 流量的 UDP 埠建立埠例外狀況。</span><span class="sxs-lookup"><span data-stu-id="914f9-111">Use the [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page) APIs to create a port exception for the UDP port assigned for Teredo traffic.</span></span> <span data-ttu-id="914f9-112">如需詳細資訊和範例，以詳述 Teredo 的必要安全性和流量考慮，請參閱 [使用 teredo](using-teredo.md)。</span><span class="sxs-lookup"><span data-stu-id="914f9-112">For more information and examples detailing required security and traffic considerations for Teredo, see [Using Teredo](using-teredo.md).</span></span>

<span data-ttu-id="914f9-113">為了確保在應用程式執行時可以使用 Teredo，應用程式開發人員應在應用程式的安裝過程中執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="914f9-113">To ensure that Teredo is available for use when the application runs, application developers should do the following during the application's installation process:</span></span>

-   <span data-ttu-id="914f9-114">使用 **netsh interface ipv6 install** 命令安裝 IPv6。</span><span class="sxs-lookup"><span data-stu-id="914f9-114">Install IPv6 with the **netsh interface ipv6 install** command.</span></span> <span data-ttu-id="914f9-115">Windows 防火牆會以與 IPv4 流量相同的方式，保護使用者的電腦免于未經要求的連入 IPv6 流量。</span><span class="sxs-lookup"><span data-stu-id="914f9-115">Windows Firewall protects the user's computer from unsolicited incoming IPv6 traffic in the same way as IPv4 traffic.</span></span>
-   <span data-ttu-id="914f9-116">使用 **netsh interface ipv6 set teredo 用戶端** 命令啟用 Teredo。</span><span class="sxs-lookup"><span data-stu-id="914f9-116">Enable Teredo with the **netsh interface ipv6 set teredo client** command.</span></span>

<span data-ttu-id="914f9-117">（選擇性）您可以測試每次應用程式執行時是否安裝 IPv6，並視需要安裝 IPv6 並啟用 Teredo。</span><span class="sxs-lookup"><span data-stu-id="914f9-117">Optionally, you can test whether IPv6 is installed each time your application runs and install IPv6 and enable Teredo as needed.</span></span> <span data-ttu-id="914f9-118">您也應該通知使用者正在安裝 IPv6，而且正在啟用 Teredo。</span><span class="sxs-lookup"><span data-stu-id="914f9-118">You should also inform the user that IPv6 is being installed and that Teredo is being enabled.</span></span>

 

 
