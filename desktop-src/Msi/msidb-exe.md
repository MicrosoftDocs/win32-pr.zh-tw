---
description: Msidb.exe 會使用 MsiDatabaseImport 和 MsiDatabaseExport 來匯入和匯出資料庫資料表和資料流程。
ms.assetid: 2eee535f-e7f6-4e1a-9667-df4b8067b132
title: Msidb.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86f2e1fa6a1cf1a9dc8a01b9f9d6542607dd9275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978002"
---
# <a name="msidbexe"></a>Msidb.exe

Msidb.exe 會使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) 和 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) 來匯入和匯出 [資料庫資料表](database-tables.md) 和資料流程。

如果在命令列上指定了模式、資料夾、資料庫和資料表清單，Msidb.exe 不會顯示任何使用者介面，而是以無訊息命令列公用程式的形式運作，以用於組建腳本。

## <a name="syntax"></a>Syntax

**MsiDb** *{option} ***...**_{option}_*_..._* * {table} ***...**_{table}_

## <a name="command-line-options"></a>命令列選項

Msidb.exe 會使用下列不區分大小寫的命令列選項。 斜線分隔符號也可以用來取代虛線。



| 選項 | Description                                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -i     | 從資料夾將文字封存檔匯入至資料庫。 匯入資料表名稱的檔案名為8個字元，副檔名為 "idt"。 如果匯入命令提供了較長的名稱，則會截斷為8個字元。 您可以使用標準萬用字元規格。                                                                 |
| -E     | 將選取的資料表從資料庫匯出至資料夾中的文字保存檔案。 匯出的資料表名稱是資料表名稱。 只可以使用萬用字元規格 " \* "。 資料表可以從唯讀資料庫匯出。                                                                                                               |
| -c     | 建立新的資料庫檔案，並匯入資料表。 覆寫現有的資料庫檔案。                                                                                                                                                                                                                                               |
| -f     | 指定包含資料表和資料流程之文字封存檔案的資料夾。 如果未指定包含文字封存檔案的資料夾，則公用程式會提示使用者輸入資料夾。                                                                                                                                       |
| -d     | 資料庫檔案的完整路徑。                                                                                                                                                                                                                                                                                          |
| -M     | 要合併之資料庫的完整路徑。 此選項僅適用于無訊息命令列模式。 此選項的多個實例最多可能會有10個。 如果未在命令列上指定資料庫，公用程式會提示使用者輸入資料庫。                                       |
| -t     | 要套用之轉換的完整路徑。 此選項僅適用于無訊息命令列模式。 此選項的多個實例最多可能會有10個。                                                                                                                                                     |
| -j     | 要從資料庫移除的儲存體名稱。 此選項僅適用于無訊息命令列模式。 此選項的多個實例最多可能會有10個。                                                                                                                                                             |
| -k     | 要從資料庫移除的資料流程名稱。 此選項僅適用于無訊息命令列模式。 此選項的多個實例最多可能會有10個。                                                                                                                                                                 |
| -X     | 要儲存到目前目錄中之磁片檔案的資料流程名稱。 此選項僅適用于無訊息命令列模式。 二進位資料串流會儲存為副檔名為 ". ibd" 的個別檔案。 使用的二進位檔案名是包含資料流程之資料列的主鍵資料。                                                  |
| -w     | 要儲存到目前的目錄中之磁片檔案的儲存體名稱。 此選項僅適用于無訊息命令列模式。                                                                                                                                                                                                         |
| -a     | 要新增至資料庫做為資料流程的檔案名。 此選項僅適用于無訊息命令列模式。 此選項的多個實例最多可能會有10個。 二進位資料串流會儲存為副檔名為 ". ibd" 的個別檔案。 使用的二進位檔案名是包含資料流程之資料列的主鍵資料。 |
| -r     | 要加入至資料庫做為 substorage 的儲存體名稱。 此選項僅適用于無訊息命令列模式。 此選項的多個實例最多可能會有10個。                                                                                                                                                     |
| -S     | 將資料表名稱截斷為匯出至 idt 的8個字元。 資料表名稱會截斷為8個字元，並加入副檔名 ". idt"。                                                                                                                                                                                           |
| -?     | 顯示命令列說明對話方塊                                                                                                                                                                                                                                                                                               |



 

> [!Note]  
> 使用含有空格的長檔名時，請使用引號括住。 例如，針對位於 "我的檔" 資料夾的資料庫，請將它指定為「c：我的 \\ 文檔」。

 

此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 開發工具](windows-installer-development-tools.md)
</dt> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



