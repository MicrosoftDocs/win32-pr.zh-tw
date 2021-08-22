---
title: IBasicDevice 介面
description: 封裝為 DLNA 裝置建立模型所需的方法和事件。
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- IBasicDevice 介面媒體串流 API
- IBasicDevice 介面媒體串流 API，說明
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25a60a3f722faac473b6f779de2d609cbdfc4ecb257d671136a8ef80535fdf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060358"
---
# <a name="ibasicdevice-interface"></a>IBasicDevice 介面

封裝為 DLNA 裝置建立模型所需的方法和事件。

## <a name="members"></a>成員

**IBasicDevice** 介面繼承自 [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)。 **IBasicDevice** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IBasicDevice** 介面具有這些方法。



| 方法                                                                                 | 描述                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**新增 \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md)       | 註冊 [**ConnectionStatusChanged**](connectionstatuschanged.md) 事件的事件處理常式。<br/>                |
| [**CanWakeDevices**](ibasicdevice-canwakedevices.md)                                  | 抓取值，指出裝置是否可以喚醒。<br/>                                                            |
| [**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))                              | 傳回列舉值，指出裝置目前為線上、離線或睡眠中，但可喚醒。<br/> |
| [**描述**](ibasicdevice-description.md)                                        | 抓取裝置的描述。<br/>                                                                              |
| [**DiscoveredOnCurrentNetwork**](ibasicdevice-discoveredoncurrentnetwork.md)          | 抓取值，指出裝置是否在目前的網路上。<br/>                                           |
| [**FriendlyName**](ibasicdevice-friendlyname.md)                                      | 抓取裝置的易記名稱。<br/>                                                                               |
| [**圖示**](ibasicdevice-icons.md)                                                    | 傳回 [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) 介面的向量。<br/>                                                  |
| [**IpAddresses**](ibasicdevice-ipaddresses.md)                                        | 傳回 IP 位址的向量。<br/>                                                                                   |
| [**ManufacturerName**](ibasicdevice-manufacturername.md)                              | 抓取裝置的製造商名稱。<br/>                                                                           |
| [**ManufacturerUrl**](ibasicdevice-manufacturerurl.md)                                | 抓取裝置的製造商 URL。<br/>                                                                            |
| [**ModelName**](ibasicdevice-modelname.md)                                            | 抓取裝置的模型名稱。<br/>                                                                                  |
| [**ModelNumber**](ibasicdevice-modelnumber.md)                                        | 抓取裝置的模型編號。<br/>                                                                                |
| [**ModelUrl**](ibasicdevice-modelurl.md)                                              | 抓取裝置的模型 URL。<br/>                                                                                   |
| [**PhysicalAddresses**](ibasicdevice-physicaladdresses.md)                            | 傳回實體位址的向量。<br/>                                                                             |
| [**PresentationUrl**](ibasicdevice-presentationurl.md)                                | 抓取裝置的簡報 URL。<br/>                                                                            |
| [**RemoteStreamingUrls**](ibasicdevice-remotestreamingurls.md)                        | 傳回遠端串流 Url 的向量。<br/>                                                                          |
| [**移除 \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) | 取消註冊 [**ConnectionStatusChanged**](connectionstatuschanged.md) 事件的事件處理常式。<br/>              |
| [**SerialNumber**](ibasicdevice-serialnumber.md)                                      | 抓取裝置序號。<br/>                                                                               |
| [**類型**](ibasicdevice-type.md)                                                      | 抓取列舉值，指出 DLNA 裝置的裝置類型。<br/>                                       |
| [**UniqueDeviceName**](ibasicdevice-uniquedevicename.md)                              | 抓取裝置的唯一裝置名稱 (UDN) 。<br/>                                                                    |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

