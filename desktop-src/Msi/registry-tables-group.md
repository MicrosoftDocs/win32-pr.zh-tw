---
description: Windows Installer 資料表的登錄群組包含登錄專案的相關資訊。
ms.assetid: 31a75c20-79e4-4bcf-bcc1-34a7d191fa90
title: 登錄資料表群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba14bdc2bc5668ce2de3ec66172c75c176ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849150"
---
# <a name="registry-tables-group"></a>登錄資料表群組

![登錄資料表群組](images/registry.png)

如需此圖表的詳細資訊，請參閱 [實體關聯性圖表圖例](entity-relationship-diagram-legend.md)。

安裝程式會針對不同類型的登錄專案提供特定的資料表。 擴展登錄資料表群組時，請務必嘗試將放置於登錄 [資料表](registry-table.md) 中的專案數目降至最低，並充分利用其他、特定的登錄資料表。 這是因為安裝程式無法區別登錄表中不同類型的登錄專案，而且無法使用充分利用所有安裝程式功能的必要內部邏輯，例如 [*廣告*](a-gly.md)。 以這種方式撰寫 COM 和 shell 相關的登錄專案也可提供更多邏輯組織，並可協助將 COM 伺服器資訊的錯誤註冊降至最低。

下圖顯示資料表的登錄專案群組，以及 [元件資料表](component-table.md)、 [功能資料表](feature-table.md)和檔案 [資料表](file-table.md)。 雖然後者不會直接參與登錄登錄，但因為它們對於登錄專案群組的邏輯而言是不可或缺的，所以會包含在圖形中。

登錄專案群組包含下列特定登錄專案的表格。

-   [延伸模組資料表](extension-table.md)包含您的應用程式使用的所有副檔名，以及其相關聯的功能和元件。
-   [動詞資料表](verb-table.md)會將命令動詞資訊與[延伸模組資料表](extension-table.md)中所列的副檔名產生關聯。 這會在功能公告所需的動詞和 Feature 資料表之間提供間接連結。
-   [TypeLib 資料表](typelib-table.md)提供安裝程式放置於登錄中的資訊，以便註冊類型程式庫。 類型程式庫專案不會在廣告時寫入。 安裝程式會在安裝程式庫相關聯的元件時，寫入類型程式庫專案。
-   [Mime 資料表](mime-table.md)會將 mime 內容類型與 CLSID 或副檔名產生關聯。 這會提供功能公告所需的 MIME 和功能資料表之間的路徑。
-   [SelfReg 資料表](selfreg-table.md)提供自行註冊模組所需的資訊。 安裝程式只會提供自我註冊，以提供回溯相容性，而且不建議用來填入登錄的方法，不過，如果您的應用程式中有任何必須自行註冊的模組，請使用 SelfReg 資料表。
-   [類別資料表](class-table.md)是用來註冊 COM 物件的類別識別碼和其他資訊。 此資料表包含必須在產品公告中產生的 COM 伺服器相關資訊。
-   [ProgId 資料表](progid-table.md)會將程式識別碼與類別識別碼產生關聯。
-   [AppId 資料表](appid-table.md)可用於註冊 DCOM 物件的一般安全性和設定。
-   環境 [資料表](environment-table.md) 是用來設定環境變數的值，而在 Windows 2000 中，環境資料表也會寫入至登錄。
-   登錄 [資料表](registry-table.md) 會保存應用程式必須放入系統登錄中的任何其他資訊。 這會包含上述資料表不支援的預設設定、使用者資訊或資料，或 COM 註冊。
-   [RemoveRegistry 資料表](removeregistry-table.md)包含應用程式在安裝時需要從系統登錄刪除的登錄資訊。

 

 



