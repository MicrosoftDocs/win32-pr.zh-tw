---
description: 郵筒是位於記憶體中的 pseudofile，而且您會使用標準的檔案函式來存取它。
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: 關於 Mailslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd83fc0d952577efdb149d4c7f25fffbab9784f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997272"
---
# <a name="about-mailslots"></a>關於 Mailslots

郵筒是位於記憶體中的 pseudofile，而且您會使用標準的檔案函式來存取它。 郵筒訊息中的資料可以是任何形式，但在電腦之間傳送時不能大於424位元組。 不同于磁片檔案，mailslots 是暫時性的。 當郵筒的所有控制碼都關閉時，會刪除信箱和其包含的所有資料。

*郵筒伺服器* 是建立並擁有郵筒的進程。 當伺服器建立信箱時，它會接收信箱控制碼。 當進程從郵件傳送程式讀取訊息時，必須使用這個控制碼。 只有建立郵筒的進程，或已透過其他機制取得控制碼 (例如繼承) 可以從信箱讀取。 所有的 mailslots 都是建立它們的進程的本機。 進程無法建立遠端郵筒。

*郵筒用戶端* 是將訊息寫入郵筒的進程。 任何具有信箱名稱的進程都可以在該處放入訊息。 新的訊息會在信箱中的任何現有訊息之後。

Mailslots 可以廣播網域內的訊息。 如果網域中的數個進程每個都使用相同的名稱來建立一個信箱，則參與的進程就會收到每個定址至該信箱並傳送至網域的訊息。 因為一個進程可以同時控制伺服器信箱控制碼和用戶端控制碼，當打開封入器開啟進行寫入作業時，應用程式可以輕鬆地在網域內執行簡單的訊息傳遞功能。

若要在電腦之間傳送大於424位元組的訊息，請改用 [具名管道](named-pipes.md) 或 [Windows 通訊端](/windows/desktop/WinSock/windows-sockets-start-page-2) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[郵筒名稱](mailslot-names.md)
</dt> <dt>

[郵筒作業](mailslot-operations.md)
</dt> </dl>

 

 
