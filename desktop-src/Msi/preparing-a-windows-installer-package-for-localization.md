---
description: 遵循這些指導方針，以促進 Windows Installer 套件的當地語系化。
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: 準備 Windows Installer 套件以進行當地語系化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972160"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a>準備 Windows Installer 套件以進行當地語系化

您可以執行下列動作，以大幅促成將 Windows Installer 封裝當地語系化為多種語言：

-   撰寫以字碼頁中立的基礎安裝資料庫。 請參閱 [使用中性程式碼建立資料庫頁面](creating-a-database-with-a-neutral-code-page.md)。 然後，您可以將具有非中性字碼頁的文字保存資料表匯入至基底資料庫，以設定當地語系化資料庫的字碼頁。 請參閱 [設定資料庫的字碼頁](setting-the-code-page-of-a-database.md)。
-   將需要當地語系化的檔案組織成個別的元件，並將這些檔案安裝在不同的目錄中。 這可確保兩個當地語系化的封裝永遠不會在相同的目錄中安裝相同的命名檔案。

例如，使用下列資源的全球應用程式可能會有三個元件。



| 元件 | 資源                   |
|-----------|----------------------------|
| 世界     | worldwide.exe              |
| 世界     | 全球登錄專案 |
| 世界     | 全球快速鍵         |
| ENG       | engui.dll                  |
| ENG       | readme.txt                 |
| FRA       | fraui.dll                  |
| FRA       | readme.txt                 |



 

需要當地語系化的檔案可能會安裝到下列目錄位置：

-   \[ProgramFilesFolder \] \\ World \\worldwide.exe
-   \[ProgramFilesFolder \] \\ World \\ 英文 \\engui.dll
-   \[ProgramFilesFolder \] \\ World \\ 英文 \\readme.txt
-   \[ProgramFilesFolder \] \\ World \\ 法文 \\fraui.dll
-   \[ProgramFilesFolder \] \\ World \\ 法文 \\readme.txt

 

 



