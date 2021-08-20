---
description: 連鎖的單向連結清單 (SList) 可簡化從連結清單插入和刪除的工作。
ms.assetid: 35463ace-33ab-4eb9-9901-2504a92456e2
title: 連鎖單向連結清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c938abc7059ad73bac5d3f3a7df4b1d2cb97bacf86346ffdaa752ecc9cf11bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959255"
---
# <a name="interlocked-singly-linked-lists"></a>連鎖單向連結清單

*連鎖的單向連結清單* (SList) 可簡化從連結清單插入和刪除的工作。 SLists 是使用非封鎖演算法來執行，以提供不可部分完成的同步處理、提高系統效能，並避免發生優先順序反轉和鎖定群組等問題。

SLists 可直接在32位程式碼中執行和使用。 不過，在64位程式碼中執行它們是很困難的，因為原生連鎖交換基本專案所交換的資料量不是位址大小的兩倍，因為它是在32位程式碼中。 因此，SLists 可以將高階可調整演算法移植至 Windows。

**Windows 8：** 從 Windows 8 開始，適當的原生連鎖交換基本專案適用于64位程式碼，例如 [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85))。

應用程式可以透過呼叫 [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead) 函式來初始化清單的開頭，以使用 SLists。 若要將專案插入清單中，請使用 [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist) 函數。 若要從清單中刪除專案，請使用 [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist) 函數。

所有清單專案都必須在 **記憶體 \_ 配置 \_ 對齊** 界限上對齊。 未對齊的專案可能會導致無法預期的結果。 請參閱 **\_ 對齊的 \_ malloc**。

如需範例，請參閱 [使用單一連結清單](using-singly-linked-lists.md)。

下表列出 SList 函數。



| 函式                                                         | 描述                                                                                                                                               |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead)               | 初始化單一連結清單的標頭。                                                                                                             |
| [**InterlockedFlushSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedflushslist)           | 清除單一連結清單中的整個專案清單。                                                                                                 |
| [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)     | 移除單一連結清單前面的專案。                                                                                                   |
| [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)   | 將專案插入單向連結清單的前面。                                                                                                     |
| [**InterlockedPushListSList**](/previous-versions/windows/desktop/legacy/hh448545(v=vs.85))     | 在另一個單一連結清單的前方插入單一連結清單。                                                                                  |
| [**InterlockedPushListSListEx**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex) | 在另一個單一連結清單的前方插入單一連結清單。 此版本的方法不會使用 **\_ \_ fastcall** 呼叫慣例。 |
| [**RtlFirstEntrySList**](/windows/desktop/api/WinNT/nf-winnt-rtlfirstentryslist)                 | 抓取單一連結清單中的第一個專案。                                                                                                        |
| [**QueryDepthSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-querydepthslist)                       | 抓取指定的單向連結清單中的專案數。                                                                                      |



 

 

 
