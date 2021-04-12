---
title: 遠端控制持續性虛擬通道
description: 遠端控制連接或中斷連接至用戶端的會話時，不會關閉遠端控制持續性虛擬通道。 資料將繼續透過此通道傳送和接收。
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d87054a79863df5816b30fced648ab40251a80e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372575"
---
# <a name="remote-control-persistent-virtual-channels"></a><span data-ttu-id="dfb96-104">遠端控制持續性虛擬通道</span><span class="sxs-lookup"><span data-stu-id="dfb96-104">Remote Control Persistent Virtual Channels</span></span>

<span data-ttu-id="dfb96-105">在 Windows XP 上，DLL 可以將一或多個虛擬通道指定為 *遠端控制持續* 性。</span><span class="sxs-lookup"><span data-stu-id="dfb96-105">On Windows XP, a DLL can specify one or more virtual channels as *remote control persistent*.</span></span> <span data-ttu-id="dfb96-106">遠端控制連接或中斷連接至用戶端的會話時，不會關閉遠端控制持續性虛擬通道。</span><span class="sxs-lookup"><span data-stu-id="dfb96-106">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="dfb96-107">資料將繼續透過此通道傳送和接收。</span><span class="sxs-lookup"><span data-stu-id="dfb96-107">Data will continue to be transmitted and received through this channel.</span></span> <span data-ttu-id="dfb96-108">在此案例中，DLL 未指定為遠端控制持續性的虛擬通道將會關閉。</span><span class="sxs-lookup"><span data-stu-id="dfb96-108">Virtual channels that the DLL does not specify as remote control persistent will close in this scenario.</span></span>

<span data-ttu-id="dfb96-109">遠端控制持續性虛擬通道是在呼叫 **VirtualChannelInit** 期間指定。</span><span class="sxs-lookup"><span data-stu-id="dfb96-109">Remote control persistent virtual channels are specified during the call to **VirtualChannelInit**.</span></span> <span data-ttu-id="dfb96-110">如需有關這個的特定資訊，請參閱 [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) 的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="dfb96-110">Refer to the reference page for [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) for specific information about this.</span></span>

 

 




