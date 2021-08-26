---
description: 具名管道是管道伺服器與一或多個管道用戶端之間通訊的已命名單向或雙工管道。
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: 具名管道
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06e7f291776e2ecba3b9da93a94d235d4fbe7df151353a7c3d379eb4d50fdd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014898"
---
# <a name="named-pipes"></a>具名管道

*具名管道* 是管道伺服器與一或多個管道用戶端之間通訊的已命名單向或雙工管道。 具名管道的所有實例都共用相同的管道名稱，但每個實例都有自己的緩衝區和控制碼，並為用戶端/伺服器通訊提供個別的管道。 使用實例可讓多個管道用戶端同時使用相同的具名管道。

任何程式都可以存取具名管道（受限於安全性檢查），使具名管道成為相關或不相關進程之間的簡單通訊形式。

任何程式都可以同時作為伺服器和用戶端，以進行對等通訊。 如這裡所用，「管道伺服器」一詞是指建立具名管道的進程，而「管道用戶端」一詞是指連接到具名管道實例的進程。 用來具現化具名管道的伺服器端函式為 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)。 用於接受連接的伺服器端函數是 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)。 用戶端進程會使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 或 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 函式連接到具名管道。

具名管道可用來提供相同電腦上的處理常式或網路上不同電腦上的進程之間的通訊。 如果伺服器服務正在執行，則所有具名管道都可從遠端存取。 如果您想要在本機使用具名管道，請拒絕存取 NT 授權單位 \\ 網路或切換至本機 RPC。

如需詳細資訊，請參閱下列主題：

-   [管道名稱](pipe-names.md)
-   [具名管道開啟模式](named-pipe-open-modes.md)
-   [具名管道類型、讀取和等候模式](named-pipe-type-read-and-wait-modes.md)
-   [具名管道實例](named-pipe-instances.md)
-   [具名管道作業](named-pipe-operations.md)
-   [同步和重迭的輸入和輸出](synchronous-and-overlapped-input-and-output.md)
-   [具名管道安全性和存取權限](named-pipe-security-and-access-rights.md)
-   [模擬具名管道用戶端](impersonating-a-named-pipe-client.md)
-   [使用管道](using-pipes.md)

 

 
