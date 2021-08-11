---
description: MP3 檔案來源會剖析 MP3 檔案。
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: MP3 檔案來源
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b5649f1bdbc9d9b3dfa0af2f04878dfa64852af85ff8e829d4d2d4c4d20d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240103"
---
# <a name="mp3-file-source"></a>MP3 檔案來源

MP3 檔案來源會剖析 MP3 檔案。

MP3 檔案來源會輸出包含 MPEG-2 音訊框架的緩衝區。 它不會解碼音訊。

## <a name="file-extensions-and-mime-types"></a>副檔名和 MIME 類型

MP3 檔案來源是下列副檔名的預設媒體來源：

-   .mp3

它也是下列 MIME 類型的預設媒體來源。

-   音訊/mpeg
-   音訊/x-mp3
-   音訊/x-mpeg

## <a name="media-types"></a>媒體類型

MP3 檔案來源所提供的媒體類型包含下列屬性。



| 屬性                                                                                    | 描述                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md)                                    | 等於 **MFMediaType \_ 音訊**。                                                                                                                   |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)                                           | 等於 **MFAudioFormat \_ MP3** 或 **MFAudioFormat \_ MPEG**。                                                                                        |
| [**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 每秒的平均位元組數。                                                                                                                |
| [**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**](mf-mt-audio-block-alignment-attribute.md)             | 等於1。                                                                                                                                        |
| [**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**](mf-mt-audio-num-channels-attribute.md)                   | 音訊聲道數目。                                                                                                                          |
| [**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**](mf-mt-audio-samples-per-second-attribute.md)      | 每秒音訊樣本數。                                                                                                                |
| [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md)                                      | 包含在結構的 **wfx** 成員後面出現的 [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat)結構部分。 |



 

## <a name="interfaces"></a>介面

MP3 檔案來源會透過 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))公開下列介面：

-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

此外，它會透過 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)公開下列介面：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>服務 GUID</th>
<th>介面</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MF_METADATA_PROVIDER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_PROPERTY_HANDLER_SERVICE</strong></td>
<td><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
<blockquote>
[!Note]<br />
請參閱 <a href="shell-metadata-providers.md">Shell 中繼資料提供者</a>。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></td>
</tr>
<tr class="even">
<td><strong>MF_RATE_CONTROL_SERVICE</strong></td>
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                           |
| DLL<br/>                      | <dl> <dt>Mf.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體來源和接收](media-sources-and-sinks.md)
</dt> <dt>

[媒體來源](media-sources.md)
</dt> <dt>

[來源解析程式](source-resolver.md)
</dt> <dt>

[媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
