---
description: 在 Windows XP 上，提供了新的命令列工具來設定和管理 IPv4。 此工具會使用 &\# 0034; netsh interface ip&\# 0034; 命令來設定和管理 IPv4。
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: 使用 IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f759d938ebebbc0ddfbb2326dfb10932c16310a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975275"
---
# <a name="using-ipv6"></a><span data-ttu-id="3bbc0-104">使用 IPv6</span><span class="sxs-lookup"><span data-stu-id="3bbc0-104">Using IPv6</span></span>

<span data-ttu-id="3bbc0-105">在 Windows XP 上，提供了新的命令列工具來設定和管理 IPv4。</span><span class="sxs-lookup"><span data-stu-id="3bbc0-105">On Windows XP a later, a new command-line tool is provided for configuring and managing IPv4.</span></span> <span data-ttu-id="3bbc0-106">此工具會使用「netsh interface ip」命令來設定和管理 IPv4。</span><span class="sxs-lookup"><span data-stu-id="3bbc0-106">This tool uses the "netsh interface ip" command for configuring and managing IPv4.</span></span>

<span data-ttu-id="3bbc0-107">在 Windows XP Service Pack 1 (SP1) 和更新版本中，這個新的命令列工具已增強，可支援 IPv6 的設定和管理。</span><span class="sxs-lookup"><span data-stu-id="3bbc0-107">On Windows XP with Service Pack 1 (SP1) and later, this new command-line tool was enhanced to support the configuration and management of IPv6.</span></span> <span data-ttu-id="3bbc0-108">此增強工具是「netsh interface ipv6」命令。</span><span class="sxs-lookup"><span data-stu-id="3bbc0-108">This enhanced tool is the "netsh interface ipv6" command.</span></span> <span data-ttu-id="3bbc0-109">使用 Netsh.exe 命令所做的設定變更是永久性的，而且在重新開機電腦或 IPv6 通訊協定時不會遺失。</span><span class="sxs-lookup"><span data-stu-id="3bbc0-109">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="3bbc0-110">下列命令可在 Windows XP SP1 和更新版本上使用，以在本機電腦上查詢和設定 IPv6：</span><span class="sxs-lookup"><span data-stu-id="3bbc0-110">The following command is available on Windows XP with SP1 and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="3bbc0-111">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="3bbc0-111">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="3bbc0-112">在 Windows XP Service Pack 1 (SP1) 之前，IPv6 設定和管理使用了數個較舊的命令列工具來設定和管理 IPv6。</span><span class="sxs-lookup"><span data-stu-id="3bbc0-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools to configure and manage IPv6.</span></span> <span data-ttu-id="3bbc0-113">使用這些較舊的工具，IPv6 變更不是永久性的，而且會在電腦或 IPv6 通訊協定重新開機時遺失。</span><span class="sxs-lookup"><span data-stu-id="3bbc0-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span>

<span data-ttu-id="3bbc0-114">Windows XP 上提供下列舊版命令</span><span class="sxs-lookup"><span data-stu-id="3bbc0-114">The following older commands are available on Windows XP</span></span>

-   [<span data-ttu-id="3bbc0-115">Net.exe</span><span class="sxs-lookup"><span data-stu-id="3bbc0-115">Net.exe</span></span>](net-exe-2.md)
-   [<span data-ttu-id="3bbc0-116">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="3bbc0-116">Ipv6.exe</span></span>](ipv6-exe-2.md)
-   [<span data-ttu-id="3bbc0-117">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="3bbc0-117">Ipsec6.exe</span></span>](ipsec6-exe-2.md)

<span data-ttu-id="3bbc0-118">Windows 2000 的 IPv6 技術預覽也提供這些舊版工具。</span><span class="sxs-lookup"><span data-stu-id="3bbc0-118">These older tools were also provided in the IPv6 Technology Preview for Windows 2000</span></span>

<span data-ttu-id="3bbc0-119">使用這些舊版工具的設定變更，可以藉由將它們作為命令列放在命令腳本檔中， ( .cmd) 在重新開機電腦或 IPv6 通訊協定之後執行。</span><span class="sxs-lookup"><span data-stu-id="3bbc0-119">Configuration changes using these older tools could be maintained by placing them as command lines in a command script file (.cmd) that is run after restarting the computer or the IPv6 protocol.</span></span> <span data-ttu-id="3bbc0-120">若要在重新開機後自動復原設定變更，可以在電腦啟動時使用 Windows 排程工作來執行 .cmd 檔。</span><span class="sxs-lookup"><span data-stu-id="3bbc0-120">To reinstate configuration changes automatically after restarting, is was possible to use the Windows Scheduled Tasks to run the .cmd file when the computer starts.</span></span>

<span data-ttu-id="3bbc0-121">Windows Server 2003 和更新版本上不提供這些舊版工具。</span><span class="sxs-lookup"><span data-stu-id="3bbc0-121">These older tools are not provided on Windows Server 2003 and later.</span></span> <span data-ttu-id="3bbc0-122">您可以從 Windows Server 2003 和更新版本的命令列，提供「netsh interface ipv6」工具來設定和管理 IPv6。</span><span class="sxs-lookup"><span data-stu-id="3bbc0-122">The "netsh interface ipv6" tool is provided for configuring and managing IPv6 from the command-line on Windows Server 2003 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bbc0-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="3bbc0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bbc0-124">網際網路通訊協定第6版 (IPv6) </span><span class="sxs-lookup"><span data-stu-id="3bbc0-124">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="3bbc0-125">適用于 Windows 通訊端應用程式的 IPv6 指南</span><span class="sxs-lookup"><span data-stu-id="3bbc0-125">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="3bbc0-126">適用于 Windows 2000 的 IPv6 技術預覽</span><span class="sxs-lookup"><span data-stu-id="3bbc0-126">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



