---
description: QuickTime 影片剖析器篩選
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: QuickTime 影片剖析器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0028b604efe31749144ca98cb80057685ed0c1db
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983611"
---
# <a name="quicktime-movie-parser-filter"></a>QuickTime 影片剖析器篩選

此元件已從 Windows Vista 和更新版本的作業系統中移除。 它可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。

QuickTime Movie 剖析器篩選器會將 Apple® QuickTime®資料分割成音訊和影片串流。 它支援 QuickTime 2.0 及更早版本。 輸入 pin 會連接到來源篩選器，例如 [非同步檔案來源](file-source--async--filter.md) 篩選或 URL 檔案 [來源](file-source--url--filter.md) 篩選。 剖析器會使用 [AVI 解壓縮](avi-decompressor-filter.md) 程式或 [QT 解壓縮](qt-decompressor-filter.md) 程式篩選器，將 QuickTime 檔案解壓縮。 此篩選器會為影片串流建立一個輸出圖釘，並為音訊串流建立一個輸出圖釘。




| 標籤 | 值 |
|--------|-------|
| 篩選介面 | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a> | 
| 輸入 Pin 媒體類型 | MEDIATYPE_Stream，MEDIASUBTYPE_QTMovie; | 
| 輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| 輸出 Pin 媒體類型 | <ul><li>MEDIATYPE_Video、MEDIASUBTYPE_Null FORMAT_VideoInfo</li><li>MEDIATYPE_Audio、MEDIASUBTYPE_Null FORMAT_WaveFormatEx</li></ul> | 
| 輸出 Pin 介面 | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| 篩選 CLSID | CLSID_QuickTimeParser | 
| 屬性頁 CLSID | 沒有屬性頁。 | 
| 可執行檔 | quartz.dll | 
| <a href="merit.md">優點</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">篩選準則分類</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



