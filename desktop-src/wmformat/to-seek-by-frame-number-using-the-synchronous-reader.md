---
title: 使用同步讀取器依框架編號搜尋
description: 使用同步讀取器依框架編號搜尋
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- Advanced Systems Format (ASF) ，依框架編號搜尋
- ASF (Advanced Systems Format) ，依框架編號搜尋
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- 同步讀取器，依框架編號搜尋
- 影片串流，依畫面格編號搜尋
- 影片串流，同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c26711d2d839e47279e7e52a50f5dc82c6e81da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314268"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a>使用同步讀取器依框架編號搜尋

若要使用同步讀取器依框架編號搜尋資料，您可以指定播放範圍。 範圍是由特定影片串流中的起始畫面格編號，以及要播放的一些畫面格所定義。

若要使用同步讀取器依框架號碼在 ASF 檔案中搜尋資料，請執行下列步驟。

1.  藉由呼叫 [**IWMSyncReader：： SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe)，設定要讀取範例傳遞的起始畫面格數目和框架數目。 您必須指定框架索引影片資料流程的串流號碼。 讀取器會將輸出的其餘部分與指定之資料流程的指定框架的呈現時間進行同步處理，並開始傳遞輸出範例。
2.  開始使用 [**IWMSyncReader：： GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample)的呼叫來抓取範例。 以您平常使用同步讀取器的方式繼續進行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMSyncReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**使用同步讀取器讀取檔案**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




