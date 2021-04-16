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
# <a name="accepting-a-connection-remote-desktop-services"></a>接受連接 (遠端桌面服務) 

在某個時間點，動態虛擬通道 (DVC) 用戶端會要求 DVC 接聽程式的連接。 發生這種情況時，接聽程式可以產生唯一的通道給用戶端，這是由 [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)的 [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection)方法所處理。 如需範例，請參閱 [DVC 用戶端外掛程式範例](dvc-client-plug-in-example.md)程式碼中的 **CDVCSamplePlugin：： OnNewChannelConnection** 的實作為範例。

下圖顯示用來建立 DVC 連接的事件順序。 陰影物件是使用者提供的 (DVC 應用程式/服務和 [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)) ，而未陰影的物件則是架構 (遠端桌面工作階段主機 (RD 工作階段主機服務、接聽程式和 [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)) 中的一部分。

![建立 dvc 連接的事件順序](images/acceptingconnection.png)

> [!Note]  
> 此圖假設已透過 [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)的 [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener)呼叫建立接聽程式物件，而且外掛程式已將 [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)指定為參數。

 

 

 




