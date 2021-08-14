---
title: 使用同步讀取器依 SMPTE 時間碼進行搜尋
description: 使用同步讀取器依 SMPTE 時間碼進行搜尋
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Advanced Systems Format (ASF) ，以 SMPTE 時間碼搜尋
- ASF (Advanced Systems Format) ，以 SMPTE 時間碼搜尋
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- Advanced Systems Format (ASF) 、SMPTE 時間碼
- ASF (Advanced Systems Format) ，SMPTE 時間碼
- 同步讀取器，依 SMPTE 時間碼搜尋
- 同步讀取器，SMPTE 時間碼
- SMPTE 時間代碼，搜尋
- SMPTE 時間代碼，同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b368492d45d3bc564ce0fbb84a6013349c26fcdaca8c1ad576863a9cee6f6f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196467"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a>使用同步讀取器依 SMPTE 時間碼進行搜尋

同步讀取器物件可以根據與影片資料流程相關聯的 SMPTE 時間代碼，來搜尋檔案中的某個點。 時間碼資料會封裝在以資料單位延伸的形式附加至影片範例的 [**WMT 時間 \_ 碼 \_ 延伸模組 \_ 資料**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) 結構中。

SMPTE 時間代碼是由範圍和該範圍內的時間代碼所定義。 範圍是連續的時間序列代碼。 每次程式碼都是以小時、分鐘、秒和框架來定義。

若要使用同步讀取器以 SMPTE 時間代碼在 ASF 檔案中搜尋資料，請執行下列步驟。

1.  藉由呼叫 [**IWMSyncReader：： SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe)，設定範例傳遞的開始時間碼和結束時間碼。 您必須指定依時間代碼編制索引之影片串流的串流號碼。 同步讀取器會將輸出的其餘部分，同步處理至指定資料流程之指定框架的呈現時間。
2.  開始使用 [**IWMSyncReader：： GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample)的呼叫來抓取範例。 以您平常使用同步讀取器的方式繼續進行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用同步讀取器讀取檔案**](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[**SMPTE 時間代碼支援**](smpte-time-code-support.md)
</dt> <dt>

[**使用索引**](working-with-indexes.md)
</dt> </dl>

 

 




