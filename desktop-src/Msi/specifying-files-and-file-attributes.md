---
description: 每個檔案的安裝和移除都是由控制檔案的 Windows Installer 元件所決定。
ms.assetid: 6f84bf57-2c68-4f37-b9cd-eee3a657e7cd
title: 指定檔案和檔案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719dacbc434d47b4074a183e67edb02a88cb3c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983584"
---
# <a name="specifying-files-and-file-attributes"></a>指定檔案和檔案屬性

每個檔案的安裝和移除都是由控制檔案的 [Windows Installer 元件](windows-installer-components.md) 所決定。 一旦指定了資源群組至元件之後，就可以將檔案屬性資訊新增至安裝資料庫。 在本節中，您會將檔案資訊新增至「記事本」範例的安裝資料庫。 請參閱檔案 [資料表群組](file-tables-group.md)。

記事本範例中的檔案未壓縮。 請參閱 [壓縮和未壓縮的來源](compressed-and-uncompressed-sources.md) ，以取得如何將封包檔新增至套件的相關資訊。 這個範例不包含檔案版本設定資訊。 如需檔案版本控制的詳細資訊，請參閱檔案 [版本控制規則](file-versioning-rules.md) 和 [預設檔案版本控制](default-file-versioning.md)。

使用資料庫編輯器開啟 MNP2000.msi，並將下列資料輸入空白檔案資料表中。

[FileTable](file-table.md)



| 檔案         | 元件\_ | FileName     | FileSize | 版本 | 語言 | 屬性 | 順序 |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | 棒球    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | 演唱會     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | 舞蹈       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | 足球    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Help        | Help.txt     | 1000     |         |          | 0          | 1        |
| January.txt  | 一月     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | [記事本]     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | [記事本]     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[繼續](specifying-source-media.md)

 

 



