---
description: SFPCatalog 資料表包含 Windows Me 使用的目錄。
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: SFPCatalog 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe887644faf6cf0a5cda626bbf757e9f448ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191602"
---
# <a name="sfpcatalog-table"></a>SFPCatalog 資料表

SFPCatalog 資料表包含 Windows Me 使用的目錄。

SFPCatalog 資料表具有下列資料行。



| Column     | 類型                       | 答案 | Nullable |
|------------|----------------------------|-----|----------|
| SFPCatalog | [檔案名稱](filename.md)   | Y   | N        |
| 目錄    | [二進位](binary.md)       | N   | N        |
| 相依性 | [格式 化](formatted.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog
</dt> <dd>

目錄的簡短檔案名。 因為目錄沒有版本，所以在此資料行中指定的目錄可以覆寫具有相同名稱且已安裝在本機系統上的目錄。 請參閱檔案版本設定主題， [這兩個檔案都沒有版本](neither-file-has-a-version.md)。

</dd> <dt>

<span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>目錄
</dt> <dd>

目錄的二進位資料。

</dd> <dt>

<span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>依賴
</dt> <dd>

此欄位中指定的目錄是 SFPCatalog 欄位中指定之相依目錄的父系。 在 [相依性] 欄位中輸入父目錄的簡短檔案名。 此欄位是回 SFPCatalog 資料行的索引鍵。 相依性相符會區分大小寫。

如果相依性欄位參考此 SFPCatalog 資料表中的另一筆記錄，則會在相依目錄之前安裝父目錄。

如果相依性欄位參考的父類別目錄不在此資料表的 SFPCatalog 欄位中，而且如果尚未安裝父目錄，則安裝會失敗。

</dd> </dl>

## <a name="remarks"></a>備註

[InstallSFPCatalogFile 動作](installsfpcatalogfile-action.md)會查詢[Component 資料表](component-table.md)、 [File Table](file-table.md)、 [FileSFPCatalog table](filesfpcatalog-table.md)和 SFPCatalog 資料表。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
</dl>

 

 



