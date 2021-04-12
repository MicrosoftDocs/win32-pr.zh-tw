---
description: MPEG-2 資料流程分隔器篩選
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: MPEG-2 資料流程分隔器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109648"
---
# <a name="mpeg-1-stream-splitter-filter"></a>MPEG-2 資料流程分隔器篩選

此篩選器會將 MPEG-2 系統資料流程分割成其元件音訊和影片串流。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>篩選介面</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>輸入 Pin 媒體類型</td>
<td>主要類型： MEDIATYPE_Stream<br/> 亞：<br/>
<ul>
<li>MEDIASUBTYPE_MPEG1System</li>
<li>MEDIASUBTYPE_MPEG1VideoCD</li>
<li>MEDIASUBTYPE_Audio</li>
<li>MEDIASUBTYPE_Video</li>
</ul>
請參閱<a href="mpeg-1-media-types.md"> <strong>Mpeg-2 媒體類型</strong></a><br/></td>
</tr>
<tr class="odd">
<td>輸入 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>輸出 Pin 媒體類型</td>
<td>主要類型： MEDIATYPE_Audio 或 MEDIATYPE_Video<br/> 子類型： MEDIASUBTYPE_MPEG1Payload 或 MEDIASUBTYPE_MPEG1Packet<br/> 請參閱<a href="mpeg-1-media-types.md"> <strong>Mpeg-2 媒體類型</strong></a><br/></td>
</tr>
<tr class="odd">
<td>輸出 Pin 介面</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>篩選 CLSID</td>
<td>CLSID_MPEG1Splitter</td>
</tr>
<tr class="odd">
<td>屬性頁 CLSID</td>
<td>沒有屬性頁</td>
</tr>
<tr class="even">
<td>可執行檔</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">優點</a></td>
<td>MERIT_NORMAL</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">篩選準則分類</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

此檔案僅支援透過 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 的提取模式;它不支援 push 模式。

由於 MPEG-2 內容未建立索引，因此搜尋可能非常近似。 通常適用于固定位元速率的 MPEG-2 系統串流 (通常是針對視訊 CD) 產生的硬體。

篩選準則支援 [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) 介面，可用於抓取 ID3 中繼資料。

並非所有 MPEG 範例都有時間戳記。 MPEG 範例上缺少時間戳記並不是錯誤。 若為篩選開發人員，這表示如果 [**IMediaSample：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime)失敗，您就不應該從輸入 Pin 的 **Receive** 方法傳回錯誤碼。 如果 **Receive** 傳回 S 以外的任何值 \_ ，則會導致分隔器停止傳送範例。

如果檔案包含影片資料流程，則 MPEG-2 資料流程分隔器支援依框架編號搜尋。 若要啟用以框架為基礎的搜尋，請在 [篩選圖形管理員](filter-graph-manager.md)上以值 **時間 \_ 格式 \_ 框架** 呼叫 [**IMediaSeeking：： SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 




