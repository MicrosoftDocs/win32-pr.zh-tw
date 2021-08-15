---
title: 工具說明函數
description: 列出工具說明程式庫函數。
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73cc425f415c9cea8af9290743fb1afbb51182f8c03e7ec087ca95948fd2ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058216"
---
# <a name="tool-help-functions"></a>工具說明函數

下列功能是工具 help library 的一部分。



| 函式                                                           | 描述                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | 取得指定進程的快照集，以及這些進程所使用的堆積、模組和執行緒。 |
| [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | 抓取進程已配置之堆積第一個區塊的相關資訊。                      |
| [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | 抓取指定進程已配置之第一個堆積的相關資訊。                       |
| [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | 抓取進程已配置之下一個堆積的相關資訊。                                  |
| [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | 抓取進程已配置之堆積的下一個區塊的相關資訊。                       |
| [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | 抓取與進程相關聯之第一個模組的相關資訊。                                          |
| [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | 抓取與進程或執行緒相關聯之下一個模組的相關資訊。                                 |
| [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | 抓取系統快照中所發生第一個進程的相關資訊。                                  |
| [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | 抓取系統快照中所記錄之下一個進程的相關資訊。                                      |
| [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | 抓取系統快照中所發生之任何進程的第一個執行緒的相關資訊。                    |
| [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | 抓取系統記憶體快照中所發生之任何進程的下一個執行緒的相關資訊。            |
| [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | 將配置給另一個進程的記憶體複製到應用程式提供的緩衝區。                                  |



 

 

 




