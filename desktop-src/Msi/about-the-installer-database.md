---
description: Windows Installer 資料庫是由許多相關的資料表組成，其中包含安裝一組應用程式所需資訊的關係資料庫。
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: 關於安裝程式資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848999"
---
# <a name="about-the-installer-database"></a>關於安裝程式資料庫

Windows Installer 資料庫是由許多相關的資料表組成，其中包含安裝一組應用程式所需資訊的關係資料庫。 因為資料庫是關聯式的，所以資料表會透過主鍵和外鍵值中的資料進行連結。 這提供了一種有效的方法來變更安裝程式，並表示使用者可以更輕鬆地自訂大型應用程式或應用程式群組。 資料庫資料表會反映整個應用程式群組的一般版面配置，包括：

-   可用的功能
-   單元
-   功能與元件之間的關聯性
-   必要的登錄設定
-   應用程式的使用者介面

若要建立安裝資料庫，您必須在資料表中填入應用程式和安裝程式的所有相關資訊。 即使是中等大小的安裝，手動編寫所有這些資料表都會變成大型工作;因此，有一些協力廠商工具可協助您建立安裝程式資料庫。 下列各節說明相關資料庫資料表的群組。

[核心資料表群組](core-tables-group.md)

[檔案資料表群組](file-tables-group.md)

[登錄資料表群組](registry-tables-group.md)

[系統資料表群組](system-tables-group.md)

[定位器資料表群組](locator-tables-group.md)

[程式資訊資料表群組](program-information-tables-group.md)

[安裝程式資料表群組](installation-procedure-tables-group.md)

[實體關聯性圖表圖例](entity-relationship-diagram-legend.md)

[壓縮檔案](text-archive-files.md)

如需安裝資料庫中所有資料表的完整清單，請參閱 [資料庫資料表](database-tables.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



