---
title: 網路介面的概觀
description: 網路介面的概觀
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows Media Format SDK，網路介面
- Windows Media Format SDK，介面
- Advanced Systems Format (ASF) ，網路介面
- ASF (Advanced Systems Format) ，網路介面
- Advanced Systems Format (ASF) ，網路功能的介面清單
- ASF (Advanced Systems Format) ，網路功能的介面清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681565"
---
# <a name="overview-of-networking-interfaces"></a>網路介面的概觀

透過下列介面的方法，可支援此 SDK 的網路功能。



| 介面                                                  | 描述                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | 取得連接到網路接收器之用戶端的相關資訊。                                                                                       |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | 提供方法，以取得附加至寫入器網路接收之用戶端的相關資訊。 這個介面會擴充 **IWMClientConnections** 介面。 |
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | 提供回呼方法，以在存取遠端網站時取得使用者認證。                                                                  |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | 提供 reader 物件的 advanced 方法。                                                                                                       |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | 擴充 **IWMReaderAdvanced2** 介面。                                                                                                         |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | 擴充 **IWMReaderAdvanced3** 介面。                                                                                                         |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | 在 reader 物件上設定網路設定。                                                                                                 |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | 在 reader 物件上設定額外的網路設定。 這個介面會擴充 **IWMReaderNetworkConfig** 介面。                         |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | 設定用來將數位媒體寫入網路的網路接收物件。                                                                |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | 設定用來將數位媒體散發至發行端點的推播接收物件。                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行網路功能**](implementing-network-functionality.md)
</dt> </dl>

 

 




