---
description: 下列通知會與檔案佇列一起使用。 如需有關通知格式和使用的詳細資訊，請參閱通知。
ms.assetid: 4a171b4a-8623-4be3-81ee-99081fe23034
title: 檔案佇列通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b674dee015c4c9408ff5dc853d5d3b2412e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027084"
---
# <a name="file-queue-notifications"></a>檔案佇列通知

下列通知會與檔案佇列一起使用。 如需有關通知格式和使用的詳細資訊，請參閱 [通知](notifications.md)。



| 通知                                                      | Description                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md)         | 檔案複製作業期間發生錯誤。                                                  |
| [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)     | 檔案刪除作業期間發生錯誤。                                                 |
| [**SPFILENOTIFY \_ ENDCOPY**](spfilenotify-endcopy.md)             | 檔案複製作業已結束。                                                                 |
| [**SPFILENOTIFY \_ ENDDELETE**](spfilenotify-enddelete.md)         | 檔案刪除操作已結束。                                                                |
| [**SPFILENOTIFY \_ ENDQUEUE**](spfilenotify-endqueue.md)           | 佇列已完成認可。                                                                  |
| [**SPFILENOTIFY \_ ENDRENAME**](spfilenotify-endrename.md)         | 檔案重新命名作業已結束。                                                                  |
| [**SPFILENOTIFY \_ ENDSUBQUEUE**](spfilenotify-endsubqueue.md)     | 子佇列 (複製、重新命名或刪除) 已結束。                                               |
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md) | 檔案已在使用中，而且目前的操作已延遲，直到系統重新開機為止。       |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)   | 目前操作的語言與系統語言不符。                           |
| [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md)         | 需要新的來源媒體。                                                                         |
| [**SPFILENOTIFY \_ QUEUESCAN**](spfilenotify-queuescan.md)         | 已掃描檔案佇列中的節點。  ( 僅限 [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea))  |
| [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md)     | 檔案重新命名作業期間發生錯誤。                                                 |
| [**SPFILENOTIFY \_ STARTCOPY**](spfilenotify-startcopy.md)         | 檔案複製作業已啟動。                                                                  |
| [**SPFILENOTIFY \_ STARTDELETE**](spfilenotify-startdelete.md)     | 檔案刪除作業已啟動。                                                                |
| [**SPFILENOTIFY \_ STARTQUEUE**](spfilenotify-startqueue.md)       | 佇列已開始認可。                                                                    |
| [**SPFILENOTIFY \_ STARTRENAME**](spfilenotify-startrename.md)     | 檔案重新命名作業已啟動。                                                                |
| [**SPFILENOTIFY \_ STARTSUBQUEUE**](spfilenotify-startsubqueue.md) | 子佇列 (複製、重新命名或刪除) 已開始。                                             |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)   | 目標上已有指定檔案的複本。                                          |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)     | 目標上有較新版本的指定檔案。                                         |



 

 

 



