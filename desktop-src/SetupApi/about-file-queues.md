---
description: 檔案佇列是一種檔案作業清單，會一次處理。 佇列中的檔案作業可能是複製、重新命名或刪除作業。 檔案佇列會依類型來組織檔案作業，建立複製、重新命名和刪除子佇列。
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: 關於檔案佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970976"
---
# <a name="about-file-queues"></a>關於檔案佇列

檔案佇列是一種檔案作業清單，會一次處理。 佇列中的檔案作業可能是複製、重新命名或刪除作業。 檔案佇列會依類型來組織檔案作業，建立複製、重新命名和刪除子佇列。

這些作業可能會以任何順序傳送至佇列，而佇列進程不需要連續。 認可佇列時， [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 函式會依作業類型的順序來執行檔案作業。

一般來說，整個安裝所需的所有檔案作業都會排入檔案佇列中，然後在認可佇列時，于單一批次中處理。

從 INF 檔案依區段將檔案作業排入佇列的優點之一，是您可以簡化安裝程式。 您可以在建立佇列時，從使用者取得安裝資訊，以取得要安裝的所有檔案，而不需要為每個要安裝的區段取得資訊。 如此一來，當 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 函式處理時間密集的複製作業時，使用者就可以釋出其他活動。

檔案佇列的另一個優點是您可以追蹤整個安裝的進度。 從 INF 檔案逐步安裝區段時，進度列之類的進度指示器只會追蹤目前的 INF 區段。 安裝下一個區段時，進度列就會從頭開始。 使用佇列時，在認可佇列之前，會先知道要在整個安裝期間處理的檔案總數，因此可以產生進度列來追蹤整個安裝。

如需詳細資訊，請參閱下列主題：

-   [佇列承諾的順序](order-of-queue-commitment.md)
-   [佇列通知](queue-notifications.md)

 

 



