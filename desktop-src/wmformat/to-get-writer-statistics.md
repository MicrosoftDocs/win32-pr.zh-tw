---
title: 取得寫入器統計資料
description: 取得寫入器統計資料
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Advanced Systems Format (ASF) 、寫入器統計資料
- ASF (Advanced 系統格式) 、寫入器統計資料
- 寫入器統計資料，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103933008"
---
# <a name="to-get-writer-statistics"></a>取得寫入器統計資料

寫入器可以提供有關撰寫作業的統計資訊。 有兩種方法可以收集寫入器統計資料： [**IWMWriterAdvanced：： GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) 和 [**IWMWriterAdvanced3：： GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex)。 **GetStatisticsEx** 抓取的資訊比 **GetStatistics** 所抓取的資訊更明確。

這兩種方法都會以統計資訊填入結構。 **GetStatistics** 會使用 [**wm \_ 寫入器 \_ 統計資料**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) 結構，而 **GetStatisticsEx** 會使用 [**wm \_ 寫入器 \_ 統計資料 \_ EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) 結構。 **GetStatisticsEx** 不會複製 **GetStatistics** 所取得的資料。 如需最完整的資訊，您應該呼叫這兩種方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMWriterAdvanced 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**IWMWriterAdvanced3 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 




