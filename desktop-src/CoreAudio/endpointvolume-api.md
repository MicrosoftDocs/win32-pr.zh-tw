---
description: EndpointVolume API
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: EndpointVolume API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22965e882a2f7d413ae58690fc9bc5f8134aba0e7b26838ca38c74d7f0093c98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018446"
---
# <a name="endpointvolume-api"></a>EndpointVolume API

EndpointVolume API 可讓特製化用戶端控制及監視 [音訊端點裝置](audio-endpoint-devices.md)的音量層級。 用戶端會取得 EndpointVolume API 中的介面參考，方法是取得音訊端點裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面，然後呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法。

標頭檔 Endpointvolume 會定義 EndpointVolume API 中的介面。

使用 [MMDEVICE API](mmdevice-api.md) 和 [WASAPI](wasapi.md) 的音訊應用程式通常會使用 [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) 介面來控制每個會話的音量層級。 只有兩種類型的音訊應用程式需要使用 EndpointVolume API。 這些應用程式類型包括：

-   管理音訊端點裝置之主要音量層級的應用程式，類似于 Windows 的音量控制程式 Sndvol.exe。
-   Professional 音訊 ( 「pro 音訊」 ) 需要獨佔模式存取音訊端點裝置的應用程式。

不當使用 EndpointVolume API 可能會干擾 Windows 的音訊原則，並中斷使用者的系統磁片區設定。

如果音訊端點裝置實行硬體磁片區和靜音控制，EndpointVolume API 會使用這些控制項來管理裝置磁片區。 否則，EndpointVolume API 會以透明的方式在用戶端上執行軟體中的控制項。

如果裝置具有硬體磁片區和靜音控制，透過 EndpointVolume API 對裝置磁片區和靜音設定所做的變更，會影響共用模式和獨佔模式中的磁片區層級。 如果裝置缺少硬體磁片區和靜音控制，透過 EndpointVolume API 對軟體磁片區和靜音控制所做的變更，會影響在共用模式中的磁片區層級，但不會影響獨佔模式。 在獨佔模式中，用戶端和裝置會直接交換音訊資料，略過軟體控制項。

對於必須管理硬體磁片區和靜音控制的應用程式，EndpointVolume API 透過 [DEVICETOPOLOGY api](devicetopology-api.md)提供兩個可能的優點。

首先，有一些音訊介面卡裝置缺少硬體磁片區控制項。 如果裝置缺少硬體磁片區控制項，EndpointVolume API 中的 [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) 介面會自動在該裝置的串流上執行軟體磁片區控制。 針對 EndpointVolume API 的用戶端，不論裝置是否已在硬體中或由 EndpointVolume API 介面在軟體中執行磁片區控制，結果都會相同。

其次，即使介面卡裝置確實執行硬體磁片區控制項，使用 DeviceTopology API 來執行拓撲遍歷演算法的應用程式可能會找不到所要尋找的控制項。 一般而言，這類應用程式是設計來跨越特定裝置或一組相關裝置的硬體拓朴。 如果應用程式嘗試跨越尚未特別設計或測試的裝置拓撲，就會發生失敗的風險。

只有必須存取磁片區和靜音控制項以外之硬體功能的特殊應用程式，才需要使用 DeviceTopology API。 針對只需要控制獨佔模式資料流程之磁片區層級的應用程式，EndpointVolume API 較容易使用，而且可以可靠地使用更廣泛的音訊硬體裝置。

如需在 EndpointVolume API 中使用介面的程式碼範例，請參閱下列主題：

-   [端點磁片區控制項](endpoint-volume-controls.md)
-   [尖峰計量](peak-meters.md)

若要查看使用 EndpointVolume API 的範例，請參閱 Windows SDK 中的[EndpointVolume](endpointvolume.md) 。

EndpointVolume API 會執行下列介面。



| 介面                                                | 描述                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | 代表音訊串流上或音訊端點裝置的音量控制項。 |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | 表示音訊串流上或音訊端點裝置的尖峰計量。        |



 

此外，EndpointVolume API 的用戶端必須在音訊端點裝置上執行磁片區和靜音變更的通知，才能執行下列介面。



| 介面                                                            | 描述                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | 當音訊端點裝置的音量層級或靜音狀態變更時，會提供通知。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音量控制項](volume-controls.md)
</dt> <dt>

[**IMMDevice 介面**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 



