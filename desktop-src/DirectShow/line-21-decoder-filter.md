---
description: 第21行解碼篩選
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: 第21行解碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b0668d4b71b8dcccf4ceacf7f5428fa7a65ad52
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468235"
---
# <a name="line-21-decoder-filter"></a>第21行解碼篩選

此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

這一行21的解碼篩選器會解碼第21行的資料，並將標題文字繪製到點陣圖上。

輸入 pin 會連接到任何第21行的資料提供者，通常是 DVD video 解碼器或 [CC 解碼器](cc-decoder-filter.md) 篩選器。 CC 解碼器提供類比電視信號 VBI 的第21行資料。 輸出連接會連線到重迭[Mixer](overlay-mixer-filter.md)上的次要 pin，或連接至另一部影片轉譯器（例如 VMR）。

此篩選器會接受標準位元組配對格式的第21行資料，或以 DVD 作為整個圖片群組 (GOP) 的封包。 針對 DVD video 串流中的每個 GOP，可能會有使用者資料封包，其中包含該特定 GOP 的標頭資訊和第21行資料。 位元組組的格式定義于 EIA/CEA-608-B 標準中;如需詳細資訊，請參閱該標準。

此篩選器有兩個版本可供使用：



| 篩選            | CLSID                 |
|-------------------|-----------------------|
| 第21行的解碼器   | CLSID \_ Line21Decoder  |
| 第21行的解碼器2 | CLSID \_ Line21Decoder2 |



 

第1版的篩選器適用于 Microsoft® Windows® 95/98/Me 和 Windows 2000 平臺。 第2版的篩選器可在 Microsoft Windows XP 及更新版本中使用，且會在影片混合轉譯器位於圖形中時使用。

下表中的資訊適用于這兩個版本的篩選：




| | |篩選介面 | <a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | |輸入 Pin 媒體類型 |主要類型： MEDIATYPE_AUXLine21DataSubtype：<br /><ul><li>MEDIASUBTYPE_Line21_BytePair (標準行 21) </li><li>MEDIASUBTYPE_Line21_GOPPacket (DVD 行 21) </li></ul>格式類型： FORMAT_VideoInfo 或 GUID_Null<br /> | |輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |輸出釘選媒體類型 |主要類型： MEDIATYPE_VideoSubtype：<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul>格式類型： FORMAT_VideoInfo<br /> | |輸出 Pin 介面 | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |篩選 CLSID |請參閱上表 | |屬性頁 CLSID |無 | |可執行檔 |qdvd.dll | | <a href="merit.md">業績</a> |第21行： MERIT_NORMALLine 21 的解碼器2： MERIT_NORMAL + 2<br /> | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> <dt>

[隱藏式輔助字幕和 Teletext](closed-captions-and-teletext.md)
</dt> <dt>

[DVD 篩選 Graph 設定](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




