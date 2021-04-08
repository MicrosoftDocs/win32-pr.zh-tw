---
title: 使用同步讀取器依時間進行搜尋
description: 使用同步讀取器依時間進行搜尋
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- Advanced Systems Format (ASF) ，依時間搜尋
- ASF (Advanced Systems Format) ，依時間搜尋
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- 同步讀取器，依時間搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a43e914a6fc0d320860db61f4747cbee3033e9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681424"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a>使用同步讀取器依時間進行搜尋

若要使用同步讀取器來搜尋資料，您可以指定播放範圍。 範圍是由起始的呈現時間和持續時間所定義，兩者皆以 100-毫微秒單位表示。

若要使用同步讀取器以簡報時間在 ASF 檔案中搜尋資料，請執行下列步驟。

1.  藉由呼叫 [**IWMSyncReader：： SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange)來指定範例傳遞的開始時間和持續時間。 這個方法不會要求您指定資料流程號碼，因為每個資料流程的呈現時間應該已同步處理。
2.  開始使用 [**IWMSyncReader：： GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample)的呼叫來抓取範例。 以您平常使用同步讀取器的方式繼續進行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMSyncReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**使用同步讀取器讀取檔案**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




