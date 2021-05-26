---
description: 標頭檔和系統元件
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: 標頭檔和系統元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a47125853b51a71f2f05dacf4534ce33cfedec
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424288"
---
# <a name="header-files-and-system-components"></a>標頭檔和系統元件

下表列出包含四個核心音訊元件之介面定義的標頭檔。



| 核心音訊元件                         | 標頭檔                  |
|----------------------------------------------|------------------------------|
| [MMDevice API](mmdevice-api.md)             | Mmdeviceapi。h                |
| [WASAPI](wasapi.md)                         | Audioclient .h、Audiopolicy。h |
| [DeviceTopology API](devicetopology-api.md) | Devicetopology。h             |
| [EndpointVolume API](endpointvolume-api.md) | Endpointvolume。h             |



 

另一個標頭檔 Audiosessiontypes 則定義 WASAPI 所使用的常數。 這些標頭檔位於目錄% MSSdk% \\ include 中，其中% MSSdk% 是您電腦上 Windows SDK 安裝的根目錄。

上表中的每個 API 都包含一組相關的 COM 介面。 因為音訊串流的某些層面取決於低延遲和精確的同步處理，所以 MMDevice、WASAPI、DeviceTopology 和 EndpointVolume Api 的執行不會使用 Microsoft .NET Framework 或受控執行環境。

核心音訊 Api 會在使用者模式系統元件中執行，Audioses.dll 和 Mmdevapi.dll。 用戶端應用程式不會直接存取這些 Dll 中的進入點。 相反地，用戶端會呼叫 **CoCreateInstance** 或 **CoCreateInstanceEx** 函數來取得 MMDeviceEnumerator 類別物件的 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面。 此物件會列舉系統中的 [音訊端點裝置](audio-endpoint-devices.md) 。 **IMMDeviceEnumerator** 介面是 MMDevice API 的一部分。 從這個介面，用戶端可以直接或間接取得 MMDevice API 中的其他介面，包括 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面。 **IMMDevice** 代表特定的音訊端點裝置。 透過 **IMMDevice**，用戶端可以直接或間接取得 WASAPI、DeviceTopology API 和 EndpointVolume API 中的裝置特定介面。 如需有關 **CoCreateInstance** 和 **CoCreateInstanceEx** 的詳細資訊，請參閱 Windows SDK 檔。 如需有關存取核心音訊 Api 介面的詳細資訊，請參閱 [列舉音訊裝置](enumerating-audio-devices.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows Core 音訊 Api](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



