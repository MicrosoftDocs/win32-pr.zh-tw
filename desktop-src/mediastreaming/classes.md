---
title: '類別 (媒體串流 API) '
description: 媒體串流 API 提供下列類別。
ms.assetid: E537FCE0-5AE5-41BC-903D-AE67CE9F4D78
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b90ace112563a5c1bf1fee7455877434371adb26
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383758"
---
# <a name="classes-media-streaming-api"></a>類別 (媒體串流 API) 

[媒體串流 API](media-streaming-api-portal.md)提供下列類別。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                   | 描述                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))<br/>                               | 實 [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice) 介面，此介面表示 (DLNA) 裝置的主動式數位生活網路聯盟。<br/>                                                                                                                                                                                                                       |
| [**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))<br/>                                           | 執行代表 DLNA 裝置的 [**IBasicDevice**](ibasicdevice.md) 介面。<br/>                                                                                                                                                                                                                                                                             |
| [**CreateMediaRendererOperation**](createmediarendereroperation.md)<br/>         | 註冊當 [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) 或 [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。<br/> |
| [**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))<br/>                                 | 會執行 [**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller) 介面，以抓取快取數位媒體轉譯器的清單 (DMRs) 和/或數位媒體伺服器 (DMSs) ，或以非同步方式尋找目前位於網路上的 DMRs 和/或 DMSs。<br/>                                                                                                            |
| [**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))<br/>                                             | 實 [**IDevicePair**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicepair) 介面，代表一組由轉譯器和伺服器組成的 [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) 物件。<br/>                                                                                                                                                                              |
| [**GetMuteOperation**](getmuteoperation.md)<br/>                                 | 註冊當 [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。<br/>                                                                                                                                                    |
| [**GetPositionInformationOperation**](getpositioninformationoperation.md)<br/>   | 註冊當 [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。<br/>                                                                                                                      |
| [**GetStreamPropertiesOperation**](getstreampropertiesoperation.md)<br/>         | 註冊當 [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。<br/>                                                                                                                            |
| [**GetTransportInformationOperation**](gettransportinformationoperation.md)<br/> | 註冊當 [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。<br/>                                                                                                                    |
| [**GetVolumeOperation**](getvolumeoperation.md)<br/>                             | 註冊當 [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。<br/>                                                                                                                                                |
| [**MediaRenderer**](mediarenderer.md)<br/>                                       | 實 [**IMediaRenderer**](imediarenderer.md) 介面，此介面表示 (DMR) 裝置的 DLNA 數位媒體轉譯器。<br/>                                                                                                                                                                                                                                            |
| [**PlaybackOperation**](playbackoperation.md)<br/>                               | 註冊事件處理常式，此處理程式會在其中一個 [**MediaRenderer**](mediarenderer.md) 播放方法啟動的非同步作業完成時叫用，並提供方法來傳回作業的結果。<br/>                                                                                                                                      |
| [**StreamSelectOperation**](streamselectoperation.md)<br/>                       | 註冊當 [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) 啟動的非同步作業完成時叫用的事件處理常式，並提供方法來傳回作業的結果。<br/>                                                                                                                                                    |
| [**StreamSelector**](streamselector.md)<br/>                                     | 實 [**IStreamSelectorStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-istreamselectorstatics) 介面並啟用選取資料流程。<br/>                                                                                                                                                                                                                                                        |



 

 

