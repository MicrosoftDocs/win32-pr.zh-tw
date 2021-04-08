---
title: 使用遠端桌面服務的虛擬通道
description: 若要執行虛擬通道，您可以提供虛擬通道應用程式的伺服器和用戶端模組。
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eafca38c19855fdb057ceeb6e79cb4613773a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672035"
---
# <a name="using-remote-desktop-services-virtual-channels"></a><span data-ttu-id="c4820-103">使用遠端桌面服務的虛擬通道</span><span class="sxs-lookup"><span data-stu-id="c4820-103">Using Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="c4820-104">若要執行虛擬通道，您可以提供虛擬通道應用程式的伺服器和用戶端模組。</span><span class="sxs-lookup"><span data-stu-id="c4820-104">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span> <span data-ttu-id="c4820-105">伺服器模組可以是使用者模式應用程式或核心模式驅動程式。</span><span class="sxs-lookup"><span data-stu-id="c4820-105">The server module can be a user-mode application or a kernel-mode driver.</span></span> <span data-ttu-id="c4820-106">用戶端模組必須是 DLL。</span><span class="sxs-lookup"><span data-stu-id="c4820-106">The client module must be a DLL.</span></span>

<span data-ttu-id="c4820-107">如需這些模組的說明，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="c4820-107">For descriptions of these modules, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c4820-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="c4820-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="c4820-109">虛擬通道伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="c4820-109">Virtual Channel Server Application</span></span>](virtual-channel-server-application.md)
</dt> <dd>

<span data-ttu-id="c4820-110">使用虛擬通道之應用程式的伺服器模組，必須是在遠端桌面工作階段主機 (RD 工作階段主機) server 的用戶端會話中執行的使用者模式應用程式。</span><span class="sxs-lookup"><span data-stu-id="c4820-110">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="c4820-111">請注意，您必須提供方法來啟動伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="c4820-111">Note that you must provide a method to start the server application.</span></span>

</dd> <dt>

[<span data-ttu-id="c4820-112">虛擬通道用戶端 DLL</span><span class="sxs-lookup"><span data-stu-id="c4820-112">Virtual Channel Client DLL</span></span>](virtual-channel-client-dll.md)
</dt> <dd>

<span data-ttu-id="c4820-113">虛擬通道應用程式的用戶端是在用戶端電腦上遠端桌面服務初始化期間載入的 DLL。</span><span class="sxs-lookup"><span data-stu-id="c4820-113">The client of a virtual channels application is a DLL that is loaded during the Remote Desktop Services initialization on the client computer.</span></span> <span data-ttu-id="c4820-114">您必須在用戶端電腦上註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="c4820-114">The DLL must be registered on the client computer.</span></span>

</dd> <dt>

[<span data-ttu-id="c4820-115">虛擬通道用戶端註冊</span><span class="sxs-lookup"><span data-stu-id="c4820-115">Virtual Channel Client Registration</span></span>](virtual-channel-client-registration.md)
</dt> <dd>

<span data-ttu-id="c4820-116">您必須將用戶端 DLL 的名稱儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="c4820-116">You must store the name of the client DLL in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="c4820-117">遠端控制持續性虛擬通道</span><span class="sxs-lookup"><span data-stu-id="c4820-117">Remote Control Persistent Virtual Channels</span></span>](remote-control-persistent-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="c4820-118">遠端控制連接或中斷連接至用戶端的會話時，不會關閉遠端控制持續性虛擬通道。</span><span class="sxs-lookup"><span data-stu-id="c4820-118">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="c4820-119">資料將繼續透過此通道傳送和接收。</span><span class="sxs-lookup"><span data-stu-id="c4820-119">Data will continue to be transmitted and received through this channel.</span></span>

</dd> <dt>

[<span data-ttu-id="c4820-120">動態虛擬通道</span><span class="sxs-lookup"><span data-stu-id="c4820-120">Dynamic Virtual Channels</span></span>](dynamic-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="c4820-121">動態虛擬通道 (DVC) Api 擴充現有的虛擬通道 Api，以供遠端桌面服務（稱為靜態虛擬通道 (SVC) Api）。</span><span class="sxs-lookup"><span data-stu-id="c4820-121">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span>

</dd> </dl>

<span data-ttu-id="c4820-122">如果您已在遠端桌面服務部署中啟用虛擬通道的應用程式，您也可以透過遠端桌面 ActiveX 控制項，讓應用程式可供存取 RD 工作階段主機伺服器的用戶端電腦使用。</span><span class="sxs-lookup"><span data-stu-id="c4820-122">If you have enabled a virtual channel's application in your Remote Desktop Services deployment, you can also make the application available to client computers that access the RD Session Host server by means of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="c4820-123">如需詳細資訊，請參閱 [使用具有虛擬通道的遠端桌面 ActiveX 控制項](using-the-remote-desktop-activex-control-with-virtual-channels.md)。</span><span class="sxs-lookup"><span data-stu-id="c4820-123">For more information, see [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




