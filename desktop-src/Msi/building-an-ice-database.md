---
description: 選取適當的 [驗證] 以進行驗證之後，開發人員必須將自訂動作一起收集到 ICE 資料庫中。
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: 建立 ICE 資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51043aa9b3c1591fa3262492c117aba35f23d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848945"
---
# <a name="building-an-ice-database"></a>建立 ICE 資料庫

選取 [適當的](internal-consistency-evaluators-ices.md) [驗證] 以進行驗證之後，開發人員必須將自訂動作一起收集到 ICE 資料庫中。 .Cub 檔案是標準 .msi 資料庫，其中只包含 Ices-003 和其所需的資料表。 無法安裝 .cub 檔案，而且只能用來儲存和提供 ICE 自訂動作的存取權。

.Cub 檔案包含下列資料庫資料表。



| 資料表                                  | 描述                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [二進位](binary-table.md)             | CustomAction 資料表中所參考之 ICE 海關動作的腳本檔案、Dll 和 Exe。                                                                                                                                                                 |
| [CustomAction](customaction-table.md) | 這個資料表中的每一筆記錄都會對應到 .cub 檔中所包含的 ICE 自訂動作。                                                                                                                                                                                   |
| \_ICESequence                          | 下表列出在其執行順序中，.cub 檔中所包含的 ICE 海關動作。 此表格中所列的 ICE 自訂動作會藉由呼叫 [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)來執行，或使用 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)個別執行。 |
| [\_驗證](-validation-table.md)  | 此資料表包含要合併至驗證資料表的 .cub 檔專案。 \_                                                                                                                                                                               |
| \_特殊                              | 特定 ICE 自訂動作所需的任何特殊處理資料表，都必須包含在 .cub 檔案中。 這些資料表的名稱必須有前置底線。                                                                                                        |



 

請參閱 [範例 .cub](sample--cub-file.md)檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[打造冰](building-an-ice.md)
</dt> </dl>

 

 



