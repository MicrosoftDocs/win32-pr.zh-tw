---
title: Network 物件
description: Network 物件提供的屬性和方法可用來存取與網路連接品質相關的統計資料，以及指定和取出網路 proxy 設定。
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- 網路物件 Windows Media Player
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d439679636bce773c43f5610060c4744ef4d5d7c
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104373463"
---
# <a name="network-object"></a>Network 物件

**Network** 物件提供的屬性和方法可用來存取與網路連接品質相關的統計資料，以及指定和取出網路 proxy 設定。

**Network** 物件支援下列屬性。



| 屬性                                           | 描述                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [頻寬](network-bandwidth.md)                 | 抓取媒體專案目前的頻寬。                                          |
| [位元速率](network-bitrate.md)                     | 抓取正在接收的目前位速率。                                              |
| [bufferingCount](network-bufferingcount.md)       | 抓取在播放期間發生緩衝處理的次數。                           |
| [bufferingProgress](network-bufferingprogress.md) | 抓取已完成的緩衝百分比。                                            |
| [bufferingTime](network-bufferingtime.md)         | 指定或抓取播放開始之前的緩衝時間量（以毫秒為單位）。 |
| [downloadProgress](network-downloadprogress.md)   | 抓取下載已完成的百分比。                                             |
| [encodedFrameRate](network-encodedframerate.md)   | 抓取內容作者指定的影片畫面播放速率。                             |
| [頻](network-framerate.md)                 | 抓取目前的影片畫面播放速率。                                                     |
| [framesSkipped](network-framesskipped.md)         | 抓取播放期間略過的總畫面格數。                               |
| [lostPackets](network-lostpackets.md)             | 捕獲遺失的封包數目。                                                       |
| [maxBandwidth](network-maxbandwidth.md)           | 指定或抓取允許的最大頻寬。                                       |
| [maxBitRate](network-maxbitrate.md)               | 抓取最大可能的影片位元速率。                                              |
| [receivedPackets](network-receivedpackets.md)     | 抓取收到的封包數目。                                                   |
| [receptionQuality](network-receptionquality.md)   | 抓取過去30秒內收到的封包百分比。                        |
| [recoveredPackets](network-recoveredpackets.md)   | 抓取已復原的封包數目。                                                  |
| [sourceProtocol](network-sourceprotocol.md)       | 抓取用來接收資料的來源通訊協定。                                         |



 

**Network** 物件支援下列方法。



| 方法                                                       | 描述                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [getProxyBypassForLocal](network-getproxybypassforlocal.md) | 抓取值，指出如果源伺服器是在區域網路上，是否應略過 proxy 伺服器。 |
| [getProxyExceptionList](network-getproxyexceptionlist.md)   | 抓取 proxy 例外清單。                                                                                  |
| [getProxyName](network-getproxyname.md)                     | 抓取要使用的 proxy 伺服器名稱。                                                                         |
| [getProxyPort](network-getproxyport.md)                     | 抓取要使用的 proxy 埠。                                                                                     |
| [getProxySettings](network-getproxysettings.md)             | 抓取指定通訊協定的 proxy 設定。                                                                    |
| [setProxyBypassForLocal](network-setproxybypassforlocal.md) | 指定值，指出如果源伺服器是在區域網路上，是否應略過 proxy 伺服器。 |
| [setProxyExceptionList](network-setproxyexceptionlist.md)   | 指定 proxy 例外清單。                                                                                  |
| [setProxyName](network-setproxyname.md)                     | 指定要使用之 proxy 伺服器的名稱。                                                                         |
| [setProxyPort](network-setproxyport.md)                     | 指定要使用的 proxy 埠。                                                                                     |
| [setProxySettings](network-setproxysettings.md)             | 指定指定通訊協定的 proxy 設定。                                                                    |



 

**網路** 物件是透過下列屬性來存取。



| Object                      | 屬性                      |
|-----------------------------|-------------------------------|
| [球員](player-object.md) | [network](player-network.md) |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




