---
title: 'IWMPNetwork (VB 和 C ) 介面 (h.264. h) '
description: 提供屬性和方法來存取與網路連接品質相關的統計資料，以及指定和取出網路 proxy 設定。IWMPNetwork 介面會公開下列屬性。
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- IWMPNetwork (VB 和 C ) 介面 Windows Media Player
- IWMPNetwork (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 301fe5c89d2eb5df3dd4c22927e75a5607e7abd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976069"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a>IWMPNetwork (VB 和 c # ) 介面

提供屬性和方法來存取與網路連接品質相關的統計資料，以及指定和取出網路 proxy 設定。

**IWMPNetwork** 介面會公開下列屬性。

## <a name="members"></a>成員

**IWMPNetwork (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IWMPNetwork (VB 和 c # )** 介面都有這些方法。



| 方法                                                                                           | 描述                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**getProxyBypassForLocal**](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | 傳回值，指出如果源伺服器是在區域網路上，是否略過 proxy 伺服器。<br/> |
| [**getProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | 傳回 proxy 例外清單。<br/>                                                                           |
| [**getProxyName**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | 傳回要使用之 proxy 伺服器的名稱。<br/>                                                            |
| [**getProxyPort**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | 傳回要使用的 proxy 埠。<br/>                                                                          |
| [**getProxySettings**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | 傳回通訊協定的 proxy 設定相關資訊。<br/>                                                |
| [**setProxyBypassForLocal**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | 指定如果源伺服器是在區域網路上，是否略過 proxy 伺服器。<br/>                  |
| [**setProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | 指定 proxy 例外清單。<br/>                                                                         |
| [**setProxyName**](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | 指定要使用之 proxy 伺服器的名稱。<br/>                                                              |
| [**setProxyPort**](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | 指定要使用的 proxy 埠。<br/>                                                                            |
| [**setProxySettings**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | 指定通訊協定的 proxy 設定。<br/>                                                                |



 

### <a name="properties"></a>屬性

**IWMPNetwork (VB 和 c # )** 介面都有這些屬性。



| 屬性                                                                                          | 存取類型           | Description                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [**頻寬**](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | 唯讀<br/>  | 取得媒體專案目前的頻寬。<br/>                                     |
| [**位元速率**](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | 唯讀<br/>  | 取得所接收的目前位速率。<br/>                                         |
| [**bufferingCount**](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | 唯讀<br/>  | 取得在播放期間發生緩衝處理的次數。<br/>                      |
| [**bufferingProgress**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | 唯讀<br/>  | 取得緩衝處理已完成的百分比。<br/>                                       |
| [**bufferingTime**](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | 讀取/寫入<br/> | 取得或設定播放開始之前的緩衝時間量（以毫秒為單位）。<br/> |
| [**downloadProgress**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | 唯讀<br/>  | 取得下載已完成的百分比。<br/>                                     |
| [**encodedFrameRate**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | 唯讀<br/>  | 取得內容作者指定的影片畫面播放速率。<br/>                        |
| [**頻**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | 唯讀<br/>  | 取得目前的影片畫面播放速率。<br/>                                                |
| [**framesSkipped**](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | 唯讀<br/>  | 取得播放期間略過的總畫面格數。<br/>                          |
| [**lostPackets**](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | 唯讀<br/>  | 取得遺失的封包數目。<br/>                                                  |
| [**maxBandwidth**](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | 讀取/寫入<br/> | 取得或設定允許的最大頻寬。<br/>                                       |
| [**maxBitRate**](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | 唯讀<br/>  | 取得最大可能的影片位速率。<br/>                                         |
| [**receivedPackets**](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | 唯讀<br/>  | 取得已接收的封包數目。<br/>                                              |
| [**receptionQuality**](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | 唯讀<br/>  | 取得過去30秒內未遺失的封包百分比。<br/>                   |
| [**recoveredPackets**](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | 唯讀<br/>  | 取得已復原的封包數目。<br/>                                             |
| [**sourceProtocol**](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | 唯讀<br/>  | 取得用來接收資料的來源通訊協定。<br/>                                    |



 

使用下列屬性來取得 **IWMPNetwork** 介面。



| Object                                                                   | 屬性                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [AxWindowsMediaPlayer 物件](axwindowsmediaplayer-object--vb-and-c.md) | [**network**](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .NET 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





