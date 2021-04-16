---
title: '接受連接 (遠端桌面服務) '
description: 在某個時間點，動態虛擬通道 (DVC) 用戶端會要求 DVC 接聽程式的連接。
ms.assetid: eab17aa9-590c-4da2-a1a9-6e50a11d1de7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13aa0b78e459c85e7ba07e043e3da313b3f6118
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104566813"
---
# <a name="accepting-a-connection-remote-desktop-services"></a><span data-ttu-id="7d35a-103">接受連接 (遠端桌面服務) </span><span class="sxs-lookup"><span data-stu-id="7d35a-103">Accepting a Connection (Remote Desktop Services)</span></span>

<span data-ttu-id="7d35a-104">在某個時間點，動態虛擬通道 (DVC) 用戶端會要求 DVC 接聽程式的連接。</span><span class="sxs-lookup"><span data-stu-id="7d35a-104">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span> <span data-ttu-id="7d35a-105">發生這種情況時，接聽程式可以產生唯一的通道給用戶端，這是由 [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)的 [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection)方法所處理。</span><span class="sxs-lookup"><span data-stu-id="7d35a-105">When this occurs, the listener can spawn a unique communication channel to the client, which is handled by the [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) method of [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback).</span></span> <span data-ttu-id="7d35a-106">如需範例，請參閱 [DVC 用戶端外掛程式範例](dvc-client-plug-in-example.md)程式碼中的 **CDVCSamplePlugin：： OnNewChannelConnection** 的實作為範例。</span><span class="sxs-lookup"><span data-stu-id="7d35a-106">For an example, see the implementation of **CDVCSamplePlugin::OnNewChannelConnection** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

<span data-ttu-id="7d35a-107">下圖顯示用來建立 DVC 連接的事件順序。</span><span class="sxs-lookup"><span data-stu-id="7d35a-107">The following figure shows the sequence of events for establishing a DVC connection.</span></span> <span data-ttu-id="7d35a-108">陰影物件是使用者提供的 (DVC 應用程式/服務和 [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)) ，而未陰影的物件則是架構 (遠端桌面工作階段主機 (RD 工作階段主機服務、接聽程式和 [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)) 中的一部分。</span><span class="sxs-lookup"><span data-stu-id="7d35a-108">The shaded objects are user-supplied (DVC application/service and [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), while the un-shaded objects are part of the framework (Remote Desktop Session Host (RD Session Host) service, listener, and [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).</span></span>

![建立 dvc 連接的事件順序](images/acceptingconnection.png)

> [!Note]  
> <span data-ttu-id="7d35a-110">此圖假設已透過 [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)的 [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener)呼叫建立接聽程式物件，而且外掛程式已將 [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)指定為參數。</span><span class="sxs-lookup"><span data-stu-id="7d35a-110">This figure assumes that a listener object has been created through a [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) call to [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager), and that the plug-in has specified [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) as a parameter.</span></span>

 

 

 




