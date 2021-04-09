---
description: 預設佇列回呼常式會以一般方式處理 SetupCommitFileQueue 所傳送的通知。
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: 關於預設佇列回呼常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847921"
---
# <a name="about-the-default-queue-callback-routine"></a>關於預設佇列回呼常式

預設佇列回呼常式會以一般方式處理 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 所傳送的通知。 您可以使用預設常式取得現成的使用者介面，以建立一般安裝程式對話方塊。 建議您使用預設佇列回呼常式（兩者都可方便使用），並確保在安裝期間所產生之對話方塊的外觀和行為都一致。

預設回呼常式需要內部記錄保留的內容結構。 此外，佇列會在一組參數（ *Param1* 和 *Param2*）中傳遞與目前通知相關的其他資訊。

例如，如果佇列將 SPFILENOTIFY \_ NEEDMEDIA 通知傳送至預設回呼常式，則 *Param1* 會指向 [**來源 \_ 媒體**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) 結構，其中包含所需媒體的相關資訊， *Param2* 指向可以接收使用者新路徑資訊的字元陣列。

預設回呼常式會使用這項資訊來提示使用者插入所需的來源媒體、指定新路徑、略過複製目前的檔案，或取消目前的操作。 根據使用者採取的動作而定，預設佇列回呼常式會傳回 FILEOP \_ NEWPATH、FILEOP \_ DOIT R、FILEOP \_ SKIP 或 FILEOP \_ ABORT 給佇列。

如需預設佇列回呼常式如何處理每個佇列通知的詳細資訊，請參閱檔案 [佇列通知](file-queue-notifications.md)。

如需自訂佇列回呼常式的詳細資訊，請參閱 [建立自訂佇列回呼常式](creating-a-custom-queue-callback-routine.md)。

 

 



