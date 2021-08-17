---
title: 取得讀取器效能統計資料
description: 取得讀取器效能統計資料
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- Advanced Systems Format (ASF) ，讀取器效能統計資料
- ASF (Advanced 系統格式) ，讀取器效能統計資料
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) ，效能統計資料
- ASF (Advanced Systems Format) ，效能統計資料
- 非同步讀取器，效能統計資料
- 效能，讀取器統計資料
- 效能，非同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2397e575d67a699c4f211d872b53632e728fc2240b396d7475c8bb6b243fe445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084260"
---
# <a name="to-get-reader-performance-statistics"></a>取得讀取器效能統計資料

使用非同步讀取器在本機讀取檔案時，不需要檢查讀取作業的效能。 但是，如果您的應用程式是從串流來源讀取，則效能統計資料可能很重要。 您的應用程式可以回應播放效能的變更，以確保能獲得最佳的終端使用者體驗。

您可以從讀取器中取出的效能資訊包括下列統計資料：

-   連接目前的頻寬。
-   從伺服器收到的封包數目。
-   已復原之遺失的封包數目。
-   未復原之遺失的封包數目。
-   已接收之已傳送封包總數的百分比。

若要取得讀取器效能統計資料，請執行下列步驟。

1.  開始播放之前，請先建立 [**WM \_ 讀取器 \_ 統計資料**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) 結構。 您必須將 **cbSize** 成員設定為 SIZEOF (WM \_ 讀取器 \_ 統計資料) 。
2.  藉由呼叫 **IWMReader：： QueryInterface**，取得讀取器物件之 [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)介面的指標。
3.  在播放期間，請經常呼叫 [**IWMReaderAdvanced：： GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) 來監視效能。 在每次呼叫時傳遞您的 **WM \_ 讀取器 \_ 統計資料** 結構，並檢查適當的成員。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用非同步讀取器讀取檔案**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




