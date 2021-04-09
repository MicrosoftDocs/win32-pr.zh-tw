---
title: 使用遠端桌面網頁連線來執行可編寫腳本的虛擬通道
description: 示範使用遠端桌面網頁連線執行可編寫腳本之虛擬通道步驟的程式碼範例。
ms.assetid: a482b84d-96b6-4f42-8841-7039a1882789
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a36f685de01312a93df67deb6be16ce031794c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674344"
---
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a><span data-ttu-id="be63f-103">使用遠端桌面網頁連線來執行可編寫腳本的虛擬通道</span><span class="sxs-lookup"><span data-stu-id="be63f-103">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>

<span data-ttu-id="be63f-104">下列程式和程式碼範例示範使用遠端桌面網頁連線來執行可編寫腳本之虛擬通道的步驟。</span><span class="sxs-lookup"><span data-stu-id="be63f-104">The following procedure and code examples show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span> <span data-ttu-id="be63f-105">這些範例是以 Visual Basic Scripting Edition 撰寫，並假設遠端桌面 ActiveX 控制項命名為 "MsRdpClient"。</span><span class="sxs-lookup"><span data-stu-id="be63f-105">The examples were written in Visual Basic Scripting Edition and assume that the Remote Desktop ActiveX control is named "MsRdpClient".</span></span>

<span data-ttu-id="be63f-106">**建立及部署可編寫腳本的虛擬通道**</span><span class="sxs-lookup"><span data-stu-id="be63f-106">**To create and deploy scriptable virtual channels**</span></span>

1.  <span data-ttu-id="be63f-107">部署應用程式的伺服器端，並確定它正在遠端桌面工作階段主機 (RD 工作階段主機) server 上執行。</span><span class="sxs-lookup"><span data-stu-id="be63f-107">Deploy the server side of the application and make sure it is running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="be63f-108">如需在伺服器上部署虛擬通道應用程式的相關資訊，請參閱 [虛擬通道伺服器應用程式](virtual-channel-server-application.md)。</span><span class="sxs-lookup"><span data-stu-id="be63f-108">For information about deploying virtual channels applications on the server, see [Virtual Channel Server Application](virtual-channel-server-application.md).</span></span>
2.  <span data-ttu-id="be63f-109">在您的用戶端腳本中，呼叫 [**IMsTscAx：： CreateVirtualChannels**](imstscax-createvirtualchannels.md)，並傳遞包含以逗號分隔之虛擬通道名稱清單的字串。</span><span class="sxs-lookup"><span data-stu-id="be63f-109">In your client script, call [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md), passing a string that contains a comma-separated list of virtual channel names.</span></span>

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    <span data-ttu-id="be63f-110">如需虛擬通道命名限制的詳細資訊，請參閱 [虛擬通道用戶端註冊](virtual-channel-client-registration.md)。</span><span class="sxs-lookup"><span data-stu-id="be63f-110">For information about virtual channel naming restrictions, see [Virtual Channel Client Registration](virtual-channel-client-registration.md).</span></span>

3.  <span data-ttu-id="be63f-111">呼叫 [**IMsTscAx：： Connect**](imstscax-connect.md) 以建立您的遠端桌面服務連接。</span><span class="sxs-lookup"><span data-stu-id="be63f-111">Call [**IMsTscAx::Connect**](imstscax-connect.md) to create your Remote Desktop Services connection.</span></span>

    ```VB
    MsRdpClient.connect
    ```

    

4.  <span data-ttu-id="be63f-112">使用 [**IMsTscAx：： SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) 方法可將資料傳送至伺服器，並傳遞包含虛擬通道名稱的字串，以及包含要傳遞之資料的第二個字串。</span><span class="sxs-lookup"><span data-stu-id="be63f-112">Use the [**IMsTscAx::SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) method to send data to the server, passing a string that contains the virtual channel name and a second string that contains the data to be passed.</span></span>

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  <span data-ttu-id="be63f-113">從伺服器接收 [**IMsTscAxEvents：： OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) 事件的資料。</span><span class="sxs-lookup"><span data-stu-id="be63f-113">Receive data from the server on the [**IMsTscAxEvents::OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) event.</span></span>

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




