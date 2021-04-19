---
title: 遠端桌面通訊協定
description: Microsoft 遠端桌面通訊協定 (RDP) 針對在伺服器上執行的 Windows 應用程式，提供網路連線的遠端顯示和輸入功能。
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- 遠端桌面通訊協定 (RDP) 遠端桌面服務
- 'RDP (請參閱遠端桌面通訊協定) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7895163a5ee92a6cc756dca9b097db8498d02e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967901"
---
# <a name="remote-desktop-protocol"></a><span data-ttu-id="876f7-105">遠端桌面通訊協定</span><span class="sxs-lookup"><span data-stu-id="876f7-105">Remote Desktop Protocol</span></span>

<span data-ttu-id="876f7-106">Microsoft 遠端桌面通訊協定 (RDP) 針對在伺服器上執行的 Windows 應用程式，提供網路連線的遠端顯示和輸入功能。</span><span class="sxs-lookup"><span data-stu-id="876f7-106">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span> <span data-ttu-id="876f7-107">RDP 的設計是為了支援不同類型的網路拓撲和多個 LAN 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="876f7-107">RDP is designed to support different types of network topologies and multiple LAN protocols.</span></span>

> [!Note]  
> <span data-ttu-id="876f7-108">本主題適用于軟體發展人員。</span><span class="sxs-lookup"><span data-stu-id="876f7-108">This topic is for software developers.</span></span> <span data-ttu-id="876f7-109">如果您要尋找遠端桌面的使用者資訊，請參閱 [Windows 支援](https://windows.microsoft.com/windows/support#1TC=windows-8)。</span><span class="sxs-lookup"><span data-stu-id="876f7-109">If you are looking for user information for Remote Desktop, see [Windows Support](https://windows.microsoft.com/windows/support#1TC=windows-8).</span></span> <span data-ttu-id="876f7-110">如果您要尋找遠端桌面的 IT 專業人員資訊，請參閱 [TechNet 上的遠端桌面服務](/windows/deployment/deploy-whats-new)。</span><span class="sxs-lookup"><span data-stu-id="876f7-110">If you are looking for IT professional information for Remote Desktop, see [Remote Desktop Services on TechNet](/windows/deployment/deploy-whats-new).</span></span>

 

## <a name="basic-architecture"></a><span data-ttu-id="876f7-111">基本架構</span><span class="sxs-lookup"><span data-stu-id="876f7-111">Basic Architecture</span></span>

<span data-ttu-id="876f7-112">RDP 是根據 ITU T. 120 系列通訊協定的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="876f7-112">RDP is based on, and an extension of, the ITU T.120 family of protocols.</span></span> <span data-ttu-id="876f7-113">RDP 是支援多通道的通訊協定，可讓不同的虛擬通道攜帶裝置通訊和來自伺服器的簡報資料，以及加密的用戶端滑鼠和鍵盤資料。</span><span class="sxs-lookup"><span data-stu-id="876f7-113">RDP is a multiple-channel capable protocol that allows for separate virtual channels for carrying device communication and presentation data from the server, as well as encrypted client mouse and keyboard data.</span></span> <span data-ttu-id="876f7-114">RDP 提供可延伸的基底，並支援最多64000個不同的通道，以進行資料傳輸和 multipoint 傳輸的布建。</span><span class="sxs-lookup"><span data-stu-id="876f7-114">RDP provides an extensible base and supports up to 64,000 separate channels for data transmission and provisions for multipoint transmission.</span></span>

<span data-ttu-id="876f7-115">在伺服器上，RDP 使用自己的視頻驅動程式來轉譯顯示輸出，其方式是使用 RDP 通訊協定將轉譯資訊建立到網路封包，並透過網路將其傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="876f7-115">On the server, RDP uses its own video driver to render display output by constructing the rendering information into network packets by using RDP protocol and sending them over the network to the client.</span></span> <span data-ttu-id="876f7-116">在用戶端上，RDP 會接收轉譯資料，並將封包轉譯成對應的 Microsoft Windows 圖形裝置介面 (GDI) API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="876f7-116">On the client, RDP receives rendering data and interprets the packets into corresponding Microsoft Windows graphics device interface (GDI) API calls.</span></span> <span data-ttu-id="876f7-117">針對輸入路徑，用戶端滑鼠和鍵盤事件會從用戶端重新導向至伺服器。</span><span class="sxs-lookup"><span data-stu-id="876f7-117">For the input path, client mouse and keyboard events are redirected from the client to the server.</span></span> <span data-ttu-id="876f7-118">在伺服器上，RDP 使用自己的鍵盤和滑鼠驅動程式來接收這些鍵盤和滑鼠事件。</span><span class="sxs-lookup"><span data-stu-id="876f7-118">On the server, RDP uses its own keyboard and mouse driver to receive these keyboard and mouse events.</span></span>

<span data-ttu-id="876f7-119">在遠端桌面會話中，所有環境變數（例如，決定色彩深度和壁紙啟用和停用的變數）都是由 RCP-Tcp 連接設定所決定。</span><span class="sxs-lookup"><span data-stu-id="876f7-119">In a Remote Desktop session, all environment variables—for example, variables determining color depth and wallpaper enabling and disabling—are determined by the RCP-Tcp connection settings.</span></span> <span data-ttu-id="876f7-120">這適用于在 [遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md) 中設定環境變數的所有函數和方法，以及 [遠端桌面服務 WMI 提供者介面](terminal-services-wmi-provider-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="876f7-120">This applies to all functions and methods that set environment variables in the [Remote Desktop Web Connection Reference](remote-desktop-web-connection-reference.md) and the [Remote Desktop Services WMI Provider interface](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="features"></a><span data-ttu-id="876f7-121">功能</span><span class="sxs-lookup"><span data-stu-id="876f7-121">Features</span></span>

<span data-ttu-id="876f7-122">Microsoft RDP 包含下列特性和功能：</span><span class="sxs-lookup"><span data-stu-id="876f7-122">Microsoft RDP includes the following features and capabilities:</span></span>

<dl> <dt>

<span data-ttu-id="876f7-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>加密</span><span class="sxs-lookup"><span data-stu-id="876f7-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Encryption</span></span>
</dt> <dd>

<span data-ttu-id="876f7-124">RDP 使用 RSA 安全性的 RC4 密碼，這是專為有效率地加密少量資料而設計的資料流程加密。</span><span class="sxs-lookup"><span data-stu-id="876f7-124">RDP uses RSA Security's RC4 cipher, a stream cipher designed to efficiently encrypt small amounts of data.</span></span> <span data-ttu-id="876f7-125">RC4 是針對透過網路的安全通訊所設計。</span><span class="sxs-lookup"><span data-stu-id="876f7-125">RC4 is designed for secure communications over networks.</span></span> <span data-ttu-id="876f7-126">系統管理員可以選擇使用56或128位金鑰來加密資料。</span><span class="sxs-lookup"><span data-stu-id="876f7-126">Administrators can choose to encrypt data by using a 56- or 128-bit key.</span></span>

</dd> <dt>

<span data-ttu-id="876f7-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>頻寬減少功能</span><span class="sxs-lookup"><span data-stu-id="876f7-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Bandwidth reduction features</span></span>
</dt> <dd>

<span data-ttu-id="876f7-128">RDP 支援各種機制來減少透過網路連線傳輸的資料量。</span><span class="sxs-lookup"><span data-stu-id="876f7-128">RDP supports various mechanisms to reduce the amount of data transmitted over a network connection.</span></span> <span data-ttu-id="876f7-129">機制包括資料壓縮、持續快取點陣圖，以及在 RAM 中快取圖像和片段。</span><span class="sxs-lookup"><span data-stu-id="876f7-129">Mechanisms include data compression, persistent caching of bitmaps, and caching of glyphs and fragments in RAM.</span></span> <span data-ttu-id="876f7-130">持續性點陣圖快取可大幅改善低頻寬連接的效能，特別是在執行大量使用大型點陣圖的應用程式時。</span><span class="sxs-lookup"><span data-stu-id="876f7-130">The persistent bitmap cache can provide a substantial improvement in performance over low-bandwidth connections, especially when running applications that make extensive use of large bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="876f7-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>漫遊中斷連線</span><span class="sxs-lookup"><span data-stu-id="876f7-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Roaming disconnect</span></span>
</dt> <dd>

<span data-ttu-id="876f7-132">使用者可以手動中斷與遠端桌面會話的連線，而不需要登出。</span><span class="sxs-lookup"><span data-stu-id="876f7-132">A user can manually disconnect from a remote desktop session without logging off.</span></span> <span data-ttu-id="876f7-133">當使用者從相同的裝置或不同的裝置登入系統時，會自動重新連線到中斷連線的會話。</span><span class="sxs-lookup"><span data-stu-id="876f7-133">The user is automatically reconnected to their disconnected session when he or she logs back onto the system, either from the same device or a different device.</span></span> <span data-ttu-id="876f7-134">當網路或用戶端失敗意外終止使用者的會話時，使用者就會中斷連線，但不會登出。</span><span class="sxs-lookup"><span data-stu-id="876f7-134">When a user's session is unexpectedly terminated by a network or client failure, the user is disconnected but not logged off.</span></span>

</dd> <dt>

<span data-ttu-id="876f7-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>剪貼簿對應</span><span class="sxs-lookup"><span data-stu-id="876f7-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Clipboard mapping</span></span>
</dt> <dd>

<span data-ttu-id="876f7-136">使用者可以刪除、複製和貼上在本機電腦上執行的應用程式，以及在遠端桌面會話中執行的應用程式，以及會話之間的文字和圖形。</span><span class="sxs-lookup"><span data-stu-id="876f7-136">Users can delete, copy, and paste text and graphics between applications running on the local computer and those running in a remote desktop session, and between sessions.</span></span>

</dd> <dt>

<span data-ttu-id="876f7-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>列印重新導向</span><span class="sxs-lookup"><span data-stu-id="876f7-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Print redirection</span></span>
</dt> <dd>

<span data-ttu-id="876f7-138">在遠端桌面會話中執行的應用程式可以列印到連接到用戶端裝置的印表機。</span><span class="sxs-lookup"><span data-stu-id="876f7-138">Applications running within a remote desktop session can print to a printer attached to the client device.</span></span>

</dd> <dt>

<span data-ttu-id="876f7-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>虛擬通道</span><span class="sxs-lookup"><span data-stu-id="876f7-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Virtual channels</span></span>
</dt> <dd>

<span data-ttu-id="876f7-140">藉由使用 RDP 虛擬通道架構，您可以擴充現有的應用程式，並開發新的應用程式來新增需要用戶端裝置與遠端桌面會話中執行之應用程式之間通訊的功能。</span><span class="sxs-lookup"><span data-stu-id="876f7-140">By using RDP virtual channel architecture, existing applications can be augmented and new applications can be developed to add features that require communications between the client device and an application running in a remote desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="876f7-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>遙控</span><span class="sxs-lookup"><span data-stu-id="876f7-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Remote control</span></span>
</dt> <dd>

<span data-ttu-id="876f7-142">電腦支援人員可以查看及控制遠端桌面會話。</span><span class="sxs-lookup"><span data-stu-id="876f7-142">Computer support staff can view and control a remote desktop session.</span></span> <span data-ttu-id="876f7-143">在兩個遠端桌面會話之間共用輸入和顯示圖形，可讓支援人員能夠從遠端診斷和解決問題。</span><span class="sxs-lookup"><span data-stu-id="876f7-143">Sharing input and display graphics between two remote desktop sessions gives a support person the ability to diagnose and resolve problems remotely.</span></span>

</dd> <dt>

<span data-ttu-id="876f7-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>網路負載平衡</span><span class="sxs-lookup"><span data-stu-id="876f7-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network load balancing</span></span>
</dt> <dd>

<span data-ttu-id="876f7-145">RDP 會利用 (NLB) 的網路負載平衡（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="876f7-145">RDP takes advantage of network load balancing (NLB), where available.</span></span>

</dd> </dl>

<span data-ttu-id="876f7-146">此外，RDP 包含下列功能：</span><span class="sxs-lookup"><span data-stu-id="876f7-146">In addition, RDP contains the following features:</span></span>

-   <span data-ttu-id="876f7-147">支援24位色彩。</span><span class="sxs-lookup"><span data-stu-id="876f7-147">Support for 24-bit color.</span></span>
-   <span data-ttu-id="876f7-148">藉由減少頻寬來改善低速度的撥號連線效能。</span><span class="sxs-lookup"><span data-stu-id="876f7-148">Improved performance over low-speed dial-up connections through reduced bandwidth.</span></span>
-   <span data-ttu-id="876f7-149">透過遠端桌面服務的智慧卡驗證。</span><span class="sxs-lookup"><span data-stu-id="876f7-149">Smart Card authentication through Remote Desktop Services.</span></span>
-   <span data-ttu-id="876f7-150">鍵盤掛鉤。</span><span class="sxs-lookup"><span data-stu-id="876f7-150">Keyboard hooking.</span></span> <span data-ttu-id="876f7-151">將特殊 Windows 按鍵組合（以全螢幕模式）導向本機電腦或遠端電腦的能力。</span><span class="sxs-lookup"><span data-stu-id="876f7-151">The ability to direct special Windows key combinations, in full-screen mode, to the local computer or to a remote computer.</span></span>
-   <span data-ttu-id="876f7-152">音效、磁片磁碟機、埠和網路印表機重新導向。</span><span class="sxs-lookup"><span data-stu-id="876f7-152">Sound, drive, port, and network printer redirection.</span></span> <span data-ttu-id="876f7-153">在用戶端電腦上執行 RDC 用戶端時，可能會聽到遠端電腦上發生的音效，遠端桌面會話將可看到本機用戶端磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="876f7-153">Sounds that occur on the remote computer can be heard on the client computer running the RDC client, and local client drives will be visible to the remote desktop session.</span></span>

 

 