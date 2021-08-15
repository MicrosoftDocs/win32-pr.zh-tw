---
description: 與多個管道用戶端通訊以及服務多個管道實例的策略。
ms.assetid: c764bde5-e053-4124-b859-1d2839ada918
title: 具名管道實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 188ec90912132e5cdd972ac2b0a4ab3f4c1f97ebbb7bc35e20b75b04eebbfa15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481959"
---
# <a name="named-pipe-instances"></a>具名管道實例

最簡單的管道伺服器會建立一個管道的單一實例、連接到單一用戶端、與用戶端進行通訊、中斷與用戶端的連線、關閉管道控制碼，然後終止。 不過，管道伺服器與多個管道用戶端的通訊比較常見。 管道伺服器可以透過連接到每個用戶端，並從每個用戶端中斷連線，使用單一管道實例連接多個管道用戶端，但效能會變差。 管道伺服器必須建立多個管道實例，才能有效率地同時處理多個用戶端。

有三種基本策略可提供多個管道實例的服務。

-   為每個管道實例建立個別的執行緒。 如需多執行緒管道伺服器的範例，請參閱 [多執行緒管道伺服器](multithreaded-pipe-server.md)。
-   藉由在 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)和 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)函數中指定重迭 [**的結構，**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)來使用重迭的作業。 如需範例，請參閱使用重迭 [i/o 的具名管道伺服器](named-pipe-server-using-overlapped-i-o.md)。
-   使用 [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) 和 [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) 函數來使用重迭的作業，這會指定完成作業時要執行的完成常式。 如需範例，請參閱 [使用完成常式的具名管道伺服器](named-pipe-server-using-completion-routines.md)。

多執行緒管道伺服器最容易寫入，因為每個實例的執行緒都會處理單一管道用戶端的通訊。 系統會視需要將處理器時間分配給每個執行緒。 但每個執行緒都使用系統資源，這是處理大量用戶端之管道伺服器的缺點。

使用單一執行緒的伺服器，可以更輕鬆地協調影響多個用戶端的作業，而且可以更輕鬆地保護共用資源，使其無法同時存取多個用戶端。 單一執行緒伺服器的挑戰是需要協調重迭的作業，以配置處理器時間來處理用戶端的同時需求。

 

 
