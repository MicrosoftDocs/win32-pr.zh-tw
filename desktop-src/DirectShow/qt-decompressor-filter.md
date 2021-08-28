---
description: QT 解壓縮程式篩選器
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: QT 解壓縮程式篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cedb26acdcfabb3c0be4aeb2cbf306b654f9570
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983644"
---
# <a name="qt-decompressor-filter"></a>QT 解壓縮程式篩選器

此元件已從 Windows Vista 和更新版本的作業系統中移除。 它可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。

QT 解壓縮程式篩選器會®2.0 影片解壓縮 Apple® QuickTime。 此格式通常用於較舊的 QuickTime 檔案中。




| 標籤 | 值 |
|--------|-------|
| 篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| 輸入 Pin 媒體類型 | MEDIATYPE_Video，FORMAT_VideoInfo<br /> 下列子類型有效：<br /><ul><li>MEDIASUBTYPE_QTRpza</li><li>MEDIASUBTYPE_QTSmc</li><li>MEDIASUBTYPE_QTRle</li><li>MEDIASUBTYPE_QTJpeg</li></ul> | 
| 輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| 輸出 Pin 媒體類型 | MEDIATYPE_Video、MEDIASUBTYPE_Null FORMAT_VideoInfo | 
| 輸出 Pin 介面 | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| 篩選 CLSID | CLSID_QTDec | 
| 屬性頁 CLSID | 沒有屬性頁。 | 
| 可執行檔 | quartz.dll | 
| <a href="merit.md">優點</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">篩選準則分類</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 




