---
description: 時間相關函數會以數種格式的其中一種傳回時間。 您可以使用時間函數在某些時間格式之間進行轉換，以方便比較和顯示。 下表摘要說明時間格式。
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: 是時候了
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cb2cd140ada7033ebe7bf672e654dbf7227385509c676176ee8e936ff590ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765029"
---
# <a name="about-time"></a>是時候了

時間相關函數會以數種格式的其中一種傳回時間。 您可以使用時間函數在某些時間格式之間進行轉換，以方便比較和顯示。 下表摘要說明時間格式。



| 格式          | 類型                                                                     | 描述                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 系統          | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | 取自內部硬體時鐘的年、月、日、小時、秒和毫秒。                                            |
| 本機           | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)或 [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) | 轉換成系統本地時區的系統時間或檔案時間。                                                               |
| 檔案            | [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | 自1601年1月1日起的 100-毫微秒間隔數目。                                                                       |
| MS-DOS          | **WORD**                                                                 | 日期的壓縮文字，另一個用於時間。                                                                                   |
| Windows         | **DWORD** 或 **ULONGLONG**                                               | 自上次啟動系統之後的毫秒數。 當抓取為 DWORD 值時，Windows 時間會每49.7 天迴圈。 |
| 中斷計數 | **ULONGLONG**                                                            | 自系統上次啟動後的 100-毫微秒間隔數目。                                                           |



 

如需詳細資訊，請參閱下列主題：

-   [系統時間](system-time.md)
-   [當地時間](local-time.md)
-   [檔案時間](file-times.md)
-   [MS-DOS 日期和時間](ms-dos-date-and-time.md)
-   [Windows Time](windows-time.md)
-   [停機時間](interrupt-time.md)

 

 
