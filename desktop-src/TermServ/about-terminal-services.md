---
title: 關於遠端桌面服務
description: 遠端桌面服務 (前身為終端機服務) 提供的功能類似于以終端為基礎、集中式主機或大型主機，也就是多個終端機連接到主機電腦的環境。
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- 遠端桌面服務遠端桌面服務，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966413"
---
# <a name="about-remote-desktop-services"></a><span data-ttu-id="1a1a9-104">關於遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="1a1a9-104">About Remote Desktop Services</span></span>

<span data-ttu-id="1a1a9-105">遠端桌面服務 (前身為終端機服務) 提供的功能類似于以終端為基礎、集中式主機或大型主機，也就是多個終端機連接到主機電腦的環境。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-105">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span> <span data-ttu-id="1a1a9-106">每個終端機都會在使用者與主機電腦之間提供輸入和輸出的管道。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-106">Each terminal provides a conduit for input and output between a user and the host computer.</span></span> <span data-ttu-id="1a1a9-107">使用者可以在終端機登入，然後在主機電腦上執行應用程式，存取檔案、資料庫、網路資源等等。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-107">A user can log on at a terminal, and then run applications on the host computer, accessing files, databases, network resources, and so on.</span></span> <span data-ttu-id="1a1a9-108">每個終端機會話都是獨立的，而且主機作業系統會管理多個使用者爭用共用資源之間的衝突。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-108">Each terminal session is independent, with the host operating system managing conflicts between multiple users contending for shared resources.</span></span>

<span data-ttu-id="1a1a9-109">遠端桌面服務與傳統大型主機環境之間的主要差異，在於大型主機環境中的啞端子只提供以字元為基礎的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-109">The primary difference between Remote Desktop Services and the traditional mainframe environment is that the dumb terminals in a mainframe environment only provide character-based input and output.</span></span> <span data-ttu-id="1a1a9-110">遠端桌面連線 (RDC) 用戶端或模擬器提供完整的圖形化使用者介面，包括 Windows 作業系統桌面，以及各種輸入裝置（例如鍵盤和滑鼠）的支援。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-110">A Remote Desktop Connection (RDC) client or emulator provides a complete graphical user interface including a Windows operating system desktop and support for a variety of input devices, such as a keyboard and mouse.</span></span>

<span data-ttu-id="1a1a9-111">在遠端桌面服務環境中，應用程式完全是在遠端桌面工作階段主機 (RD 工作階段主機) server (先前稱為終端機伺服器) 上執行。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-111">In the Remote Desktop Services environment, an application runs entirely on the Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server).</span></span> <span data-ttu-id="1a1a9-112">RDC 用戶端不會執行應用程式軟體的本機處理。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-112">The RDC client performs no local processing of application software.</span></span> <span data-ttu-id="1a1a9-113">伺服器會將圖形化使用者介面傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-113">The server transmits the graphical user interface to the client.</span></span> <span data-ttu-id="1a1a9-114">用戶端會將使用者的輸入傳送回伺服器。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-114">The client transmits the user's input back to the server.</span></span>

<span data-ttu-id="1a1a9-115">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1a1a9-116">本節內容</span><span class="sxs-lookup"><span data-stu-id="1a1a9-116">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="1a1a9-117">修改裝置重新導向預設值</span><span class="sxs-lookup"><span data-stu-id="1a1a9-117">Modify Device Redirection Default</span></span>](modify-device-redirection-default-.md)
</dt> <dd>

<span data-ttu-id="1a1a9-118">因為遠端桌面閘道伺服器在將用戶端連線傳遞到遠端桌面工作階段主機伺服器之前，嘗試強制執行安全的裝置重新導向原則，所以在某些情況下，您可能需要停用此預設值。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-118">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

</dd> <dt>

[<span data-ttu-id="1a1a9-119">遠端桌面通訊協定</span><span class="sxs-lookup"><span data-stu-id="1a1a9-119">Remote Desktop Protocol</span></span>](remote-desktop-protocol.md)
</dt> <dd>

<span data-ttu-id="1a1a9-120">Microsoft 遠端桌面通訊協定 (RDP) 針對在伺服器上執行的 Windows 應用程式，提供網路連線的遠端顯示和輸入功能。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-120">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span>

</dd> <dt>

[<span data-ttu-id="1a1a9-121">遠端桌面服務 API</span><span class="sxs-lookup"><span data-stu-id="1a1a9-121">Remote Desktop Services API</span></span>](terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="1a1a9-122">遠端桌面服務 API 主要適用于遠端桌面服務管理的用戶端/伺服器應用程式和應用程式。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-122">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

</dd> <dt>

[<span data-ttu-id="1a1a9-123">遠端桌面服務管理應用程式</span><span class="sxs-lookup"><span data-stu-id="1a1a9-123">Remote Desktop Services management applications</span></span>](terminal-services-management-applications.md)
</dt> <dd>

<span data-ttu-id="1a1a9-124">描述遠端桌面服務支援的管理應用程式。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-124">Describes the management applications that Remote Desktop Services supports.</span></span>

</dd> <dt>

[<span data-ttu-id="1a1a9-125">遠端桌面服務程式設計指導方針</span><span class="sxs-lookup"><span data-stu-id="1a1a9-125">Remote Desktop Services programming guidelines</span></span>](terminal-services-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="1a1a9-126">本主題提供在遠端桌面服務環境中開發應用程式的指導方針。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-126">Topics that provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="1a1a9-127">遠端桌面會話</span><span class="sxs-lookup"><span data-stu-id="1a1a9-127">Remote Desktop Sessions</span></span>](terminal-services-sessions.md)
</dt> <dd>

<span data-ttu-id="1a1a9-128">因為每次登入遠端桌面連線 (RDC) 用戶端會收到個別的會話識別碼，所以使用者體驗類似于同時登入多部電腦;例如，辦公室電腦和家用電腦。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-128">Because each logon to a Remote Desktop Connection (RDC) client receives a separate session ID, the user-experience is similar to being logged on to multiple computers at the same time; for example, an office computer and a home computer.</span></span>

</dd> <dt>

[<span data-ttu-id="1a1a9-129">遠端桌面網頁連線</span><span class="sxs-lookup"><span data-stu-id="1a1a9-129">Remote Desktop Web Connection</span></span>](remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="1a1a9-130">說明如何安裝遠端桌面網頁連線。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-130">Describes how to install a Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="1a1a9-131">遠端桌面工作階段主機伺服器上的資源</span><span class="sxs-lookup"><span data-stu-id="1a1a9-131">Resources on a Remote Desktop Session Host Server</span></span>](resources-on-a-terminal-server.md)
</dt> <dd>

<span data-ttu-id="1a1a9-132">多個使用者可以同時登入單一 RD 工作階段主機伺服器，並共用伺服器的硬體和軟體資源。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-132">Multiple users can log on simultaneously to a single RD Session Host server, sharing the hardware and software resources of the server.</span></span>

</dd> <dt>

[<span data-ttu-id="1a1a9-133">遠端桌面服務的新功能</span><span class="sxs-lookup"><span data-stu-id="1a1a9-133">What's New in Remote Desktop Services</span></span>](what-s-new-in-terminal-services.md)
</dt> <dd>

<span data-ttu-id="1a1a9-134">描述每個遠端桌面服務 API 版本中變更的主題。</span><span class="sxs-lookup"><span data-stu-id="1a1a9-134">Topics that describe the changes in each release of the Remote Desktop Services API.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="1a1a9-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a1a9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a1a9-136">使用遠端桌面連線連接到其他電腦</span><span class="sxs-lookup"><span data-stu-id="1a1a9-136">Connect to another computer using Remote Desktop Connection</span></span>](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




