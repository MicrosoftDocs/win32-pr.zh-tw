---
description: 裝置格式
ms.assetid: 591437e4-21ef-42f1-a752-7f50440cbd63
title: 裝置格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332f3ecd4b30213328552077bdef040a63e31992deaf217b77838dd0cd0797f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957337"
---
# <a name="device-formats"></a>裝置格式

針對音訊應用程式，使用較高層級音訊 API （例如 DirectSound 或 Windows 多媒體 **waveOutXxx** 函式）的優點是，API 會自動轉換應用程式所使用的資料流程格式，以及音訊裝置所使用的格式。 相反地，核心音訊 Api 的限制較高，因為它們需要應用程式資料流程使用與裝置所使用的格式相同或密切相關的格式。 因此，使用核心音訊 Api 來播放或錄製音訊串流的應用程式，可能需要執行資料流程格式之間的部分或所有轉換。

使用 WASAPI 管理共用模式資料流程的應用程式，可以依賴音訊引擎來執行有限的格式轉換。 音訊引擎可以在應用程式所使用的標準 PCM 樣本大小與引擎用於其內部處理的浮點範例之間進行轉換。 不過，應用程式資料流程的格式通常必須有相同數目的通道，以及與裝置使用的資料流程格式相同的取樣率。

如果應用程式使用獨佔模式中的裝置，應用程式必須使用音訊硬體明確支援的串流格式。 在獨佔模式中，應用程式和裝置會直接交換音訊資料，而不會由音訊引擎介入。

許多音訊裝置都支援 PCM 和非 PCM 串流格式。 不過，音訊引擎只能混合 PCM 串流。 因此，只有獨佔模式串流可以有非 PCM 格式。 此外，獨佔模式僅支援具有固定資料速率的非 PCM 格式。 固定速率非 PCM 格式的範例是 48-kHz Windows Media 音訊 Professional (WMA Pro) 音訊串流，以數位形式傳遞未經過解碼的索尼/Philips 數位介面 (S/PDIF) 連結。 如需有關使用 WMA Pro stream over S/PDIF 的詳細資訊，請參閱下列檔：

-   在 \_ \_ \_ Windows DDK 檔中，WAVE 格式 WMA SPDIF wave 格式標記的說明。
-   「音訊驅動程式支援 WMA Pro over S/PDIF 格式」白皮書的白皮書，[適用于 Windows 網站的音訊裝置技術](https://www.microsoft.com/whdc/device/audio/default.mspx)。

WASAPI 使用 **WAVEFORMATEX** 或 **WAVEFORMATEXTENSIBLE** 結構來指定資料流程格式。 **WAVEFORMATEXTENSIBLE** 結構實際上是一種已擴充的 **WAVEFORMATEX** 結構，可描述更大範圍的格式。 可由獨立 **WAVEFORMATEX** 結構描述的任何格式，也可以透過 **WAVEFORMATEXTENSIBLE** 結構來描述。

**WAVEFORMATEXTENSIBLE** 結構的第一個成員是 **WAVEFORMATEX** 結構。 **WAVEFORMATEX** 結構的內容會指出它是獨立的 **WAVEFORMATEX** 結構，還是一部分的 **WAVEFORMATEXTENSIBLE** 結構。

獨立的 **WAVEFORMATEX** 結構可以充分描述具有一或兩個通道的格式，以及一個大小為8位的樣本大小。 **WAVEFORMATEX** 結構本身無法指定通道與喇叭位置的對應。 此外，雖然 **WAVEFORMATEX** 會指定每個音訊樣本的容器大小，但無法在 (範例中指定有效位數的位數，例如，24位容器中的20位精確度) 。 相反地， **WAVEFORMATEXTENSIBLE** 結構可以同時指定通道與喇叭的對應，以及每個樣本中的位數位數。

如需有關 **WAVEFORMATEX** 和 **WAVEFORMATEXTENSIBLE** 的詳細資訊，請參閱 Windows DDK 檔。

從 Windows 7 開始， **WAVEFORMATEXTENSIBLE** 已擴充為代表裝置格式，可透過 IEC 61937 相容介面傳輸編碼的音訊。 如需新結構的詳細資訊，請參閱 [代表 IEC 61937 傳輸的格式](representing-formats-for-iec-61937-transmissions.md)。

### <a name="specifying-the-device-format"></a>指定裝置格式

下列 WASAPI 方法會使用 **WAVEFORMATEX** 和 **WAVEFORMATEXTENSIBLE** 結構來描述資料流程格式：

-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)
-   [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

**GetMixFormat** 方法會抓取音訊引擎用來內部處理共用模式資料流程的資料流程格式。 方法一律會使用 **WAVEFORMATEXTENSIBLE** 結構，而不是使用獨立的 **WAVEFORMATEX** 結構來指定格式。

**IsFormatSupported** 方法會指出音訊端點裝置是否支援特定的串流格式。 呼叫端必須指定資料流程格式是否要在共用模式或獨佔模式中使用。 若是共用模式格式，方法會查詢音訊引擎來判斷它是否支援指定的格式。 針對獨佔模式格式，方法會查詢設備磁碟機。 如果格式是由獨立的 **WAVEFORMATEX** 結構所指定，則某些設備磁碟機將會報告其支援1個通道或2通道 PCM 格式，但如果 **WAVEFORMATEXTENSIBLE** 結構指定了格式，則會拒絕相同的格式。 若要從這些驅動程式取得可靠的結果，獨佔模式應用程式應該針對每個單聲道或2通道 PCM 格式呼叫 **IsFormatSupported** 兩次：一個呼叫應該使用獨立的 **WAVEFORMATEX** 結構來指定格式，而另一個呼叫應該使用 **WAVEFORMATEXTENSIBLE** 結構來指定相同的格式。

在應用程式使用 **GetMixFormat** 或 **IsFormatSupported** 來尋找適當的共用模式或獨佔模式資料流程格式之後，應用程式就可以呼叫 **initialize** 方法，以使用該格式來初始化資料流程。 嘗試初始化共用模式資料流程的應用程式，其格式與從 **GetMixFormat** 方法取得的混合格式不同，但具有相同數目的通道和混合格式的取樣速率，可能會成功。 在呼叫 **initialize** 之前，應用程式可以呼叫 **IsFormatSupported** 來確認 **initialize** 將接受格式。

音訊引擎用來進行共用模式資料流程內部處理的混合格式，與音訊端點裝置在共用模式中使用的資料流程格式不一定相同。 透過 Windows 多媒體控制台 Mmsys.cpl，使用者可以選取音訊端點裝置在共用模式中運作時將使用的流格式。 步驟如下：

1.  若要執行 Mmsys.cpl，請開啟命令提示字元視窗，然後輸入下列命令：

    **控制項 mmsys.cpl**

    或者，您也可以用滑鼠右鍵按一下通知區域（位於工作列右邊）中的喇叭圖示，然後選取 [ **播放裝置** ] 或 [ **錄製裝置**]，來執行 Mmsys.cpl。

2.  Mmsys.cpl 視窗開啟後，從播放裝置清單或錄製裝置清單中選取裝置，然後按一下 [內容 **]。**
3.  當 [屬性] 視窗開啟時，按一下 [ **Advanced**]，然後從標示為 [ **預設格式**] 方塊中的可用格式清單中選取格式。

例如，假設使用者從播放裝置的可用格式清單中選取下列預設格式：

**2聲道、16位、44100 Hz (CD 品質)**

這是裝置在共用模式中運作時，後續將使用的格式。 在 Windows Vista 中，音訊引擎會使用此格式的稍微修改版本，來進行共用模式資料流程的內部處理。 音訊引擎會使用具有相同通道數目的格式 (兩個) 和相同的取樣率 (44100 Hz) ，但它會先將樣本轉換成浮點數，再進行處理。 音訊引擎會將輸出混合中的浮點樣本轉換成16位整數，然後才能透過裝置播放這些樣本。

應用程式可以查詢音訊端點裝置的 [**PKEY \_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md) 屬性，以取得使用者為裝置選取的共用模式格式。 如需查詢裝置屬性的詳細資訊，請參閱 [裝置屬性](device-properties.md)。

某些應用程式可能會發現裝置的 **PKEY \_ AudioEngine \_ DeviceFormat** 屬性所指定的格式，是在裝置上開啟獨佔模式串流的適當格式。 其他管理獨佔模式資料流程的應用程式可能會有其他需求，而這些需求會要求與裝置進行複雜的格式協商。 一般來說，其中一個應用程式會使用清單開頭的慣用格式來建立適當格式的清單。 然後，應用程式會反復地以清單中的每個後續格式來呼叫 **IsFormatSupported** ，並從清單的開頭開始，直到找到裝置支援的格式為止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊端點裝置](audio-endpoint-devices.md)
</dt> </dl>

 

 



