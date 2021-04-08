---
title: 舊版系統還原參考
description: 本檔說明舊版系統還原所使用的儲存機制的執行詳細資料。 它並不適用于 Windows Vista 上的系統還原執行。
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839343"
---
# <a name="legacy-system-restore-reference"></a>舊版系統還原參考

\[此資訊只適用于 Windows XP Service Pack 2 (SP2) 。\]

本檔說明舊版系統還原所使用的儲存機制的執行詳細資料。 它並不適用于 Windows Vista 上的系統還原執行。

## <a name="system-restore-repository-structure"></a>系統還原存放庫結構

Windows XP （含 SP2）包含下列資料夾中系統還原的儲存機制：% SYSTEMDRIVE% \\ 系統磁碟區資訊。 此存放庫包含還原點的資訊，基本上是系統的快照集。

存放庫的結構如下：

**系統磁碟區資訊**    ** \_ 還原 {*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **rp * n** *     ** \_ restore {*GUID*}**       **RP1**       **RP2**       **RP *n-1*-1**       **RP * n***

若要判斷 \_ 要使用哪一個 restore {*GUID*} 資料夾，請閱讀下列檔案中指定的 **GUID** ： SYSTEMROOT% \\ System32 \\ restore \\MachineGUID.txt。

在每個 \_ restore {*GUID*} 資料夾中，driver .config 檔案 \_ 包含的資訊來自于定義如下的 **sr-iov \_ 持續 \_** 設定結構：

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a>每個 RP *n* 資料夾中包含的檔案

每個 RP *n* 資料夾都包含快照集資料夾，其中包含下列各項：

-   登錄 hive 的快照
-   包含 WMI 存放庫快照集的存放庫資料夾
-   COM + 資料庫的快照集
-   IIS 資料庫的快照集

每個 RP *n* 資料夾都包含一個 rp .log 檔案，其中包含來自 [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) 結構之還原點的一般資訊。

每個 RP *n* 資料夾都可能包含用來追蹤還原點變更的檔案。 第一個檔案的名稱為 change .log，下一個檔案的名稱為 change .log。 每個變更記錄檔都包含下列結構：

-   [**變更 \_ 記錄 \_ 標頭**](change-log-header.md)
-   [**變更 \_記錄 \_ 專案**](change-log-entry.md)1
-   [**變更 \_記錄 \_ 專案**](change-log-entry.md)2
-   ...
-   [**變更 \_記錄 \_ 專案**](change-log-entry.md)*n*

## <a name="related-topics"></a>相關主題

<dl> <dt>

[舊版系統還原結構](legacy-system-restore-structures.md)
</dt> </dl>

 

 




