---
description: 因為升級會更新應用程式所使用的檔案，所以您必須修改資料庫的檔案資料表。
ms.assetid: 65a7ae86-b426-4dd4-8cf5-f905dc2a1727
title: 更新升級的檔案和檔案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c56560432a18746b31e3bb983be1f465199c51b15601c3dfd47911fe7f6ab4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809888"
---
# <a name="updating-files-and-file-attributes-for-an-upgrade"></a>更新升級的檔案和檔案屬性

因為升級會更新應用程式所使用的檔案，所以您必須修改資料庫的檔案 [資料表](file-table.md) 。 使用 SDK 所提供的資料庫編輯器 Orca，或使用其他編輯器開啟 MNP2001.msi，並在檔案 [資料表](file-table.md)中輸入下列資料。

[FileTable](file-table.md)



| 檔案         | 元件\_ | FileName     | FileSize | 版本 | 語言 | 屬性 | 順序 |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseba01.txt | 棒球    | Baseba01.txt | 1000     |         |          | 0          | 1        |
| Concer01.txt | 演唱會     | Concer01.txt | 1000     |         |          | 0          | 1        |
| Dance01.txt  | 舞蹈       | Dance01.txt  | 1000     |         |          | 0          | 1        |
| Opera01.txt  | Opera       | Opera01.txt  | 1000     |         |          | 0          | 1        |
| Footba01.txt | 足球    | Footba01.txt | 1000     |         |          | 0          | 1        |
| Basket01.txt | 籃球  | Basket01.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | 說明        | Help.txt     | 1000     |         |          | 0          | 1        |
| Januar01.txt | 一月     | Januar01.txt | 1000     |         |          | 0          | 1        |
| NewYea01.txt | NewYears    | NewYea01.txt | 1000     |         |          | 0          | 1        |
| Memori01.txt | 紀念    | Memori01.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | [記事本]     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | [記事本]     | Readme.txt   | 1000     |         |          | 0          | 1        |



 

[繼續](updating-components-for-an-upgrade.md)

 

 



