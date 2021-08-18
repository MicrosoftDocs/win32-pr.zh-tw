---
title: 啟動 DVC 接聽程式
description: 若要建立兩個動態虛擬通道之間的成功連接 (DVC) 遠端桌面連線 (RDC) 用戶端和伺服器上執行的模組，則 DVC 接聽程式必須正在執行且處於接聽狀態。
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d440069cb64597c16a14323a67926376bf1c425f5a29c77e451c52866a5399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000448"
---
# <a name="starting-a-dvc-listener"></a>啟動 DVC 接聽程式

若要建立兩個動態虛擬通道之間的成功連接 (DVC) 遠端桌面連線 (RDC) 用戶端和伺服器上執行的模組，則 DVC 接聽程式必須正在執行且處於接聽狀態。

接聽程式的具現化通常會發生在 DVC 外掛程式的 [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) 方法中。 不過，具現化不限於 **Initialize** 方法，而且可以在外掛程式執行的任何時間點啟動。 接聽程式是由 [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)具現化的 [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)介面所描述。 通道管理員的實例會在初始化點傳遞至外掛程式。 外掛程式可以維持實例的內部參考，只要它需要。

外掛程式可以具現化所需的多個接聽程式。 任何連入連線都將由 [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)處理，這是在 [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)的 [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener)方法中提供。 如需範例，請參閱 [DVC 用戶端外掛程式範例](dvc-client-plug-in-example.md)程式碼中的 **CDVCSamplePlugin：： Initialize** 的實作為範例。

 

 




