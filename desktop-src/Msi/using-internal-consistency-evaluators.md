---
description: 若要驗證資料庫，請使用特殊的驗證工具，將包含內部一致性評估工具的 .cub 檔案， (等) 併入您的資料庫、執行等，然後報告結果。
ms.assetid: bdf38673-ee3d-47d8-ad6e-562cd5626918
title: 使用內部一致性評估工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e6dab453ae495dc6029b54eb039c8acc60f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973649"
---
# <a name="using-internal-consistency-evaluators"></a>使用內部一致性評估工具

若要驗證資料庫，請使用特殊的驗證工具，將包含 [內部一致性評估](internal-consistency-evaluators-ices.md) 工具的 .cub 檔案， (等) 併入您的資料庫、執行等，然後報告結果。 Microsoft Windows 軟體開發套件 (SDK) 提供許多這類工具。 從協力廠商撰寫環境也可以將 ICE 驗證系統納入其撰寫環境中。 您也可以撰寫自己的工具來執行 ICE 驗證。 大部分的 ICE 驗證工具會將 .cub 檔和您的資料庫合併為第三個暫存資料庫。 Windows Installer 在 .cub 檔案中執行每個 ICE 時，會顯示警告、錯誤、調試資訊和 API 錯誤。 當安裝程式完成執行時，它會關閉 .msi 檔案、.cub 檔和暫存資料庫，而不會儲存任何變更。 此 .msi 檔案和 .cub 檔案會由驗證測試保持不變。

ICE 自訂動作會藉由呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 和張貼 INSTALLMESSAGE 使用者訊息來與使用者通訊 \_ 。 ICE 訊息通常會傳回如下的資訊：

-   發現錯誤的 ICE 名稱
-   ICE 的建立日期
-   ICE 作者
-   ICE 上次修改的日期。
-   導致 ICE 失敗的 API 錯誤描述
-   錯誤的描述
-   使用者的警告
-   包含錯誤或警告的資料庫資料表名稱
-   包含錯誤或警告的資料表資料行名稱
-   包含錯誤或警告的資料表主要索引鍵
-   提供調試建議的 HTML 檔案 URL
-   可能包含其他資訊的字串

安裝套件的作者可以撰寫 ICE 自訂動作，或使用 SDK 隨附的 .cub 檔案中包含的標準一組標準。 如需如何撰寫 ICE 的詳細資訊，請參閱 [建立 ice](building-an-ice.md)。

撰寫適當的 Ices-003 以進行驗證之後，開發人員必須將自訂動作一起收集到 .msi 資料庫（稱為 .cub 檔），其中只包含等位及其所需的資料表。 無法安裝 .cub 檔案，而且只能用來儲存和提供 ICE 自訂動作的存取權。 如需建立 .cub 檔案的詳細資訊，請參閱 [建立 ICE 資料庫](building-an-ice-database.md)。 或者，開發人員可以使用 [ICE 參考](ice-reference.md)中所述的現有內容來驗證其安裝套件。 您可以從 SDK 隨附的標準 .cub 檔案取得這些等。

安裝資料庫資料表編輯器 Orca 或驗證工具 msival2 會提供 .cub、Darice 和 Mergemod 等檔案。 標誌中的一組等量檔案是 Darice 檔中的一組。 如果您的套件使用 Darice 傳遞驗證，它就會以 .cub 來傳遞。 Mergemod 包含一組用來驗證合併模組的一組。 如需詳細資訊，請參閱 [合併模組 ICE 參考](merge-module-ice-reference.md)。

**驗證安裝套件**

1.  取得或撰寫適當的 ICE 自訂動作。 您可以使用 [ICE 參考](ice-reference.md)中所述的一或多個現有的 ices-003。 如果您的驗證需要不在這份清單中的 ICE，您可以建立新的 ICE，如 [建立 ice](building-an-ice.md)所述。
2.  準備包含所有 ICE 自訂動作的 ICE 資料庫。 如需準備 .cub 檔案的相關資訊，請參閱 [建立 ICE 資料庫](building-an-ice-database.md) 一節。
3.  將 .cub 檔案和 .msi 檔案提供給封裝驗證工具，例如 [Orca.exe](orca-exe.md) 或 [Msival2.exe](msival2-exe.md)。

請注意，合併模組應該依照 [驗證合併模組](validating-merge-modules.md)中的說明進行驗證。

 

 



