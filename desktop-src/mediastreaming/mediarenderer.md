---
title: MediaRenderer 類別
description: 實 IMediaRenderer 介面，此介面表示 (DMR) 裝置的 DLNA 數位媒體轉譯器。
ms.assetid: bac7898f-1334-4e28-92c7-6de464884eaf
keywords:
- MediaRenderer 類別媒體串流 API
- MediaRenderer 類別媒體串流 API，說明
topic_type:
- apiref
api_name:
- MediaRenderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d14cdea89535fc680874905a9fb2b3358595baab
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507883"
---
# <a name="mediarenderer-class"></a>MediaRenderer 類別

實 [**IMediaRenderer**](imediarenderer.md) 介面，此介面表示 (DMR) 裝置的 DLNA 數位媒體轉譯器。

**MediaRenderer** 具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MediaRenderer** 類別有這些方法。



| 方法                                                                                       | 描述                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**新增 \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828962(v=vs.85))        | 註冊 [**RenderingParametersUpdate**](renderingparametersupdate.md) 事件的事件處理常式。<br/>                                                                                                                                                                                                                                                       |
| [**新增 \_ TransportParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828963(v=vs.85))        | 註冊 [**TransportParametersUpdate**](transportparametersupdate.md) 事件的事件處理常式。<br/>                                                                                                                                                                                                                                                       |
| [**GetMuteAsync**](/previous-versions/windows/desktop/legacy/hh828964(v=vs.85))                                           | 以非同步方式查詢 DMR，以判斷音訊目前是否為靜音或 unmuted。<br/>                                                                                                                                                                                                                                                                            |
| [**GetPositionInformationAsync**](/previous-versions/windows/desktop/legacy/hh828965(v=vs.85))             | 以非同步方式查詢 DMR 以取得位置資訊。<br/>                                                                                                                                                                                                                                                                                               |
| [**GetTransportInformationAsync**](/previous-versions/windows/desktop/legacy/hh828966(v=vs.85))           | 以非同步方式查詢 DMR 以取得傳輸資訊。<br/>                                                                                                                                                                                                                                                                                              |
| [**GetVolumeAsync**](/previous-versions/windows/desktop/legacy/hh828967(v=vs.85))                                       | 以非同步方式查詢其目前音訊音量層級的 DMR。<br/>                                                                                                                                                                                                                                                                                             |
| [**PauseAsync**](mediarenderer-pauseasync.md)                                               | 指示 DMR 以非同步方式暫停播放目前的內容。<br/>                                                                                                                                                                                                                                                                                         |
| [**PlayAsync**](/previous-versions/windows/desktop/legacy/hh828972(v=vs.85))                                                 | 指示 DMR 以非同步方式播放藉由呼叫 [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85))、 [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))或 [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) 方法所指定的內容。<br/>                       |
| [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/legacy/hh828973(v=vs.85))                                   | 指示 DMR 以非同步方式播放依指定速率呼叫 [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85))、 [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))或 [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) 方法所指定的內容。<br/> |
| [**移除 \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828974(v=vs.85))  | 取消註冊 [**RenderingParametersUpdate**](renderingparametersupdate.md) 事件的事件處理常式。<br/>                                                                                                                                                                                                                                                     |
| [**移除 \_ TransportParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828975(v=vs.85))  | 取消註冊 [**TransportParametersUpdate**](transportparametersupdate.md) 事件的事件處理常式。<br/>                                                                                                                                                                                                                                                     |
| [**SeekAsync**](/previous-versions/windows/desktop/legacy/hh828976(v=vs.85))                                                 | 指示 DMR 以非同步方式搜尋特定的時間位移。<br/>                                                                                                                                                                                                                                                                                          |
| [**SetMuteAsync**](/previous-versions/windows/desktop/legacy/hh828977(v=vs.85))                                           | 指示 DMR 以非同步方式將音訊靜音或取消靜音。<br/>                                                                                                                                                                                                                                                                                           |
| [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828978(v=vs.85)) | 指示 DMR 在目前的內容完成播放時，以非同步方式準備要播放的指定內容。<br/>                                                                                                                                                                                                                                   |
| [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828979(v=vs.85))           | 指示 DMR 在目前的內容完成播放時，以非同步方式準備要播放的指定媒體串流。<br/>                                                                                                                                                                                                                              |
| [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828980(v=vs.85))                 | 當目前的內容完成播放時，指示 DMR 以非同步方式準備指定 URI 所識別的內容以供播放。<br/>                                                                                                                                                                                                             |
| [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85))         | 指示 DMR 以非同步方式準備要播放的指定內容。<br/>                                                                                                                                                                                                                                                                                 |
| [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))                   | 指示 DMR 在目前的內容完成播放時，以非同步方式準備要播放的指定媒體串流。<br/>                                                                                                                                                                                                                              |
| [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85))                         | 以非同步方式指示 DMR，以準備所指定 URI 所識別的內容以供播放。<br/>                                                                                                                                                                                                                                                           |
| [**SetVolumeAsync**](/previous-versions/windows/desktop/legacy/hh828984(v=vs.85))                                       | 以非同步方式將 DMR 上的音訊音量層級設定為指定的值。<br/>                                                                                                                                                                                                                                                                                  |
| [**StopAsync**](mediarenderer-stopasync.md)                                                 | 指示 DMR 以非同步方式停止播放目前的內容。<br/>                                                                                                                                                                                                                                                                                          |



 

### <a name="properties"></a>屬性

**MediaRenderer** 類別具有這些屬性。



| 屬性                                                                | 存取類型          | Description                                                                                 |
|:------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------|
| [**Actioninformation .action**](mediarenderer-actioninformation.md)<br/> | 唯讀<br/> | 取得目前可以在 DMR 上叫用哪些方法的相關資訊。<br/>        |
| [**IsAudioSupported**](mediarenderer-isaudiosupported.md)<br/>   | 唯讀<br/> | 取得值，這個值會指出 DMR 是否能夠播放音訊內容。<br/> |
| [**IsImageSupported**](mediarenderer-isimagesupported.md)<br/>   | 唯讀<br/> | 取得值，這個值會指出 DMR 是否能夠顯示影像。<br/>     |
| [**IsVideoSupported**](mediarenderer-isvideosupported.md)<br/>   | 唯讀<br/> | 取得值，這個值會指出 DMR 是否能夠播放影片內容。<br/> |



 

 

