---
description: 回送記錄
ms.assetid: 71c567f7-fffa-4b75-897a-63ed30c4c9b0
title: 回送記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa5ffe48bf11ad57b02085ab00dfd1ca09be0f72a56935cbd8d1bb40543033f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005271"
---
# <a name="loopback-recording"></a>回送記錄

在回送模式中，WASAPI 的用戶端可以捕獲呈現端點裝置所播放的音訊串流。 若要以回送模式開啟資料流程，用戶端必須：

-   取得呈現端點裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面。
-   在轉譯端點裝置上以回送模式初始化捕獲資料流程。

在遵循這些步驟之後，用戶端可以呼叫 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) 方法，以取得轉譯端點裝置上的 [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) 介面。

WASAPI 會提供回送模式，主要是為了支援 (AEC) 的聲場回應取消。 不過，其他類型的音訊應用程式可能會發現回送模式對於捕捉音訊引擎所播放的系統混合很有用。

在 [捕捉資料流程](capturing-a-stream.md)的程式碼範例中，您可以輕鬆地修改 RecordAudioStream 函數來設定回送模式的捕獲資料流程。 必要的修改包括：

-   在 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 方法的呼叫中，將 (*資料流程*) 的第一個參數從 eCapture 變更為 eRender。
-   在 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法的呼叫中，將第二個參數的值 (*StreamFlags*) 從0變更為 AUDCLNT \_ StreamFlags \_ 回送。

在 Windows 10 1703 之前的 Windows 版本中，提取模式捕獲用戶端不會在使用事件驅動緩衝來初始化資料流程時接收任何事件，而且會啟用回送功能。 若要解決這個問題，請在事件驅動模式中初始化轉譯資料流程。 每次用戶端收到轉譯資料流程的事件時，必須通知 capture 用戶端執行捕獲執行緒，以從 capture 端點緩衝區讀取下一組範例。 在 Windows 10 1703 和更新版本中，支援事件驅動的回送用戶端，而且不再需要涉及轉譯資料流程的因應措施。  

用戶端只能針對共用模式串流啟用回送模式， (AUDCLNT \_ SHAREMODE \_ 共用) 。 獨佔模式資料流程無法在回送模式下運作。

WASAPI 回送的執行取決於硬體的功能。 如果硬體支援轉譯端點上的回送 pin，WASAPI 會使用此 pin 提供的音訊來提供回送資料流程。 當硬體不支援回送 pin 時，除了將音訊資料複製到硬體的轉譯 pin 之外，WASAPI 還會將音訊引擎的輸出資料流程複製到回送應用程式的擷取緩衝區。

有些硬體廠商會將回送設備 (，而不是在其音訊介面卡) 的轉譯裝置上釘選實例。 雖然硬體回送裝置類似于 WASAPI 回送模式的操作，但它們可能更難使用。

硬體回送裝置對於音訊應用程式有下列缺點：

-   並非所有音訊介面卡都有回送裝置。 因此，相依于這些應用程式的應用程式將無法在所有系統上運作。
-   在應用程式可以從回送裝置錄製之前，使用者必須先識別回送裝置，並加以啟用以供使用。

不同的廠商會將不同的名稱指派給他們的硬體回送裝置。 以下是範例的名稱：

-   身歷聲混合
-   Waveout 混合
-   混合輸出
-   您聽到的內容

缺乏標準化名稱可能會導致使用者難以識別裝置名稱清單中的回送裝置。

硬體回送裝置是一種捕獲裝置。 因此，如果介面卡支援回送裝置，音訊應用程式可以從裝置記錄，其方式與從任何其他捕獲裝置記錄的方式相同。

例如，如果您選取要做為預設捕獲裝置的硬體回送裝置，則可以使用 RecordAudioStream 函式 (而不需要修改) 在 [捕捉串流](capturing-a-stream.md) 以從裝置捕獲串流的程式碼範例中。  (您也可以使用舊版音訊 API （例如 Windows 多媒體 **waveInXxx** 函式），從裝置捕獲串流。 ) 

如果您的音訊介面卡包含硬體回送裝置，您可以使用 Windows 多媒體控制台 Mmsys.cpl，將裝置指定為預設的擷取裝置。 步驟如下：

1.  若要執行 Mmsys.cpl，請開啟命令提示字元視窗，然後輸入下列命令：

    ```C++
    control mmsys.cpl,,1
    ```

    

    或者，您也可以用滑鼠右鍵按一下通知區域中的喇叭圖示（位於工作列右邊），然後選取 [ **錄製裝置**] 來執行 Mmsys.cpl。

2.  Mmsys.cpl 視窗開啟後，以滑鼠右鍵按一下錄製裝置清單中的任意位置，並確認已核取 [ **顯示已停用的裝置** ] 選項。  (否則，如果回送裝置已停用，它就不會出現在清單中。 ) 
3.  流覽錄製的裝置清單，找出回送裝置 (是否存在) 。 如果回送裝置已停用，請在裝置上按一下滑鼠右鍵，然後按一下 [ **啟用**] 來啟用它。
4.  最後，若要選取作為預設擷取裝置的回送裝置，請在裝置上按一下滑鼠右鍵，然後按一下 [ **設定為預設裝置**]。

無論音訊硬體是否包含回送裝置，或使用者是否已啟用裝置，WASAPI 都支援回送記錄。

WindowsVista 提供 (DRM) 的數位版權管理。 內容提供者依賴 DRM 保護其專屬音樂或其他內容，防止未經授權的複製和其他非法用途。 同樣地，受信任音訊驅動程式不允許回送裝置捕獲包含受保護內容的數位串流。 WindowsVista 只允許信任的驅動程式播放受保護的內容。 如需有關信任的驅動程式和 DRM 的詳細資訊，請參閱 Windows DDK 檔。

無論音訊源自何種終端機服務會話，WASAPI 回送都包含所有播放中音訊的混合。 例如，您可以在會話0執行的服務中執行回送用戶端，並從所有使用者會話捕獲音訊，以及從會話0播放音訊。

遠端桌面可讓您將音訊重新導向至用戶端。 這是藉由建立只顯示該會話的新音訊裝置來實行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[串流管理](stream-management.md)
</dt> </dl>

 

 



