---
description: MPEG-2 影片解碼篩選器
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: MPEG-2 影片解碼篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7f48e441226dee33ef949219e8008e15c9d711
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973128"
---
# <a name="mpeg-1-video-decoder-filter"></a>MPEG-2 影片解碼篩選器

解碼 MPEG 1 影片。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>篩選介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>輸入 Pin 媒體類型</td>
<td>MEDIATYPE_Video，FORMAT_MPEGVideo<br/> 下列子類型有效：<br/>
<ul>
<li><strong>MEDIASUBTYPE_MPEG1Packet</strong></li>
<li><strong>MEDIASUBTYPE_MPEG1Payload</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>輸入 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"> <strong>IMemInputPin</strong></a></td>
</tr>
<tr class="even">
<td>輸出 Pin 媒體類型</td>
<td>主要類型： <strong>MEDIATYPE_Video</strong>、<br/> 格式類型： <strong>FORMAT_VideoInfo</strong> 或 <strong>FORMAT_VideoInfo2</strong><br/> 亞：<br/>
<ul>
<li><strong>MEDIASUBTYPE_RGB24</strong></li>
<li><strong>MEDIASUBTYPE_RGB32</strong></li>
<li><strong>MEDIASUBTYPE_RGB8</strong></li>
<li><strong>MEDIASUBTYPE_RGB555</strong></li>
<li><strong>MEDIASUBTYPE_RGB565</strong></li>
<li><strong>MEDIASUBTYPE_UYVY</strong></li>
<li><strong>MEDIASUBTYPE_Y41P</strong></li>
<li><strong>MEDIASUBTYPE_YUY2</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>輸出 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td><strong>CLSID_CMpegVideoCodec</strong></td>
</tr>
<tr class="odd">
<td>屬性頁 CLSID</td>
<td><strong>CLSID_MpegVideoDecodePropertyPage</strong></td>
</tr>
<tr class="even">
<td>可執行檔</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">優點</a></td>
<td>0x40000001</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">篩選準則分類</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

此篩選器可以解碼成 DirectDraw 表面。 如果電腦支援 MMX，則篩選器會使用 MMX。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 




