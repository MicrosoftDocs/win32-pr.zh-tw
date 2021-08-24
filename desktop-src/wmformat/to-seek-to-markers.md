---
title: 搜尋標記
description: 搜尋標記
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- Advanced Systems Format (ASF) ，搜尋標記
- ASF (Advanced Systems Format) ，搜尋標記
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) ，標記
- ASF (Advanced Systems Format) ，標記
- 非同步讀取器，搜尋標記
- 非同步讀取器，標記
- 標記，搜尋
- 標記，非同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3361546f4087e0c2104809435d9d75e8711560ec4f3c55855d14b05ef4dfb8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807348"
---
# <a name="to-seek-to-markers"></a>搜尋標記

標記是 ASF 檔案中的命名位置。 您只能使用非同步讀取器，從標記的位置開始播放。 您可以遵循下列步驟，開始在標記上播放。

1.  呼叫 **IWMReader：： QueryInterface** 以取得 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 介面的指標。
2.  藉由呼叫 [**IWMHeaderInfo：： GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount)，以取出檔案中的標記總數。
3.  使用步驟2中取出的標記計數，逐一查看標記。 針對每個標記呼叫 [**IWMHeaderInfo：： GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) ，以抓取每個標記的名稱和時間。 儲存所需標記的索引。
4.  呼叫 **IWMReader：： QueryInterface** 以取得 [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) 介面的指標。
5.  藉由呼叫 [**IWMReaderAdvanced2：： StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)，指定要開始播放的標記。 您必須傳遞所需標記的索引，這是您在步驟3中儲存的標記。
6.  如同您在 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) 方法的實中一般地處理範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**標記**](markers.md)
</dt> <dt>

[**使用非同步讀取器讀取檔案**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**使用索引**](working-with-indexes.md)
</dt> </dl>

 

 




