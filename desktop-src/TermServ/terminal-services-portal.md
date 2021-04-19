---
title: '遠端桌面服務 (遠端桌面服務) '
description: Microsoft 遠端桌面服務是支援遠端桌面存取的遠端電腦存取軟體。 遠端桌面服務會將多個用戶端連接至遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- 遠端桌面服務遠端桌面服務
- 遠端桌面服務遠端桌面服務，首頁
- 終端機服務查看遠端桌面服務遠端桌面服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39e176473c98f1e240d58592463df749a95f939
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967706"
---
# <a name="remote-desktop-services-remote-desktop-services"></a><span data-ttu-id="017fd-107">遠端桌面服務 (遠端桌面服務) </span><span class="sxs-lookup"><span data-stu-id="017fd-107">Remote Desktop Services (Remote Desktop Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="017fd-108">目的</span><span class="sxs-lookup"><span data-stu-id="017fd-108">Purpose</span></span>

<span data-ttu-id="017fd-109">Windows Server 2012 R2、Windows Server 2012、Windows Server 2008 R2 或 Windows Server 2008 （具有遠端桌面服務 (前身為終端機服務）) 讓伺服器同時裝載多個用戶端會話。</span><span class="sxs-lookup"><span data-stu-id="017fd-109">Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 with Remote Desktop Services (formerly known as Terminal Services) allow a server to host multiple, simultaneous client sessions.</span></span> <span data-ttu-id="017fd-110">遠端桌面使用遠端桌面服務技術，讓單一會話可以從遠端執行。</span><span class="sxs-lookup"><span data-stu-id="017fd-110">Remote Desktop uses Remote Desktop Services technology to allow a single session to run remotely.</span></span> <span data-ttu-id="017fd-111">使用者可以使用 () RDC 遠端桌面連線用戶端軟體，連接到遠端桌面工作階段主機 (RD 工作階段主機) server (先前稱為終端機伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="017fd-111">A user can connect to a Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server) by using Remote Desktop Connection (RDC) client software.</span></span> <span data-ttu-id="017fd-112">遠端桌面網頁連線將遠端桌面服務的技術延伸至網路。</span><span class="sxs-lookup"><span data-stu-id="017fd-112">The Remote Desktop Web Connection extends Remote Desktop Services technology to the web.</span></span>

> [!Note]  
> <span data-ttu-id="017fd-113">本主題適用于軟體發展人員。</span><span class="sxs-lookup"><span data-stu-id="017fd-113">This topic is for software developers.</span></span> <span data-ttu-id="017fd-114">如果您要尋找遠端桌面連線的使用者資訊，請參閱 [遠端桌面連線：常見問題](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8)。</span><span class="sxs-lookup"><span data-stu-id="017fd-114">If you are looking for user information for Remote Desktop connections, See [Remote Desktop Connection: frequently asked questions](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="017fd-115">適用時</span><span class="sxs-lookup"><span data-stu-id="017fd-115">Where applicable</span></span>

<span data-ttu-id="017fd-116">遠端桌面連線 (RDC) 用戶端可以存在於各種不同的表單中。</span><span class="sxs-lookup"><span data-stu-id="017fd-116">A Remote Desktop Connection (RDC) client can exist in a variety of forms.</span></span> <span data-ttu-id="017fd-117">執行內嵌 Windows 作業系統的瘦用戶端硬體裝置可以執行 RDC 用戶端軟體，以連接到 RD 工作階段主機伺服器。</span><span class="sxs-lookup"><span data-stu-id="017fd-117">Thin-client hardware devices that run an embedded Windows-based operating system can run the RDC client software to connect to an RD Session Host server.</span></span> <span data-ttu-id="017fd-118">Windows-、Macintosh 或 UNIX 電腦可以執行 RDC 用戶端軟體，以連線到 RD 工作階段主機伺服器以顯示 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="017fd-118">Windows-, Macintosh-, or UNIX-based computers can run RDC client software to connect to an RD Session Host server to display Windows-based applications.</span></span> <span data-ttu-id="017fd-119">這種 RDC 用戶端組合可讓您從幾乎任何作業系統存取以 Windows 為基礎的應用程式。</span><span class="sxs-lookup"><span data-stu-id="017fd-119">This combination of RDC clients provides access to Windows-based applications from virtually any operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="017fd-120">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="017fd-120">Developer audience</span></span>

<span data-ttu-id="017fd-121">使用遠端桌面服務的開發人員應該熟悉 C 和 c + + 程式設計語言，以及 Windows 架構的程式設計環境。</span><span class="sxs-lookup"><span data-stu-id="017fd-121">Developers who use Remote Desktop Services should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="017fd-122">需要熟悉用戶端/伺服器架構。</span><span class="sxs-lookup"><span data-stu-id="017fd-122">Familiarity with client/server architecture is required.</span></span> <span data-ttu-id="017fd-123">遠端桌面網頁連線包含可編寫腳本的介面，可在遠端桌面服務 Web 應用程式中建立和部署可編寫腳本的虛擬通道。</span><span class="sxs-lookup"><span data-stu-id="017fd-123">The Remote Desktop Web Connection includes scriptable interfaces to create and deploy scriptable virtual channels within Remote Desktop Services web applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="017fd-124">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="017fd-124">Run-time requirements</span></span>

<span data-ttu-id="017fd-125">使用遠端桌面服務的應用程式需要 Windows Server 2012 R2、Windows 8.1、Windows Server 2012、Windows 8、Windows Server 2008 R2、Windows 7、Windows Server 2008 或 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="017fd-125">Applications that use Remote Desktop Services require Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, or Windows Vista.</span></span> <span data-ttu-id="017fd-126">若要使用遠端桌面網頁連線的功能，遠端桌面服務用戶端應用程式需要 Internet Explorer 和全球 Web 的連接。</span><span class="sxs-lookup"><span data-stu-id="017fd-126">To use Remote Desktop Web Connection functionality, the Remote Desktop Services client application requires Internet Explorer and a connection to the World Wide Web.</span></span> <span data-ttu-id="017fd-127">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。</span><span class="sxs-lookup"><span data-stu-id="017fd-127">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="017fd-128">本節內容</span><span class="sxs-lookup"><span data-stu-id="017fd-128">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="017fd-129">遠端桌面 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="017fd-129">Remote Desktop ActiveX control</span></span>](remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="017fd-130">說明如何使用遠端桌面 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="017fd-130">Describes how to use the Remote Desktop ActiveX control.</span></span>

</dd> <dt>

[<span data-ttu-id="017fd-131">遠端桌面通訊協定提供者 API</span><span class="sxs-lookup"><span data-stu-id="017fd-131">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dd>

<span data-ttu-id="017fd-132">您可以使用遠端桌面通訊協定提供者 API 來建立通訊協定，以提供遠端桌面服務服務與多個用戶端之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="017fd-132">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

</dd> <dt>

[<span data-ttu-id="017fd-133">遠端桌面服務虛擬通道</span><span class="sxs-lookup"><span data-stu-id="017fd-133">Remote Desktop Services virtual channels</span></span>](terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="017fd-134">*虛擬通道* 是軟體延伸模組，可用來將功能增強功能新增至遠端桌面服務應用程式。</span><span class="sxs-lookup"><span data-stu-id="017fd-134">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span>

</dd> <dt>

[<span data-ttu-id="017fd-135">RemoteFX 媒體重新導向 API</span><span class="sxs-lookup"><span data-stu-id="017fd-135">RemoteFX Media Redirection API</span></span>](remotefx-api.md)
</dt> <dd>

<span data-ttu-id="017fd-136">在遠端桌面會話中，會使用 RemoteFX 媒體重新導向 API 來識別伺服器的區域，以顯示快速變更內容，例如影片。</span><span class="sxs-lookup"><span data-stu-id="017fd-136">The RemoteFX Media Redirection API is used in a Remote Desktop session to identify areas of the server that are displaying fast changing content, such as video.</span></span> <span data-ttu-id="017fd-137">然後，此內容可以編碼並以編碼格式傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="017fd-137">This content can then be video encoded and sent to the client in encoded format.</span></span>

</dd> <dt>

[<span data-ttu-id="017fd-138">遠端桌面連線代理人用戶端 API</span><span class="sxs-lookup"><span data-stu-id="017fd-138">Remote Desktop Connection Broker client API</span></span>](connection-broker-client-api.md)
</dt> <dd>

<span data-ttu-id="017fd-139">說明如何使用遠端桌面連線代理人用戶端 API。</span><span class="sxs-lookup"><span data-stu-id="017fd-139">Describes how to use the Remote Desktop Connection Broker client API.</span></span>

</dd> <dt>

[<span data-ttu-id="017fd-140">個人桌面工作代理程式 API 參考</span><span class="sxs-lookup"><span data-stu-id="017fd-140">Personal desktop task agent API reference</span></span>](task-agent-api-reference.md)
</dt> <dd>

<span data-ttu-id="017fd-141">個人桌面工作代理程式 API 會用來處理對個人虛擬桌面的排程更新。</span><span class="sxs-lookup"><span data-stu-id="017fd-141">The personal desktop task agent API is used to handle scheduled updates to a personal virtual desktop.</span></span>

</dd> <dt>

[<span data-ttu-id="017fd-142">關於遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="017fd-142">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> <dd>

<span data-ttu-id="017fd-143">遠端桌面服務 (前身為終端機服務) 提供的功能類似于以終端為基礎、集中式主機或大型主機，也就是多個終端機連接到主機電腦的環境。</span><span class="sxs-lookup"><span data-stu-id="017fd-143">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span>

</dd> <dt>

[<span data-ttu-id="017fd-144">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="017fd-144">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> <dd>

<span data-ttu-id="017fd-145">遠端桌面管理服務 (RDMS) 提供者會管理 (VDI) 環境的虛擬桌面基礎結構。</span><span class="sxs-lookup"><span data-stu-id="017fd-145">The Remote Desktop Management Services (RDMS) Provider manages virtual desktop infrastructure (VDI) environments.</span></span>

</dd> <dt>

[<span data-ttu-id="017fd-146">遠端桌面服務參考</span><span class="sxs-lookup"><span data-stu-id="017fd-146">Remote Desktop Services reference</span></span>](terminal-services-reference.md)
</dt> <dd>

<span data-ttu-id="017fd-147">您可以用來檢查和設定遠端桌面服務使用者屬性的屬性方法檔。</span><span class="sxs-lookup"><span data-stu-id="017fd-147">Documentation of property methods that you can use to examine and configure Remote Desktop Services user properties.</span></span> <span data-ttu-id="017fd-148">也記載了遠端桌面服務函式、結構和遠端桌面網頁連線可編寫腳本的介面。</span><span class="sxs-lookup"><span data-stu-id="017fd-148">Remote Desktop Services functions, structures, and Remote Desktop Web Connection scriptable interfaces are also documented.</span></span>

</dd> <dt>

[<span data-ttu-id="017fd-149">遠端桌面服務快速鍵</span><span class="sxs-lookup"><span data-stu-id="017fd-149">Remote Desktop Services Shortcut Keys</span></span>](terminal-services-shortcut-keys.md)
</dt> <dd>

<span data-ttu-id="017fd-150">遠端桌面服務快速鍵的清單。</span><span class="sxs-lookup"><span data-stu-id="017fd-150">A list of the Remote Desktop Services shortcut keys.</span></span>

</dd> <dt>

[<span data-ttu-id="017fd-151">遠端桌面服務 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="017fd-151">Remote Desktop Services WMI provider</span></span>](terminal-services-wmi-provider.md)
</dt> <dd>

<span data-ttu-id="017fd-152">遠端桌面服務 WMI 提供者可透過程式設計的方式，存取遠端桌面服務設定/連線 Microsoft Management Console (MMC) 嵌入式管理單元所公開的資訊和設定。</span><span class="sxs-lookup"><span data-stu-id="017fd-152">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

</dd> <dt>

[<span data-ttu-id="017fd-153">使用遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="017fd-153">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> <dd>

<span data-ttu-id="017fd-154">如何在遠端桌面服務環境中進行程式設計，以及如何使用遠端桌面網頁連線將先前稱為終端機服務) 技術的遠端桌面服務 (延伸至網路。</span><span class="sxs-lookup"><span data-stu-id="017fd-154">How to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="017fd-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="017fd-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="017fd-156">終端機服務現在遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="017fd-156">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




