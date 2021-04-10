---
description: 動作會封裝在安裝或維護應用程式期間執行的一般功能。 Windows Installer 有許多內建的標準動作。 安裝套件的開發人員也可以撰寫自己的自訂動作。
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: 標準動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ed4f9c2a7fc6671442f6b72cd10889e2fcf5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192306"
---
# <a name="standard-actions"></a>標準動作

動作會封裝在安裝或維護應用程式期間執行的一般功能。 Windows Installer 有許多內建的標準動作。 安裝套件的開發人員也可以撰寫自己的 [自訂動作](custom-actions.md)。

安裝程式標準動作的範例包括：

-   [CreateShortcuts 動作](createshortcuts-action.md)：管理與目前應用程式一起安裝之檔案的快捷方式建立。 此動作會使用 [快速鍵表格](shortcut-table.md) 來取得其資料。
-   [InstallFiles 動作](installfiles-action.md)：將選取的檔案從來源目錄複寫到目的地目錄。 此動作會使用 [File 資料表](file-table.md) 來取得其資料。
-   [WriteRegistryValues 動作](writeregistryvalues-action.md)：設定應用程式在登錄中所需的登錄資訊。 此動作會使用登錄 [資料表](registry-table.md) 來取得其資料。

下列各節將討論標準動作。

-   [關於標準動作](about-standard-actions.md)
-   [使用標準動作](using-standard-actions.md)
-   [標準動作參考](standard-actions-reference.md)

 

 



