---
description: 如需您可以在 Windows Vista 和更新版本中用來設定 Windows HTTP 之 proxy 和追蹤設定的命令，請參閱 Windows 超文字傳輸通訊協定 (WINHTTP) 的 Netsh 命令。
ms.assetid: 81f6b25e-ea14-4dbd-a715-926db7cf90e7
title: 使用 WinHTTP 工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e402962dc34cbf654fa8db49f96b86e7406a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986345"
---
# <a name="using-winhttp-tools"></a><span data-ttu-id="5c570-103">使用 WinHTTP 工具</span><span class="sxs-lookup"><span data-stu-id="5c570-103">Using WinHTTP Tools</span></span>

<span data-ttu-id="5c570-104">如需您可以在 Windows Vista 和更新版本中用來設定 Windows HTTP 之 proxy 和追蹤設定的命令，請參閱 [Windows 超文字傳輸通訊協定 (WINHTTP) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="5c570-104">For the commands you can use in Windows Vista and later to configure proxy and tracing settings for Windows HTTP , see [Netsh Commands for Windows Hypertext Transfer Protocol (WINHTTP)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)).</span></span>

<span data-ttu-id="5c570-105">**Windows Server 2003 及更早版本：** 有數個工具可用來協助您撰寫和偵測應用程式。</span><span class="sxs-lookup"><span data-stu-id="5c570-105">**Windows Server 2003 and Earlier:** There are several tools that are available to help you write and debug your applications.</span></span> <span data-ttu-id="5c570-106">這些主題將在下列主題中說明：</span><span class="sxs-lookup"><span data-stu-id="5c570-106">They are explained in the following topics:</span></span>

-   <span data-ttu-id="5c570-107">[WinHttpCfg.exe，「憑證設定工具](winhttpcertcfg-exe--a-certificate-configuration-tool.md) 」可讓系統管理員在任何 [*憑證存放區*](glossary.md) 中安裝和設定用戶端憑證，以供網際網路伺服器 Web 應用程式管理員 (的) 帳戶存取。</span><span class="sxs-lookup"><span data-stu-id="5c570-107">[WinHttpCfg.exe, a Certificate Configuration Tool](winhttpcertcfg-exe--a-certificate-configuration-tool.md) enables administrators to install and configure client certificates in any [*certificate store*](glossary.md) that can be accessed by the Internet Server Web Application Manager (IWAM) account.</span></span> <span data-ttu-id="5c570-108">此工具也可讓您不需要對帳戶（例如 IWAM 帳戶）採取任何特殊動作，就能在使用 Active Server Pages (ASP) 時取得憑證的存取權。</span><span class="sxs-lookup"><span data-stu-id="5c570-108">The tool also eliminates the need to do anything special to accounts such as the IWAM account to gain access to certificates when using Active Server Pages (ASP).</span></span>
-   <span data-ttu-id="5c570-109">[Netsh.exe 或 ProxyCfg.exe proxy 組態工具](proxycfg-exe--a-proxy-configuration-tool.md) 可以使用 MICROSOFT Windows HTTP Services (WinHTTP) 來設定 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="5c570-109">[Netsh.exe or ProxyCfg.exe Proxy Configuration Tools](proxycfg-exe--a-proxy-configuration-tool.md) can be used to configure proxy servers with Microsoft Windows HTTP Services (WinHTTP).</span></span>
-   <span data-ttu-id="5c570-110">[WinHttpTraceCfg，追蹤設定工具](winhttptracecfg-exe--a-trace-configuration-tool.md) 可讓您監視 WinHTTP 函式和對應的網路流量。</span><span class="sxs-lookup"><span data-stu-id="5c570-110">[WinHttpTraceCfg, a Trace Configuration Tool](winhttptracecfg-exe--a-trace-configuration-tool.md) provides the ability to monitor WinHTTP functions and the corresponding network traffic.</span></span> <span data-ttu-id="5c570-111">使用加密的線路通訊協定（例如安全通訊端層 (SSL) ）進行的偵錯工具，會阻止網路傳輸層的探查封包，而且必須能夠在用戶端和伺服器解密之後攔截流量。</span><span class="sxs-lookup"><span data-stu-id="5c570-111">Debugging applications which utilize encrypted wire protocols, such as Secure Sockets Layer (SSL), preclude sniffing packets at the network transport layer and require the ability to intercept traffic between the client and server after it has been decrypted.</span></span> <span data-ttu-id="5c570-112">WinHTTP 追蹤設備具有一系列的功能，可攔截用戶端與伺服器之間的流量串流。</span><span class="sxs-lookup"><span data-stu-id="5c570-112">The WinHTTP trace facility has a range of capabilities for intercepting the traffic stream between the client and server.</span></span>

 

 
