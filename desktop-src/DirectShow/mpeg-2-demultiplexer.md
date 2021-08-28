---
description: 此篩選器會 demultiplexes 以推送模式傳遞的 MPEG-2 傳輸和程式串流。
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: MPEG-2 信號信號
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21898cb4fa3c16b07508dc3370c519d3edfbced
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983951"
---
# <a name="mpeg-2-demultiplexer"></a>MPEG-2 信號信號

此篩選器會 demultiplexes 以推送模式傳遞的 MPEG-2 傳輸和程式串流。 從 Windows XP 開始，此篩選器也支援在提取模式下的程式資料流程 (檔案播放) 。 在舊版平臺上，請在提取模式中使用程式資料流程的 [Mpeg-2 分隔](mpeg-2-splitter.md) 器篩選器。 此篩選器可以在任何類型的篩選圖形中使用，包括 BDA 數位電視濾波器圖形。

> [!Note]  
> MPEG-2 信號信號不支援框架正確的搜尋。

 




| 標籤 | 值 |
|--------|-------|
| 篩選介面 | 所有模式：<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><strong>ISpecifyPropertyPages</strong></li></ul>僅限推送模式：<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li></ul> | 
| 輸入 Pin 媒體類型 | 主要類型： MEDIATYPE_STREAM<br /> 亞：<br /><ul><li>KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</li></ul>如需詳細資訊，請參閱 <a href="mpeg-2-demultiplexer-media-types.md"><strong>Mpeg-2 信號的媒體類型</strong></a>。<br /> | 
| 輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| 輸出 Pin 媒體類型 | 音訊和影片的基本資料流程必須有主要類型的 MEDIATYPE_Audio 或 MEDIATYPE_Video。<br /> 如需詳細資訊，請參閱 <a href="mpeg-2-demultiplexer-media-types.md"><strong>Mpeg-2 信號的媒體類型</strong></a>。<br /> | 
| 輸出 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>，僅限 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>Push 模式： <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>、 <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a><br /> 僅提取模式： <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a><br /> | 
| 篩選 CLSID | CLSID_MPEG2Demultiplexer | 
| 屬性頁 CLSID | 僅供測試之用。 使用 <strong>ISpecifyPropertyPages</strong> 介面存取屬性頁 | 
| 可執行檔 | mpg2splt.ax | 
| <a href="merit.md">優點</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">篩選準則分類</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>備註

若要輸出音訊和影片的基本資料流程，demux 必須接收 PCR 和 SCR 資料流程。 在輸入端，這表示傳輸資料流程必須包含定義 PCR 資料流程之 PID 的 PAT 和 PMT 資料表;和程式資料流程必須包含至少一個套件標頭。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |
| 伺服器支援結束<br/>    | Windows Server 2003 R2<br/>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> <dt>

[使用 MPEG-2 信號信號](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




