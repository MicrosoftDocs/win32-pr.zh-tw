---
description: MPEG-2 分隔器
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: MPEG-2 分隔器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417fcca0bfc7a5c24416cfc2cb915f968c12105d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465251"
---
# <a name="mpeg-2-splitter"></a>MPEG-2 分隔器

從 Microsoft® Windows® XP 開始，MPEG 2 分隔器篩選器已被取代。 請改用 [Mpeg-2 信號](mpeg-2-demultiplexer.md) 。

在舊版平臺上，使用 MPEG-2 分隔器，以提取模式提供的 MPEG-2 程式資料流程，其中至少包含下列其中一個資料流程類型： MPEG-2 影片;MPEG-2 音訊;以 DVD video 定義的 AC3 音訊編碼;或 PCM 音訊編碼為 DVD 影片的定義。 此篩選器會剖析串流、建立每個資料流程的輸出針腳，然後將壓縮的 MPEG 音訊或影片封包輸出到 MPEG-2 的解碼器篩選器。

針對以推送模式傳遞的程式和傳輸資料流程，請在所有平臺上使用 [Mpeg-2 信號](mpeg-2-demultiplexer.md)。

> [!Note]  
> MPEG-2 分隔器不支援框架精確的搜尋。

 




| | |篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <strong>ISpecifyPropertyPages</strong>、 <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a> | |輸入 Pin 媒體類型 | <ul><li>MEDIATYPE_Stream，MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIATYPE_Stream，MEDIASUBTYPE_MPEG1_Video</li><li>MEDIATYPE_Stream，MEDIASUBTYPE_Null</li></ul> | |輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |輸出釘選媒體類型 |相依于資料流程類型。 請參閱 <a href="mpeg-2-splitter-media-types.md">Mpeg-2 分隔器媒體類型</a> | |輸出 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | |篩選 CLSID |CLSID_MMSPLITTER | |屬性頁 CLSID |不適用 | |可執行檔 |mpg2splt.ax | | <a href="merit.md">業績</a> |MERIT_NORMAL + 1 | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_AudioInputDeviceCategory | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> <dt>

[使用 MPEG-2 分隔器](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



