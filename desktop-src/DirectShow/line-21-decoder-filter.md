---
description: 第21行解碼篩選
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: 第21行解碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970876"
---
# <a name="line-21-decoder-filter"></a>第21行解碼篩選

此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

這一行21的解碼篩選器會解碼第21行的資料，並將標題文字繪製到點陣圖上。

輸入 pin 會連接到任何第21行的資料提供者，通常是 DVD video 解碼器或 [CC 解碼器](cc-decoder-filter.md) 篩選器。 CC 解碼器提供類比電視信號 VBI 的第21行資料。 輸出圖釘會連接到重迭 [混音](overlay-mixer-filter.md) 器上的次要 pin 或其他影片轉譯器，例如 VMR。

此篩選器會接受標準位元組配對格式的第21行資料，或以 DVD 作為整個圖片群組 (GOP) 的封包。 針對 DVD video 串流中的每個 GOP，可能會有使用者資料封包，其中包含該特定 GOP 的標頭資訊和第21行資料。 位元組組的格式定義于 EIA/CEA-608-B 標準中;如需詳細資訊，請參閱該標準。

此篩選器有兩個版本可供使用：



| 篩選            | CLSID                 |
|-------------------|-----------------------|
| 第21行的解碼器   | CLSID \_ Line21Decoder  |
| 第21行的解碼器2 | CLSID \_ Line21Decoder2 |



 

第1版的篩選器是在 Microsoft® Windows® 95/98/Me 和 Windows 2000 平臺上使用。 第2版的篩選器可在 Microsoft Windows XP 和更新版本中使用，並會在影片混合轉譯器位於圖形中時使用。

下表中的資訊適用于這兩個版本的篩選：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>篩選介面</td>
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>輸入 Pin 媒體類型</td>
<td>主要類型： MEDIATYPE_AUXLine21DataSubtype：<br/>
<ul>
<li>MEDIASUBTYPE_Line21_BytePair (標準行 21) </li>
<li>MEDIASUBTYPE_Line21_GOPPacket (DVD 行 21) </li>
</ul>
格式類型： FORMAT_VideoInfo 或 GUID_Null<br/></td>
</tr>
<tr class="odd">
<td>輸入 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>輸出 Pin 媒體類型</td>
<td>主要類型： MEDIATYPE_VideoSubtype：<br/>
<ul>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
</ul>
格式類型： FORMAT_VideoInfo<br/></td>
</tr>
<tr class="odd">
<td>輸出 Pin 介面</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td>請參閱上表</td>
</tr>
<tr class="odd">
<td>屬性頁 CLSID</td>
<td>無</td>
</tr>
<tr class="even">
<td>可執行檔</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">優點</a></td>
<td>第21行： MERIT_NORMALLine 21 的解碼器2： MERIT_NORMAL + 2<br/></td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">篩選準則分類</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[隱藏式輔助字幕和 Teletext](closed-captions-and-teletext.md)
</dt> <dt>

[DVD 篩選圖形設定](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




