---
description: WAVE 剖析器篩選
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: WAVE 剖析器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb30465a25ab3a6eef190b5fbecd4a4878c2744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986405"
---
# <a name="wave-parser-filter"></a>WAVE 剖析器篩選

WAVE 剖析器篩選器會剖析 wav、澳大利亞或. aif 檔案中的 WAV 格式音訊資料。 上游篩選必須是非同步檔案 [來源](file-source--async--filter.md) 篩選、URL 檔案 [來源](file-source--url--filter.md) 篩選，或包含 WAV 音訊資料的相容協力廠商非同步來源篩選。 輸出資料流程是音訊資料，您可以直接連接到音訊轉譯篩選器，也可以連接到中間的音訊轉換篩選。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>篩選介面</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></td>
</tr>
<tr class="even">
<td>輸入 Pin 媒體類型</td>
<td>主要類型： MEDIATYPE_StreamThe 下列子類型有效：<br/>
<ul>
<li>MEDIASUBTYPE_AIFF</li>
<li>MEDIASUBTYPE_AU</li>
<li>MEDIASUBTYPE_WAVE</li>
</ul></td>
</tr>
<tr class="odd">
<td>輸入 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>輸出 Pin 媒體類型</td>
<td>主要類型： MEDIATYPE_AudioSubtype： MEDIASUBTYPE_PCM 或其他壓縮類型。  (查看 <a href="audio-subtypes.md"><strong>音訊子類型</strong></a>。 ) <br/> 格式類型： FORMAT_WaveFormatEx<br/></td>
</tr>
<tr class="odd">
<td>輸出 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td>{D51BD5A1-7548-11cf-A520-0080C77EF58A}</td>
</tr>
<tr class="odd">
<td>屬性頁 CLSID</td>
<td>沒有屬性頁。</td>
</tr>
<tr class="even">
<td>可執行檔</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">優點</a></td>
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">篩選準則分類</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

此篩選器支援下列檔案類型：

-   WAVE ( .wav) 
-   .AIFF 和 .AIFF-C ( 的) 
-   AU ( 澳大利亞) 

但是，它對音訊格式有下列限制：

-   音訊必須是8位或16位的線性 PCM。
-   若為 .AIFF-C 檔案，必須將音訊解壓縮，以位元組由大到小的位元組順序 (壓縮類型 ' NONE ' ) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 




