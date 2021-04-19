---
description: 音訊 Resampler 會在音訊串流上執行下列一或兩個動作。變更取樣率。變更通道數目。
ms.assetid: bee755c4-0585-40fb-aa4d-4e964f5144a3
title: 音訊 Resampler DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb173fa4f8d964bec1102c4cfeefa4bf83f1ffe
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106981760"
---
# <a name="audio-resampler-dsp"></a>音訊 Resampler DSP

音訊 Resampler 會在音訊串流上執行下列一或兩個動作。

-   變更取樣率。
-   變更通道數目。

## <a name="clsid"></a>CLSID

CLSID \_ CResamplerMediaObject

## <a name="interfaces"></a>介面

-   [**IMediaObject**](/previous-versions/ms785953(v=vs.85))
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResamplerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops)

## <a name="formats"></a>格式

PCM 或 IEEE 浮點數

媒體類型必須指定未壓縮的 PCM 或浮點音訊格式。

-   針對 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，請依照 [未壓縮的音訊媒體類型](uncompressed-audio-media-types.md)中所述，將媒體類型初始化。
-   針對 [**IMediaObject**](/previous-versions/ms785953%28v%3dvs.85%29) 介面，媒體類型必須是 **\_ WaveFormatEx 類型格式** 。 如需詳細資訊，請參閱 [**Sql-dmo \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)。

## <a name="properties"></a>屬性

-   [MFPKEY \_ WMRESAMP \_ FILTERQUALITY](mfpkey-wmresamp-filterquality.md)
-   [MFPKEY \_ WMRESAMP \_ CHANNELMTX](mfpkey-wmresamp-channelmtx.md)
-   [MFPKEY \_ WMRESAMP \_ 低通 \_ 頻寬](mfpkey-wmresamp-lowpass-bandwidth.md)

## <a name="required-attributes"></a>必要的屬性

Resampler 需要設定下列屬性：

-   [MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩](mf-mt-audio-channel-mask-attribute.md)
-   [\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊](mf-mt-audio-block-alignment-attribute.md)

## <a name="custom-channel-mapping"></a>自訂通道對應

音訊 resampler 會根據下列資訊，將輸入音訊通道對應到輸出音訊頻道：

-   頻道的數目。 這是在媒體類型的 [MF \_ MT \_ 音訊 \_ NUM \_](mf-mt-audio-num-channels-attribute.md) Channel 屬性中提供，或 [WAVEFORMATEX](mf-mt-audio-prefer-waveformatex-attribute.md)結構的 **nChannels** 成員提供。
-   通道遮罩，可將通道指派給喇叭位置。 通道遮罩是在媒體類型的 MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩屬性中提供，或 [**WAVEFORMATEXTENSIBLE**](/windows/desktop/api/mmreg/ns-mmreg-waveformatextensible)結構的 **dwChannelMask** 成員提供。
-   對應加權的矩陣。

矩陣包含一系列加權，因此每個輸出通道都是輸入通道的加權平均值。

您可以藉由呼叫 [**IWMResamplerProps：： SetUserChannelMtx**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-setuserchannelmtx) 或設定 [**MFPKEY \_ WMRESAMP \_ CHANNELMTX**](mfpkey-wmresamp-channelmtx.md) 屬性，來指定通道對應的自訂矩陣。 如果未提供自訂矩陣，音訊 Resampler 會使用一組預設矩陣。

## <a name="default-channel-mapping"></a>預設通道對應

如果您未指定自訂矩陣，音訊 Resampler DSP 會使用通道對應的預設值。

在接下來的表格中，會將通道縮寫：

-   L：左方
-   R： Right
-   C： Center
-   LFE：低 Frequence 效果
-   BL： Back 左方
-   BR：向右
-   SL：左方環繞
-   SR：圍住範圍右邊

下表顯示對應6個通道的預設係數 (mask 0x3F) 為2個通道。



|     | L     | R     | C     | LFE   | BL    | BR    |
|-----|-------|-------|-------|-------|-------|-------|
| L   | 0.314 | 0     | 0.222 | 0.031 | 0.268 | 0.164 |
| R   | 0     | 0.314 | 0.222 | 0.031 | 0.164 | 0.268 |



 

下表顯示對應6個通道的預設係數 (mask 0x60F) 為2個通道。



|     | L     | R     | C     | LFE   | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|
| L   | 0.320 | 0     | 0.226 | 0.032 | 0.292 | 0.130 |
| R   | 0     | 0.320 | 0.226 | 0.032 | 0.130 | 0.292 |



 

下表顯示對應 6 (mask 0x3F 或 0x60F) 通道到1個通道的預設係數。



|     | L     | R     | C     | LFE   | BL (SL)  | BR (SR)  |
|-----|-------|-------|-------|-------|--------|--------|
| C   | 0.192 | 0.192 | 0.192 | 0.038 | 0.192  | 0.192  |



 

下表顯示對應8個通道的預設係數 (mask 0x63F) 為2個通道。



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0.222 | 0     | 0.157 | 0.022 | 0.189 | 0.116 | 0.203 | 0.090 |
| R   | 0     | 0.222 | 0.157 | 0.022 | 0.116 | 0.189 | 0.090 | 0.203 |



 

下表顯示對應8個通道 (mask 0x63F) 為1個通道的預設係數。



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| C   | 0.139 | 0.139 | 0.139 | 0.028 | 0.139 | 0.139 | 0.139 | 0.139 |



 

下表顯示對應8個通道的預設係數 (mask 0x63F) 為6個通道 (mask 0x3F) 。



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0.518 | 0     | 0     | 0     | 0     | 0     | 0.189 | 0     |
| R   | 0     | 0.518 | 0     | 0     | 0     | 0     | 0     | 0.189 |
| C   | 0     | 0     | 0.518 | 0     | 0     | 0     | 0     | 0     |
| LFE | 0     | 0     | 0     | 0.518 | 0     | 0     | 0     | 0     |
| BL  | 0     | 0     | 0     | 0     | 0.518 | 0     | 0.482 | 0     |
| BR  | 0     | 0     | 0     | 0     | 0     | 0.518 | 0     | 0.482 |



 

下表顯示對應8個通道的預設係數 (mask 0x63F) 為6個通道 (mask 0x60F) 。



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0.447 | 0     | 0     | 0     | 0     | 0     | 0     | 0     |
| R   | 0     | 0.447 | 0     | 0     | 0     | 0     | 0     | 0     |
| C   | 0     | 0     | 0.447 | 0     | 0     | 0     | 0     | 0     |
| LFE | 0     | 0     | 0     | 0.447 | 0     | 0     | 0     | 0     |
| SL  | 0     | 0     | 0     | 0     | 0.429 | 0.124 | 0.447 | 0     |
| SR  | 0     | 0     | 0     | 0     | 0.124 | 0.429 | 0     | 0.447 |



 

若要瞭解如何解讀係數的資料表，請考慮將6個通道對應到2的第一個資料表。 資料表的第一個資料列 (0.314、0、0.222、0.031、0.268、0.164) 是加權的向量，可指定每個輸入通道占輸出左邊通道的程度。 資料表的第二個數據列 (0、0.314、0.222、0.031、0.164、0.268) 是加權的向量，可指定每個輸入通道對輸出的右聲道有多高的程度。

下列公式顯示輸出通道的計算方式。

``` syntax
L_out = L*0.314 + C*0.222 + LFE*0.031 + BL*0.268 + BR*0.164 
R_out = R*0.314 + C*0.222 + LFE*0.031 + BL*0.164 + BR*0.268
```

> [!Note]  
> 如果您使用音訊 Resampler DSP 來增加通道數目，新增的通道將會指派0值。

 

## <a name="output-quality"></a>輸出品質

您可以藉由呼叫 [**IWMResamplerProps：： SetHalfFilterLength**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-sethalffilterlength) 或設定 [**MFPKEY \_ WMRESAMP \_ FILTERQUALITY**](mfpkey-wmresamp-filterquality.md) 屬性，來指定音訊 Resampler DSP 的輸出品質。 如果您未指定輸出品質，音訊 Resampler DSP 會使用預設品質值30。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Resampledmo.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

[數位訊號處理器](windowsmediadigitalsignalprocessors.md)
