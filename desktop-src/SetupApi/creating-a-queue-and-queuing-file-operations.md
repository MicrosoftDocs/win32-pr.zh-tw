---
description: 將檔案作業排入佇列很有用，因為它可讓您處理整個安裝，而不是透過 INF 區段。
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: 建立佇列和佇列檔案作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977996"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a>建立佇列和佇列檔案作業

將檔案作業排入佇列很有用，因為它可讓您處理整個安裝，而不是透過 INF 區段。

若要建立檔案佇列，請宣告變數來儲存佇列控制碼，然後呼叫 [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) 函數。 建立佇列之後，您可以將複製、重新命名和刪除作業排入佇列，以及掃描檔案佇列以驗證已排入佇列的作業。

若要將單一檔案作業加入至佇列，請使用 [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)、 [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)和 [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) 函數。

[ **複製** 檔案]、[ **刪除** 檔案] 或 [ **重新命名** 檔案] 區段中所列的所有檔案作業，都可以分別使用 [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)、 [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)或 [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)新增至佇列。

另一種將 INF **安裝** 區段中所列的 [**複製** 檔案] 區段中的所有檔案排入佇列的另一種方式是使用 [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)函式。

下列範例會使用 [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) 函式，將 INF 檔案的 [ **複製** 檔案] 區段中所列之所有檔案的複製作業排入佇列。

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

在此範例中，MyQueue 是要新增複製作業的佇列，"A： \\ " 指定來源的路徑，而 MyInf 是開啟的 INF 檔案的控制碼。 參數 *ListInfHandle* 設定為 **Null**，表示複製的區段位於 MyInf 中。 MySection 是 MyInf 中的區段，其中包含要排入佇列以供複製的檔案。

旗標 SP \_ 複製 \_ NOSKIP 和 sp \_ 複製 \_ NOBROWSE 已使用 OR 運算子結合，指出如果發生錯誤，則不應提供使用者略過或流覽檔案的選項。

 

 



