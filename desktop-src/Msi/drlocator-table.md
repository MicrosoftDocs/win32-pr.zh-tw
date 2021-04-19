---
description: DrLocator 資料表會透過搜尋目錄樹狀結構，來保存尋找檔案或目錄所需的資訊。
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: DrLocator 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78df5a5af83a18a14027b88033e977b2c63d2027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967170"
---
# <a name="drlocator-table"></a>DrLocator 資料表

DrLocator 資料表會透過搜尋目錄樹狀結構，來保存尋找檔案或目錄所需的資訊。

DrLocator 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 簽名\_ | [識別碼](identifier.md) | Y   | N        |
| 父代      | [識別碼](identifier.md) | Y   | Y        |
| 路徑        | [AnyPath](anypath.md)       | Y   | Y        |
| 深度       | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>簽名\_
</dt> <dd>

簽章資料 \_ 行是簽章 [資料表](signature-table.md)第一個資料行的外部索引鍵。 此欄位可能代表簽章資料表中所列的唯一檔案簽章。 如果此資料行中的值不存在於簽章資料表中，則會假設搜尋是針對 DrLocator 資料表所指向的目錄。

</dd> <dt>

<span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>父母
</dt> <dd>

此資料行是簽章資料行中檔案或目錄之父目錄的簽章 \_ 。 如果此欄位為 null，而且 [路徑] 資料行沒有展開至完整路徑，則會使用路徑來搜尋使用者系統的所有固定磁片磁碟機。

此欄位是下列其中一個資料表的索引鍵： [RegLocator](reglocator-table.md)、 [IniLocator](inilocator-table.md)、 [CompLocator](complocator-table.md)或 DrLocator 資料表。

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>路徑
</dt> <dd>

[路徑] 資料行包含使用者系統上的路徑。 這是在父資料行中指定的目錄下方的完整路徑或相對子路徑。 請參閱 [AnyPath](anypath.md) 資料類型的限制。

</dd> <dt>

<span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>深度
</dt> <dd>

在安裝程式搜尋簽章資料行中所指定之檔案或目錄的路徑下方的深度 \_ 。 [深度] 欄位中所使用的值是以零為基礎。 例如，如果 [路徑] 欄位是 [c：/Program Files/bin]，則 [深度] 欄必須設定為0或更大，才能偵測位於資料夾 bin 內的檔案。 如果 [深度] 欄位是空的，則會假設深度為零。

</dd> </dl>

## <a name="remarks"></a>備註

此資料表與 [AppSearch 資料表](appsearch-table.md)搭配使用。

此資料表的資料行通常不會當地語系化。 如果作者決定要搜尋多種語言的產品，則每種語言的表格中都必須包含個別的專案。

請參閱 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



