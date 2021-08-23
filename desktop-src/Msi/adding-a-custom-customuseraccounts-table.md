---
description: 範例的規格是從安裝資料庫中的自訂資料表讀取使用者帳戶資訊，而不是硬式編碼為自訂動作。
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: 新增自訂 CustomUserAccounts 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede08ad733e2870e970416da3de345bfc89b7e63147bc848f3d36ffe66721585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066458"
---
# <a name="adding-a-custom-customuseraccounts-table"></a>新增自訂 CustomUserAccounts 資料表

範例的規格是從安裝資料庫中的自訂資料表讀取使用者帳戶資訊，而不是硬式編碼為自訂動作。

將自訂資料表新增至名為 CustomUserAccounts 的範例安裝資料庫，以保存使用者帳戶資訊。 如需如何加入自訂資料表的範例，請參閱[使用 SQL 和腳本的資料庫查詢範例](examples-of-database-queries-using-sql-and-script.md)。 針對 CustomUserAccounts 資料表使用下列架構。 如需資料行類型的說明，請參閱資料 [行定義格式](column-definition-format.md) 。



| Column     | 類型 | 答案 | Nullable | 描述                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserName   | s72  | Y   | N        | 正在建立之使用者帳戶的名稱。                                                                                                                                                                                                                                                                        |
| 密碼   | s72  |     | N        | 包含帳戶密碼的屬性名稱。 這是在命令列上或透過使用者介面中的[編輯控制項](edit-control.md)設定的[公用屬性](public-properties.md)。 此編輯控制項應具有 [密碼控制項屬性](password-control-attribute.md)。 |
| 屬性 | i4   |     | Y        | 帳戶的屬性。 這些會定義為 \_ 使用者 \_ 資訊1結構之 usri1 旗標成員的 DWORD 值 \_ 。                                                                                                                                                                              |



 

將 CustomUserAccounts 資料表加入至資料庫之後，您可以使用 Orca、Windows Installer SDK 提供的資料表編輯器或其他編輯器來編輯此資料表。 在 CustomUserAccounts 資料表中輸入下列記錄，為名為 TestUser 的使用者建立密碼安全的使用者帳戶。 請注意，512是 UF \_ 標準帳戶的數值 \_ 。

CustomUserAccounts 資料表



| UserName | 密碼         | 屬性 |
|----------|------------------|------------|
| TestUser | TESTUSERPASSWORD | 512        |



 

將下列記錄加入 \_ 自訂資料表的驗證資料表中。

[\_驗證資料表](-validation-table.md)



| 資料表              | 資料行     | Nullable | MinValue | MaxValue   | KeyTable | KeyColumn | 類別                     | 集合 | 描述 |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| CustomUserAccounts | 使用者名稱   | N        |          |            |          |           | [Text](text.md)             |     |             |
| CustomUserAccounts | 密碼   | N        |          |            |          |           | [識別碼](identifier.md) |     |             |
| CustomUserAccounts | 屬性 | Y        | 0        | 2147483647 |          |           | null                         |     |             |



 

繼續 [撰寫 ActionText 和錯誤資料表](authoring-the-actiontext-and-error-tables.md)。

 

 



