---
description: 在 Windows 7 中，[Windows 多媒體] 控制台（Mmsys.cpl）會提供新的 [通訊] 索引標籤。
ms.assetid: bec2127d-fb82-436d-beee-d43e8fef5c35
title: 使用通訊裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f677245e650cf11c71c879b2c26d3183ff4a0b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847377"
---
# <a name="using-a-communication-device"></a>使用通訊裝置

在 Windows 7 中，[Windows 多媒體] 控制台（Mmsys.cpl）會提供新的 [ **通訊** ] 索引標籤。此索引標籤包含的選項可讓使用者設定選項，以定義系統管理 *通訊裝置* 的方式。 通訊裝置主要用於在電腦上撥打電話或接收電話。 如果電腦只有一個轉譯裝置 (喇叭) 和一個) 裝置 (麥克風，這些音訊裝置也會作為預設通訊裝置。 當使用者連接新的裝置（例如 USB 耳機）時，系統會藉由查閱 OEM 所填入的設定來執行自動裝置角色偵測。 如果系統判斷最適合通訊用途的裝置，系統會將 **eCommunications** 角色指派給裝置。 針對這些裝置，Windows 7 Mmsys.cpl 提供選項 **預設通訊裝置** ，讓使用者可以選取每個音訊轉譯的通訊裝置， ([ **播放** ] 索引標籤) 以及音訊捕獲 (**錄製** ] 索引標籤) 。 系統會執行自動角色偵測，但不會設定要用於通訊的特定裝置。 這必須由使用者完成。 新的 **eCommunications** 角色可讓應用程式區分使用者選擇的裝置來處理電話，以及使用裝置作為多媒體裝置， (音樂播放) 。 例如，如果使用者有連接到電腦的耳機和說話者，系統會將 **eConsole** 角色指派給喇叭，並將 **eCommunications** 角色指派給耳機。 當使用者選取用來作為通訊裝置的耳機之後，若要開發通訊應用程式，您可以特別以耳機為目標來呈現音訊串流。 應用程式，使用者無法變更系統指派的裝置角色。 如需裝置角色的詳細資訊，請參閱 [裝置角色](device-roles.md)。

通訊應用程式（例如 VoIP 和整合通訊應用程式）會透過電腦撥打電話及接收電話。 例如，VoIP 應用程式可能會將包含環形通知的串流指派給用於轉譯音訊串流的通訊裝置集合端點。 此外，應用程式可能會在已設定為通訊裝置的捕獲和轉譯端點裝置上，開啟語音輸入和輸出串流。

若要將通訊功能整合到您的應用程式，您可以使用：

-   [MMDEVICE API](mmdevice-api.md)-取得通訊裝置端點的參考。
-   [WASAPI](wasapi.md)-透過通訊裝置轉譯和捕獲音訊串流。 作業系統會將通訊裝置上開啟的串流視為 *通訊串流*。

通訊應用程式會列舉裝置，並為通訊串流提供資料流程管理 (轉譯或捕捉) 串流的方式，與使用核心音訊 Api 來管理非通訊串流的方式相同。

您可以在通訊應用程式中整合的其中一項功能是 *回避* 或 *串流衰減*。 此行為定義在開啟通訊串流時，其他音效必須發生什麼事，例如在通訊裝置上收到電話時。 視使用者的選擇而定，系統可能會將非通訊資料流程的音訊音量靜音或降低。 當開啟或關閉用於轉譯或捕獲資料流程的通訊資料流程時，音訊系統會產生回避事件。 根據預設，作業系統會提供預設的回避體驗。 媒體應用程式可以取代預設行為，並處理這些事件本身，以提供自訂的回避體驗。

下列各節說明如何使用核心音訊 Api 來提供自訂回避體驗。

-   [預設回避體驗](stream-attenuation.md)
-   [停用預設的回避體驗](disabling-the-ducking-experience.md)
-   [提供自訂回避行為](providing-a-custom-ducking-experience.md)
-   [回避通知的執行考慮](handling-audio-ducking-events-from-communication-devices.md)
-   [取得回避事件](getting-ducking-events-from-a-communication-device.md)

### <a name="getting-a-reference-to-the-communication-device-endpoint"></a>取得通訊裝置端點的參考

若要使用通訊裝置，直接 WASAPI 用戶端必須使用裝置枚舉器來列舉裝置。 藉由呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)，取得預設通訊裝置端點的參考。 在此呼叫中，應用程式必須在 *Role* 參數中指定 **eCommunications** ，以將裝置列舉限制為通訊裝置。 取得裝置的裝置端點參考之後，您可以藉由呼叫 [**IMMDevice：： activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)來啟動端點範圍的服務。 例如，您可以傳遞 **iid \_ IAudioClient** 服務識別碼來啟用音訊用戶端物件，並使用它進行串流管理、使用 **iid \_ IAudioEndpointVolume** 識別碼來存取通訊裝置端點的磁片區控制項，或使用 **iid \_ IAudioSessionManager** 識別碼來啟用會話管理員，讓您能夠與端點的原則引擎進行互動。 如需資料流程作業的詳細資訊，請參閱 [資料流程管理](stream-management.md)。

您也可以使用 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 參考，存取裝置端點的屬性存放區。 這些屬性值（例如裝置易記名稱和製造商名稱）會由 OEM 填入，並可讓應用程式判斷通訊裝置的特性。 如需詳細資訊，請參閱 [裝置屬性](device-properties.md)。

下列範例程式碼會取得預設通訊裝置端點的參考，以呈現音訊串流。


```C++
IMMDevice *defaultDevice = NULL;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), NULL,
            CLSCTX_INPROC_SERVER, 
            __uuidof(IMMDeviceEnumerator), 
            (LPVOID *)&deviceEnumerator);

hr = deviceEnumerator->GetDefaultAudioEndpoint(eRender, 
            eCommunications, &defaultDevice);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[串流管理](stream-management.md)
</dt> </dl>

 

 



