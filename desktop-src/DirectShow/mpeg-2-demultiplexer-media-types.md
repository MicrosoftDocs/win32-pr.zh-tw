---
description: MPEG-2 信號信號媒體類型
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: MPEG-2 信號信號媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9b5276b975771ba62118976c8e63b4d5faa53d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909996"
---
# <a name="mpeg-2-demultiplexer-media-types"></a>MPEG-2 信號信號媒體類型

[Mpeg-2 信號信號](mpeg-2-demultiplexer.md)篩選器可識別下列媒體類型。

### <a name="input-types"></a>輸入類型

主要類型一律為 **媒體型 \_ 串流**。 子類型可以是下列任何一項。



| GUID                                             | Description                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **KSDATAFORMAT \_ 子類型 \_ BDA \_ MPEG2 \_ 傳輸** | 從廣播驅動程式架構傳輸串流 (BDA) 裝置篩選器。 MPEG-2 信號信號會將這個子類型視為與 **MEDIASUBTYPE \_ MPEG2 \_ 傳輸** 相同。                                |
| **MEDIASUBTYPE \_ MPEG2 \_ 計畫**                 | 程式資料流程                                                                                                                                                                                            |
| **MEDIASUBTYPE \_ MPEG2 \_ 傳輸**               | 傳輸串流 (TS) ，包含188個位元組的封包                                                                                                                                                              |
| **MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE**       | 具有 "strided" 封包的傳輸資料流程。 此子類型表示 TS 封包可以填補額外的位元組。 如需詳細資訊，請參閱 [**MPEG2 \_ 傳輸 \_ STRIDE**](mpeg2-transport-stride.md)。 |



 

針對 strided 傳輸封包 (**MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ stride**) ，每個媒體範例都必須包含整數個傳輸封包，如 [**MPEG2 \_ 傳輸 \_ 跨距**](mpeg2-transport-stride.md)中所述。 對於所有其他輸入類型，範例界限沒有任何限制;個別的封包可以跨越範例界限。

### <a name="output-types"></a>輸出型別

MPEG-2 信號信號不會驗證輸出類型;下游篩選器負責剖析它從信號剖析收到的資料。 不過，下游篩選器通常會接受下列類型做為信號的輸出。

### <a name="mpeg-2-sections"></a>MPEG 2 區段



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>主要類型</td>
<td><strong>MEDIATYPE_MPEG2_SECTIONS</strong></td>
</tr>
<tr class="even">
<td>Subtype</td>
<td>下列任何一項：<br/>
<ul>
<li><strong>MEDIASUBTYPE_ATSC_SI</strong>： ATSC 服務資訊。</li>
<li><strong>MEDIASUBTYPE_DVB_SI</strong>： Dvb-t 服務資訊。</li>
<li><strong>MEDIASUBTYPE_ISDB_SI</strong>：整合服務數位廣播 (ISDB) 服務資訊。</li>
<li><strong>MEDIASUBTYPE_MPEG2DATA</strong>： mpeg-2 區段資料。</li>
</ul></td>
</tr>
<tr class="odd">
<td>格式類型</td>
<td>無</td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a>MPEG-2 影片



| 標籤 | 值 |
|------------------|------------------------------------------|
| 主要類型       | **媒體 \_ 媒體**                     |
| Subtype          | **MEDIASUBTYPE \_ MPEG2 \_ 影片**           |
| 格式類型      | **格式 \_ MPEG2Video**                   |
| 格式結構 | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a>MPEG-2 音訊



| 標籤 | 值 |
|------------------|--------------------------------------|
| 主要類型       | **媒體 \_ 媒體**                 |
| Subtype          | **MEDIASUBTYPE \_ MPEG2 \_ 音訊**       |
| 格式類型      | **格式 \_ WaveFormatEx**             |
| 格式結構 | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MPEG-2 媒體類型](mpeg-2-media-types.md)
</dt> </dl>

 

 
