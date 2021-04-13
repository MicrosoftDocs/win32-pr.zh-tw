---
title: 遠端桌面服務虛擬通道
description: 虛擬通道是軟體延伸模組，可用來將功能增強功能新增至遠端桌面服務應用程式。
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300728"
---
# <a name="remote-desktop-services-virtual-channels"></a><span data-ttu-id="c8084-103">遠端桌面服務虛擬通道</span><span class="sxs-lookup"><span data-stu-id="c8084-103">Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="c8084-104">*虛擬通道* 是軟體延伸模組，可用來將功能增強功能新增至遠端桌面服務應用程式。</span><span class="sxs-lookup"><span data-stu-id="c8084-104">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span> <span data-ttu-id="c8084-105">功能增強功能的範例可能包括：支援特殊類型的硬體、音訊或其他遠端桌面服務 [遠端桌面通訊協定](remote-desktop-protocol.md) (RDP) 所提供的核心功能。</span><span class="sxs-lookup"><span data-stu-id="c8084-105">Examples of functional enhancements might include: support for special types of hardware, audio, or other additions to the core functionality provided by the Remote Desktop Services [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP).</span></span> <span data-ttu-id="c8084-106">RDP 通訊協定提供多個虛擬通道的多重管理管理。</span><span class="sxs-lookup"><span data-stu-id="c8084-106">The RDP protocol provides multiplexed management of multiple virtual channels.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c8084-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="c8084-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="c8084-108">使用遠端桌面服務的虛擬通道</span><span class="sxs-lookup"><span data-stu-id="c8084-108">Using Remote Desktop Services virtual channels</span></span>](using-terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="c8084-109">若要執行虛擬通道，您可以提供虛擬通道應用程式的伺服器和用戶端模組。</span><span class="sxs-lookup"><span data-stu-id="c8084-109">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span>

</dd> <dt>

[<span data-ttu-id="c8084-110">動態虛擬通道參考</span><span class="sxs-lookup"><span data-stu-id="c8084-110">Dynamic virtual channels reference</span></span>](dynamic-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="c8084-111">遠端桌面服務支援動態虛擬通道 (DVC) 用戶端介面。</span><span class="sxs-lookup"><span data-stu-id="c8084-111">Dynamic virtual channel (DVC) client interfaces are supported by Remote Desktop Services.</span></span>

</dd> <dt>

[<span data-ttu-id="c8084-112">圖形虛擬通道參考</span><span class="sxs-lookup"><span data-stu-id="c8084-112">Graphics virtual channels reference</span></span>](graphics-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="c8084-113">圖形虛擬通道參考包含可讓您建立虛擬圖形通道的程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="c8084-113">The graphics virtual channels reference contains programming elements that enable you to create a virtual graphics channel.</span></span>

</dd> </dl>

<span data-ttu-id="c8084-114">虛擬通道應用程式有兩個部分：用戶端模組和伺服器模組。</span><span class="sxs-lookup"><span data-stu-id="c8084-114">A virtual channel application has two parts, a client module and a server module.</span></span> <span data-ttu-id="c8084-115">伺服器模組是在遠端桌面工作階段主機 (RD 工作階段主機) server 上執行的可執行程式。</span><span class="sxs-lookup"><span data-stu-id="c8084-115">The server module is an executable program running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="c8084-116">用戶端模組是在遠端桌面連線 (RDC) 用戶端程式執行時，必須載入至用戶端電腦記憶體的 DLL。</span><span class="sxs-lookup"><span data-stu-id="c8084-116">The client module is a DLL that must be loaded into memory on the client computer when the Remote Desktop Connection (RDC) client program runs.</span></span>

<span data-ttu-id="c8084-117">虛擬通道可以在與 RDP 通訊協定無關的遠端桌面連線 (RDC) 用戶端上新增功能增強功能。</span><span class="sxs-lookup"><span data-stu-id="c8084-117">Virtual channels can add functional enhancements to a Remote Desktop Connection (RDC) client, independent of the RDP protocol.</span></span> <span data-ttu-id="c8084-118">透過虛擬通道支援，您可以新增新功能，而不需要更新用戶端或伺服器軟體或 RDP 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c8084-118">With virtual channel support, new features can be added without having to update the client or server software, or the RDP protocol.</span></span>

<span data-ttu-id="c8084-119">已識別出虛擬通道使用者的四個主要類別：</span><span class="sxs-lookup"><span data-stu-id="c8084-119">Four major classes of users of virtual channels have been identified:</span></span>

-   <span data-ttu-id="c8084-120">一般核心模式驅動程式，例如序列或印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="c8084-120">General kernel-mode drivers, such as serial or printer drivers.</span></span>
-   <span data-ttu-id="c8084-121">檔案系統重新導向 (這只是一般核心模式驅動程式) 的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="c8084-121">File system redirection (this is just a special case of a general kernel-mode driver).</span></span>
-   <span data-ttu-id="c8084-122">使用者模式應用程式，例如遠端剪下和貼上。</span><span class="sxs-lookup"><span data-stu-id="c8084-122">User mode applications, for example remote cut-and-paste.</span></span>
-   <span data-ttu-id="c8084-123">音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="c8084-123">Audio devices.</span></span>

<span data-ttu-id="c8084-124">如需詳細資訊，請參閱 [使用遠端桌面服務的虛擬通道](using-terminal-services-virtual-channels.md)。</span><span class="sxs-lookup"><span data-stu-id="c8084-124">For more information, see [Using Remote Desktop Services Virtual Channels](using-terminal-services-virtual-channels.md).</span></span>

<span data-ttu-id="c8084-125">如果您已在遠端桌面服務部署中啟用虛擬通道應用程式，可以透過遠端桌面 Microsoft ActiveX 控制項，讓應用程式可供存取 RD 工作階段主機伺服器的用戶端電腦使用。</span><span class="sxs-lookup"><span data-stu-id="c8084-125">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make the application available to client computers that access the RD Session Host server by means of the Remote Desktop Microsoft ActiveX control.</span></span> <span data-ttu-id="c8084-126">如需詳細資訊，請參閱可 [編寫腳本的虛擬通道](scriptable-virtual-channels.md) 和 [使用具有虛擬通道的遠端桌面 ActiveX 控制項](using-the-remote-desktop-activex-control-with-virtual-channels.md)。</span><span class="sxs-lookup"><span data-stu-id="c8084-126">For more information, see [Scriptable Virtual Channels](scriptable-virtual-channels.md) and [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




