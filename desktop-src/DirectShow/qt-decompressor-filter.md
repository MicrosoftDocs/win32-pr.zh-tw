---
description: QT 解壓縮程式篩選器
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: QT 解壓縮程式篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6f28058a1c729c9d42b20651a86ba31b4d98c7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467965"
---
# <a name="qt-decompressor-filter"></a>QT 解壓縮程式篩選器

此元件已從 Windows Vista 和更新版本的作業系統中移除。 它可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。

QT 解壓縮程式篩選器會®2.0 影片解壓縮 Apple® QuickTime。 此格式通常用於較舊的 QuickTime 檔案中。




| | |篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | |輸入 Pin 媒體類型 |MEDIATYPE_Video，FORMAT_VideoInfo<br /> 下列子類型有效：<br /><ul><li>MEDIASUBTYPE_QTRpza</li><li>MEDIASUBTYPE_QTSmc</li><li>MEDIASUBTYPE_QTRle</li><li>MEDIASUBTYPE_QTJpeg</li></ul> | |輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |輸出釘選媒體類型 |MEDIATYPE_Video、MEDIASUBTYPE_Null、FORMAT_VideoInfo | |輸出 Pin 介面 | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |篩選 CLSID |CLSID_QTDec | |屬性頁 CLSID |沒有屬性頁。 | |可執行檔 |quartz.dll | | <a href="merit.md">業績</a> |MERIT_NORMAL | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 




