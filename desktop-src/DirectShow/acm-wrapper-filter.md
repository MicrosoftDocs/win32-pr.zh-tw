---
description: 條件式包裝函式篩選
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: 條件式包裝函式篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6aaa56d955fe9cf1966e17c657fbf741b4bb8694a7f18b501b148b0383ea19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664077"
---
# <a name="acm-wrapper-filter"></a>條件式包裝函式篩選

「通過包裝函式」篩選器可讓音訊壓縮管理員 (的) 編解碼器來聯結篩選圖形。 它可做為解壓縮篩選器或壓縮篩選器。

在解壓縮篩選器中，[LegacyAmFilterCategory 篩選] 類別目錄 DirectShow 中會出現 [篩選] 類別， (CLSID \_) 並具有正常的業績 \_ 。 輸入 pin 的連接媒體類型會決定篩選器所使用的編解碼器。 一般而言，應用程式不需要將篩選準則加入至篩選圖形;當需要時，篩選 Graph 管理員會自動將它提取。 解壓縮只適用于 PCM 音訊。

若為壓縮篩選，則會在 [音訊壓縮機] 類別中顯示「」類別 (CLSID \_ AudioCompressorCategory) ，並有 \_ 「 \_ 未使用」的優點 \_ 。 每個編解碼器都會顯示為個別的實例。 針對壓縮，您無法直接使用 CoCreateInstance 建立篩選器。 相反地，您必須使用系統裝置枚舉器。 如需詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>篩選介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、IPersist、IPersistPropertyBag</td>
</tr>
<tr class="even">
<td>輸入 pin 媒體類型</td>
<td>MEDIATYPE_Audio、MEDIASUBTYPE_Null FORMAT_WaveFormatEx</td>
</tr>
<tr class="odd">
<td>輸入 pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>輸出 pin 媒體類型</td>
<td>MEDIATYPE_Audio、MEDIASUBTYPE_PCM FORMAT_WaveFormatEx。可能的任何組合如下：<br/>
<ul>
<li>每秒樣本數 (kHz) ：44.1、22.05、11.025 或8.0。</li>
<li>通道：身歷聲或 mono。</li>
<li>每個樣本的位數：8或16。</li>
</ul></td>
</tr>
<tr class="odd">
<td>輸出 pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td>CLSID_ACMWrapper</td>
</tr>
<tr class="odd">
<td>屬性頁 CLSID</td>
<td>沒有屬性頁。</td>
</tr>
<tr class="even">
<td>可執行檔</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">優點</a></td>
<td>MERIT_NORMAL 或 MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">篩選準則分類</a></td>
<td>CLSID_LegacyAmFilterCategory 或 CLSID_AudioCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 




