---
description: 安裝程式會將安裝目錄結構的相關資訊保留在目錄資料表中。
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: 指定目錄結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848186"
---
# <a name="specifying-directory-structure"></a>指定目錄結構

安裝程式會將安裝目錄結構的相關資訊保留在 [目錄資料表](directory-table.md)中。 請參閱 [核心資料表群組](core-tables-group.md)。 在本節中，您會將「記事本」範例的目錄結構資訊新增至您在匯 [入空白資料庫](importing-a-blank-database.md)時所建立的空資料庫。 使用 SDK 或其他編輯器提供的資料庫編輯器 Orca，在 MNP2000.msi 中開啟目錄資料表。 使用編輯器，將下列資料輸入到空白目錄資料表中。

[目錄資料表](directory-table.md)



| 目錄                                        | 目錄 \_ 父系                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| ARTSDIR                                          | NOTEPADDIR                                       | 藝術：活動       |
| HOLDIR                                           | MONDIR                                           | .：假日        |
| MENUDIR                                          | NOTEPADDIR                                       | 功能表              |
| MONDIR                                           | NOTEPADDIR                                       | 門              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | 紅色 \_ 公園：記事本 |
| SPORTDIR                                         | NOTEPADDIR                                       | 運動：活動     |



 

將此資料輸入目錄資料表中，會指定來源和目標目錄結構。 請參閱 [目錄表格](directory-table.md) ，並 [使用目錄資料表](using-the-directory-table.md) 主題。 請注意， [**TARGETDIR**](targetdir.md) 屬性必須是每個安裝的目錄資料表中一個根項目的名稱。

[繼續](specifying-components.md)

 

 



