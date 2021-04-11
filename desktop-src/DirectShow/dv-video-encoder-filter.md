---
description: DV 影片編碼器篩選器
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: DV 影片編碼器篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b91da15fda0597e9b943c78fd5a6716021a3ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935670"
---
# <a name="dv-video-encoder-filter"></a>DV 影片編碼器篩選器

此篩選會將未壓縮的影片串流編碼為數位視訊 (DV) 。 它會提供自訂介面 [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)，以設定編碼解析度和格式。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>篩選介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>、 <strong>IPersistStream</strong>、 <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>輸入 Pin 媒體類型</td>
<td><ul>
<li>主要類型： MEDIATYPE_VideoThe 下列子類型有效：<br/>
<ul>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB555</li>
</ul></li>
<li>格式類型： FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>輸入 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>輸出 Pin 媒體類型</td>
<td><ul>
<li>主要類型： MEDIATYPE_Video</li>
<li>子類型： MEDIASUBTYPE_dvsd</li>
<li>格式類型： FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>輸出 Pin 介面</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td>CLSID_DVVideoEnc</td>
</tr>
<tr class="odd">
<td>屬性頁 CLSID</td>
<td>CLSID_DVEncPropertiesPage</td>
</tr>
<tr class="even">
<td>可執行檔</td>
<td>qdv.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">優點</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">篩選準則分類</a></td>
<td>CLSID_VideoCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

若為16位的影片 (MEDIASUBTYPE \_ RGB555 或 MEDIASUBTYPE \_ RGB565) ，則輸入必須為 720 x 480 圖元（NTSC）或 720 x 576 圖元（代表 PAL）。 若是24位的影片，輸入上沒有大小限制。

適用于 NTSC 的輸出一律是 720 x 480，或適用于 PAL 的 720 x 576;24位影片會調整成符合這些尺寸。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> </dl>

 

 




