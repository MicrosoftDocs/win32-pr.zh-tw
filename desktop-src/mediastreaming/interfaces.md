---
title: 媒體串流介面
description: 媒體串流 API 提供下列介面。
ms.assetid: 1E25B452-D23C-4A1D-BC39-A5B719DF2C5D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb21c5c17502c887f78fa223ec2a2f8f814d3998bb75b81812eb4de9919f7342
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972187"
---
# <a name="media-streaming-interfaces"></a>媒體串流介面

[媒體串流 API](media-streaming-api-portal.md)提供下列介面。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                 | 描述                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice)<br/>                           | 代表與 UPnP 裝置相關聯的作用中 [**IBasicDevice**](ibasicdevice.md) 。 <br/>                                                                                                                                          |
| [**IActiveBasicDeviceStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevicestatics)<br/>             | 提供用來建立 [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice) 物件的靜態方法。 <br/>                                                                                                                                            |
| [**IBasicDevice**](ibasicdevice.md)<br/>                                       | 封裝為 DLNA 裝置建立模型所需的方法和事件。<br/>                                                                                                                                                                         |
| [**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)<br/>                             | 封裝取出快取數位媒體轉譯器清單所需的方法和事件 (DMRs) 和/或數位媒體伺服器 (DMSs) ，或是以非同步方式尋找目前位於網路上的 DMRs 和/或 DMSs。<br/>              |
| [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)<br/>                                         | 封裝提供 DLNA 裝置圖示相關資訊所需的方法。<br/>                                                                                                                                                    |
| [**IDevicePair**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicepair)<br/>                                         | 代表一組由轉譯器和伺服器組成的 [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) 物件。<br/>                                                                                                                 |
| [**IMediaRenderer**](imediarenderer.md)<br/>                                   | 封裝代表 DMR) 裝置 (的 DLNA 數位媒體轉譯器所需的方法和事件。<br/>                                                                                                                                        |
| [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)<br/> | 封裝所需的方法，以提供目前可在 DMR 上叫用之方法的相關資訊。<br/>                                                                                                                             |
| [**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)<br/>                     | 封裝非同步建立物件的新實例（此實例會實 [**IMediaRenderer**](imediarenderer.md) 介面）所需的方法。<br/>                                                                               |
| [**IStreamSelectorStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-istreamselectorstatics)<br/>                   | 封裝以非同步方式選取資料流程所需的方法。<br/>                                                                                                                                                                         |
| [**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)<br/>                       | 封裝提供 DMR 目前傳輸相關設定相關資訊所需的方法。 這些設定包括目前的傳輸狀態，以及目前可在 DMR 上叫用哪些方法的相關資訊。<br/> |



 

 

