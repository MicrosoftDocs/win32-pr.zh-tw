---
description: 當 SetupCommitFileQueue 函式認可檔案佇列時，它會依下列連續處理檔案作業：檔案刪除作業、檔案重新命名作業，最後是檔案複製作業。
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: 佇列承諾的順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f261b1e42631e35146dc3d11f848ff543c999c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849600"
---
# <a name="order-of-queue-commitment"></a>佇列承諾的順序

當 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 函式認可檔案佇列時，它會依下列連續處理檔案作業：檔案刪除作業、檔案重新命名作業，最後是檔案複製作業。 下列大綱說明佇列的承諾用量流程的生命週期。

 

-   啟動刪除子佇列
    -   開始 < 的檔案刪除作業--為每個作業重複
    -   完成檔案刪除作業 <--已排入佇列的檔案刪除
-   完成刪除子佇列

<!-- -->

-   啟動重新命名子佇列
    -   開始重新命名作業 <--為每個動作重複
    -   完成檔案刪除作業 <--已排入佇列的檔案重新命名
-   完成重新命名子佇列

<!-- -->

-   啟動複製 subque
    -   開始檔案複製作業 <--為每個作業重複
    -   完成檔案複製作業 <--已排入佇列的檔案複製
    -   完成複製子佇列
-   完成佇列

 

在每個步驟中，或如果發生錯誤， [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 函式會將通知傳送給回呼常式。 回呼常式可以使用佇列所傳送的資訊來追蹤安裝進度，並視需要與使用者互動。

例如，如果檔案複製作業需要目前路徑無法使用的原始程式檔， [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 會將 SPFILENOTIFY \_ NEEDMEDIA 通知傳送給回呼常式，以及所需的檔案和媒體的相關資訊。 回呼常式可以使用此資訊來產生對話方塊，以提示使用者透過呼叫 SetupPromptForDisk 來插入下一個磁片[ ](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)

預設佇列回呼常式 [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)會隨附于安裝程式 API。 此常式會處理佇列通知，並產生安裝的錯誤對話方塊和進度列。 您可以使用預設佇列回呼常式，或撰寫篩選回呼常式來處理通知的子集，並將其他通知傳遞至預設佇列回呼常式。

如果回呼常式的任何功能都不符合您的需求，您可以撰寫獨立的自訂回呼常式，而不會呼叫預設佇列回呼常式。

如需佇列回呼常式的詳細資訊，請參閱 [預設佇列回呼常式](default-queue-callback-routine.md)和 [建立自訂佇列回呼常式](creating-a-custom-queue-callback-routine.md)。

 

 



