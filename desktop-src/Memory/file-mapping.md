---
description: 檔案對應是檔案內容與進程虛擬位址空間之一部分的關聯。
ms.assetid: 86a8bc81-914d-46a2-99fd-65dfd03bbcdd
title: 檔案對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8efa02b7de4565adc6ec9cc4c252a7b3114169f1897a2950340a492035409008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067850"
---
# <a name="file-mapping"></a>檔案對應

檔案 *對應* 是檔案內容與進程虛擬位址空間之一部分的關聯。 系統會建立檔案 *對應物件* (也稱為 *區段物件*) 來維護此關聯。 檔案 *視圖* 是進程用來存取檔案內容的虛擬位址空間部分。 檔案對應可讓進程同時使用隨機輸入和輸出 (i/o) 和連續 i/o。 它也可讓程式有效率地處理大型資料檔案（例如資料庫），而不需要將整個檔案對應到記憶體。 多個進程也可以使用記憶體對應檔案來共用資料。

進程會使用指標來讀取和寫入檔案視圖，就像使用動態配置的記憶體一樣。 使用檔案對應可提升效率，因為檔案位於磁片上，但是檔案視圖位於記憶體中。 處理常式也可以使用 [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) 函式來操作檔案視圖。

下圖顯示磁片上的檔案、檔案對應物件和檔案視圖之間的關聯性。

![磁片上的檔案、檔案對應物件和檔案視圖之間的關聯性。](images/fmap.png)

磁片上的檔案可以是您想要對應到記憶體中的任何檔案，也可以是系統分頁檔案。 檔案對應物件可以包含全部或只包含部分檔案。 它是由磁片上的檔案所支援。 這表示當系統交換檔案對應物件的頁面時，對檔案對應物件所做的任何變更都會寫入至檔案。 當檔案對應物件的頁面換回時，會從檔案還原它們。

檔案視圖可以包含全部或只包含檔案對應物件的一部分。 程式會透過檔案視圖來操作檔案。 進程可以建立檔案對應物件的多個視圖。 每個處理常式所建立的檔案視圖都位於該進程的虛擬位址空間中。 當進程需要來自檔案一部分以外的資料，而不是目前檔案視圖中的資料時，它可以取消目前的檔案視圖的對應，然後建立新的檔案視圖。

當多個進程使用相同的檔案對應物件來建立本機檔案的視圖時，資料是一致的。 也就是，這些視圖包含磁片上相同的檔案複本。 如果您想要在多個進程之間共用記憶體，檔案不能位於遠端電腦上。

如需詳細資訊，請參閱下列主題：

-   [建立檔案對應物件](creating-a-file-mapping-object.md)
-   [建立檔案視圖](creating-a-file-view.md)
-   [共用檔案和記憶體](sharing-files-and-memory.md)
-   [從檔案視圖讀取和寫入](reading-and-writing-from-a-file-view.md)
-   [關閉檔案對應物件](closing-a-file-mapping-object.md)
-   [檔案對應安全性和存取權限](file-mapping-security-and-access-rights.md)
-   [使用檔案對應](using-file-mapping.md)

 

 
