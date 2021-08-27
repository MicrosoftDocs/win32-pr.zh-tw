---
description: 此核心音訊 SDK 的程式設計參考包含下列屬性。
ms.assetid: db7d68c3-5642-4238-a212-88d3479ce73d
title: 核心音訊屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2d6513798a03cbcd9092e24b37900b5eb686d5fd0c434480a933af50c02fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058998"
---
# <a name="core-audio-properties"></a>核心音訊屬性

此核心音訊 SDK 的程式設計參考包含下列屬性。

## <a name="audio-endpoint-properties"></a>音訊端點屬性

Core Audio SDK 包含數個 [音訊端點裝置](audio-endpoint-devices.md)屬性。 如需詳細資訊，請參閱 [音訊端點屬性](audio-endpoint-properties.md)。

下列屬性是在 Windows Vista 和更新版本的 Mmdeviceapi 中定義。



| 屬性                                                                                                            | 描述                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ AudioEndpoint \_ 關聯**](pkey-audioendpoint-association.md)                                          | 將核心串流 (KS) 釘選類別與音訊端點裝置產生關聯。                                                                                |
| [**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider**](pkey-audioendpoint-controlpanelpageprovider.md)                | 為音訊端點裝置的裝置屬性延伸模組指定已註冊提供者的 CLSID。                                              |
| [**PKEY \_ AudioEndpoint \_ Disable \_ SysFx**](pkey-audioendpoint-disable-sysfx.md)                                     | 指出是否已在流入或流出音訊端點裝置的共用模式資料流程中啟用系統效果。                                       |
| [**PKEY \_ AudioEndpoint \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | 指出音訊端點裝置的實體屬性。                                                                                               |
| [**PKEY \_ AudioEndpoint \_ FullRangeSpeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | 指定連線到音訊端點裝置的全範圍喇叭的通道設定遮罩。                                         |
| [**PKEY \_ AudioEndpoint \_ GUID**](pkey-audioendpoint-guid.md)                                                        | 提供對應于音訊端點裝置的 DirectSound 裝置識別碼。                                                                     |
| [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)                                | 定義音訊端點裝置的實體喇叭設定。                                                                                     |
| [**PKEY \_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md)                                            | 指定裝置格式，也就是音訊引擎針對流入或流出音訊端點裝置的共用模式資料流程所使用的格式。       |
| [**PKEY \_ AudioEngine \_ OEMFormat**](pkey-audioengine-oemformat.md)<br/>                                       | 指定用於轉譯或捕捉資料流程之裝置的預設格式。 在 .inf 檔案中，OEM 會填入這些值。 <br/> |
| [**PKEY \_ AudioEndpoint \_ 支援 \_ EventDriven \_ 模式**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | 指出端點是否支援事件驅動模式。 在 .inf 檔案中，OEM 會填入這些值。<br/>                                |
| [**PKEY \_ AudioEndpoint \_ JackSubType**](pkey-audioendpoint-jacksubtype.md)<br/>                               | 包含音訊端點裝置的輸出類別 GUID。 <br/>                                                                                    |



 

## <a name="device-properties"></a>裝置內容

Core Audio SDK 包含數個 [音訊端點裝置](audio-endpoint-devices.md)的裝置屬性。 如需詳細資訊，請參閱 [裝置屬性](device-properties.md)。

下列屬性是在 \_ Windows Vista 和更新版本的 Functiondiscoverykeys devpkey 中定義。



| 屬性                                                                         | 描述                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ DeviceInterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | 端點裝置所連接之音訊介面卡的易記名稱 (例如「XYZ 音訊介面卡」 ) 。                                                                               |
| [**PKEY \_ 裝置 \_ DeviceDesc**](pkey-device-devicedesc.md)                       | 端點裝置的裝置描述 (例如「喇叭」 ) 。                                                                                                                          |
| [**PKEY \_ 裝置 \_ FriendlyName**](pkey-device-friendlyname.md)                   | 端點裝置的易記名稱 (例如「喇叭 (XYZ 音訊介面卡) 」 ) 。                                                                                                           |
| **PKEY \_ 裝置 \_ ContainerId**                                                    | 儲存執行音訊端點之 PnP 裝置的容器識別碼。 如需此屬性的詳細資訊，請參閱 Windows WDK 檔中的「裝置屬性參考」。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計參考](programming-reference.md)
</dt> </dl>

 

 




