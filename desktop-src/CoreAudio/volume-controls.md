---
description: 音量控制項
ms.assetid: b1799372-8d2c-4774-995d-e7926a159d0a
title: 音量控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758fd25d4157030071a47ac8eec26dc0e4d50e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847376"
---
# <a name="volume-controls"></a>音量控制項

管理共用模式資料流程的用戶端通常會使用 [WASAPI](wasapi.md)中的 [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)和 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)介面，來控制和監視資料流程磁片區的層級。 透過 **ISimpleAudioVolume** 介面中的方法，用戶端可以取得和設定共用模式串流所屬 [音訊會話](audio-sessions.md) 的音量層級。 如果 Sndvol 或其他應用程式變更會話磁片區層級，用戶端可以透過 **IAudioSessionEvents** 介面接收變更的通知。

管理獨佔模式資料流程的用戶端通常會使用 [ENDPOINTVOLUME API](endpointvolume-api.md)中的 [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)和 [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback)介面，來控制和監視資料流量層級。 透過 **IAudioEndpointVolume** 介面中的方法，用戶端可以取得並設定 [音訊端點裝置](audio-endpoint-devices.md)的音量層級。 如果 Sndvol 或其他應用程式變更端點裝置的磁片區層級，用戶端可以透過 **IAudioEndpointVolumeCallback** 介面接收變更的通知。

如同 [音訊課程](audio-sessions.md)中所述，Sndvol 是系統音量控制程式。 它會顯示系統中音訊呈現端點裝置的音量控制項。  (目前不會顯示音訊捕獲端點裝置的音量控制項。 ) 若要查看特定裝置的音量控制項，請按一下功能表列中的 [ **裝置** ]，然後從可用裝置清單中選取裝置名稱。

Sndvol 視窗會將裝置的音量控制項分割成兩個群組。 視窗左側的群組方塊會標示為 [ **裝置**]。 [ **裝置** ] 方塊包含由 [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) 介面控制的單一音量控制項。 使用者對此磁片區控制項進行的變更，可以透過 [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) 介面進行監視。

Sndvol 視窗右側的群組方塊會標示為 [ **應用程式**]。 [ **應用程式** ] 方塊包含目前共用裝置之應用程式的磁片區控制項。 針對在共用模式中使用裝置的應用程式，磁片區控制項代表 [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) 介面所控制的磁片區層級。 使用者對這些磁片區控制項所做的變更，可以透過 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面進行監視。

雖然共用模式應用程式可以使用其 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面，來監視使用者在 [Sndvol] 視窗中的 [ **應用程式** ] 方塊中對應用程式音量控制項進行的變更，但應用程式無法監視其他不相關應用程式的磁片區控制項變更。 同樣地，應用程式可以透過 [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) 介面變更其音訊會話的音量層級，但無法變更屬於其他、不相關應用程式之會話的音量層級。

不過，兩個或多個相關的應用程式 (或相同應用程式的實例) 可以在 Sndvol 視窗的 [ **應用程式** ] 方塊中共用相同的音量控制項，方法是將其音訊串流指派給相同的跨進程會話，或將其各自的會話與相同的群組參數建立關聯。 如需詳細資訊，請參閱 [音訊會話](audio-sessions.md) 和 [群組參數](grouping-parameters.md)。

WASAPI 提供兩個額外的介面（ [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) 和 [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)），以控制共用模式資料流程的磁片區層級。 這些介面主要是供特殊用戶端使用，這些用戶端需要控制會話中的個別通道或會話中個別資料流程的磁片區層級。

[DEVICETOPOLOGY API](devicetopology-api.md)可讓用戶端存取音訊介面卡拓撲中的音量控制項。 不過，管理獨佔模式資料流程的用戶端通常會使用 EndpointVolume API，而不是使用 DeviceTopology API 來控制串流磁片區層級。 EndpointVolume API 會以兩種方式簡化端點裝置的控制量。 首先，如果端點裝置會實作為硬體磁片區控制項，則 DeviceTopology API 會要求用戶端在搜尋硬體控制項時，先跨越裝置拓撲。 相反地，EndpointVolume API 會自動尋找用戶端的硬體磁片區控制項。 其次，如果端點裝置未執行硬體磁片區控制，DeviceTopology 用戶端必須在軟體中執行磁片區控制。 相反地，EndpointVolume API 會自動將軟體音量控制項替換為遺漏的硬體控制項。

下列各節說明音訊會話和音訊端點裝置的音量控制項：

-   [會話磁片區控制項](session-volume-controls.md)
-   [端點磁片區控制項](endpoint-volume-controls.md)
-   [EndpointVolume API](endpointvolume-api.md)
-   [音訊-錐形音量控制項](audio-tapered-volume-controls.md)
-   [尖峰計量](peak-meters.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計指南](programming-guide.md)
</dt> </dl>

 

 



