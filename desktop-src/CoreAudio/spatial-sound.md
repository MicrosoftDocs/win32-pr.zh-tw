---
description: Microsoft 空間音效是 Microsoft 的平台層級解決方案，適用于 Xbox、Windows 和 HoloLens 2 上的空間音效支援，可在接聽程式上方或低於接聽程式) 音訊提示時，啟用環繞和提高許可權 (。
ms.assetid: 4F962F1A-CA4A-4018-BA97-516EA3519650
title: 適用於開發人員的空間音效
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/18/2020
ms.openlocfilehash: 9db3614ea7932af874da351e7a92980d51b90011
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/04/2021
ms.locfileid: "104555276"
---
# <a name="spatial-sound-for-developers"></a>適用於開發人員的空間音效
> [!Note] 
> 本檔的目標物件是開發人員。 如需在裝置上啟用空間音效的終端使用者支援，請參閱 [如何在 Windows 10 中開啟空間音效](https://support.microsoft.com/help/4563140/how-to-turn-on-spatial-sound-in-windows-10)。

Microsoft 空間音效是 Microsoft 的平台層級解決方案，適用于 Xbox、Windows 和 HoloLens 2 上的空間音效支援，可在接聽程式上方或低於接聽程式) 音訊提示時，啟用環繞和提高許可權 (。空間音效可由 Windows 桌面 (Win32) 應用程式，以及在支援的平臺上通用 Windows 平臺 (UWP) 應用程式來運用。 空間音效 Api 可讓開發人員建立音訊物件，以從3D 空間中的位置發出音訊。 動態音訊物件可讓您從空間中的任意位置發出音訊，這可能會隨著時間而改變。 您也可以指定音訊物件從17個預先定義的靜態通道之一發出音效 (可代表真實或虛擬化喇叭的 8.1.4.4) 。 實際的輸出格式是由使用者選取，並且可以從 Microsoft 空間音效的實作為抽象化;音訊將會呈現給現有的喇叭、耳機和家用劇院接收器，而不需要變更任何程式碼或內容。 平臺完全支援 HDMI 和身歷聲耳機輸出的即時杜兼編碼、DTS： X 用於耳機，以及適用于身歷聲耳機的耳機用 Windows Sonic 編碼。 最後，Microsoft 空間音效應用程式遵守系統混合原則，而其音訊也會與非空間感知應用程式混合。 Microsoft 空間音效支援也已整合至媒體基礎;使用媒體基礎的應用程式可以成功地播放杜比 Atmos 內容，而不需執行其他任何程式。

具有 Microsoft 空間音效的空間音效支援支援杜比的電視、家用劇院和音效。 空間音效也可以搭配消費者可能擁有的任何一對耳機使用，並使用耳機用 Windows Sonic、Dolby Atmos for Headphones 或 DTS 耳機： X 以平臺轉譯音訊。


## <a name="enabling-microsoft-spatial-sound"></a>啟用 Microsoft 空間音效

不論是開發人員或取用者，使用者都必須在其裝置上啟用 Microsoft 空間音效，才能聽到 hrtf 音效。

### <a name="windows"></a>Windows
在 Windows 電腦上，這是透過指定音效輸出裝置的 [內容] 頁面來完成。 從 **音效** 控制台選取輸出裝置，然後按一下 [ **裝置屬性**]。 在頁面的 [ **空間音效** ] 區段中，如果裝置支援空間音效，您可以從 [ **空間音效格式** ] 下拉式清單中選取其中一種可用的格式。

![在音效控制台中啟用空間音效](images/spatialsoundsettingswindows1.png)

您也可以用滑鼠右鍵按一下工作列中的 **音量** 圖示來啟用 Microsoft 空間音效。

![從工作列啟用空間音效](images/spatialsoundsettingswindows2.png)

### <a name="xbox-one"></a>Xbox One
在 Xbox One 上，適用于取用者的 Microsoft 空間音效功能一律可供取用者使用，並可透過 **[一般] > 音量 & 音訊輸出** 中的 [設定] 應用程式啟用。


![在 [設定] 應用程式中啟用 xbox one 的空間音效 ](images/audiosettingsbitstream.png)

將 [家用劇院] 的 [杜比 Atmos] 選取為 [位流格式] 之後，就會透過 HDMI 擴充顯示器識別資料 (EDID) 來檢查此格式的支援。 如果 HDMI 裝置不支援此格式，則會向使用者顯示錯誤訊息。 請注意，第一次需要使用者下載 Dolby Access 應用程式時，請選取此選項。

如果為 **HDMI 音訊** 選取了 "位流 out" 以外的格式，則會停用 [ **位流格式** ] 下拉式清單。

![在 [設定] 應用程式中的 xbox one 上停用空間音效 ](images/audiosettingsplain.png)

從 **耳機音訊** 下的 **耳機格式** 下拉式清單中選取 Dolby Atmos for Headphones、DTS 耳機： X 或耳機用 Windows Sonic

![在 [設定] 應用程式的 xbox one 上啟用耳機的空間音效 ](images/audiosettingsheadphone.png)

當 Microsoft 空間音效無法使用時 (例如，當您播放 embedded 膝上型電腦身歷聲喇叭，或使用者未明確啟用每個以上) 的 Microsoft 空間音效時， [**ISpatialAudioClient：： GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) 對應用程式所傳回的可用動態物件數目將會是0。

### <a name="hololens-2"></a>HoloLens 2

在 HoloLens 2 上，預設會啟用 Microsoft 空間音效，並使用專門針對耳機用 Windows Sonic 所設計的硬體 DSP 卸載。

## <a name="microsoft-spatial-sound-and-audio-middleware"></a>Microsoft 空間音效和音訊中介軟體

許多應用程式和遊戲開發人員使用協力廠商音訊轉譯引擎解決方案，通常包括精密的撰寫和試聽工具。 Microsoft 已與數個解決方案提供者合作，在現有的撰寫環境中實行 Microsoft 空間音效。 這通常表示從應用程式的觀點來看，這裡討論的 Api 是抽象的，它們會包裝為數字信號處理 (可具現化應用程式的 DSP) 外掛程式，以及應用程式的音訊實作者可以用來混合到 Microsoft 空間音效 channel 床、submix，或視需要將個別語音傳送給動態物件實例外掛程式。 請洽詢您的音訊中介軟體解決方案提供者，以瞭解其對 Microsoft 空間音效的支援層級。

## <a name="microsoft-spatial-sound-for-audio-renderers"></a>適用于音訊轉譯器的 Microsoft 空間音效

許多音訊轉譯器都是以 Windows 音訊會話 API 為目標 (WASAPI) [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 端點，其中應用程式會將混合和採用格式之音訊資料的緩衝區輸出到 WASAPI 音訊接收器;接著會使用傳遞的緩衝區來與其他用戶端、最終的系統層級處理和轉譯進行混合。

Microsoft 空間音效空間端點會實作為 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)，與 **IAudioClient** 有許多相似之處。 它支援形成通道床的 *靜態* 音效物件，最多可支援 8.1.4.4 (通道，在接聽程式的周圍有8個通道：左邊、右邊、中央、左邊、右邊、左方、向右和後置：1個低頻率效果頻道;接聽程式上方的4個通道;接聽程式) 的4個通道。 此外，它也支援 *動態* 音效物件，這些物件可任意放置於3d 空間中。

**ISpatialAudioClient** 的一般執行程式碼撰寫模式如下：

-   建立靜態和/或動態音訊物件。
-   將每個物件的音訊緩衝區送入每個框架，讓系統可以轉譯它。
-   視需要將動態物件的3D 位置更新為應用程式所需的頻繁 (或不常) 。

請注意，目前的輸出格式 (喇叭或耳機;耳機用 Windows Sonic、杜比 Atmos 或 DTS 耳機： X) 是從上述的實作為抽象化，應用程式開發人員可以專注于空間音效，而不需要根據格式進行資料透視。 如果應用程式想要根據輸出格式來分離行為，可以查詢使用中的格式，但抽象表示應用程式不需要處理這些格式。

## <a name="microsoft-spatial-sound-integration-with-audio-renderers"></a>Microsoft 空間音效與音訊轉譯器的整合

因為 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) 是使用資料的音訊接收器，所以音訊轉譯器有數個選項，可讓您與之互動和傳遞音訊資料給它。 有三種常用的整合技巧 (以及使用音訊中介軟體的標題，您可能會看到根據這些選項所提供的對應外掛程式) ：

-   **7.1.4 panners 和掌控語音**：已支援7.1 端點的轉譯器，可選擇直接新增 **ISpatialAudioClient** 靜態通道平臺支援之四個額外高度通道的支援。 先前所做過的任何頻道移動 (可能已經利用 x、y、z 座標) 可以更新成現在包含這些高度通道。 這通常會提供轉譯器和應用程式音訊工作流程、信號、流程和混合控制的最少干擾。 在耳機上，請注意完整的應用程式混合將會 hrtf，因此甚至身歷聲音樂也可以從接聽程式被視為「外部化」。
-   **維護現有的端點，再加上7.1.4 匯流排 (和 panners)**：某些標題可能會選擇維護兩個端點：其現有的身歷聲 WASAPI 端點 (適用于「直接到耳」內容，而不是 hrtf) 與支援 ISpatialAudioClient (的 **7.1.4** 靜態通道平臺或甚至高達 8.1.4.4) 。 當然，管理兩個混合之間的互動會對內容建立者帶來額外的挑戰，雖然會維持同步處理，但是在指定時間內作用中的 WASAPI 和 ISAC 實例都使用相同的緩衝區大小和時鐘進行處理。
-   **針對特定聲音或 Submixes 使用動態音效物件**：提供最詳細/精確的定位，但可能建立混合的不透明度，這項技術牽涉到使用 **ISpatialAudioClient** 動態音效物件。 請注意，中繼資料加上音訊緩衝區會傳遞至轉譯器，因此這些音效對應用程式混合的其餘部分會是不透明的。 此外，由於可用的動態音效物件數目有限，因此轉譯器必須考慮採用優先順序技術–剔除、音效共置、混合到靜態 channel 床等等。 遊戲經常針對個別的「主圖」音效使用這項技術，例如會在接聽程式上方移動的直升機。

轉譯器也可以在這些方法之間進行混合和比對。

## <a name="microsoft-spatial-sound-runtime-resource-implications"></a>Microsoft 空間音效執行時間資源含意

在 Windows 和 Xbox 上，可用的語音數目會根據使用中的格式而有所不同。 杜比 Atmos 格式支援32的作用中物件總數 (因此，如果 7.1.4 channel 床正在使用中，則可以) 20 個額外的動態音效物件。 耳機用 Windows Sonic 支援128個作用中物件總數，並具有低頻率的效果 (LFE) 通道實際上不會被視為物件，因此當 8.1.4.4 channel 床正在使用中時，112動態音效物件可以處於作用中狀態。

針對在 Xbox One 遊戲主控台上執行的通用 Windows 平臺應用程式，即時編碼 (以針對家用劇院、Dolby Atmos for Headphones、DTS 耳機： X 和耳機用 Windows Sonic) 在硬體中執行，不需 CPU 成本。

| 格式                       |  (Channel 床的最大靜態物件)  | 最大動態物件 <br> Xbox One | 最大動態物件 <br> Windows | 最大動態物件 <br> HoloLens 2
|------------------------------|----------------------------------|-------------------------------------------|------------------------------------------|------------------------------------------|
| 杜比 Atmos (HDMI)            | 12 (7.1.4)                        | 20                                        | 20                                       | NA |
|  (耳機 & 內建的喇叭)      | 17 (8.1.4.4)                      | 16                                        | 16                                       | NA |
| DTS 耳機： X (耳機)  | 17 (8.1.4.4)         | 16                                        | 32                                      | NA |
| 耳機用 Windows Sonic | 17 (8.1.4.4)         | 15                                        | 112                                      | 31 |


應用程式也應該考慮下列資源含意：

-   **儲存體/光碟頻寬**：預先編寫給7.1.4 的線性內容通常會大於7.1 線性內容 (但感知編解碼器通常會利用通道相互關聯，使其遠低於50% 的音訊資料通道) 
-   **其他數位信號處理成本**：某些先前的全域效果現在可能會成為每個動態音效物件的實例。 此外，某些內容建立者可能會想要更新某些 DSP 效果，以支援其他通道或使用它們。

## <a name="microsoft-spatial-sound-and-sound-spatialization-cues"></a>Microsoft 空間音效和音效 Spatialization 提示

Microsoft 空間音效著重在接聽程式周圍理想化球體的音效定位模擬。 耳機用 Windows Sonic、DTS 耳機： X 和杜型 Atmos 可將說話者對應和虛擬化運用於耳機，但請注意，許多其他的音效空間模擬功能，通常都是以內容建立者為啟用的方式來執行，這會留給現有的引擎。 內容建立者會繼續使用現有的遊戲工具和先前針對這類空間提示所擁有的 Doppler、以距離為基礎的衰減和篩選、遮蔽和障礙物，以及環境殘響。

## <a name="additional-resources"></a>其他資源

-   [Microsoft 空間音效範例 github 存放庫](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio)
-   杜比提供許多與杜和 Dolby Access 應用程式相關的支援資源 <https://developer.dolby.com> 。

## <a name="spatial-sound-interfaces"></a>空間音效介面



| 介面                                                                              | 描述                                                                                                                    |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)                                     | 讓用戶端能夠建立音訊串流，以從3D 空間中的位置發出音訊。                                          |
| [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)                                     | 表示物件，這個物件會提供從3D 空間中的位置（相對於使用者）轉譯音訊資料的物件。                |
| [**ISpatialAudioObjectRenderStream**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)             | 提供控制空間音訊物件轉譯資料流程的方法，包括啟動、停止和重設資料流程。 |
| [**ISpatialAudioObjectRenderStreamNotify**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreamnotify) | 提供空間音訊用戶端的通知，以回應 ISpatialAudioObjectRenderStream 狀態的變更。     |



 

> [!Note]  
> 在 Xbox One 開發工具組上使用 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) 介面時 (XDK) 標題，您必須先呼叫 **EnableSpatialAudio** ，然後再呼叫 [**IMMDeviceEnumerator：： EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) 或 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)。 若未這麼做，將會導致 \_ 從啟動的呼叫傳回電子 NOINTERFACE 錯誤。 **EnableSpatialAudio** 僅適用于 XDK 標題，不需要針對 Xbox One 上執行的通用 Windows 平臺應用程式，或任何非 Xbox One 裝置呼叫。

 

## <a name="spatial-sound-structures"></a>空間音效結構



| 結構                                                                                                 | Description                                                                  |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) | 代表空間音訊轉譯資料流程的啟用參數。          |
| [**SpatialAudioClientActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioclientactivationparams)                          | 代表空間音訊轉譯資料流程的選擇性啟動參數。 |



 

## <a name="spatial-sound-enumerations"></a>空間音效列舉



| 列舉型別                                | 描述                                   |
|--------------------------------------------|-----------------------------------------------|
| [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) | 指定 ISpatialAudioObject 的類型。 |



 

 

 



