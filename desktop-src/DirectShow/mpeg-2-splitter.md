---
description: MPEG-2 分隔器
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: MPEG-2 分隔器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187528"
---
# <a name="mpeg-2-splitter"></a>MPEG-2 分隔器

從 Microsoft® Windows® XP 開始，MPEG 2 分隔器篩選器已被取代。 請改用 [Mpeg-2 信號](mpeg-2-demultiplexer.md) 。

在舊版平臺上，使用 MPEG-2 分隔器，以提取模式提供的 MPEG-2 程式資料流程，其中至少包含下列其中一個資料流程類型： MPEG-2 影片;MPEG-2 音訊;以 DVD video 定義的 AC3 音訊編碼;或 PCM 音訊編碼為 DVD 影片的定義。 此篩選器會剖析串流、建立每個資料流程的輸出針腳，然後將壓縮的 MPEG 音訊或影片封包輸出到 MPEG-2 的解碼器篩選器。

針對以推送模式傳遞的程式和傳輸資料流程，請在所有平臺上使用 [Mpeg-2 信號](mpeg-2-demultiplexer.md)。

> [!Note]  
> MPEG-2 分隔器不支援框架精確的搜尋。

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>篩選介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <strong>ISpecifyPropertyPages</strong>、 <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></td>
</tr>
<tr class="even">
<td>輸入 Pin 媒體類型</td>
<td><ul>
<li>MEDIATYPE_Stream，MEDIASUBTYPE_MPEG2_PROGRAM</li>
<li>MEDIATYPE_Stream，MEDIASUBTYPE_MPEG1_Video</li>
<li>MEDIATYPE_Stream，MEDIASUBTYPE_Null</li>
</ul></td>
</tr>
<tr class="odd">
<td>輸入 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>輸出 Pin 媒體類型</td>
<td>相依于資料流程類型。 請參閱 <a href="mpeg-2-splitter-media-types.md">Mpeg-2 分隔器媒體類型</a></td>
</tr>
<tr class="odd">
<td>輸出 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td>CLSID_MMSPLITTER</td>
</tr>
<tr class="odd">
<td>屬性頁 CLSID</td>
<td>不適用</td>
</tr>
<tr class="even">
<td>可執行檔</td>
<td>mpg2splt.ax</td>
</tr>
<tr class="odd">
<td><a href="merit.md">優點</a></td>
<td>MERIT_NORMAL + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">篩選準則分類</a></td>
<td>CLSID_AudioInputDeviceCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[使用 MPEG-2 分隔器](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



