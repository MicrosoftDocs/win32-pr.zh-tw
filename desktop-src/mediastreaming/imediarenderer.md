---
title: IMediaRenderer 介面
description: 封裝代表 DMR) 裝置 (的 DLNA 數位媒體轉譯器所需的方法和事件。
ms.assetid: FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB
keywords:
- IMediaRenderer 介面媒體串流 API
- IMediaRenderer 介面媒體串流 API，說明
topic_type:
- apiref
api_name:
- IMediaRenderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 363db88b67d29d92b1e79516056f5fa8e78ca22e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933193"
---
# <a name="imediarenderer-interface"></a>IMediaRenderer 介面

封裝代表 DMR) 裝置 (的 DLNA 數位媒體轉譯器所需的方法和事件。

## <a name="members"></a>成員

**IMediaRenderer** 介面繼承自 [**IBasicDevice**](ibasicdevice.md)。 **IMediaRenderer** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMediaRenderer** 介面具有這些方法。



| 方法                                                                                        | 描述                                                                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Actioninformation .action**](imediarenderer-actioninformation.md)                                 | 抓取目前可在 DMR 上叫用哪些方法的相關資訊。<br/>                                                                                                                                                                                                                                                                                    |
| [**新增 \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate)        | 註冊 [**RenderingParametersUpdate**](renderingparametersupdate.md) 事件的事件處理常式。<br/>                                                                                                                                                                                                                                                          |
| [**新增 \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate)        | 註冊 [**TransportParametersUpdate**](transportparametersupdate.md) 事件的事件處理常式。<br/>                                                                                                                                                                                                                                                          |
| [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync)                                           | 以非同步方式查詢 DMR，以判斷音訊目前是否為靜音或 unmuted。<br/>                                                                                                                                                                                                                                                                               |
| [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync)             | 以非同步方式查詢 DMR 以取得位置資訊。<br/>                                                                                                                                                                                                                                                                                                  |
| [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync)           | 以非同步方式查詢 DMR 以取得傳輸資訊。<br/>                                                                                                                                                                                                                                                                                                 |
| [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync)                                       | 以非同步方式查詢其目前音訊音量層級的 DMR。<br/>                                                                                                                                                                                                                                                                                                |
| [**IsAudioSupported**](imediarenderer-isaudiosupported.md)                                   | 抓取值，指出 DMR 是否能夠播放音訊內容。<br/>                                                                                                                                                                                                                                                                             |
| [**IsImageSupported**](imediarenderer-isimagesupported.md)                                   | 抓取值，指出 DMR 是否能夠顯示影像。<br/>                                                                                                                                                                                                                                                                                 |
| [**IsVideoSupported**](imediarenderer-isvideosupported.md)                                   | 抓取值，指出 DMR 是否能夠播放影片內容。<br/>                                                                                                                                                                                                                                                                             |
| [**PauseAsync**](imediarenderer-pauseasync.md)                                               | 指示 DMR 以非同步方式暫停播放目前的內容。<br/>                                                                                                                                                                                                                                                                                            |
| [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync)                                                 | 指示 DMR 以非同步方式播放藉由呼叫 [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromuriasync)、 [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromstreamasync)或 [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefrommediasourceasync) 方法所指定的內容。<br/>                       |
| [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync)                                   | 指示 DMR 以非同步方式播放依指定速率呼叫 [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromuriasync)、 [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromstreamasync)或 [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefrommediasourceasync) 方法所指定的內容。<br/> |
| [**移除 \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate)  | 取消註冊 [**RenderingParametersUpdate**](renderingparametersupdate.md) 事件的事件處理常式。<br/>                                                                                                                                                                                                                                                        |
| [**移除 \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate)  | 取消註冊 [**TransportParametersUpdate**](transportparametersupdate.md) 事件的事件處理常式。<br/>                                                                                                                                                                                                                                                        |
| [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync)                                                 | 指示 DMR 以非同步方式搜尋特定的時間位移。<br/>                                                                                                                                                                                                                                                                                             |
| [**SetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setmuteasync)                                           | 指示 DMR 以非同步方式將音訊靜音或取消靜音。 <br/>                                                                                                                                                                                                                                                                                             |
| [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) | 指示 DMR 在目前的內容完成播放時，以非同步方式準備要播放的指定內容。<br/>                                                                                                                                                                                                                                      |
| [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync)           | 指示 DMR 在目前的內容完成播放時，以非同步方式準備要播放的指定媒體串流。<br/>                                                                                                                                                                                                                                 |
| [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync)                 | 當目前的內容完成播放時，指示 DMR 以非同步方式準備指定 URI 所識別的內容以供播放。<br/>                                                                                                                                                                                                                |
| [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefrommediasourceasync)         | 指示 DMR 以非同步方式準備要播放的指定內容。<br/>                                                                                                                                                                                                                                                                                    |
| [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromstreamasync)                   | 指示 DMR 以非同步方式準備要播放的指定媒體串流。<br/>                                                                                                                                                                                                                                                                               |
| [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromuriasync)                         | 以非同步方式指示 DMR，以準備所指定 URI 所識別的內容以供播放。<br/>                                                                                                                                                                                                                                                              |
| [**SetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setvolumeasync)                                       | 以非同步方式將 DMR 上的音訊音量層級設定為指定的值。<br/>                                                                                                                                                                                                                                                                                     |
| [**StopAsync**](imediarenderer-stopasync.md)                                                 | 指示 DMR 以非同步方式停止播放目前的內容。<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

