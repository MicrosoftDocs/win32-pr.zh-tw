---
title: 進程記憶體使用量資訊
description: GetProcessMemoryInfo 函式會採用進程控制碼做為輸入，並將進程 \_ 記憶體 \_ 計數器結構填入進程的記憶體統計資料相關資訊。
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac85a62853cf95dcf42380c76b914f23045152b32499870182a47ee2449e8ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094700"
---
# <a name="process-memory-usage-information"></a>進程記憶體使用量資訊

[**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo)函式會採用進程控制碼做為輸入，並將進程 [**\_ 記憶體 \_ 計數器**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters)結構填入進程的記憶體統計資料相關資訊。 **Cb** 成員接收結構的大小。 **PageFaultCount** 成員會收到分頁錯誤數。 其餘成員會收到下列類別的目前和尖峰記憶體使用量：

-   工作集
-   分頁集區
-   非分頁集區
-   分頁檔

*工作集* 是指在指定時間實際對應至進程內容的記憶體數量。 *分頁式集* 區中的記憶體是系統記憶體，可在磁片上傳送至分頁檔 (分頁) 未使用時使用。 *非分頁集區中* 的記憶體是系統記憶體，只要配置了對應的物件，就無法將其分頁至磁片。 *頁面* 檔案使用方式代表針對系統分頁檔案中的進程所設定的記憶體數量。 當記憶體使用量過高時，虛擬記憶體管理員會將選取的記憶體分頁至磁片。 當執行緒需要不在記憶體中的頁面時，記憶體管理員會從分頁檔重載該頁面。

 

 




