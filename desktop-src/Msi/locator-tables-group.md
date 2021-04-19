---
description: 定位器資料表群組是用來尋找檔案和應用程式。
ms.assetid: 44ab770b-1a7f-4590-9681-8f6bd343bf86
title: 定位器資料表群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 300a869a912c06b2112476f50bcda021833cfbe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975763"
---
# <a name="locator-tables-group"></a>定位器資料表群組

定位器資料表群組是用來尋找檔案和應用程式。 若要搜尋檔案，請先判斷檔案簽章，然後找出檔案。 定位器資料表是用來搜尋登錄、安裝程式設定資料、樹狀目錄或 .ini 檔案，以取得檔案的唯一簽章。 然後，您可以在簽章 [資料表](signature-table.md) 中檢查檔案簽章，以確定特定檔案確實是正在搜尋的檔案，而不是另一個具有相同名稱的檔案。 如果定位器資料表中的記錄未在簽章資料表中包含索引鍵，則記錄會參考目錄而不是檔案。

您可以透過[元件資料表](component-table.md)的外部索引鍵，在檔案[資料表](file-table.md)中找到控制檔案的元件。 因為每個檔案都屬於一個元件，所以安裝程式會透過元件表格解析檔案的位置。 元件資料表中的外部索引鍵可透過 [目錄資料表](directory-table.md)找到元件的位置。

藉由搜尋組成應用程式的檔案，即可找到應用程式的位置。 安裝程式也提供兩個數據表來搜尋舊版的應用程式： [AppSearch 資料表](appsearch-table.md) 和 [CCPSearch 資料表](ccpsearch-table.md)。

下表構成定位器資料表群組，用來判斷檔案簽章。

-   [RegLocator 資料表](reglocator-table.md)包含搜尋登錄中的檔案或目錄所需的資訊。
-   [IniLocator 資料表](inilocator-table.md)會保存搜尋 .ini 檔案所需的資訊。 .Ini 檔案必須存在於預設的 Microsoft Windows 目錄中。
-   [CompLocator 資料表](complocator-table.md)包含使用安裝程式的設定資料搜尋檔案或目錄所需的資訊。
-   [DrLocator 資料表](drlocator-table.md)包含搜尋目錄樹狀目錄中的檔案或目錄所需的資訊。
-   [AppSearch 資料表](appsearch-table.md)包含必須設定為對應檔案簽章之搜尋結果的屬性。
-   [CCPSearch 資料表](ccpsearch-table.md)包含檔案簽章的清單，其中至少有一個必須存在於使用者電腦上，才能進行合規性檢查程式 (CCP) 。

 

 



