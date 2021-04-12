---
description: Windows Media 來源篩選
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Windows Media 來源篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe60a038cfd5109a5c55ca6c40640d39b2426d3a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104195719"
---
# <a name="windows-media-source-filter"></a>Windows Media 來源篩選

此篩選器是 Windows Media®內容的舊版來源篩選器。 它是由 Windows Media Player 6.4 所使用。 一般而言，使用此篩選器的最簡單且最可靠的方式，就是使用 Windows Media Player 6.4 ActiveX 控制項。 此篩選器公開的許多方法也會透過 ActiveX 控制項公開。 如需詳細資訊，請參閱 Windows Media Player SDK。

當此篩選器指定本機 ASF 檔案的名稱或遠端檔案的 URL 時，它會讀取檔案、剖析壓縮的資料流程，並為每個檔案建立輸出圖釘。 此篩選器不會使用 Windows Media 格式 SDK。 它會使用 Windows Media 解碼器的可安裝編解碼器版本，而不是 SQL-DMO 版本。 音訊輸出圖釘一律會連接到 ASF 的處理常式篩選器，而影片 pin 一律會連接到 ASF ICM 處理常式。  (ICM 在此案例中是指視訊壓縮管理員的原始名稱。 ) 篩選器不支援搜尋。

下圖顯示具有此篩選的篩選圖形。

![windows media 來源篩選圖形](images/wms-wmv-graph.png)

為了維持與 Windows Media Player 6.4 的回溯相容性，此篩選器是具有 .wma、.wmv 和 .asf 副檔名之檔案的預設來源篩選。 針對檔案播放，較新的應用程式應該使用 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器。 但是，WM ASF 讀取器不支援播放資料流程內容。

應用程式播放資料流程式 Windows 媒體內容的最簡單方式是使用 Windows Media Player SDK。 另一個選項是使用 Windows Media Format SDK。 不建議您嘗試以 Windows Media 來源篩選器為基礎來建立自訂播放機。



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IAMChannelInfo**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo)、 [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking)、 [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)、 [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)、 [**IAMNetShowConfig**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig)、 [**IAMNetShowExProps**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops)、 [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll)、 [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus)、 [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| 輸入 pin 媒體類型                    | 不適用。                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 輸入 pin 介面                     | 不適用。                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 輸出 pin 媒體類型                   | 會根據 ASF 檔案內的資料流程而有所不同。                                                                                                                                                                                                                                                                                                                                                                                                               |
| 輸出 pin 介面                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 篩選 CLSID                             | 請參閱備註                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 可執行檔                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [優點](merit.md)                       | 一般的業績 \_                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>備註

Qnetwork 中未定義篩選的 CLSID。 在您自己的標頭檔中使用此宏：


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[在 DirectShow 中讀取 ASF 檔案](reading-asf-files-in-directshow.md)
</dt> <dt>

[WM ASF 讀取器篩選器](wm-asf-reader-filter.md)
</dt> </dl>

 

 



