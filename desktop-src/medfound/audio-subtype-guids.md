---
description: 音訊子類型 Guid
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: 音訊子類型 Guid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04192f19f530c288b9aef7b5718b8329ea108bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468652"
---
# <a name="audio-subtype-guids"></a>音訊子類型 Guid

已定義下列音訊子類型 Guid。 若要指定子類型，請在媒體類型上設定 [ [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) ] 屬性。 除非有注明，否則這些常數會定義在標頭檔 mfapi 中。

使用這些子類型時，請將 [ [MF \_ MT \_ 主要 \_ 類型](mf-mt-major-type-attribute.md) ] 屬性設定為 [ **MFMediaType \_ 音訊**]。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Description</th>
<th>格式化標記 (FOURCC) </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MEDIASUBTYPE_RAW_AAC1</strong></td>
<td>Advanced Audio 編碼 (AAC) 。<br/> 此子類型是用於包含在音訊格式標記等於0x00FF 之 AVI 檔案中的 AAC。 <br/> 如需詳細資訊，請參閱 <a href="aac-decoder.md"><strong>AAC 解碼器</strong></a>。<br/> 定義于 wmcodecdsp .h 中<br/></td>
<td>WAVE_FORMAT_RAW_AAC1 (0x00FF) </td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>Advanced Audio 編碼 (AAC) 。<br/>
<blockquote>
[!Note]<br />
相當於 MEDIASUBTYPE_MPEG_HEAAC，定義于 wmcodecdsp 中。
</blockquote>
<br/> 資料流程可以在音訊資料傳輸資料流程中包含原始的 AAC 資料或 AAC 資料 (ADTS) 串流。<br/> 如需詳細資訊，請參閱<br/>
<ul>
<li><a href="aac-decoder.md"><strong>AAC 解碼器</strong></a></li>
<li><a href="mpeg-4-file-source.md">MPEG-2 檔案來源</a></li>
</ul></td>
<td>WAVE_FORMAT_MPEG_HEAAC (0x1610) </td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_ADTS</strong></td>
<td>未使用。</td>
<td>WAVE_FORMAT_MPEG_ADTS_AAC (0x1600) </td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_ALAC</strong></td>
<td>Apple 無失真音訊編解碼器<br/> 在 Windows 10 和更新版本中支援。<br/></td>
<td>WAVE_FORMAT_ALAC (0x6C61) </td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_NB</strong></td>
<td>Adaptative 多速率音訊<br/> 在 Windows 8.1 和更新版本中支援。<br/></td>
<td>WAVE_FORMAT_AMR_NB</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AMR_WB</strong></td>
<td>Adaptative 多比率寬頻音訊<br/> 在 Windows 8.1 和更新版本中支援。<br/></td>
<td>WAVE_FORMAT_AMR_WB</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_WP</strong></td>
<td>在 Windows 8.1 和更新版本中支援。<br/></td>
<td>WAVE_FORMAT_AMR_WP</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_AC3</strong></td>
<td>杜比數位 (AC-3) 。<br/> 與 <strong>MEDIASUBTYPE_DOLBY_AC3</strong>相同的 GUID 值，其定義于 ksuuids 中。<br/></td>
<td>無。</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></td>
<td>透過索尼/Philips 數位介面 (S/PDIF) 的杜比 AC-3 音訊。<br/> 這個 GUID 值與下列子類型相同：<br/>
<ul>
<li><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>，定義于 ksmedia 中。</li>
<li><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>，定義于 uuid. h 中。</li>
</ul></td>
<td>WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092) </td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_DDPlus</strong></td>
<td>杜比數位 Plus。<br/> 與 <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>相同的 GUID 值，其定義于 wmcodecdsp 中。<br/></td>
<td>無</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_DRM</strong></td>
<td>搭配安全音訊路徑使用的加密音訊資料。</td>
<td>WAVE_FORMAT_DRM (0x0009) </td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_DTS</strong></td>
<td>數位劇院系統 (DTS) 音訊。</td>
<td>WAVE_FORMAT_DTS (0x0008) </td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_FLAC</strong></td>
<td>免費的無失真音訊編解碼器<br/> 在 Windows 10 和更新版本中支援。<br/></td>
<td>WAVE_FORMAT_FLAC (0xF1AC) </td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Float</strong></td>
<td>未壓縮的 IEEE 浮點音訊。</td>
<td>WAVE_FORMAT_IEEE_FLOAT (0x0003) </td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Float_SpatialObjects</strong></td>
<td>未壓縮的 IEEE 浮點音訊。</td>
<td>無</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MP3</strong></td>
<td>MPEG 音訊第3層 (MP3) 。</td>
<td>WAVE_FORMAT_MPEGLAYER3 (0x0055) </td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_MPEG</strong></td>
<td>MPEG-2 音訊承載。</td>
<td>WAVE_FORMAT_MPEG (0x0050) </td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MSP1</strong></td>
<td>Windows Media 音訊9語音編解碼器。</td>
<td>WAVE_FORMAT_WMAVOICE9 (0x000A) </td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Opus</strong></td>
<td>Opus<br/> 在 Windows 10 和更新版本中支援。<br/></td>
<td>WAVE_FORMAT_OPUS (0x704F) </td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>未壓縮的 PCM 音訊。</td>
<td>WAVE_FORMAT_PCM (1) </td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_QCELP</strong></td>
<td>QCELP (的 Qualcomm 程式碼興奮線性預測) 音訊。</td>
<td>無</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMASPDIF</strong></td>
<td>S/PDIF Windows Media 音訊 9 Professional 編解碼器。</td>
<td>WAVE_FORMAT_WMASPDIF (0x0164) </td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudio_Lossless</strong></td>
<td>Windows Media 音訊9無失真編解碼器或 Windows Media 音訊9.1 編解碼器。</td>
<td>WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163) </td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMAudioV8</strong></td>
<td>Windows Media 音訊8編解碼器、Windows Media 音訊9編解碼器或 Windows Media 音訊9.1 編解碼器。</td>
<td>WAVE_FORMAT_WMAUDIO2 (0x0161) </td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudioV9</strong></td>
<td>Windows Media 音訊 9 Professional 編解碼器或 Windows Media 音訊 9.1 Professional 編解碼器。</td>
<td>WAVE_FORMAT_WMAUDIO3 (0x0162) </td>
</tr>
</tbody>
</table>



 

此資料表的第三個數據行中所列的格式標記會在 **WAVEFORMATEX** 結構中使用，並定義于標頭檔 mmreg 中。

指定音訊格式標記時，您可以建立音訊子類型 GUID，如下所示：

1.  從值 **MFAudioFormat \_ Base** 開始，此值定義于 mfaph 中。
2.  以格式標記取代這個 GUID 的第一個 **DWORD** 。

您可以使用 [**定義 \_ 媒體 \_ guid**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) 宏來定義遵循此模式的新 GUID 常數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊媒體類型](audio-media-types.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型 Guid](media-type-guids.md)
</dt> <dt>

[媒體類型](media-types.md)
</dt> </dl>

 

 




