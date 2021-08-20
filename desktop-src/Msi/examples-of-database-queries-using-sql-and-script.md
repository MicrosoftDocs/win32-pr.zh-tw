---
description: 使用腳本驅動的資料庫查詢的範例，可在 Windows Installer 軟體發展工具組 (SDK) 中提供作為公用程式 WiRunSQL.vbs。
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: 使用 SQL 和腳本的資料庫查詢範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137927ba47c4fae5eef4534b7dfab1fa5c8fa1af2ba28d27669cc4605f836b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947053"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a>使用 SQL 和腳本的資料庫查詢範例

Windows[安裝程式軟體發展工具組](platform-sdk-components-for-windows-installer-developers.md)中提供使用腳本驅動資料庫查詢的範例 (SDK) 作為公用程式 WiRunSQL.vbs。 此公用程式會使用[SQL 語法](sql-syntax.md)一節中所述的 Windows Installer 版本 SQL 來處理資料庫查詢。

**從資料表中刪除記錄**

下列命令列將從 Test.msi 資料庫的 [功能](feature-table.md) 資料表中，刪除具有主鍵 RED 的記錄。

**Cscript WiRunSQL.vbs Test.msi」功能的 [刪除] \` \` \` \` 。 \`Feature \` = ' RED ' "**

**將資料表加入至資料庫**

下列命令列將 [目錄](directory-table.md) 資料表新增至 Test.msi 資料庫。

**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` directory \` (\` directory \` CHAR (72) NOT Null、 \` Directory \_ Parent \` char (72) 、 \` DEFAULTDIR \` CHAR (255) NOT Null 可當地語系化的 PRIMARY KEY \` Directory \`) "**

**從資料庫中移除資料表**

下列命令列將從 Test.msi 資料庫移除 [功能](feature-table.md) 資料表。

**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \` Feature \` "**

**將新資料行加入至資料表**

下列命令列會將測試資料行加入 Test.msi 資料庫的 [CustomAction](customaction-table.md) 資料表中。

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` CustomAction \` ADD \` Test \` INTEGER"**

**在資料表中插入新的記錄**

下列命令列將新記錄插入 Test.msi 資料庫的 [功能](feature-table.md) 資料表中。

**Cscript WiRunSQL.vbs Test.msi 「插入 \` 功能 \` (\` 功能 \` 。 \`功能 \` \` \` 。 \`功能 \_ 父系 \` 、 \` 功能 \` 。 \`標題 \` 、 \` 功能 \` 。 \`描述 \` ， \` 功能 \` 。 \`顯示 \` 、 \` 功能 \` 。 \`層級 \` 、 \` 功能 \` 。 \`目錄 \_ \` 、 \` 功能 \` 。 \`屬性 \`) 值 ( 「網球」、「運動」、「網球」、「聯賽」、25、3、「SPORTDIR」、2) 」**

這會將下列記錄插入 Test.msi 的 [功能](feature-table.md) 資料表中。

[功能](feature-table.md) 表



| 功能 | 功能 \_ 父系 | 標題  | 描述 | 顯示 | 層級 | 目錄\_ | 屬性 |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| 網球  | 運動項目           | 網球 | 比賽  | 25      | 3     | SPORTDIR    | 2          |



 

請注意，二進位資料無法使用 INSERT into 或 UPDATE SQL 查詢，直接插入資料表中。 如需詳細資訊，請參閱[使用 SQL 將二進位資料加入至資料表](adding-binary-data-to-a-table-using-sql.md)。

**修改資料表中的現有記錄**

下列命令列將 [標題] 欄位中的現有值變更為 [效能]。 更新的記錄會以 "藝術" 作為其主鍵，而且位於 Test.msi 資料庫的功能資料表中。

**Cscript WiRunSQL.vbs Test.msi 「更新 \` 功能 \` 集」 \` 功能 \` 。 \`Title \` = 功能的「效能 \` 」 \` 。 \`Feature \` = ' 藝術 ' "**

**選取一組記錄**

下列命令列會選取屬於 Test.msi 資料庫中 ErrorDialog 之所有控制項的名稱和類型。

**CScript WiRunSQL.vbs Test.msi 選取 \` 控制項 \` ，然後 \` \` \` \` 在 \` 對話方塊 \_ \` = ' ErrorDialog ' 的控制項中輸入**

**將資料表放入記憶體中**

下列命令列將鎖定記憶體中 Test.msi 資料庫的 [元件](component-table.md) 資料表。

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` HOLD"**

**釋放記憶體中的資料表**

下列命令列將從記憶體釋放 Test.msi 資料庫的 [元件](component-table.md) 資料表。

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` FREE"**

 

 



