---
title: 裝置和資料類型
description: 裝置和資料類型
ms.assetid: 46247983-19c3-4c7a-a615-ba6cd8bd3289
keywords:
- 波形音訊，開啟輸出裝置
- 波形-音訊介面，開啟輸出裝置
- 開啟波形音訊輸出裝置
- 波形音訊，查詢輸出裝置
- 波形-音訊介面，查詢輸出裝置
- 查詢波形音訊輸出裝置
- 波形音訊、裝置控點
- 波形-音訊介面、裝置控點
- 波形音訊、裝置識別碼
- 波形-音訊介面、裝置識別碼
- 波形音訊，輸出資料類型
- 波形-音訊介面、輸出資料類型
- 波形音訊，資料格式
- 波形-音訊介面、資料格式
- 寫入波形-音訊資料
- 波形音訊，寫入資料
- 波形-音訊介面，寫入資料
- PCM 波形-音訊資料
- 波形音訊、PCM 資料
- 波形-音訊介面、PCM 資料
- 波形音訊，關閉輸出裝置
- 波形-音訊介面，關閉輸出裝置
- 關閉波形-音訊輸出裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29561a74695fb8bde950e2e75a430803a1a0351b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966856"
---
# <a name="devices-and-data-types"></a>裝置和資料類型

本節說明如何使用波形音訊裝置，並包含如何開啟、關閉和查詢其功能的相關資訊。 它也會說明如何使用裝置控制碼和裝置識別碼，來追蹤系統中的裝置。

## <a name="opening-waveform-audio-output-devices"></a>開啟 Waveform-Audio 輸出裝置

使用 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) 函式來開啟波形音訊輸出裝置以進行播放。 此函式會開啟與指定裝置識別碼相關聯的裝置，並藉由撰寫指定記憶體位置的控制碼，傳回開啟裝置的控制碼。

有些多媒體電腦有多個波形音訊輸出裝置。 除非您想要在系統中開啟特定的波形音訊輸出裝置，否則 \_ 當您開啟裝置時，應該針對裝置識別碼使用 WAVE 對應程式旗標。 **WaveOutOpen** 函式會在系統中選擇最能播放指定資料格式的裝置。

## <a name="querying-audio-devices"></a>查詢音訊裝置

Windows 提供下列功能來判斷系統中有多少裝置具有特定類型。



| 函式                                       | 描述                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------|
| [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)         | 抓取系統中出現的輔助輸出裝置數目。      |
| [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)   | 抓取系統中顯示的波形音訊輸入裝置數目。  |
| [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) | 抓取系統中出現的波形音訊輸出裝置數目。 |



 

音訊裝置是由裝置識別碼來識別。 裝置識別碼是由系統中的裝置數目隱含決定。 裝置識別碼的範圍介於0到1之間，且小於裝置數目。 例如，如果系統中有兩個波形音訊輸出裝置，則有效的裝置識別碼為0和1。

判斷系統中有多少個特定類型的裝置之後，您可以使用下列其中一項功能來查詢每個裝置的功能。



| 函式                                       | 描述                                                             |
|------------------------------------------------|-------------------------------------------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | 抓取指定之輔助輸出裝置的功能。      |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | 抓取指定之波形音訊輸入裝置的功能。  |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | 抓取指定之波形音訊輸出裝置的功能。 |



 

這些函式中的每一個都會以指定裝置功能的相關資訊填入結構。 下表列出對應至每個函數的結構。



|                                                |                                    |
|------------------------------------------------|------------------------------------|
| 函式                                       | 結構                          |
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)         |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)   |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) |



 

標準格式會列在 **WAVEOUTCAPS** 結構的 **dwFormats** 成員中。 波形-音訊裝置可支援非標準格式。 若要判斷裝置是否支援特定格式 (標準或非標準) ，您可以使用 WAVE [](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) \_ 格式查詢旗標來呼叫 waveOutOpen 函數 \_ 。 此旗標不會開啟裝置。 您可以在傳遞給 **waveOutOpen** 的 *pwfx* 參數所指向的 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)結構中指定有問題的格式。

波形-音訊輸出裝置所支援的功能不同。 [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)結構的 **dwSupport** 成員會指出裝置是否支援磁片區和音調變更這類功能。

## <a name="device-handles-and-device-identifiers"></a>裝置控制碼和裝置識別碼

開啟音訊裝置的每個函式都會指定裝置識別碼、記憶體位置的指標，以及每種裝置類型特有的一些參數。 記憶體位置會以裝置控制碼填滿。 呼叫其他音訊函式時，請使用此裝置控制碼來識別開啟的音訊裝置。

音訊裝置的識別碼和控制碼之間的差異很微妙，但很重要：

-   裝置識別碼是由系統中出現的裝置數目隱含決定。 您可以使用 [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)、 [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)或 [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) 函數來取得這個數位。
-   使用 [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) 或 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) 函式開啟設備磁碟機時，會傳回裝置控制碼。

沒有可開啟或關閉輔助音訊裝置的函式。 因為沒有任何與它們相關聯的連續資料傳輸，所以不需要開啟和關閉輔助音訊裝置，例如波形音訊裝置。 所有輔助音訊功能都會使用裝置識別碼來識別裝置。

## <a name="waveform-audio-output-data-types"></a>Waveform-Audio 輸出資料類型

下列資料類型是針對波形音訊輸出函式所定義。



| 類型                                 | Description                                                                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEOUT**                         | 開啟波形音訊輸出裝置的控制碼。                                                                                                               |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | 結構，指定特定波形音訊輸入裝置所支援的資料格式。 此結構也會 usedfor 波形-音訊輸入裝置。 |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | 結構，用來做為波形音訊輸入資料區塊的標頭。 此結構也可用於波形音訊輸入裝置。                            |
| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)   | 用來查詢特定波形音訊輸出裝置功能的結構。                                                                        |



 

## <a name="specifying-waveform-audio-data-formats"></a>指定 Waveform-Audio 資料格式

當您呼叫 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) 函式來開啟設備磁碟機以供播放，或查詢驅動程式是否支援特定的資料格式時，請使用 *pwfx* 參數來指定 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) 結構的指標，其中包含要求的波形-音訊資料格式。 **WAVEFORMATEX** 會取代 [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) 和 [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) 結構。

如果音訊資料分成兩個以上的通道，或其樣本大小不是8的倍數，您應該使用 [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)。 此結構只會設定 **WAVEFORMATEX** 的 **cbSize** 成員所指向的額外位元組，以提供有關格式的額外資訊。 **WAVEFORMATEXTENSIBLE** 可以轉換成 **WAVEFORMATEX**。

另外還有兩種剪貼簿格式可供您用來代表音訊資料： CF \_ WAVE 和 cf \_ RIFF。 使用 CF \_ WAVE 格式來代表其中一種標準格式的資料，例如 11 khz 或 22 KHZ PCM。 使用 CF \_ RIFF 格式來表示更複雜的資料格式，而這些格式無法表示為標準波形-音訊檔案。

## <a name="writing-waveform-audio-data"></a>寫入 Waveform-Audio 資料

成功開啟波形音訊輸出設備磁碟機之後，您就可以開始播放音效。 Windows 提供 [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) 函式，可將資料區區塊轉送到波形音訊輸出裝置。

使用 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) 結構來指定您使用 **waveOutWrite** 傳送的波形音訊資料區塊。 此結構包含鎖定資料區塊的指標、資料區塊的長度，以及某些旗標。 您必須先備妥此資料區塊，才能使用它。如需準備資料區塊的相關資訊，請參閱 [音訊資料區塊](audio-data-blocks.md)。

使用 **waveOutWrite** 將資料區區塊轉送到輸出裝置之後，您必須等到設備磁碟機完成後再釋放資料區塊。 如果您要傳送多個資料區塊，則必須監視資料區塊的完成，以瞭解何時傳送其他區塊。 如需資料區塊的詳細資訊，請參閱 [音訊資料區塊](audio-data-blocks.md)。

## <a name="pcm-waveform-audio-data-format"></a>PCM Waveform-Audio 資料格式

[**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構 Pointsetts 的 **lpData** 成員會至波形音訊資料樣本。 若為8位 PCM 資料，每個範例都會以單一不帶正負號的資料位元組來表示。 若是16位 PCM 資料，每個範例都會以16位帶正負號的值表示。 下表摘要說明 PCM 波形-音訊資料的最大值、最小值和中點值。



|             |                 |                  |                |
|-------------|-----------------|------------------|----------------|
| 資料格式 | 最大值   | 最小值    | 中點值 |
| 8位 PCM   | 255 (0xFF)       | 0                | 128 (0x80)      |
| 16位 PCM  | 32767 (0x7FFF)  | – 32768 (0x8000)  | 0              |



 

## <a name="pcm-data-packing"></a>PCM 資料封裝

資料位元組的順序會依8位和16位格式，以及 mono 與身歷聲格式而有所不同。 下列清單說明不同 PCM 波形-音訊資料格式的資料封裝。



| PCM 波形-音訊格式 | Description                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8位 mono                | 每個範例都是一個對應至單一音訊通道的1個位元組。 範例1後面接著範例2、3、4等等。                                                                                                                                                                                                                           |
| 8位身歷聲              | 每個範例都是2個位元組。 範例1後面接著範例2、3、4等等。 針對每個範例，第一個位元組是通道 0 (左聲道) ，而第二個位元組是通道1， (右通道) 。                                                                                                                                               |
| 16位 mono               | 每個範例都是2個位元組。 範例1後面接著範例2、3、4等等。 針對每個範例，第一個位元組是通道0的低序位位元組，而第二個位元組是通道0的高序位位元組。                                                                                                                                         |
| 16位身歷聲             | 每個範例都是4個位元組。 範例1後面接著範例2、3、4等等。 針對每個範例，第一個位元組是通道 0 (左通道) 的低序位位元組;第二個位元組是通道0的高序位位元組;第三個位元組是通道1的低序位位元組 (右通道) ;第四個位元組是通道1的高序位位元組。 |
| 其他                    | 每個範例都包含在多個4個位元組的區塊中，但這些樣本可能是非位元組對齊。 通道的相片順序是由遮罩指定。 如需詳細資訊，請參閱 [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)。                                                                                                 |



 

## <a name="closing-waveform-audio-output-devices"></a>關閉 Waveform-Audio 輸出裝置

波形-音訊播放完成之後，請呼叫 [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) 來關閉輸出裝置。 如果在播放波形音訊檔案時呼叫 **waveOutClose** ，關閉作業就會失敗，且函式會傳回錯誤碼，指出裝置未關閉。 如果您不想要在關閉裝置之前等候播放結束，請在關閉之前呼叫 [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) 函式。 這會結束播放，並允許關閉裝置。 在關閉裝置之前，請務必使用 [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) 函式來清除所有資料區塊的準備工作。

 

 