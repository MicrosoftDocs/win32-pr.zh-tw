---
description: AVI 繪製篩選
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: AVI 繪製篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6d6b318b7a1f7e762fc0806186114fb9256f5c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108621"
---
# <a name="avi-draw-filter"></a>AVI 繪製篩選

當影片輸出到外部 NTSC 電視監視器時，會自動將 AVI 繪圖篩選器提取到播放圖形，而不是 [Avi 解壓縮](avi-decompressor-filter.md) 程式。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>篩選介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>輸入 Pin 媒體類型</td>
<td>主要類型： MEDIATYPE_VideoSubtypes：<br/>
<ul>
<li>MEDIASUBTYPE_MJPG</li>
<li>MEDIASUBTYPE_TVMJ</li>
<li>MEDIASUBTYPE_WAKE</li>
<li>MEDIASUBTYPE_CFCC</li>
<li>MEDIASUBTYPE_IJPG</li>
<li>MEDIASUBTYPE_Plum</li>
<li>MEDIASUBTYPE_DVCS</li>
<li>MEDIASUBTYPE_DVSD</li>
<li>MEDIASUBTYPE_MDVF</li>
<li>格式類型： FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>輸入 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>輸出 Pin 媒體類型</td>
<td>MEDIATYPE_Video，MEDIASUBTYPE_Null</td>
</tr>
<tr class="odd">
<td>輸出 Pin 介面</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td>CLSID_AVIDraw</td>
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
<td>MERIT_NORMAL + 100</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">篩選準則分類</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

由於 AVI Draw 篩選和 [VFW Capture 篩選器](vfw-capture-filter.md) 都連接到相同的硬體，因此它們不能在相同的篩選圖形中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 




