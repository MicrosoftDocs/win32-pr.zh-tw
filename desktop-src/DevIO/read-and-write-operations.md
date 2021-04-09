---
description: Windows 支援對序列通訊資源上的同步和非同步 (重迭) 檔案 i/o 作業。
ms.assetid: cee44596-ad73-4afb-b86a-744b0b46d9d5
title: 讀取和寫入作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26cc53dbe8c52286fe53c81202ab3828808b1aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110592"
---
# <a name="read-and-write-operations"></a>讀取和寫入作業

Windows 支援對序列通訊資源上的同步和非同步 (重迭) 檔案 i/o 作業。 當作業在背景中執行時，重迭作業可讓呼叫執行緒執行其他工作。 執行緒使用 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 或 [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) 函式來讀取通訊資源，並使用 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 或 [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) 函式來寫入通訊資源。 **ReadFile** 和 **WriteFile** 可以同步或非同步方式執行。 **ReadFileEx** 和 **WriteFileEx** 只能以非同步方式執行。

這些讀取和寫入函式的行為會受到是否以重迭的作業來執行、超時參數是否與控制碼相關聯，以及流程式控制制參數是否與控制碼相關聯，而受到影響。

執行緒也可以使用 [**TransmitCommChar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar) 函式來寫入通訊資源，此函式會在輸出緩衝區中的任何暫止資料之前傳輸指定的字元。 此函式適用于將高優先順序的信號字元傳送至接收系統。 高優先順序字元的傳輸仍會受到流量控制和寫入超時，而且會以同步的方式執行操作。

執行緒可以使用 [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) 函數來捨棄裝置輸出或輸入緩衝區中的所有字元。 **PurgeComm** 也可以終止暫止的讀取或寫入作業，即使作業尚未完成。 如果執行緒使用 **PurgeComm** 來清除輸出緩衝區，則不會傳送已刪除的字元。 若要在確定傳輸內容時清空輸出緩衝區，執行緒可以呼叫 [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) 函式 () 的同步作業。 不過，請注意， **FlushFileBuffers** 會受限於流量控制，但無法寫入超時時間，而且必須等到所有暫止的寫入作業都經過傳輸之後，才會返回。

 

 
