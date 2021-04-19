---
description: 下列函式會與檔案佇列一起使用。
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: 檔案佇列函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acaf1fb1fbd2dc4f020577a1ae68d6ec9b2e95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000296"
---
# <a name="file-queue-functions"></a>檔案佇列函式

下列函式會與檔案佇列一起使用。



| 函式                                                             | 描述                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | 終止佇列。 未認可任何剩餘的交易。                                   |
| [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | 認可所有已排入佇列的交易。                                                                      |
| [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | 初始化並傳回檔案佇列的控制碼。                                                   |
| [**SetupPromptReboot**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | 視需要提示使用者重新開機電腦。                                         |
| [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | 將檔案複製排在佇列中。                                                                                   |
| [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | 將 [INF 複製檔案] 區段中的檔案排入佇列。                                                        |
| [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | 使用 INF 檔案中指定的預設資訊，將 INF 複製檔案區段中的檔案排入佇列。 |
| [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | 將檔案刪除排在佇列中。                                                                               |
| [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | 將 INF [刪除檔案] 區段中的檔案排入佇列。                                                      |
| [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | 將檔案重新命名為佇列。                                                                                 |
| [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | 在 [INF 重新命名檔案] 區段中將檔案排入佇列。                                                      |
| [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | 掃描檔案佇列。                                                                                 |
| [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | 設定平臺路徑覆寫。                                                                      |



 

 

 



