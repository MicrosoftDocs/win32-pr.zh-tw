---
title: 使用非同步讀取器依 SMPTE 時間程式碼進行搜尋
description: 使用非同步讀取器依 SMPTE 時間程式碼進行搜尋
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Advanced Systems Format (ASF) ，以 SMPTE 時間碼搜尋
- ASF (Advanced Systems Format) ，以 SMPTE 時間碼搜尋
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) 、SMPTE 時間碼
- ASF (Advanced Systems Format) ，SMPTE 時間碼
- 非同步讀取器，依 SMPTE 時間碼搜尋
- 非同步讀取器，SMPTE 時間碼
- SMPTE 時間代碼，搜尋
- SMPTE 時間代碼，非同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bb90e899db9820ccbd14e42b9699a5f99c7434
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374382"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a>使用非同步讀取器依 SMPTE 時間程式碼進行搜尋

讀取器物件可以根據與影片資料流程相關聯的 SMPTE 時間代碼，來搜尋檔案中的某個點。 時間碼資料會封裝在以資料單位延伸的形式附加至影片範例的 [**WMT 時間 \_ 碼 \_ 延伸模組 \_ 資料**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) 結構中。

SMPTE 時間代碼是由範圍和該範圍內的時間代碼所定義。 範圍是連續的時間序列代碼。 每次程式碼都是以小時、分鐘、秒和框架來定義。

若要使用非同步讀取器以 SMPTE 時間程式碼在 ASF 檔案中搜尋資料，請執行下列步驟。

1.  藉由呼叫 **IWMReader：： QueryInterface**，取得讀取器物件之 [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)介面的指標。
2.  藉由呼叫 [**IWMReaderAdvanced3：： StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition)來設定開始時間的程式碼和持續時間。 您必須指定依時間代碼編制索引之影片資料流程的串流號碼。 讀取器會將輸出的其餘部分與指定之資料流程的指定框架的呈現時間進行同步處理，並開始傳遞輸出範例。
3.  如同您在 **IWMReaderCallback：： OnSample** 方法的實中一般地處理範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用非同步讀取器讀取檔案**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**使用索引**](working-with-indexes.md)
</dt> <dt>

[**SMPTE 時間代碼支援**](smpte-time-code-support.md)
</dt> </dl>

 

 




