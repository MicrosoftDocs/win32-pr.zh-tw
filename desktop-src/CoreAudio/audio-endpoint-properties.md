---
description: 音訊端點屬性
ms.assetid: db85ff3b-dbb1-4ed0-b663-21ca9eb66352
title: 音訊端點屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ce4ed9b853c2b73b73de014f3a4c8a90072a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187743"
---
# <a name="audio-endpoint-properties"></a>音訊端點屬性

標頭檔 Mmdeviceapi 會在 Windows Vista 和更新版本中定義 [音訊端點裝置](audio-endpoint-devices.md) 的數個屬性。 Windows 音訊服務會設定這些屬性的值。 用戶端可以讀取這些屬性，但是不應該設定它們。 屬性值會儲存為 **PROPVARIANT** 結構。

讀取音訊輸入裝置屬性的建議方式是使用 Windows 中的 Api。 [**列舉**](/uwp/api/Windows.Devices.Enumeration) 命名空間。 Windows Store 應用程式和桌面應用程式支援這些 Api。 針對使用 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面讀取裝置屬性的現有桌面應用程式，請參閱 [裝置屬性](device-properties.md)。 **IMMDevice** 不支援 Windows Store 應用程式。

如需示範如何存取音訊端點裝置屬性的程式碼範例，請參閱下列主題：

-   [裝置事件](device-events.md)
-   [DirectSound 應用程式的裝置角色](device-roles-for-directsound-applications.md)

如需 **PROPVARIANT** 的詳細資訊，請參閱 Windows SDK 檔。

下列是音訊端點裝置專用的屬性。



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



 

核心音訊 Api 支援不會專門用於音訊端點裝置的其他屬性。 如需這些額外屬性的詳細資訊，請參閱 [裝置屬性](device-properties.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊端點裝置](audio-endpoint-devices.md)
</dt> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

