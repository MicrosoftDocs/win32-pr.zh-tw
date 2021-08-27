---
description: DVD 瀏覽器篩選
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: DVD 瀏覽器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d248e490201536e92afeb38f520028e29ea9a5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477295"
---
# <a name="dvd-navigator-filter"></a>DVD 瀏覽器篩選

DVD 瀏覽器篩選器是 DVD-Video 播放篩選圖形的來源篩選。 它會開啟 DVD-Video 磁片區中所有必要的檔案、流覽線性 DVD-Video，然後剖析產生的 MPEG-2 程式串流、將資料流程分割成三種 (的影片、音訊、子圖片) 輸出圖釘。

DVD 瀏覽器篩選器也會執行 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 和 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) 介面，讓 DVD 播放應用程式控制 DVD-Video 播放。




| | |篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>、 <strong>ISpecifyPropertyPages</strong> | |輸入 Pin 媒體類型 |MEDIATYPE_Stream，MEDIASUBTYPE_MPEG2_PROGRAM | |輸入 Pin 介面 |不適用。 | |輸出釘選媒體類型 |基底類型：<br /><ul><li>影片： <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>、 <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li>音訊： <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>， <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li>子圖片： <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>、 <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li></ul>擴充類型：<br /> 視訊：<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>， <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li><strong>MEDIATYPE_Video</strong>， <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>， <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li></ul>音訊：<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>， <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li><strong>MEDIATYPE_Audio</strong>， <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>， <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li></ul>子圖片<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>， <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li><li><strong>MEDIATYPE_Video</strong>， <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>， <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li></ul>若要啟用擴充類型，請呼叫 <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2：： SetOption</strong></a> ，並設定 <br /> | |輸出 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |篩選 CLSID |CLSID_DVDNavigator | |屬性頁 CLSID |沒有屬性頁。 | |可執行檔 |qdvd.dll | | <a href="merit.md">業績</a> |MERIT_DO_NOT_USE | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 




