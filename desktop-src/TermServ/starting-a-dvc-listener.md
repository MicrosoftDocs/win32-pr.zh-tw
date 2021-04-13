---
title: 啟動 DVC 接聽程式
description: 若要建立兩個動態虛擬通道之間的成功連接 (DVC) 遠端桌面連線 (RDC) 用戶端和伺服器上執行的模組，則 DVC 接聽程式必須正在執行且處於接聽狀態。
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b625d5547facd0487af170af9d59eddd6bfed87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311319"
---
# <a name="starting-a-dvc-listener"></a><span data-ttu-id="b3014-103">啟動 DVC 接聽程式</span><span class="sxs-lookup"><span data-stu-id="b3014-103">Starting a DVC Listener</span></span>

<span data-ttu-id="b3014-104">若要建立兩個動態虛擬通道之間的成功連接 (DVC) 遠端桌面連線 (RDC) 用戶端和伺服器上執行的模組，則 DVC 接聽程式必須正在執行且處於接聽狀態。</span><span class="sxs-lookup"><span data-stu-id="b3014-104">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

<span data-ttu-id="b3014-105">接聽程式的具現化通常會發生在 DVC 外掛程式的 [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) 方法中。</span><span class="sxs-lookup"><span data-stu-id="b3014-105">The instantiation of a listener typically occurs in the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of the DVC plug-in.</span></span> <span data-ttu-id="b3014-106">不過，具現化不限於 **Initialize** 方法，而且可以在外掛程式執行的任何時間點啟動。</span><span class="sxs-lookup"><span data-stu-id="b3014-106">However, instantiation is not limited to the **Initialize** method, and can be started at any point of the plug-in execution.</span></span> <span data-ttu-id="b3014-107">接聽程式是由 [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)具現化的 [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)介面所描述。</span><span class="sxs-lookup"><span data-stu-id="b3014-107">The listener is described by the [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) interface which is instantiated by the [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="b3014-108">通道管理員的實例會在初始化點傳遞至外掛程式。</span><span class="sxs-lookup"><span data-stu-id="b3014-108">An instance to the channel manager is passed to the plug-in at the initialization point.</span></span> <span data-ttu-id="b3014-109">外掛程式可以維持實例的內部參考，只要它需要。</span><span class="sxs-lookup"><span data-stu-id="b3014-109">The plug-in can maintain an internal reference to the instance as long as it needs to.</span></span>

<span data-ttu-id="b3014-110">外掛程式可以具現化所需的多個接聽程式。</span><span class="sxs-lookup"><span data-stu-id="b3014-110">A plug-in can instantiate as many listeners as it needs to.</span></span> <span data-ttu-id="b3014-111">任何連入連線都將由 [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)處理，這是在 [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)的 [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener)方法中提供。</span><span class="sxs-lookup"><span data-stu-id="b3014-111">Any incoming connection will be handled by [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), which is supplied in the [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) method of [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="b3014-112">如需範例，請參閱 [DVC 用戶端外掛程式範例](dvc-client-plug-in-example.md)程式碼中的 **CDVCSamplePlugin：： Initialize** 的實作為範例。</span><span class="sxs-lookup"><span data-stu-id="b3014-112">For an example, see the implementation of **CDVCSamplePlugin::Initialize** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

 

 




