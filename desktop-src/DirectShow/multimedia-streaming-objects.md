---
description: 多媒體串流物件
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: 多媒體串流物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05762e4a3d7aa486b8a22b73905fc5d9c1610078
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321651"
---
# <a name="multimedia-streaming-objects"></a>多媒體串流物件

> [!Note]  
> 此 API 即將淘汰。 新的應用程式不應使用它。

 

下表描述多媒體串流物件。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>CLSID</th>
<th>Description</th>
<th>支援的介面</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CLSID_AMMediaTypeStream</td>
<td>可以為任何支援 DirectShow 的資料類型建立媒體範例</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>CLSID_AMAudioData</td>
<td><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a>音訊容器物件的執行。</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>CLSID_AMDirectDrawStream</td>
<td>可以新增至 DirectShow 多媒體串流的 DirectDraw 媒體資料流程。</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>CLSID_AMMultiMediaStream</td>
<td>多媒體串流的 DirectShow 實行。</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>CLSID_MediaStreamFilter</td>
<td>透過 <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> 介面提供 CLSID_AMMultiMediaStream 物件的多媒體串流處理功能。</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>N/A</td>
<td>CLSID_AMMediaTypeStream 物件所建立的範例。</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>N/A</td>
<td>DirectDraw 資料流程所建立的範例。</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



