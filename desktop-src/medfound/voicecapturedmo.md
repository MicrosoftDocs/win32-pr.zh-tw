---
description: 封裝與語音捕捉相關之多個 Dsp 的物件。
ms.assetid: 6c77c8f6-289e-4130-b56a-e1f0bcc40f3e
title: '語音捕捉 DSP (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48c3b3194873008f45ef80ef3a21dad416158b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692291"
---
# <a name="voice-capture-dsp"></a>語音捕獲 DSP

封裝與語音捕捉相關之多個 Dsp 的物件。

## <a name="clsid"></a>CLSID

CLSID \_ CWMAudioAEC

## <a name="interfaces"></a>介面

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   **IPropertyStore**

## <a name="properties"></a>屬性



| 屬性                                                                                     | 描述                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [MFPKEY \_ WMAAECMA \_ 裝置 \_ 索引](mfpkey-wmaaecma-device-indexesproperty.md)              | 指定用來捕捉和轉譯音訊的 SQL-DMO 音訊裝置。                     |
| [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md)            | 識別應用程式目前使用的音訊裝置組合。              |
| [MFPKEY \_ WMAAECMA \_ SQL-DMO \_ 來源 \_ 模式](mfpkey-wmaaecma-dmo-source-modeproperty.md)           | 指定是使用來源模式或篩選模式。                                        |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)                        | 指定當您在剩餘的信號上 (AES) 執行聲場 echo 抑制的次數。 |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)                        | 指定，是否執行自動增益控制項。                                        |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ 中心 \_ 剪輯](mfpkey-wmaaecma-featr-center-clipproperty.md)       | 指定，是否執行中心裁剪。                                               |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ ECHO \_ LENGTH](mfpkey-wmaaecma-featr-echo-lengthproperty.md)       | 指定聲場 echo 取消 (AEC) 演算法可以處理的回應持續時間。    |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ 畫面格 \_ 大小](mfpkey-wmaaecma-featr-frame-sizeproperty.md)         | 指定音訊框架大小。                                                                   |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ 橫樑](mfpkey-wmaaecma-featr-micarr-beamproperty.md)       | 指定用來處理麥克風陣列的橫樑。                                |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ 模式](mfpkey-wmaaecma-featr-micarr-modeproperty.md)       | 指定 SQL-DMO 執行麥克風陣列處理的方式。                                       |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ PREPROC](mfpkey-wmaaecma-featr-micarr-preprocproperty.md) | 指定，是否執行麥克風陣列前置處理。                                |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ 雜訊 \_ 填滿](mfpkey-wmaaecma-featr-noise-fillproperty.md)         | 指定，是否執行雜訊填滿。                                                 |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ NS](mfpkey-wmaaecma-featr-nsproperty.md)                          | 指定是否執行雜訊隱藏。                                             |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)                        | 指定由的語音活動偵測類型。                             |
| [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md)                  | 讓應用程式覆寫各種屬性的預設設定。                   |
| [MFPKEY \_ WMAAECMA \_ MIC \_ 增益 \_ BOUNDER](mfpkey-wmaaecma-mic-gain-bounderproperty.md)         | 指定是否套用麥克風增益周框。                                       |
| [MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR](mfpkey-wmaaecma-micarray-descptrproperty.md)          | 指定麥克風陣列幾何。                                                          |
| [MFPKEY \_ WMAAECMA \_ 品質 \_ 計量](mfpkey-wmaaecma-quality-metricsproperty.md)            | 取得 AEC 的品質計量。                                                                |
| [MFPKEY \_ WMAAECMA \_ 取得 \_ TS \_ 統計資料](mfpkey-wmaaecma-retrieve-ts-statsproperty.md)       | 指定是否將時間戳記統計資料儲存在登錄中。                           |
| [MFPKEY \_ WMAAECMA \_ 系統 \_ 模式](mfpkey-wmaaecma-system-modeproperty.md)                    | 設定處理模式。                                                                         |



 

## <a name="remarks"></a>備註

與其他 Dsp 不同的是，語音捕捉物件會將多個 Dsp 封裝在單一物件中，而物件只是一種物件， (不會執行 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)) 。 語音捕獲中包含下列 DSP 元件：

-   聲場 echo 取消 (AEC) 
-   麥克風陣列處理
-   雜訊隱藏
-   自動增益控制
-   語音活動偵測

應用程式可以個別開啟和關閉每個元件。

語音捕獲（voice capture）支援兩種作業模式： *篩選* 模式和 *來源* 模式。 在篩選模式中，應用程式會從麥克風和說話者將音訊樣本傳送至，並產生輸出。

在來源模式中，應用程式不需要將範例傳遞給 SQL-DMO。 取而代之的是，一來管理音訊裝置上的所有作業，包括初始化裝置、捕獲和同步處理音訊串流、計算時間戳記，以及取得麥克風陣列的幾何。 使用來源模式時，應用程式只會設定 SQL-DMO，而來自的輸出是乾淨且經過處理的麥克風信號。 來源模式比篩選模式更容易使用，而且建議用於大部分的應用程式。

目前，語音捕獲僅支援單聲道的聲場 echo 取消 (AEC) ，因此喇叭線的輸出必須是單一通道。 如果已停用麥克風陣列處理，多重通道輸入會折迭至一個通道以進行 AEC 處理。 如果麥克風陣列處理和 AEC 處理都已啟用，則會在麥克風陣列處理之前，在每個麥克風元素上執行 AEC。

### <a name="microphone-array-processing"></a>麥克風陣列處理

麥克風陣列是一組緊密定位的麥克風。 麥克風陣列的方向比單一麥克風更好，因為聲場會以稍微不同的時間抵達每個麥克風。 如需麥克風陣列的詳細資訊，請參閱 [Windows vista 中的 web 文章麥克風陣列支援](/windows-hardware/design/component-guidelines/audio) ，以及 [如何建立和使用適用于 Windows vista 的麥克風](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format)陣列。

### <a name="using-the-voice-capture-dsp"></a>使用語音捕獲 DSP

若要使用語音捕獲 DSP，請執行下列步驟。

### <a name="1-initialize-the-dmo"></a>1. 初始化 SQL-DMO

使用 CLSID **clsid \_ CWMAudioAEC** 呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立語音捕獲。 語音捕獲 DSDP 只會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 和 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面，因此只能用來做為。

的預設值為來源模式。 若要選取篩選模式，請將 [MFPKEY \_ WMAAECMA \_ sql-dmo \_ 來源 \_ 模式](mfpkey-wmaaecma-dmo-source-modeproperty.md) 屬性設定為 **VARIANT \_ FALSE**。

接下來，使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面設定 sql-dmo 的內部屬性。 應用程式必須設定的唯一屬性是 [ [MFPKEY \_ WMAAECMA \_ 系統 \_ 模式]](mfpkey-wmaaecma-system-modeproperty.md) 屬性。 這個屬性會設定在中的處理管線。 其他屬性是選擇性的。

### <a name="2-set-the-input-and-output-formats"></a>2. 設定輸入和輸出格式

如果您在篩選模式中使用 SQL-DMO，請呼叫 [**IMediaObject：： SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype)來設定輸入格式。 輸入格式幾乎可以是任何有效的未壓縮 PCM 或 IEEE 浮點音訊類型。 如果輸入格式不符合輸出格式，則會自動執行取樣速率轉換。

如果您在來源模式中使用的是，請勿設定輸入格式。 SQL-DMO 會根據音訊裝置自動設定輸入格式。

在任一種模式中，藉由呼叫 [**IMediaObject：： SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype)來設定輸出格式。 SQL-DMO 可以接受下列輸出格式：

-   子類型： **MEDIASUBTYPE \_ PCM** 或 **MEDIASUBTYPE \_ IEEE \_ FLOAT**
-   格式區塊： [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) 或 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))
-   每秒樣本數： 8000;11025;16000;或22050
-   通道：1表示僅限 AEC 模式，2或4表示麥克風陣列處理
-   每個樣本位數：16

下列程式碼會將輸出型別設定為16位單一通道 PCM 音訊：


```
DMO_MEDIA_TYPE mt;  // Media type.
mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.lSampleSize = 0;
mt.bFixedSizeSamples = TRUE;
mt.bTemporalCompression = FALSE;
mt.formattype = FORMAT_WaveFormatEx;

// Allocate the format block to hold the WAVEFORMATEX structure.
hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    WAVEFORMATEX *pwav = (WAVEFORMATEX*)mt.pbFormat;
    pwav->wFormatTag = WAVE_FORMAT_PCM;
    pwav->nChannels = 1;
    pwav->nSamplesPerSec = 16000;
    pwav->nAvgBytesPerSec = 32000;
    pwav->nBlockAlign = 2;
    pwav->wBitsPerSample = 16;
    pwav->cbSize = 0;

    // Set the output type.
    if (SUCCEEDED(hr))
    {
        hr = pDMO->SetOutputType(0, &mt, 0); 
    }
    // Free the format block.
    MoFreeMediaType(&mt);
}
```



### <a name="3-process-data"></a>3. 處理資料

在處理任何資料之前，建議您呼叫 [**IMediaObject：： AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources)。 這個方法會配置用來在內部使用的資源。 在先前所列的步驟之後（而非之前）呼叫 **AllocateStreamingResources** 。 如果您沒有呼叫這個方法，則會在資料處理開始時自動設定資源。

如果您在篩選模式中使用 SQL-DMO，則必須呼叫 [**IMediaObject：:P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput)，將輸入資料傳遞給： 來自麥克風的音訊資料會進入串流0，而喇叭線的音訊資料則會移至串流1。 如果您在來源模式中使用的是，就不需要呼叫 **ProcessInput**。

若要從 DSP 取得輸出資料，請執行下列步驟：

1.  建立緩衝區物件以保存輸出資料。 緩衝區物件必須執行 [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) 介面。 緩衝區的大小取決於您的應用程式需求。 配置較大的緩衝區可減少發生問題的機會。
2.  宣告 [**Sql-dmo \_ 輸出 \_ 資料 \_ 緩衝區**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) 結構，並設定 **pBuffer** 成員以指向您的緩衝區物件。
3.  將 [**Sql-dmo \_ 輸出 \_ 資料 \_ 緩衝區**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) 結構傳遞至 [**IMediaObject：:P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) 方法。
4.  只要每個值都有輸出資料，繼續呼叫這個方法。 DSP 會在 [**Sql-dmo \_ 輸出 \_ 資料 \_ 緩衝區**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer)結構的 **dwStatus** 成員中設定 [ **sql-dmo \_ 輸出 \_ 資料 \_ BUFFERF \_ 未完成**] 旗標，以表示它有更多輸出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfwmaaec.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數位訊號處理器](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
