---
description: DeviceTopology API
ms.assetid: 051311ef-dd29-4014-bb9c-4cdccf7ce7de
title: DeviceTopology API
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 3b79def9f1cb1f5ec9342074b813e50993cbc37e7a7af2a9e0b577c730156247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406753"
---
# <a name="devicetopology-api"></a>DeviceTopology API

請參閱[Microsoft 高品質語音捕獲 DMO 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/audio/aecmicarray)。

DeviceTopology API 可讓用戶端應用程式能夠跨越音訊轉譯和捕獲裝置的功能性硬體拓撲。 透過 DeviceTopology API 中的介面和方法，用戶端可以探索功能次單元連接 (例如，沿著 [音訊端點裝置](audio-endpoint-devices.md)的資料路徑中的音量控制) 。 用戶端可以跨越兩個音訊介面卡裝置和音訊端點裝置的內部拓撲，以及跨連線將一部裝置連結至另一個裝置的步驟。 如需詳細資訊，請參閱 [裝置拓撲](device-topologies.md)。

標頭檔 Devicetopology 會定義 DeviceTopology API 中的介面。

若要存取 DeviceTopology API 介面，用戶端會先依照下列步驟取得音訊端點裝置的 [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) 介面參考：

1.  使用 [**IMMDevice 介面**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)中所述的其中一種技術，取得音訊端點裝置的 **IMMDevice** 介面參考。
2.  呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法，並將參數 *Iid* 設定為 **REFIID** iid \_ IDeviceTopology。

用戶端可以藉由呼叫 [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) 介面中的方法，取得 DeviceTopology API 中其他介面的參考。

DeviceTopology API 會執行下列介面。



| 介面                                                  | 描述                                                                                                                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | 提供硬體自動增益控制 (AGC) 的存取權。                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | 提供硬體低音等級控制項的存取權。                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | 提供硬體通道配置控制項的存取權。                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | 提供硬體多工器控制項 (輸入選取器) 的存取權。                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | 提供對 "音量" 補償控制項的存取。                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | 提供硬體中型層級控制項的存取權。                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | 提供硬體靜音控制項的存取。                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | 提供硬體信號信號控制 (輸出選取器) 的存取權。                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | 提供硬體尖峰計量控制項的存取權。                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | 提供硬體高音層級控制項的存取。                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | 提供硬體磁片區控制項的存取權。                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                           | 表示元件之間的連接點。                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)             | 代表元件上的控制項介面， (子或連接器) 。                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | 代表連接器或子單位的裝置特定屬性。                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                 | 提供對音訊裝置拓撲的存取。                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)               | 提供有關軟體設定的 i/o 連線所支援之音訊資料格式的資訊 (通常是音訊裝置和系統記憶體之間) DMA 通道。                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)           | 提供有關插座或內部連接器的資訊，這些連接器會提供音訊介面卡上裝置與外部或內部端點裝置之間的實體連線 (例如麥克風或 CD 播放機) 。 |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                     | 代表裝置拓撲的部分 (連接器或次級) 。                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                           | 代表 (連接器和次單元連接) 的部分清單。                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)           | 代表泛型次級控制項介面，可針對音訊串流的音量層級或音訊串流中的頻率寬線，提供每個通道的控制。                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                               | 代表硬體子單位 (例如，位於用戶端和音訊端點裝置之間的資料路徑中的磁片區層級控制) 。                                                                             |



 

在連接器和次單元連接中需要控制項變更事件通知的 DeviceTopology API 用戶端應該執行下列介面。



| 介面                                            | 描述                                                                      |
|------------------------------------------------------|----------------------------------------------------------------------------------|
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify) | 當元件 (連接器或子) 的狀態變更時，會提供通知。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置拓撲](device-topologies.md)
</dt> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 
