---
title: 遠端桌面 ActiveX 控制項隨附的範例網頁
description: 遠端桌面網頁連線安裝所在的目錄中 (Default.htm) 的範例網頁。
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec07ee86dcb5d10dc289e8095c83771ebe9a8b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301080"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a><span data-ttu-id="f3e6f-103">遠端桌面 ActiveX 控制項隨附的範例網頁</span><span class="sxs-lookup"><span data-stu-id="f3e6f-103">Sample webpage included with the Remote Desktop ActiveX control</span></span>

<span data-ttu-id="f3e6f-104">當您安裝遠端桌面網頁連線的遠端桌面 ActiveX 控制項時，會將範例網頁 (Default.htm) 複製到遠端桌面網頁連線安裝所在的目錄。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-104">When you install the Remote Desktop ActiveX control of Remote Desktop Web Connection, a sample webpage (Default.htm) is copied to the directory where Remote Desktop Web Connection is installed.</span></span> <span data-ttu-id="f3e6f-105">此頁面可以依原樣執行或自訂，以符合使用者或組織的需求。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-105">This page can be run as-is or customized to fit the needs of a user or an organization.</span></span>

<span data-ttu-id="f3e6f-106">範例網頁必須安裝在執行 Windows Server 和 Internet Information Server 4.0 或更新版本的 web 伺服器上。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-106">The sample webpage must be installed on a web server running Windows Server and Internet Information Server 4.0 or later.</span></span> <span data-ttu-id="f3e6f-107">此外，用戶端電腦上的瀏覽器應該 Internet Explorer 4.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-107">Also, the browser on the client computer should be Internet Explorer version 4.0 or later.</span></span> <span data-ttu-id="f3e6f-108">如需詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-108">For more information, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

<span data-ttu-id="f3e6f-109">Default.htm 是預設的登入網頁，會收集使用者的連接資訊。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-109">Default.htm is a default logon webpage that collects connection information from the user.</span></span> <span data-ttu-id="f3e6f-110">登入頁面包含一個必要欄位，使用者可在其中輸入要連接的遠端桌面工作階段主機 (RD 工作階段主機) 伺服器或遠端電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-110">The logon page contains one required field into which the user enters the name of the Remote Desktop Session Host (RD Session Host) server or remote computer to connect to.</span></span> <span data-ttu-id="f3e6f-111">登入頁面也包含螢幕大小和使用者登入資訊的選擇性欄位，包括使用者名稱和網域。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-111">The logon page also includes optional fields for screen size and user logon information, including user name and domain.</span></span>

<span data-ttu-id="f3e6f-112">收集使用者資料之後，Default.htm 會將它傳遞到遠端桌面 ActiveX 控制項 (Msrdp) 以起始遠端桌面會話。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-112">After collecting the user data, Default.htm passes it to the Remote Desktop ActiveX control (Msrdp.ocx) to initiate a remote desktop session.</span></span> <span data-ttu-id="f3e6f-113">初始化會話所需的步驟如下：</span><span class="sxs-lookup"><span data-stu-id="f3e6f-113">The steps involved in initiating the session are the following:</span></span>

1.  <span data-ttu-id="f3e6f-114">如有必要，Internet Explorer 下載 .cab 檔，並將它安裝在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-114">If necessary, Internet Explorer downloads the .cab file and installs it on the user's computer.</span></span>
2.  <span data-ttu-id="f3e6f-115">使用者會在適當的欄位中輸入遠端電腦的完整功能變數名稱或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-115">The user enters the fully qualified domain name or IP address of the remote computer in the appropriate field.</span></span>

    -   <span data-ttu-id="f3e6f-116">使用者可以選擇性地指定連接的螢幕大小。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-116">The user can optionally specify a screen size for the connection.</span></span> <span data-ttu-id="f3e6f-117">如果使用者未指定螢幕大小，則會話會在全螢幕模式中開啟（如果使用者位於受信任的 URL 安全性區域中）。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-117">If the user does not specify a screen size, the session opens in full-screen mode if the user is in a trusted URL security zone.</span></span> <span data-ttu-id="f3e6f-118">否則，會話會在視窗模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-118">Otherwise, the session opens in window mode.</span></span>
    -   <span data-ttu-id="f3e6f-119">使用者可以選擇性地為遠端會話 (的使用者名稱、網域) 提供自動登入資訊。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-119">The user can optionally supply automatic logon information (user name, domain) for the remote session.</span></span>

3.  <span data-ttu-id="f3e6f-120">當使用者按一下 [ **連接]** 按鈕時，Default.htm 會將使用者提供的資料做為參數傳遞給遠端桌面 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-120">When the user clicks the **Connect** button, Default.htm passes the user-supplied data as parameters to the Remote Desktop ActiveX control.</span></span>
4.  <span data-ttu-id="f3e6f-121">遠端桌面會在瀏覽器視窗中開啟，或在全螢幕模式中開啟（由使用者所指定）。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-121">The remote desktop opens in the browser window or in full-screen mode, as specified by the user.</span></span>

<span data-ttu-id="f3e6f-122">當 Default.htm 第一次使用 Internet Explorer 開啟時，會出現一個對話方塊，讓使用者可以選擇下載遠端桌面 ActiveX 控制項 (Msrdp .ocx) 。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-122">When Default.htm opens for the first time using Internet Explorer, a dialog box appears giving the user the option to download the Remote Desktop ActiveX control (Msrdp.ocx).</span></span> <span data-ttu-id="f3e6f-123">此對話方塊會在下列條件下出現：</span><span class="sxs-lookup"><span data-stu-id="f3e6f-123">The dialog box appears under the following conditions:</span></span>

-   <span data-ttu-id="f3e6f-124">存取網頁的電腦未完整安裝遠端桌面網頁連線用戶端 (或遠端桌面服務進階用戶端) 有 Web 支援。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-124">The computer that accessed the webpage does not have a full installation of the Remote Desktop Web Connection client (or the Remote Desktop Services Advanced Client) with web support.</span></span>
-   <span data-ttu-id="f3e6f-125">用戶端電腦上安裝的 .cab 檔案版本比 Default.htm 網頁上的版本還舊。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-125">The installed version of the .cab file on the client computer is older than the version on the Default.htm webpage.</span></span>

<span data-ttu-id="f3e6f-126">顯示在瀏覽器視窗中的遠端桌面會話大小是 Default.htm 網頁中指定的大小。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-126">The size of the remote desktop session that appears in the browser window is the size specified in the Default.htm webpage.</span></span> <span data-ttu-id="f3e6f-127">若要變更螢幕大小，使用者必須從會話中斷連線、回到 Default.htm 網頁，然後編輯連接資訊。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-127">To change the screen size, the user must disconnect from the session, return to the Default.htm webpage and edit the connection information.</span></span> <span data-ttu-id="f3e6f-128">如果未指定任何螢幕大小，則會話會在預設全螢幕模式的瀏覽器視窗中開啟。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-128">If no screen size was specified, the session opens in the browser window in the default full-screen mode.</span></span> <span data-ttu-id="f3e6f-129">在此解決方案中，遠端桌面會展開以符合使用者畫面的完整尺寸，而不會顯示 Internet Explorer 瀏覽器工具列和視窗框架。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-129">At this resolution the remote desktop expands to match the full dimensions of the user's screen and the Internet Explorer browser toolbars and window frames do not display.</span></span> <span data-ttu-id="f3e6f-130">如同 full 遠端桌面連線用戶端，使用者可以按全螢幕模式 [快速鍵](terminal-services-shortcut-keys.md) 組合 (CTRL + ALT + BREAK) 來切換全螢幕和視窗模式。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-130">As with the full Remote Desktop Connection client, the user can toggle between full-screen and window mode by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="f3e6f-131">基於安全性理由，在遠端桌面 ActiveX 控制項中，某些遠端桌面服務連線管理員可用的選項會限制為特定 Internet Explorer URL 安全性區域。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-131">For security reasons, some options that are available in the Remote Desktop Services Connection Manager are restricted in the Remote Desktop ActiveX control to certain Internet Explorer URL security zones.</span></span> <span data-ttu-id="f3e6f-132">請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 的詳細資訊，以取得有關這些選項的詳細資訊，以及指定在連接時要執行的程式。</span><span class="sxs-lookup"><span data-stu-id="f3e6f-132">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about these options and about specifying a program to run upon connection.</span></span>

 

 




