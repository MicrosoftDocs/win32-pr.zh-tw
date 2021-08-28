---
description: 條件式包裝函式篩選
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: 條件式包裝函式篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0688150ab417c6ebb71313a438f72ef7839042
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985351"
---
# <a name="acm-wrapper-filter"></a>條件式包裝函式篩選

「通過包裝函式」篩選器可讓音訊壓縮管理員 (的) 編解碼器來聯結篩選圖形。 它可做為解壓縮篩選器或壓縮篩選器。

在解壓縮篩選器中，[LegacyAmFilterCategory 篩選] 類別目錄 DirectShow 中會出現 [篩選] 類別， (CLSID \_) 並具有正常的業績 \_ 。 輸入 pin 的連接媒體類型會決定篩選器所使用的編解碼器。 一般而言，應用程式不需要將篩選準則加入至篩選圖形;當需要時，篩選 Graph 管理員會自動將它提取。 解壓縮只適用于 PCM 音訊。

若為壓縮篩選，則會在 [音訊壓縮機] 類別中顯示「」類別 (CLSID \_ AudioCompressorCategory) ，並有 \_ 「 \_ 未使用」的優點 \_ 。 每個編解碼器都會顯示為個別的實例。 針對壓縮，您無法直接使用 CoCreateInstance 建立篩選器。 相反地，您必須使用系統裝置枚舉器。 如需詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。




| 標籤 | 值 |
|--------|-------|
| 篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、IPersist、IPersistPropertyBag | 
| 輸入 pin 媒體類型 | MEDIATYPE_Audio、MEDIASUBTYPE_Null FORMAT_WaveFormatEx | 
| 輸入 pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| 輸出 pin 媒體類型 | MEDIATYPE_Audio、MEDIASUBTYPE_PCM FORMAT_WaveFormatEx。可能的任何組合如下：<br /><ul><li>每秒樣本數 (kHz) ：44.1、22.05、11.025 或8.0。</li><li>通道：身歷聲或 mono。</li><li>每個樣本的位數：8或16。</li></ul> | 
| 輸出 pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| 篩選 CLSID | CLSID_ACMWrapper | 
| 屬性頁 CLSID | 沒有屬性頁。 | 
| 可執行檔 | Quartz.dll | 
| <a href="merit.md">優點</a> | MERIT_NORMAL 或 MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">篩選準則分類</a> | CLSID_LegacyAmFilterCategory 或 CLSID_AudioCompressorCategory | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 




